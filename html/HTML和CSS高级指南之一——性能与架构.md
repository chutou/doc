# HTML和CSS高级指南之一——性能与架构

> 本文由[99](http://99jty.com/?page_id=365)根据[Shay Howe](http://shayhowe.com/)的《[An Adavnced Guide to HTML & CSS](http://learn.shayhowe.com/advanced-html-css/)》第一课《[Performance & Organization](http://learn.shayhowe.com/advanced-html-css/performance-organization)》所译，整个译文带有我们自己的理解与思想，如果译得不好或不对之处还请同行朋友指点。如需转载此译文，需注明英文出处：[http://learn.shayhowe.com/advanced-html-css/performance-organization](http://learn.shayhowe.com/advanced-html-css/performance-organization)，以及作者相关信息

会书写html和css，且对他们有深刻的理解，是非常难得的。随着网站代码和流量的增长，迫切需要掌握一套新的技能，这对开发时间和用户体验來讲都是极其重要的。 了解网站性能与架构的基本原理，对之后的发展非常有帮助。

对代码进行组织与架构，不仅可以提高开发速度，还会提升页面的加载速度。这两个因素对于开发者和用户来言都是极大关注的。投入时间去设计网站适合的代码架构，同时确保不同组件之间如何共同作用，会加速开发进程，带来更好的用户体验。

此外，只需要几个小步骤提升网站的性能，你就会得到回报。[网站性能](http://stevesouders.com/hpws/rules.php)也遵循80/20原则，只需要做20%的优化就可以提升网站80%的速度。

#### 本课主要内容：

**HTML**

-  [减小和压缩文件](http://www.w3cplus.com/css/advanced-html-css-lesson1-performance-organization.html#minifyAndCompressFiles)
-  [文件缓存](http://www.w3cplus.com/css/advanced-html-css-lesson1-performance-organization.html#cacheCommonFiles)

**CSS**

-  [技巧与结构](http://www.w3cplus.com/css/advanced-html-css-lesson1-performance-organization.html#strategyAndStructure)
-  [高性能选择器](http://www.w3cplus.com/css/advanced-html-css-lesson1-performance-organization.html#performanceDrivenSelectors)
-  [可重用代码](http://www.w3cplus.com/css/advanced-html-css-lesson1-performance-organization.html#reusableCode)
-  [减少HTTP请求](http://www.w3cplus.com/css/advanced-html-css-lesson1-performance-organization.html#reduceHTTPRequests)

#### 技巧与结构

提高网站性能和组织的最基本一点，就是探索出一套开发代码基础的良好战略和结构。具体来讲，就是建立完备的目录结构，勾勒设计模式，以及对公用代码的有效重用。

**样式风格**

如何正确的组织样式表呢？这与具体网站跟个人偏好都有关系。不过，一般而言我们也可以遵循一些最佳实践。其中一个就是有目的的切分你的样式表，并为这些样式表建立目录，包括基础样式、界面相关的组件，以及商业需求模块。

```
# Base
  – normalize.css
  – layout.css
  – typography.css
# Components
  – alerts.css
  – buttons.css
  – forms.css
  – list.css
  – nav.css
  – tables.css
# Modules
  – aside.css
  – footer.css
  – header.css	

```

以上的代码组织结构包含三个目录，都对样式表做了独立的分类。这里要把站点认为是一个“系统”，而不是很多单独的页面，同时，代码要体现这个思路。要留意以上的组织结构没有针对“某页面”的样式表存在。

Base目录用来存放公用样式，以及全站通用的样式如布局字体等。Components目录用来存放特定用户界面相关的样式，这些样式按照界面组件被拆分为多个文件，比如警告及按钮。Modules目录用来存放页面的不同部分，这些部分是由商业需求决定的。

组件样式是与网站核心的商业逻辑无关的，纯粹由界面驱动的样式。模块则根据特定的商业逻辑呈现不同的样式。当我们建立一个模块时，里面使用的用户界面组件通常是不同的。举例来说，一个页面的侧边栏可能会包含列表及按钮，这些样式是定义在组件样式中的。而其他的样式需要从侧边栏样式中继承而来，这些样式是从模块样式中定义的。这种样式分离的原则鼓励我们对样式预先进行仔细的规划，以及样式表的共享与重用性。

组织样式表的策略不是什么新鲜事物。在之前不同的css理论如面向对象的css OOCSS, 可拓展模块化的CSS, SMACSS 中均提到过这方面的要求。 这些方法论包含他们自身独特的代码组织方式，以及样式表的使用。

**面向对象的CSS**

[面向对象的css](http://oocss.org/)是Nicole Sullivan所倡导的，她撰写大型网站样式表的一种方法。面向对象的css认为，两种原则可以帮助构建可扩展的，拥有强劲架构及合理的代码量的网站。

-  表现与结构分离
-  内容与容器分离

从一个网站的主题中完全把皮肤包括元素的布局结构整体分离。一个模块的结构是透明的，他可以继承任何样式和不会造成样式冲突。最常见的就是使用一个网格系统和布局结构，再结过加工设计成为一个经典模块。

内容从容器中分离出来，包括父元素与子元素的嵌套。一个标题应该是一样的，无论它的父元素是谁。为了做到这一点，元素需要一些默认的样式，然后通过多个类名来扩展其样式是有必要的。

**HTML**

```
<div class="alert alert-error">
  <p class="msg">...</p>
</div>

```

**CSS**

```
.alert {...}
.alert-error {...}
.msg {...}	

```

OOCSS提倡建立组件库，保持样式表的灵活性，以及利用网格来布局。这是非常有效的基本法则，当你要向站点添加页面或者新需求时，遵循这些原则可以避免添加额外的样式表。

**可扩展和模块化CSS**

与OOCSS不谋而合的理论是Jonathan Snook提出的：[构建可扩展的，模块化的css架构](http://smacss.com/)。如何构建可扩展的，模块化的css呢？这个理论要求css要拆分为五个核心类别，包含：

-  基础
-  布局
-  模块
-  声明
-  主题

基础部分包含一些核心元素的样式及全局样式。布局部分规定了不同元素的尺寸与网格样式，定义了他们的排列规则。模块部分更加针对页面某个独立的部分的特定样式，比如导航条等。状态部分定义了一些在某种情况下用来覆盖现有模块表现的样式，比如一个选定状态下的tab主题部分可能添加一些样式比如皮肤，视觉与体验，不同的模块等。

**HTML**

```
<div class="alert is-error">
  <p>...</p>
</div>	

```

**CSS**

```
.alert {...}
.alert.is-error {...}
.alert p {...}
.alert.is-error p {...}	

```

以上的例子里，alert 这个class的样式被划分到模块类别中，同时 is-error这个class的样式被划分到状态 类别中。之后就可以按照需求来继承某个类别中的样式了。

**选择一种方法**

选择什么样的方法去组织代码，完全决定于你。你认为这个方法是对某个网站最适合的，那么他就是管用的。一般而言适当的混合使用两种方法是有效的，对于每种方法你可以按照自己的意愿取其精华。

#### 高性能选择器

Css一个经常被滥用而没有意识到的功能是选择器。对于css，人们把注意力都集中在属性与值上了。他们认为，只要这些样式作用到该作用的元素上，元素表现正常就行了。 这是一个非常狭隘的认识。元素在Css中是怎样被选择的，与性能息息相关。页面渲染多快，样式表结构对于全站来说是否实用，是否模块化都与css选择器有关系。

**保证简短的选择器**

保证选择器尽可能简短是有一些好处的。这些好处包括降低选择器的权重，提供更好的继承与可移植性，以及提高效率。冗长且限制过多的选择器会降低性能，因为这会强迫浏览器从右到左的去解析每个独立的选择器。把选择器更具体化。

```
<!-- Bad -->
header nav ul li a {...}
<!-- Good -->
.primary-link {...}
<!-- Bad -->
button strong span {...}
button strong span .callout {...}
<!-- Good -->
button span {...}
button .callout {...}	

```

上面的代码中，第一个选择器过分冗余，若使用class，会让元素的识别跟解析变得更快。另外在这个场景里使用class就不需要判断元素的父元素了，这样可以任意移动元素的位置，而不需要改动任何样式。

相比第一个例子而言，第二个例子包含一个更短的选择器，他为同级选择器提供了特殊样式。避免使用权重过高的选择器，因为当元素次序变化的时候，这类选择器会解析出不同的结果。切分一些独立的选择器单元，然后给予他们相同的权重，可以让选择器之间更好配合。

我们使用简短的选择器的原因是降低选择器的权重，书写一份干净且可维护性强的代码。

**倾向于使用class**

Class类名是很赞的，渲染速度快，重用性高，已经被广泛应用于网站建设中。不过我们在使用class的时候，同样要权衡一些问题。

由于选择器是从右到左解析的，所以一定要注意 关键字选择器。 关键字选择器位于选择器单元的尾端，在最右边。这个选择器是非常重要的，因为他标识了浏览器要首先查找的元素。一个效率低下的选择器会给浏览器带来很多无谓的查找工作。不用担心使用一个特殊的类名会影响性能。

另外一点，在给元素定义样式时，不要用另外的选择器来修饰class选择器。当你用额外的选择器来限制class选择器时，你就失去了应用此选择器到其他元素的机会，同时增加了整个选择器的权重。

```
<!-- Bad -->
#container header nav {...}
<!-- Good -->
.primary-nav {...}
<!-- Bad -->
article.feat-post {...}
<!-- Good -->
.feat-post {...}	

```

同样要留意的是，远离id选择器，他们的权重太高，不存在任何可重用性。对于我们来说使用id与使用!Important没有什么明显区别。

#### 可重用代码

不断膨胀的无用代码是造成性能缺陷最大的原因之一。而一个有效降低css文件尺寸的方法是尽可能的重用样式。任何重复定义的样式或者接口模式都需要合并，从而使代码可被他人使用。如果两个模块拥有同样的背景，圆角，以及盒子阴影，毫无疑问你不能写两遍同样的样式。因此这些样式可以被合并在一个class中来定义。这样样式在书写一次后就可以再次使用。

重用代码不会造成语义问题。我们可以通过组合多个选择器的方式，用逗号分割选择器，让同样的样式通过两个选择器来定义并继承。另外一种方法就是遵循上述oocss及smacss所提到的方法，把样式绑定在一个class类名上，之后可以用多个class定义原本那个元素。

```
<!-- Bad -->
.news {
  background: #eee;
  border-radius: 5px;
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.25);
}
.social {
  background: #eee;
  border-radius: 5px;
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.25);
}
<!-- Good -->
.news, .social {
  background: #eee;
  border-radius: 5px;
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.25);
}
<!-- Even Better -->
.modal {
  background: #eee;
  border-radius: 5px;
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.25);
}	

```

采取哪种方法区别不大，当你的代码被重用后，整个文件的尺寸就会下降。

#### 减小和压缩文件

降低文件大小最好的方式是去掉重复与无用的代码。不过对此还有其他方式可用。其中就包括[压缩](http://www.hanselman.com/blog/TheImportanceAndEaseOfMinifyingYourCSSAndJavaScriptAndOptimizingPNGsForYourBlogOrWebsite.aspx)html,css与javascript文件。此外，通过去掉无用的信息与颜色配置，图片也可以被压缩。

**开启gzip压缩**

Gzip是最流行的文件压缩方式之一。Gzip压缩对通常如html，css javascript等类型的文件进行分析，之后对其字符串进行分析，从而压缩。Gzip处理过的字符串越多，压缩后的文件尺寸越小，因此服务器端可以传输更小的文件到浏览器端。

设置gzip几乎不需要任何代价，[HTML5 Boilerplate](http://html5boilerplate.com/)已经对此做了非常好的处理。如果你要对文件进行gzip处理， .htaccess文件需要放到网站服务器根目录下面，同时将你需要gzip压缩的特定文件列出来。注意这个文件前面的点号(这是个隐藏文件)。

[HTML5 Boilerplate](http://html5boilerplate.com/)给.htaccess文件单独开辟了一个部分用来处理gzip压缩。对于你自己的服务器来说，你可以重用或者使用一部分文件内的设置，来帮助你开启[gzip压缩](https://github.com/h5bp/html5-boilerplate/blob/master/.htaccess#L152)。不过值得注意的是.htaccess文件只能工作在apache web服务器上，而且要开启下列模块。

-  mod_setenvif.c
-  mod_headers.c
-  mod_deflate.c
-  mod_filter.c
-  mod_expires.c
-  mod_rewrite.c

通常来讲这不是什么问题，而且有些web服务器为你已经开启了压缩，毕竟压缩文件也是web服务器最关注的几个方面之一。

**衡量压缩效果**

Chrome浏览器开发者工具提供了非常多的数据来度量性能，尤其是network面板。此外也有一些第三方网站可以帮你确保gzip压缩是否开启。

![衡量压缩效果](http://cdn1.w3cplus.com/cdn/farfuture/AiY8LAmV1cfjOghQ58vwHUL_UjABsfw8qJmi8fFDZyw/mtime:1421035046/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson1-1.jpg)

Network面板检视了每个被浏览器加载的文件，且展示了文件大小及加载时间。注意gzip压缩把文件大小降低了大约60%。

![衡量压缩效果](http://cdn1.w3cplus.com/cdn/farfuture/3WIAkrR8tyF_2WKWa70-dp1KmgyKa-Y1rU_W4MgmiUw/mtime:1421035046/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson1-2.jpg)

点击某个文件，观察这个文件的请求与响应消息。在这里可以确认浏览器支持怎样的方式来压缩编码。注意请求头中的accept-encoding 表示在请求头中，浏览器支持了gzip, deflate 与 sdch注意响应头中的content-encoding 表示文件是使用gzip压缩编码来传输的。

> http协议及请求响应头的详细介绍可以参考[深入理解HTTP协议、HTTP协议原理分析(转）](http://www.cnblogs.com/shepherd2012/archive/2012/08/03/2621797.html)一文
>
> 译者：[99](http://99jty.com/?page_id=365)

**压缩图片**

降低文本文件的大小是有效的，如果你对图像进行压缩将会取得更好的效果。网站所有图片的大小轻易就会猛涨，因此对文件进行压缩将会极大程度的帮助你控制文件尺寸。

很多人对压缩图片敬而远之，原因是他们担心压缩图片会降低图片质量。在大多数情况下这是不正确的。图片可以以无损的方式压缩，在压缩时去除无用的颜色配置及图片信息，一点都不会影响图片自身质量。

有一些工具来帮助压缩图片,在Mac下的[ImageOptim](http://imageoptim.com/)和Window下的[PNGGauntlet](http://pnggauntlet.com/)。这两种是最常用来压缩图像,特别是JPG和PNG文件。

**图片压缩的示例**

未压缩前：455kb

![图片压缩](http://cdn.w3cplus.com/cdn/farfuture/GRsE7XUejTxSlcaq_y57vIfEVwLlL1hsa1gJ4odAOrU/mtime:1421035047/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson1-3.jpg)

压缩后，401kb

![图片压缩](http://www.w3cplus.com/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson1-4.jpg)

![图片压缩](http://cdn1.w3cplus.com/cdn/farfuture/M04eGWso1evalcFILbNerbS8cFra-AnM3ok9gq8vQQc/mtime:1421035047/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson1-5.jpg)

使用ImageOptim 上面的图片尺寸减小了14%，但图片质量没有下降。

同样要注意的是，在html中设置图片的宽高也会帮助页面更快的渲染,设置合适的宽高来为图片留出空间。需要明白的是，这些属性只是为了确保图片以准确大小渲染，而不会让图片收缩。如果你用一张较大的图片，但通过width height属性来缩放这张图片，这是很糟糕的方式，会加载更多的数据。

```
<img src="ocean.jpg" height="440" width="660" alt="Oceanview">
```

#### 减少HTTP请求

与文件大小类似，一个网站的http请求数可能是网站最大的性能缺陷。每当页面与服务器建立了一个请求，页面就会加载的更慢。有些请求必须在其他请求完成后才能建立，过多的请求甚至能当掉服务器。

**合并同样类型的文件**

合并同类型的文件可能是一种最简单的减少http请求的方法。特别是把所有的js文件，css文件各合并成一个文件。 合并这些文件之后，压缩合并后的文件，可以成功降低http请求。

```
<!-- Bad -->
<link href="css/reset.css" rel="stylesheet">
<link href="css/base.css" rel="stylesheet">
<link href="css/site.css" rel="stylesheet">
<!-- Good -->
<link href="css/styles.css" rel="stylesheet">	

```

通常，页面中的css文件应该优先加载，可以放到head标签里面。而js文件应该最后加载，放到body的闭合标签之前。这样做的原因是当页面剩余部分正在加载时，css可以并行加载。而js刚好相反，加载时只能解析一个文件。这样，在js加载的时候就会阻止其他部分的加载。这里有两个例外：一是当js文件在页面渲染后以异步方式加载，二是有些js文件与页面渲染有关系，比如 [html5 shiv](http://code.google.com/p/html5shiv)( 让ie浏览器支持html5标签及设置样式)。

**使用Image Sprites（css精灵/雪碧图）**

ss精灵是指单张图片，利用css控制作为多个元素背景的技术。这个举措，会减少使用多张图片作为背景图所造成的http请求。

为了创建包含一些背景图片的精灵图，常见的做法是把这些背景图片排列到一张图片里。之后利用css设置这张精灵图为图片背景，之后利用background-position属性来移动图片，从而显示应该显示的部分。

with the rest of the background image being hidden. 考虑情景：一个在元素下面不断滑动的图片，只会露出这个元素所圈定的部分。比如一个元素宽高16像素，若一张图片在下面，仅仅会显示一个16*16的区域，而区域外的图片部分则不会显示。

![图片精灵](http://cdn2.w3cplus.com/cdn/farfuture/CKh3exS-Geg9HEXP2b2ysx6WNXvNnc4iAZyei0czBrU/mtime:1421035048/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson1-6-1.jpg)

这是一个文本编辑器的精灵图，其外围蓝色轮廓显示出图片背景的參考位置。

我们创建一个菜单，利用上面的精灵图作为span元素的背景图片。之后利用class类名来改变精灵图的位置，相应的图片便会显示出来。

**HTML**

```
<ul>
  <li><a href="#"><span class="bold">Bold Text</span></a></li>
  <li><a href="#"><span class="italic">Italicize Text</span></a></li>
  <li><a href="#"><span class="underline">Underline Text</span></a></li>
  <li><a href="#"><span class="size">Size Text</span></a></li>
  <li><a href="#"><span class="bullet">Bullet Text</span></a></li>
  <li><a href="#"><span class="number">Number Text</span></a></li>
  <li><a href="#"><span class="quote">Quote Text</span></a></li>
  <li><a href="#"><span class="left">Left Align Text</span></a></li>
  <li><a href="#"><span class="center">Center Align Text</span></a></li>
  <li><a href="#"><span class="right">Right Align Text</span></a></li>
</ul>	

```

**CSS**

```
li {
  float: left;
  list-style: none;
  margin: 0 2px;
}
li a {
  background: linear-gradient(#fff, #eee);
  border: 1px solid #ccc;
  border-radius: 3px;
  display: block;
  padding: 3px;
}
li a:hover {
  border-color: #999;
}
li span {
  background: url("sprite.png") 0 0 no-repeat;
  color: transparent;
  display: block;
  font: 0/0 a;
  height: 16px;
  width: 16px;
}
.italic {
  background-position: -16px 0;
}
.underline {
  background-position: -32px 0;
}
.size {
  background-position: -48px 0;
}
.bullet {
  background-position: -64px 0;
}
.number {
  background-position: -80px 0;
}
.quote {
  background-position: -96px 0;
}
.left {
  background-position: -112px 0;
}
.center {
  background-position: -128px 0;
}
.right {
  background-position: -144px 0;
}	

```

**效果**

![图片精灵](http://cdn.w3cplus.com/cdn/farfuture/Vlt0qizgUhoR5UEztivpa9Vmnp_mw7EMboIrhPzNYLk/mtime:1421035048/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson1-7.jpg)

**Image Data URI**

此外，利用datauri的方法可以代替css sprite雪碧图，通过datauri，图片可以被编码，从而包含在html与css内，直接被加载，消除了图片的http请求。对于一些不会更新的小图片来说[Data URI](http://css-tricks.com/data-uris/)非常有效，特别是html与css被缓存的时候。当然，datauri也会造成很多问题。由于更新图片需要重新编码，这种方式非常难以维护。并且在老的浏览器里，比如ie7以下，这种方式是无效的。

如果利用data uris可以减少一些http请求，而html与css可以得到有效的缓存的话，这个措施是利大于弊的。可以利用[converters](http://websemantics.co.uk/online_tools/image_to_data_uri_convertor/)与[ pattern generators](http://www.patternify.com/)等工具来根据图片创建datauris。在使用datauris前一定要再三确保生成的datauri代码尺寸要比原图小。

**HTML**

```
<img height="100" width="660" alt="Rigged Pattern" 
  src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAoAAAAICAYAAADA
    +m62AAAAPUlEQVQYV2NkQAN9x+z/F1kdZEQXRxGAKcKmGK4QXRKdD1aIyzpkcUZcimB
    uhMljOBrdEzAbiVIIUky0QgBkMCabd5DVAwAAAABJRU5ErkJggg==">	

```

**CSS**

```
div {
  background: url("data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAoAAAAICAYAAADA
    +m62AAAAPUlEQVQYV2NkQAN9x+z/F1kdZEQXRxGAKcKmGK4QXRKdD1aIyzpkcUZcimB
    uhMljOBrdEzAbiVIIUky0QgBkMCabd5DVAwAAAABJRU5ErkJggg==") repeat;
}	

```

效果

![Image Data URI](http://cdn1.w3cplus.com/cdn/farfuture/XI2cqf2pHFXhxPsekyvcQqmiBcKHAMd8eNw_hbxgyOw/mtime:1421035048/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson1-8.jpg)

#### 文件缓存

缓存特定文件也可以减少http请求，让页面加载的更快。当页面第一次加载后，一些特定的文件会被缓存住。之后一段时间内，重复访问这个页面时，浏览器不需要再次请求相同的文件。这段时间取决于你，是根据你想让特定类型的文件在客户端保存的时间长短来决定的。

对于gzip压缩过的文件来说，可以通过htaccess文件 来设置expires头(过期时间)用以缓存文件。 HTML5 Boilerplate再次走在了前列，他们的对.htaccess文件划分出专门一块区域来设置[expires头](https://github.com/h5bp/html5-boilerplate/blob/master/.htaccess#L192)。

图片，视频，网络字体，以及一些常见的媒体类型一般都会缓存一个月，而css与js文件一般会缓存一年。Css或者其他文件如果更新频率超过一年一次的话，最好通过更改文件名进行版本控制，从而重新加载文件。此外，expires头可以改成更小的时段。

```
ExpiresByType text/css "access plus 1 year"
ExpiresByType application/javascript "access plus 1 year"	

```

把"access plus 1 year" 换成 "access plus 1 week"，对于那些每周更新，但没有利用文件名做版本控制的css与js文件是更适合的。关于有效的expires头的资料可以参考 mod_expires [语法](http://httpd.apache.org/docs/current/mod/mod_expires.html)。

#### 扩展阅读：

1.  [Best Practices for Speeding Up Your Web Site](http://developer.yahoo.com/performance/rules.html) via Yahoo! Developer Network
2.  [Rules for Faster-Loading Web Sites](http://stevesouders.com/hpws/rules.php) via Steve Sounders
3.  [CSS Strategy Square-off](http://viget.com/inspire/css-squareoff) via Viget Labs
4.  [Writing Efficient CSS Selectors](http://csswizardry.com/2011/09/writing-efficient-css-selectors/) via Harry Roberts
5.  [Minifying and Optimizing Files](http://www.hanselman.com/blog/TheImportanceAndEaseOfMinifyingYourCSSAndJavaScriptAndOptimizingPNGsForYourBlogOrWebsite.aspx) via Scott Hanselman
6.  [HTML5 Boilerplate](http://html5boilerplate.com/)
7.  [Data URIs](http://css-tricks.com/data-uris/) via CSS-Tricks
8.  [CSS DIY Organization](http://net.tutsplus.com/tutorials/html-css-techniques/css-diy-organization/)
9.  [Efficiently Rendering CSS](http://css-tricks.com/efficiently-rendering-css/)
10.  [70 Expert Ideas For Better CSS Coding](http://coding.smashingmagazine.com/2007/05/10/70-expert-ideas-for-better-css-coding/)
11.  [OOCSS——概念篇](http://www.w3cplus.com/css/oocss-concept)
12.  [OOCSS——核心篇](http://www.w3cplus.com/css/oocss-core)
13.  [面向对象的CSS(OOCSS)](http://www.w3cplus.com/css/an-introduction-to-object-oriented-css-oocss.html)
14.  [CSS架构](http://www.w3cplus.com/css/css-architecture.html)