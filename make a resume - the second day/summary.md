# 第二天ife 验证总结
***
##1. HTML是什么，HTML5是什么？

**HTML是什么:**

> 超文本标记语言  (英语：Hypertext Markup Language，简称：HTML)  是一种用来结构化Web网页及其内容的标记语言。
HTML 不是一种编程语言，而是一种标记语言 (markup language)
标记语言是一套标记标签 (markup tag)
HTML 使用标记标签来描述网页
HTML 文档 = 网页

**HTML5是什么:**

> HTML5 是最新的 HTML 标准。
HTML5 是专门为承载丰富的 web 内容而设计的，并且无需额外插件。
HTML5 拥有新的语义、图形以及多媒体元素。
HTML5 提供的新元素和新的 API 简化了 web 应用程序的搭建。
HTML5 是跨平台的，被设计为在不同类型的硬件（PC、平板、手机、电视机等等）之上运行。

* * *

##2. HTML元素标签、属性都是什么概念？
**HTML元素标签:**

> HTML 文档是由 HTML 元素定义的（由许许多多的HTML元素构成文本文件），HTML元素就是通过使用HTML标签进行定义的。 
标签就是诸如`<head>`、`<body>`等被尖括号“<”和“>”包起来的对象，绝大部分的标签都是成对出现的，如`<table></talbe>、<form></form>`。当然还有少部分不是成对出现的，如`<br>、<hr>`等。 
位于起始标签和结束标签之间的文本就是HTML元素的内容。

**HTML元素属性:**

> 为HTML元素提供各种附加信息的就是HTML属性，它总是以"属性名=属性值"这种名值对的形式出现，而且属性总是在HTML元素的开始标签中进行定义。

* * *
##3. 文档类型是什么概念，起什么作用？

文档类型个人理解为Doctype,如我们现在写html5要用到的`<!DOCTYPE html>`一样，主要作用是说明文档设计所用的类型，html或者xhtml，能够让浏览器按照指定的规则去解释文档中的标记标签。
总之，doctype使浏览器按照dtd指定的渲染方式对页面进行渲染。

* * *

##4.meta标签都用来做什么的？

**元数据：`<meta>`元素**
> 用来构建HTML文档的基本结构，以及就如何处理文档向浏览器提供信息和指示，它们本身不是文档内容，但提供了关于后面文档内容的信息。——出自《html5权威指南》。

**具体用途:**

`<meta>`元素除去charset属性外，都是http-equiv属性或name属性结合content来使用

```
1. 指定名/值对定义元数据

<meta name="参数" content="具体描述信息">

　　这里可以添加作者和描述
　　　如
        <meta name="keywords" content="电商,物流">
        <meta name="author" content="张三">
        <meta name="description" content="网站描述...">
　　这些信息能被搜索引擎及爬虫等捕捉。

2. 声明字符编码

　　如 <meta charset="utf-8">

3. 模拟http标头字段

　　如 <meta http-equiv="参数" content="具体的描述"> 

　　具体详细功能暂不描述。

　　笔记来自 令狐寻欢 的 meta笔记
```
* * *

##5. Web语义化是什么，是为了解决什么问题?

个人理解 web 语义化 主要是使用正确的html标签，html标签设计的时候本来每个标签都为之赋予了相应的语义，语义化良好的应用在于，能够让别人打开你设计的html文档能够大概知道每个标签使用的意义，不至于一头雾水。

同时 良好的语义化使用 ，能够使我们的机器（如搜索引擎，网络爬虫等）能够更好的理解文档中的内容，使用有意义的标签 如 `<header> <footer> <nav>`等 而不是一味的滥用`<div>`。

* * *

##6.链接是什么概念，对应什么标签？

链接可以使我们的文档与任何其他文档（或其他资源）相连，也可以链接到文档的指定部分。

对应了 html的 `<a>`标签。

有两种使用 `<a>` 标签的方式：

通过使用 href 属性 - 创建指向另一个文档的链接
通过使用 name 属性 - 创建文档内的书签

个人理解，部分其他标签也有类似于链接的作用 如 `<img>`通过 `<img src="url">`来链接图像，通过`<link rel="stylesheet" href="style.css">`来链接css文件, 通过`<script type="text/javascript" src="url">`来链接js文件等。

* * * 

##7.常用标签都有哪些，都适合用在什么场景

总结起来太多 暂时略过 orz

* * * 

##8.表单标签都有哪些，对应着什么功能，都有哪些属性

**表单标签`<form>`**

`<form>` 标签用于为用户输入创建 HTML 表单。

表单能够包含 input 元素，比如文本字段、复选框、单选框、提交按钮等等。

表单还可以包含 menus、textarea、fieldset、legend 和 label 元素。

表单用于向服务器传输数据。

功能及属性详情见[w3school表单](http://www.w3school.com.cn/tags/tag_form.asp).,

* * *

##9.ol, ul, li, dl, dd, dt等这些标签都适合用在什么地方，举个例子

1. - ol有序列表标签,创建一个有序的列表，默认会在列项目前添加序号。
   - ul无序列表标签，创建一个无序的列表，对比ol就是没有项目前有序的序号。
   - li 对应了ul ol 中的列项目
   ol ul li可以应用在一套列表中，如一堆图标组， 一个排行榜列表等。
2. - dl dd dt
　　dl dd dt对应了一套自定义的列表
	用dl创建对应列表 dt dd 分别对应列表中的两个项目， 可以用于 一个标题(dt) + 一个描述(dd)，曾经在人物图片+对应描述用到过dl dd dt

做过一个小demo 创建了一个静态html页面 用于练习html标签的使用，里面就用到了 ul + li 以及 dl dt dd 详情见我的[github项目](https://github.com/fncZy/iMooc-test/tree/master/Html5%E6%A0%87%E7%AD%BE%E6%9E%84%E5%BB%BA%E9%A1%B5%E9%9D%A2%E7%BB%83%E4%B9%A0).,
