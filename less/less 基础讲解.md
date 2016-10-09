title: html 基本介绍
speaker: zhouwenyong
url: https://github.com/ksky521/nodePPT
transition: slide3
files: /js/demo.js,/css/demo.css

[slide]

# HTML 介绍
## 分享人：周文勇

# HTML基本概念

[slide]

## 什么是HTML 
----
* HTML的英文全称是Hypertext Marked Language，中文叫做“超文本标记语言” {:&.rollIn}
* 和一般文本的不同的是，一个HTML文件不仅包含文本内容，还包含一些Tag，中文称“标记”
* 一个HTML文件的后缀名是.htm或者是.html

[slide]

## 示例 
----

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8" />
	<title>Document</title>
</head>
<body>
	This is my first homepage. <b>This text is bold</b>
</body>
</html>
```

​	

[slide]

## 示例解释
----

* <!DOCTYPE html>  声明位于文档中的最前面的位置，处于 html 标签之前。此标签可告知浏览器文档使用哪种 HTML 或 XHTML 规范

  HTML 4.01 规定了三种文档类型：Strict、Transitional 以及 Frameset

* <html lang="en"> 这里的lang="en"可以删除或者改为zh-CN，如果不删除的，用谷歌之类打开，它会认为是英文的，会自动给翻译（如果设置了自动翻译的话）

* <head></head> 是头部区域

* <title></title>之间的内容，是这个文件的标题

* <body>和</body>之间的信息，是正文

[slide]

## html 元素

----

* HTML元素(HTMLElement)用来标记文本，表示文本的内容。比如body, p, title就是HTML元素。 
* HTML元素用Tag表示，Tag以<开始，以>结束。 
* Tag通常是成对出现的，比如<body></body>。起始的叫做Opening Tag，结尾的就叫做ClosingTag。 
* 目前HTML的Tag不区分大小写的。比如，<HTML>和<html>其实是相同的。


[slide]

## html 属性

----

```
<div>
  <label for='username'></label>
  <input name="username" type="text" value='name' />
</div>
```





[slide]

# HTML头部信息(Head)

----

* 标题(title)
* 链接(link)
* 样式(style)
* 关于网页信息(meta)

```
<meta name="description" content="HTML中文教程之头部信息">
<meta name="keywords" content="HTML,tutorials,source codes">
<meta name="author" content="站长网 站长学院">
<meta http-equiv="Refresh" content="5;url=http://www.admin5.com/html/html_tutorials/index.html">
```

* 脚本script

[slide]

# 基础HTML 标签

## html 5 常用标签

```
<article> 定义文章
<aside> 定义页面内容之外的内容
<audio> 定义声音内容
<canvas> 定义图形
<footer> 定义 section 或 page 的页脚
<header> 定义 section 或 page 的页眉
<nav> 定义导航链接
<video> 定义视频
```



[slide]

## html 4 常用标签

```
<a> 定义锚,链接
<address> 定义文档作者或拥有者的联系信息
<b> 定义粗体字
<div> 定义文档中的节
<form> 定义供用户输入的 HTML 表单
<h1> to <h6> 定义 HTML 标题
<img> 定义图像
<iframe> 定义内联框架
<label> 定义 input 元素的标注
<strong> 定义强调文本
<em> 定义强调文本
.....
```



[slide]

# HTML 常用格式

| **Tag**      | **Tag****说明****** |
| ------------ | ----------------- |
| <b>          | 粗体bold            |
| <i>          | 斜体italic          |
| <del>        | 文字当中划线表示删除        |
| <ins>        | 文字下划线表示插入         |
| <sub>        | 下标                |
| <sup>        | 上标                |
| <blockquote> | 缩进表示引用            |
| <pre>        | 保留空格和换行           |
| <code>       | 表示计算机代码，等宽字体      |



[slide]

# HTML 特殊字符显示

## 最常用的特殊字符

| **显示结果****** | **说明****** | **Entity  Name** | **Entity  Number** |
| ------------ | ---------- | ---------------- | ------------------ |
|              | 显示一个空格     | &nbsp;           | &#160;             |
| <            | 小于         | &lt;             | &#60;              |
| >            | 大于         | &gt;             | &#62;              |
| &            | &符号        | &amp;            | &#38;              |
| "            | 双引号        | &quot;           | &#34;              |



[slide]

## 其他常用的字符实体(Character Entities)

| **显示结果****** | **说明****** | **Entity  Name** | **Entity  Number** |
| ------------ | ---------- | ---------------- | ------------------ |
| ©            | 版权         | &copy;           | &#169;             |
| ®            | 注册商标       | &reg;            | &#174;             |
| ×            | 乘号         | &times;          | &#215;             |
| ÷            | 除号         | &divide;         | &#247;             |



[slide]

# HTML 超链接

```
<a href="../asdocs/html_tutorials/humor02.html">这是一个链接</a>
<a href="http://www.admin5.com/html" target=_blank>站长网 站长学院站点链接</a>
<!-- 将一个图片作为一个超链接 -->
<a href="../asdocs/html_tutorials/humor03.html"><img  src="../images/html_tutorials/smile.jpg" ></a>
<a href="http://www.admin5.com/html" title = "站长网 站长学院网页教程与代码的中文站点">站长网 站长学院网站</a
<!-- 使用name属性，可以跳转到一个文件的指定部位 -->
<a href="#C1">参见第一章</a> 
<a name="C1">第一章</a> 
<!-- 链接到email地址 -->
<a href = "mailto:info@sina.com">联系新浪</a>
<p>
这个邮箱地址链接写了to, cc, bcc, subject, body的内容：
<a href="mailto:info@sina.com?cc=webmaster@vip.sina.com&bcc=media@sina.com&subject=I%20like%20your%20site&body=真是个好站点！">写信给新浪</a>
</p>


