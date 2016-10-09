# HTML和CSS高级指南之三——丰富多彩的选择器



> 小编推荐：[掘金](http://gold.xitu.io/welcome/frontend?utm_source=w3cplus&utm_medium=word&utm_content=ganhuo&utm_campaign=q3_personal)是一个高质量的技术社区，从 ECMAScript 6 到 Vue.js，性能优化到开源类库，让你不错过前端开发的每一个技术干货。各大应用市场搜索「掘金」即可下载APP，技术干货尽在掌握中。

> 本文由[99](http://99jty.com/?page_id=365)根据[Shay Howe](http://shayhowe.com/)的《[An Adavnced Guide to HTML & CSS](http://learn.shayhowe.com/advanced-html-css/)》第三课《[Complex Selectors](http://learn.shayhowe.com/advanced-html-css/complex-selectors)》所译，整个译文带有我们自己的理解与思想，如果译得不好或不对之处还请同行朋友指点。如需转载此译文，需注明英文出处：http://learn.shayhowe.com/advanced-html-css/complex-selectors，以及作者相关信息
>
> 作者：[Shay Howe](http://shayhowe.com/)
>
> 译者：[99](http://99jty.com/?page_id=365)

选择器是css最重要的部分。选择器搭建了css的层叠大厦，决定了样式如何应用到页面元素上来。

直到最近人们关注CSS的焦点也未真正触及选择器。选择器规范内的偶尔有一些增量更新，但从来没有任何真正的突破性的改进。幸运的是，选择器在最近被赋予了越来越多的关注，焦点集中在选择不同类型的元素，及选择元素不同的使用状态。

<iframe width="0" height="0" name="FMT" id="FMT" src="" frameborder="0" scrolling="no"></iframe>

<iframe id="iframeu1490106_0" src="http://pos.baidu.com/yckm?rdid=1490106&dc=2&exps=112003&di=u1490106&dri=0&dis=0&dai=1&ps=1128x30&dcb=BAIDU_SSP_define&dtm=HTML_POST&dvi=0.0&dci=-1&dpt=none&tsr=0&tpr=1473818645072&ti=HTML%E5%92%8CCSS%E9%AB%98%E7%BA%A7%E6%8C%87%E5%8D%97%E4%B9%8B%E4%B8%89%E2%80%94%E2%80%94%E4%B8%B0%E5%AF%8C%E5%A4%9A%E5%BD%A9%E7%9A%84%E9%80%89%E6%8B%A9%E5%99%A8_HTML%E5%92%8CCSS%E9%AB%98%E7%BA%A7%E6%8C%87%E5%8D%97%20%E6%95%99%E7%A8%8B_w3cplus&ari=2&dbv=2&drs=1&pcs=1265x676&pss=1265x1239&cfv=0&cpl=5&chi=1&cce=true&cec=UTF-8&tlm=1473818645&rw=676&ltu=http%3A%2F%2Fwww.w3cplus.com%2Fcss%2Fadvanced-html-css-lesson3-complex-selectors.html&ltr=http%3A%2F%2Fwww.w3cplus.com%2Fcss%2Fadvanced-html-css-lesson4-responsive-web-design.html&ecd=1&psr=1280x800&par=1280x773&pis=-1x-1&ccd=24&cja=false&cmi=7&col=zh-CN&cdo=-1&tcn=1473818645&qn=affa40dd4b5febcf&tt=1473818645052.23.24.27" width="468" height="60" align="center,center" vspace="0" hspace="0" marginwidth="0" marginheight="0" scrolling="no" frameborder="0" style="border:0; vertical-align:bottom;margin:0;" allowtransparency="true"></iframe>

Css3带来了很多新的选择器，为旧的秩序打开了一扇新的大门。这篇文章中，我们将会讨论新旧 [选择器](http://net.tutsplus.com/tutorials/html-css-techniques/the-30-css-selectors-you-must-memorize/)以及应用他们的最佳实践。

#### 	这一课中主要包括下面几个部分内容：

* [常见选择器](http://www.w3cplus.com/css/advanced-html-css-lesson3-complex-selectors.html#commonSelectors)
* [子选择器](http://www.w3cplus.com/css/advanced-html-css-lesson3-complex-selectors.html#childSelectors)
* [兄弟选择器](http://www.w3cplus.com/css/advanced-html-css-lesson3-complex-selectors.html#siblingSelectors)
* [属性选择器](http://www.w3cplus.com/css/advanced-html-css-lesson3-complex-selectors.html#attributeSelectors)
* [伪类](http://www.w3cplus.com/css/advanced-html-css-lesson3-complex-selectors.html#pseudoClasses)
* [伪元素](http://www.w3cplus.com/css/advanced-html-css-lesson3-complex-selectors.html#pseudoElements)

  #### 常见选择器

在深入探讨css3带来的更加复杂的选择器之前，我们简单回顾一下在现在看来很普通的那些选择器,比如 元素类型，class类名，id选择器

类型选择器选择根据其类型来选择元素，尤其是该元素在HTML中的声明。Class选择器根据元素class属性的值来选择元素，当为了共用一个常用样式时，这个值可以重用在多个元素上。ID选择器根据元素ID属性的值来选择元素，这个属性是独一无二的，在每个页面中同样的ID属性值只能被使用一次。

**CSS**

<pre class="bash">
h1 {...}
.tagline {...}
\#intro {...}	
</pre>

**HTML**

<pre class="xml">
<section id="intro"><h1>...</h1>
  <h2 class="tagline">...</h2>
</section>
</pre>

**普通选择器简表**

<thbody></thbody>

				例子       |				 类别    |				 解释                          
------------ | --------- | --------------------------------
				h1       |				 类型选择器 |				 选择元素的一个类型                   
				.tagline |				 类选择器  |				 以class属性的值来选择元素,可以在一个页面中出现多个
				\#intro  |				 ID选择器 |				 以id属性的值来选择元素,在页面中是唯一的，只能出现一次

#### 	子选择器

子选择器提供了一个选择从属关系元素的方式，将某元素作为父元素的“后代”来处理。可以创建两类元素集合：后代元素或者只包含子元素

**后代选择器**

最常用的子选择器为后代选择器，可以匹配指定祖先元素的所有后代元素。后代元素不需要如父母与子女的关系一样，直接跟随于祖先元素的文档树后，而是在祖先元素内部的任何地方。当你利用空格分割两个元素时可以创建一个后代选择器，可以为每个元素创建新的层级关系。

article h2选择器是一个后代选择器，可以选择article元素内的h2元素。注意，不论这个h2元素是否“存在”，只要他是在article元素内部，就会被选择。此外，在article元素外面的ｈ２元素则不会被选择。

下面代码中第三行与第五行的标题元素被选中，因此被应用加粗的样式:

**CSS**

<pre class="undefined">
article h2 {...}	
</pre>

**HTML**

<pre class="xml">
<h2>...</h2>
<article>
  **<h2>...</h2>**
  <div>
    **<h2>...</h2>**
  </div>
</article>
</pre>

**子元素选择器**

有些时候后代选择器的功能过于强大，与我们想要的结果相比他匹配的更多。有时我们只需要选择父元素的直接子元素而不是一个祖先元素内部嵌套的所有元素。这时候子选择器闪亮登场，可以使用＞代替空白符号来放在父元素与子元素之间，就可以创建一个子选择器。

举例来讲，article >　ｐ　选择器是一个子选择器，只会选择ａｒｔｉｃａｌ元素内紧跟的ｐ子元素。Ａｒｔｉｃａｌ元素外面的ｐ元素，及ａｒｔｉｃａｌ元素内部嵌套更深的ｐ元素则不会被选择

下面第三段的ｐ元素为父元素的直接子元素，因此被选择，应用样式加粗

**CSS**

<pre class="undefined">
article > p {...}	
</pre>

**HTML**

<pre class="xml">
<p>...</p>
<article>
  **<p>...</p>**
  <div>
    <p>...</p>
  </div>
</article>
</pre>

**子选择器概览**

<thbody></thbody>

				例子           |				 类别     |				 解释            
---------------- | ---------- | ------------------
				article h2   |				 后代选择器  |				 选择指定祖先元素内的后代元素
				article > h2 |				 子元素选择器 |				 选择指定父元素内的直接子元素

#### 	兄弟选择器

学习如何[选择子元素](http://css-tricks.com/child-and-sibling-selectors/)是很有用的，也很常用。而当兄弟元素拥有一个共同的父元素时，也需要被选择。兄弟选择器可以通过普通兄弟选择器与相邻兄弟选择器两种方式创建

**普通兄弟选择器**

普通兄弟选择器可以根据拥有共同父元素的兄弟元素，来让元素被选择。当你在两个元素间使用~符号时即创建了一个兄弟选择器。这表示第二个元素是第一个元素的兄弟元素，两个元素拥有共同的父元素。

h2~p 选择器是一个普通兄弟选择器，查询h2元素后面的拥有共同父元素的兄弟元素p。因此若p元素要被选择，必须跟在h2元素后面。

第5行跟第9行的段落会被选择，因为他们相对文档流在h2元素的后面，同时拥有相同的父元素，因此元素被选择，应用样式加粗。

**CSS**

<pre class="undefined">
h2 ~ p {...}	
</pre>

**HTML**

<pre class="xml">
<p>...</p>
<section>
  <p>...</p>
  <h2>...</h2>
  **<p>...</p>**
  <div>
    <p>...</p>
  </div>
  **<p>...</p>**
</section>
</pre>

**相邻兄弟选择器**

有时我们想对兄弟元素的选择结果做控制，这时候可以使用相邻兄弟选择器。相邻兄弟选择器只会选择紧跟着一个元素的另一个元素。在两个元素间你可以用+符号替代~符号就可以创建相邻兄弟选择器。同样，第二个元素应该直接紧跟第一个元素并且拥有相同父元素。

比如h2+p这个相邻兄弟选择器，它只会选择紧接着h2元素，同时拥有相同父元素的p元素。

第5行段落会被选择，因为他紧挨着h2元素的后面，同时拥有相同的父元素，因此元素被选择，应用样式加粗。

**CSS**

<pre class="undefined">
h2 + p {...}	
</pre>

HTML

<pre class="xml">
<p>...</p>
<section>
  <p>...</p>
  <h2>...</h2>
  **<p>...</p>**
  <div>
    <p>...</p>
  </div>
  <p>...</p>
</section>
</pre>

**兄弟选择器示例**

HTML

<pre class="xml">
<input type="checkbox" id="toggle">
<label for="toggle">☰</label>
<nav>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Services</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
</pre>

CSS

<pre class="css">
input {
  display: none;
}
label {
  background: \#f5f5f5;
  background: linear-gradient(#fff, #eee);
  border: 1px solid \#ccc;
  border-radius: 6px;
  cursor: pointer;
}
label:hover {
  color: \#f7941d;
}
input:checked + label {
  background: \#f5f5f5;
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.15);
  color: \#8c9198;
}
nav {
  max-height: 0;
  overflow: hidden;
  transition: all .2s linear;
}
input:checked ~ nav {
  max-height: 500px;
}
</pre>

效果

![兄弟选择器示例](http://cdn1.w3cplus.com/cdn/farfuture/4CIekDANkgR5XglVh9SDobtNA-MFui4j5E5YPKEcg5w/mtime:1421035051/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson3-1.jpg)

**兄弟选择器概览**

<thbody></thbody>

				例子     |				 类别      |				 解释                      
---------- | ----------- | ----------------------------
				h2 ~ p |				 相邻兄弟选择器 |				 选择第一个元素后的兄弟元素,两者拥有相同的父元素
				h2 + p |				 子元素选择器  |				 选择第一个元素后紧跟的元素,两者拥有相同的父元素

#### 	属性选择器

先前讲的一些常见的选择器也可以被定义为属性选择器，因为他们是根据元素的class或者id属性来选择的。Class与id选择器很有用，使用广泛，但这仅仅是个开始。其他[属性的选择器](http://www.css3.info/preview/attribute-selectors/)多年来不断出现，特别是在css3规范中，属性选择器迎来了一个大的飞跃。现在，元素不仅可以根据属性是否存在，而且可以根据属性的值来被选择。

**目前属性选择器**

首先要介绍的一个属性选择器通过识别元素是否包含某种属性来选择元素，而不管这属性的值具体是多少。选择器可以将属性名放在方括号内[] 来判断属性是否存在。方括号可以跟随或者不跟随任何元素类型或者class，这取决于你所要求的选择器权重。

**CSS**

<pre class="undefined">
a[target] {...}	
</pre>

**HTML**

<pre class="xml">
<a href="#" target="_blank">...</a>
</pre>

**属性均等选择器**

为了识别一个特定且完全匹配的值，我们可以使用上面用过的属性选择器，而这时候要把要求匹配的值写在方括号内。方括号内以属性名开头，紧跟着等号=与引号””,引号内则是你需要匹配的属性值。

**CSS**

<pre class="ini">
a[href="http://google.com/"] {...}	
</pre>

**HTML**

<pre class="xml">
<a href="http://google.com/" >...</a>
</pre>

**属性包含选择器**

当我们需要寻找一个属性值包含某特定值，但不一定完全匹配时，属性选择器的方括号内可以使用*通配符。通配符需要紧跟着属性名字，后面跟等号。这样书写，表示所要求匹配的值只需要出现，或者被包含于属性值中即可。

**CSS**

<pre class="perl">
a[href\*="login"] {...}	
</pre>

**HTML**

<pre class="xml">
<a href="/login.php" >...</a>
</pre>

**属性开头选择器**

为了进一步选择一个属性值包含某特定值的元素，也可以根据属性开头包含的值来选择元素。在方括号内，属性名与等号间使用抑扬音符(^)表示属性值以某个特定值开头。

**CSS**

<pre class="undefined">
a[href^="https://"] {...}	
</pre>

**HTML**

<pre class="xml">
<a href="https://chase.com" >...</a>
</pre>

**属性结尾选择器**

与属性开头选择器相反，我们也可以使用属性结尾选择器。这里在方括号内利用$符号替换刚才的^，放在属性名与等号之间。$符号表示属性值以一个特定的值结尾。

**CSS**

<pre class="ruby">
a[href$=".pdf"] {...}	
</pre>

**HTML**

<pre class="xml">
<a href="/docs/menu.pdf" >...</a>
</pre>

**属性间隔选择器**

有时属性名可能是空格分隔的多个单词组成的，而我们需要匹配其中的一个单词来选择元素。这种情况下可以在方括号内，属性名与等号之间使用波浪线~,这表示属性值可能被空格分割为多个单词，而其中一个单词匹配特定值。

**CSS**

<pre class="undefined">
a[rel~="tag"] {...}	
</pre>

**HTML**

<pre class="xml">
<a href="#" rel="tag nofollow" >...</a>
</pre>

**属性连字符选择器**

当属性值包含连字符而不是空白时，竖线|可以写在方括号里，放在属性名与等号之间。这表示属性值可能由连字符分割，而连字符分割的几个单词必须匹配一个特定值。

**CSS**

<pre class="undefined">
a[lang|="en"] {...}	
</pre>

**HTML**

<pre class="xml">
<a href="#" lang="en-US" >...</a>
</pre>

**属性选择器示例**

HTML:

<pre class="xml">
<ul>
  <li><a href="#.pdf" title="PDF Document">PDF Document</a></li>
  <li><a href="#.doc" title="Word Document">Word Document</a></li>
  <li><a href="#.jpg" title="Image File">Image File</a></li>
  <li><a href="#.mp3" title="Audio File">Audio File</a></li>
  <li><a href="#.mp4" title="Video File">Video File</a></li>
</ul>
</pre>

CSS

<pre class="css">
ul{
  list-style: none;
}
ul a {
  padding-left: 22px;
}
ul a[href$=".pdf"] {
  background: url("images/pdf.png") 0 50% no-repeat;
}
ul a[href$=".doc"] {
  background: url("images/doc.png") 0 50% no-repeat;
}
ul a[href$=".jpg"] {
  background: url("images/image.png") 0 50% no-repeat;
}
ul a[href$=".mp3"] {
  background: url("images/audio.png") 0 50% no-repeat;
}
ul a[href$=".mp4"] {
  background: url("images/video.png") 0 50% no-repeat;
}
</pre>

效果

![属性选择器示例](http://cdn1.w3cplus.com/cdn/farfuture/KM52k_WhCq5bmdu1jrXI8a6nzKqkYQHNkAwIyBZvk4o/mtime:1421035051/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson3-2.jpg)

**属性选择器概览**

<thbody></thbody>

				例子                                                     |				 类别       |				 解释                                
---------------------------------------------------------- | ------------ | --------------------------------------
				a[target]                                              |				 目标属性选择器  |				 选择一个存在某属性的元素                      
				a[href="[http://google.com/"]](http://google.com/%22]) |				 属性均等选择器  |				 选择一个属性值匹配特定值的元素                   
				a[href*="login"]                                       |				 属性包含选择器  |				 选择一个属性值包含特定值的元素                   
				a[href^="https://"]                                    |				 属性开头选择器  |				 选择一个属性值以特定值开头的元素                  
				a[href$=".pdf"]                                        |				 属性结尾选择器  |				 选择一个属性值以特定值结尾的元素                  
				a[rel~="tag"]                                          |				 属性间隔选择器  |				 选择一个属性值被空白分割成多个单词，且其中一个单词匹配给定值的元素 
				a[lang|="en"]                                          |				 属性连接符选择器 |				 选择一个属性值被连接符分割成多个单词，且其中一个单词匹配给定值的元素

#### 	伪类

[伪类](http://coding.smashingmagazine.com/2011/03/30/how-to-use-css3-pseudo-classes/)类似通常HTML中的类，但是它们不会直接以html标记的形式定义，而是一个动态的，作为用户交互的等行为的结果填充到文档结构中。

最常见的，你肯定见过的一个伪类是:hover.注意这个伪类是由一个冒号开头的，其他伪类也一样。

**链接性伪类**

一些很基本的伪类都是围绕链接来展开的。:link与:visited伪类一个定义未访问过，另一个定义访问过的链接样式。 当定义一个未访问过的样式时，:link伪类派上用场，而:visited伪类根据浏览器历史记录来判断用户访问过的链接，从而定义样式。

<pre class="perl">
a:link {...}
a:visited {...}	
</pre>

**用户行为性伪类**

根据用户行为，伪类可以动态添加到一个元素上，包括:hover,:activem:focus 伪类。当用户把光标挪动到元素上面时:hover伪类所定义的样式被应用到元素上。当用户激活一个元素时，比如点击一个元素，:active伪类所定义的样式被应用到元素上。当用户使一个元素获得焦点时，也包括利用键盘切换焦点，:focus伪类所定义的样式被应用到元素上。

<pre class="undefined">
a:hover {...}
a:active {...}
a:focus {...}	
</pre>

**用户界面状态性伪类**

与link相关的伪类相类似，也有很多伪类与用户界面上的元素状态相关，特别是表单元素。这些与用户界面状态相关的伪类包括 :enabled,:disabled:checked :indeterminate.

:enabled伪类选择一个处于默认状态下，可用的input元素，而:disabled伪类正好相反。 很多浏览器会使disabled的input元素变淡，来告知用户此input不可用于交互。不过这一类的样式可以通过:disabled伪类来调整。

<pre class="undefined">
input:enabled {...}
input:disabled {...}	
</pre>

另外两个用户界面相关的伪类，:checked与:inderterminate都围绕单选与多选按钮展开。 :checked伪类选择那些被选中的单选或多选按钮。当一个单选或多选按钮既未被选中，又不处于非选中状态，这个元素为 indeterminate状态(未决定状态).我们可以用:indeterminate伪类来定义处于此类状态的元素。

<pre class="cs">
input:checked {...}
input:indeterminate {...}	
</pre>

**结构性伪类**

一部分伪类是结构性的和基于位置的，这是由元素处于文档树中的什么地方决定的。这些结构性伪类看起来非常类似，不过每种都提供了他们自己独特的功能。一些伪类算是历史悠久，但CSS3带来了整个一套新的伪类，来弥补先前的不足。

**:first-child, :last-child, & :only-child**

首先与大家见面的结构性伪类是:first-child, :last-child, 以及:only-child伪类。:first-child伪类会选择父元素下的第一个子元素，而:last-child伪类会选择父元素下的最后一个子元素。这些伪类对于选择列表中的首项或末项极其有用。此外，若父元素下面只有一个子元素，这个元素将会被:only-child伪类选择。因此这个伪类也可以写成:first-child:last-child ，不过:only-child的写法权重要低些。

选择器 li:first-child 标记了列表中的第一个元素而li:last-child标记了列表中的最后一个元素。因此第二行与第十行代码里的li被应用样式加粗。选择器 div:only-child寻找一个div元素，而这个div元素的父元素只含有一个子元素。因此第四行代码的div被选中 应用样式加粗，因为他是相对应的列表元素仅有的一个子元素。

**CSS**

<pre class="perl">
li:first-child {...}
li:last-child {...}
div:only-child {...}	
</pre>

**HTML**

<pre class="xml">
<ul>**<p>...</p>**
  <li>
    **<div>...</div>**
  </li>
  <li>
    <div>...</div>
    <div>...</div>
  </li>
  **<li>...</li>**
</ul>
</pre>

**:first-of-type, :last-of-type, & :only-of-type**

寻找到特定父元素的首个子元素，最后一个子元素，以及仅有的子元素是很有用的，而且很多时候这也是需求。不过有时对于某元素，你只想找到特定类型的子元素。比如我只想得到文章的第一段或者最后一段，或者文章中唯一的图片。很幸运的是我们可以利用first-of-type, :last-of-type, 与 :only-of-type 三个伪类来完成。

:first-of-type伪类会选择父元素下某种子元素的第一个，而 :last-of-type伪类会选择父元素下某种子元素的最后一个。若元素是父元素的子元素，且只有一个这种类型的子元素，那这个元素会被 :only-of-type伪类选择。

下面的例子中，:first-of-type伪类与 :last-of-type伪类分别选择了文章的第一段与最后一段，而不会管段落是否是文章元素的第一个子元素或最后一个子元素。第三行与第六行被选中，应用样式加粗。img:only-of-type识别出了文章中仅有的图像，也应用了样式加粗。

**CSS**

<pre class="perl">
p:first-of-type {...}
p:last-of-type {...}
img:only-of-type {...}	
</pre>

**HTML**

<pre class="xml">
<article><h1>...</h1>
  **<p>...</p>**
  <p>...</p>
  **<img src="#">
  <p>...</p>**
  <h6>...</h6>
</article>
</pre>

最后这里有一些基于代数表达式来选择元素的伪类。这些伪类包括:nth-child(n), :nth-last-child(n), :nth-of-type(n)与 :nth-last-of-type(n)。这些独特的伪类均以nth前缀开头，括号内接收一个以n作为参数的代数表达式。

括号内以数字作为表达式，可以直接决定哪个元素被选择。直接使用数字可以从文档树开头或结尾算起，计入单独的元素。而利用n作为参数的代数表达式，可以同样从从文档树开头或结尾算起，批量选择一组元素。

**使用伪类数字或表达式**

刚才也提到了，括号内以数字作为表达式，可以从文档树开头或结尾算起，计入单独的元素。举例来讲，li:nth-child(4)会选择列表项中第四个元素。从列表第一个元素开始计算，每次计数增加1，对应每一个列表元素，直到找到第四个列表元素。当直接使用数字时，数字必须为正数

[伪类表达式](http://reference.sitepoint.com/css/understandingnthchildexpressions)为这些格式:an, an+b, an-b, n+b, -n+b, -an+b.这些都会被解释并阅读为(a×n)±b。变量a代表乘数，表示每a的倍数个元素，而b变量表示从a的倍数个元素开始，加减计数的个数，从而选择元素。

比如li:nth-child(3n)选择器，会选择列表内每3的倍数个列表元素。利用表达式计算的结果：3×0, 3×1, 3×2，等等。你可以看到结果是3 6这些3的倍数，即第3 6个元素被选择。

此外 与奇数偶数相关的关键字作为值也可以。如预期结果，两个值分别可以选择第奇数个与偶数个元素。其中关键词也可以用表达式来表示，其中“2n+1”将选择所有奇数（odd），而“2n”将选择所有偶数（en）。

使用li:nth-child(4n+7) 选择器，可以从第4的倍数个元素开始计算，直到识别第七个元素。使用这个表达式计算出的值等同于 (4×0)+7, (4×1)+7, (4×2)+7，结果是第7个，第11个，第15个等，选择出4的倍数加7。

当n参数前面不加数字前缀时，等同于a变量被解释为1.比如使用i:nth-child(n+5)，那么每个列表元素都会做为计算起点，之后计算第五个元素。结果就是前四个元素不会被选择，因为表达式计算出的结果是(1×0)+5, (1×1)+5, (1×2)+5 等。

更复杂一点也可以使用负数。举例来讲 li:nth-child(6n-4) 选择器会帝从6的倍数个列表元素开始计算，之后往前面计算4个，结果就是第2个，第8个，第14个等。li:nth-child(6n-4)也可以写成li:nth-child(6n+2)，这样就不用使用负数了。

若参数a，或者n为负数，那么紧跟着的b参数，必须为正数。当a为负数时，或者n为负数时，b实际上标志了被计算的“最大数”。举例来讲 li:nth-child(-3n+12) 选择器的范围在前12个列表元素之内(因为最大只能是12了)，li:nth-child(-n+9) 只能选择前九个元素，这时候n前面没有系数a，可以被认为是-1。

**:nth-child(n) & :nth-last-child(n)**

当我们对伪类的数字与代数表达式如何计算做了一个大概了解后，我们来看看实际应用中如何使用这些数字与代数表达式。首先以:nth-child(n)和:nth-last-child(n) 开始。这两个伪类的表现很类似:first-child 与:last-child伪类，因为他们都会寻找父元素下的子元素，然后只选择一个匹配给定值的元素。:nth-child(n) 伪类从文档树开头开始计算，而:nth-last-child(n) 则从文档树尾部开始计算。

我们以 li:nth-child(3n)作为例子。这个选择器会识别第3的倍数个元素，因此第四行代码与第七行代码的元素被选择，应用样式加粗

**CSS**

<pre class="undefined">
li:nth-child(3n) {...}	
</pre>

**HTML**

<pre class="xml">
<ul><li>...</li>
  <li>...</li>
  **<li>...</li>**
  <li>...</li>
  <li>...</li>
  **<li>...</li>**
</ul>
</pre>

在:nth-child伪类中使用一个不同的表达式会产生一个不同的选择元素集合。举例来说，li:nth-child(2n+3)选择器将会每两个元素一组，计算这组的第三个元素，之后选择。结果，下面列表元素中，第四行与第六行代码代表的元素被选择，应用样式加粗

**CSS**

<pre class="undefined">
li:nth-child(2n+3) {...}	
</pre>

**HTML**

<pre class="xml">
<ul><li>...</li>
  <li>...</li>
  **<li>...</li>**
  <li>...</li>
  **<li>...</li>**
  <li>...</li>
</ul>
</pre>

我们再次改变表达式，这次使用负值，产生了一个新的选择元素集合。li:nth-child(-n+4)选择器识别了列表中最开始的四个元素，其余列表元素不被选择。第二行至第五行四个元素被选中，应用加粗样式。

**CSS**

<pre class="undefined">
li:nth-child(-n+4) {...}	
</pre>

**HTML**

<pre class="xml">
<ul>**<li>...</li>
  <li>...</li>
  <li>...</li>
  <li>...</li>**
  <li>...</li>
  <li>...</li>
</ul>
</pre>

我们再次改变表达式，在n前面添加一个负整数作为系数。li:nth-child(-2n+5)选择器从前五个元素中寻找，识别了第2的倍数个元素，因此第2，4，6行代码的元素被选中，应用样式加粗

**CSS**

<pre class="undefined">
li:nth-child(-2n+5) {...}	
</pre>

**HTML**

<pre class="xml">
<ul>**<li>...</li>**
  <li>...</li>
  **<li>...</li>**
  <li>...</li>
  **<li>...</li>**
  <li>...</li>
</ul>
</pre>

用 :nth-last-child(n) 伪类替换:nth-child(n) 改变了计数的方向，当你从文档树末尾开始计算时，请使用:nth-last-child(n) 伪类。如li:nth-last-child(3n+2) 这个会从列表末尾开始，选择列表中每三个一组，之后数两个元素，朝着列表开头去计数。这里第三行与第六行的代码被选择，应用样式加粗。

**CSS**

<pre class="perl">
li:nth-last-child(3n+2) {...}	
</pre>

**HTML**

<pre class="xml">
<ul><li>...</li>
  **<li>...</li>**
  <li>...</li>
  <li>...</li>
  **<li>...</li>**
  <li>...</li>
</ul>
</pre>

**:nth-of-type(n) & :nth-last-of-type(n)**

:nth-of-type(n) 与:nth-last-of-type(n)伪类与 :nth-child(n) 和:nth-last-child(n) 伪类很类似。而与后者不同的是，nth-of-type伪类只会选择那些指定类型(type)的元素。举例来讲，当计算文章中有几段时， :nth-of-type(n) 与:nth-last-of-type(n)伪类会忽略标题元素(h1之类)，块元素(div)这些不是段落元素p的元素。而 :nth-child(n) 和:nth-last-child(n) 伪类则会计入所有的元素，而不考虑元素的类型，只需要元素匹配即可。另外所有可以用在:nth-child(n) 和:nth-last-child(n) 伪类中的n表达式，在 :nth-of-type(n) 与:nth-last-of-type(n)伪类中也是可用的。

我们使用p:nth-of-type(3n) 选择器，父元素相同的每三个p元素会被我们选择一个，而会忽略同级的其他类型的元素。这里第五行与第九行的元素会被选择，应用加粗的样式

**CSS**

<pre class="undefined">
p:nth-of-type(3n) {...}	
</pre>

**HTML**

<pre class="xml">
<article><h1>...</h1>
  <p>...</p>
  <p>...</p>
  **<p>...</p>**
  <h2>...</h2>
  <p>...</p>
  <p>...</p>
  **<p>...</p>**
</article>
</pre>

与:nth-child(n)跟 :nth-last-child(n)的关系类似，:nth-of-type(n) 与:nth-last-of-type(n)两个伪类，前者是从文档树开头开始计算，后者是从文档树尾部开始计算。

利用p:nth-last-of-type(2n+1) 这个选择器，从最后一段往前计算，每两个段落可以被标记选中。这里代码4，7，9行的段落元素被选中，应用样式加粗。

**CSS**

<pre class="perl">
p:nth-last-of-type(2n+1) {...}	
</pre>

**HTML**

<pre class="xml">
<article><h1>...</h1>
  <p>...</p>
  **<p>...</p>**
  <p>...</p>
  <h2>...</h2>
  **<p>...</p>**
  <p>...</p>
  **<p>...</p>**
</article>
</pre>

**目标伪类**

URI片段标识可以认为是 哈希符号 # 后面紧跟的字符。比如url http://example.com/index.html#hello 哈希符号后面跟着hello这个标识符。当这个标识符与页面中某元素的id属性相匹配时，如 <section id=”hello”>，通过使用目标位类，这个元素会被识别并应用样式。片段标识符最常用在页面链接及链接到页面的其他地方。

看以下的代码。当用户访问一个页面时，如果他的URI片段标识符为hello,与section的id属性相同，通过使用:target伪类，section就会被应用样式。如果URI片段标识符变更，且匹配某元素的id属性，通过使用:target伪类，这个元素就会被应用样式

**CSS**

<pre class="undefined">
section:target {...}	
</pre>

**HTML**

<pre class="xml">
<section id="hello">...</section>
</pre>

**空伪类**

“:empty”伪类将选择不包含子元素或者文本的元素。当然，注解、处理指令和空的文本节点并不属于这个范围内。

使用“div:empty”伪类选择器，将选择没有任何子元素或者文本内容为空的“div”元素。以下的示例将选择标记2和标记3，因为他们是完全空的。尽管第二个标签中包含了一个注解标签，但注解标签并不会当作“div”的子元素，因此也属于空的标签。第一个div标签内包含了一个文本，第三个div标签包含了一空白文本空间，最后一个div里包含了一个strong标签，因此这三个标签都被排除未被选择。

**CSS**

<pre class="php">
div:empty {...}	
</pre>

**HTML**

<pre class="xml">
<div>Hello</div>
**<div><!-- Coming soon. --></div>
<div></div>**
<div> </div>
<div><strong></strong></div>
</pre>

**否定伪类**

否定伪类 :not(x) 在选择的元素集合中，通过一个声明来过滤掉符合某种条件的元素。p:not(.intro)选择器利用否定伪类，来匹配所有类名不包含intro的段落元素。通过选择器开头的p来匹配段落元素，之后通过否定伪类括号内的内容来过滤元素，在这里是一个类名.intro。

下面的div:not(.awesome) 与 :not(div)均使用了否定伪类。div:not(.awesome) 选择器识别了不包含awesome类名的div元素。而:not(div) {...} 选择器识别了不是div元素的元素。结果第一行的div元素被匹配，第三行的section元素也被匹配，这些元素被应用样式加粗。唯一未被选中的元素是一个拥有类名awesome的div元素，他被两个否定伪类排除在外。

**CSS**

<pre class="ruby">
div:not(.awesome) {...}
:not(div) {...}	
</pre>

**HTML**

<pre class="xml">
**<div>...</div>**
<div class="awesome">...</div>
**<section>...</section>
<section class="awesome">...</section>	**
</pre>

**伪类示例**

HTML

<pre class="xml">
<table><thead><tr><th>Number</th><th>Player</th>
      <th>Position</th>
      <th>Height</th>
      <th>Weight</th>
      <th>Birthday</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>8</td>
      <td>Marco Belinelli</td>
      <td>G</td>
      <td>6-5</td>
      <td>195</td>
      <td>03/25/1986</td>
    </tr>
    <tr>
      <td>5</td>
      <td>Carlos Boozer</td>
      <td>F</td>
      <td>6-9</td>
      <td>266</td>
      <td>11/20/1981</td>
    </tr>
    <tr>
      <td>21</td>
      <td>Jimmy Butler</td>
      <td>G-F</td>
      <td>6-7</td>
      <td>220</td>
      <td>09/14/1989</td>
    </tr>
    ...
  </tbody>
</table>
</pre>

CSS

<pre class="css">
table {
  border-spacing: 0;
  width: 100%;
}th{
  background: \#404853;
  background: linear-gradient(#687587, #404853);
  border-left: 1px solid rgba(0, 0, 0, 0.2);
  border-right: 1px solid rgba(255, 255, 255, 0.1);
  color: \#fff;
  padding: 8px;
  text-align: left;
  text-transform: uppercase;
}
th:first-child {
  border-top-left-radius: 4px;
  border-left: 0;
}
th:last-child {
  border-top-right-radius: 4px;
  border-right: 0;
}
td {
  border-right: 1px solid \#c6c9cc;
  border-bottom: 1px solid \#c6c9cc;
  padding: 8px;
}
td:first-child {
  border-left: 1px solid \#c6c9cc;
}
tr:first-child td {
  border-top: 0;
}
tr:nth-child(even) td {
  background: \#e8eae9;
}
tr:last-child td:first-child {
  border-bottom-left-radius: 4px;
}
tr:last-child td:last-child {
  border-bottom-right-radius: 4px;
}
</pre>

效果

![伪类示例](http://cdn.w3cplus.com/cdn/farfuture/XiwFuCp25cKzBPQ_kHLBnRjAt40XxoKX-2TVmhkjqH8/mtime:1421035051/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson3-3.jpg)

**伪类概览**

<thbody></thbody>

				例子                       |				 类别         |				 解释                                               
---------------------------- | -------------- | -----------------------------------------------------
				a:link                   |				 链接(link)伪类 |				 选择一个用户没有访问过的链接                                   
				a:visited                |				 链接(link)伪类 |				 选择一个用户访问过的链接                                     
				a:hover                  |				 行为性伪类      |				 选择一个用户将鼠标指针悬浮在上方的元素                              
				a:active                 |				 行为性伪类      |				 选择一个用户使用中的元素                                     
				a:focus                  |				 行为性伪类      |				 选择一个拥有用户焦点的元素                                    
				input:enabled            |				 状态性伪类      |				 选择一个处于可编辑状态(默认)下的元素                              
				input:disabled           |				 状态性伪类      |				 选择一个通过设置disabled属性而处于不可编辑状态下的元素                  
				input:checked            |				 状态性伪类      |				 选择一个被选中的单选或者复选按钮                                 
				input:indeterminate      |				 状态性伪类      |				 选择一个处于不确定状态下的单选或者复选按钮(可能被选中或者不被选中)               
				li:first-child           |				 结构性伪类      |				 选择父元素下的第一个子元素                                    
				li:last-child            |				 结构性伪类      |				 选择父元素下的最后一个子元素                                   
				div:only-child           |				 结构性伪类      |				 如果某个元素是它父元素中惟一的子元素,那么将会被匹配                       
				p:first-of-type          |				 结构性伪类      |				 选择父元素中同类型的第1个子元素                                 
				p:last-of-type           |				 结构性伪类      |				 选择父元素中同类型的最后一个子元素                                
				img:only-of-type         |				 结构性伪类      |				 若元素为父元素中同类型的唯一元素，则会被匹配                           
				li:nth-child(2n+3)       |				 结构性伪类      |				 当父元素中子元素的序列匹配所给数字时会被选中，会以文档树开头作为起点，来计算所有元素       
				li:nth-last-child(3n+2)  |				 结构性伪类      |				 当父元素中子元素的序列匹配所给数字时会被选中，会以文档树开头作为起点，来计算所有元素       
				p:nth-of-type(3n)        |				 结构性伪类      |				 当父元素中子元素的序列匹配所给数字时会被选中，会以文档树开头作为起点，只计算文档树中给定类型的元素
				p:nth-last-of-type(2n+1) |				 结构性伪类      |				 当父元素中子元素的序列匹配所给数字时会被选中，会以文档树开头作为起点，只计算文档树中给定类型的元素
				section:target           |				 目标伪类       |				 选择URI片段标示符的值指向的元素                                
				div:empty                |				 空伪类        |				 选择没有任何子元素或者文本的元素                                 
				div:not(.awesome)        |				 否定伪类       |				 选择不匹配某个状态标示符的元素                                  

#### 	伪元素

伪元素并不存在于dom树中，是一种动态元素。通过选择器操纵[伪元素](http://coding.smashingmagazine.com/2009/08/17/taming-advanced-css-selectors/)，可以给页面的一些特殊部分应用样式。有个要点需要注意，一个选择器只能给一个伪元素，比如：“.el:before”，但不能同时存在多个，比如：“.el:before:after”。

**文本伪元素**

首先发布的两个伪元素是:first-letter 与:first-line 文本伪元素。:first-letter 会匹配一个元素内文字的第一个字母，:first-line 则会匹配第一行。

下面的例子中，段落的第一个字符被alpha 这个class类名设置为较大的字体以及橙色，而bravo这个类名则将段落的第一行也设置成这样。这两个部分分别使用了:first-letter 与:first-line 文本伪元素来得到效果。

**CSS**

<pre class="css">
.alpha:first-letter,
.bravo:first-line {
  color: \#dfa054;
  font-size: 18px;
}
</pre>

**HTML**

<pre class="xml">
<p class="alpha">Lorem ipsum dolor...</p>
<p class="bravo">Integer eget enim...</p>
</pre>

效果

![文本伪元素](http://cdn.w3cplus.com/cdn/farfuture/8F7L_jRZLU8TkviKZPquB0viLNZBPh2ZhMfVEEpHJzQ/mtime:1421035052/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson3-4.jpg)

**生成内容伪元素**

:before与:after生成内容伪元素向被选择的元素内部追加新的行内伪元素。这一类伪元素最普遍的用法，是配合content属性，向页面内添加一些不太重要的内容，但并不常常如此。伪元素不需要使用额外的元素标签，就可以向页面添加一些用户界面相关的内容。

:BEFORE 伪元素可以在被选择元素前创建伪元素，而:AFTER伪元素可以被选择元素后面创建伪元素。这些伪元素嵌入被选择元素内，而不是外面。下面的:after伪类用来在链接内利用括号显示a标签的href属性。这里的信息是有帮助的，但最终，不需要所有浏览器支持这些伪元素。

**CSS**

<pre class="css">
a:after {
  color: \#8c9198;
  content: " (" attr(href) ")";
  font-size: 11px;
}
</pre>

**HTML**

<pre class="xml">
<a href="http://google.com/">Search the Web</a>
<a href="http://learn.shayhowe.com/">Learn How to Build Websites</a>
</pre>

效果

![生成内容伪元素](http://cdn2.w3cplus.com/cdn/farfuture/-TxMHLUPcdSehPERpNkH9P0jOuWuBEEeLbiz7S3mumY/mtime:1421035052/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson3-5.jpg)

**片段伪元素**

::selection片段伪元素选择通过用户操作所选定或者高亮的部分，选定的部分会被应用样式，不过只能使用color,background,background-color,text-shadow属性。值得注意的是background-image属性会被忽略。当利用缩写的background属性来定义样式时，只有背景色会生效，任何图片都会被忽略。

**单个冒号（:）和双冒号（::）**

片段伪元素是css3新增加的内容，为了与伪类所区别，伪元素前前面用双冒号表示。很幸运的是大部分浏览器都支持单引号与双引号两种方式，不过 ::selection伪元素前面必须以双引号开头。

在 ::selection片段伪元素的帮助下，选择下面的示例文字后，背景会变橙色(orange)，且文字阴影会去掉。同时注意使用 ::-moz-selection，增加火狐的浏览器前缀来确保这特性在所有浏览器下都支持完美。

<pre class="css">
::-moz-selection,
::selection {
  background: \#dfa054;
  text-shadow: none;
}
</pre>

效果

![片段伪元素](http://cdn.w3cplus.com/cdn/farfuture/7BfgGuY16jE4Ufy9B0aRPKBvBiuU66IwF5QK2F1TMmk/mtime:1421035052/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson3-6.jpg)

**伪元素举例**

**HTML**

<pre class="xml">
<a class="arrow" href="#">Continue Reading</a>
</pre>

**CSS**

<pre class="css">
.arrow{
  background: \#8ec63f;
  color: \#fff;
  display: inline-block;
  height: 30px;
  line-height: 30px;
  padding: 0 12px;
  position: relative;
}
.arrow:before,
.arrow:after {
  content: "";
  height: 0;
  position: absolute;
  width: 0;
}
.arrow:before {
  border-bottom: 15px solid \#8ec63f;
  border-left: 15px solid transparent;
  border-top: 15px solid \#8ec63f;
  left: -15px;
}
.arrow:after {
  border-bottom: 15px solid transparent;
  border-left: 15px solid \#8ec63f;
  border-top: 15px solid transparent;
  right: -15px;
}
.arrow:hover {
  background: \#f7941d;
  color: \#fff;
}
.arrow:hover:before {
  border-bottom: 15px solid \#f7941d;
  border-top: 15px solid \#f7941d;
}
.arrow:hover:after {
  border-left: 15px solid \#f7941d;
}
</pre>

**效果**

![伪元素举例](http://cdn.w3cplus.com/cdn/farfuture/qL24Xxx99SE3jMt4csDVz7emGcCRWr3Xtbi7792uN3g/mtime:1421035052/sites/default/files/styles/print_image/public/blogs/2013/AdvancedGuide/lesson3-7.jpg)

**伪元素概览**

<thbody></thbody>

				例子                  |				 类别    |				 解释                
----------------------- | --------- | ----------------------
				.alpha:first-letter |				 文本伪元素 |				 选择元素内文本的第一个字母     
				.bravo:first-line   |				 文本伪元素 |				 选择元素内文本的第一行       
				div:before          |				 生成的内容 |				 在被选择元素前创建伪元素      
				a:after             |				 生成的内容 |				 在被选择元素末尾创建伪元素     
				::selection         |				 片段伪元素 |				 选择通过用户操作所选定或者高亮的部分

**选择器浏览器兼容性**

虽然这些选择器为css提供了丰富多彩的能力，让其可以做到一些难以置信的事情，但我们仍然不断地为一些老浏览器的兼容性而困扰。判断这些选择器在你网站访问者常使用的浏览器上的可用性，之后决定他们是否适合你的网站。

CSS3.info提供了一个选择器[测试工具](http://tools.css3.info/selectors-test/test.html)，可以提示你使用的选择器是否被浏览器所支持。 而从浏览器提供商那里参考浏览器兼容性也比较适合。

此外你也可以使用一个js库 [Selectivizr](http://selectivizr.com/) 来给ie6-8提供对选择器的良好的兼容性，也可以用[jquery选择器。](http://api.jquery.com/category/selectors/)

**选择器的速度与性能**

关注选择器的速度与性能是很重要的，因为使用过分复杂的选择器可以降低你的页面渲染速度。保持一丝不苟，当你使用一个选择器时，站在局外人的角度去审视他，考虑是否可以找到更好的解决方案。

#### 	扩展阅读

1.  [《CSS3基本选择器》](http://www.w3cplus.com/css3/basic-selectors)
2.  [《CSS3属性选择器》](http://www.w3cplus.com/css3/attribute-selectors)
3.  [《CSS3伪类选择器》](http://www.w3cplus.com/css3/pseudo-class-selector)
4.  [选择符类型查看](http://selectors.linxz.de/)
5.  [《CSS选择器优化》](http://www.w3cplus.com/css/css-selector-performance)
6.  [《你应该知道的一些事情——CSS权重》](http://www.w3cplus.com/css/css-specificity-things-you-should-know.html)
7.  [The 30 CSS Selectors you Must Memorize](http://net.tutsplus.com/tutorials/html-css-techniques/the-30-css-selectors-you-must-memorize/ "The 30 CSS Selectors you Must Memorize")
8.  [Child and Sibling Selectors](http://css-tricks.com/child-and-sibling-selectors/ "Child and Sibling Selectors")
9.  [CSS3 Substring Matching Attribute Selectors](http://www.css3.info/preview/attribute-selectors/ "CSS3 Substring Matching Attribute Selectors")
10.  [How To Use CSS3 Pseudo-Classes](http://coding.smashingmagazine.com/2011/03/30/how-to-use-css3-pseudo-classes/ "How To Use CSS3 Pseudo-Classes")
11.  [Understanding :nth-child Pseudo-class Expressions](http://reference.sitepoint.com/css/understandingnthchildexpressions "Understanding :nth-child Pseudo-class Expressions")
12.  [Taming Advanced CSS Selectors](http://coding.smashingmagazine.com/2009/08/17/taming-advanced-css-selectors/ "Taming Advanced CSS Selectors")
13.  [CSS 3 selectors explained](http://www.456bereastreet.com/archive/200601/css_3_selectors_explained/)
14.  [Awesome New CSS3 Selectors](http://perishablepress.com/awesome-new-css3-selectors/)
15.  [CSS3 Selectors](http://ie.microsoft.com/testdrive/HTML5/CSS3Selectors/)
16.  [CSS3 Selectors & Browser Support](http://www.standardista.com/css3/css3-selector-browser-support/)
17.  [Browser Support for CSS3 Selectors](http://www.impressivewebs.com/browser-support-css3-selectors/)
18.  [The Lowdown on :Before and :After in CSS](http://designshack.net/articles/css/the-lowdown-on-before-and-after-in-css/)
19.  [CSS ::Selection](http://www.w3cplus.com/content/css-selection)