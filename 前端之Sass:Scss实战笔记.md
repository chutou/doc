# 前端之Sass/Scss实战笔记

# Introduction

Sass 有两种语法规则(syntaxes),目前新的语法规则（从 Sass 3开始）被称为 “SCSS”( 时髦的css（Sassy CSS）),它是css3语法的的拓展级，就是说每一个语法正确的CSS3文件也是合法的SCSS文件，SCSS文件使用.scss作为拓展名。第二种语法别成为缩进语法（或者 Sass），它受到了Haml的简洁精炼的启发，它是为了人们可以用和css相近的但是更精简的方式来书写css而诞生的。它没有括号，分号，它使用 行缩进 的方式来指定css 块，虽然sass不是最原始的语法，但是缩进语法将继续被支持，在缩进语法的文件以 .sass 为拓展名。

## 注释

有三种形式：

（1）//comment：该注释只是在.scss源文件中有，编译后的css文件中没有。

（2）/*! */：重要注释，任何style的css文件中都会有，一般放置css文件版权说明等信息。

（3）/* */：该注释在compressed的style的css中没有，其他style的css文件都会含有。

## Quick Start

### Installation

### Build

**1.切换到.scss文件所在目录**

命令行下切换到代码文件夹目录（如Z:\），假设有文件test.scss文件，里面内容如下：（SASS完全支持css语法）

```
h1{
    font-size:17px;    
}
h2{
    font-size:18px;
}
```

**2.编译scss文件为css文件**

　　运行命令：sass --style compressed test.scss test.css，即可生成压缩版的css文件，并且命名为test.css。几点说明：

（1）--style 后面可以有四个参数可选，分别为expanded、nested、compact、compressed，分别选用不同参数的效果可以自己尝试体验。

（2）test.scss和test.css文件目录可以自定义，例如把Z盘sass目录下的test.scss文件编译为压缩版的文件，并放置在Z盘css目录下，那么命令即：sass --style compressed z:\sass\test.scss z:\css\test.css

（3）开发过程中，只需要修改scss文件，然后编译；前端页面只需要引用相应的css文件即可。

**3.侦听文件和文件夹**

如果希望某一个scss文件或者相应的文件夹下面文件修改后，自动进行编译，那么可以使用侦听命令。

（1）侦听文件：

sass --watch --style compressed test.scss:test.css

当test.scss文件有修改后，会自动编译为test.css，并且是compressed的。

（2）侦听文件夹：

sass --watch --style compressed sass:css

当sass文件夹下.scss文件有修改的时候，会自动编译为与sass中文件同名的css文件。

 **备注：**

（1）注意源文件和目标文件之间是**冒号**，与编译命令中为空格不同。

（2）生成的map文件可以查找source map文件的作用。

### Webpack

Webpack中也内置了sass-loader，通过简单的配置既可以使用。不过需要注意的是，Webpack的sass-loader还是依赖于node-sass以及sass(gem)，所以如果安装sass-loader报错可以先尝试安装sass。

# 变量与选择器

## 变量

### 定义

变量的定义一般以$开头，某个变量的作用域仅限于他们定义的层级以及子层级。如果变量是定义在所有嵌套选择器之外的，那么他们可以在各处被调用。

```
$color1:#aeaeae;
.div1{
    background-color:$color1;
}
```

编译后：

```
.div1 {
  background-color: #aeaeae;
}
/*# sourceMappingURL=test.css.map */
```

如果希望某个在子选择器中定义的变量能够成为全局变量，可以使用!global关键字：

```
#main {
  $width: 5em !global;
  width: $width;
}

#sidebar {
  width: $width;
}
```

### 嵌套引用

嵌套引用在其他编程语言中即是字符串插值，需要用#{}进行包裹：

```
$left:left;
.div1{
    border-#{$left}-width:5px;
}
```

### 变量计算

Sass中也是支持对于变量进行简单的计算：

```
$left:20px;
.div1{
    margin-left:$left+12px;
}
```

变量可以支持计算的类型，还是比较多的：

