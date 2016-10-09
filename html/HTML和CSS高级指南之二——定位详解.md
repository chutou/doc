# HTML和CSS高级指南之二——定位详解

本文由[大漠](http://www.w3cplus.com/)根据[Shay Howe](http://shayhowe.com/)的《[An Adavnced Guide to HTML & CSS](http://learn.shayhowe.com/advanced-html-css/)》第二课《[Detailed Positioning](http://learn.shayhowe.com/advanced-html-css/detailed-css-positioning)》所译，整个译文带有我们自己的理解与思想，如果译得不好或不对之处还请同行朋友指点。如需转载此译文，需注明英文出处：[http://learn.shayhowe.com/advanced-html-css/detailed-css-positioning](http://learn.shayhowe.com/advanced-html-css/detailed-css-positioning)，以及作者相关信息

作者：[Shay Howe](http://shayhowe.com/)

译者：[大漠](http://www.w3cplus.com/)

当在这一个页面上实现布局和定位有几种不同的技术。使用哪种技术，很大程序上取决于内容和目标页面，因为有很多技术比别人的更牛。

例如，浮动可以让页面元素并排显示，而且还可以制作一个干净的布局。然而，有时候需要一些严格的定位，这时需要使用其他的技术，包括“relative”和“absolute”定位。

在这节课中，我们先来介绍一下浮动的使用，接下来详细介绍定位的技巧，包括如何准确的给元素在X轴、Y轴和Z轴定位。

-  [包含浮动](http://www.w3cplus.com/css/advanced-html-css-lesson2-detailed-css-positioning.html#containingFloats)
-  [定位属性](http://www.w3cplus.com/css/advanced-html-css-lesson2-detailed-css-positioning.html#positionProperty)
-  [z-index属性](http://www.w3cplus.com/css/advanced-html-css-lesson2-detailed-css-positioning.html#zindexProperty)

#### 包含浮动

创建一全页面的布局时，浮动是一种常用的方法，也是页面元素定位的一种基本功能。浮动可以让元素一个挨着一个。浮动可以创建一个自然流布局，同时充许元素设置自身尺寸和其父元素容器的尺寸大小。

当元素浮动时，一个元素的位置依赖于放置在他周边的其他元素。那么围绕在他周边的是哪个元素呢？这个元素会换行吗？这一切都取决于围绕于他的元素的DOM（文档对象模型）。

> #### DOM是什么？
>
> DOM是Document Object Model的简称，被译为文档对象模型。是HTML或者XML文档结构的API。在我们的例子中，我们说的是HTML的文档，因此DOM就是代表所有元素以及这些元素之间的关系。
>
> 可以考虑树形的表现方式，展元素元素之间的关系。元素嵌套时他们存在父子关系，相同级别的还存在兄弟关系。

虽然 [浮动](http://css-tricks.com/all-about-floats/)相当的给力，但他们自己还是存在一定的问题。最典型的问题就是一个父元素包含了多个浮动的子元素。页面的内容设置了一个宽度，子元素的浮动确定了他们的位置，但浮动元素不会影响父元素的宽度。这样做会让父元素塌陷，从而使父元素的高度为“0”，以及忽略其他的属性。很多时候，这种现像都被忽略，特别是在父元素没有任何样式，以及其子元素看起来都正确的对齐。

嵌套的元素不会正确的排列，也会有错误的样式出现。来看看下面的演示，在“.box-set”的div应该有一个高亮的灰色背景，因为所有的子元素浮动后，这个灰色的背景色并不看到。仔细检查后，“.box-set”的高度变成了“0”。

**HTML**

```
<div class="box-set">
  <div class="box">Box 1</div>
  <div class="box">Box 2</div>
  <div class="box">Box 3</div>
</div>	

```

**CSS**

```
.box-set {
  background: #e8eae9;
}
.box {
  background: #8ec63f;
  height: 100px;
  float: left;
  margin: 10px;
  width: 200px;
}	

```

**DEMO效果**

![包含浮动](http://cdn.w3cplus.com/cdn/farfuture/DkV8vEVZR_X4hzAn_gjsSdIha_8LCZjMekrX5N2Z_7g/mtime:1421035049/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson2-1.jpg)

有一种方法，在容器的结束标签前添加一个空标签，在空标签上直接设置样式“clear:both”。用这种方法来清除浮动，在大多数情况下是有效的，但这不太适合语义化。这取决于一个页面有多少浮动需要清除，这样造成页面上的空标签迅速堆积，而且在页面中没有上下文内容。

幸运的是有几种不同[方法](http://www.ejeliot.com/blog/59)可以用来清除浮动，而其中用得最多的是“overflow”技巧和"clearfix"技巧。

**Overflow技巧**

一种清除浮动的技巧是使用“overflow”属性。在具有浮动元素的父容器中设置“overflow”的属性值为“auto”，这样父容器就会有一个高度存在，在我们例子中的灰色背景也就能看得到了。

在IE6里面，父容器是需要设置一个“width”和“height”。因为高度可能是一个变量，宽度为100%，他们将能正常的工作。使用“overflow:auto;”,在IE浏览器中会给元素添加滚动条，这样一来，最好是直接使用“overflow:hidden;”来清除浮动。

```
.box-set {
  background: #404853;
  overflow: auto;
}	

```

**清除浮动后效果**

![包含浮动](http://cdn.w3cplus.com/cdn/farfuture/qeK6Lq0b4iTUD6RAuBQV3NMz7RdANf2m5Asl0DzhF3E/mtime:1421035049/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson2-2.jpg)

使用“overflow”技巧清除浮动，确实存在一些缺点。例如：当你添加样式，或者将嵌套在里面的“span”元素移动到父容器的外面，或者你想给元素添加一个盒子阴影和制作一个下拉菜单。在下面的演示例子中，你可以看到元素的盒子阴影被切断在父元素之内。

不同的浏览器对“overflow”属性解析不一样，在浏览器的显示风格也不一样。看看下面的例子，注意列在不同浏览器的显示效果。

![包含浮动](http://cdn1.w3cplus.com/cdn/farfuture/bt_6HV85Z2visXDPmFzSA3rRZIZIemAFp38mNOYsUqM/mtime:1421035049/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson2-3.jpg)

**clearfix技巧**

根据上下文，清除浮动更好的方法是[clearfix](http://nicolasgallagher.com/micro-clearfix-hack/)技巧。“clearfix”清除浮动的技术是有点复杂，但有有比使用“overflow”技巧清除浮动更好的方法？

“clearfix”技巧是基于在父元素上使用“:before”和“:after”两个伪类。使用这些伪类，我们可以在浮动元素的父容器前面和后面创建隐藏元素。“:before”伪类是用来防止子元素顶部的外边距塌陷，使用“display: table”创建一个匿名的“table-cell”元素。这也确保在IE6和IE7下具有一致性。“:after”伪类是用来防止子元素的底部的外边距塌陷，以及用来清除元素的浮动。

在IE6和7的浏览器中，加上“*zoom”属性来触发父元素的[hasLayout](http://www.satzansatz.de/cssd/onhavinglayout.html)的机制。决定了元素怎样渲染内容，以及元素与元素之间的相互影响。

采取上面同样的例子，你可以看到容器也清除了浮动，元素也可以移到父容器外面：

```
.box-set:before,
.box-set:after {
  content: "";
  display: table;
}
.box-set:after {
  clear: both;
}
.box-set {
  *zoom: 1;
}	

```

**清除浮动后效果**

![包含浮动](http://cdn2.w3cplus.com/cdn/farfuture/jmSUTwo8h__j1W2szbu3GvabowsEKkLz9E6A8Lv9P-U/mtime:1421035049/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson2-4.jpg)

**有效的包含浮动**

使用哪种技巧来清除浮动，终究要看你自己喜好。有些人坚持使用“clearfix”来清除浮动，因为这种方法可以贯穿整个项目。有些人认为“clearfix”技巧使用的代码太多，他还是喜欢简单点的。至于使用什么技巧由您来决定，只要在运用了浮动的元素的父容器需要清除浮动。

一个常见的方法是将定义一个类名，把这个类名加到需要清除浮动的容器上。例如使用“clearfix”清除浮动，Dan Cederholm为容器设置了一个类名“group”。在需要清除浮动的容器上添加这个类名“group”。

```
.group:before,
.group:after {
  content: "";
  display: table;
}
.group:after {
  clear: both;
}
.group {
  *zoom: 1;
}	

```

> #### 单个伪类
>
> 值得注意的是，目前每个元素只有一个“:before”和“:after”伪类。当你尝试使用其他的“:before”和“:after”的clearfix技巧，你的内容可能无法达到想要的效果。

在上面的例子中，clearfix的样式不应该直接插入到“.box-set”类中，应该是给需要清除浮动的元素中添加类名“group”。

#### 定位属性

很多情况下，你需要控制更多元素的位置，而且超过了浮动所能提供的范围，这个时候我们就需要发挥“position”属性的作用。“position”属性提供五个不同的属性值，每种不同的方式可以给元素提供不同的[位置](http://alistapart.com/article/css-positioning-101)。

**Position static**

元素都有position属性，其默认值是“static”，这也意味着，他们没有也不接受[位置属性设置](http://learn.shayhowe.com/html-css/box-model#positioning-elements)（top、right、bottom、left属性值设置）。另外元素设置了position属性，将会覆盖元素的默认值“static”。

在下面的演示中，所有的盒子都是静态的，每个盒子都在相邻盒子顶部，因为他们都是块元素，而且没有进行浮动设置。

**HTML**

```
<div class="box-set">
  <div class="box">Box 1</div>
  <div class="box">Box 2</div>
  <div class="box">Box 3</div>
</div>	

```

**CSS**

```
.box-set {
  background: #e8eae9;
}
.box {
  background: #8ec63f;
  height: 80px;
  width: 80px;
}	

```

**效果**

![包含浮动](http://cdn1.w3cplus.com/cdn/farfuture/DiuA7yGt_YyKD4FoC_npASVVVVa3-zUt5MnKo5a8Npo/mtime:1421035049/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson2-5.jpg)

**Position relative**

“relative”是“position”的另一个属性值，他和“static”属性值非常的相似。主要的区别是“relative”可以给元素设置位移（offset）“top、right、bottom和left”属性。通过这些位移属性设置可以给元素进行精确的定位。

> #### 盒子位移属性是如何工作？
>
> 盒子的位移属性有四个“top、right、bottom和left”，用来指定元素的定位位置和方向。这些属性只能在元素的“position”属性设置了“relative、absolute和fixed”属性值，才生效。
>
> 对于相对定位元素，这些属性的设置让元素从默认位置移动。例如，top设置一个值“20px”在一个相对定位的元素上，这个元素会在原来位置向下移动“20px”。反之，“top”设置一个“-20px”，这个元素会在原来的位置向上移动“20px”。
>
> 对于绝对定位和固定定位鲜红，这些属性指定了元素与父元素边缘之间的距离，例如，绝对定位的元素设置一个“top”值为“20px”，将使绝对定位元素相对于其设置了相对定位的祖先元素顶部边缘向下移动“20px”，反之，如果设置一个“top”值为“20px”，将使绝对定位元素相对于其设置了相对定位的祖先元素顶部边缘向上移动“20px”。（绝对定位的参考点是其祖先元素设置了“relative”或者“absolute”值）。

设置了位移属性的相对定位元素，他在页面中仍然是正常的、静态的，仍属于自然流。在这种情况下，其他元素不会占用相对定们元素当初的位置。此外，其他元素没有进行位置移动时，相对定伴元素可能会和其他元素重叠。

在下面的演示中，每个元素还是在另一个元素顶部，然后他们根据自己移位属性，从默认位置进行移动，由于他们移向方向不一样，这些值使元素重叠在一起。当元素设置了相对定时，周边的元素也能看到相对定位元素的默认位置。（也就是说，相对定位元素的默认位置还是被元素自身占用，别的元素是无法占用的。也就是说相对定位元素的位移是相对于元素自身的边缘进行位移）。

**HTML**

```
<div class="box-set">
  <div class="box">Box 1</div>
  <div class="box">Box 2</div>
  <div class="box">Box 3</div>
</div>	

```

**CSS**

```
.box-set {
  background: #e8eae9;
}
.box {
  background: #8ec63f;
  height: 80px;
  position: relative;
  width: 80px;
}
.box-1 {
    top: 20px;
  }
.box-2 {
  left: 40px;
}
.box-3 {
  bottom: -10px;
  right: 20px;
}	

```

**效果：**

![相对定位](http://cdn2.w3cplus.com/cdn/farfuture/LLfQ0jUm5TIZtdIjfW1BQZNO1Q0AhR43QGUzHBcXWjw/mtime:1421035049/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson2-6.jpg)

事实上，一个相对定位元素同时设置了“top”和“bottom”位移属性值，实际上“top”优先级高于“bottom”。然而，一个相对定位元素同时设置了“left”和“right”位移属性，他们的优先级取决于页面使用的是哪种语言，例如，如果你的页面是英文页面，那么“left”位移属性优先级高，如果你的页面是阿拉伯语，那么“right”的位移属性优先级高。

**Position absolute**

绝对定位元素也具有盒子位移属性，然而，绝对定位元素会脱离文档流。绝对定位元素直接从文档流中移出，绝对定位元素的位置直接和父容器是否设置了相对定位（绝对定位）有直接关系。绝对定位元素需要至少一个祖先元素设置了相对定位（绝对定位），不然元素定位会相对于页面的主体进行定位。

使用绝对定位的元素可以指定垂直和水平的位移属性，使绝对定位元素相对于设置了相对定们的祖先元素边缘进行移位。例如，一个绝对定位的元素设置了“top”值为“50px”和一个“right”值为“100px”,绝对定位元素会相对于其设置了相对定位的父元素的顶边向下移动50px;向左移动100px。

然而，使用了绝对定位的元素并没有进行任何盒子位移属性设置，那么绝对定位元素的顶部和左部会和设置了相对定位的父元素的顶边和左边重合。如果设置了一个盒子位移属性，比如说“top”，那么绝对定位元素垂直方向会进行移动，而水平位置默认还是左边对齐。

在下面的演示中，你可以看到所有的盒子都相对于div的父元素进行绝对定位，每个元素都从特定的面使用定位值进行移动，而且使用了负值的，元素移动到盒子的外面。

**HTML**

```
<div class="box-set">
  <div class="box">Box 1</div>
  <div class="box">Box 2</div>
  <div class="box">Box 3</div>
</div>	

```

**CSS**

```
.box-set {
  background: #e8eae9;
  height: 200px;
  position: relative;
}
.box {
  background: #8ec63f;
  height: 80px;
  position: absolute;
  width: 80px;
}
.box-1 {
  top: 6%;
  left: 2%;
}
.box-2 {
  top: 0;
  right: -40px;
}
.box-3 {
  bottom: -10px;
  right: 20px;
}
.box-4 {
  bottom: 0;
}	

```

**效果**

![绝对定位](http://cdn1.w3cplus.com/cdn/farfuture/x28NFiadRzoY7yvC0Eszbs7kPI0RDHnV7kuZRDwOeFY/mtime:1421035050/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson2-7.jpg)

当一个绝对定位的元素有固定的高度和宽度，并且盒子位移同时设置了“top”和“bottom”时，“top”更具优先组，另外和相对定位元素一样，当同时设置了“left”和“right”时，优先级取决于他的页面使用的语言。

当一个绝对定位的元素没有明确指定高度和宽度，同时使用盒子位移的“top”和“bottom”属性时，会使整个元素的高度跨越整个容器。同样的，当这个元素同时使用位移“left”和“right”属性值，会使整个元素的宽度跨越整个容器。如果同时使用位移四个属性，可以指定一个宽度和高度显示元素。（这个时候绝对定位元素的宽度和高度都是100%。）

**Position fixed**

固定定位和绝对定位很类似，但是他定位是相对于浏览器窗口，并且不会随滚动条进行滚动。也就是说，不管用户停留在页面那个地方，固定定位的元素将始终停留在页面的一个地方。“position”属性值中，仅有“fixed”属性值不能在IE6浏览器下运行，如果你想在IE6正常使用固定定位，那么你就需要为他写一些Hacks。

固定定位元素的盒子位移属性的使用和绝对定位的一样。

保持前面盒子移位，可以看到盒子固定定位是相对于浏览器窗口而不是设置了相对定位的父元素。

**HTML**

```
<div class="box-set">
  <div class="box">Box 1</div>
  <div class="box">Box 2</div>
  <div class="box">Box 3</div>
</div>	

```

**CSS**

```
.box {
  background: #8ec63f;
  height: 80px;
  position: fixed;
  width: 80px;
}
.box-1 {
  top: 6%;
  left: 2%;
}
.box-2 {
  top: 0;
  right: -40px;
}
.box-3 {
  bottom: -10px;
  right: 20px;
}
.box-4 {
  bottom: 0;
}	

```

**效果**

![绝对定位](http://cdn1.w3cplus.com/cdn/farfuture/-Vt_ajn1Rnp98-kPRqyjXuvDuvtSpwq7qbBdmiPTfWM/mtime:1421035050/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson2-8.jpg)

**固定页头和页脚**

固定定位最常见的一种用途就是在页面中创建一个固定头部、或者脚部、或者固定页面的一个侧面。就算是用户移动浏览器的滚动条，还是固定在页现与用户交流。

下面的示例代码能实现。注意如何设置“left”和“right”两个盒子位移，这使得“页脚”跨越了页面的整个宽度，而不需使用margin、border和padding来破坏盒模形就做了收缩自如。

**HTML**

```
< footer >Fixed Footer </footer>	

```

**CSS**

```
footer {
  bottom: 0;
  left: 0;
  position: fixed;
  right: 0;
}	

```

![固定定位](http://cdn2.w3cplus.com/cdn/farfuture/yZNMwZB8YUnk78KrRwGt9SI2wvpcMV-FRqVYqgCvgqY/mtime:1421035050/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson2-9.jpg)

#### z-index属性

通常都认为Web页面是二维页面，显示的元素都在X轴和Y轴上。当你的元素有定位时，他们有时候会放置在另一个元素的顶部。要改变这些元素是一个 [怎么样的层叠顺序](http://www.impressivewebs.com/a-detailed-look-at-the-z-index-css-property/)，要知道z轴，z轴是用“z-index”属性来控制的。

一般来说，在DOM中，元素出现的时候就放置在z轴上。在Dom中，元素在顶部的要低于底部的。改变这种层叠顺序可以直接使用“z-index”来控制。元素的“z-index”值越高将会出现在越上面，不管元素在Dom哪个位置上。

给元素设置“z-index”属性，首先要在这个元素上设置了“position”属性值为“relatvie”、“absolute”或者“fixed”之一。同样的，你要使用盒子位移属性，你也要先确认元素设置了“positions”属性值为“relative”、“absolute”或者“fixed”之一。

在下面的登例子中，如果每个盒子都不设置“z-index”，那么第一个box在第二个下面，第二个在第三个下面，第三个在第四个下面。如果在盒子中指定“z-index”的值，第二个盒子在第一个和第三个上面，第三个盒子在第四个上面。

**HTML**

```
<div class="box-set">
  <div class="box">Box 1</div>
  <div class="box">Box 2</div>
  <div class="box">Box 3</div>
</div>  

```

**CSS**

```
 .box-set {
  background: #e8eae9;
  height: 160px;
  position: relative;
}
.box {
  background: #8ec63f;
  border: 3px solid #f7941d;
  position: absolute;
}
.box-1 {
  left: 10px;
  top: 10px;
}
.box-2 {
  bottom: 10px;
  left: 70px;
  z-index: 3;
}
.box-3 {
  left: 130px;
  top: 10px;
  z-index: 2;
}
.box-4 {
  bottom: 10px;
  left: 190px;
  z-index: 1;
} 

```

**不设置z-index效果**

![固定定位](http://cdn.w3cplus.com/cdn/farfuture/nYS2wW3PKhR6YP0QF1ehJifgjWACiNsV5toiWo7mOqM/mtime:1421035050/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson2-10.jpg)

**设置z-index效果**

![固定定位](http://cdn2.w3cplus.com/cdn/farfuture/0E2L3mATuiRsv5SlN-j7n0btTopdyy0QyqRE99hSq_U/mtime:1421035050/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson2-11.jpg)

#### 扩展阅读

1.  [CSS的Float之一](http://www.w3cplus.com/css/css-containing-floats)
2.  [CSS的Float之二](http://www.w3cplus.com/css/css-containing-floats-part-2)
3.  [CSS Float Theory: Things You Should Know](http://coding.smashingmagazine.com/2007/05/01/css-float-theory-things-you-should-know/)
4.  [All About Floats](http://css-tricks.com/all-about-floats/)
5.  [Methods for Containing Floats](http://www.ejeliot.com/blog/59)
6.  [CSS Floats 101](http://alistapart.com/article/css-floats-101)
7.  [Everything You Never Knew About CSS Floats](http://designshack.net/articles/css/everything-you-never-knew-about-css-floats/)
8.  [SIMPLE TIPS ON CONTAINING FLOATS](http://pageaffairs.com/notebook/containing-floats)
9.  [Clear Float](http://www.w3cplus.com/css/clear-float)
10.  [Clearing floats nowadays](http://www.red-team-design.com/clearing-floats-nowadays)
11.  [CSS Hackz Series: Clearing Floats with the Clearfix Hack](http://perishablepress.com/css-hackz-series-clearing-floats-with-the-clearfix-hack/)
12.  [十步图解CSS的position](http://www.w3cplus.com/css/learn-css-positioningin-ten-steps)
13.  [A New Micro Clearfix Hack](http://nicolasgallagher.com/micro-clearfix-hack)
14.  [CSS Positioning 101](http://www.alistapart.com/articles/css-positioning-101)
15.  [On Having layout](http://www.satzansatz.de/cssd/onhavinglayout.html)
16.  [A Detailed Look at the z-index CSS Property](http://www.impressivewebs.com/a-detailed-look-at-the-z-index-css-property)
17.  [The Z-Index CSS Property: A Comprehensive Look](http://coding.smashingmagazine.com/2009/09/15/the-z-index-css-property-a-comprehensive-look/)

[上一课](http://www.w3cplus.com/css/advanced-html-css-lesson1-performance-organization.html)[下一课](http://www.w3cplus.com/css/advanced-html-css-lesson3-complex-selectors.html)

**译者手语：**整个翻译依照原文线路进行，并在翻译过程略加了个人对技术的理解。如果翻译有不对之处，还烦请同行朋友指点。谢谢！

如需转载烦请注明出处：

英文原文：[http://learn.shayhowe.com/advanced-html-css/detailed-css-positioning](http://learn.shayhowe.com/advanced-html-css/detailed-css-positioning)

中文译文：[http://www.w3cplus.com/css/advanced-html-css-lesson2-detailed-css-positioning.html](http://www.w3cplus.com/css/advanced-html-css-lesson2-detailed-css-positioning.html)