```



[slide]

# 如何在HTML中创建表格

* HTML表格用table表示。一个表格可以分成很多行(row)，用tr表示；每行又可以分成很多单元格(cell)，用td表示
* 用th来表示表格的表头，表头的字是粗体显示的
* 用caption在一个表格上加上标题
* 用colspan，rowspan设置多列或者多行的单元格
* 用cellpadding这个属性设置单元格内容与单元格边界之间的距离
* 用cellspacing这个属性设置单元格之间的距离



[slide]

# HTML 框架(Frames)

* frameset决定如何划分Frame。frameset有cols属性和rows属性。使用cols属性，表示按列分布Frame；使用rows属性，表示按行分布Frame 
* 用frame这个Tag设定网页。frame里有src属性，src值就是网页的路径和文件名

```
<frameset cols="25%,75%">
   <frame src="../asdocs/html_tutorials/Frame_a.html">
   <frame src="../asdocs/html_tutorials/Frame_b.html">
</frameset>
```

* 行分Frame

```
<html>
<frameset rows="25%,50%,25%">
<frame src="../asdocs/html_tutorials/Frame_a.html">
<frame src="../asdocs/html_tutorials/Frame_b.html">
<frame src="../asdocs/html_tutorials/Frame_c.html">
</frameset>
</html>
```

* 混合Frameset

```
<html>
<frameset rows="50%,50%">
<frame src="../asdocs/html_tutorials/Frame_a.html">
<frameset cols="25%,75%">
<frame src="../asdocs/html_tutorials/Frame_b.html">
<frame src="../asdocs/html_tutorials/Frame_c.html">
</frameset>
</frameset>
</html>
```



[slide]

# HTML 列表(lists)

* 排序列表Ordered List

```
<ol>
<li>站长网 站长学院之网页课程</li>
<li>站长网 站长学院之网页代码</li>
<li>站长网 站长学院之魔兽世界</li>
</ol>
```

* 不排序列表Unordered List

```
<ul type="square">
<li>站长网 站长学院之网页课程</li>
<li>站长网 站长学院之网页代码</li>
<li>站长网 站长学院之魔兽世界</li>
</ul>

```

* 定义列表

```
<dl>
<dt>野生动物</dt>
<dd>所有非经人工饲养而生活于自然环境下的各种动物。</dd>
<dt>宠物</dt>
<dd>指猫、狗以及其它供玩赏、陪伴、领养、饲养的动物，又称作同伴动物。</dd>
</dl>
```

* 嵌套的列表

```
<ul>
  <li>肉类</li>
  <li>蔬菜
    <ul>
      <li>番茄</li>
      <li>青菜</li>
    </ul>
  </li>
</ul>
```





[slide]

# HTML表单(Forms)

* 表单控件(FormControls)
* Action 
* Method

```
<form action="http://www.admin5.com/html/asdocs/html_tutorials/yourname.asp" method="get">
<div>
  <label for="yourname">请输入你的姓名：</label>
  <input type="text" name="yourname">
</div>
<div><input type="submit" value="提交"></div>
</form>

```





[slide]

## HTML表单(Form)常用控件(Controls)

| **表单控件****(Form Contros)** | **说明******                      |
| -------------------------- | ------------------------------- |
| input  type="text"         | 单行文本输入框                         |
| input  type="submit"       | 将表单(Form)里的信息提交给表单里action所指向的文件 |
| input  type="checkbox"     | 复选框                             |
| input  type="radio"        | 单选框                             |
| select                     | 下拉框                             |
| textArea                   | 多行文本输入框                         |
| input  type="password"     | 密码输入框(输入的文字用*表示)                |

