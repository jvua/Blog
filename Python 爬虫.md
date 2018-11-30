爬虫前奏： 

明确目的

找到数据对应的网页

分析网页的结构找到数据所在的标签位置

模拟 HTTP 请求，向服务器发送这个请求，获取到服务器返回给我们的 HTML ，用正则表达式提取我们要的数据

urlparse 多一个 params 属性

代理的原理：在请求目的网址之前，先请求代理服务器，然后让代理服务器去请求目的网站，代理服务器拿到目的网站的数据后，在转发给我们的代码。

request 库，默认会使用自己猜测的编码方式将抓取下来的网页进行解码，然后存储到 text 属性上去

find_all 的使用：

- 在提取标签的时候，第一个参数是标签的名字。如果在提取标签的时候想要使用标签属性进行过滤，那么可以在这个方法中通过关键字参数的形式，将属性的名字以及对应的值传进去，或者是使用`attrs`属性，将所有的属性以及对应的值放在一个字典中传给`attrs`属性。
- 有些时候，在提取标签的时候，不想提取那么多，那么可以使用`limit`参数，限制提取个数。

BeautifulSoup 中使用 css 选择器：

在`BeautifulSoup`中，要使用 css 选择器，那么应该使用`soup.select()`方法，应该传递一个 css 选择器的字符串给 select 方法。

`*` 匹配 0 个或多个字符

`+` 匹配 1 个或多个字符

`?` 匹配 1 个或 0 个

## Request 与 Response

- 浏览器发送消息给该网址所在的服务器，这个过程叫做 HTTP Request。
- 服务器收到浏览器发送的消息后，能够根据浏览器发送消息的内容，做相应处理，然后把消息回传给浏览器。这个过程叫做 HTTP Response。
- 浏览器收到服务器的 Response 信息后，会对信息进行相应处理，然后展示。

## 怎样解决 JavaScript 渲染的问题？

- 分析 Ajax 请求
- Selenium/WebDriver
- Splash
- PyV8、Ghost.py

## 怎样保存数据？

- 文本
- 关系型数据库
- 非关系型数据库
- 二进制文件

 ## 什么是 Urllib

- Python 内置的 HTTP 请求库
- urllib.request 请求模块
- urllib.error 异常处理模块
- urllib.parse url 解析模块
- urllib.robotparser robots.txt 解析模块