```
p {
  font: 10px/8px;             // Plain CSS, no division
  $width: 1000px;
  width: $width/2;            // Uses a variable, does division
  width: round(1.5)/2;        // Uses a function, does division
  height: (500px/2);          // Uses parentheses, does division
  margin-left: 5px + 8px/2px; // Uses +, does division
  font: (italic bold 10px/8px); // In a list, parentheses don't count
}
```

## 选择器

### 嵌套

```
.div1{
    .span1{
        height: 12px;
    }
    .div2{
        width: 16px;
    }
}
```

属性也可以嵌套，比如border-color属性，可以写成：

```
　　p {
　　　　border: {
　　　　　　color: red;
　　　　}
　　}
```

注意，border后面必须加上冒号。

### 父元素引用

在嵌套的子层级中，允许使用&引用父元素：

```
.div1{
    &:hover{
        cursor: hand;
    }
}
```

# 代码重用

## 继承

SASS允许一个选择器，继承另一个选择器。比如，现有class1：

```
.class1{
    font-size:19px;
}
.class2{
    @extend .class1;
    color:black;
}
```

**注意：如果在class2后面有设置了class1的属性，那么也会影响class2，如下：**

```
.class1{
    font-size:19px;
}
.class2{
    @extend .class1;
    color:black;
}
.class1{
    font-weight:bold;
}
```

由此可以看出Scss也是递归编译的。

## **引用外部css文件（Partials）**

有时网页的不同部分会分成多个文件来写样式，或者引用通用的一些样式，那么可以使用@import。

```
@import "_test1.scss";
@import "_test2.scss";
@import "_test3.scss";
```

## Mixin&Include

Mixin有点像C语言的宏（macro），是可以重用的代码块。

使用@mixin命令，定义一个代码块。

```
　　@mixin left {
　　　　float: left;
　　　　margin-left: 10px;
　　}
```

使用@include命令，调用这个mixin。

```
　　div {
　　　　@include left;
　　}
```

### 参数与缺省值

- 边距设置

```
@mixin common($value1,$value2,$defaultValue:12px){
    display:block;
    margin-left:$value1;
    margin-right:$value2;
    padding:$defaultValue;
}
.class1{
    font-size:16px;
    @include common(12px,13px,15px);
}
.class2{
    font-size:16px;
    @include common(12px,13px);
}
```

- 浏览器前缀设置设置

下面是一个mixin的实例，用来生成浏览器前缀。

```
　　@mixin rounded($vert, $horz, $radius: 10px) {
　　　　border-#{$vert}-#{$horz}-radius: $radius;
　　　　-moz-border-radius-#{$vert}#{$horz}: $radius;
　　　　-webkit-border-#{$vert}-#{$horz}-radius: $radius;
　　}
```

使用的时候，可以像下面这样调用：

```
　　#navbar li { @include rounded(top, left); }
　　#footer { @include rounded(top, left, 5px); }
```

# 编程式方法

## 流程控制

### 条件语句

@if可以用来判断：

```
　　p {
　　　　@if 1 + 1 == 2 { border: 1px solid; }
　　　　@if 5 < 3 { border: 2px dotted; }
　　}
```

配套的还有@else命令：

```
　　@if lightness($color) > 30% {
　　　　background-color: #000;
　　} @else {
　　　　background-color: #fff;
　　}
```

### 循环语句

SASS支持for循环：

```
　　@for $i from 1 to 10 {
　　　　.border-#{$i} {
　　　　　　border: #{$i}px solid blue;
　　　　}
　　}
```

也支持while循环：

```
　　$i: 6;
　　@while $i > 0 {
　　　　.item-#{$i} { width: 2em * $i; }
　　　　$i: $i - 2;
　　}
```

each命令，作用与for类似：

```
　　@each $member in a, b, c, d {
　　　　.#{$member} {
　　　　　　background-image: url("/image/#{$member}.jpg");
　　　　}
　　}
```

## 函数

Sass允许用户自定义函数，原型如下所示：

```
　　@function double($n) {
　　　　@return $n * 2;
　　}

　　#sidebar {
　　　　width: double(5px);
　　}
```

### 颜色函数

SASS提供了一些内置的颜色函数，以便生成系列颜色。

```
　　lighten(#cc3, 10%)  // #d6d65c
　　darken(#cc3, 10%)  //  #a3a329
　　grayscale(#cc3) // #808080
　　complement(#cc3) // #33c
```

