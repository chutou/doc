#	SCSS迷你书(上)



# 注释

支持常规的两种注释方法; 
1. `//`双斜杠的单行注释, eg : //这是一个圆角按钮 
2. `/**/`范围注释, eg:

```
/*
    什么功能;
    做什么用的;
*/12341234
```

------

# 设置文件编码

编码`@charset "encoding-name";` , 若需要支持中文注释,在SCSS文件的顶部写上`@charset "UTF-8";`

------

# 变量

- 普通变量:

```
$fs:12px;
p{
   font-size: $fs;   //css: font-size:12px;
}12341234
```

- 默认变量; 
  **sass 的默认变量仅需要在值后面加上 !default 即可。**

```
//调用默认变量
$fs:12px !default;
p{
   font-size: $fs;   //css: font-size:12px;
}

//覆盖默认变量
$fs:15px;
$fs:12px !default;
p{
   font-size: $fs;   //css: font-size:15px;
}123456789101112123456789101112
```

- 全局变量:

```
$fs:12px;   //在元素内部外或者mixin外部定义皆可理解为全局
p{
   font-size: $fs;   //css: font-size:12px;
}12341234
```

- 局部变量:

```
$fs:12px;
p{
   $fs : 20px;        //在元素内部定义的变量为局部变量,若是外部全局变量和局部变量命名一致,全局会被局部变量
   font-size: $fs;   //css: font-size:20px;
}1234512345
```

------

# CSS样式继承

**除了个别选择符,基本和CSS一样,就是写法是内嵌格式** 
\- 元素嵌套

```
#main{
     p{ font-size:15px}     //css : #main p{};
     >a{
         span{font-size:10px;} //css: #main>a span{font-size:10px;}                     
     }
}123456123456
```

- 属性嵌套

```
#main{
     border{
            top:1px solid #ccc;
            left:2px solid #ddd;
     }
}
/*
#main border {
  top: 1px solid #ccc;
  left: 2px solid #ddd;
}
*/
1234567891011121312345678910111213
```

------

# `&` : 父类选择符

```
#main{
     p{ font-size:15px}     //css : #main p{};
     >a{                              //css: #main>a{}
          &:link,
          &:visited{}           //css: #main>a:link,#main>a:link{}
          &:hover{};            // &在SCSS内嵌中代表父类,css: #main>a:hover{};
          &:active{};
     }
}123456789123456789
```

------

# `%` 占位符,减少CSS无用的样式的好方法

**若是用调用,则占位符变量生效,无则不生效;可以避免@extend class的隐患**

```
%mr5{
   margin-right:5px;
}

body{
    @extend %mr5;       //css: body{margin-right:5px}
}
1234567812345678
```

------

# 声明宏

**宏其实有点类似编程语言的函数,都是以达到复用为目的的** 
\- 不带参数混合宏

```
   @mixin ul-unstyle{
        list-style:none;
  } 123123
```

- 带参数混合宏

```
   $width:50px;
   $display:inline-block;

   @mixin li-unstyle($width,$display){
        list-style:none;
        width:$width;
        display:$display;
  } 

  ul{
    @include li-unstyle($width,$display);
  }

/*
ul {
  list-style: none;
  width: 50px;
  display: inline-block;
}
*/

1234567891011121314151617181920212212345678910111213141516171819202122
```

- 带默认值参数混合宏

```
   @mixin li-unstyle($width:5px,$display:block){
        list-style:none;
        width:$width;
        display:$display;
  } 

  li{  
    @include li-unstyle;
  }

/*
li {
  list-style: none;
  width: 5px;
  display: block;
}
*/

1234567891011121314151617181912345678910111213141516171819
```

- 混合宏的参数–传一个不带值的参数

```
     $width:50px;
     $display:inline-block;

     @mixin li-unstyle($width,$display){
          list-style:none;
          width:$width;
          display:$display;
    } 

    ul{
      @include li-unstyle(500px,block);
    }

/*

ul {
  list-style: none;
  width: 500px;
  display: block;
}

*/1234567891011121314151617181920212212345678910111213141516171819202122
```

- 混合宏传参,类值列表参数

```
$shadow:0 0 3px rgba(#000,.5);
@mixin sw($shadow...){
  text-shadow:$shadow;

}

p{
  @include sw($shadow);
}

/*
p {
  text-shadow: 0 0 3px rgba(0, 0, 0, 0.5);
}

*/1234567891011121314151612345678910111213141516
```

------

# 插值 #{}

**可以设置参数以字符串的形式输出**

```
$test:(margin,border);
@mixin t($t1, $t2){
  @each $t3 in $test{
    #{$t3}-#{$t1}:$t2;
  }
}

.btn{
  @include t(right,5px);

}


/*
.btn {
  margin-right: 5px;
  border-right: 5px;
}

*/12345678910111213141516171819201234567891011121314151617181920
```

------

# 数据类型

SCSS有以下这么多数据类型**数字,字符串,颜色,布尔值,空值,值列表** 
\- 数字: 1、 2、 13、 10px； 
\- 字符串：有引号字符串或无引号字符串，如，”foo”、 ‘bar’、 baz； 
\- 颜色：blue、 #04a3f9、 rgba(255,0,0,0.5)； 
\- 布尔型：true、 false； 
\- 空值： null； 
\- 值列表：1.5em 1em 0 2em Helvetica, Arial, sans-serif。[用空格或者逗号分开]

