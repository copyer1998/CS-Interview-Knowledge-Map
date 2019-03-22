# Generator 实现

Generator 是 ES6 中新增的语法，和 Promise 一样，都可以用来异步编程

```js
// 使用 * 表示这是一个 Generator 函数
// 内部可以通过 yield 暂停代码
// 通过调用 next 恢复执行
function* test() {
  let a = 1 + 2;
  yield 2;
  yield 3;
}
let b = test();
console.log(b.next()); // >  { value: 2, done: false }
console.log(b.next()); // >  { value: 3, done: false }
console.log(b.next()); // >  { value: undefined, done: true }
```

从以上代码可以发现，加上 `*` 的函数执行后拥有了 `next` 函数，也就是说函数执行后返回了一个对象。每次调用 `next` 函数可以继续执行被暂停的代码。以下是 Generator 函数的简单实现

```js
// cb 也就是编译过的 test 函数
function generator(cb) {
  return (function() {
    var object = {
      next: 0,
      stop: function() {}
    };

    return {
      next: function() {
        var ret = cb(object);
        if (ret === undefined) return { value: undefined, done: true };
        return {
          value: ret,
          done: false
        };
      }
    };
  })();
}
// 如果你使用 babel 编译后可以发现 test 函数变成了这样
function test() {
  var a;
  return generator(function(_context) {
    while (1) {
      switch ((_context.prev = _context.next)) {
        // 可以发现通过 yield 将代码分割成几块
        // 每次执行 next 函数就执行一块代码
        // 并且表明下次需要执行哪块代码
        case 0:
          a = 1 + 2;
          _context.next = 4;
          return 2;
        case 4:
          _context.next = 6;
          return 3;
		// 执行完毕
        case 6:
        case "end":
          return _context.stop();
      }
    }
  });
}
```

# Map、FlatMap 和 Reduce

`Map` 作用是生成一个新数组，遍历原数组，将每个元素拿出来做一些变换然后 `append` 到新的数组中。

```js
[1, 2, 3].map((v) => v + 1)
// -> [2, 3, 4]
```

`Map` 有三个参数，分别是当前索引元素，索引，原数组

```js
['1','2','3'].map(parseInt)
//  parseInt('1', 0) -> 1
//  parseInt('2', 1) -> NaN
//  parseInt('3', 2) -> NaN
```

`FlatMap` 和 `map` 的作用几乎是相同的，但是对于多维数组来说，会将原数组降维。可以将 `FlatMap` 看成是 `map` + `flatten` ，目前该函数在浏览器中还不支持。

```js
[1, [2], 3].flatMap((v) => v + 1)
// -> [2, 3, 4]
```

如果想将一个多维数组彻底的降维，可以这样实现

```js
const flattenDeep = (arr) => Array.isArray(arr)
  ? arr.reduce( (a, b) => [...a, ...flattenDeep(b)] , [])
  : [arr]

flattenDeep([1, [[2], [3, [4]], 5]])
```

`Reduce` 作用是数组中的值组合起来，最终得到一个值

```js
function a() {
    console.log(1);
}

function b() {
    console.log(2);
}

[a, b].reduce((a, b) => a(b()))
// -> 2 1
```

# async 和 await

一个函数如果加上 `async` ，那么该函数就会返回一个 `Promise`

```js
async function test() {
  return "1";
}
console.log(test()); // -> Promise {<resolved>: "1"}
```

可以把 `async` 看成将函数返回值使用 `Promise.resolve()` 包裹了下。

`await` 只能在 `async` 函数中使用

```js
function sleep() {
  return new Promise(resolve => {
    setTimeout(() => {
      console.log('finish')
      resolve("sleep");
    }, 2000);
  });
}
async function test() {
  let value = await sleep();
  console.log("object");
}
test()
```

上面代码会先打印 `finish` 然后再打印 `object` 。因为 `await` 会等待 `sleep` 函数 `resolve` ，所以即使后面是同步代码，也不会先去执行同步代码再来执行异步代码。

`async 和 await` 相比直接使用 `Promise` 来说，优势在于处理 `then` 的调用链，能够更清晰准确的写出代码。缺点在于滥用 `await` 可能会导致性能问题，因为 `await` 会阻塞代码，也许之后的异步代码并不依赖于前者，但仍然需要等待前者完成，导致代码失去了并发性。

下面来看一个使用 `await` 的代码。

```js
var a = 0
var b = async () => {
  a = a + await 10
  console.log('2', a) // -> '2' 10
  a = (await 10) + a
  console.log('3', a) // -> '3' 20
}
b()
a++
console.log('1', a) // -> '1' 1
```

对于以上代码你可能会有疑惑，这里说明下原理

- 首先函数 `b` 先执行，在执行到 `await 10` 之前变量 `a` 还是 0，因为在 `await` 内部实现了 `generators` ，`generators` 会保留堆栈中东西，所以这时候 `a = 0` 被保存了下来
- 因为 `await` 是异步操作，遇到`await`就会立即返回一个`pending`状态的`Promise`对象，暂时返回执行代码的控制权，使得函数外的代码得以继续执行，所以会先执行 `console.log('1', a)`
- 这时候同步代码执行完毕，开始执行异步代码，将保存下来的值拿出来使用，这时候 `a = 10`
- 然后后面就是常规执行代码了