# Reference

> - [阮一峰-SASS用法指南](http://www.ruanyifeng.com/blog/2012/06/sass.html)
> - [Official Documentation](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#variables_)

# mixins

sass mixins，require `Sass ~> 3.3.0`

**utility**

- [`prefix`](https://github.com/huanz/mixins#prefix)
- [`clearfix`](https://github.com/huanz/mixins#clearfix)
- [`float`](https://github.com/huanz/mixins#float)
- [`text-overflow`](https://github.com/huanz/mixins#text-overflow)
- [`animation`](https://github.com/huanz/mixins#animation)
- [`placeholder`](https://github.com/huanz/mixins#placeholder)
- [`rem`](https://github.com/huanz/mixins#rem)
- [`opacity`](https://github.com/huanz/mixins#opacity)
- [`arrow`](https://github.com/huanz/mixins#arrow)
- [`triangle`](https://github.com/huanz/mixins#triangle)
- [`center`](https://github.com/huanz/mixins#center)
- [`media`](https://github.com/huanz/mixins#media)
- [`box-sizing`](https://github.com/huanz/mixins#box-sizing)
- [`touch-scroll`](https://github.com/huanz/mixins#touch-scroll)
- [`font`](https://github.com/huanz/mixins#font)

**functions**

*string*

- [`str-split`](https://github.com/huanz/mixins#str-split)
- [`str-repeat`](https://github.com/huanz/mixins#str-repeat)
- [`str-replace`](https://github.com/huanz/mixins#str-replace)

*list*

- [`first`](https://github.com/huanz/mixins#first)
- [`last`](https://github.com/huanz/mixins#last)
- [`prepend`](https://github.com/huanz/mixins#prepend)
- [`insert-nth`](https://github.com/huanz/mixins#insert-nth)
- [`replace`](https://github.com/huanz/mixins#replace)
- [`replace-nth`](https://github.com/huanz/mixins#replace-nth)
- [`remove`](https://github.com/huanz/mixins#remove)
- [`remove-nth`](https://github.com/huanz/mixins#remove-nth)
- [`slice`](https://github.com/huanz/mixins#slice)
- [`to-string`](https://github.com/huanz/mixins#to-string)
- [`shift`](https://github.com/huanz/mixins#shift)

## [](https://github.com/huanz/mixins#install)install

```
npm i mixins-sass --save
```

## [](https://github.com/huanz/mixins#utility)utility

### [](https://github.com/huanz/mixins#prefix)`prefix`

```
// scss 默认前缀：webkit moz ms o
.test {
    @include prefix((transliton: all 0.5s ease-out), webkit);
}
// css
.test {
    -webkit-transliton: all 0.5s ease-out;
    transliton: all 0.5s ease-out;
}

```

### [](https://github.com/huanz/mixins#clearfix)clearfix

```
@include clearfix;
```

### [](https://github.com/huanz/mixins#float)float

```
@include float(left);
```

### [](https://github.com/huanz/mixins#text-overflow)text-overflow

文字超出显示省略号，支持多行，`$substract`为预留区域百分比%

```
@mixin text-overflow($line: 1, $substract: 0);
```

### [](https://github.com/huanz/mixins#animation)animation

```
@include animation(slideUp 900ms ease both) {
    0% {
        transform: translate3d(0, -200px, 0);
    }
    100% {
        transform: translate3d(0, 0, 0);
    }
}
```

### [](https://github.com/huanz/mixins#placeholder)placeholder

```
// scss
@include placeholder() {
    ...
}
// css
::-webkit-input-placeholder {
    ...
}
::-moz-placeholder {
    ...
}
:-ms-input-placeholder {
   ...
}
```

### [](https://github.com/huanz/mixins#rem)rem

px转rem

```
// @mixin rem($property, $values, $support-ie: true, $base: null)
// $support-ie不支持rem的浏览器使用px
// $base 如果未传，会搜索全局变量 $base-font，如果没有默认为 16px

@include rem('padding', '10px 5px 5px 10px', true, '16px');
```

### [](https://github.com/huanz/mixins#opacity)opacity

兼容ie的透明度

### [](https://github.com/huanz/mixins#arrow)arrow

生成上下左右的小箭头：[http://lugolabs.com/caret](http://lugolabs.com/caret)

```
// @mixin arrow($width, $border-width, $direction, $color, $background-color, $position: relative)
// 箭头宽度  线宽 方向 颜色 背景颜色（一般和父级背景同色）

@include arrow(10px, 1px, 'bottom', '#00f', '#fff');
```

### [](https://github.com/huanz/mixins#triangle)triangle

三角形生成

```
// @mixin triangle($width, $height, $color: #000, $direction: down)

@include triangle(10px, 5px);
```

### [](https://github.com/huanz/mixins#center)center

居中

```
// horizontal,vertical,both

@include center(both);
```

### [](https://github.com/huanz/mixins#media)media

媒体查询相关

```
// min-width max-width

@mixin screen($min, $max)
@mixin max-screen($width)
@mixin min-screen($width)
@mixin hidpi($ratio: 1.3)
@mixin retina-image($filename, $retina-filename, $ratio: 1.3, $background-size: 100%)
@mixin iphone6($orientation: all)
@mixin iphone6plus($orientation: all)
@mixin iphone5($orientation: all)
@mixin iphone4($orientation: all)
@mixin ipad($orientation: all)
@mixin ipad-mini($orientation: all)
@mixin ipad-retina($orientation: all)

@include retina-image(test.png, test@2.png test@3.png, 2 3);
```

### [](https://github.com/huanz/mixins#box-sizing)box-sizing

```
html {
    @include box-sizing(border-box);
}
```

### [](https://github.com/huanz/mixins#touch-scroll)touch-scroll

```
body {
    @include touch-scroll;
}
// css
body {
    -webkit-overflow-scrolling: touch;
    overflow-scrolling: touch;
}
```

### [](https://github.com/huanz/mixins#font)font

中文字体解决方案，来自[https://github.com/zenozeng/fonts.css](https://github.com/zenozeng/fonts.css)，有`font-hei`、`font-kai`、`font-song`、`font-fang-song`。

```
body {
    @include font-hei;
}
```

## [](https://github.com/huanz/mixins#functions)functions

**string**

### [](https://github.com/huanz/mixins#str-split)str-split

字符串分隔

```
@function str-split($string, $delimiter: " ")
```

### [](https://github.com/huanz/mixins#str-repeat)str-repeat

字符串重复

```
@function str-repeat($string, $times)
```

### [](https://github.com/huanz/mixins#str-replace)str-replace

字符串替换

```
@function str-replace($string, $search, $replace: "")
```

**list**

### [](https://github.com/huanz/mixins#first)first

返回列表第一项

```
@function first($list)
```

### [](https://github.com/huanz/mixins#last)last

返回列表最后一项

```
@function last($list)
```

### [](https://github.com/huanz/mixins#prepend)prepend

向列表前面插入一个

```
@function prepend($list, $value)
```

### [](https://github.com/huanz/mixins#insert-nth)insert-nth

向列表某个位置插入

```
@function insert-nth($list, $index, $value)
```

### [](https://github.com/huanz/mixins#replace)replace

替换列表的某个元素 `$recursive` 是否全部替换

```
@function replace($list, $old-value, $new-value, $recursive: false)
```

### [](https://github.com/huanz/mixins#replace-nth)replace-nth

替换列表某个位置的元素

```
@function replace-nth($list, $index, $value)
```

### [](https://github.com/huanz/mixins#remove)remove

删除列表某个元素 `$recursive` 是否删除所有

```
@function remove($list, $value, $recursive: false)
```

### [](https://github.com/huanz/mixins#remove-nth)remove-nth

删除列表指定位置元素

```
@function remove-nth($list, $index)
```

### [](https://github.com/huanz/mixins#slice)slice

截取列表中的一部分

```
@function slice($list, $start: 1, $end: length($list))
```

### [](https://github.com/huanz/mixins#to-string)to-string

列表变成字符串，`$glue`为连接符，`$is-nested`是否是嵌套的列表

```
@function to-string($list, $glue: '', $is-nested: false)
```

### [](https://github.com/huanz/mixins#shift)shift

将列表部分元素前置

```
@function shift($list, $index: 1)
```