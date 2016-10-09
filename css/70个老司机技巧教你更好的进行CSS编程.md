# 70个老司机技巧教你更好的进行CSS编程

**CSS 并不总是容易处理。** 在你的能力和经验不够的时候，CSS编程会成为一个噩梦，特别是你不确定为页面元素中选择哪种选择器的时候。使用一个不常见的CSS属性以实现更好的语义化，没有比这个方法更好用的更简单的的实现减少代码复杂度的了。

我们研究了一些很有用的CSS窍门，提示，意见，方法，技巧以及编程解决方案，并在下面列出了他们。我们也把一些开发中会用到却一时无法查到的基础技巧列入其中。

下面列出的**70+条专业CSS建议**可以提高你的CSS编程效率。在文章的结尾可以查阅相关参考文献和文章。

对于那些与读者分享建议，技巧，方法，知识和经验的设计师，我们向他们**表示重心的感谢**。无论是程序员，还是设计师，开发者，信息架构师，不一而足，真的非常感谢。

你可能对我们之前的文章[离不开的53种Css工具](http://www.smashingmagazine.com/2007/01/19/53-css-techniques-you-couldnt-live-without/)[1](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#1)很感兴趣，这篇文章提供了一个CSS基础技巧的基础工具集，你可能在之后的项目中用到他们。

Update (29/05/2007): [文章的巴西-葡萄牙语翻译](http://www.maujor.com/blog/2007/05/29/70-dicas-para-escrever-css/)[2](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#2) 也发布了. 在此致谢 Maurício Samy Silva。

### 1.1. 工作流：开始

- **当你有了设计图之后，开始于一个空白页。** “页面包括页面的页眉，标题，页面示例，页脚。然后开始添加html标记。再然后添加CSS。这样页面效果看起来更好了。” [[CSSing](http://cssing.blogspot.com/2006/02/10-css-tips-for-new.html)[17](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#17)[3](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#3)]
- **使用master样式表** “我观察到初等水平和中等水平开发者都会犯的一个相同的错误，他们都会因为没有移除浏览器的默认CSS样式而困扰。这会导致一个你通过浏览器展现出的设计图与原设计图是矛盾的，最终使很多设计师把这种矛盾归咎于浏览器。当然这是一种误解。因此当你编写网站之前，首先要重置样式表。” [[Master Stylesheet: The Most Useful CSS Technique](http://www.crucialwebhost.com/blog/master-stylesheet-the-most-useful-css-technique/)[4](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#4)], [Ryan Parr]

```
/* master.css */
@import url("reset.css");
@import url("global.css");  
@import url("flash.css");
@import url("structure.css");
```

```
<style type="text/css" media="Screen">
   @import url("css/master.css");
</style>
```

- **首先重置CSS样式** “你可能经常使用某属性的默认值而不是专门为该属性设置一个值。有的开发者倾向于设置[Global white space reset](http://leftjustified.net/journal/2004/10/19/global-ws-reset/)[5](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#5) ，在样式表的顶部将所有元素的margin和padding都设置为0。”[[Roger Johansson](http://www.456bereastreet.com/archive/200503/css_tips_and_tricks_part_1/)[66](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#66)[53](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#53)[49](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#49)[45](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#45)[30](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#30)[23](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#23)[6](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#6)]
- **编写一个辅助CSS类库**此类库用于辅助调试，但是要避免用于已发布的版本中（将标记层与表现层分离）。 你可以使用如下多种类名(即 `...`)来调试标记层。 (*updated*) [[Richard K. Miller](http://www.richardkmiller.com/blog/archives/2006/08/css-best-practices)[7](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#7)]

```
.width100 { width: 100%; }
.width75 { width: 75%; }
.width50 { width: 50%; }
.floatLeft { float: left; }
.floatRight { float: right; }
.alignLeft { text-align: left; }
.alignRight { text-align: right; }
```

- Eric Meyer’s [Global Reset](http://meyerweb.com/eric/thoughts/2007/05/01/reset-reloaded/)[8](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#8), [Christian Montoya’s initial CSS file](http://www.christianmontoya.com/2007/02/01/css-techniques-i-use-all-the-time/)[9](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#9), [Mike Rundle’s initial CSS file](http://businesslogs.com/design_and_usability/my_5_css_tips.php)[10](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#10), [Ping Mag’s initial CSS file](http://www.pingmag.jp/2006/05/18/5-steps-to-css-heaven/)[11](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#11).

### 1.2. 编写你自己的CSS代码

- **编写你自己的CSS样式之使用master样式表** “编写你自己的CSS有助于未来的网站维护。从主样式表开始。在这个样式表里可以引入`reset.css`，`global.css`，`flash.css`（如果需要的话）和 `structure.css` ，有时还有布局样式表。下面是一个 “master”样式表的例子以及它是如何嵌入到文件里的：”

```
h2 { }
#snapshot_box h2 { padding: 0 0 6px 0; font: bold 14px/14px "Verdana", sans-serif; }
#main_side h2 { color: #444; font: bold 14px/14px "Verdana", sans-serif; }
.sidetagselection h2 { color: #fff; font: bold 14px/14px "Verdana", sans-serif; }
```

- **编写你自己的样式表之使用标记** “把你的样式表分为具体的部分：即全局样式-（body，paragraphs， lists等），页眉，页面结构，标题，字体样式，导航栏，表单，注释，其他内容。[[编写CSS样式表的5个tips](http://www.erraticwisdom.com/2006/01/18/5-tips-for-organizing-your-css)[12](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#12)]

```
`/* ------------------------*/ /* ---------->>> GLOBAL <<<-----------*/ /* ------------------------*/`
```

- **编写你自己的样式之制作一个内容表** 在你CSS文件的顶部，编写一个内容表。例如，你可以概括出CSS文件所设置样式（header,main,footer等）的不同区域。然后，设置一个大的明显的板块断点来划分这些区域。Then, use a large, obvious section break to separate the areas. [[5 Steps to CSS Heaven](http://www.pingmag.jp/2006/05/18/5-steps-to-css-heaven/)[89](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#89)[24](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#24)[13](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#13)]
- **编写你自己的样式表之按字母顺序排列属性** “我忘了我是从哪里得到这个灵感的，但在将CSS属性按字母排序一个月以来，不管你信不信，这个方法使一些特殊的属性很容易找到。” [[Christian Montoya](http://www.christianmontoya.com/2007/02/01/css-techniques-i-use-all-the-time/)[38](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#38)[14](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#14)]

```
body {
   background: #fdfdfd;
   color: #333;
   font-size: 1em;
   line-height: 1.4;
   margin: 0;
   padding: 0;
}
```

- **划分单独的代码块**. “这对一些人来说可能是常识，但是有时我看到一些CSS并没有被分解成几部分。这样做可以让你更容易的处理数周、数月甚至数年后的代码。你能够轻而易举的找到需要修改的类和元素。如： `/* Structure */`, `/* Typography */`等” [[CSS Tips and Tricks](http://www.blogherald.com/2006/09/08/css-tips-and-tricks/)[15](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#15)]
- **挂钩，线和铅坠。** “当CSS及其分段都准备就绪，你会开始考虑选择器要钩在哪里，那么接下来就需要依靠在你的标记里使用结构挂钩。这为网站未来的编写和维护创造了优势，也增强了文档的健壮性。” [Ryan Parr]
- **将样式表分解成单独的代码块** “我把自己的样式表分解成三个单独的代码块。第一部分是直接的元素声明。改变body、一些links样式、一些header样式，以及重置窗体的margin和padding等等。 […] 在元素声明之后是类声明：一些像错误信息或者callout的东西会放在这里。 [..] 最后我开始声明主容器，然后对这个容器里的元素样式进行缩进。扫视之后我就能看清楚我的页面是如何划分的，而且找一些东西也会变得很容易。即使容器里没有任何内容我也会声明它。” [[Jonathan Snook](http://snook.ca/archives/html_and_css/top_css_tips/)[68](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#68)[34](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#34)[18](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#18)[16](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#16)]

### 1.3. 工作流程：处理ID、类、选择器和属性。

- **使容器保持最小化。** “将你的文档从结构臃肿中拯救出来。新手开发者倾向于使用很多类似于表格单元格的DIV来实现布局。实际上许多其他结构元素都可以用来实现布局。不要使用过多的DIV。在使用过多的包装（DIV）去实现效果前考虑所有的选择，会发现使用一点漂亮的CSS也能达到相同的预期效果。” [Ryan Parr]
- **使属性保持最少化** “工作时要多思考而不是纠结于CSS。在这条规则之下会衍生出很多子规则：如果添加一个CSS属性不是必需的，那么不要添加；如果你不确定为什么要添加一个CSS属性，不要添加；如果你感觉同一个属性添加了很多次，那么把它们找出来处理后只添加一次。” [[CSSing](http://cssing.blogspot.com/2006/02/10-css-tips-for-new.html)[17](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#17)[3](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#3)]
- **使选择器保持最小化** “避免不必要的选择器。使用较少的选择器意味着在实现特殊样式时所重写的选择器也较少-这更有利于故障排除。” [[Jonathan Snook](http://snook.ca/archives/html_and_css/top_css_tips/)[68](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#68)[34](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#34)[18](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#18)[16](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#16)]
- **使CSS hack保持最少** “除非遇到了已知的已公布的bug，否则不要使用hack。这是一个很重要的要点，因为我也经常看到hack被用来处理一些压根儿就没有问题的东西。如果你发现需要找一个hack来处理某个设计中的问题，那么首先你需要做一些调查（Google这里能派上用场），然后试着鉴定一下你遇到的这个问题（是否真的需要hack来处理）。[[10 Quick Tips for an easier CSS life](http://www.search-this.com/2007/03/26/10-quick-tips-for-an-easier-css-life/)[19](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#19)]
- **在敏捷开发中使用CSS常量** “常量的概念-通过你的代码可以使用的固定值是有用的。有一种应对CSS中缺乏常量的方法是在CSS文件顶部注释中添加一些相关的定义来定义‘常量’。这种方法常见的一种应用是‘创建颜色词汇表’。这种方法可以让你对网站中使用的颜色有一个快速的参考，避免在使用颜色时失误，并且一旦你需要修改颜色，你可以马上利用这个速查表进行搜索和替换。” [[Rachel Andrew](http://24ways.org/2006/faster-development-with-css-constants)[20](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#20)]

```
/*
   # Dark grey (text): #333333
   # Dark Blue (headings, links) #000066
   # Mid Blue (header) #333399
   # Light blue (top navigation) #CCCCFF
   # Mid grey: #666666 #
*/
```

- **使用一个通用的命名系统。** 在寻找bug或者更新文件时，如果你有一个id和class的命名系统会节省很多时间。特别是大型的CSS文件，如果命名不规范，很快就会导致巨大的混乱。我推荐使用`parent_child`模式。 [[10 CSS Tips](http://christopher-scott.org/blog/10-css-tips-you-might-not-have-known-about)[67](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#67)[43](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#43)[21](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#21)]
- **根据class和id的语义适当的为他们命名。** “我们倾向于避免表明表象方面的命名。否则，如果我们命名一些右列的东西，完全可能改变CSS并且“右列”最终在页面的左边显示。这在未来可能导致混乱，所以最好避免这种表象的命名方案。 [[Garrett Dimon](http://www.digital-web.com/articles/markup_as_craft/)[22](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#22)]
- **分类常见的CSS声明选择器。** “分类选择器。当一些元素类型，类或者id共享一些属性时，你可以分类选择器避免在有些时候设置了相同的属性。这将会节省潜在的大量空间。” [[Roger Johansson](http://www.456bereastreet.com/archive/200503/css_tips_and_tricks_part_1/)[66](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#66)[53](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#53)[49](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#49)[45](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#45)[30](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#30)[23](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#23)[6](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#6)]
- **将你可能会重复使用很多次某个唯一的属性单独分离出来。** “如果你发现你使用某个唯一的属性很多次，为了使你不再一遍又一遍的重复不仿将其分离出来，而且也使你能够改变网站中所有使用过此属性的部分的显示。” [[5 Steps to CSS Heaven](http://www.pingmag.jp/2006/05/18/5-steps-to-css-heaven/)[89](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#89)[24](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#24)[13](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#13)]
- **尽量将id和class的命名持平文档树** 尽可能的使用 [上下文选择器](http://www.456bereastreet.com/archive/200509/css_21_selectors_part_1/)[25](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#25) 。不要担心这样做会使选择器变得冗长。长的选择器会使css文档更容易阅读，也减少了发展成 classitis 或者 [divitis](http://juicystudio.com/article/div-mania.php)[26](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#26)的可能。[[Chric Casciano](http://placenamehere.com/article/156/TenSimpleCSSTips)[76](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#76)[41](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#41)[27](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#27)]
- **学会利用CSS级联的特性** “比方说你的网站里有两个相似的有些许不同的盒模型-你可以分别为每个盒模型写好CSS样式，也可以为两个盒模型写一个CSS样式，然后再下面写出两个盒模型的不同属性样式来区分两个盒模型。” [[5 Steps to CSS heaven](http://www.pingmag.jp/2006/05/18/5-steps-to-css-heaven/)[28](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#28)]
- **使用实用标签: , * 和 \*** “很多时候在设计中会设置一个对各种印刷权重做出要求的部分，比如设置为同一行或者字与字之间间距很近。这些设置分散在各个div和class中，我觉得它们不符合语义化，而且会干扰你一直遵循的良好的XHTML准则。” 建议使用语义化标签代替这些设置。[[Mike Rundle’s 5 CSS Tips](http://businesslogs.com/design_and_usability/my_5_css_tips.php)[29](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#29)]

### 1.4. 工作流程: 使用简写标记

- **缩写16进制颜色标记。** “在CSS中，一种颜色由三对十六进制数组成，当你使用这种颜色标记时，你可以使用省略每组的第二个数字这种有效率的方法：`#000 相当于 #000000, #369 相当于 #336699`。 [[Roger Johansson](http://www.456bereastreet.com/archive/200503/css_tips_and_tricks_part_1/)[66](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#66)[53](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#53)[49](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#49)[45](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#45)[30](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#30)[23](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#23)[6](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#6)]
- **根据LoVe/HAte排序法定义伪类链接。**: Link, Visited, Hover, Active. “首先确定你了解各种链接样式，然后最好把样式按照“link-visited-hover-active”或者“LVHA”顺序排列。如果你关注焦点样式，那么可以在这之后加入—但是在决定之前看一下这个解释。” [[Eric Meyer](http://meyerweb.com/eric/css/link-specificity.html)[31](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#31)]

```
a:link { color: blue; }
a:visited { color: purple; }
a:hover { color: purple; }
a:active { color: red; }
```

- **按照TRouBLed排序法定义元素的margin, padding 或者border **: Top, Right, Bottom, Left. “这里介绍一个简写定义元素的margin,padding或border的方法，从top开始按照顺时针：Top, Right, Bottom, Left。” [[Roger Johansson](http://www.456bereastreet.com/lab/developing_with_web_standards/css/)[44](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#44)[32](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#32)]
- **你可以使用 简写属性33.** “为 `margin`, `padding` and `border` 使用简写属性可以节省很大空间。”

```
margin: top right bottom left;
margin: 1em 0 2em 0.5em;
(margin-top: 1em; margin-right: 0; margin-bottom: 2em; margin-left: 0.5em;)
```

```
border: width style color;
border: 1px solid #000;
```

```
background: color image repeat attachment position;
background: #f00 url(background.gif) no-repeat fixed 0 0;
```

```
font: font-style (italic/normal) font-variant (small-caps) font-weight font-size/line-height font-family;
font: italic small-caps bold 1em/140% "Lucida Grande",sans-serif;
```

### 1.5. 工作流程: 设置字体

- **在body标签里设置字号为62.5%从而像使用px一样使用EM**. `font-size`的默认值是16px; 应用这个规则之后，Em的值大约相当于10px(16 x 62.5% = 10).“我更倾向于在body标签里设置字号为:62.5%。这种方法能够在考虑px时使用em去指定大小，例如，1.3em几乎相当于1.3px。 ” [[Jonathan Snook](http://snook.ca/archives/html_and_css/top_css_tips/)[68](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#68)[34](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#34)[18](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#18)[16](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#16)] （译者注：经众成翻译用户[拉着你的手说爱你]提示，在chrome中默认最小字体12px，所以这种方法在chrome中不适用。）


- **使用通用字符集进行编码**. “[..] 答案就是使用单独的通用字符集去覆盖大部分异常事件。幸运的是这种字符集是存在的：基于Unicode的UTF-8。Unicode是一种行业标准，是为了使所有语言的文字和符号能够为电脑一视同仁的所表示和操控而设计的。 UTF- 8 应该像这样包含在你的网页页头中。” [[20 pro tips](http://www.netmag.co.uk/zine/design-tutorials/20-pro-tips)[77](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#77)[71](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#71)[36](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#36)[35](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#35)]

```
`<meta http-equiv="content-type" content="text/ html;charset=utf-8" />`
```

- **你可以使用CSS来切换大写。** 如果你需要吧一些东西转换成大写，比如一个标题，又不行重写一个副本，那么可以使用CSS来进行这项无聊的工作。下面的代码会将目标h1的所有文本转化为大写，无论是什么格式”。 [[20 pro tips](http://www.netmag.co.uk/zine/design-tutorials/20-pro-tips)[77](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#77)[71](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#71)[36](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#36)[35](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#35)]

```
`h1 { text-transform: uppercase; }`
```

- **你可以用small-caps自动显示文本。** `font-variant` 属性是用来显示小型大写字母文本，这其中所有的小写字母被转化为大写字母，但是所有的小型大写字母下的文本相比其余的文本字号较小。

```
`h1 { font-variant: small-caps; }`
```

- **定义通用字体类型来覆盖通用设置。** “当我们声明一个设计中使用的特定字体时，我们会希望这种字体以及在用户的系统中安装。简单的说如果他们的系统没有安装这个字体，那么将无法看到这个字体。我们需要做的就是参考用户在他们机器上可能会安装的字体，比如下面的font-family属性。我们完成一个通用字体类型是非常重要的。”[[Getting into good coding habits](http://www.communitymx.com/content/article.cfm?cid=FAF76&print=true)[37](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#37)]

```
`p { font-family: Arial, Verdana, Helvetica, sans-serif; }`
```

- **将line-height设置为1.4em – 1.6em。** “`line-height:1.4`”为易读的行，合理的行高避免了行超过10个字而过长，而且颜色对比也不会太不明显。比如，对于过亮的CRT显示屏来说，纯黑色在纯白色的背景下往往对比太强烈，因此我尝试运用米白色(`#fafafa`是一个好的选择)和暗灰色（`#333333`也不错）。” [[Christian Montoya](http://www.christianmontoya.com/2007/02/01/css-techniques-i-use-all-the-time/)[38](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#38)[14](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#14)]
- **设置 html-元素为100.01%。** 这个针对字号的奇怪100.01%会对几个浏览器bug进行弥补。首先，设置一个默认的body百分比字号（而不是em）消除了IE/Win系统中的字体缩放比例问题，即使之后在其它元素中设置为em。此外，一些版本的Opera浏览器会设置一个比其他浏览器小的100%的默认字号。另一方面，Safari浏览器却有一个101%字号的问题。目前流行的最佳解决方案是针对这个属性设置为100.01%的值。” [[CSS: Getting into good habits](http://www.communitymx.com/content/article.cfm?cid=FAF76&print=true)[39](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#39)]

### 1.6. 工作流程: 调试

- **添加边框以确定容器** “在构建文档或者调整布局问题时使用大量的测试样式，比如额外的边框或者背景颜色。`div { border:1px red dashed; }`就像一个小装饰品。这里有 [应用边框的书签](http://www.squarefree.com/bookmarklets/webdevel.html)[40](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#40) ，并且还能为你做其它事情。” 你也可以使用 `* { border: 1px solid #ff0000; }`. [[Chric Casciano](http://placenamehere.com/article/156/TenSimpleCSSTips)[76](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#76)[41](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#41)[27](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#27)]. 为元素添加一个边框来认清它们，这样有助于识别正常情况下不易察觉的重叠部分或者额外的空白部分。[[CSS Crib Sheet](http://www.mezzoblue.com/css/cribsheet/)[69](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#69)[42](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#42)]

```
`* { border: 1px solid #f00; }`
```

- **在调试前首先检查封闭的元素。** “如果你曾经因为只修改了很少的东西就破坏了你优美的宝贝布局而沮丧，那么很可能是因为没有封闭的元素。[[10 CSS Tips](http://christopher-scott.org/blog/10-css-tips-you-might-not-have-known-about)[67](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#67)[43](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#43)[21](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#21)]

### 2.1. 技术性技巧: IDs, Classes

- **每个页面一个id，每个页面很多class。** “检查你使用的id:文档中只有一个元素能使用某个值的id属性，而共享同一个类名的元素个数是无限制的。[..]class名和id名只能由字母[A-Za-z0-9]和连字符 (-)组成，而且不能由连字符或者数字开头(参考 CSS2 的语法和基本数据类型)。” [[Roger Johansson](http://www.456bereastreet.com/lab/developing_with_web_standards/css/)[44](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#44)[32](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#32)]


- **区分选择器中元素名的大小写。** “记住要严格区分大小写。当CSS与XHTML用在一起时，选择器中的元素名是区分大小写的。为了避免这个问题我总是推荐在CSS选择器中使用小写的元素名。class和id属性值在HTML和XHTML中都是区分大小写的，所以要避免混合大小写的class和id名字。”[[Roger Johansson](http://www.456bereastreet.com/archive/200503/css_tips_and_tricks_part_1/)[66](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#66)[53](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#53)[49](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#49)[45](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#45)[30](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#30)[23](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#23)[6](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#6)]
- **CSS中的class与id必须是有效的**“即 [由字母开头](http://www.w3.org/TR/html401/types.html#type-id)[46](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#46), 而不是数字或者下划线。id必须是唯一的。他们的名字应当 [具有普遍性](http://www.w3.org/QA/Tips/goodclassnames)[47](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#47),能够描述功能而不是装装样子。” [[CSS Best Practices](http://learningtheworld.eu/2006/best-practices/#css)[48](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#48)]
- **你可以将多个class的名字分配给一个给定的元素。** “你可以将多个class的名字分配给一个元素。这样有利于书写不同的规则来定义不同的属性，并且只在需要的地方应用它们。” [[Roger Johansson](http://www.456bereastreet.com/archive/200503/css_tips_and_tricks_part_1/)[66](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#66)[53](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#53)[49](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#49)[45](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#45)[30](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#30)[23](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#23)[6](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#6)]

### 2.2. 技术性技巧：充分用好选择器。

Roger Johansson写了一系列关于[CSS 2.1 选择器](http://www.456bereastreet.com/archive/200509/css_21_selectors_part_1/)[50](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#50)的**非常**有实用性的文章。这篇文章**重磅推荐** – 下面会列举其中一些有用的方面。要注意IE6及其更早的版本是不支持选择器 ‘>’ 和 ‘+’的。 (*updated*).

- **你可以使用子选择器** “一个子选择器指向某个元素的直接孩子。一个子选择器由两个或者更多的选择器组成，这些选择器由大于号“>”分割。父类在大于号“>”的左边，并且选择符和选择器之间允许出现空格。这个规则会影响所有div元素下的strong元素。 [[Roger Johansson](http://www.456bereastreet.com/archive/200510/css_21_selectors_part_2/)[52](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#52)[51](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#51)]

```
`div > strong { color:#f00; }`
```

- **你可以使用相邻选择器。** 一个相邻选择器由两个简单的选择器组成，这两个选择器由加号“+”分开。相邻选择器内部允许出现空格。这个选择器匹配一个元素，这个元素是前一个元素的相邻元素。这两个元素必须有相同的父元素，并且第一个元素必须是紧挨第二个元素。[[Roger Johansson](http://www.456bereastreet.com/archive/200510/css_21_selectors_part_2/)[52](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#52)[51](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#51)]

```
`p + p { color:#f00; }`
```

- **你可以使用属性选择器。** 属性选择器匹配的元素是基于这个属性的存在或值。下面是四条属性选择器的匹配情况：

```
[att] 匹配包含att属性的元素，无论它是什么值。
[att=val] 匹配包含属性att值为“val”的元素。
[att~=val] 匹配含属性att，且att的值中包含“val”的元素。这种情况下“val”中不能包含空格。
[att|=val] 匹配含属性att且值为连字号分割的开头为“val”的元素。这种匹配主要用于匹配由lang属性(xml:lang in XHTML)指定的语言码，即 “en”, “en-us”, “en-gb”等。
```

- 下面规则中的选择器匹配含`title`属性的`p`元素，无论它是什么值：

```
`p[title] { color:#f00; }`
```

- 这个选择器匹配所有的class属性值为error的div元素:

```
`div[class=error] { color:#f00; }`
```

- 多属性的选择器可以用于同一个选择器。这个方法可以实现对同一个元素的不同属性的匹配。下面的规则将适用于所有类值为“quate”且包含cite属性的blockquote元素：

```
`blockquote[class=quote][cite] { color:#f00; }`
```

- **你也可以使用后代选择器。** “后代选择器可以帮助你从你的标记中消除很多类属性，从而是你的CSS选择器更加的有效。 ” [[Roger Johansson](http://www.456bereastreet.com/archive/200503/css_tips_and_tricks_part_1/)[66](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#66)[53](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#53)[49](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#49)[45](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#45)[30](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#30)[23](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#23)[6](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#6)]

### 2.3.技术性技巧:样式链接

- **如果你使用锚，在设计链接时要小心。** “如果你在代码中使用了经典的锚(`[`](undefined)) ，那么你会注意到它失去了`:hover`和`:active` 伪类作用。为了避免这种情况，你需要为锚设置`id`而不是用[略晦涩难懂](http://dbaron.org/css/1999/09/links)[54](https://hackhands.com/70-Expert-Ideas-For-Better-CSS-Coding/#54)的语法： `:link:hover, :link:active`来设计。” [[Dave Shea](http://www.mezzoblue.com/css/cribsheet/)[55](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#55)]

- **为链接定义关系。** “rel属性是用来从一个资源指向另一个资源表示语义链接关系。

  ```
  a[rel~="nofollow"]::after { content: "2620"; color: #933; font-size: x-small; }
  a[rel~="tag"]::after { content: url(http://www.technorati.com/favicon.ico); }
  ```

- “这些使用空格分隔的值列表的属性选择器。包含这些值的关系的任何一个元素将会被匹配。含禁止链接关联的链接将会伴随一个暗红色的骷髅头（？）而标签关联的链接将会伴随一个Technocrati图标。” [[Handy CSS](http://lachy.id.au/log/2005/04/handy-css)[90](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#90)[57](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#57)[56](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#56)]

- 你可以自动标记外部链接。许多人利用非标准关联 `rel="external"`来指定一个外部站点的链接。然而，把它添加到每一个link上是消耗时间并且没有必要的。这个样式规则将会使网站上的外部链接放在一个东北向箭头上。[[Handy CSS](http://lachy.id.au/log/2005/04/handy-css)[90](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#90)[57](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#57)[56](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#56)]

```
`a[href^="http://"]:not([href*="smashingmagazine.com"])::after { content: "2197"; }`
```

- **你可以使用 outline: none;来去除链接的虚线**使用 `outline: none;`[去除链接虚线](http://sonspring.com/journal/removing-dotted-links)[58](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#58)：

```
`a:focus { outline: none; }`
```

### 2.4. 技术性技巧: CSS-Techniques

- **你可以指定body标签的id。** “大多数情况下在body标签上设置一个id有助于操作CSS的表面条目及标记页面的基础元素。你不仅仅可以组织你的章节，而且还可以在不改变模板和标记的情况下创建多个CSS样式。” [Ryan Parr, [Invasion of Body Switchers](http://alistapart.com/articles/bodyswitchers)[59](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#59)]
- **你可以通过CSS创建高度相等的列。** [等高技术](http://www.positioniseverything.net/articles/onetruelayout/equalheight)[60](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#60): 使所有列展示为相同高度的方法。但是没有伪列式背景图片的需要。 [伪列](http://www.alistapart.com/articles/fauxcolumns/)[61](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#61): 结合背景图片。
- **你可以使CSS垂直对齐。** “比方说一个导航菜单，高度指定为2em。解决方法：在CSS中将行高设置为与盒子高度相同。 在这种情况下，盒子高度是2em，因此我们可以在CSS规则中设置line-height：2em，那么盒子中的文本将会浮动在中间位置。” [[Evolt.org](http://evolt.org/article/rdf/17/60369/)[62](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#62)]
- **你可以使用伪元素和类来动态生成内容。** [伪类和伪元素](http://www.456bereastreet.com/archive/200510/css_21_selectors_part_3/)[63](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#63). 伪类和伪元素可以用来格式化元素，这些元素的信息都是在文档树中无法得到的。例如，没有元素指向一段的第一行或者一个元素文本的第一个字母。你可以使用 :first-child, :hover, :active, :focus, :first-line, :first-letter, :before, :after and more.
- **你可以使用来优雅的分隔帖子。** “重新设计的水平规则 (

------

) 结合图片将会给网页很大程度的加分。[[CSS: Best Practices](http://www.richardkmiller.com/blog/archives/2006/08/css-best-practices)[64](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#64)]

- **你可以在每页上都是用相投的导航(X)HTML代码。** “大多数网站突出了用户位置的导航栏。但是这样会很痛苦，因为你必须调整每一个页面的导航栏后面的HTML代码。能不能找到一个两全其美的方法呢？” [[Ten More CSS Tricks you may not know](http://www.sitepoint.com/article/top-ten-css-tricks)[65](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#65)]

```
<ul>
   <li><a href="#" class="home">Home</a></li>
   <li><a href="#" class="about">About us</a></li>  
   <li><a href="#" class="contact">Contact us</a></li>
</ul>
```

- 将一个`id` 加入到 `body` 标签中。这个id应该能表现出网站中用户的位置，并且当用户访问站点的不同部分时也能随之变化。

```
`#home .home, #about .about, #contact .contact {  commands for highlighted navigation go here }`
```

- **使用margin: 0 auto; 实现水平居中布局。** “要实现用CSS水平居中一个元素，你需要指定这个元素的宽度和水平的margin。” [Roger Johansson]

```
 `<div id="wrap"> <!-- Your layout goes here --> </div>`
```

```
`#wrap { width:760px; /* Change this to the width of your layout */  margin:0 auto; }`
```

- **你可以将CSS样式添加到RSS源。** “你可以用XSL样式表做很多事情（将链接转化为可点击链接等），但是CSS可以使非专业人员对你的代码不那么恐惧。 [Pete Freitag]

```
`<?xml version="1.0" ?> <?xml-stylesheet type="text/css" href="http://you.com/rss.css" ?>  ...`
```

- **你可以隐藏旧浏览器的CSS。** “从旧的浏览器隐藏CSS文件的一种常用方法是使用`@import`的诀窍。 [[Roger Johansson](http://www.456bereastreet.com/archive/200503/css_tips_and_tricks_part_1/)[66](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#66)[53](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#53)[49](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#49)[45](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#45)[30](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#30)[23](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#23)[6](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#6)]

```
`@import "main.css";`
```

- **别忘了声明块级元素中的margin和padding。** [[10 CSS Tips](http://christopher-scott.org/blog/10-css-tips-you-might-not-have-known-about)[67](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#67)[43](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#43)[21](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#21)]
- **设置宽度或者margin和padding。** “我的经验法则是，如果设置了一个宽度，就不设置margin或padding。同样，如果设置了一个margin或padding，就不设置宽度。处理盒模型是就是会有如此的痛苦，特别是当你处理百分比的那种。所以，我设置外部容器的宽度，然后对其中的元素设置margin和padding。如此一来一切都会顺利。” [[Jonathan Snook](http://snook.ca/archives/html_and_css/top_css_tips/)[68](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#68)[34](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#34)[18](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#18)[16](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#16)]
- **避免将padding/border和固定宽度应用到元素中。** “IE5的盒模型是有误的，这带来了一大堆麻烦。这其中有很多解决方案，但是最好是通过设置父元素的padding来避开这个问题，而不是对子元素设置固定宽度。 [[CSS Crib Sheet](http://www.mezzoblue.com/css/cribsheet/)[69](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#69)[42](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#42)]
- **提供打印样式。** “你可以像加入一个正规样式一样为你的页面加入一个打印样式：

```
`<link rel="stylesheet" type="text/css" href="print.css" media="print">`
```

或

```
`<style type=”text/css” media=”print”> @import url(print.css); </style>`
```

- 这将确保此CSS只会应用于打印时的页面而不会影响这个页面在屏幕上的显示。应用新的打印样式后你可以确保实现白色背景下的实心黑色文本并且移除多余的特性，极大提高可读性。 [More about CSS-based print-Layouts](http://www.smashingmagazine.com/2007/02/21/printing-the-web-solutions-and-techniques/)[70](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#70). [[20 pro tips](http://www.netmag.co.uk/zine/design-tutorials/20-pro-tips)[77](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#77)[71](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#71)[36](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#36)[35](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#35)]

### 2.5. 技术性技巧: IE 调整

- **你可以强制使IE应用透明PNG图片。** “理论上，PNG文件支持各种级别的透明程度；然而，一个IE6的bug阻碍了这个属性的跨浏览器运作。” [[CSS Tips, Outer-Court.com](http://blog.outer-court.com/archive/2007-03-30-n51.html)[72](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#72)]

```
#regular_logo { background: url('test.png'); width:150px; height:55px; }
* html #regular_logo {
   background:none;
   float:left;
   width:150px;
   filter:progid:DXImageTransform.Microsoft.AlphaImageLoader(src='test.png', sizingMethod='scale');
}
```

- **你可以在IE中定义min-width 和 max-width 。**[[Ten More CSS Trick you may not know](http://www.sitepoint.com/article/top-ten-css-tricks)[73](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#73)]

```
#container {
   min-width: 600px;
   max-width: 1200px;
   width:expression(document.body.clientWidth < 600? "600px" : document.body.clientWidth > 1200? "1200px" : "auto");
}
```

- **你可以为IE设置条件注释。** “IE/Win条件下最安全的处理方式是使用条件注释。使用微软专有的条件注释感觉起来比CSS hack更有前途。你可以利用这个方法为IE/Win设置一个单独的样式表，这个样式表包含所有使其正确运作的必须的规则。” [[Roger Johansson](http://www.456bereastreet.com/archive/200503/css_tips_and_tricks_part_2/)[74](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#74)]

```
`<!--[if IE]> <link rel="stylesheet" type="text/css" href="ie.css" /> <![endif]-->`
```

### 工作流程:获得灵感

- **娱乐试验向CSS** “去玩。玩背景图。玩浮动. ” [[Play with positive and negative margins](http://chunkysoup.net/article/12/AbusingMargins)[75](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#75). 玩继承和级联规则。就是玩。[[Chric Casciano](http://placenamehere.com/article/156/TenSimpleCSSTips)[76](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#76)[41](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#41)[27](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#27)]
- **向别人学习** 从别人优秀的网站中汲取知识。任何网站的HTML都可以轻易的通过查看网页的源代码得到。观察别人是如何做的并把他们的方法应用到自己的中做种。 [[20 pro tips](http://www.netmag.co.uk/zine/design-tutorials/20-pro-tips)[77](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#77)[71](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#71)[36](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#36)[35](http://www.zcfy.cc/article/70-expert-ideas-for-better-css-coding-hackhands-1078.html#35)]

### 来源及相关

- [CSS Tips and Tricks](http://www.456bereastreet.com/archive/200503/css_tips_and_tricks_part_1/) by *Roger Johansson*
- [(The Only) Ten Things To Know About CSS](http://blog.jm3.net/2007/03/16/the-only-ten-things-to-know-about-css/) by *John Manoogian*
- [CSS Crib Sheet](http://www.mezzoblue.com/archives/2003/11/19/css_crib_she/) by *Dave Shea*
- [My Top Ten CSS Tricks [CSS Tutorials\]](http://www.sitepoint.com/article/top-ten-css-tricks) by *Trenton Moss*
- [CSS Tips](http://blog.outer-court.com/archive/2007-03-30-n51.html) by *Philipp Lenssen*
- [Top CSS Tips](http://www.snook.ca/archives/html_and_css/top_css_tips/) by *Jonathan Snook*
- [Ten CSS tricks — corrected and improved](http://tantek.com/log/2004/09.html#d07t1434) by *Tantek Çelik*
- [Ten More CSS Trick you may now know](http://www.webcredible.co.uk/user-friendly-resources/css/more-css-tricks.shtml) by *Trenton Moss*
- [CSS techniques I use all the time](http://www.christianmontoya.com/2007/02/01/css-techniques-i-use-all-the-time/) by *Christian Montoya*
- [CSS Tip Flags](http://www.stopdesign.com/log/2005/05/03/css-tip-flags.html) by *Douglas Bowman*
- [My 5 CSS Tips](http://businesslogs.com/design_and_usability/my_5_css_tips.php) by *Mike Rundle*
- [5 Steps to CSS Heaven](http://www.pingmag.jp/2006/05/18/5-steps-to-css-heaven/) by *Ping Mag*
- [Handy CSS](http://lachy.id.au/log/2005/04/handy-css) by *Lachlan Hunt*
- [Erratic Wisdom: 5 Tips for Organizing Your CSS](http://erraticwisdom.com/2006/01/18/5-tips-for-organizing-your-css) by *Thame Fadial*
- [15 CSS Properties You Probably Never Use (but perhaps should)](http://www.seomoz.org/blog/css-properties-you-probably-never-use) by *SeoMoz*
- [10 CSS Tips You Might Not Have Known About](http://christopher-scott.org/blog/10-css-tips-you-might-not-have-known-about) by *Christopher Scott*
- [A List Apart: Articles: 12 Lessons for Those Afraid of CSS and Standards](http://www.alistapart.com/articles/12lessonsCSSandstandards) by *Ben Henick*
- [Tips for a better design review process](http://www.dkeithrobinson.com/entry/tips_for_a_better_design_review_process/) by *D. Keith Robinson*
- [20 pro tips – .net magazine](http://www.netmag.co.uk/zine/design-tutorials/20-pro-tips) by *Jason Arber*
- [CSS Best Practices](http://www.richardkmiller.com/blog/archives/2006/08/css-best-practices) by *Richard K Miller*
- [10 Quick Tips for an Easier CSS Life](http://www.search-this.com/2007/03/26/10-quick-tips-for-an-easier-css-life/) by *Paul Ob*
- 10 CSS Tips from a Professional CSS Front-End Architect by *72 DPI in the shade team blog*
- [Web Design References: Cascading Style Sheets](http://www.d.umn.edu/itss/support/Training/Online/webdesign/css.html#tips) by *Laura Carlson*
- [Getting Into Good Coding Habits](http://www.communitymx.com/content/article.cfm?cid=FAF76&print=true) by *Adrian Senior*