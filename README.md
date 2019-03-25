> 源地址为https://yuchengkai.cn/docs/ fork自https://github.com/InterviewMap/CS-Interview-Knowledge-Map
>
> 作者：[InterviewMap](https://github.com/InterviewMap/CS-Interview-Knowledge-Map)
>
> 授权：[署名-非商用许可证](http://creativecommons.org/licenses/by-nc/4.0/)

## ⛏JS

- [内置类型](/JS/JS-ch.md#%E5%86%85%E7%BD%AE%E7%B1%BB%E5%9E%8B)
- [Typeof](/JS/JS-ch.md#typeof)
- [类型转换](/JS/JS-ch.md#%E7%B1%BB%E5%9E%8B%E8%BD%AC%E6%8D%A2)
  - [转Boolean](/JS/JS-ch.md#%E8%BD%ACboolean)
  - [对象转基本类型](/JS/JS-ch.md#%E5%AF%B9%E8%B1%A1%E8%BD%AC%E5%9F%BA%E6%9C%AC%E7%B1%BB%E5%9E%8B)
  - [四则运算符](/JS/JS-ch.md#%E5%9B%9B%E5%88%99%E8%BF%90%E7%AE%97%E7%AC%A6)
  - [`==` 操作符](/JS/JS-ch.md#-%E6%93%8D%E4%BD%9C%E7%AC%A6)
  - [比较运算符](/JS/JS-ch.md#%E6%AF%94%E8%BE%83%E8%BF%90%E7%AE%97%E7%AC%A6)
- [原型](/JS/JS-ch.md#%E5%8E%9F%E5%9E%8B)
- [new](/JS/JS-ch.md#new)
- [instanceof](/JS/JS-ch.md#instanceof)
- [this](/JS/JS-ch.md#this)
- [执行上下文](/JS/JS-ch.md#%E6%89%A7%E8%A1%8C%E4%B8%8A%E4%B8%8B%E6%96%87)
- [闭包](/JS/JS-ch.md#%E9%97%AD%E5%8C%85)
- [深浅拷贝](/JS/JS-ch.md#%E6%B7%B1%E6%B5%85%E6%8B%B7%E8%B4%9D)
  - [浅拷贝](/JS/JS-ch.md#%E6%B5%85%E6%8B%B7%E8%B4%9D)
  - [深拷贝](/JS/JS-ch.md#%E6%B7%B1%E6%8B%B7%E8%B4%9D)
- [模块化](/JS/JS-ch.md#%E6%A8%A1%E5%9D%97%E5%8C%96)
  - [CommonJS](/JS/JS-ch.md#commonjs)
  - [AMD](/JS/JS-ch.md#amd)
- [防抖](/JS/JS-ch.md#%E9%98%B2%E6%8A%96)
- [节流](/JS/JS-ch.md#%E8%8A%82%E6%B5%81)
- [继承](/JS/JS-ch.md#%E7%BB%A7%E6%89%BF)
- [call, apply, bind 区别](/JS/JS-ch.md#call-apply-bind-%E5%8C%BA%E5%88%AB)
  - [模拟实现 call 和 apply](/JS/JS-ch.md#%E6%A8%A1%E6%8B%9F%E5%AE%9E%E7%8E%B0-call-%E5%92%8C-apply)
- [Promise 实现](/JS/JS-ch.md#promise-%E5%AE%9E%E7%8E%B0)
- [Generator 实现](/JS/JS-ch.md#generator-%E5%AE%9E%E7%8E%B0)
- [Map、FlatMap 和 Reduce](/JS/JS-ch.md#mapflatmap-%E5%92%8C-reduce)
- [async 和 await](/JS/JS-ch.md#async-%E5%92%8C-await)
- [Proxy](/JS/JS-ch.md#proxy)
- [为什么 0.1 + 0.2 != 0.3](/JS/JS-ch.md#%E4%B8%BA%E4%BB%80%E4%B9%88-01--02--03)
- [正则表达式](/JS/JS-ch.md#%E6%AD%A3%E5%88%99%E8%A1%A8%E8%BE%BE%E5%BC%8F)
  - [元字符](/JS/JS-ch.md#%E5%85%83%E5%AD%97%E7%AC%A6)
  - [修饰语](/JS/JS-ch.md#%E4%BF%AE%E9%A5%B0%E8%AF%AD)
  - [字符简写](/JS/JS-ch.md#%E5%AD%97%E7%AC%A6%E7%AE%80%E5%86%99)
- [V8 下的垃圾回收机制](/JS/JS-ch.md#v8-%E4%B8%8B%E7%9A%84%E5%9E%83%E5%9C%BE%E5%9B%9E%E6%94%B6%E6%9C%BA%E5%88%B6)
  - [新生代算法](/JS/JS-ch.md#%E6%96%B0%E7%94%9F%E4%BB%A3%E7%AE%97%E6%B3%95)
  - [老生代算法](/JS/JS-ch.md#%E8%80%81%E7%94%9F%E4%BB%A3%E7%AE%97%E6%B3%95)

## 🌍浏览器

- [事件机制](Browser/browser-ch.md#%E4%BA%8B%E4%BB%B6%E6%9C%BA%E5%88%B6)
  - [事件触发三阶段](Browser/browser-ch.md#%E4%BA%8B%E4%BB%B6%E8%A7%A6%E5%8F%91%E4%B8%89%E9%98%B6%E6%AE%B5)
  - [注册事件](Browser/browser-ch.md#%E6%B3%A8%E5%86%8C%E4%BA%8B%E4%BB%B6)
  - [事件代理](Browser/browser-ch.md#%E4%BA%8B%E4%BB%B6%E4%BB%A3%E7%90%86)
- [跨域](Browser/browser-ch.md#%E8%B7%A8%E5%9F%9F)
  - [JSONP](Browser/browser-ch.md#jsonp)
  - [CORS](Browser/browser-ch.md#cors)
  - [document.domain](Browser/browser-ch.md#documentdomain)
  - [postMessage](Browser/browser-ch.md#postmessage)
- [Event loop](Browser/browser-ch.md#event-loop)
  - [Node 中的 Event loop](Browser/browser-ch.md#node-%E4%B8%AD%E7%9A%84-event-loop)
    - [timer](Browser/browser-ch.md#timer)
    - [I/O](Browser/browser-ch.md#io)
    - [idle, prepare](Browser/browser-ch.md#idle-prepare)
    - [poll](Browser/browser-ch.md#poll)
    - [check](Browser/browser-ch.md#check)
    - [close callbacks](Browser/browser-ch.md#close-callbacks)
- [存储](Browser/browser-ch.md#%E5%AD%98%E5%82%A8)
  - [cookie，localStorage，sessionStorage，indexDB](Browser/browser-ch.md#cookielocalstoragesessionstorageindexdb)
  - [Service Worker](Browser/browser-ch.md#service-worker)
- [渲染机制](Browser/browser-ch.md#%E6%B8%B2%E6%9F%93%E6%9C%BA%E5%88%B6)
  - [Load 和 DOMContentLoaded 区别](Browser/browser-ch.md#load-%E5%92%8C-domcontentloaded-%E5%8C%BA%E5%88%AB)
  - [图层](Browser/browser-ch.md#%E5%9B%BE%E5%B1%82)
  - [重绘（Repaint）和回流（Reflow）](Browser/browser-ch.md#%E9%87%8D%E7%BB%98repaint%E5%92%8C%E5%9B%9E%E6%B5%81reflow)
  - [减少重绘和回流](Browser/browser-ch.md#%E5%87%8F%E5%B0%91%E9%87%8D%E7%BB%98%E5%92%8C%E5%9B%9E%E6%B5%81)

## 💡性能

- [网络相关](Performance/performance-ch.md#%E7%BD%91%E7%BB%9C%E7%9B%B8%E5%85%B3)
  - [DNS 预解析](Performance/performance-ch.md#dns-%E9%A2%84%E8%A7%A3%E6%9E%90)
  - [缓存](Performance/performance-ch.md#%E7%BC%93%E5%AD%98)
    - [强缓存](Performance/performance-ch.md#%E5%BC%BA%E7%BC%93%E5%AD%98)
    - [协商缓存](Performance/performance-ch.md#%E5%8D%8F%E5%95%86%E7%BC%93%E5%AD%98)
      - [Last-Modified 和 If-Modified-Since](Performance/performance-ch.md#last-modified-%E5%92%8C-if-modified-since)
      - [ETag 和 If-None-Match](Performance/performance-ch.md#etag-%E5%92%8C-if-none-match)
    - [选择合适的缓存策略](Performance/performance-ch.md#%E9%80%89%E6%8B%A9%E5%90%88%E9%80%82%E7%9A%84%E7%BC%93%E5%AD%98%E7%AD%96%E7%95%A5)
  - [使用 HTTP / 2.0](Performance/performance-ch.md#%E4%BD%BF%E7%94%A8-http--20)
  - [预加载](Performance/performance-ch.md#%E9%A2%84%E5%8A%A0%E8%BD%BD)
  - [预渲染](Performance/performance-ch.md#%E9%A2%84%E6%B8%B2%E6%9F%93)
- [优化渲染过程](Performance/performance-ch.md#%E4%BC%98%E5%8C%96%E6%B8%B2%E6%9F%93%E8%BF%87%E7%A8%8B)
  - [懒执行](Performance/performance-ch.md#%E6%87%92%E6%89%A7%E8%A1%8C)
  - [懒加载](Performance/performance-ch.md#%E6%87%92%E5%8A%A0%E8%BD%BD)
- [文件优化](Performance/performance-ch.md#%E6%96%87%E4%BB%B6%E4%BC%98%E5%8C%96)
  - [图片优化](Performance/performance-ch.md#%E5%9B%BE%E7%89%87%E4%BC%98%E5%8C%96)
    - [计算图片大小](Performance/performance-ch.md#%E8%AE%A1%E7%AE%97%E5%9B%BE%E7%89%87%E5%A4%A7%E5%B0%8F)
    - [图片加载优化](Performance/performance-ch.md#%E5%9B%BE%E7%89%87%E5%8A%A0%E8%BD%BD%E4%BC%98%E5%8C%96)
  - [其他文件优化](Performance/performance-ch.md#%E5%85%B6%E4%BB%96%E6%96%87%E4%BB%B6%E4%BC%98%E5%8C%96)
  - [CDN](Performance/performance-ch.md#cdn)
- [其他](Performance/performance-ch.md#%E5%85%B6%E4%BB%96)
  - [使用 Webpack 优化项目](Performance/performance-ch.md#%E4%BD%BF%E7%94%A8-webpack-%E4%BC%98%E5%8C%96%E9%A1%B9%E7%9B%AE)
  - [监控](Performance/performance-ch.md#%E7%9B%91%E6%8E%A7)
  - [面试题](Performance/performance-ch.md#%E9%9D%A2%E8%AF%95%E9%A2%98)

## 🛡安全

- [XSS](Safety/safety-cn.md#xss)
  - [如何攻击](Safety/safety-cn.md#%E5%A6%82%E4%BD%95%E6%94%BB%E5%87%BB)
  - [如何防御](Safety/safety-cn.md#%E5%A6%82%E4%BD%95%E9%98%B2%E5%BE%A1)
  - [CSP](Safety/safety-cn.md#csp)
- [CSRF](Safety/safety-cn.md#csrf)
  - [如何攻击](Safety/safety-cn.md#%E5%A6%82%E4%BD%95%E6%94%BB%E5%87%BB-1)
  - [如何防御](Safety/safety-cn.md#%E5%A6%82%E4%BD%95%E9%98%B2%E5%BE%A1-1)
    - [SameSite](Safety/safety-cn.md#samesite)
    - [验证 Referer](Safety/safety-cn.md#%E9%AA%8C%E8%AF%81-referer)
    - [Token](Safety/safety-cn.md#token)
- [密码安全](Safety/safety-cn.md#%E5%AF%86%E7%A0%81%E5%AE%89%E5%85%A8)
  - [加盐](Safety/safety-cn.md#%E5%8A%A0%E7%9B%90)
## 🎉框架通识

- [MVVM](Framework/framework-zh.md#mvvm)
  - [脏数据检测](Framework/framework-zh.md#%E8%84%8F%E6%95%B0%E6%8D%AE%E6%A3%80%E6%B5%8B)
  - [数据劫持](Framework/framework-zh.md#%E6%95%B0%E6%8D%AE%E5%8A%AB%E6%8C%81)
  - [Proxy 与 Object.defineProperty 对比](Framework/framework-zh.md#proxy-%E4%B8%8E-objectdefineproperty-%E5%AF%B9%E6%AF%94)
- [路由原理](Framework/framework-zh.md#%E8%B7%AF%E7%94%B1%E5%8E%9F%E7%90%86)
- [Virtual Dom](Framework/framework-zh.md#virtual-dom)
  - [为什么需要 Virtual Dom](Framework/framework-zh.md#%E4%B8%BA%E4%BB%80%E4%B9%88%E9%9C%80%E8%A6%81-virtual-dom)
  - [Virtual Dom 算法简述](Framework/framework-zh.md#virtual-dom-%E7%AE%97%E6%B3%95%E7%AE%80%E8%BF%B0)
  - [Virtual Dom 算法实现](Framework/framework-zh.md#virtual-dom-%E7%AE%97%E6%B3%95%E5%AE%9E%E7%8E%B0)
    - [树的递归](Framework/framework-zh.md#%E6%A0%91%E7%9A%84%E9%80%92%E5%BD%92)
    - [判断属性的更改](Framework/framework-zh.md#%E5%88%A4%E6%96%AD%E5%B1%9E%E6%80%A7%E7%9A%84%E6%9B%B4%E6%94%B9)
    - [判断列表差异算法实现](Framework/framework-zh.md#%E5%88%A4%E6%96%AD%E5%88%97%E8%A1%A8%E5%B7%AE%E5%BC%82%E7%AE%97%E6%B3%95%E5%AE%9E%E7%8E%B0)
    - [遍历子元素打标识](Framework/framework-zh.md#%E9%81%8D%E5%8E%86%E5%AD%90%E5%85%83%E7%B4%A0%E6%89%93%E6%A0%87%E8%AF%86)
    - [渲染差异](Framework/framework-zh.md#%E6%B8%B2%E6%9F%93%E5%B7%AE%E5%BC%82)
  - [最后](Framework/framework-zh.md#%E6%9C%80%E5%90%8E)

## 🥈vue

- [NextTick 原理分析](Framework/vue-zh.md#nexttick-%E5%8E%9F%E7%90%86%E5%88%86%E6%9E%90)
- [生命周期分析](Framework/vue-zh.md#%E7%94%9F%E5%91%BD%E5%91%A8%E6%9C%9F%E5%88%86%E6%9E%90)
- [VueRouter 源码解析](Framework/vue-zh.md#vuerouter-%E6%BA%90%E7%A0%81%E8%A7%A3%E6%9E%90)
  - [重要函数思维导图](Framework/vue-zh.md#%E9%87%8D%E8%A6%81%E5%87%BD%E6%95%B0%E6%80%9D%E7%BB%B4%E5%AF%BC%E5%9B%BE)
  - [路由注册](Framework/vue-zh.md#%E8%B7%AF%E7%94%B1%E6%B3%A8%E5%86%8C)
  - [VueRouter 实例化](Framework/vue-zh.md#vuerouter-%E5%AE%9E%E4%BE%8B%E5%8C%96)
  - [创建路由匹配对象](Framework/vue-zh.md#%E5%88%9B%E5%BB%BA%E8%B7%AF%E7%94%B1%E5%8C%B9%E9%85%8D%E5%AF%B9%E8%B1%A1)
  - [路由初始化](Framework/vue-zh.md#%E8%B7%AF%E7%94%B1%E5%88%9D%E5%A7%8B%E5%8C%96)
  - [路由跳转](Framework/vue-zh.md#%E8%B7%AF%E7%94%B1%E8%B7%B3%E8%BD%AC)

## 🏅React

- [React 生命周期分析](Framework/react-zh#react-%E7%94%9F%E5%91%BD%E5%91%A8%E6%9C%9F%E5%88%86%E6%9E%90)
  - [V16 生命周期函数用法建议](Framework/react-zh#v16-%E7%94%9F%E5%91%BD%E5%91%A8%E6%9C%9F%E5%87%BD%E6%95%B0%E7%94%A8%E6%B3%95%E5%BB%BA%E8%AE%AE)
- [setState](Framework/react-zh#setstate)
- [Redux 源码分析](Framework/react-zh#redux-%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90)

<script async src="//jsrun.net/WeXKp/embed/all/light/"></script>

