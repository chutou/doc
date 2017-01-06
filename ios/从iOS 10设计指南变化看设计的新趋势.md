# 从iOS 10设计指南变化看设计的新趋势

9月7日，Apple将会召开本年度的秋季发布会，发布的新产品包括新款的MacBook Pro、iPhone 7以及Apple Watch 2。

但是我更加关注的是随着iPhone 7一起发布的iOS 10正式版，因为在之前6月份的WWDC 2016大会上，Apple就宣称iOS 10是「The biggest iOS release ever」，这次正式版的发布，Apple应该会对iOS 10给予重大的期望。

在iOS 10正式发布前夕，本文主要针对已经发布的iOS 10的人机界面设计指南（Human Interface Guidelines，简称HIG）来对比分析新老版本的iOS系统在设计上究竟有哪些改变，有哪些设计趋势值得我们注意。

## **改变：越来越像给设计师用的「设计指南」**

首先，我们先来看一下iOS 10之前的HIG历史版本记录，了解一下在以前的版本中Apple都做了些什么：

![](https://isux.tencent.com/wp-content/uploads/2016/09/052906-54254-630x433.png)

图1 iOS HIG Revision History

自从iOS 7开始，每个版本的HIG都是在**同一个框架**中进行维护的，而且维护频率之低改动幅度之小令人发指（当然跟Apple一贯的严谨风格有关）

而针对设计部分的内容一共也只有两次改动，这种情况一直持续到iOS 9，如果你愿意把iOS 7、8、9三个版本的HIG拿出来一起看，简直就是在玩**找茬游戏**。

然后，我们再拿iOS 9 和 iOS 10 的HIG结构框架进行一下对比：

![construction3](https://isux.tencent.com/wp-content/uploads/2016/09/051352-60046.png)

图2 iOS HIG版本对比

### **几乎是完全不同的结构框架！**

历经三年以及三个版本都没动过的框架被开了刀，我相信Apple的设计师绝对不是因为闲的无聊才干出这种事的。

对于Apple这种严谨且强迫症的公司来说，做每一件事必然有其原因，这里面传递出了一个信号：iOS 10的设计会发生**「****重大改变」**，而Apple也期望通过设计的改变来获取更多的用户。

让我们把视角再深入到具体的章节中，看看都有些什么变化：

1）**增加**了之前没有过的**Interaction**章节 (主要内容为软硬件与用户的交互）

2）原来的Icon and Image Design章节(主要内容为系统中不同情境下的icon设计定义）**改名为Graphics章节并且优先级上浮**

3）原来的iOS Technologies章节（系统中的新技术）**改名为Technologies章节且优先级下移**

4）原来**UI Design Basics**章节中的**动画/品牌/色彩/布局/字体**的内容专门提取出来生成新的**Visual Design**章节

![construction](https://isux.tencent.com/wp-content/uploads/2016/09/051354-79702.png)

图3 iOS HIG版本对比

5）原来的UI Elements一级目录被取消，其中的二级目录全部成为了一级目录

![construction2](https://isux.tencent.com/wp-content/uploads/2016/09/051353-23604.png)

图4 iOS HIG版本对比

6）增加了新的Resources章节，提供了PSD Templates、San Francisco Fonts和Xcode Projects的下载！这是让我觉得最有诚意的部分了！你什么时候见过Apple爸爸这么贴心了！

![resource](https://isux.tencent.com/wp-content/uploads/2016/09/051403-27164-590x479.png)

图5 增加的Resources章节

Apple的设计师对内部的细节内容也进行了翻新和扩建，在这里就不赘述了，但是确实值得大家细细去研究一番的，传送门在此：[iOS 10 Human Interface Guidelines](https://developer.apple.com/ios/human-interface-guidelines/)

我个人的感觉是，以前的HIG像是写给非设计人士/个人开发者的，使当年的他们在缺乏专业设计师的条件下也能保证产品的基础体验；现在的HIG更像是写给专业设计师的，说明了移动互联网整个行业已经成熟，职业分工越来越细，职业化程度越来越高，而用户和行业对设计的要求、设计对于产品的重要性也达到了一个新的高度。

而重视设计的Apple变的更加关注设计，试图像当年iOS 7一样，在设计和体验上带一波新的节奏。

P.S.  在这个方向上走在前列的是早在14年就发布了[Material Design](https://material.google.com/)的Google。

## **趋势：大而简，简而精**

在**HIG最最最重要的设计原则**的部分，仍然是万年不变的Deference（顺从）/Clarity（清晰）/Depth（深度）。

但是不知道大家有没有注意，其中有了一个非常细微的变化，就是**万年老二的Clarity（清晰）**原则，这次成了老大。具体原因也只有Apple的设计师知道了（貌似是来自于用户吐槽），但是就结果来说，**「清晰」**这一设计准则应当会是以后的设计趋势和重点

另外，对于设计原则的解释的内容也增多了，不要以为Apple突然抽风从冰山美人变成了话痨，增多的内容恰恰告诉了我们Apple重视的究竟是什么。

![differences](https://isux.tencent.com/wp-content/uploads/2016/09/054616-74095-630x358.png)

图6 新老设计三原则对比

在Clarity（清晰）原则中，增加了一段解释：留白、色彩、字体、图形和界面元素要强调重要内容并且对交互进行指引。

我们抽取一下其中的关键字，**内容、留白、色彩、字体、界面元素**，从描述来看，界面的**内容**将成为Apple关注的重点，其他关键字都是为内容的传达而服务的。但是，具体到底是怎么实施的呢？

实际上在WWDC 2016大会上展示的Apple Music已经告诉了我们答案：

![music1](https://isux.tencent.com/wp-content/uploads/2016/09/084621-4912-630x566.png)

图7 Apple Music改版

### 答案就是：加大字号！加粗字体！加多留白！减少页面的视觉层级！

另外还有......**加大控件！！！**在锁屏播放界面中，播放和音量的控件都被明显放大了，并且控件之间的间距也被加大了，大大降低了被误触的概率。

![music](https://isux.tencent.com/wp-content/uploads/2016/09/082222-67396-630x530.png)

图8 锁屏播放改版

以及**给重要控件赋予色彩**。新的控制中心的按钮都有了不同的颜色，从而让他们具有更明显的区分度以及视觉注意度，同样的，按钮也被加大了不少，Night Shift、AirPlay和AirDrop更是被独立了出来。

![control center](https://isux.tencent.com/wp-content/uploads/2016/09/052018-36992-590x409.png)

图9 Control Center改版

这样的优化出现在更多的界面中，再以新版的地图为例：

首先是**控件位置**的变化，原来的“开始”从底部移动到了规划路线的右侧，变的更加明显并且与路线本身产生更强的关联性；集中在顶部的操作也全部被移动到了底部，在大屏手机下的用户操作变的更加便捷，手指不用上下来回移动也能完成所有的操作了。

然后是**控件形式**的变化，原来的“开始”由纯文字Label变成了一个绿色的按钮，对用户产生了更强的视觉指引，还有个细节就是文案也由原来的**「Start（开始）」** 变成了 **「Go（出发）」**

![map](https://isux.tencent.com/wp-content/uploads/2016/09/082447-7825-630x530.png)

图10 Apple Map改版

这些改进具有一些**共同点**：

_1.   通过对**字体大小和粗细**的调整以及更多的留白来帮助用户理解界面的层级架构，取代了之前使用平面元素的分割和分层来构建界面架构的方式，从而让界面变的更加扁平，内容更加突出。另外，让具有一定程度视觉障碍的用户（色盲/色弱/老年人）也能够无障碍的使用。_

_**2.  放大按钮的尺寸、改变按钮的布局、赋予按钮不同的色彩**来提高用户对可操作内容的认知，降低点击操作的难度，使界面与用户的交互行为变的更友好。引用Apple在它的Accessibility Guideline（无障碍指南）中的描述就是「You view what you can do」 和「We make it easy to push all the right buttons」_

当然，这些变化解决了一些问题，但是带来了一些新的问题，比如在Apple Music中，内容展示效率的下降，原来能够展示6张专辑的界面，现在只能放下3张。不过目前发布的仍然是Beta版，不知道在正式版中是否会Fix这些问题。

### 但是，「The biggest iOS release ever」，iOS 10名至实归

### 比Apple Music做的更早更彻底的Airbnb

似乎不光是Apple一家在试图进行这样的改进，这种趋势已经开始蔓延。比如Airbnb在今年4月份上线的新设计，几乎完全舍弃了原来以图片衬底为主的设计，换成了大面积的留白和加粗加大的文字，底tab的高度也加高了不少，当然，按钮也加大了一圈。

全新的设计去掉了任何可能会给用户带来视觉干扰的东西，变的极度的纯粹。

![airbnb](https://isux.tencent.com/wp-content/uploads/2016/09/062237-47228-630x537.png)

图11 Airbnb改版

本人的好友[JJ-Ying](http://iconmoon.com/blog2/)也在前段时间的博文[「后扁平化时代」的 i18n 和 L10n](http://iconmoon.com/blog2/i18n-l10n-in-modern-ui-design/)中详细的分析了Airbnb的这次改版，引用文章内一个有趣的描述Airbnb的新设计是「比交互稿还交互稿」，不过他在文中更多关注的问题是：在这样的趋势下，**字体设计与产品品牌的关系**以及在进行**本地化与国际化设计时设计师所遇到的挑战，**感兴趣的同学可以点上面的链接阅读。

## 

### 另外一个搭上这班车的公司就是Instagram

几乎是紧接着Airbnb的步伐Instagram就发布了他们的新LOGO和新设计。对于褒贬不一的新LOGO我们暂且放在一边，主要还是看看UI的变化：

Ins去掉了头栏和底栏的颜色，通过加粗文字的方式来区分内容结构，取代了之前通过给文字添加颜色的方式（如：用户昵称、获赞数）。

![instagram](https://isux.tencent.com/wp-content/uploads/2016/09/060308-30431-590x497.png)

图12 Instagram改版

Ins的设计总监Ian[在Medium上对于这次改版的说明](https://medium.com/@ianspalter/designing-a-new-look-for-instagram-inspired-by-the-community-84530eb355e3#.5p31zylzz)是：“我们的新icon已经足够colorful了（确实非常colorful……），所以我们更希望App内的颜色是来自于用户上传的照片和视频而不是App本身，然后我们就把影响用户内容展现的干扰给干掉了。”

## 结语

总结成一句话来形容这股趋势就是**「大而简，简而精」**。

在这股趋势下，未来的设计将更注重产品的**内容和操作体验，**降低其他因素对用户使用上的干扰，这对设计师来说，是不小的挑战，因为越简单的东西越难设计，特别是如何在界面设计中去把握**「大」**和**「简」**的程度以及如何通过**更有限的手段和空间**来传达更多的信息和指引用户来达到**「精」**的目标，这是我们在未来需要不断考虑、探索和解决的问题。