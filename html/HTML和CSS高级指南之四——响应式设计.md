# HTML和CSS高级指南之四——响应式设计

> 本文由[D姐](http://www.cnblogs.com/different/)根据[Shay Howe](http://shayhowe.com/)的《[An Adavnced Guide to HTML & CSS](http://learn.shayhowe.com/advanced-html-css/)》第四课《[Responsive Web Design](http://learn.shayhowe.com/advanced-html-css/responsive-web-design)》所译，整个译文带有我们自己的理解与思想，如果译得不好或不对之处还请同行朋友指点。如需转载此译文，需注明英文出处：[http://learn.shayhowe.com/advanced-html-css/responsive-web-design](http://learn.shayhowe.com/advanced-html-css/responsive-web-design)，以及作者相关信息

互联网发展的速度超乎所有人的想象，甚至可以说是疯狂。在过去几年里，移动互联网的发展已经开始崭露头角。而他的发展速度也远远超过了传统互联网。

如今很难找到一个人既没有移动设备，也没有多个可以上网的设备。在英国 [移动电话](http://www.gpmd.co.uk/blog/2012-mobile-internet-statistics/)的数量已远远超过人口数，保持这样的 [增长势头](http://www.digitalbuzzblog.com/2011-mobile-statistics-stats-facts-marketing-infographic/)，今年移动互联网的使用应该就有望超过桌面互联网。

随着移动互联网的兴起，也带来了一个问题，就是如何搭建一个网站，可以适合所有用户访问。行业对于这个问题的回答是响应式设计，也就是熟知的RWD。

**第四课所涉及的主要内容**

HTML

-  [响应式设计概述](http://www.w3cplus.com/css/advanced-html-css-lesson4-responsive-web-design.html#responsiveOverview)
-  [视窗](http://www.w3cplus.com/css/advanced-html-css-lesson4-responsive-web-design.html#viewport)

CSS

-  [流式布局](http://www.w3cplus.com/css/advanced-html-css-lesson4-responsive-web-design.html#flexibleLayouts)
-  [媒体查询](http://www.w3cplus.com/css/advanced-html-css-lesson4-responsive-web-design.html#MediaQueries)
-  [移动第一](http://www.w3cplus.com/css/advanced-html-css-lesson4-responsive-web-design.html#mobileFirst)
-  [流式媒体](http://www.w3cplus.com/css/advanced-html-css-lesson4-responsive-web-design.html#flexbleMedia)

#### 响应式设计概述

响应式设计是一个网站搭建的实践尝试，他使得每种设备和屏幕尺寸都能很好的工作，而不论是大屏还是小屏，手机或是pc。响应式设计关注于提供每个人一个直观的感受和满足。使得pc和手机用户都能够从中受益。

[响应式设计](http://alistapart.com/article/responsive-web-design)本身的很多术语是由[Ethan Marcotte](http://alistapart.com/author/emarcotte)提出的。他们第一次出现在Ethan在线访谈和他的书中，而且[响应式](http://www.abookapart.com/products/responsive-web-design/)这本书也是很值得一读的。

![响应式设计](http://cdn.w3cplus.com/cdn/farfuture/qgrp091zgDsrxYleGLfc1e9ttNvNtt68RvJsH-FAxUk/mtime:1421035053/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson4-1.jpg)

[Food Sense](http://foodsense.is/)是个很漂亮的网站，他响应所有不同的设备尺寸。不管设备尺寸大小如何，食物感官网站都可以轻松适应，给用户一个很自然的用户体验。（如上图所示）

**响应式、自适应、移动的区别**

响应式中的一些术语可能并不是新的，而其他术语又跟自适应或是移动有点像。那么你也许会困惑，他们之间的区别到底是什么?

响应式和自适应的关系很密切，经常二者是互通的。响应式通常意味着对待任何变化，反应更积极更快。而自适应往往是应对一个新需求或是情况的被动反应，例如变化。响应式设计应对不同因素的变化，都会很流畅自如，例如设备宽度。而自适应设计会基于一定的因素搭建。将二者结合是一种理想化，提供一个完美功能模式的网站，这个术语不会产生很大的歧义。

另一方面，移动设备，通常意味着需要为移动用户，专门搭建一个移动网站。然而这样做可能有些作用，却不是很好的主意。移动网站要求必须非常轻巧，然而他又很依赖一个新的代码库和浏览器的嗅探。所有的这些都是摆在开发者和用户面前的一个障碍。

目前在响应式设计中最流行的技术，就是对于不同浏览器和设备的动态布局设计，他会根据不同的浏览器和设备尺寸的变化，动态改变网页的布局和内容。这个解决方案充分发挥了响应式，自适应和移动设备的三方优势。

> #### 扩展阅读
>
> 1.  [Responsive Web Design](http://www.w3cplus.com/css3/responsive-web-design.html)
> 2.  [Responsive设计的十个基本技巧](http://www.w3cplus.com/css3/10-basic-tips-about-responsive-design.html)
> 3.  [Responsive设计的关键三步](http://www.w3cplus.com/css3/responsive-design-in-3-steps)
> 4.  [了解Responsive网页设计的三个特性](http://www.w3cplus.com/css3/understanding-the-elements-of-responsive-web-design)
> 5.  [Responsive列布局](http://www.w3cplus.com/css3/responsive-column-layouts.html)
> 6.  [响应式导航菜单在移动端的制作方法与解决方案](http://www.w3cplus.com/css3/responsive-mobile-navigation-menumethods-and-solutions.html)
> 7.  [基于CSS搭建一个响应式网站](http://www.w3cplus.com/css3/build-basic-responsive-site-css.html)
> 8.  [Responsive教程集（W3cplus提供）](http://www.w3cplus.com/blog/tags/79.html)
> 9.  [Responsive资源集（W3cplus提供）](http://www.w3cplus.com/resource/tags/153.html)
> 10.  [Responsive Web Design](http://www.alistapart.com/articles/responsive-web-design/)
> 11.  [Viewport Percentage Lengths](http://dev.w3.org/csswg/css3-values/#viewport-relative-lengths)
> 12.  [CSS Media Queries](http://css-tricks.com/css-media-queries/)
> 13.  [Mobile First Presentation](http://www.lukew.com/presos/preso.asp?26) via Luke Wroblewski
> 14.  [An Introduction to Meta Viewport and @viewport](http://dev.opera.com/articles/view/an-introduction-to-meta-viewport-and-viewport/)
>
> [大漠](http://www.w3cplus.com/)

#### 流式布局

响应式设计主要有三部分组成：流式布局，媒体查询和灵活的媒体类型。第一部分，流式布局，就是用灵活的网格搭建一个网站布局，它可以动态的调整以适应于任何宽度。网格布局使用相对长度单位，通常是百分比或是em。这些相对长度多用于网格，诸如宽度，间距或是留白等属性。

**相对视窗长度**

Css3中引入一些新的相对长度，他们是针对浏览器或是设备视窗尺寸的，这些新单位包括vw，wh，vmin和vmax。目前支持他们的设备或是浏览器并不多，但是支持他们的数量在不断增长。他们在搭建响应式网站发挥很大的作用。

-  **vw:**视窗宽度;
-  **vh:**视窗高度;
-  **vmin:**视窗最小尺寸;
-  **vmax:**视窗最大尺寸;

> #### 相对视窗长度扩展阅读：
>
> 1.  [Combining meta viewport and media queries](http://www.quirksmode.org/blog/archives/2010/09/combining_meta.html)
> 2.  [A tale of two viewports — part two](http://www.quirksmode.org/mobile/viewports2.html)
> 3.  [Learning to Love the Boring Bits of CSS](http://alistapart.com/article/love-the-boring-bits-of-css)
> 4.  [An introduction to meta viewport and @viewport](http://dev.opera.com/articles/view/an-introduction-to-meta-viewport-and-viewport/)
> 5.  [SIZING WITH CSS3'S VW AND VH UNITS](http://snook.ca/archives/html_and_css/vm-vh-units)
> 6.  [CSS Length](https://developer.mozilla.org/en-US/docs/CSS/length)
> 7.  [New Viewport-relative Units](http://blog.teamtreehouse.com/new-viewport-relative-units)
> 8.  [@-ms-viewport rule](http://msdn.microsoft.com/en-us/library/ie/hh869615(v=vs.85).aspx)
> 9.  [CSS Values and Units Module Level 3](http://dev.bowdenweb.com/css/values-and-units.html)
>
> [大漠](http://www.w3cplus.com/)

流式布局不推荐使用固定单位，如px或是英寸。因为屏幕的宽高会随着设备的不同而改变。网站布局需要适应这种变化，而固定单位有太多的限制。幸运的是，Ethan指出用一个简单的公式，就可以在流式布局中使用相对值。

公式是用目标元素的宽度除以他父元素的宽度，结果就是目标元素的相对宽度：

```
target ÷ context = result	

```

**灵活网格**

让我们看看这个公式在两列布局中是如何运用的。一个container的div，包裹着section和aside两个元素。Section在左aside在右，他们之间是相等的间距。这样布局的结构和样式大致如下:

**HTML**

```
<div class="container">
  <section>...</section>
  <aside>...</aside>
</div>	

```

**CSS**

```
.container {
  width: 660px;
}
section {
  float: left;
  margin: 10px;
  width: 420px;
}
aside {
  float: right;
  margin: 10px;
  width: 200px;
}	

```

**效果：**

![灵活网格](http://cdn2.w3cplus.com/cdn/farfuture/13vgoDLNt0RF64jCC2sKuPcgWLnHHIjYyXDL3QJhRpw/mtime:1421035053/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson4-2.jpg)

使用网格公式我们可以把固定长度换算成相对单位长度。这个例子中我们将使用百分比，他跟em有相同的效果。注意，不管容器变的多宽，section和aside之间的间距和宽度都会按照比例变化。

```
.container {
  max-width: 660px;
}
section {
  float: left;
  margin: 1.51515151%;   /*  10px ÷ 660px = .01515151 */
  width: 63.63636363%;   /* 420px ÷ 660px = .63636363 */   
}
aside {
  float: right;
  margin: 1.51515151%;   /*  10px ÷ 660px = .01515151 */
  width: 30.30303030%;   /* 200px ÷ 660px = .30303030 */
}	

```

**效果**

![灵活网格](http://cdn.w3cplus.com/cdn/farfuture/-IxpCjcf0nIAQSl_a2Qd1RBJ5Gzcpm4IOXEKLEw82z0/mtime:1421035053/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson4-3.jpg)

采用流式布局概念和公式，把他们运用到网格的所有部分，就可以创建一个完全动态的网站了，它可以适应各种尺寸的设备。为了更好的控制流式布局，你也可以使用最小宽度（min-width），最大宽度（max-width），最小高度（min-height）和最大高度（max-height），把他们应用到容器元素(container)上。

仅仅有流式布局是不够的。有时浏览器的显示窗口宽度可能很小，以至于按照缩放比例得到的布局，创建出来的列太小不能有效的显示内容。具体说，就是当布局太小或是太大，内容可能难以辨认，布局也可能遭到破坏。在这种情况下，媒体查询就用来辅助建立一个更好的用户体验。

> #### 灵活网格扩展阅读
>
> 1.  [CREATE A FLEXIBLE LAYOUT](http://blendinsider.com/tutorial/blend-tutorial-part-4-create-a-flexible-layout-memory-game-2012-1-20/)
> 2.  [FLEXIBLE WEB DESIGN](http://www.flexiblewebbook.com/)
> 3.  [Writing a Flexible Grid Script for Photoshop](http://webdesign.tutsplus.com/tutorials/javascript-tutorials/writing-a-flexible-grid-script-for-photoshop/)
> 4.  [Don’t Overthink It Grids](http://css-tricks.com/dont-overthink-it-grids/)
> 5.  [Blankwork:Simple, Flexible and Semantic](http://www.blankwork.net/)
> 6.  [5grid](http://n33.co/files/5grid/docs/)
> 7.  [Responsive设计的十个基本技巧](http://www.w3cplus.com/css3/10-basic-tips-about-responsive-design.html)
> 8.  [Mobile Responsive Design: The Flexible Grid](http://www.studiopress.com/design/flexible-grid.htm)
> 9.  [Flexibility: A Foundation for Responsive Design](http://msdn.microsoft.com/en-us/magazine/hh912616.aspx)
> 10.  [Going From Adaptive To Fully Responsive](http://www.leemunroe.com/adaptive-responsive/)
> 11.  [Responsive Web Design](http://msdn.microsoft.com/en-us/magazine/hh653584.aspx)
> 12.  [Gridpak: The Responsive Grid Generator](http://coding.smashingmagazine.com/2012/03/19/gridpak-the-responsive-grid-generator/)
> 13.  [Five steps to gettin’ flexy in responsive web design](http://www.netmagazine.com/features/five-steps-gettin-flexy-responsive-web-design)
> 14.  [30+ CSS Grid System](http://www.w3cplus.com/source/30-css-grid-system.html)
> 15.  [8个实用的响应式设计框架](http://www.w3cplus.com/source/8-useful-responsive-css-frameworks.html)
>
> [大漠](http://www.w3cplus.com/)

#### 媒体查询

媒体查询是对媒体类型的一个扩展，因为经常发现目标设备自带样式，他为特定的浏览器和设备提供特殊的样式。能够为目标设备提供有针对性的样式，在响应式设计中发挥作用。

**初始化媒体查询**

有好几种方式使用媒体查询，在现有样式表中使用@media规则，或是在一个新样式表里使用@import规则，或是用link标签给html文档引用一个单独的样式表。通常推荐在现有样式表中使用@media规则，以避免多次发送http请求：

**HTML**

```
<!-- Separate CSS File -->
<link href="styles.css" rel="stylesheet" media="all and (max-width: 1024px)">

```

**CSS**

```
/* @media Rule */
@media all and (max-width: 1024px) {...}
/* @import Rule */
@import url(styles.css) all and (max-width: 1024px) {...}	

```

每个媒体查询可以包含一个或多个媒体类型。常见的媒体类型有所有(all)，屏幕（screen），打印（print），电视（tv）和盲文（braille）。Html5中又添加了新的媒体类型，甚至包含3d眼镜（3d-glasses）。一个没有特别声明媒体类型的媒体查询，默认媒体类型是屏幕（screen）。

媒体查询表达式可能包含不同的媒体属性和属性值，然后分配是真还是假。当一个媒体属性和值都为真时，应用样式，否则忽略样式。

**媒体查询中的逻辑运算符**

媒体查询中的逻辑运算符，帮助建立强大的表达式。在媒体查询中有三个不同的逻辑运算符，分别是与(and)，非（not）和唯一（only）。

在媒体查询中使用与逻辑运算符，容许添加额外的条件，以确保浏览器或是设备同时满足a，b，c条件等等。多个媒体查询可以用逗号分开，作为一个筛选条件。下面的例子就是选择满足宽度在800到1024之间的所有设备。

```
@media all and (min-width: 800px) and (max-width: 1024px) {...}	

```

在查询中的非逻辑运算符，表示除了满足查询条件设备的所有设备都适用。在这个例子表达式，就是应用于任何设备除了彩屏的，黑白屏或是单色屏幕都适用。

```
@media not screen and (color) {...}	

```

唯一的逻辑运算符是一个新运算符，不识别html4算法的用户代理，所以隐藏设备或是浏览器不支持的媒体查询样式。下面表达式只匹配屏幕方向是竖屏，能够渲染的媒体查询的用户代理。

```
@media only screen and (orientation: portrait) {...}	

```

**忽略一个媒体类型**

当同时使用非和唯一逻辑运算符，媒体类型就会失效，这种情况下媒体类型是默认的所有设备。

**在媒体查询中的媒体特性**

了解媒体查询的语法和逻辑运算符如何工作，对于媒体查询而言是个了不起的事情，但是真正工作的却是媒体特性。媒体属性可以识别出在媒体查询表达式中，有针对的属性是什么？

**媒体特性中的宽高**

最常见的一种媒体特性围绕设备或浏览器视窗的宽高。这些尺寸可以使用媒体特性中的height，width，device-height和 device-width获取到，并且这些特性均可以用min或max作为前缀，建立例如min-width 或 max-device-width的特性。

宽高基于视窗渲染区域的宽高而定，以浏览器窗口为例。另一方面，设备高度和设备宽度特性，是基于输出设备的宽高，他们也许大于实际的渲染区域。这些宽高媒体特性可以使用任何相对或绝对的长度单位。

```
@media all and (min-width: 320px) and (max-width: 780px) {...}	

```

在响应式设计中使用最多的特性是最小宽度和最大宽度，它有助于在台式机和移动设备搭建同样的响应式网站，避免与设备特性的混淆。

**使用最大最小前缀**

最大最小前缀在媒体特性中有相当多的地方使用。最小前缀表示一个值大于或是等于，而最大前缀表示一个值小于或是等于。使用最大最小前缀避免与html普通语法冲突，尤其不用使用<和>符号

**屏幕方向媒体特性**

屏幕方向媒体特性决定一个设备是处于横屏还是竖屏。横屏模式显示宽大于高，而竖屏模式触发高大于宽。这个媒体特性在移动设备上发挥很大的作用。

```
@media all and (orientation: landscape) {...}	

```

**长宽比媒体特性**

长宽比与设备长宽比，均是指目标呈现区域或输出设备的宽高像素比。min和max前缀可以适用不同长宽比特性。用于确定当前状态是一个比率高还是低。

长宽比是包括两个正数由斜杠分隔。第一个整数表示像数宽度，第二个整数表示像数高度。

```
@media all and (min-device-pixel-ratio: 16/9) {...}	

```

**像素比特性**

除了长度比外还有像素比媒体特性。这些特性包含设备像素比也有min和max前缀。具体来说，像素比功能非常时候高清设备，包括视网膜屏幕。这样的媒体查询要如下这样写。

```
@media only screen and (-webkit-min-device-pixel-ratio: 1.3), only screen and (min-device-pixel-ratio: 1.3) {
...
}	

```

**分辨率媒体特性**

这个媒体特性是指在输出设备上的像素密度，也就是常说的每英寸的像素点数或是DPI。这个媒体特性也接受min和max前缀。此外，这个媒体特性可以表示，每像素多少点数(如1.3 dppx，表示每像素1.3个像素点),每厘米多少点数(如118 dpcm表示每厘米118个像素点),和其他长度单位的分辨率。

```
@media print and (min-resolution: 300dpi) {...}	

```

**其他媒体特性**

其他媒体特性包括识别使用颜色的可输出颜色，颜色指数，单色特性，带有网格特性的识别位图设备，识别具有扫描功能的电视。这些特性虽不常用，但在需要的时候很有用。

**媒体查询浏览器支持**

不幸的是，媒体查询在ie8及其以下的浏览器不能支持。不过，幸好有一些插件对它们进行处理兼容。

[Respond.js](https://github.com/scottjehl/Respond/)是一个轻量级的插件，只是查找媒体查询中的min/max-width，在那些只使用媒体查询中完美的适用。[CSS3-MediaQueries.js](http://code.google.com/p/css3-mediaqueries-js/)是一个更复杂，功能更强大的插件，支持更复杂的媒体查询。不过，记住一点，就是任何插件都会有性能问题，也就是放缓网站的访问速度。所以在使用插件前要确保这个性能的损失是值得的。

**媒体查询demo**

现在我们使用媒体查询重新写一下之前写的流式布局。现在demo面临的一个问题是，在一个小屏幕设备上侧栏变得无限小。用媒体查询为尺寸在420以下的设备改变布局，去掉section和aside的宽度和浮动。

```
@media all and (max-width: 420px) {
  section, aside {
    float: none;
    width: auto;
  }
}	

```

![媒体查询](http://cdn2.w3cplus.com/cdn/farfuture/dOqlquRFY6RsS3_KAJGAjsasrEHRr4EM8vO3dX-Z9_o/mtime:1421035053/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson4-4.jpg)

上图是没有媒体查询的section和aside会变的很小。而太小可能不能装下真正的内容。

![媒体查询](http://cdn.w3cplus.com/cdn/farfuture/gTXDjhdV4Sz5bj5hXhQJlZZsV_3ppHtTjdxtCQAi9M4/mtime:1421035054/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson4-5.jpg)

上图运用媒体查询去掉section和aside的宽度和浮动，使他们能够全屏显示，容许他们的内容占据所有空间。

**断点识别**

你的直觉可能告诉你在写媒体查询时，要根据常见的视窗尺寸设置断点，用以判断不同的分辨率，例如320px,480px,768px, 1024px, 1224px等等。但这是个坏主意。

在搭建响应式网站时，应该可以适应各种不同视窗尺寸，而不需要考虑设备的分辨率。设置断点只是在网站布局被破坏，看起来很怪或是内容无法显示的时候才需要设置。

此外，每时每刻都会有新设备和新分辨率在发布。而试图跟上这些变化可能是个无止境的过程。

> #### 扩展阅读
>
> 1.  [CSS3 Media Queries](http://www.w3cplus.com/content/css3-media-queries)
> 2.  [CSS3 Media Queries模板](http://www.w3cplus.com/css3/css3-media-queries-for-different-devices)
> 3.  [Responsive设计和CSS3 Media Queries的结合](http://www.w3cplus.com/css3/responsive-design-with-css3-media-queries)
> 4.  [CSS3 Media Queries在iPhone4和iPad上的运用](http://www.w3cplus.com/css3/css3-media-queries-for-iPhone-and-iPads)
> 5.  [iPads和iPones的Media Queries](http://www.w3cplus.com/css3/css-media-queries-for-iPads-and-iPhones.html)
> 6.  [CSS3 Media Queries案例——Hicksdesign](http://www.w3cplus.com/css3/media-queries-hicksdesign)
> 7.  [CSS3 Media Queries案例——A List Apart](http://www.w3cplus.com/css3/media-queries-alistpart)
> 8.  [CSS3 Media Queries案例——Tee Gallery](http://www.w3cplus.com/css3/media-queries-tee-gallery)
> 9.  [W3CPLUS上Media Queries教程集合](http://www.w3cplus.com/blog/tags/49.html)
> 10.  [media query ie8- 兼容实现总结](http://www.36ria.com/5960)
> 11.  [CSS Media Queries & Using Available Space](http://css-tricks.com/css-media-queries/)
> 12.  [Introduction to media queries – Part 1: What are media queries?](http://www.adobe.com/devnet/dreamweaver/articles/introducing-media-queries.html)
> 13.  [http://www.adobe.com/devnet/dreamweaver/articles/introducing-media-queries-pt2.html](http://www.adobe.com/devnet/dreamweaver/articles/introducing-media-queries-pt2.html)
> 14.  [Media Queries (Windows)](http://msdn.microsoft.com/en-us/library/windows/apps/hh453556.aspx)
> 15.  [CSS Media Queries](http://cssmediaqueries.com/)
> 16.  [Media Queries Tutorial – Convert Burnstudio into a Responsive Website](http://www.1stwebdesigner.com/css/media-queries-tutorial-convert-burnstudio-responsive-website/)
> 17.  [Breaking Down Media Queries for Responsive Web Design](http://www.1stwebdesigner.com/design/media-queries-for-responsive-web-design/)
> 18.  [Media Query splitting](http://simurai.com/post/30451824480/media-query-splitting)
> 19.  [Techniques For Gracefully Degrading Media Queries](http://coding.smashingmagazine.com/2011/08/10/techniques-for-gracefully-degrading-media-queries/)
>
> [大漠](http://www.w3cplus.com/)

#### 移动第一

使用媒体查询中的一个先进技术，就是移动优先。移动优先方法是指，先在小视窗加载网站默认样式，然后再添加用媒体查询设置的视窗样式。

移动优先背后的操作理念就是，一个移动设备的用户，通常使用小视窗的设备，不应该加载pc机上面的所有样式，之后又加载为移动设备写的样式。如此一来浪费了带宽，而带宽对于任何搜索漂亮网站的用户来说，都是很宝贵的。

移动优先方法也提出为移动用户设置一定的限制。在不久的将来，大多数的网络消费将在移动设备上进行。所以理应为他们设计相应的移动体验。

移动优先的媒体查询可能如下：

```
/* Default styles first then media queries */
@media screen and (min-width: 400px)  {...}
@media screen and (min-width: 600px)  {...}
@media screen and (min-width: 1000px) {...}
@media screen and (min-width: 1400px) {...}	

```

此外，下载不需要的媒体资源可以用媒体查询停止。通常来说，避免css3的阴影，渐变，动画，移动的过度使用，否则会造成加载过慢，甚至有损电池的寿命。

```
/* Default media */
body {
  background: #ddd;
}
/* Media for larger devices */
@media screen and (min-width: 800px) {
  body {
    background-image: url("bg.png") 50% 50% no-repeat;
  }
}	

```

**移动第一案例**

给我们前面的例子添加媒体查询，之前重写的样式是为了，尺寸小于420像素宽度的视窗下有个不错的布局。这次首先重写默认的手机样式，然后添加媒体查询，为了适应视窗尺寸大于420像素宽度。

查看代码如下：

```
section, aside {
  margin: 1.51515151%;
}
@media all and (min-width: 420px) {
  .container {
    max-width: 660px;
  }
  section {
    float: left;
    width: 63.63636363%;
  }
  aside {
    float: right;
    width: 30.30303030%;
  }
}	

```

注意，这部分代码跟以前一样，唯一的区别就是，移动设备只需要渲染一个css声明。只不过在大视窗设备所有其他样式延迟加载，并没有覆盖最初的样式。

#### 视窗

如今用移动设备显示网站是一个很cool的事情。虽然有时辅助帮助有点不到位，特别是视窗的尺寸规模，对网站的处理。为了解决这些问题，苹果发明了视窗meta标签。

![视窗](http://cdn1.w3cplus.com/cdn/farfuture/6zpYhx9vk72vOeLQcu11J7oPh0OK3TlW9KZ2saUV8QA/mtime:1421035054/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson4-6.jpg)

尽管这个demo里面有媒体查询，但是许多移动设备仍然不知道网站的初始宽度或是规模，所以也就无法解析媒体查询。

**视窗宽高**

使用视窗meta标签，那么视窗的宽高需要分别定义。每个值可以是正值或是关键字。高度属性用device-height表示，相应的宽度属性用device-width表示。这些关键字继承设备默认的宽高。

一个看上去很棒的网站的最好的处理方式，建议你使用设备高度和设备宽度作为设备默认值。

```
<meta name="viewport" content="width=device-width">	

```

![视窗](http://cdn1.w3cplus.com/cdn/farfuture/cnCezQGoKxeEwMruEK_KiPUQ1q2idjcBAacsltTSENQ/mtime:1421035054/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson4-7.jpg)

让设备知道网站的预定宽度，在这种情况的设备宽度，容许应用媒体查询对网站的尺寸，做出适当调整。

**视窗比例**

如何控制一个网站在手机设备上的显示比例，可以通过minimum-scale, maximum-scale, initial-scale,和 user-scalable 四个属性来控制。

一个网站的初始比例应该设置为1，这样定义的比例是在设备高度和视窗高度之间，而竖屏时候，初始比例就是视窗尺寸。同样横屏的初始比例应该是在设备宽度和视窗宽度之间。视窗比例应该始终是0到10之间的正数。

```
<meta name="viewport" content="initial-scale=2">	

```

![视窗](http://cdn1.w3cplus.com/cdn/farfuture/6HKMGyERh1KhUvv9zsoQjhvH1fxB8VHnQzQS0_XDn70/mtime:1421035054/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson4-8.jpg)

如果使用一个大于1的整数比例，使得缩放出的网站比默认比例还大，一般来讲，这个值就应该设置为1。

最大最小范围值是确定视窗可以缩放到多大或是多小。最小范围值是指一个小于等于初始比例的值，同理，最大范围值是指一个大于等于初始比例的值。但这两个值都应该是在0到10 之间。

```
<meta name="viewport" content="minimum-scale=0">	

```

一般来讲，这些值不必设置为相同的初始值。这将禁用缩放，所以完全可以用用户比例代替。设置用户比例不会禁用缩放，相反会自动开启缩放功能。

关闭一个网站的缩放功能是一个坏主意。他不利于残疾人按照他们的意愿浏览一个网站。

```
<meta name="viewport" content="user-scalable=yes">	

```

**视窗分辨率**

让浏览器决定如何缩放，一个基于任何视窗比例的网站，往往是奏效的。当需要更多的控制时，特别是在解决一个设备的分辨率，目标分辨率就派上用场了。这个目标分辨率接受如下值，他们是device-dpi, high-dpi, medium-dpi, low-dpi,或是一个实际的 DPI大小。

目标分辨率（target-densitydpi）值很少使用，但是在需要控制像素尤其有用。

```
<meta name="viewport" content="target-densitydpi=device-dpi">	

```

**组合视窗值**

视窗meta标签接受单独值也接受多个值，容许一次设置多个视窗属性。设置多个值要求他们之间用逗号分割。一个推荐的视窗值设置描述如下，同时使用设备宽度和初始比例属性。

```
<meta name="viewport" content="width=device-width, initial-scale=1">	

```

![视窗](http://cdn1.w3cplus.com/cdn/farfuture/gU75xlZdv79XTYB7iAttmsxJVYbhOWd0JrZ8eZUjvdY/mtime:1421035054/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson4-9.jpg)

设备宽度和初始比例为1的组合视窗属性，就是提供一个初始尺寸和普遍的缩放比例要求。

**Css视窗规则**

因为视窗meta标签需要设置一个网站样式如何渲染，感觉头太重，所以推荐把他从html的meta标签中，移动到使用css样式中定义。这样有助于样式与内容分离，可以提供更多的定义。

目前一些浏览器已经实现了@viewport规则，可是并没有得到广泛的支持。前面推荐的视窗meta标签，在css中也许像下面@viewport这样定义

```
@viewport {
  width: device-width;
  zoom: 1;
}	

```

> #### 扩展阅读
>
> 1.  [视窗meta标签的理解](http://www.w3cplus.com/css/understanding-the-viewport-meta-tag.html)
> 2.  [此像素非彼像素](http://www.w3cplus.com/css/A-pixel-is-not-a-pixel-is-not-a-pixel.html)
> 3.  [响应式新首页设备适配（Device Adaptation）小结](http://www.36ria.com/5986)
> 4.  [Configuring the Viewport](http://developer.apple.com/library/safari/#documentation/AppleApplications/Reference/SafariWebContent/UsingtheViewport/UsingtheViewport.html)
> 5.  [Supported Meta Tags](http://developer.apple.com/library/safari/#documentation/AppleApplications/Reference/SafariHTMLRef/Articles/MetaTags.html#//apple_ref/html/const/viewport)
> 6.  [Using the viewport meta tag to control layout on mobile browsers](https://developer.mozilla.org/en-US/docs/Mobile/Viewport_meta_tag)
> 7.  [Combining meta viewport and media queries](http://www.quirksmode.org/blog/archives/2010/09/combining_meta.html)
> 8.  [A tale of two viewports — part two](http://www.quirksmode.org/mobile/viewports2.html)
> 9.  [Vexing Viewports](http://alistapart.com/article/vexing-viewports)
> 10.  [Viewport.](http://www.themezilla.com/themes/viewport/)
> 11.  [VIEWPORT RESIZER](http://lab.maltewassermann.com/viewport-resizer/)
> 12.  [The Mobile Viewport and Orientation](http://docs.webplatform.org/wiki/tutorials/mobile_viewport)
> 13.  [The viewport metatag (Mobile web part 1)](http://davidbcalhoun.com/2010/viewport-metatag)
> 14.  [Responsive Viewport](http://responsiveviewport.com/)
> 15.  [Media Queries, Viewports, and Responsive Layouts – oh my!](http://harrywolff.com/media-queries-viewports-and-responsive-layouts/)
> 16.  [Viewport Meta Tag For Mobile Devices](http://www.onlywebpro.com/2011/08/30/viewport-meta-tag-for-mobile-devices/)
> 17.  [Metatag viewport tutorial and examples](http://www.eyenoxmedia.nl/blog/metatag-viewport-tutorial-and-examples)
> 18.  [CSS @viewport or Meta Tag?](http://menacingcloud.com/?c=cssViewportOrMetaTag)
> 19.  [Elegantly Resize Your Page With the @-viewport CSS Declaration](http://html5hacks.com/blog/2012/11/28/elegantly-resize-your-page-with-the-at-viewport-css-declaration/)
> 20.  [Quick Tip: Don’t Forget the Viewport Meta Tag](http://webdesign.tutsplus.com/tutorials/htmlcss-tutorials/quick-tip-dont-forget-the-viewport-meta-tag/)
>
> [大漠](http://www.w3cplus.com/)

#### 流式媒体

最后，流式的媒体对于响应式设计也是同等重要的部分。当视窗开始改变尺寸时，媒体大小并不总是做适当改变的。所以图片，视频以及其他媒体类型需要在视窗改变的情况下，按照比例改变大小。

通过使用最大宽度值为100%，是一个快速实现媒体按照比例缩放的方法。这样做可以确保在视窗变小的情况下，任何媒体可以根据他的容器宽度，按照比例缩放 。

```
img, video, canvas {
  max-width: 100%;
}	

```

效果

![流式媒体](http://cdn1.w3cplus.com/cdn/farfuture/oqmhsxIxzxEUSyGWYw6nxMCqdtV4M9gZfKHUd6YcBxU/mtime:1421035055/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson4-10.jpg)

**流式嵌入媒体**

不幸的是最大宽度属性，并不是在所有的媒体上都运行良好，尤其是对于iframe和嵌入媒体。当涉及到第三方的网站，例如YouTube，那些使用iframe来嵌入媒体的，都会因为不起作用而失望。幸好，有个解决办法。

为了让嵌入媒体充分响应，嵌入元素需要在父元素中绝对定位。父元素需要宽度100%，这样缩放才能基于视窗宽度。父元素还需要一个为0的高度，是为了在ie下面触发haslayout。

在父元素底部设置留白，这个值也是依赖于视频的宽高比。他容许父元素的高度跟宽度使用相同的比例。还记得前面提到的响应式设计公式吗？如果一个视频的宽高比是16比9，9除以16等于56.25%，所以底部需要一个56.25%的留白。底部留白而不是头部留白，这是专门用于处理ie5.5的bug，还有父元素是绝对定位的情况。

**HTML**

```
<figure>
  <iframe src="https://www.youtube.com/embed/4Fqg43ozz7A"></iframe>
</figure>

```

**CSS**

```
figure {
  height: 0;
  padding-bottom: 56.25%; /* 16:9 */
  position: relative;
  width: 100%;
}
iframe {
  height: 100%;
  left: 0;
  position: absolute;
  top: 0;
  width: 100%;
}	

```

**效果**

![流式媒体](http://cdn.w3cplus.com/cdn/farfuture/atJUy4fY_TaNSJugExuRbTBstow7Hpn_whJzapbuOC4/mtime:1421035055/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson4-11.jpg)

> #### 扩展阅读
>
> 1.  [Rundown of Handling Flexible Media](http://css-tricks.com/rundown-of-handling-flexible-media/)
> 2.  [Responsive Images: How they Almost Worked and What We Need](http://alistapart.com/article/responsive-images-how-they-almost-worked-and-what-we-need)
> 3.  [FLUID IMAGES](http://unstoppablerobotninja.com/entry/fluid-images/)
> 4.  [How To Create Flexible Images And Media In CSS Layouts](http://www.vanseodesign.com/css/flexible-images/)
> 5.  [How to style flexible images for RWD](http://m.techrepublic.com/blog/webmaster/how-to-style-flexible-images-for-rwd/1800)
> 6.  [Flexible, dynamically resizing images with CSS](http://blog.kurtschindler.net/post/flexible-dynamically-resizing-images-with-css)
> 7.  [CSS: Elastic Videos](http://webdesignerwall.com/tutorials/css-elastic-videos)