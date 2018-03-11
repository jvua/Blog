# JavaScript 笔记

##### JavaScript 作用域链？

```
全局函数无法查看局部函数的内部细节，但局部函数可以查看其上层的函数细节，直至全局细节。
当需要从局部函数查找某一属性或方法时，如果当前作用域没有找到，就会上溯到上层作用域查找，直至全局函数，这种组织形式就是作用域链。
```

##### 什么是 Polyfill？

```
polyfill 是“在旧版浏览器上复制标准 API 的 JavaScript 补充”，可以动态地加载 JavaScript 代码或库，在不支持这些标准 API 的浏览器中模拟它们。
```

##### 谈谈 This 对象的理解。

```
this 总是指向函数的直接调用者（而非间接调用者）；
如果有 new 关键字，this 指向 new 出来的那个对象；
在事件中，this 指向触发这个事件的对象，特殊的是，IE 中的 attachEvent 中的 this 总是指向全局对象 Window；
```

##### 什么是 Window 对象？什么是 Document 对象？

```
Window 对象表示浏览器🀄️打开的窗口。
每个载入浏览器的 HTML 文档都会成为 Document 对象。
Document 对象使我们可以从脚本🀄️对 HTML 页面🀄️的所有元素进行访问。
提示：Document 对象是 Window 对象的一部分，可通过 window.document 属性对其进行访问。
```
##### Undefinde 类型

- 在使用 var 声明变量但未对其加以初始化时，这个变量就是 undefined。