# 加减乘除

**都建议用括号包起来,只要单位相同,都可以做运算;不同单位,少数会报错** 
\- 比如除法,因为CSS有双参数斜杆隔开的写法: 50px/30px , SCSS是无法识别的位除法的,加了括号即可 
\- 颜色也可以做运算; 
\- 变量也可以做运算;

------

# 逻辑处理

- @if : 判断

```
@mixin tt($b:false){
  @if $b{

    border-right:5px;
  }
  @else{
    @for $i from 1 through 3 {
      .item-#{$i} { width: 2em * $i; }
    }
  }

}

.b1{
  @include tt($b:true);
}
.b2{
  @include tt;
}
/*
.b1 {
  border-right: 5px;
}

.b2 .item-1 {
  width: 2em;
}
.b2 .item-2 {
  width: 4em;
}
.b2 .item-3 {
  width: 6em;
}

*/123456789101112131415161718192021222324252627282930313233343536123456789101112131415161718192021222324252627282930313233343536
```

- @for : 循环 
  在 Sass 的 @for 循环中有两种方式： 
  `@for $i from  through ` 
  `@for $i from  to ` 
  $i 表示变量start 表示起始值end 表示结束值

```
@for $i from 1 through 3 {
  .item-#{$i} { width: 2em * $i; }
}

/*
.item-1 {
  width: 2em;
}

.item-2 {
  width: 4em;
}

.item-3 {
  width: 6em;
}

*/123456789101112131415161718123456789101112131415161718
```

- @while : 循环

```
$num : 2;
$height: 10px;
@while $num > 0 {
  .page-#{height}{
    height:$height * $num;
  };
  $num : $num - 1;
}

/*
.page-height {
  height: 20px;
}

.page-height {
  height: 10px;
}

*/12345678910111213141516171819201234567891011121314151617181920
```

- each 遍历

**@each 循环就是去遍历一个列表，然后从列表中取出对应的值** 
**@each 循环指令的形式：@each $var in **

```
$test:top,right,bottom,left;

@mixin btn-extend{
  @each $i in  $test{
    border-#{$i}:5px;
  }
}

.btn{
  @include btn-extend;
}

/*
.btn {
  border-top: 5px;
  border-right: 5px;
  border-bottom: 5px;
  border-left: 5px;
}

*/
1234567891011121314151617181920212212345678910111213141516171819202122
```

------

# 函数功能

## 字符串与数字函数

- unquote()函数 : 只会去除最外层的字符串,不处理中间的字符串,没有字符串符号则不处理

```
p:before{
  content:unquote("sss");
}

p:before{
  content:unquote('"sss"');
}

/*
p:before {
  content: sss;
}

p:before {
  content: "sss";
}

*/
1234567891011121314151617181912345678910111213141516171819
```

- to-upper-case(),to-lower-case() : 转换大小写

```
.test {
  text: to-upper-case(aaaaa);
  text: to-upper-case(aA-aAAA-aaa);
}

.test2{
  text: to-lower-case(AAAZDc)
}

/*
.test {
  text: AAAAA;
  text: AA-AAAA-AAA;
}

.test2 {
  text: aaazdc;
}

*/12345678910111213141516171819201234567891011121314151617181920
```

## 数字函数

- percentage($value)：将一个不带单位的数转换成百分比值；
- round($value)：将数值四舍五入，转换成一个最接近的整数；
- ceil($value)：将大于自己的小数转换成下一位整数；
- floor($value)：将一个数去除他的小数部分；
- abs($value)：返回一个数的绝对值；
- min($numbers…)：找出几个数值之间的最小值；
- max($numbers…)：找出几个数值之间的最大值；
- random(): 获取随机数

```
$fs:5.3;
$t:10 99 1 2 3 4 5 6;
.test{
  height:percentage($fs);
  width:round($fs);
  width:ceil($fs);
  width:floor($fs);
  width:abs($fs);
  width:min($t...);
  width:max($t...);
  border-radius:random();
}

/*
.test {
  height: 530%;
  width: 5;
  width: 6;
  width: 5;
  width: 5.3;
  width: 1;
  width: 99;
  border-radius: 0.28517;
}

*/12345678910111213141516171819202122232425261234567891011121314151617181920212223242526
```

## 列表函数

- length($list)：返回一个列表的长度值； input`length(10px)` print 1 ,input `length(border 1px solid)` print3;
- nth(list,n)：返回一个列表中指定的某个标签值; input`nth(10px 20px 30px,2)`,print `20px`;
- join(list1,list2, [$separator])：将两个列给连接在一起，变成一个列表(最多只能两个)。input:`join((blue,red),(#abc #def))` ,print`(#0000ff, #ff0000, #aabbcc, #ddeeff)`；
- append(list1,val, [$separator])：将某个值放在列表的最后；input: `append(10px 20px ,30px)` , print `(10px 20px 30px)`;
- zip($lists…)：将几个列表结合成一个多维的列表；input:`zip(1px 2px 3px,solid dashed dotted,green blue red)` , print`((1px "solid" #008000), (2px "dashed" #0000ff), (3px "dotted" #ff0000))`;
- index(list,value)：返回一个值在列表中的位置值; input : `index(1px solid red, solid)` , print 2;