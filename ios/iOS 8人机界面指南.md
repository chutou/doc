# iOS 8人机界面指南

## 1. UI设计基础

### 1.1 为iOS而设计（Designing for iOS）

iOS 的革新关键词如下：

* **遵从**：UI能够更好地帮助用户理解内容并与之互动，但却不会分散用户对内容本身的注意力。
* **清晰**：各种大小的文字应该易读，图标应该醒目，去除多余的修饰，突出重点，很好地突显了设计理念。
* **深度**：视觉的层次和生动的交互动作会赋予UI新的活力，不但帮助用户更好理解新UI的操作并让用户在使用过程中感到惊喜。

[![weather_app_7_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922141348954.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922141348954.png)

无论你是重新设计一个现有的应用或是重新开发一个，请尝试下列方法：

* 首先，去除了UI元素让应用的核心功能呈现得更加直接并强调其相关性。
* 其次，直接使用iOS的系统主题让其成为应用的UI，这样能给用户统一的视觉感受。
* 最后，保证你设计的UI可以适应各种设备和不同操作模式，这样用户可以在不同场景下舒适地享用你的应用。

在整个设计过程中，时刻准备着推翻先例，假设问题，并以重点内容和功能（为目标）来驱动每个细节设计。

### 1.1.1 以内容为核心（Defer to Content）

虽然明快美观的UI和流畅的动态效果是iOS体验的亮点，但内容始终是iOS的核心。

这里有一些方法，以确保你的设计能够提升你的应用功能体验并关注内容本身。

**充分利用整个屏幕。**天气应用是最好的例子：漂亮的天气图片充满全屏，呈现用户所在地当前天气情况这最重要的信息，同时也留出空间呈现了每个时段的气温数据。

![weather_focus_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922141637148.png)

**尽量减少视觉修饰和拟物化设计的使用。**UI面板、渐变和阴影有时会让UI元素显得很厚重，致使抢了内容的风头。应该以内容为核心，让UI成为内容的支撑。

![restrain_visual_indicators_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922141636135.png)

**尝试使用半透明底板。**半透明的控件——比如控制中心——关联了使用场景，帮助用户看到更多可用的内容，并可以起到短暂的提示作用。在iOS中，透明的控件只让它遮挡住的地方变得模糊——看上去像蒙着一层米纸一样——它并没有遮挡屏幕剩余的部分。

![embrace_translucency_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922141633495.png)

### 1.1.2 保证清晰度（Provide Clarity）

保证清晰度是另一个方法，以确保你的应用中内容始终是核心。以下是几种方法，让最重要的内容和功能清晰，易于交互。

**使用大量留白。**留白让重要内容和功能显得更加醒目。此外，留白可以传达一种平静和安宁的视觉感受，它可以使一个应用看起来更加聚焦和高效。

[![use_white_space_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922141636668.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922141636668.png)

**让颜色简化UI****。**一个主题色——比如在记事本中使用的黄色——让重要区域更加醒目并巧妙地表示交互性。这同时也给了一个应用一个统一的视觉主题。内置应用使用家族化的系统颜色，无论在深色和浅色背景上看起来都干净，纯粹。

[![notes_color_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922141635546.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922141635546.png)

**通过使用系统字体确保易读性。**iOS的系统字体自动调整行间距和行的高度，使阅读时文本清晰易读，无论何种大小的字号都表现良好。无论你是使用系统或是自定义字体，务必使用动态型，这样你的应用可以在用户选择不同字号时做出应对。

[![mail_message_fonts_2x](https://isux.tencent.com/wp-content/uploads/2014/09/2014092214163585.png)](https://isux.tencent.com/wp-content/uploads/2014/09/2014092214163585.png)

**使用无边框的按钮。**默认情况下，所有bar上的按钮都是无边框的。在内容区域，无边框按钮以文案、颜色以及操作指引标题来表明按钮功能。当按钮被激活时，该按钮呈现高亮的浅色状态来作为操作响应。

[![contact_card_2x](https://isux.tencent.com/wp-content/uploads/2014/09/2014092214163313.png)](https://isux.tencent.com/wp-content/uploads/2014/09/2014092214163313.png)

### 1.1.3 用深度来体现层次（Use Depth to Communicate）

iOS经常在不同的层级上展现内容，用以表达分组和位置，并帮助用户了解在屏幕上的对象之间的关系。

通过使用一个在主屏幕上方的半透明背景浮层来区分文件夹和其余部分的内容。

[![folder_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922141633945.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922141633945.png)

备忘录以不同的层级展示，如插图所示。用户在使用备忘录里的某个条目时，其他的条目被收起在屏幕下方（译者按：其实这个视觉提示使用起来很隐晦）。

[![layered-reminders_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922141634411.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922141634411.png)

日历有较深的层级，当他们在翻阅年、月、日的时候，以及增强的交互动画给用户一种层级纵深感（循序切换的层次，从年到月到日）。在滚动年份视图时，用户可以即时看到今天的日期以及其他日历任务。当用户处于月份视图时，点击年份视图按钮，月份会缩小至年份视图中的所处位置。

![cal_year_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922141632512.png)

今天的日期依然处于高亮状态，年份出现在返回按钮处，这样用户可以清楚地知道他们在哪儿，他们从哪里进来并且知道如何返回。

![cal_month_2x](https://isux.tencent.com/wp-content/uploads/2014/09/2014092214163266.png)

类似的过渡动画出现在用户选择一个日期时：月份视图从所选位置分开，将当前的周日期推向屏幕顶端并翻转出以小时为单位的当天时间视图。这些动画加强了日历上年月日之间的关系的感知度。

[![cal_day_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922141631619.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922141631619.png)

### 1.2 iOS应用解析（iOS App Anatomy）

几乎所有的iOS 应用都应用了UIKit framework中定义的组件。了解这些组件的名字，作用和构成能够帮助你设计应用过程中做出更好的决定。

[![01](https://isux.tencent.com/wp-content/uploads/2014/09/20140922142148415-590x398.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922142148415.png)

UIKit提供的UI组件大致分成以下4种大类：

**Bars****：**包含了导航信息，告诉用户他们所在的位置并包含了一些能帮助用户浏览或启动某些操作的控制按钮。

**内容视图：**包含了应用的主体内容以及某些操作行为，比如滚动、插入、删除、排序等等。

**控制按钮：**展示信息或者控制动作。

**临时视图：**短时间出现，给用户重要信息或者额外的选择或者其他功能。

除了定义UI组件，UIKit也定义对象实现的功能，例如手势识别、绘图、辅助功能和打印支持。

从编程的角度来说，UI组件被认为是不同类别的视图，因为他们从UIView得到继承。视图能绘制屏幕内容并且知道用户何时触摸了屏幕。视图的所有类型有：控件（比如按钮和滑块），内容视图（比如集合视图和表格视图），以及临时视图（如警告提示和动作菜单）。

要在应用中管理一组或者一系列的视图，通常需要使用一个视图控制器，它能协调视图的显示内容，实现与用户交互的功能并能在不同屏幕内容之间切换。比如，“设置”使用了一个导航控制器来展示其视图层级。

下面是一个例子，关于视图与视图控制器如何结合并呈现iOS 应用的UI。

[![02](https://isux.tencent.com/wp-content/uploads/2014/09/20140922142257717-590x556.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922142257717.png)

虽然开发者认为真正起到作用的是视图和视图控制器，但一般用户感知到的iOS应用是不同屏幕内容的集合。从这个角度来看，在应用里，屏幕内容一般对应于一个独特的视觉状态或者模式。

**注：**一个iOS应用程序包含一个窗口。但是，不同于计算机程序中的窗口，iOS窗口没有可见的部分并且不能在屏幕上被移动到另一个位置。很多iOS应用程序只有一个窗口；可以支持外部显示设备器的应用程序可以有不止一个窗口。

在_iOS Human Interface Guidelines_中，_screen_这个词和大部分用户理解的一样。作为一个开发者，你也许需要读一下其他与[UIscreen](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIScreen_Class/index.html#//apple_ref/occ/cl/UIScreen)相关的章节，这样你可以更好的了解如何关联外部屏幕。

### 1.3 适应性和布局（Adaptivity and Layout）

### 1.3.1 为自适应而开发（Build In Adaptivity）

人们通常想随心所欲地使用自己喜欢的应用程序。在iOS 8及未来的版本中，你可以使用不同分辨率和自动布局来帮助你定义屏幕布局视图，视图控制器以及需要随显示环境改变的视图（显示环境display environment的概念指的是设备的整个屏幕或者其中一部分，比如一个跳出菜单区域或一个分视图控制器的主视图部分）。

iOS定义了两个尺寸类别（size class），常规的（regular）和压缩的（compact）。常规尺寸有着较易拓展的空间，而压缩尺寸约束了空间的使用。想要定义一种显示环境，你需要定义横纵尺寸类型。如你所想，iOS设备可以有横屏竖屏两种不同的使用模式。

iOS能随着显示环境和尺寸类别变化而自动生成不同布局。举个例子，当垂直尺寸从压缩变为常规时，导航栏和工具栏会自动变高。

当你靠尺寸类别来驱动布局变化时，你的应用在任何显示环境时都能显示得很好。关于如何在Interface Builder中更好的使用尺寸类别，你可以查阅_[Size Classes Design Help](https://developer.apple.com/library/ios/recipes/xcode_help-IB_adaptive_sizes/_index.html#//apple_ref/doc/uid/TP40014436)__。_

**注：**在一种尺寸类别中，持续使用Auto Layout进行小的布局调整，比如拉伸或压缩内容。

下面的实例可以帮助你理解尺寸类型是如何适配不同设备的显示环境。例如：iPad在长宽和横屏竖屏时都使用常规尺寸类型。换句话说，iPad显示环境一直处于垂直和水平的常规状态。

[![03](https://isux.tencent.com/wp-content/uploads/2014/09/20140922142628708-590x287.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922142628708.png)

iPhone的显示环境可根据不同的设备和不同的握持方向而改变。

竖屏时，iPhone6 Plus使用的是常规高度和压缩宽度类型。

[![04](https://isux.tencent.com/wp-content/uploads/2014/09/20140922142509495.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922142509495.png)

横屏时，iPhone6 Plus使用的是压缩高度和常规宽度类型。

[![05](https://isux.tencent.com/wp-content/uploads/2014/09/20140922142509932.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922142509932.png)

其他iPhone型号，包括iPhone6使用相同的尺寸类型设置。

竖屏时，iPhone 6，iPhone 5 和iPhone 4S使用的是压缩宽度和常规高度。

[![06](https://isux.tencent.com/wp-content/uploads/2014/09/20140922142510346.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922142510346.png)

横屏时，这些设备在宽高上使用的都是压缩类。

[![07](https://isux.tencent.com/wp-content/uploads/2014/09/20140922142510765.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922142510765.png)

### 1.3.2 在不同环境提供良好体验（Provide a Great Experience in Each Environment）

当你使用自适应来开发UI时，你可以保证UI跟随显示环境变化而适当地响应。遵照这些指南，你可以给用户良好的设备响应体验。

**在所有环境下都保持对主体内容的专注。**这是最高优先级。人们使用应用时，与感兴趣的内容发生互动。当使用环境变化的同时，改变专注点会让用户感觉到迷失方向，丧失了对应用的控制。

**避免布局上不必要的变化。**在所有环境中类似的使用体验让人们在旋转设备或在不同设备上运行你的应用时维持使用模式。例如，如果你使用一个网格在水平的常规模式下显示图像，你无需在一个列表中展示与压缩模式下相同信息，虽然你可能调整了网格的尺寸。

**如果你的应用****只在一个方向上运行，那么请直接一点。**人们希望在各种握持方式下都可以使用你的应用，能满足这个期待是最好的。但是，如果你的应用只在一个方向下运行，那么以下几点请务必注意：

* **避免提示人们旋转设备的提示UI****出现。**让应用清晰地运行在支持的方向下，让用户明白应该旋转设备，而不是添加不必要的引导性混乱。
* **支持同一个方向上的变化。**例如，如果一个应用只能垂直运行，用户无论用左手或是右手握持时都能触及到home键。如果用户在使用应用时180度旋转设备，那最好应用内容也能及时响应并旋转180度。

**如果你的应用****将设备方向翻转视为用户输入（的一种指令），那么就按照程序设定的方式来响应设备翻转。**举个例子，一个游戏让用户利用设备翻转来移动游戏中的部件，那么这个游戏应用本身（的UI）不能对翻转屏幕产生响应。在这种情况下，你必须关联两个需要变化的方向，并且允许人们在这两个方向切换直到他们开始（了解并执行）应用的主体任务。一旦人们开始执行主要任务，那就开始按程序设定的那样来响应设备的动作吧。

### 1.3.3 使用布局来沟通（Use Layout to Communicate）

**布局包含的不仅仅是一个应用****屏幕上的UI****元素外观。**你的布局，应该告诉用户什么是最重要的，他们的选择是什么，以及事物是如何关联起来的。

**提升重要内容或功能，让用户容易集中注意在主要任务上。**有几个比较好的办法是在屏幕上半部分放置主要内容，以从左到右的习惯，从靠近左侧的屏幕开始。

[![08](https://isux.tencent.com/wp-content/uploads/2014/09/20140922142511204-590x568.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922142511204.png)

**使用视觉化的重量和平衡向用户展示相关的屏显重要元素。**大型控件吸引眼球，而比小的控件更容易在出现时被注意到。而且大型控件也更容易被用户点击，这让它们在应用中更加有用——就像电话和时钟（上面的按钮）——用户经常在容易分心的环境中能（正常）使用它们。

[![phone_hangup_button_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922142512475.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922142512475.png)

**使用对齐来让阅读更舒缓，让分组和层次之间更有秩序。**对齐让应用看起来整洁而有序，也让用户在专注于屏幕时更有空间，从而专注于重要信息。不同信息组的缩进与对齐让它们之间的关联更清晰，也让用户更容易找到某个控件。

**确保用户能明白处于默认尺寸的首要内容的含义。**例如，用户无需水平滚动就能看到重要的文本，或不用放大就可以看到主体图像。

**准备好改变字体大小。**用户期望大多数应用能有设置字号大小的功能。为了适应一些文本大小的变化，你也许需要调整布局；想要得到更多文本显示相关的信息，你可以查阅章节[Text Should Always Be Legible](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/ColorImagesText.html#//apple_ref/doc/uid/TP40006556-CH58-SW3).

**尽量避免UI****上不一致的表现。**在一般情况下，有着相似功能的控件看起来也应该类似。用户常常认为他们看到的不同总有原因，而且他们倾向于花时间去尝试（译者按：因此为了避免用户做无用的尝试所以建议类似功能外观一样）。

**给每个互动的元素充足的空间，从而让用户容易操作这些内容和控件。**常用的点按类控件的大小是44 x 44点（points）。

[![interact_with_content_r_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922162720481-590x442.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922162720481.png)

### 1.4 起始与停止（Starting and Stopping）

### 1.4.1 即时启动（Start Instantly）

有种说法是用户往往不会花超过一两分钟去审视一个新应用，当你将应用从打开到启动这段时间压缩得很短，并且同时在载入过程中呈现一些对用户有帮助的内容，你就会激发用户的兴趣并给所有用户一个惊喜。

重要：不要在安装过程结束后告诉用户需要重启设备。重启需要时间并且会让人觉得你的应用看上去不可靠而且很难使用。

如果你的应用有内存使用问题，或者不重启就无法流畅运行，你必须声明这些问题。关于如何开发一款性能良好的应用，请查阅[iOS应用编程指南](https://developer.apple.com/library/ios/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40007072)。

**尽可能避免使用闪屏或者其他启动体验。**用户能够在启动后立即开始使用应用是最好不过的。

[![00](https://isux.tencent.com/wp-content/uploads/2014/09/20140922163431595-590x393.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922163431595.png)

**避免让用户做过多设置。**而应该如此：

* **聚焦在满足****80%****的用户需求上。**这样主体用户群就无需设置各种选项，因为你的应用已经默认处于他们想要的状态。如果有些功能有少部分用户想要，换句话说，大部分人不需要的话，就别管它了。
* **尽可能用其他方式获取更多（用户）信息。**如果你能得到用户在内置应用或硬件设置中提供的信息，直接从系统中获取它们，而不需要再次让用户输入。
* **如果你必须获取设置信息，在你的应用中直接向用户询问，然后尽快保存这些设定**（译者注：这段讲的是权限许可，如能否访问照片或者日历或地理位置信息等等）。这样用户就无需强制跳出应用进入系统设置页面了。如果用户需要更改设置，他们可以在任何时候进入应用的设置选项进行修改。

**尽可能让用户晚一些再登录。**最理想的状态是，用户在无需登录的情况下就能尽量多地浏览内容并使用部分功能。例如，App Store应用会在用户浏览商品并确定进行购买时，才要求用户进行登录。对于必须登录才能进行后续浏览和操作的应用，用户往往会直接放弃。

如果你的应用必须先登录后使用，那么你应该在登录页面有一些简短的文字，来描述为什么必须先登录，以及这样做会给用户带来什么好处。

**谨慎使用新手引导**（介绍应用的功能和如何进行操作）。在考虑新手引导之前，你应该完善你的应用，尽可能使应用的功能直观和易于寻找。有句话说得好，_好的应用不需要新手引导_。如果你确实觉得需要新手引导，那么请参考如下的建议，设计一个简洁、有针对性并且不妨碍用户的新手引导。

* **只提供开始使用应用所必需的信息。**好的新手引导应该告诉用户接下来第一步应该做什么，或者简短地演示大部分用户感兴趣的一些功能。在能够浏览你的应用之前，如果用户遇到太多的信息，让用户记住这些不是当前所必须的内容，他们很可能会觉得你的应用很难用。如果在某些特定场景下确实需要一些引导，那么也应该在用户进入这个场景之后再进行。

* **使用交互动画来吸引用户，并让用户通过实际上手来学习如何使用。**对于文字内容的增加应该谨慎，且仅当增加文字对于提升体验有益时才这么做。不要指望用户会阅读大段的文字。例如，可以使用动画而不是文字来描述如何执行一个简单的任务。在引导用户了解较为复杂的任务时，可以通过一些引导浮层来简要说明每一个步骤用户需要做什么。尽可能避免展示应用截图，因为截图是死的，用户可能会混淆截图和应用的实际界面。

* **能够简单地取消或者跳过新手引导。**有些用户看完新手引导之后就不想再看，有些甚至根本就不想看新手引导。请记住用户的选择，不要强迫用户每次打开你的应用都要再做一次选择。

**不要太早要求用户去给你的应用评分。**过早要求用户进行评分可能会适得其反。如果你想获得用户有价值的反馈和评论，在邀请用户评论之前，请给他们一点时间来使用你的应用，并对你的应用形成印象。例如，你可以等用户访问了一定数量的页面或完成了一定数量的任务之后，再邀请他们进行评价。

**一般建议按照屏幕默认的定向方式启动你的应用。**尽管如此，如果你的应用只有一种屏幕方向，那么就始终以这个方向启动，让用户在他们自己需要时再改变设备方向。例如，一个游戏或者媒体观看应用只在横屏模式下运行，那么就应该以横屏模式启动，即使设备当前处于竖屏模式。这样的话，如果用户在竖屏模式下打开应用，他们也知道应该把设备转成横屏来进行使用。

[![default_orientation_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922163601832-590x378.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922163601832.png)

**注：**最好让横屏应用支持两种模式的横屏，即home键处于左右两侧的状态。如果设备当前已经处于横向状态，那么就按照当前状态启动应用，除非你有充分的理由不这么做。其他情况时，可以考虑按home键处于右侧的方式启动应用。（想要了解更多关于支持不同设备方向的内容，请参阅Respond to Changes in Device Orientation.）

**准备一张与应用首页看上去一样的闪屏。**iOS会在启动应用时调用这张图，这样可以让用户觉得启动速度很快，降低对等待时间的感知度。具体如何制作闪屏，请查阅[Launch Images](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/LaunchImages.html#//apple_ref/doc/uid/TP40006556-CH32-SW1)。（译者注：Launch Images章节处在iOS Human Interface Guidelines的Icon and Image Design部分，翻译将在后续更新中放出，烦请各位耐心等候。）

**如果可能，不要让用户在初次启动应用时阅读免责声明或者确认用户协议。**你可以直接在App Store展示这些内容，使用户在下载前就有所了解；虽然这个办法能最大地减少麻烦，但也不是一直可行。如果在某些情况下你必须展示这些内容，要确保它们与UI保持统一并在产品功能与用户体验之间达成平衡。

**在应用重启后，需要恢复到用户退出使用时的状态，让他们可以从中断之处继续使用。**无需让用户记住是如何达到此种退出状态的。

### 1.4.2 时刻准备好停止（Always Be Prepared to Stop）

**iOS** **应用无需关闭或退出选项。**当用户切换应用，回到主屏幕或者将设备调至睡眠模式的时候，其实就是停止了当前应用的使用。

当用户切换应用时，iOS的多任务系统会将其放置到后台并将新应用的UI替换上来。在这种情况下，你必须做到以下几点：

* 随时并尽快保存用户信息，因为在后台的应用随时有可能被终止或退出。
* 当应用停止的时候保存当前状态，使用户可以在回到应用时能从中断之处继续使用。例如，在使用可滚动的数据列表时，退出后保存列表所在的位置。

有些应用可能需要一直在后台运行。例如，用户可能希望能在使用一个应用的同时还能一直听歌，接着又想用另外一个应用来检查代办项或者玩游戏。关于如何正确处理多任务，请查阅[Multitasking](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Multitasking.html#//apple_ref/doc/uid/TP40006556-CH38-SW1)。（译者注：Multitasking章节处在iOS Human Interface Guidelines的iOS Technologies部分，翻译将在后续更新中放出，烦请各位耐心等候。）

**不要强制让应用退出**。因为这样会让用户误以为是crash。如果有问题产生，需要告诉用户具体状况以及如何解决。以下有两个建议，取决于出现的问题有多严重而酌情使用：

**如果应用中所有的功能当前都不可用，那么应该显示一些内容来解释当前的情形，并建议用户如何进行后续操作。**这部分内容给予了用户以反馈，使用户相信你的应用现在没问题。同时这也可以稳定用户情绪，让他们决定是否要采取纠正措施，继续使用应用，还是切换到另一个应用。

[![all_features_unavailable_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922163801598.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922163801598.png)

**如果只有部分功能不可用，那么只要当用户使用这些功能时显示提示即可。**不然的话，用户就应该能正常使用应用的其他功能。如果你决定使用警告框来进行提示，请确保只在用户尝试使用不可用的功能时再显示。

[![one_feature_unavailable_2x](https://isux.tencent.com/wp-content/uploads/2014/09/2014092216380299.png)](https://isux.tencent.com/wp-content/uploads/2014/09/2014092216380299.png)

### 1.5 导航（Navigation）

除非导航设计的不合理，不然用户不应明显察觉到应用中的导航体验。放置导航到一个能够支撑你的应用结构和目的却又不过分引起用户注意的状态。

广义来说，有三种主要类型的导航，每种导航都有其适应的应用结构：

* 分层。
* 扁平。
* 内容或经验驱动。

在分层应用中，用户在每个层级中都要选择其中一项，直到目的层级。如果要切换到另一个层级，用户必须回退一些层级，或者直接回到初始层级进行再次选择。系统的设置和邮件应用在这方面是很好的示范，可以参考他们。

<!--[if lt IE 9]><script>document.createElement('video');</script><![endif]-->Video Player

<video class="wp-video-shortcode" id="video-16135-1" width="508" height="348" preload="metadata" src="https://isux.tencent.com/wp-content/uploads/2014/09/20140922163952373.m4v?_=1" style="width: 100%; height: 100%;">
    <source type="video/mp4" src="https://isux.tencent.com/wp-content/uploads/2014/09/20140922163952373.m4v?_=1">https://isux.tencent.com/wp-content/uploads/2014/09/20140922163952373.m4v
</video>

<button type="button" aria-controls="mep_0" title="Play" aria-label="Play"></button>

00:00

00:00

00:06

<button type="button" aria-controls="mep_0" title="Mute" aria-label="Mute"></button>[Use Up/Down Arrow keys to increase or decrease volume.](javascript:void(0);)

<button type="button" aria-controls="mep_0" title="Fullscreen" aria-label="Fullscreen"></button>

在扁平应用中，用户可以从一个主要分类直接切换到另一个，因为所有的主要分类都可以从主屏直接访问。音乐和App Store是两个使用扁平结构的好例子。

Video Player

<video class="wp-video-shortcode" id="video-16135-2" width="580" height="360" preload="metadata" src="https://isux.tencent.com/wp-content/uploads/2014/09/20140922164218524.m4v?_=2" style="width: 100%; height: 100%;">
    <source type="video/mp4" src="https://isux.tencent.com/wp-content/uploads/2014/09/20140922164218524.m4v?_=2">https://isux.tencent.com/wp-content/uploads/2014/09/20140922164218524.m4v
</video>

<button type="button" aria-controls="mep_1" title="Play" aria-label="Play"></button>

00:00

00:00

00:08

<button type="button" aria-controls="mep_1" title="Mute" aria-label="Mute"></button>[Use Up/Down Arrow keys to increase or decrease volume.](javascript:void(0);)

<button type="button" aria-controls="mep_1" title="Fullscreen" aria-label="Fullscreen"></button>

在内容驱动或经验驱动信息结构的应用中，导航的内容也会根据内容或经验来进行设计。例如，在阅读一本电子书时，用户会一页接一页地进行阅读，也会在目录中选择想要阅读的页码跳转后开始阅读。同样的，在游戏应用中，导航的作用也非常重要。

Video Player

<video class="wp-video-shortcode" id="video-16135-3" width="680" height="258" preload="metadata" src="https://isux.tencent.com/wp-content/uploads/2014/09/20140922164218977.m4v?_=3" style="width: 100%; height: 100%;">
    <source type="video/mp4" src="https://isux.tencent.com/wp-content/uploads/2014/09/20140922164218977.m4v?_=3">https://isux.tencent.com/wp-content/uploads/2014/09/20140922164218977.m4v
</video>

<button type="button" aria-controls="mep_2" title="Play" aria-label="Play"></button>

00:00

00:00

00:10

<button type="button" aria-controls="mep_2" title="Mute" aria-label="Mute"></button>[Use Up/Down Arrow keys to increase or decrease volume.](javascript:void(0);)

<button type="button" aria-controls="mep_2" title="Fullscreen" aria-label="Fullscreen"></button>

在某些情况下，在一个应用中结合多种导航类型会有很好的效果。例如，对于扁平信息结构中某一分类下的内容，用分层导航的方式来显示可能会更好。

**用户应该时刻清楚自己当前在应用中所处的位置，以及如何前往他们所想到的页面。**

无论导航类型是否适合你的应用结构，最重要的是用户访问内容的路径应该是合理、可预期和易于寻找的。

UIKit定义了一些标准的UI元素，这些元素即可以构建分层或扁平的导航，也可以实现以内容为中心的导航，例如电子书或者媒体观看类应用。游戏或者其他经验驱动的应用通常需要一些自定义的元素和行为。

**使用导航栏（Navigation Bar****）帮助用户轻松访问分层内容。**导航栏的标题可以显示用户当前所处的层级，而后退按钮可以回到上一层级。查看[Navigation Bar](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Bars.html#//apple_ref/doc/uid/TP40006556-CH32-SW3)了解更多。

**使用标签栏（Tab Bar****）显示同类型的内容或功能。**标签栏很适合于扁平信息结构，可以让用户在分类之间随意切换，而不用在意当前所处的位置。查看[Tab Bar](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Bars.html#//apple_ref/doc/uid/TP40006556-CH32-SW52)了解更多。

**在应用中，如果每屏显示的都是同类项或同类页，可以使用页面控件（Page Control****）。**页面控件的优点是可以直观地告诉用户共有多少个项目或页面，以及当前所处的位置。查看[Page Control](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Controls.html#//apple_ref/doc/uid/TP40006556-CH35-SW6)了解更多。

**一般来说，最好能给用户到达每一屏的路径。**如果用户需要，就应该考虑使用临时视图，例如模态视图、动作菜单或警告框。查看[Modal View](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Alerts.html#//apple_ref/doc/uid/TP40006556-CH34-SW3)、[Action Sheet](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Alerts.html#//apple_ref/doc/uid/TP40006556-CH34-SW36)和[Alert](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Alerts.html#//apple_ref/doc/uid/TP40006556-CH34-SW2)了解更多。

（译者注：上文提到的章节均处在iOS Human Interface Guidelines的第4章，翻译将在后续更新中放出，烦请各位耐心等候。若有需要，亦可先参考先前已翻译的iOS7 UI Elements章节：[上](https://isux.tencent.com/ios-human-interface-guidelines-ui-design-ios7-ui-1.html)，[下](https://isux.tencent.com/ios-human-interface-guidelines-ui-design-ios7-ui-2.html)。）

UIKit同时还提供了以下相关控件：

* 分段控件（Segmented Control）。分段控件让用户在一屏内就可以查看到不同分类的内容，而不需要切换到其他屏幕。
* 工具栏（Toolbar）。尽管工具栏看起来和导航栏或标签栏相似，但是工具栏不具导航作用。相反，工具栏为用户提供了可以控制当前屏幕内容的控件。

### 1.6 模态情境（Modal Contexts）

模态是一个承载某些连贯操作或内容的优缺点并存的模式。它可以给用户提供一种不脱离主任务的方式去完成一个任务或者获得信息，但是也会临时性地阻止用户对应用的其他部分进行交互操作。

[![11](https://isux.tencent.com/wp-content/uploads/2014/09/20140922165024665-590x380.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922165024665.png)

理想情况下，用户可以与iOS 应用进行一种非线性的交互，所以，尽可能减少应用中的模态体验是最好的。通常情况，在以下情形下可以考虑使用模态情境：

* 必须引起用户关注的时候。
*  一个独立的任务需要完成或者很明确需要被放弃，为了避免在模棱两可的状态下遗漏用户信息的时候。

**保持模态任务的简单，简短和高度聚焦。**你肯定不希望用户使用模态视图时像使用应用中的一个mini应用一样。如果子任务过于复杂，用户会在进入模态情境时忽略主要任务。在设计一个涉及视觉层次的模态任务时特别要考虑这一点，因为用户有可能迷失并且忘记如何回到之前的操作中去。如果一个模态任务必须包含不同视图的子任务，确保给用户一个独立、清晰的导航路径，并避免迂回。

**始终提供明显、安全的途径退出模态任务。**确保用户在退出模态视图时可以预期操作的结果。

**一个任务需要多层级的模态视图时，确保用户理解点击完成按钮的结果。**点击一个低层级视图上的完成按钮是完成这个视图中任务的一部分，还是整个任务？因为存在这种困惑的可能性，所以要尽可能避免在下级视图中添加完成按钮。

**保证提醒对话框的内容都是重要且可操作的。**提醒对话框会打断用户的体验并且要点击才会消失，所以要让用户感到提醒信息是有用的，打断是有价值的。

**尊重用户关于接收通知的选择。**用户会设置接收应用通知的形式，必须尊重要用户的喜好设置，否则可能触怒用户，导致其关闭所有的推送通知。

### 1.7 交互性和反馈（Interactivity and Feedback）

### 1.7.1 用户知道标准手势（Users Know the Standard Gestures）

用户使用点击、拖拽、捏合等手势与iOS设备进行交互。使用手势拉近了用户和设备之间的距离，并且增强了直接操纵感。用户通常期待手势在不同应用之间都是通用的。

[![gesture](https://isux.tencent.com/wp-content/uploads/2014/09/20140922172649583.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922172649583.png)

除了用户熟悉的标准手势，iOS还定义了一些系统范围内的操作，例如呼出控制中心或消息中心。在任意应用下都可以使用这些操作。

**不要给标准手势赋予不同的行为。**除非你的应用是游戏，否则重新定义标准手势会使用户迷惑，且增加使用难度。

**不要创建和标准手势功能相似的手势操作。**用户已经习惯了标准手势的行为，没有必要让用户学习达到同样效果的不同操作。

**可以用复杂手势作为完成某任务的快捷方式，但不能是唯一触达方式。**最好给用户提供一些简单、直接的方式完成某操作，即使这种方法需要额外的动作。简单的手势能让用户集中于当前的体验和内容，而不是交互操作本身。

**除非是游戏，否则避免定义新的手势。**在游戏或其他沉浸式的应用中，操作手势也是有趣体验的一部分。但是在普通应用中，帮助用户达成目标要比操作本身重要的多，所以最好使用标准手势，尽量避免让用户去发掘和记忆新的操作。

**在特定的环境中，可以考虑使用多指操作。**虽然复杂的操作并不一定适用于所有应用，但对用户会花大量时间使用的应用来说可以丰富体验，例如游戏或创建内容环境。但因为非标准手势可发现性差，要尽量少用，并且不要让这类手势成为完成任务的唯一方式。

### 1.7.2 可交互元素吸引用户点击（Interactive Elements Invite Touch）

为了暗示交互性，设计时会使用很多线索，包括颜色、位置、上下文、表意明确的图标和标签等。并不需要过于修饰元素来向用户展示可交互性。

一个关键的颜色可以给用户提供很强的视觉指引，尤其是没有冗余的其它颜色时。为了有对比，使用蓝色标记可交互的元素，并且使用统一的、易识别的视觉风格。

[![01](https://isux.tencent.com/wp-content/uploads/2014/09/20140922172948543.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922172948543.png)

返回按钮使用多个线索指明其可交互性并传达其功能：它出现在导航中，显示了一个指向后方的图标，使用了关键色，显示了上一级页面的标题。

[![02](https://isux.tencent.com/wp-content/uploads/2014/09/20140922173015940.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922173015940.png)

一个图标或者标题提供了清晰的名称指引用户点击它。例如，地图中的标题“立交桥路线”，“定位到这里”，清晰地说明了用户可做的操作。结合关键色，就可以省去按钮边界或其他多余的修饰。

[![03](https://isux.tencent.com/wp-content/uploads/2014/09/20140922173046882.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922173046882.png)

**在内容区域，有必要给按钮添加边界或背景。**操作条中的按钮、动作表单和提醒对话框可以不需要边界，因为用户知道在这种区域中大多数选项是可交互的。但是在内容区域，按钮有必要使用边界或背景将按钮从其他内容中区分出来。例如，系统自带的音乐、时钟、照片和App Store应用会在一些特别的场景中使用这种按钮。

照片应用中给分享按钮增加了边框，与其他解释性文本进行了区分。

[![04](https://isux.tencent.com/wp-content/uploads/2014/09/20140922173119490.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922173119490.png)

时钟应用在秒表和计时页面中给按钮增加背景来强调开始和暂停按钮，并且使按钮在周围的内容中更容易点击。

[![05](https://isux.tencent.com/wp-content/uploads/2014/09/20140922173143910.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922173143910.png)

App Store应用中使用有边界的按钮，将按钮和整个内容条区分开来，点击整条内容查看详细信息，点击按钮进行下载安装。

[![06](https://isux.tencent.com/wp-content/uploads/2014/09/20140922173216529.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922173216529.png)

### 1.7.3 反馈有助于理解（Feedback Aids Understanding）

反馈会帮助用户了解应用当前在做什么，发现接下来可以做什么以及理解动作产生的结果。UIKit提供了很多反馈。

**尽可能将状态或其他的反馈信息整合到UI中。**用户不进行操作或不跳出当前内容就能获得需要的信息是最好的。例如，邮箱应用将当前邮箱的状态显示工具条上，这样就不会影响当前内容。

[![07](https://isux.tencent.com/wp-content/uploads/2014/09/20140922173243598.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922173243598.png)

**避免显示不必要的警告框。**警告框是一种很强的反馈机制，只有在传递非常重要也是理论上可行的信息时才需要使用它。如果用户常看到很多不是重要信息的警告框，他们很快就会忽略所有对话框提醒。

### 1.7.4 输入信息的方式要简单（Inputting Information Should Be Easy）

不管用户是点击控件还是使用键盘，输入信息都会花费时间和精力。如果发挥有用的效用前就让用户输入大量信息会减弱用户继续使用的欲望。

**让用户更容易地进行选择。**例如，使用选择器或者表格代替纯文本，避免要求用户打字来提高选择效率，降低选择成本。

[![10](https://isux.tencent.com/wp-content/uploads/2014/09/20140922173843170-590x393.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922173843170.png)

**适宜地从iOS中获取信息。**设备上存储了大量的用户信息。可以的话，不要让用户提供你可以轻易找到的信息，例如联系人或日历信息。

**提供有用的反馈来平衡用户的输入。**付出和回报的概念可以帮助用户感到进程在被推进。

### 1.8 动画（Animation）

iOS的用户界面中遍布着细微、精美的动画，它们使得应用的体验更具吸引力、更具动态性。适当的动画可以：

* 传达状态和提供反馈
* 增强直接操作的感觉
* 帮助人们可视化他们的操作结果

Video Player

<video class="wp-video-shortcode" id="video-16135-4" width="640" height="260" preload="metadata" src="https://isux.tencent.com/wp-content/uploads/2014/09/20140922174109766.m4v?_=4" style="width: 100%; height: 100%;">
    <source type="video/mp4" src="https://isux.tencent.com/wp-content/uploads/2014/09/20140922174109766.m4v?_=4">https://isux.tencent.com/wp-content/uploads/2014/09/20140922174109766.m4v
</video>

<button type="button" aria-controls="mep_3" title="Play" aria-label="Play"></button>

00:00

00:00

00:06

<button type="button" aria-controls="mep_3" title="Mute" aria-label="Mute"></button>[Use Up/Down Arrow keys to increase or decrease volume.](javascript:void(0);)

<button type="button" aria-controls="mep_3" title="Fullscreen" aria-label="Fullscreen"></button>

**谨慎地增加动画，特别是在那些无法提供沉浸性体验的应用中。**看起来过多的无理由的动画会阻碍应用的流畅性，降低性能，还会分散用户在任务中的注意力。尤其要说的是，要有目的和限制性地使用运动效果和UI组件中的动态行为，并确保对结果进行测试。一旦被合理的使用，这些效果能提高用户的理解度和愉悦度；过度使用他们则会使应用看起来很迷惑，很难控制。

**在合适的时候，使自定义的动画与内置动画保持统一。**人们习惯于谨慎添加动画，尤其是在那些不能提供沉浸式用户体验的应用中。如果应用主要关注一些严肃的任务或者生产性任务，那么动画就显得多余了，还会无端打乱应用的使用流程，降低应用的性能，让用户从当前的任务中分心。

**开发者的自定义动画应该切合内置iOS应用的动画。**用户习惯于内置iOS 应用使用的精细动画。事实上，用户趋向于把视图之间的平滑转换，对设备方向改变的流畅响应和基于物理力学的滚动效果看作是iOS体验的一部分。除非你的应用能够给用户沉浸式的体验--比如游戏--自定义动画应该可以与内置应用的动画相媲美。

**使用风格类型一致的动画。**在应用中使用风格类型一致的动画非常重要，可以让用户构建基于使用应用获得的用户体验。

**大多数情况下，恰当一点的做法是让自定义动画更具现实性。**用户乐意于接受自由的艺术创作，但当你的动画违背物理定律和自然法则的时候，他们会感觉到非常迷惑。

### 1.9 品牌推广（Branding）

品牌推广并不仅仅是在应用中展示品牌的颜色和logo。理想状态下，你开发的某个特定品牌的应用应该通过创建独特的外观和感觉来为用户提供难忘的体验。

在iOS系统之下可以很容易地使用自定义的图标、颜色和字体来创建区别于其他应用的UI。当你进行这些元素的设计时，牢记以下两点：

* 每个自定义的元素本身都需要具备良好的观感和功能性，但它也应该与应用中其他元素保持一致，无论应用中其他元素是自定义的还是标准的。
* 为了在iOS中感觉舒适，你的应用虽然不必看起来跟内置的一样，但是需要对它的遵从、清晰度和深度（如欲了解更多，参见1.1 为iOS而设计（Design for iOS））进行整合。花些时间弄清楚在你的应用中遵从、清晰和深度所代表的意味，并把它们在你的自定义元素中表达出来。

当你需要让用户意识到你的品牌时，你应该遵循以下几点：

**以精致优雅不唐突的方式植入品牌的颜色和图片。**用户使用你的应用来完成事务或者进行娱乐，他们不希望被强迫着去观看广告。为了获得最好的用户体验，你可以通过字体、颜色和图像的设计来潜移默化地地提醒用户你的品牌身份。

**避免远离用户关心的内容。**比如，在屏幕顶部展示一个二级栏目，仅用来展示品牌资产，这意味着内容没有足够的空间，可以考虑以其他低侵入性的方法无处不在地展示品牌，比如巧妙地定制屏幕的背景。

[![branding_r_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922174634433-590x442.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922174634433.png)

**抵抗住诱惑，不要把你的logo贯穿整个应用。**移动设备的屏幕多数相当小，logo的每一次出现都会占据空间而将用户与他们想看的内容隔离开。而且，在应用中显示logo并不能像在网页中显示logo那样达到相同的目的：对于用户来说通常会很容易在不知道网页所属的情况下访问一个网页，但却极少有用户会在完全不看一个iOS系统中的应用图标的情况下就打开它。

### 1.10 颜色与字体（Color and Typography）

### 1.10.1 色彩有助于增进沟通（Color Enhances Communication）

在iOS系统中，颜色会用于表征交互，传递活性以及提供视觉连续性。内置的应用程序选择使用那些看起来更具个性的、纯粹、干净的颜色，并辅以或亮或暗的背景组合。

[![color_family_a_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922174710514-590x284.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922174710514.png)

**如果你要创建多样的自定义颜色，要确保它们能够和谐共存。**例如，如果你的应用的基本风格是柔和的色调，你就应该创建一个协调的柔和色调的色板用于整个应用。

**注意在不同情境下的颜色对比。**例如，如果在导航栏的背景与栏按钮标题之间没有足够的对比，按钮就会很难被用户看到。 依据经验的法则来说，需要区分的颜色必须至少存在50%的亮度差异。（我们）需要将设备置于不同的光照环境之中（包括晴朗的室外）来测试设备上的观感效果。

**提示：**一种发现需要更高对比度的区域的方法是降低UI的饱和度并在灰度模式下查看它。如果在灰度版本中你很难区分可交互与非可交互元素或背景等，你有可能需要增加这些元素之间的对比度。

**当你使用自定义的栏颜色时，着重考虑半透明的栏和应用内容。**当你需要创建能匹配特别颜色的栏颜色时（比如一个已有品牌中的颜色），可能在你获得你想要的结果之前，你需要用各种颜色进行实验。栏的显示将会同时受到iOS系统所提供的半透明栏与藏在栏后面的应用内容的呈现所影响。

**API注释：**使用浅色（TintColor）的属性值给予栏按钮颜色，使用栏浅色（BarTintColor）的属性值为栏本身赋色。欲了解更多关于栏属性的内容，可参见_[UINavigationBar Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UINavigationBar_Class/index.html#//apple_ref/doc/uid/TP40006887)_,，[UITabBar Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITabBar_Class/index.html#//apple_ref/doc/uid/TP40007521)，_[UIToolbar Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIToolbar_Class/index.html#//apple_ref/doc/uid/TP40006927)_和 _[UISearchBar Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UISearchBar_Class/index.html#//apple_ref/doc/uid/TP40007529)。_（译者注：相关章节翻译将在后续更新中放出，烦请各位耐心等候。）

**注意颜色的盲区。**多数色盲的人很难区分红色与绿色。需要对你的应用进行测试以确保在其中你没有将红色与绿色作为区分两个不同状态或值的唯一方式，一些图像编辑软件或工具能够有效的帮你验证颜色的盲区。通常意义来说，使用多种方式来表征原色的交互性是非常好的（需要了解更多关于在iOS系统中表征交互性的信息，详见Interactive Elements Invite Touch）。

**考虑选择一种基准色颜色来表征交互性与状态。**在内置的应用中基准色有比如备忘录中的黄色与日历中的红色等。如果你定义一种用于表征交互和状态的基准色，要确保你的应用中的其他颜色不会与它发生冲突。

**色彩可以向用户传达信息，但不一定会以你希望的方式。**每个人眼中的色彩是不一样的，不同的文化为色彩赋予的意义也是不相同的。花时间来研究如何使用色彩才可能会被其他国家或者文化接受。你要尽可能确定应用中运用的色彩向用户传达了恰当的信息。

**大多数情况下，不能让颜色喧宾夺主，让用户分心。**除非色彩是应用的目的和本质所在，通常情况下色彩应该用来从细微细节之处提升用户体验。

### 1.10.2 文字应该清晰易读（Text Should Always Be Legible）

文字首先必须是清晰可辨的。如果用户不能看清楚应用中的字词，那么文字再好看也是没是无意义的。当你在你的应用中采用Dynamic Type时，你可以实现：

* 能自动调整文字的粗细，字母间距以及行高。
* 为语义上有区别的文本模块指定不同的文本样式，比如正文、脚注或者标题。
* 文本可以根据用户在动态文字和可访问性设置中指定字体大小的变化作出适当的响应。

**注：**如果你是用自定义字体，你仍然可以依据系统的字号设置来规划字体范围。当用户改变设置时，你的应用也必须响应式的配合。

就你而言，要采用Dynamic Type需要一些工作。为了学习如何使用文字样式并确保当用户改变文字型号设置时你的应用能够获取通知，可以参考_[Text Styles](https://developer.apple.com/library/ios/documentation/StringsTextFonts/Conceptual/TextAndWebiPhoneOS/CustomTextProcessing/CustomTextProcessing.html#//apple_ref/doc/uid/TP40009542-CH4-SW65)_ in _[Text Programming Guide for iOS](https://developer.apple.com/library/ios/documentation/StringsTextFonts/Conceptual/TextAndWebiPhoneOS/Introduction/Introduction.html#//apple_ref/doc/uid/TP40009542)。_（译者注：相关章节翻译将在后续更新中放出，烦请各位耐心等候。）

**文本尺寸的响应式变化需要优先考虑内容。**并不是所有的内容对于用户都是同等重要的。当用户选择更大的文本尺寸时，他们是想要使他们关注的内容更容易阅读；他们并不总是想要屏幕上的每个单词都更大。

例如，当用户选择具备更大易用性的文本尺寸时，邮件将会以更大的尺寸显示邮件的主题和内容，而对于那些没那么重要的信息——如时间和收件人——则采用较小的尺寸。

![mail_message_axlarge_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922175017938.png)

**在适当的情况下，当用户选择一个不同的文本尺寸时要调整页面布局。**例如，当用户选择小的文本尺寸时，你可能想将内容由一列的布局方式改为两列。如果你决定根据不同的文本尺寸调整布局，你可以选择针对尺寸的子集来实现——如包含小，中和大尺寸——而不是对于每个可能的尺寸都进行布局的调整。

**确保一个自定义字体在不同尺寸下的所有类型都具备可读性。**实现这一效果的方法之一是效仿在不同的文本尺寸下iOS系统呈现字体样式的一些方法。例如：

* 文本永远都不应该小于11点（points），即使是用户选择极小的文本尺寸。相较而言，内容样式使用17点的字号作为大尺寸的默认文本尺寸设置。
* 通常来说，字号与行距值在每一档的文本尺寸设置中差别为1点。唯一例外的是两种标题的样式，它们被应用在极小、小和中尺寸的设置中，使用了相同的字号、行距和字距。
* 在最小的三种文本尺寸中，字间距相对较大；而在最大的三中文本尺寸中，字间距相对紧凑。
* 标题和内容的样式使用相同的字体尺寸，同时，为了区分标题与内容样式，标题样式使用更重的值。
* 导航控制栏的文本使用相同的字号，而内容文本的样式则使用大尺寸的设置（值为17点）。
* 文本总是使用常规或者中重，一般不适用轻或者加粗。

**通常情况下，应用中整体应该使用单一字体。**多种字体的混杂会使你的应用看上去支离破碎和草率。相反，使用一种字体和少数样式。根据语义用途，使用[UIFont](https://developer.apple.com/library/prerelease/ios/documentation/UIKit/Reference/UIFont_Class/Reference/Reference.html#//apple_ref/occ/cl/UIFont)类的API来定义不同文本区域的样式，比如正文或者标题。

[![font_choice_rec_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922175243391-590x442.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922175243391.png)

### 1.11 图标和图形（Icons and Graphics）

### 1.11.1 应用图标（The App Icon）

每个应用都需要一个漂亮的图标。用户常常会在看到应用图标的时候便建立起对应用的第一印象，并以此评判应用的品质、作用以及可靠性。

[![app_icon_gallery_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922175419642-590x79.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922175419642.png)

以下几点是你在设计应用图标时应当记住的。当你确定要开始设计时，请参考[App Icon](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/AppIcons.html#//apple_ref/doc/uid/TP40006556-CH39-SW1)来获取更详细的设计规格与指导。（译者注：App Icon章节处在iOS Human Interface Guidelines的Icon and Image Design部分，翻译将在后续更新中放出，烦请各位耐心等候。）

* 应用图标是整个应用品牌的重要组成部分。将图标设计当成一个讲述应用背后的故事，以及与用户建立情感连接的机会。
* 最好的应用图标是独特的，整洁的，打动人心的，让人印象深刻的。
* 一个好的应用图标应该在不同的背景以及不同的规格下都同样美观。为了丰富大尺寸图标的质感而添加的细节有可能让图标在小尺寸时变得不清晰。

### 1.11.2 栏图标（Bar Icons）

iOS提供了一系列小的icon，用以代表各种常见任务与操作，它们常用在标签栏(Tab Bar)、工具栏(Toolbars)与导航栏(Navigation Bar)中。用户通常都已经了解这些内置图标的含义了，因此可以尽可能的多使用它们。

[![bar-icons_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922175420171.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922175420171.png)

如果需要自定义动作或者内容，你也可以设计自定义图标。设计这些小的线性图标与设计应用图标有很大的区别，请参考[Bar Button Icons](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/BarIcons.html#//apple_ref/doc/uid/TP40006556-CH31-SW1)来了解更多内容。（译者注：Bar Button Icons章节处在iOS Human Interface Guidelines的Icon and Image Design部分，翻译将在后续更新中放出，烦请各位耐心等候）

请注意，你有时候也可以用文字来代替工具栏和导航栏的图标。 就像iOS的日历里面，工具栏上便是使用“今天”、“日历”和“收件箱”来代替图标进行表意的。

[![text_in_toolbar_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922180604418.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922180604418.png)

想要决定在工具栏和导航栏中到底是用图标还是文字，可以优先考虑一屏中最多会同时出现多少个图标。如果数量过多，可能会让整个应用看起来难以理解。使用图标还是文字还取决于屏幕方向是横向还是纵向，因为水平视图下通常会拥有更多的空间，可以承载更多的文字。

### 1.11.3 图形（Graphics）

iOS应用大多数图形丰富。无论是你需要展示用户的照片，还是需要创建自定义图片，以下这些需求都应该遵守：

* **支持****Retina****显示屏。**确保你应用中的所有图片资源都提供了高分辨率规格。尤其需要注意的是，iPhone 6 Plus需要提供@3x规格的图片，而所有其他的高分辨率iOS设备都需要提供@2x规格的图片。
* **显示照片或图片时请使用原始尺寸，并不要将它拉伸到大于****100%****。**你不会希望在你的应用中看到拉伸和变形的图片。可以让用户自己来选择他们是否想要缩放图片。

**不要使用带有苹果符号与版权的图片。**这些符号都拥有版权，并且产品的设计可能会经常改变。

### 1.12 术语和措辞（Terminology and Wording）

你在应用中呈现的每一个字都是与用户进行对话的一部分。把握这样的对话机会，为你的用户提供清晰的表意与愉悦的体验。

[![appropriate_terminology_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922180325192.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922180325192.png)

设置是面向全体用户的一个基础应用，它使用了简明扼要的语言来描述了用户可以进行的操作。举个例子，设置→勿扰模式（Do Not Disturb）就没有使用难以理解的复杂术语，而是用了简单的语言，给用户描述了里头的一系列操作。

**保证你使用的术语是用户能理解的。**根据你对用户群的理解来决定在应用中使用什么样的词汇。举个例子，在一款针对小白用户的应用中使用技术术语是不合适的，但对于针对高端用户的应用来说，使用技术术语是很自然的事情。

**使用非正式的友好语气，但不需要太过低三下四。**避免太正式太僵化，或者太过嘻嘻哈哈，傲慢无礼。请记住，用户可能会反复阅读这些文本，因此有些起初看上去很俏皮的语句，多看几次之后可能会显得幼稚和烦人。

**像新闻编辑一般遣词造句，避免不必要的冗余语句。**当你的文案足够简明扼要，用户就可以很轻松地阅读和理解它。确定最重要的信息，精炼它并且突出它，让用户不需要读一大段文字才能了解他们在找什么，以及下一步要做什么。

**给控件加上短标签或者容易理解的图标。**让用户只扫一眼就能知道这个控件是干什么的。

**描述时间时要注意准确性。**今天和明天这些词汇确实显得比较友好，但有时候会让用户费解，因为你可能没有办法确定用户当前的时区和时间。举个例子，假如有一项活动会在半夜12点前开始，对于在同一个时区的用户而言，这个活动是在今天开始的，但对于那些在早一点的时区里的用户而言，这个活动在昨天就已经开始了。

为你的应用写一则漂亮的App Store描述，最大程度地把握住这个与潜在用户沟通的绝佳机会。除了准确描述你的应用、强调应用的品质与亮点以外，你还需要：

* **修正所有的拼写、语法与标点符号错误。**这些小错误也许不会影响用户正常使用，但是可能会让他们对应用的整体品质产生负面印象。
* **尽量少用全大写的词汇。**虽然大写单词有时候可以吸引注意力，但是全大写的段落不适合阅读，而且会产生一种朝用户扯着嗓子吼的感觉。
* **可以描述****bug****修复情况。**如果你的应用新版包含用户一直期待的bug修复，那在你的软件描述中提到这一点就是个很好的做法。

### 1.13 与iOS的整合（Integrating with iOS）

与iOS整合，指的是在当前平台上给用户提供一种舒适的、宾至如归般的体验，当然这并不意味着我们要把每一个应用做的和内置应用一模一样。

最好的与iOS整合的方式便是深刻地了解iOS的主题与核心——这一部分在上文1.1 为iOS而设计（Designing for iOS）部分中已有详细描述，并寻求出如何在你的应用中融合与表达这种主题。当你这么做的时候，遵循本章中的指引可以帮助你为你的用户提供他们想要的体验。

### 1.13.1 正确使用标准UI元素（Use Standard UI Elements Correctly）

尽可能使用UIKit提供的标准UI元素。多使用标准元素而非自定义元素，你与你的用户都将受益：

* 标准UI元素会根据iOS官方的更新而自动更新——而自定义元素不会。
* 标准UI元素对于你自定义外观和行为来说拥有优秀的扩展性。举个例子，iOS中所有的视图（Views）都是可自定义颜色的，它让应用配色变得很简单。想要了解更多如何给UI元素定义颜色，可以参考[iOS 7 UI Transition Guide](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/TransitionGuide/index.html#//apple_ref/doc/uid/TP40013174)中[Using Tint Color](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/TransitionGuide/AppearanceCustomization.html#//apple_ref/doc/uid/TP40013174-CH35-SW3)的相关章节。
* 用户更熟悉和习惯标准的元素，因为这对于他们来说没有学习成本，他们可以立刻明白这些元素的用途。

想要充分地利用标准UI元素的优点，有一些关键点需要特别注意：

**严格遵循每个****UI****元素的设计规范。**当你应用中的UI元素的外观与功能都是用户所熟悉的，他们可以很容易地根据先前的经验来使用他们，进而更好地使用你的应用。你可以从这些章节中找到各种UI元素的设计规范：[Bars](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Bars.html#//apple_ref/doc/uid/TP40006556-CH32-SW1), [Content Views](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/ContentViews.html#//apple_ref/doc/uid/TP40006556-CH33-SW1), [Controls](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Controls.html#//apple_ref/doc/uid/TP40006556-CH35-SW1), [Temporary Views](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Alerts.html#//apple_ref/doc/uid/TP40006556-CH34-SW1).

（译者注：上文提到的章节均处在iOS Human Interface Guidelines的第4章，翻译将在后续更新中放出，烦请各位耐心等候。若有需要，亦可先参考先前已翻译的iOS7 UI Elements章节：[上](https://isux.tencent.com/ios-human-interface-guidelines-ui-design-ios7-ui-1.html)，[下](https://isux.tencent.com/ios-human-interface-guidelines-ui-design-ios7-ui-2.html)。）

**不要混用不同版本的****iOS****里的****UI****元素。**你一定不希望让用户觉得你的UI元素来自于与当前设备版本不同的iOS系统。

**大体来说，请避免创造自定义****UI****元素来表现标准交互行为。**先问问你自己为什么一定要创建一个与标准UI元素行为完全相同的自定义元素。如果你只是想改变标准UI元素的外观，可以考虑使用UIKit外观定制API（UIKit appearance customization APIs），或者给元素填充别的颜色。如果你需要定义一个与标准控件稍有不同的行为，请确保你在改变了这个UI元素的属性和行为之后，这个元素仍然能完成你所希望的操作。

**不要用系统自带的按钮和图标表达其他含义。**iOS提供了多种可用的按钮和图标。请确认你了解它们的准确表意；不要单纯凭借你看到这些图标样式的猜测和理解来解读和使用它们。（你可以在[Toolbar and Navigation Bar Buttons](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Bars.html#//apple_ref/doc/uid/TP40006556-CH32-SW33)和[Tab Bar Icons](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Bars.html#//apple_ref/doc/uid/TP40006556-CH32-SW34)中了解到这些按钮和图标的准确含义。）

如果你所需要的功能无法用系统提供的按钮和图标来表现，你也可以设计自定义按钮。自定义按钮的设计可以参考[Bar Button Icons](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/BarIcons.html#//apple_ref/doc/uid/TP40006556-CH31-SW1)。

（译者注：上文提到的章节均处在iOS Human Interface Guidelines的第4章，翻译将在后续更新中放出，烦请各位耐心等候。若有需要，亦可先参考先前已翻译的iOS7 UI Elements章节：[上](https://isux.tencent.com/ios-human-interface-guidelines-ui-design-ios7-ui-1.html)，[下](https://isux.tencent.com/ios-human-interface-guidelines-ui-design-ios7-ui-2.html)。）

**如果你的应用****是沉浸式体验，那么创造全新的自定义****UI****是合理的。**因为你在创造一个统一的体验环境，让用户在其中能够有所期待并探索如何控制应用。

### 1.13.2 弱化文件和文档处理（Downplay File and Document Handing）

iOS应用可以帮助用户创建和处理文件，但这并不意味着用户需要过分考虑iOS设备的文件系统如何运作。

如果你的应用中支持用户创建和编辑文档，那么提供一个清晰的图形库视图（document library view）让用户能够方便地打开或者新建文档是一个好的做法。理想状况下，这样的图形库视图拥有以下特征：

* **高度图形化。**用户通过屏幕上的缩略图就可以一目了然，快速找出自己想要的文件。
* **让用户用最少的动作完成自己的任务。**比如说，用户可以快速地水平滚动文件列表，然后轻点一下自己想要的文件来打开它。
* **包含新建文档功能。**一个图形库视图应该支持让用户点击一个新建文档的占位图便完成新建文档操作，而不是让用户通过访问别的地方来新建文档。

举个例子，Pages应用的图形库视图里面，既展示了用户已存在的文档，也加入了便捷的新建文档操作。

[![document_library_2x](https://isux.tencent.com/wp-content/uploads/2014/09/20140922180411133-590x293.png)](https://isux.tencent.com/wp-content/uploads/2014/09/20140922180411133.png)

如果你的应用允许用户使用在其他应用中创建的文档，你可以通过模态文档选择视图控制器(modal document picker view controller)来帮助用户触达它们。这个控制器可以提取用户在iCloud中的文档，还可以通过文档提供者扩展（Document Provider extensions）来提取在其它应用中创建和储存的文件。想要了解更多文档提供者扩展的内容，可以参考[Document Provider Extensions](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/AppExtensions.html#//apple_ref/doc/uid/TP40006556-CH67-SW5); 想要了解更多文档提取视图控制器，请参考[_Document Picker Programming Guide_](https://developer.apple.com/library/ios/documentation/FileManagement/Conceptual/DocumentPickerProgrammingGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP4001445).

**给用户足够的信心，让他们相信除非主动取消或者删除，他们的成果会被随时妥善保存****。**如果你的应用帮助用户创建于管理文档，不能要求用户每次都能及时保存。无论是打开另一个文档或切换应用的时候，iOS应用都应当承担起帮助用户保存输入内容的责任。

如果你的应用的主要功能不是创造内容，但又允许用户查看或编辑信息，这种情况下你需要询问用户是否要保存修改。在这种场景下，比较好的做法是提供“编辑”按钮，点击后进入编辑状态，同时编辑按钮变成“保存”和“取消”按钮，这种变化可以提示用户当前处于编辑模式。“保存”可以保留修改内容，“取消”则退出编辑模式。

### 1.13.3 必要时提供可配置选项（Be Configurable If Necessary）

某些应用需要用户手动安装或设置选项，但是大部分应用不需要如此。一个好的应用可以让大部分用户快速上手，并通过主界面给用户提供便捷的调整体验的方式。

当你的应用在默认状态下就能满足大部分用户的期望，用户对设置的需求就减少了。如果你需要储存用户的基本资料，可以优先向系统请求和拉取相关信息，而不是上来就让用户自己填写它。如果你一定要提供用户鲜少用到的设置项，请参考[_App Programming Guide for iOS_](https://developer.apple.com/library/ios/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40007072)中的[The Setting Bundle](https://developer.apple.com/library/ios/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/Inter-AppCommunication/Inter-AppCommunication.html#//apple_ref/doc/uid/TP40007072-CH6-SW7)部分来了解如何在代码中定义它们。

**尽可能在主界面提供设置选项。**如果用户在进行主线任务时有可能频繁改变设置，将设置项放在主UI中会很方便。如果用户只是偶尔才会用到设置项，那么可以将其放在独立的视图中。

**如果应用内相关设置需要在系统设置中改变，帮助用户直接访问系统设置。**尤其是，如果你要用一段文字来描述如何改变这个设置，比如“设置>隐私>定位服务”，倒不如直接放置一个按钮，点击后即可到达设置中的定位服务。想要了解如何实现，请参考 [Settings Launch URL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html#//apple_ref/doc/constant_group/Settings_Launch_URL).

### 1.13.4 充分利用iOS技术（Take Advantage of iOS Technologies）

iOS提供了丰富的技术方式来支持用户完成他们所期望的各种任务和场景。这意味着在绝大多数情况下，将系统提供的技术整合到你的应用中，往往比自定义一种新的技术更为可靠。

某些iOS技术，比如多任务并行（[Multitasking](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Multitasking.html#//apple_ref/doc/uid/TP40006556-CH38-SW1)）与语音向导（[VoiceOver](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/VoiceOverAccessibility.html#//apple_ref/doc/uid/TP40006556-CH45-SW1)）等等，是所有应用都应该包含的系统级特性。而另外一些技术是否整合到应用中，则取决于应用本身的功能性。比如处理门票和礼品卡的应用（[Passbook](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Passbook.html#//apple_ref/doc/uid/TP40006556-CH33-SW1)）支持用户通过[In-App Purchase](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/InAppPurchase.html#//apple_ref/doc/uid/TP40006556-CH36-SW1)完成购买，展示应用内置广告（[iAd Rich Media Ads](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/iAdRichMediaAds.html#//apple_ref/doc/uid/TP40006556-CH41-SW1)）则可以整合 [Game Center](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/GameCenter.html#//apple_ref/doc/uid/TP40006556-CH37-SW1)，同时支持[iCloud](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/iCloud.html#//apple_ref/doc/uid/TP40006556-CH35-SW1)。

## 2.设计策略

### 2.1 设计原则（Design Principles）

### 2.1.1 美学完整性（Aesthetic Integrity）

美学完整性并不评判应用的视觉设计，或者用来描述应用的风格特征。美学完整性是指一款应用的视觉表现和交互行为在与功能结合后所传达出的整体一致性。

[![01](https://isux.tencent.com/wp-content/uploads/2014/10/20141014193747280-590x307.png)](https://isux.tencent.com/wp-content/uploads/2014/10/20141014193747280.png)

人们关心应用是否提供了应有的功能，但是也会潜移默化甚至是很直接地被应用的视觉表现和交互行为所影响。举个例子，一款协助用户完成任务的应用，可以通过使用精美而又无干扰的装饰性元素、标准的控件和可预期的交互行为来帮助用户聚焦在任务本身上。这样，应用就能传达出清晰一致的信息，使得人们信任它。但是，如果应用使用干扰的、琐碎或随意的UI来呈现任务，那么人们可能会对其可靠性和可信赖度产生怀疑。

另一方面，在沉浸式应用中—例如游戏—用户期待惊艳的视觉表现，为用户带来乐趣和刺激，并鼓励用户进行探索。人们不希望在游戏中完成严肃的或生产力式的任务，他们会期待游戏的视觉表现和交互行为能够整合进任务当中。

### 2.1.2 一致性（Consistency）

一致性可以让人们在一款应用中的不同部分甚至不同应用间复用他们的知识和技能。一款具备一致性的应用不应盲从地复制其他应用，也不应在风格上一成不变。应用应专注于让人们觉得舒适的标准和范例，并提供应用内部统一的体验。

[![02](https://isux.tencent.com/wp-content/uploads/2014/10/20141014193747967-590x234.png)](https://isux.tencent.com/wp-content/uploads/2014/10/20141014193747967.png)

在决定一款iOS应用是否要遵守一致性原则时，请思考如下问题：

- 应用是否和iOS标准一致？是否正确地使用了系统提供的控件、视图和图标？是否以用户所预期的方式整合了设备的特性？
- 应用是否内部统一？文案是否使用了一致的措辞和风格？同样的图标是否表意相同？在不同的位置执行同样的操作时，人们是否能能预期会发生什么？
- 应用是否和先前的版本保持一致？条款和意义是否保持不变？基本概念和主要功能是否发生了变化？

### 2.1.3 直接操作（Direct Manipulation）

当人们不再使用一堆控件进行操作，而是直接操作屏幕上的对象时，他们能更集中精力完成任务，也更容易理解这些行为所产生的结果。

[![03](https://isux.tencent.com/wp-content/uploads/2014/10/20141014193748601-590x286.png)](https://isux.tencent.com/wp-content/uploads/2014/10/20141014193748601.png)

使用多点触摸界面，人们可以通过捏合操作来直接放大和缩小图片或文本内容。在游戏中，玩家应该直接移动和作用在屏幕上的对象。例如，游戏中可能会显示密码锁，用户可以通过转动它来打开。

在一款iOS应用中，如下情况中人们应该能够进行直接操作：

- 旋转或者移动设备来影响屏幕上的对象
- 使用手势来操作屏幕上的对象
- 显示即时可视的操作反馈

### 2.1.4 反馈（Feedback）

反馈可以明示人们的行为，展示操作的结果，并更新于任务进程之中。

[![04](https://isux.tencent.com/wp-content/uploads/2014/10/20141014193749242-590x386.png)](https://isux.tencent.com/wp-content/uploads/2014/10/20141014193749242.png)

iOS内置的应用对用户的每个行为都提供了可感知的反馈。当人们点击列表项和控件时，它们会被临时高亮，并会在操作过程中持续一段时间，以此展示控件被执行的过程。

精细的动画会给人们带来有意义的反馈，帮助阐明行为的结果。例如，列表中新增一项时的动画可以从视觉上帮助人们发现列表的变化。

音效同样可以为人们提供有效的反馈，但不应成为唯一的反馈方式，因为人们不一定能听到。

### 2.1.5 隐喻（Metaphors）

当应用中的虚拟对象和交互行为与用户已经熟悉的体验相似时—无论这些体验是来源于真实或数字生活—用户就可以快速地掌握如何来使用这个应用。

当应用使用隐喻来传达某种用法或体验时，最好不要让隐喻突破所依赖的对象或交互行为本身的限制。（译者注：此处可理解为对于隐喻的使用应量力而为，不要过于牵强。）

由于人们实际上是和屏幕进行物理上的交互，所以iOS应用有很大的余地来使用隐喻。iOS中的隐喻包括：

- 移动分层视图来显示被遮挡的内容
- 拖曳、轻扫和滑动游戏中的对象
- 点击开关，滑动滑块，转动选择器
- 轻扫来翻阅书本或杂志

### 2.1.6 用户控制（User Control）

是人—而不是应用—发起和控制行为。应用可以对用户进行操作建议，对有危害的后果予以警示，但是不应替用户来做决策。好的应用会在给人们帮助他们避免不必要结果的能力时，找到正确的平衡。

[![05](https://isux.tencent.com/wp-content/uploads/2014/10/20141014193749941.png)](https://isux.tencent.com/wp-content/uploads/2014/10/20141014193749941.png)

当对应用的交互行为和控件都较为熟悉和可预期时，用户会觉得应用更易上手。那些简单直白的交互行为更容易被用户所理解和记住。

人们会希望在一个操作被执行之前有足够的机会来取消，也希望在执行一个不可逆的操作之前可以有机会来进行确认。最后，人们还会希望能够停止正在执行中的操作。

### 2.2 从概念到产品(From Concept to Product)

### 2.2.1 定义应用（Define Your App）

**应用的定义**是对应用主要功能和目标用户的简明具体的描述。

尽可能早地创建应用的定义可以帮助你将一个想法和功能清单转换为用户想要的条理清晰的产品。在开发过程中，可以使用定义来决定某些功能和行为是否合理。使用以下几个步骤来创建一个可靠的应用定义。

#### **1****、列出所有你认为用户可能喜欢的功能**

可以直接进行头脑风暴。此时，你需要列出所有与产品中心有关的任务。不用担心清单太长，因为接下来会进行删减。

假设你一开始的想法是开发一个帮助人们购买食品杂货的应用。你可以思考在进行这项活动时，会涉及到哪些相关的任务，这些就是用户可能感兴趣的潜在功能。例如：

- 创建清单
- 查找食谱
- 比较价格
- 定位商店
- 给食谱做注释
- 查找可使用的优惠劵
- 查看烹饪演示
- 探索不同的烹调方法
- 寻找某些食材的替代物

#### **2****、确定目标用户**

现在你需要清楚地将你应用的用户与其他iOS应用的用户区分开来。确定在此情此景下，什么是对你的用户最重要的。在食品杂货例子中，你可能需要问问你的用户：

- 通常是在家里做饭还是更喜欢现成的食物
- 是忠实的优惠券用户还是认为优惠券没多大价值
- 喜欢寻找特别的食材还是喜欢基本食材
- 严格按照食谱做菜还是只把食谱当做灵感来源
- 喜欢少量多次购买还是一次性购买大量食物
- 希望能保留多个不同目的的清单还是只希望记录回家路上需要购买的几个东西
- 坚持使用固定的品牌还是会使用方便的替代品
- 习惯于购买固定的一些物品还是会按照食谱来购买

思考过这些问题之后，你可以从三个方面来描述目标用户的特征：喜欢按照食谱进行尝试，时常很匆忙，通常情况下很节俭。

#### **3****、根据目标用户过滤功能清单**

如果在确定了一些用户特征后，你最终只得到了几个主要功能，那么你就已经步入了正轨：出色的iOS应用应该聚焦在帮助用户解决问题的核心任务上。

例如，即使第一步想出的那些可能需要的功能都是有用的，也不可能全都被第二步定义的目标用户认可。

当你在目标用户的使用情境下检查功能清单时，就可以判断你的应用应该聚焦在三个主要功能上：创建清单，获得并使用优惠劵，获得食谱。

此时你就可以给出应用定义了，总结该应用做什么以及为谁做。食品杂货购买应用的定义可能如下：

“为热爱烹饪且节俭的用户订制的创建购物清单工具。”

#### **4****、不止于此**

应用定义应该贯穿于整个开发过程，使用应用定义来确定功能，控件，措辞的合理性。例如：

**当你想要新增一个功能时**，问问你自己这对应用的主要目的和目标用户是否非常重要。如果不是，可以置之不理。例如，你已经确定了你的用户对大胆新颖的烹饪方法感兴趣，那么着重展示盒装蛋糕和现成的食物就不太合适。

**当你考虑用户界面的外观和行为时**，问问你自己你的用户更喜欢简单的、流线型的风格，还是有明显主题的风格。以用户目标为指导来完成你的应用，理解用户期望通过你的应用完成什么，例如完成任务的能力，快速找到答案的能力，深入综合内容的能力，或者获得娱乐的能力。例如，尽管你的食品杂货清单应用需要易于理解和快速上手，但你的用户还是可能倾向于一个有关食物的主题界面。

**当你考虑应该使用怎样的措辞时**，努力和用户对这个主题的专业程度相匹配。例如，尽管你的用户可能不是由专业的大厨组成，但你也可以肯定他们希望看到有关食材和技术专用的措辞。

### 2.2.2 为任务量身订制界面（Tailor Customization to the Task）

好的iOS应用会根据清晰的目标和易用性来平衡用户界面的设计。为了达到这种平衡，要确保在设计阶段前期就考虑定制化。因为考虑品牌性、原创性和适销性通常会影响定制化的决策，所以专注于定制化怎样影响用户体验是有挑战性的。

可以由应用中的任务着手：用户执行这些任务的频率如何，在什么样的环境下进行？

举个例子，想象一个计算器应用使用的是精心设计的，充满艺术感的风格，并且使用了创新的布局来展示大家熟悉的计算器元素。这些像艺术品一样的细节渲染和创新的布局并不会影响用户去理解怎样点击按钮和查看计算结果。但是对于只想简单完成任务的用户，这种新奇的体验和美丽的界面很快就会失去效用，并且可能成为一种妨碍。

[![06](https://isux.tencent.com/wp-content/uploads/2014/10/20141014194112485.png)](https://isux.tencent.com/wp-content/uploads/2014/10/20141014194112485.png)

相反，GarageBand（随身录音室应用）可以不展示好看的、逼真的乐器来帮助用户制作音乐，但这样会使应用缺少身临其境的愉悦感。在GarageBand里，界面不只是向用户展示了如何使用，同样使得制作音乐的主任务更容易完成。

[![07](https://isux.tencent.com/wp-content/uploads/2014/10/2014101419411362-590x332.png)](https://isux.tencent.com/wp-content/uploads/2014/10/2014101419411362.png)

当你思考定制化如何增强或减弱用户完成任务的注意力时，记住以下几点：

**定制总要有缘由。**理想情况下，定制化的用户界面能促进用户完成任务并增强他们的体验。你最好尽可能地用任务驱动定制化决策。

**尽量避免增加用户的认知负担。**用户对标准界面元素的外观和行为都已经很熟悉了，所以他们不用停下来思考如何使用它们。当用户面对外观和行为与标准不同的元素时，他们就失去了经验优势。除非你的独一无二的元素能够使任务更容易完成，否则用户很可能不喜欢被强制学习一些在其他应用都不通用的操作。

**保持内在的一致性。**你的应用中自定义元素越多，保持这些元素外观和行为的一致性就越重要。如果用户花费时间去学习了你创建的那些不熟悉的控件，那么他们会希望新学到的这些操作能够在整个应用中通用。

**总是以内容为重点。**因为标准元素很熟悉，所以它们不会分散用户在内容上的注意力。当你自定义用户界面时，注意确保界面元素不会抢走用户对内容的注意力。例如，如果你的应用允许用户观看视频，你可能选择设计一个自定义的重播控件。但是不管你用的是自定义还是标准的重播控件，都没有它是否在用户开始观看后隐藏，点击屏幕后出现来的重要。

**在对标准控件进行重设计时再三思考。**如果你不只是想自定义标准控件，而是想重设计，确保你的重设计能提供尽可能多的信息。例如，你设计了一个开关控件，它没有可以指明相反状态存在的信息，那么用户很可能意识不到这是个有两个状态的控件。

**一定要彻底测试自定义的界面元素。**在测试过程中，近距离的观察用户是否能预测你的元素如何使用以及是否能容易地与它们交互。例如，如果你创建的控件的可点击区域小于44 x 44点，用户点击时就会有困难。或者如果你创建了一个视图对点击和滑动的反馈不一样，确保这个视图提供的功能值得用户去额外关注交互的不同。

### 2.2.3 原型与迭代（Prototype & Iterate）

在你投入工程资源实现设计之前，创建原型来进行用户测试是个很好的主意。即使只有几个同事来帮你测试原型，你也会收获一些关于应用功能和用户体验的新鲜观点。

在设计的早期阶段，你可以使用纸面原型或者线框图去呈现主要的视图和控件，并且标明每个页面之间的跳转关系。你可以从线框图测试中获得一些有用的反馈，但是线框图的稀疏性有可能会误导用户。因为用户很难想象当线框被实际内容填满时体验会有什么样的变化。

如果你有一个可以在设备上运行的原型，那你可以得到更多有用的反馈。当用户能在设备上与你的原型进行交互时，他们能更容易发现应用中哪里功能不满足预期，哪里体验过于复杂。

创建可靠原型的最简单的方法是使用基于故事板（storyboard）的Xcode模板创建一个基础应用，然后使用一些类似于占位符的内容来进行填充。（**故事板（storyboard）**文件可以涵盖应用中的所有界面，并且包括界面之间的跳转关系。）接着，将这个原型导入到设备中，这样被测者就可以有一个尽可能真实的体验了。

你不需要在原型中提供大量的实际内容或者使每一个控件都可用，但是你确实需要营造足够的情境来保证真实的体验。并且需要在典型用户体验和非典型的边缘情况之间做好平衡。例如，如果你的应用需要处理很长的列表项，你的原型就不能只显示一两个条目。而且在用户测试交互中，只要被测者能够点击屏幕上的一个区域进入到下一个逻辑页面或者完成主任务，那他们就可能会提供更有建设性的反馈。

当你使用Xcode应用模板来创建原型时，你可以免费使用很多功能，并且它可以相对容易地进行设计中的响应反馈调节。在你确定设计方案并投入资源进行实现之前，应该对原型进行多次迭代测试。想要开始学习Xcode，请参考*Xcode Overview*。

### 2.3 案例学习：从桌面到iOS（Case Study: From Desktop to iOS）

### 2.3.1 iPad版Keynote应用（Keynote on iPad）

桌面版的Keynote 应用是一个十分强大而又灵活的应用，可以创建非常优秀的幻灯片。人们喜爱Keynote将简单易用与良好的细粒度的操作结合进而控制无数精确细节的方式，如动画和文本属性等。

[![08](https://isux.tencent.com/wp-content/uploads/2014/10/20141014194423883-590x356.png)](https://isux.tencent.com/wp-content/uploads/2014/10/20141014194423883.png)

iPad版的Keynote提取了Keynote桌面版的核心要素，并通过创造以下的用户体验使它在iPad上更舒适：

- 专注于用户内容
- 在不削减功能的基础上减少系统的复杂性
- 提供有用而又令人愉悦的快捷操作
- 延续桌面版本的体验
- 利用动人的动画提供良好的反馈与交流

Keynote用户能很快理解如何使用iPad版，是因为它使用了iPad原生的范例，符合了用户对功能上的预期。新用户可以用简单、自然的方式直接操控内容，所以可以很容易学会如何使用iPad版的Keynote。

Keynote从桌面版向iPad版的转变是基于从细节到深层的大量修改和重新设计的。这些都是一些最明显的适应性：

**流线型的工具栏**

工具栏中只有少数的元素，但是它们是用户在创建内容时所使用的全部功能和工具的统一入口。

[![09](https://isux.tencent.com/wp-content/uploads/2014/10/20141014194424468-590x24.png)](https://isux.tencent.com/wp-content/uploads/2014/10/20141014194424468.png)

**简化并优先响应用户焦点的检查器**

iPad版的Keynote能自动侦测各种工具，能通过对用户需求进行分类以修正被选择的对象。（译者注：特别是根据当前的操作对象而有限选择某些工具。）通常，人们可以在第一检查器视图中完成他们需要的所有修改操作。如果他们需要修改那些不常用的属性，他们可以下拉另一个检查器视图来进行。

[![10](https://isux.tencent.com/wp-content/uploads/2014/10/20141014194424849.png)](https://isux.tencent.com/wp-content/uploads/2014/10/20141014194424849.png)

**丰富的预设样式集**

人们可以利用预设的样式很简单地改变对象（如表格或图表）的外观或者感觉。除了颜色之外，每个集中，例如表格的标题和轴区分标识等的预设属性都被设计得与整体的主题和谐一致。

[![11](https://isux.tencent.com/wp-content/uploads/2014/10/20141014194425346.png)](https://isux.tencent.com/wp-content/uploads/2014/10/20141014194425346.png)

**直接操作内容，丰富有意义的动画**

在iPad版的Keynote中，用户可以拖动滑块到一个新的位置，可以扭动旋转一个对象，也可以轻击图片来选中它。iPad版Keynote的响应动画进一步加强了这种可直接操作的印象。例如，用户在移动某个滑块时它通常会暂停，而当它被放置在一个新的位置时，环绕在周围的滑块将会向外扩散给它留出空间。

### 2.3.2 iPhone版邮件应用（Mail on iPhone）

邮件应用是OS X中一款好用而又广受好评的常见应用。它也是一个很强大的程序，可以允许用户撰写、接收、分类和存储邮件，追踪行动和事件，也可以编写备忘录和邀请等。桌面版的邮件应用通过一系列的窗口提供了这些强大的功能。

[![12](https://isux.tencent.com/wp-content/uploads/2014/10/20141014194425847.jpg)](https://isux.tencent.com/wp-content/uploads/2014/10/20141014194425847.jpg)

iPhone版的邮件专注于桌面版邮件的核心功能，帮助人们接收、撰写、发送和组织他们的信息。为了塑造移动iPhone版的邮件应用，将这些功能浓缩在为其量身定制的界面之中，做了如下的工作：

- 将人们的内容前置和居中的合理化呈现
- 专为处理不同任务而设计的不同视图
- 易于浏览并符合认知的信息结构
- 适时提供强大的编辑和组织性工具
- 传达动作和提供反馈的微妙且动人的动画

（我们）必须明白相较于桌面版的邮件应用，iPhone版的邮件应用不是（译者注：或者说并不需要是）一个更好的应用，而是为移动端用户重新设计的邮件应用。iPhone版的邮件应用专注于桌面版的功能子集并将它们呈现在一个吸引人的精简界面之中，据此为移动端的用户提供了核心的邮件体验。

为了使邮件应用的体验能适应移动场景，iPhone版的邮件应用在几个关键的方面革新了用户界面。

**直接、高度专注的页面**

每个页面显示了邮件应用体验的一个方面：账户列表、邮箱列表、消息列表、消息查看和编辑视图。用户可以在一个屏幕内滑动查看完整的内容。

[![13](https://isux.tencent.com/wp-content/uploads/2014/10/20141014194426391-590x320.png)](https://isux.tencent.com/wp-content/uploads/2014/10/20141014194426391.png)

**简单、可预见的导航**

通过每屏的一次点击，用户可以逐层展开通用内容（账户列表）进入具体页面（一封消息）。每个页面会显示一个标题用以指示用户所在的位置，以及一个返回按钮用以更容易地回溯到他们之前的步骤。

**需要时即可获取的、简单的点击性控件**

基本上在任何场景之下，编写邮件和查阅新邮件都是人们首要希望进行的操作，因此iPhone版的邮件应用保证了这两个功能在多个页面中都可以便利地进行。当用户查看一封消息时，就会显示诸如回复、移动和删除等对消息的操作。

**针对不同任务的不同类型的反馈**

当人们删除一封消息时，它会动态地进入垃圾桶图标中。当人们发送一封消息时，可以看到它的发送过程；而当发送结束时，人们可以听到一个特别的声音提示。通过消息列表页面工具栏的副标题，用户通过简单一瞥就可以查看邮箱上次更新的时间。

### 2.3.3 iOS系统内的网页内容（Web Content in iOS）

iOS版的Safari应用在iOS设备上提供了出众的移动网页浏览体验。人们喜欢阅读清晰的文字和图片，也希望能通过旋转设备或者捏合和点击屏幕来调整视图。

基于标准建立的网站可以在iOS设备上显示得很好。特别是那些能侦测设备并不需要插件的网站可以同时在iPhone和iPad上都表现得很好，两者之间不会需要太多的修改，即使有也很小。

除此之外，成功的网站应具备以下的典型性：

- 如果页面宽度需要匹配设备宽度，可以设置合适的视窗（viewport）来适应设备
- 避免CSS中固定的定位，以便当用户缩放或拖动页面时内容无法被移出屏幕
- 拥有一套基于触控操作的用户界面，而不是依赖基于传统点击操作的交互

有时候，额外的一些修改可以（使页面）更合理。例如，在iOS系统中，很多网页应用会设置合适的视窗（viewport）宽度并通常隐藏Safari的UI。如欲了解更多如何进行这些修改，参见*Safari Web Content Guide*章节中的[Configuring the Viewport](https://developer.apple.com/library/ios/documentation/AppleApplications/Reference/SafariWebContent/UsingtheViewport/UsingtheViewport.html#//apple_ref/doc/uid/TP40006509)和[Configuring Web Applications](https://developer.apple.com/library/ios/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html#//apple_ref/doc/uid/TP40002051-CH3)。

网站也可以通过其他的方法适配桌面网页体验到iOS端的Safari浏览器中：

**使键盘适应iOS端的Safari**

当键盘和格式辅助信息出现时，iPhone上的Safari应用会将你的网页显示在URL地址下方和键盘与格式辅助信息上方。

**使弹出式菜单适应iOS端的Safari**

在桌面版的Safari应用中，弹出式菜单会包含很多选项，就如在其他OS X应用中一样。在必要的情况下，菜单展开后可以超出应用窗口的边界以显示其中的所有选项。在iOS版的Safari应用中，弹出式菜单由原生的元素所呈现，这样能提供更好的用户体验。例如，在iPhone上，弹出式菜单会出现在选择器（**picker**）当中，选择器里会一个用户可选择的选项列表。（欲了解更多选择器控件的内容，可以参见[Picker](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Controls.html#//apple_ref/doc/uid/TP40006556-CH15-SW23)。）

## 3. iOS技术

### 3.1 应用扩展（App Extensions）

应用扩展可以延伸应用的使用范围。当用户使用其他应用时，应用扩展使得用户仍能使用你应用的核心功能。举个例子，当人们在Safari中浏览网页时，他们可以使用你的分享扩展来发送一张图片或一篇文章到你的社交网站上。或者当使用照片应用时，人们可能会使用你的图片编辑扩展来为一张图片加上一个滤镜效果。（在这些场景中，Safari和照片应用承载用户使用扩展的场景，因而被称为**宿主应用（****host apps****）**。）

你需要提交包含应用扩展的完整iOS应用到App Store（包含扩展的应用被称为**容器应用（****containing app****）**）。在启用扩展之后，人们就可以在使用其他应用时，通过使用扩展来执行快速任务。例如，在邮件中浏览某个商品时，人们可以不用离开邮件应用就使用你的动作扩展来把商品添加到购物清单中。

表17-1列举了可以创建的iOS应用扩展类型。

表17-1应用扩展类型

| **应用扩展类型**               | **人们使用扩展来做…**              |
| ------------------------ | -------------------------- |
| 今天部件（Today widget）       | 在通知中心中获得快速更新或者在今天视图中快速完成任务 |
| 分享（Share）                | 发送到网站或者和他人分享内容             |
| 动作（Action）               | 通过另一个应用的上下文信息来操作或查看内容      |
| 图片编辑（Photo Editing）      | 使用照片应用编辑图片或视频              |
| 文档提供者（Document Provider） | 进入和管理文档库                   |
| 自定义键盘（Custom keyboard）   | 替换iOS系统键盘                  |

以下指南适用于所有类型的应用扩展，针对特定类型应用扩展的指南请参阅后续章节。（如果想了解如何开发、调试和发布一个扩展，请参阅[*App Extension Programming Guide*](https://developer.apple.com/library/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214)。）

**确保是单任务。**应用扩展并不是应用的精简版，它帮助用户在有全局目标的上下文中完成狭义范围内的有限任务。例如，动作扩展可以为用户提供一种不同的方式来查看当前内容。

**保证用户的交互是有限和流畅的。**好的应用扩展应该只需几步点击就可以帮助人们完成任务，这样他们就能尽快回到之前的场景中。例如，分享扩展只需一次点击即可完成一张图片的分享。

**将容器应用****及其应用扩展的名称保持一致。**一个容器应用中如果有多个扩展，需要使用不同的名称，你需要确保用户能够理解你的扩展和应用之间的关系。人们会在很多不同的情况下遇到扩展，如果他们当下没有认出来，那么他们就未必会信任这些扩展。

**大部分情况下，复用容器应用的图标。**显示用户熟悉的图标是获得用户信任的另一种方式。请注意，对于动作扩展来说，你应该使用单色版本的容器应用图标（详见[分享和动作扩展](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/AppExtensions.html#//apple_ref/doc/uid/TP40006556-CH67-SW3)）。

重要：和设计图标和图形一样，不要重复使用iOS的图标和图片，不要为苹果的产品和设计再设计一套图片。

**避免在扩展上显示模态视图。**很多扩展默认以模态视图来显示，所以应避免再叠加模态视图。尽管有时候用户可能会在扩展上遇到警告框，但是在设计扩展的流程时，应避免出现模态视图。

### 3.1.1 今天部件（Today Widgets）

人们会在通知中心的今天区域中查看今天部件（Today widgets）。因为人们会设置今天区域以显示他们最关注的信息，所以在此进行设计可以有效帮助你的部件在这些用户最重要的信息中占据一席之地。

[![01](https://isux.tencent.com/wp-content/uploads/2014/11/20141123151916566.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123151916566.png)

**设计与通知中心风格一致的外观。**当使用通知中心的默认边距和背景时，你的今天部件就会给用户以统一的体验。为获得最佳的结果，你应该重点关注你的内容而不是背景或者其他的，尤其应该避免绘制一片纯色背景。

注意：iOS会自动在自定义的部件内容上方显示应用的图标和标题（图标会显示在标题前面的空白处）。

**将部件内容与标题对齐。**当你的部件内容与标题对齐时，人们就可以很简单地浏览今天视图中他们想要的部件。遵守今天视图中的边距规范，并将内容约束在如图的部件内容区内。

[![02](https://isux.tencent.com/wp-content/uploads/2014/11/20141123152249949-590x622.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123152249949.png)

**一般情况下，使用白色的系统字体来显示文本。**在通知中心默认背景下白色文字会看起来较好。对于二级文本，可以使用系统提供的vibrant外观样式（查看[notificationCenterVibrancyEffect](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIVibrancyEffect/index.html#//apple_ref/occ/clm/UIVibrancyEffect/notificationCenterVibrancyEffect)了解更多）。

**提供通知中心式的体验。**人们访问通知中心来获取简要的更新或者执行一个非常简单的任务，所以今天部件最好只显示适量的信息和进行有限的互动，特别是：

- 避免用户在部件中需要滚动或纵向移动来查看全部的信息。部件可以通过纵向扩展来显示更多的信息，但若部件的高度超过通知中心的高度就不是一种好的体验了，因为这样会干扰其他部件的查看。
- 避免使用横向扫动或拖曳，因为这会干扰在通知中心进行导航。
- 尽可能使用户只需一步操作就完成任务或打开你的应用（注意，在今天部件中键盘是不可用的）。
- 优化性能以便人们可以即刻获得有用的信息。可以考虑在本地缓存信息，以便当有更新时就可显示最近信息。人们只希望在今天视图中花很少的时间，如果部件使用内存不当，iOS就可能会终止它。

**在适当情况下，让人们点击你的今天部件来打开你的应用。**因为今天部件提供了专一的体验，所以就能有效引导人们去到你的应用以获取更多信息或功能。最好不要显示“打开应用”按钮，而是应该让你的整个今天部件都可被点击来打开应用。你也可以让用户点击部件中的UI对象，以打开你的应用并跳转到关于此UI对象的视图中。举个例子，日历部件显示了今天的事件，如果用户想要获得某个事件的更多信息，他们可以点击部件中的事件来打开日历应用进行查看。

注意：虽然从部件打开应用的方式对用户来说还不错，但继续在部件中提供有用且及时的信息依然是很重要的。人们可不一定会欣赏一个功能只是打开应用的今天部件。

### 3.1.2 分享和动作扩展（Share and Action Extensions）

人们通过点击应用中的动作按钮（Action button）来使用分享和动作扩展。在通过动作按钮显示的动作视图控制器（activity view controller）中，动作扩展被列在底部，分享扩展被列在动作扩展之上。人们可以使用更多（More）按钮来管理显示在动作视图控制器中的分享和动作扩展。

[![03](https://isux.tencent.com/wp-content/uploads/2014/11/20141123152426973.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123152426973.png)

分享或动作扩展通常被认为是在当前用户场景下用来输入内容之用。例如，当在Safari中阅读一篇文章时，用户可能会点击动作按钮并使用一个分享扩展来发送这篇文章到分享网站上，也可能会使用一个动作扩展来查看这篇文章的翻译。

注意：在动作视图控制器中，iOS只会显示支持当前内容类型的动作扩展。例如，当用户当前内容是视频时，iOS就不会显示支持文本的动作扩展。

**尽可能在分享扩展中使用系统提供的UI****。**系统所提供的撰写视图控制器（compose view controller）提供给用户一种一致的体验，并能自动支持一些常用任务，例如预览和确认标准项，同步内容，查看动画，以及完成一封邮件。欲知更多关于使用系统提供的撰写视图控制器，请参见[*App Extension Programming Guide*](https://developer.apple.com/library/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214)中的[Share](https://developer.apple.com/library/ios/documentation/General/Conceptual/ExtensibilityPG/ShareSheet.html#//apple_ref/doc/uid/TP40014214-CH12)。

**如果上传需要一定时间，那就应考虑在分享扩展的容器应用中显示上传进度。**无论分享的文件有多大，人们都期待在点击扩展中的发送或分享按钮后，能立即返回他们之前的场景。你需要让进度状态随时更新，但是人们不想每次上传完毕后都收到通知，并且也无法自动重启扩展。在这种场景下，在容器应用中显示上传进度是一种解决方案，这样容器应用就可以在后台处理任务，并在遇到问题时发送通知。

**动作扩展使用单色的应用图标。**（不同的是，分享扩展则应该使用其容器应用的彩色应用图标。）要为动作扩展设计图标时，你可能需要从创建一个应用图标的模版开始着手。如有需要，可以专注图标所特有的元素来进行简化设计。

如果你在容器应用中提供了多个动作扩展，那么最好为他们设计一套图标，且确保这套图标中的每一个看起来都与容器应用的图标是有关联的。

### 3.1.3 图片编辑扩展（Photo Editing Extensions）

当人们在照片（Photos）应用中查看图片或视频时，可以使用图片编辑扩展。一般来说，图片编辑扩展能帮助用户筛选图片或进行一些其他的图片或视频编辑。在用户确认之后，编辑后的内容就会出现在照片应用中。

照片应用提供了一个模态视图来显示图片编辑扩展的自定义UI。当用户在确认对图片或视频的编辑时选择了取消（你必须要在代码上保证存在这个行为），照片应用还可以显示一个确认视图。

**避免在图片编辑扩展中使用导航栏。**如图所示，承载扩展的模态视图已经包含了导航栏，若再增加另一个导航栏，既会占据更多你的界面空间，还会使用户产生困扰。（照片应用默认会以全屏高度来显示你的视图，所以你的内容会出现在内建的导航栏之下。）

[![04](https://isux.tencent.com/wp-content/uploads/2014/11/20141123152513261.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123152513261.png)

**如果可以，让用户能够预览编辑结果。**尽可能让用户在关闭扩展返回照片应用之前看到他们编辑的成果。

### 3.1.4 文档提供者扩展（Document Provider Extensions）

文档提供者扩展帮助人们在其他各种应用中查阅你的应用所管理的文档。在宿主应用（host app）中，文档采集视图控制器（document picker view controller）会显示你的扩展所提供的UI（想要了解更多有关文档采集视图控制器的内容，请查阅[*UIDocumentPickerViewController Class Reference*](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIDocumentPickerViewController_Class/index.html#//apple_ref/doc/uid/TP40014342)）。

注意：文档提供者扩展由两个不同的部分组成：文档采集视图控制器扩展和文件提供者扩展。文档采集视图控制器扩展包括了你的自定义UI，文件提供者扩展实现对文件的访问。本节所使用的术语*文档提供者扩展（**Document Provider extension**）*是为了表述扩展中文档采集视图控制器部分的UI和体验。

**避免在文档提供者扩展中使用导航栏。**iOS会显示扩展的自定义UI，而自定义UI又包含在文档采集视图控制器中基于导航栏的界面之中。所以，在内建导航栏之下再显示第二个导航栏会使用户感到困惑，并且还会占据原本你的内容区域。（文档采集视图控制器默认会以全屏高度来显示你的视图，所以你的内容会出现在内建的导航栏之下。）

[![05](https://isux.tencent.com/wp-content/uploads/2014/11/20141123153446507.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123153446507.png)

### 3.1.5 自定义输入法（Custom Keyboards）

人们使用带有自定义输入法的输入法扩展来替换iOS的自带输入法。在启用输入法扩展之后，除了受保护的文本区域（例如密码输入区）和手机键盘区（例如联系人中的电话号码区）外，当人们点击任何文本输入区域后就能使用自定义输入法。

**为用户提供明显的方式来切换输入法。**人们对于iOS的输入法切换按钮很熟悉，他们会期望在你的输入法中也有类似的体验。

[![06](https://isux.tencent.com/wp-content/uploads/2014/11/20141123153532931.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123153532931.png)

 

### 3.2 通知（Notifications）

通知为人们提供即时的重要信息和功能。人们能在多种情况下收到通知，例如在锁屏界面中，或者在使用应用时，或者访问通知中心时。

通知中心有两种视图：通知（Notifications ）和今天（Today）。

今天视图显示了一组可编辑的部件。今天部件是一个应用扩展，显示了少量及时和重要的信息或功能，这些信息或功能则是由用户所关注的应用所提供。举例来说，日历部件只显示了今天的事件。点击日历部件中的一个事件可以唤起日历应用，并打开该事件，用户接下来可以编辑该事件或管理其他的事件。想要了解更多关于设计今天部件的内容，请参见[今天部件](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/AppExtensions.html#//apple_ref/doc/uid/TP40006556-CH67-SW4)。

[![07](https://isux.tencent.com/wp-content/uploads/2014/11/20141123153709980.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123153709980.png)

通知视图会显示用户感兴趣的应用所发出的最近通知。用户可以在设置（Settings）中来设置是否在通知中心显示该应用的通知。

[![08](https://isux.tencent.com/wp-content/uploads/2014/11/20141123153811991.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123153811991.png)

iOS应用可以使用通知来让人们知道一些有趣的事情是什么时候发生的，例如：

- 收到一条消息
- 事件即将发生
- 有新的数据可下载了
- 某些状态发生了变化

在iOS8及之后的版本中，应用可以定义用户在通知中的操作。例如，用户可以在待办事项应用的通知中就标记该事项已完成，而无需额外打开应用。

iOS定义了两种类型的通知。

- **本地通知（local notification）**由应用安排待发送，最终通过iOS发送到同一设备中，无论该应用当前是否正在后台运行。例如，日历或待办事项应用可以安排一条本地通知来提醒人们一个即将到来的会议或者日期。
- **远程通知（remote notification）**（也称为**推送通知（push notification）**）是由应用的远程服务器通过苹果推送通知服务来发送的，这类通知最终会被推送到所有安装了该应用的设备。例如，一款在线竞技类的游戏，用户可以和其他玩家竞赛的，可以更新所有玩家的最新状态。

注意：应用扩展可能会要求远程通知必须发送到它的容器应用。在这种场景下，容器应用常常会在后台运行来处理通知。想要了解更多关于应用扩展的内容，请参见[应用扩展](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/AppExtensions.html#//apple_ref/doc/uid/TP40006556-CH67-SW1)。

如果当你的应用正在后台运行时收到了本地或远程的通知，你就应该以你的应用所特有的方式将信息传达给你的用户。

为了确保用户能够自定义他们的通知体验，你应该尽可能多地支持以下的通知类型：

- 横幅（Banner）
- 警告框（Alert）
- 小气泡（Badge）
- 声音（Sound）

注意：在iOS8及之后的版本中，你必须对所有你想发送给用户的通知类型进行注册。当你第一次进行注册动作时，用户会遇到一个警告框，他们可以在其中操作来决定允许或拒绝所有来自你的应用的通知。不管用户选择的结果是什么，他们应始终能访问应用的设置来更改此项设置，或者设置他们想要接收的通知类型。

**横幅（banner****）**是一个小而透明的视图，会出现在屏幕顶部并在几秒后消失。用户还可以看到在锁屏当中的横幅以及在通知中心中以通知形式出现的横幅。在横幅中，iOS会显示通知的内容和应用的小图标（欲了解更多关于小图标的内容，请参见 [App Icon](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/AppIcons.html#//apple_ref/doc/uid/TP40006556-CH19-SW1)）。用户点击横幅来隐藏显示并切换到发送通知的应用。

[![09](https://isux.tencent.com/wp-content/uploads/2014/11/20141123154354806.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123154354806.png)

除了默认的点击动作之外，当用户轻扫横幅时,你还可以定义两个动作按钮。点击通知动作按钮来隐藏横幅的显示并启动你的应用（可能是在后台）来执行动作。

[![10](https://isux.tencent.com/wp-content/uploads/2014/11/20141123154438806.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123154438806.png)

通知**警告框**是显示在屏幕上的标准警告框视图，需要用户操作后才会隐藏。当用户点击Options按钮后，你需要提供并显示通知消息以及任何一个默认动作，或最多四个特定动作。警告框的背景样式不能做修改。

[![11](https://isux.tencent.com/wp-content/uploads/2014/11/20141123154452492.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123154452492.png)

当用户点击警告框中的一个默认或自定义动作按钮时，iOS会同时隐藏警告框并运行你的应用（可能是在后台）。点击关闭或确定按钮会隐藏警告框而不打开应用。

[![12](https://isux.tencent.com/wp-content/uploads/2014/11/20141123154503254.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123154503254.png)

**小气泡（badge****）**是一个显示未读通知数量的红色小圆（小气泡显示在应用图标的右上角）。小气泡的大小和颜色不能做修改。

[![13](https://isux.tencent.com/wp-content/uploads/2014/11/20141123154513229.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123154513229.png)

横幅、警告框和小气泡这三种通知都可以使用自定义或系统提供的**声音**。

**在通知中谨慎使用具破坏性的动作。**要确定用户有足够的上下文来避免意想不到的后果。为了帮助用户区分你所定义的破坏性动作，iOS会用红色来显示它。有时候，在应用执行破坏性动作之前，应该请求用户进行确认。举个例子，如果在锁屏的横幅（banner）中提供了一个破坏性动作，那么就应确保只有设备的主人才能执行该动作（你需要在代码上实现这一需求）。

**为每个动作按钮提供自定义标题。**创建一个简短的标题来描述清楚将要发生的动作。例如，游戏可能会使用“Play”作为标题来表明，点击这个按钮会打开应用来进行游戏。确保标题：

- 使用标题样式的大小写（title-style capitalization）
- 足够简短，能不被截断地显示在按钮内（也应确保测试各种语言文字的标题显示正常）

**不要为同一个事件重复发送通知。**用户可以选择处理通知项；通知项在用户未处理前会一直显示。如果为同一事件重复发送通知，通知中心列表中会满是通知，用户就有可能会关闭你的应用的通知。

**不要在通知消息中包含你的应用名称。**自定义信息会在警告框和横幅中显示，也会在通知中心中以通知的形式显示。你无需在自定义信息中显示你的应用名称，因为iOS会在显示信息的同时自动显示应用名称。

为了使本地或远程通知信息更有作用，你应该：

- 专注于信息而不是用户的行为。避免告诉人们点击哪个按钮或如何打开你的应用。
- 足够简短，一两行就可以显示完整。较长的信息对于用户来说很难进行快速阅读，也会造成在警告框中需要滚动才能查看完整。
- 使用句式大小写（sentence-style capitalization），并配以合适的结束语句符号。可能的时候，可以使用一个整句。

注意：如有必要，iOS会缩短你的消息以便能在各种通知发送样式下显示；为了最好的效果，你不应主动缩减你的消息。

**保持小气泡的内容是最新的。**当用户注意到新信息时，即时更新小气泡非常重要，这样用户就不会觉得收到了额外的通知。注意，当小气泡为0时也会移除通知中心中所有对应的通知项。

重要：不要使用小气泡做通知以外的用途。记住，用户能够关闭应用的小气泡，所以你无法确定他们一定能看到小气泡中的内容。

**当收到通知时，提供用户可以选择听到的音效。**当人们没有在看屏幕的时候，可以通过音效获取他们的注意。例如，日历应用可能会在显示警告框的同时播放一个音效来提醒人们一个即将到来的事件。再如，协作任务管理应用可能会在小气泡更新时播放一个音效来告知某个远程协同的同事已经完成了某个任务。

你可以提供自定义的音效，或者使用内置的警告音。如果你创建了自定义音效，请确保它是简短的、有特色的并且是经由专业制作的。（想要了解更多关于音效的技术需求，请参阅[*Local and Remote Notification Programming Guide*](https://developer.apple.com/library/ios/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/Introduction.html#//apple_ref/doc/uid/TP40008194)中的[Preparing Custom Alert Sounds](https://developer.apple.com/library/ios/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/Chapters/IPhoneOSClientImp.html#//apple_ref/doc/uid/TP40008194-CH103-SW6)。）注意，当通知发送后，你无法以编程方式来触发设备的震动，因为用户对于警告框是否伴随震动拥有支配权。

 

### 3.3 多任务处理（Multitasking）

多任务处理让人们可以在最近使用的应用之间进行快速切换。

[![14](https://isux.tencent.com/wp-content/uploads/2014/11/20141123154835612.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123154835612.png)

为了支持这样的体验，多任务处理会让一款应用在用户切换离开后，在后台进入挂起状态。当用户切换回来时，应用可以快速被重新使用，因为应用无需重新加载UI。人们使用多任务处理UI（如上图）来选择一款最近使用的应用。

API注释：想要学习在你的代码中如何支持多任务处理，请参阅*App Programming Guide for iOS*中的[App States and Multitasking](https://developer.apple.com/library/ios/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/BackgroundExecution/BackgroundExecution.html#//apple_ref/doc/uid/TP40007072-CH4)。

能否在多任务处理中处理好取决于能否在设备中与其他应用和谐共存。从更高的层面来说，这意味着所有的应用都应：

- 处理好中断或来自其他应用的声音
- 停止和重启，即快速平滑地从后台切换到前台
- 不在前台时应恪守己任

下述指南细则可以帮助你的应用在多任务处理中取得成功。

**准备好被打断，并恢复。**多任务处理增加了后台应用中断你的应用的可能性。其他特性，诸如广告出现和更快的应用切换，也会造成更频繁地打断。越快速和越精确地保存应用当前状态，人们就可以越快地重新运行应用，并从之前离开的页面继续使用。你可以通过利用UIKit的状态保存和恢复来为用户提供无缝的重新开始的体验（查看State Preservation and Restoration了解更多信息）。

**确保你的UI****可以处理两倍高度的状态栏。**两倍高度的状态栏会在诸如通话、录音和共享等过程中出现。在未作处理的应用中，状态栏的额外高度会引起布局问题，如UI被向下挤压或者被遮住。在多任务处理环境中，使两倍高状态栏显示正常是格外重要的，因为它可能会出现在更多的应用当中。

**准备好暂停需要人们注意或主动参与的活动。**例如，如果你的应用是一款游戏或媒体观看应用，你需要确保你的用户从应用切换走时，不会丢失任何内容或事件。当人们切换回游戏或媒体播放器时，他们希望能继续之前的体验，就好像他们从未离开过应用。

**确保音频行为合适。**当你的应用正在运行时，多任务处理会使得其他媒体活动更可能地同时进行，也会有更多可能性使你的音频不得不暂停，并恢复处理中断。查看[声音](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Sound.html#//apple_ref/doc/uid/TP40006556-CH44-SW1)来帮助你确保你的音频能满足人们的期望，并与设备中的其他音频和平共处。

**适度使用本地通知。**应用可以在特定时间发送本地通知，无论应用是在暂停中还是运行中亦或是根本就没有运行。为了达到最好的用户体验，应避免用过多的通知来骚扰人们，并遵循[通知](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/NotificationCenter.html#//apple_ref/doc/uid/TP40006556-CH39-SW1)中创建通知内容的指南。

**必要时，在后台完成用户的任务。**当人们开始一个任务时，他们通常会期望即使已经从应用中切换走了任务仍能够完成。如果你的应用在执行用户任务途中，并且这个任务不需要额外的用户交互，那么你就应该在应用挂起之前就在后台完成任务。

 

### 3.4 社交媒体（Social Media）

人们会期望在任何场景下都可以使用他们喜爱的社交媒体帐号。iOS以人们喜欢的方式将社交媒体的交互与你的应用进行了整合。

[![15](https://isux.tencent.com/wp-content/uploads/2014/11/20141123154938475.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123154938475.png)

注意：当用户点击动作按钮时，他们会得到一个如上图的动作视图控制器。想要了解更多关于这个视图控制器的内容，请参见[Activity View Controller](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/ContentViews.html#//apple_ref/doc/uid/TP40006556-CH13-SW121)。
动作视图控制器的中间一行显示了用户启用的和系统提供的分享应用扩展。想要了解更多关于设计分享扩展的内容，请参见[Share and Action Extensions](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/AppExtensions.html#//apple_ref/doc/uid/TP40006556-CH67-SW3)。

**考虑在你的应用中为用户提供一种简便的方式来撰写邮件。**用户有可能会启用分享扩展以便能在任何地方都可以发送内容。但是你也可以使用系统提供的撰写视图控制器来呈现给用户，他们可以在其中进行编辑操作。你可以在显示给用户进行编辑之前，预先加载具有自定义内容的撰写视图（在你呈现给用户之后，只有用户可以编辑这些自定义内容）。想要了解更多关于社交框架（Social framework）的编程界面，包括[SLComposeViewController](https://developer.apple.com/library/ios/documentation/NetworkingInternet/Reference/SLComposeViewController_Class/index.html#//apple_ref/occ/cl/SLComposeViewController)类，请参见[*Social Framework Reference*](https://developer.apple.com/library/ios/documentation/Social/Reference/Social_Framework/index.html#//apple_ref/doc/uid/TP40012233)。

**可能时，避免要求用户登录进入一个社交媒体账户。**社交框架（Social framework）会和帐号框架（Accounts framework）一起来支持一个单点登录模式，所以你可以获得授权来访问用户的帐号，而无需要求他们来重新授权。如果用户还没有登录进入一个帐号，你可以显示UI来让他们进行登录。

 

### 3.5 iCloud

iCloud可以让用户随时随地用不同的设备访问他们想要的内容。将iCloud集成到应用中，用户不用进行同步操作就可以在不同场景下使用不同的设备访问并编辑私人信息。

[![16](https://isux.tencent.com/wp-content/uploads/2014/11/2014112315500873-590x514.png)](https://isux.tencent.com/wp-content/uploads/2014/11/2014112315500873.png)

为了提供这种体验，你可能需要重新检查你的应用中现有的信息，尤其是用户自建内容的存储、访问和展示方式。想要学习如何使用iCloud，请参考[iCloud Design Guide](https://developer.apple.com/library/ios/documentation/General/Conceptual/iCloudDesignGuide/Chapters/Introduction.html)。

iCloud用户体验的一个基本方向是透明性：理想情况下，用户不需要知道他们的信息存储在什么地方，也不需要去思考当前浏览的信息是哪个版本的。以下几点可以帮助你创建用户期望的iCloud体验。

**如果可以的话，让用户方便地启用iCloud。**在iOS设备上，用户可以在设置中登录iCloud账户，因此多半用户会期望应用可以自动启用iCloud。但是如果你觉得用户可能需要自主选择是否使用你应用的云服务，你可以在用户第一次进入应用时提供一个简单的选项来进行设置。大多数情况下，这个选项应该为：是否将所有内容上传到云端。

**注意用户iCloud空间大小。**一定要记住iCloud空间是用户花钱买来的有限资源。你应该使用iCloud来存储用户自己创建和可理解的信息，避免将可再生的应用资源和内容存储在云端。同样要记住，当用户登录了iCloud账户时，你的应用的文件夹内容也会自动备份到云端。所以为了节省用户云端空间，你最好只挑选必要的信息存储于文件夹中。

**避免让用户自己选择在iCloud上存储哪些文件。**一般，用户会期望他们在意的所有信息都能够通过iCloud访问到。为了提供更好的用户体验，你可能想要重新构建处理和展示内容的方式，这样就可以给用户提供更多的文件管理功能。但实际上大多数用户都不需要进行个人文件存储的管理，所以你的应用也可以不用考虑这个问题。

**决定哪种类型的信息需要存储在云端。**除了存储用户自建的文件和内容，你还可以存储少量的其他信息在云端，例如用户当前的状态，用户的偏好设置等等。你可以使用iCloud的关键值存储来保存这类信息。例如，用户使用你的应用看了一个杂志，你可以使用iCloud的关键值存储来保存用户浏览到的位置，这样用户在别的设备上重新打开这个杂志时就能从上次离开的地方继续浏览了。

如果你使用iCloud的关键值存储来保存用户的偏好设置，确保用户在每个设备上都是想这样设置的。例如，有些偏好设置在工作环境中比在家里要更好用。在某些情况下，将偏好设置保存在应用服务器上要比保存在云端更合理，这样偏好设置就不会受iCloud的限制。

**确保iCloud无法使用时应用的行为是合理的。**例如，用户退出iCloud账户，关闭应用的iCloud或者进入飞行模式时，iCloud都是无法使用的。在这些情况下，用户都进行了某些操作来禁止iCloud服务，所以你的应用可以不用再进行提醒。但是，需要告诉用户在打开iCloud之前，当前做的修改在其他设备上都无法看到。

**避免给用户创建本地文件的选项。**不管你的应用是否支持iCloud，都不应该给用户提供因设备而区分的文件系统。相反，你应该希望用户关注通过iCloud访问文件的普适性。

**在合适的时候自动更新信息。**最好不需要用户来确认他们正在访问的是最新的内容。但是，也需要在用户设备存储空间和带宽限制之间做出平衡。如果你的用户要使用非常大的文件，那么让他们自己选择是否要从云端下载一个更新的文件可能更合适。如果需要这样做的话，可以设计一种方式来指出当前在云端有一个该文件的最新版本。当用户选择更新时，如果下载时间较长最好给用户明显的反馈。

**告知用户删除某文件的后果。**当用户从有iCloud服务的应用上删除文件的时候，这个文件同样会从用户的iCloud账号和其他设备上删除。所以最好在执行删除操作之前告知用户删除的后果，让用户进行确认。

**必要时尽可能早地告知用户冲突问题。**使用iCloud编程接口，你需要在不打扰到用户的情况下解决大多数不同版本之间的冲突问题。但在有些情况下，你需要尽可能早地检测出冲突问题来避免用户在错误版本上浪费太多时间。你需要设计一种自然的方式来告诉用户有冲突存在，接着给用户提供方便的方式来区分不同版本以及做出决策。

**确保在搜索中包括用户在云端的信息。**使用iCloud的用户趋向于认为云端的信息是普遍可访问的，所以他们会期望搜索结果中也有云端的信息。如果你的应用允许用户搜索他们的信息，确保你使用了将搜索扩展到iCloud账户的接口。

 

### 3.6 电子卡包（Passbook）

Passbook应用是帮助用户查看和管理各种数字化票券的，例如登机证、优惠券、会员卡和各种票。你可以在应用中创建一个票券，向用户描述它，并且在有更改时进行更新。

[![17](https://isux.tencent.com/wp-content/uploads/2014/11/20141123155258815.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123155258815.png)

使用PassKit框架可以方便地用自定义内容来收集一个票券到用户票券库中并访问它。（想要学习Passbook技术的核心概念和PassKit接口的使用方法，请参考[Passbook Programming Guide](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/PassKit_PG/Chapters/Introduction.html#//apple_ref/doc/uid/TP40012195)。）以下几点可以帮助你创建一个用户乐意保留并使用的票券。

**不要只是简单复制已有的物理票券。**Passbook已经建立了有美感的设计，票券也都配合这种设计以看起来更好。所以不要只是复制物理票券的外观，抓住这次机会设计一个符合Passbook组成和功能的干净简洁的票券样式。

**对放在票券正面的信息精挑细选。**用户期望扫一眼票券就能快速获得他们需要的信息，所以票券正面的信息应该是整洁且易读的。如果有用户可能会需要的额外信息，将它们放到票券的背面要比挤在正面好得多。

**通常情况下，避免使用纯白色背景。**通常，一个好看的票券应该使用鲜艳的纯色背景或者使用强烈的，充满活力的图片作为背景。当然，在设计背景时还要确保内容的可读性。

注意：最好在票券的合适区域展示所有的文本内容，并且避免将文本嵌入图片或使用自定义的字体。这样做有两个好处：它方便使用VoiceOver的用户获得票券中的所有信息并且可以使你的票券有一致的外观。（译者注：VoiceOver是一种帮助视障人士的语音辅助程序。）

**在商标文本区域显示你的公司名称。**所有票券的商标文本区域的文字都使用了统一的字体。为了避免和其他票券发生冲突，还是建议您在商标文本区域输入文字，不要使用自定义字体。

**使用单色的公司商标。**商标图片放置在票券左上角公司名称的旁边。最好提供一个单色的，不包含文字的商标。如果你想要增强商标的效果，又想要与文字风格匹配的话，可以增加一个在y轴方向上有1像素偏移，有1像素模糊和透明度为35%的黑色阴影效果。

**如果可以的话，使用长方形的条形码。**类似于PDF417这样的长方形条形码比正方形二维码更适合票券的布局。如下右图所示，正方形的二维码会使两边有空白区域并且会在垂直方向上使上下方内容变得拥挤。

[![18](https://isux.tencent.com/wp-content/uploads/2014/11/20141123155934270.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123155934270.png)

**为性能优化图片。**因为用户通常会通过电子邮件或者浏览器接收票券，所以下载的越快越好。为了提高用户体验，使用能满足视觉效果的最小的图片文件。

**在合适的时候更新票券以增强其效用。**即使一个票券代表的物理实体并不会改变，数字的票券也可以通过映射真实世界的一些事件来提供更好的用户体验。例如，当某个航班延误时你可以更新登机牌上的信息，这样用户就能够通过查看电子登机牌来获得当前的信息了。

 

### 3.7 应用内购买服务（In-App Purchase）

应用内购买服务使用户可以在你的应用、你设计的商店中购买数字产品。

[![19](https://isux.tencent.com/wp-content/uploads/2014/11/20141123160047661.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123160047661.png)

例如，用户可能：

- 将一个应用从基础版升级到高级版
- 每月订阅新内容
- 购买虚拟商品，例如游戏中的等级或道具
- 购买并下载新书

重要：应用内购买服务只提供支付功能，其他功能由你自己提供，例如向用户展示商品，解锁内置功能，从你自己的服务器上下载内容等等。当然，你所提供的所有商品都必须在应用商店注册过。

想要了解添加购买功能的技术问题，请查看[In-App Purchase Programming Guide](https://developer.apple.com/library/ios/documentation/NetworkingInternet/Conceptual/StoreKitGuide/Introduction.html#//apple_ref/doc/uid/TP40008267)。想要了解应用内购买的商业问题，请查看[App Store Resource Center](https://developer.apple.com/app-store/)。当然，你还应该查看许可协议来确定你的应用出售哪些商品以及如何提供商品。

你可以使用StoreKit框架在你的应用中嵌入一个商店并且支持应用内购买服务。当用户进行购买时，StoreKit连接到应用商店进行安全支付，然后再告知你的应用来提供购已购买的商品。

以下几点可以帮助你设计用户喜欢的购买体验。

**将商店体验集成到你的应用中。**在展示商品和处理用户交易时，给用户提供一致性的体验。你一定不想让用户在访问你的商店时感觉进入了另一个不同的应用。

**使用简短简洁的标题和说明。**最好能让用户在扫过一组条目时快速发现感兴趣的内容。用户更容易理解不需要截断隐藏的简单直接的语言和标题。

**不要替换默认的确认提醒框。**当用户购买一个商品时，StoreKit会提供一个确认提醒框（上方有展示）。这个提醒框可以帮助用户避免意外购买，所以不要修改它。

 

### 3.8 游戏中心（Game Center）

游戏中心给用户提供玩游戏，组织在线多人游戏以及其他更多的功能。玩家可以使用内置的游戏中心应用来注册一个账户，发现新游戏，添加好友，浏览玩家排名和战绩成就。

[![20](https://isux.tencent.com/wp-content/uploads/2014/11/20141123160119594-590x1010.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123160119594.png)

作为一个游戏开发商，你可以使用GameKit接口发送分数和战绩到游戏中心的服务器上，在你的游戏页面中显示玩家排名，帮助用户找到其他玩家。想要学习如何将游戏中心集成到你的应用中，请查看[Game Center Programming Guide](https://developer.apple.com/library/ios/documentation/NetworkingInternet/Conceptual/GameKit_Guide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40008304)。

以下几点可以帮助你给用户提供好的游戏中心体验。

**不要使用自定义的界面来提示用户登录到游戏中心。**如果用户在未登录到游戏中心的情况下打开了一个需要启用游戏中心的应用，系统会自动提醒他们登录。所以自定义登录界面没有存在的必要，而且有可能使用户感到困惑。

**一般情况下，使用标准的游戏中心界面。**在少数情况下，可能有必要自定义游戏中心的界面，但是这样做有使用户感到疑惑的风险。标准游戏界面是iOS和OS X用户熟悉的，而且它会给用户一种置身于一个大的游戏社区的感觉。

**给用户提供关闭语音聊天的途径。**有些用户可能不想在进入游戏时自动开启语音聊天功能，而且大多数用户希望在特定情境下可以关闭语音聊天。

 

### 3.9 iAd富媒体广告（iAd Rich Media Ads）

如果你允许你的应用中出现广告，那么你就可以通过用户浏览或者点击广告获得收益。（这里是一个放置iAd横幅(banner)的简单示例。）

[![21](https://isux.tencent.com/wp-content/uploads/2014/11/20141123160835738.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123160835738.png)

iAd网络提供的广告都会有一个确定的样式。最简单的，这种样式可以是一个作为入口的横幅广告。当用户点击这个横幅时，广告执行预排程序的动作，例如播放一段影片，展示可交互的内容或者启动浏览器打开一个页面。这个动作展示的内容会盖住你当前的界面，或者使你的应用转换到后台运行。

有三种类型的横幅：标准（standard），中等矩形（medium rectangle）和全屏（full screen）。所有类型的横幅都提供同样的功能，就是引导用户进入广告，只是它们的外观和行为不同。

**标准横幅（standard banner）**占用屏幕较少的空间，通常从始至终都可见。你可以选择在应用的哪些页面显示标准横幅，并且在这些页面布局时给横幅留出空间。

[![22](https://isux.tencent.com/wp-content/uploads/2014/11/20141123160936969.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123160936969.png)

所有的iOS应用都可以展示标准横幅。你可以使用[ADBannerView](https://developer.apple.com/library/ios/documentation/userexperience/Reference/ADBannerView_Ref/index.html#//apple_ref/occ/cl/ADBannerView)类中的视图来显示标准横幅。

**中等矩形横幅（medium rectangle banner）**的行为和标准横幅相同，同样也可以选择展示中等矩形横幅的位置。

[![23](https://isux.tencent.com/wp-content/uploads/2014/11/20141123161032562-590x766.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123161032562.png)

中等矩形横幅只能在iPad应用中使用。你可以使用[ADBannerView](https://developer.apple.com/library/ios/documentation/userexperience/Reference/ADBannerView_Ref/index.html#//apple_ref/occ/cl/ADBannerView)类中的视图来显示中等矩形横幅。

**全屏横幅（full screen banner）**会占用屏幕的大部分甚至是所有空间，并且通常只在应用程序流的特定时间或特定位置显示。你可以选择使用模态显示横幅或者用独立的页面来展示可滚动的内容。（在下面的示例中，应用提供了一种杂志阅读的体验，通过翻页离开或回到全屏广告页面。）

[![24](https://isux.tencent.com/wp-content/uploads/2014/11/20141123161058261-590x752.png)](https://isux.tencent.com/wp-content/uploads/2014/11/20141123161058261.png)

你可以使用[ADInterstitialAd](https://developer.apple.com/library/ios/documentation/iAd/Reference/ADInterstitialAd_Ref/index.html#//apple_ref/occ/cl/ADInterstitialAd)类中的视图来显示全屏横幅。

iAd框架包含了所有类型的横幅，并且会在右下角显示iAd的标识。iAd框架的设计固定在屏幕底部时最好看。

为了保证无缝的集成和提供最好的用户体验，可以遵循以下几点。

**将标准横幅尽量放置在屏幕底部或底部附近。**这个位置的差别取决于底部是否有栏（bar）以及是什么样的栏。

| **栏**                         | **标准横幅的位置** |
| ----------------------------- | ----------- |
| 屏幕底部没有栏                       | 屏幕底部        |
| 屏幕任何地方都没有栏                    | 屏幕底部        |
| 底部有工具栏（toolbar）或者选项卡（tab bar） | 底部栏上方       |

**将中等矩形横幅放置在不会干扰内容的地方。**和标准横幅一样，中等矩形横幅也最好放置在屏幕底部或底部附近。放在底部附近也能减少干扰用户的可能性。

**用户体验中有中断时使用模态展示全屏横幅。**如果你的应用中有自然中断或者情景转换，模态展示的风格会更合适。当你模态展示全屏横幅时（通过使用[presentFromViewController](https://developer.apple.com/library/ios/documentation/iAd/Reference/ADInterstitialAd_Ref/index.html#//apple_ref/occ/instm/ADInterstitialAd/presentFromViewController:)实现）用户要么进入广告，要么关闭它。出于这个原因，当用户有做出转变的预期时（例如完成了一个任务后）用模态展示形式比较好。

**应用视图中有转场切换时不要使用模态展示全屏横幅。**如果用户在使用你的应用时会频繁的进行屏幕切换操作，例如杂志翻页或翻阅一些条目集合，此时使用非模态的形式会更合适。当你使用非模态来显示全屏横幅时（通过使用[presentInView](https://developer.apple.com/library/ios/documentation/iAd/Reference/ADInterstitialAd_Ref/index.html#//apple_ref/occ/instm/ADInterstitialAd/presentInView:)实现），可以在界面中保留栏（bar）让用户通过应用控件进入或退出广告。和其他横幅广告一样，点击全屏横幅会启动iAd体验，但是如果条件允许，你也可以在应用中支持横幅内的其他手势操作（例如拖动或滑动）。

确保使用合适的动画效果来显示和隐藏非模态的全屏横幅视图。例如，杂志阅读应用可以用和杂志翻页一样的动画效果。

**确保横幅在应用中出现的时间和位置的合理性。**用户只有在不觉得广告打扰了他们时才可能进入iAd。这点对于游戏这样的沉浸式应用尤其重要：你肯定不想将横幅放置在影响用户玩游戏的位置。

**避免将横幅放置在用户只一扫而过的页面。**最好不要将横幅放置在用户会快速略过的页面。因为通常用户在一个页面停留1、2秒后才可能点击一个广告。

**尽可能的支持双向展示横幅广告。**最好让用户在使用应用时不必旋转设备就能浏览广告。当然，支持双向也能给你的广告提供更大的区域。想要学习如何确保转换方向时横幅能正常响应，请查看[iAd Programming Guide](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/iAd_Guide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40009881)。

**不要让标准或中等矩形横幅滚出屏幕。**如果你的应用需要滚动来展示内容，确保横幅一直固定在它的位置上。

**当用户浏览广告或与广告进行交互时，暂停那些吸引用户注意力或需要操作的活动。**当用户选择浏览广告时，他们不想因此错过应用中的事件，也同样不想让应用打断广告体验。一个好的方法是像应用转入后台运行那样暂停当前活动。

**除非有特殊情况，否则不要中断广告。**一般情况下，在用户浏览并与广告交互时，应用还是在继续运行并接收事件的，所以也有可能突然出现一个事件需要获得用户的注意力。然而，需要打断广告的场景其实非常少。有一种情形是应用提供互联网语音协议服务（VoIP）。在这种应用中，有电话接入时可能会取消正在运行的广告。

### 3.10 无线打印（AirPrint）

用户可以通过AirPrint无线打印应用中的内容，还可以使用打印中心应用检查打印任务。

[![01](https://isux.tencent.com/wp-content/uploads/2014/12/20141207165105835.png)](https://isux.tencent.com/wp-content/uploads/2014/12/20141207165105835.png)

你可以使用内置的支持程序来打印图片和PDF文件，或者可以使用特定的打印程序接口来做自定义的格式设置和渲染设置。iOS会处理打印机的发现，任务的排序以及在指定打印机上执行打印任务。

通常来讲，用户想要打印文件的时候，只需要点击应用中的标准动作按钮（Action button）。当他们选择了要打印的条目后，可以选择打印机，设置打印属性，最后点击打印按钮开始打印。

打印中心应用是一个只有在处理打印任务时才可见的后台系统应用，用户可以用它来查看打印任务。用户可以在打印中心浏览当前打印队列，查看某个打印任务的详情，还可以取消某个任务。

只需添加少量代码就可以支持基本打印功能（想要学习在代码中添加打印功能，请查看[Drawing and Printing Guide for iOS](https://developer.apple.com/library/ios/documentation/2DDrawing/Conceptual/DrawingPrintingiOS/Introduction/Introduction.html#//apple_ref/doc/uid/TP40010156)）。想要确保好的打印体验，可以遵循以下几点：

**使用系统提供的动作按钮。**用户对系统提供的按钮的含义和行为都很熟悉，所以尽可能的使用系统动作按钮。如果你的应用没有工具栏或导航栏，那就要另当别论了。在这种情况下，你就需要自己设计一个可以出现在应用主界面的打印按钮，因为动作按钮只能在工具栏和导航栏中使用。

**在当前情境下打印操作是基本功能时才显示打印项（Print item）。**如果当前情境并不适合打印，或者用户并不想打印，就不要将打印项显示出来。

**在合适的时候给用户提供更多打印选项。**例如，让用户设置打印页码范围或打印份数。

**如果用户不能打印，则不要显示特定的打印页面。**在向用户展示有打印项的界面前，确保用户的设备是支持打印的。学习如何在代码中实现，请查看[UIPrintInteractionController Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIPrintInteractionController_Class/index.html#//apple_ref/doc/uid/TP40010141)。

### 3.11 访问用户数据（Accessing User Data）

位置服务允许应用获取用户当前大致的地理位置，设备指向的方向以及用户移动的方向。其他系统服务，例如通讯录、日历、备忘录和相册等，同样也允许应用访问用户存储在里面的数据。

[![02](https://isux.tencent.com/wp-content/uploads/2014/12/20141207165153169.png)](https://isux.tencent.com/wp-content/uploads/2014/12/20141207165153169.png)

虽然获取了用户数据的应用能带来一定的方便，但还是需要为用户提供维持信息私密性的功能。例如，用户喜欢应用自动给内容加上位置标签，或者可以找到附近的好友，但用户也需要能在不想分享位置的时候关闭这些功能。（想要学习如何给应用增加获取位置功能，请查看[Location and Maps Programming Guide](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/LocationAwarenessPG/Introduction/Introduction.html#//apple_ref/doc/uid/TP40009497)。）

以下几点可以帮助您以用户不反感的方式获取用户数据。

**确保使用户理解分享私人数据的原因。**如果没有明显的需要，用户自然会对私人信息的请求感到怀疑。为了避免用户反感，确保在用户使用明显需要个人信息的功能时再进行提醒。例如，即使没有打开位置服务用户也可以使用地图，但是在用户使用定位或导航功能时就会有提醒。

**应用需要个人信息的原因不明显时向用户做出解释。**你可以在提醒框中给出文字性的描述，例如“这个应用需要访问你的通讯录”或者“是否允许应用获取你的地理位置？”。这些文案最好明确且有礼貌以让用户无压力的理解为什么需要访问他们的信息。

讲述原因的文案应该：

* 不要包含你的应用名称，因为系统提供的提醒框已经包含了。
* 清楚地描述你的应用为什么需要这些数据。如果可以的话，你也可以解释不会用这些数据做什么。
* 使用以用户为中心的术语并且进行本地化。
* 在易于理解的情况下越短越好。尽可能避免超过一句话。
* 使用句式大小写（sentence-style capitalization）。（句式大小写指的是第一个单词大写，除了专有名词和专有形容词以外的词都小写。）

**只有当你的应用没有用户数据就无法提供基础服务时，才在一开始就征求用户的许可。**如果你的应用在知道了用户私人信息后才能提供主要功能是显而易见的话，用户不会因此觉得烦扰。

**避免在用户选择需要数据的功能之前调用触发提醒框的程序。**这样，就可以避免用户疑惑为什么在使用不需要私人数据的功能时有请求提醒。（注意，检查用户位置服务的设置并不会触发提醒。）

**检查位置服务的设置来避免触发没必要的提醒。**你可以使用核心位置的程序接口来实现（想要学习如何做，请查看[Core Location Framework Reference](https://developer.apple.com/library/ios/documentation/CoreLocation/Reference/CoreLocation_Framework/index.html#//apple_ref/doc/uid/TP40007123)）。使用这些知识，可以尽可能地在使用需要位置信息的功能时才进行提醒，或者完全避免提醒。

### 3.12 快速查看（Quick Look）

使用Quick Look，用户可以在你的应用内预览文件，即使你的应用是打不开这个文件的。例如，你可以允许用户预览一些从网站上下载或从其他来源收到的文件。

[![03](https://isux.tencent.com/wp-content/uploads/2014/12/20141207165317429.png)](https://isux.tencent.com/wp-content/uploads/2014/12/20141207165317429.png)

想要学习如何在应用中加入Quick Look文件预览功能，请查看[Document Interaction Programming Topics for iOS](https://developer.apple.com/library/ios/documentation/FileManagement/Conceptual/DocumentInteraction_TopicsForIOS/Introduction/Introduction.html#//apple_ref/doc/uid/TP40010403)。

用户在应用中预览文件之前，可以在你自定义的视图中查看文件的信息。例如，用户从一封邮件中下载了附件之后，邮件应用（Mail）会在邮件中以自定义的视图展示文件的图标、标题和大小。用户可以通过点击它来预览文件。

[![04](https://isux.tencent.com/wp-content/uploads/2014/12/20141207165348770.png)](https://isux.tencent.com/wp-content/uploads/2014/12/20141207165348770.png)

你可以在应用中用一个新的视图来显示文件预览，使用全屏或者模态视图。展示的形式取决于你的应用运行在什么设备上。

**在iPad上可以使用模态视图显示文件预览。**iPad的大屏幕很适合在一个方便用户离开的沉浸式环境中展示文件预览。缩放操作（zoom transition）很适合显示预览。

**在iPhone上可以使用专用的视图，最好是导航视图来显示文件预览。**这样可以使用户在应用情境中通过导航进入文件预览。虽然也可以在iPhone应用中使用模态显示，但并不推荐这样。（注意缩放操作在iPhone上并不适用。）

当然，在导航视图中显示文件预览可以在导航栏上放置特定的预览控件。（如果你的视图有工具栏，Quick Look会将预览控件放在工具栏上。）

### 3.13 声音（Sound）

无论声音是你的应用的主要内容的一部分，还是锦上添花的元素，你都需要知道用户对声音的期望以及与如何满足这些期望。

### 3.13.1 理解用户期望（Understand User Expectations）

人们可以使用设备控件来改变声音，也可能使用有线或无线的耳机和听筒。人们也会对于他们的行为如何作用于他们听到的声音有各种各样的期望。虽然你可能发现有一些期望很让人意外，但它们都会遵循用户控制的原则，即应是用户而非设备掌控听到声音的时机。

**用户会依据需要将设备静音：**

* 避免被突兀的音效打断，比如手机铃声和信息接收音等
* 避免听到作为用户操作副产品的音效，比如键盘或其他反馈音、偶然的声音或应用启动的声音
* 避免听到那些玩游戏时不必要出现的声音，如音效和配乐

例如，在剧院中，用户将他们的设备调至静音以避免打扰剧院中的其他人。在这一情境下，用户仍然希望能在他们的设备上使用应用，但他们不希望被无预期或突兀的声音所打断，如手机铃声或新消息音。

在用户进行单纯操作和有明确期望的操作时，铃音/静音开关（或静音开关）不会屏蔽这些操作所导致的的声音。例如：

* 独立媒体应用中的媒体播放是不会被静音的，因为媒体播放是用户明确要求的。
* 闹钟不能被静音，因为闹钟是用户明确设置的。
* 语言学习应用中的音效素材不能被静音，因为用户进行了明确的操作希望听到它。
* 音频对话应用中的对话不被静音，因为用户打开这个应用的唯一目的就是进行音频对话。

**用户使用设备的音量键调整所有音效的音量**，包括歌曲、应用音效和设备声音。用户能使用音量按钮屏蔽所有声音，无论铃声/静音（或静音）的开关在什么位置。使用音量键调整应用当前所播放的音频时同样调整了全局系统的音量，只有铃声音量除外。

对于iPhone：当没有音频播放时使用音量键可以调整铃声音量。

**用户使用耳机可以私密地接听声音并解放他们的双手。**不管这些配件是有线或无线的，用户都对用户体验有特定的期待。

当用户插入耳机或连接无线音频设备时，他们意图继续收听当前的音频，但是是以私密的状态。由于这一原因，他们希望当前正在播放音频的应用能继续不中断地播放。

当用户拔出耳机或断开与无线设备的连接时（抑或设备超出范围或关闭时），他们不希望他们刚刚收听的内容被自动地与他人分享。基于这一原因，他们希望正在播放音频的应用暂停播放，并可以允许他们在愿意时能容易地重新开启播放。

### 3.13.2 定义应用的音频行为（Define the Audio Behavior of Your App）

**如果必要的话，你可以调整相关的、独立的音量水平以在你的应用音效输出端制造出最好的混音。**但是，最终音效输出的音量也应该能被系统音量所控制，无论是通过音量键还是音量滑条进行调节。这意味着应用的音频输出的控制权仍在它所属的用户手中。

**确保你的应用适时的显示音频路径选择。**（音频路径（audio route）是指音频信号的电子通路，例如源于设备的耳机或是设备的扬声器。）即使人们没有物理性的插入或拔出音频设备，他们也仍希望能选择一个不同的音频路径。为了实现这一功能，iOS能自动显示一个控件来允许用户选择一个输出音频路径（使用[MPVolumeView](https://developer.apple.com/library/ios/documentation/MediaPlayer/Reference/MPVolumeView_Class/index.html#//apple_ref/occ/cl/MPVolumeView)类能允许这个控件显示在你的应用中）。由于选择不同的音频路径是用户主动的行为，用户期望当前播放的音频能继续不中断。

**如果你需要显示音量滑条**并使用[MPVolumeView](https://developer.apple.com/library/ios/documentation/MediaPlayer/Reference/MPVolumeView_Class/index.html#//apple_ref/occ/cl/MPVolumeView)类时，确保使用系统原生的音量滑条以保证可用。要注意，当激活的音频输出设备不支持音量控制时，要使用合适的设备名称来替代音量滑条。

**如果你的应用只产生一些与其功能无必要关系的界面音效时，（尽量）使用系统音效服务（**System Sound Services**）。**系统音效服务是iOS系统下产生警示音、界面音效和调用振动的技术；它不适合任何其他用途。当你使用系统音效服务来产生音效时，你无法干涉你的音频与设备的音频的交互方式，也无法干涉设备配置变化和干扰的响应方式。如想了解如何使用这一技术，参阅_[Audio UI Sounds (SysSound)](https://developer.apple.com/library/ios/samplecode/SysSound/Introduction/Intro.html#//apple_ref/doc/uid/DTS40008018)_中的范例项目。

**如果音效在你的应用中扮演重要的角色，使用音频会话服务（**Audio Session Services**）**或是[AVAudioSession](https://developer.apple.com/library/ios/documentation/AVFoundation/Reference/AVAudioSession_ClassReference/index.html#//apple_ref/occ/cl/AVAudioSession)类。这些程序接口不产生音效；相反，它们会帮助你了解你的音频应该如何与设备的音频进行交互以及如何响应设备配置的干扰与变化。

对于iPhone：无论你使用什么样的技术来制作音频，无论你如何定义来它的行为，手机总是可以中断当前运行的应用。这是因为任何应用都不应该阻止人们接收来电。

在音频会话服务中，**音频会话（**audio session**）**执行了你的应用与系统之间音频中介的功能。音频会话中最重要的方面之一就是**类目（**category**）**，它定义了你的应用的音频行为。

为了实现音频会话服务带来的好处并能提供用户期望的音频体验，你需要选择可以完美描述应用音频行为的类目。具体情况取决于你的应用只在前台播放音频还是也要在后台播放音频。在你做这一选择的时候，遵循以下这些原则：

* **依据其语义而非精确的行为来选择音频会话类目。**通过选择目的清晰的类目，你可以确保你的应用能表现得符合用户期望。除此之外，当以后行为的精确集合被重新定义时，它可以为你的应用提供最佳的机会使其合理运行。
* **在极少数情况下，可以添加属性到音频会话中以修正一个类别的标准行为。**一个类别的标准行为代表多数用户的期望，因此在你改变那个行为之前你应该仔细地考虑。例如，你可能要添加“闪避”属性以确保你的音频声音能比其他所有的音频都大（除了手机音频），如果你的用户对你的应用是如此期望的话。（欲了解更多关于音频会话属性的内容， 请参见_[Audio Session Programming Guide](https://developer.apple.com/library/ios/documentation/Audio/Conceptual/AudioSessionProgrammingGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40007875)_中的[Fine-Tuning the Category](https://developer.apple.com/library/ios/documentation/Audio/Conceptual/AudioSessionProgrammingGuide/AudioSessionBasics/AudioSessionBasics.html#//apple_ref/doc/uid/TP40007875-CH3-SW2)章节。）
* **依据设备当前的音频环境来考虑你的类目选择。**这也许意味着，例如，用户在使用你的应用时可能听着其它的音效而非你的配乐。如果你这样做，要确保避免当你的应用启动时，迫使用户停止收听当前的内容或要需要额外地在两者之间做出选择。
* **通常来说，要避免在你的应用运行时改变类目。**改变类目的首要依据是你的应用是否需要在不同的时机支持记录和播放。在这种情况下，更好的选择是依据需要在录音类目与播放类目之间转换，而非选择播放和录音类目。这是因为选择录音类目可以确保正在录音时不会听到警告音，比如来信提示音。

表31-1列举了你可以使用的音频会话类目。不同的类目可以允许通过铃声/静音开关或静音开关（或设备锁）来实现静音、与其他的音频混合或者控制应用在后台播放。（欲了解编程界面上所呈现的的类目和属性的准确名称，参见_[Audio Session Programming Guide](https://developer.apple.com/library/ios/documentation/Audio/Conceptual/AudioSessionProgrammingGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40007875)_。）

表31-1 音频会话类目及其相关行为

| col 1  | col 2                 | col 3  | col 4                       | col 5    |
| ------ | --------------------- | ------ | --------------------------- | -------- |
| **类目** | **意义**                | **静音** | **混合**                      | **后台播放** |
| 个人环境   | 声音增强了应用的功能且应该静音其他音频   | 支持     | 不支持                         | 不支持      |
| 环境     | 声音增强了应用的功能且应该静音其他音频。  | 支持     | 支持                          | 不支持      |
| 播放     | 声音对应用来说很重要且可能与其他音频混合。 | 不支持    | 不支持                         | 支持       |
| 录音     | 音频是用户记录的。             | 不支持    | 不支持（默认）支持（当“与其他音频混合”属性被添加时） | 支持       |
| 播放和录音  | 声音代表音频输入与输出，可以按顺序或同时。 | 不支持    | 不支持（默认）支持（当“与其他音频混合”属性被添加时） | 支持       |
| 音频处理   | 应用执行硬件辅助音频编码（不播放或录音）。 | 不适用    | 不支持                         | 支持       |

\*如果你选择音频处理类目并且你希望在后台运行音频进程，你需要在完成音频处理之前防止你的应用被暂停。欲了解如何实现这一功能，参见_[《iOS应用编程指南》](https://developer.apple.com/library/ios/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40007072)_中的执行长时间运行的后台任务。

以下是一些示例情境，其中指示了如何选择音频会话类目以提供用户喜欢的音频体验。

**情境1：一个帮助人们学习新语言的教育类应用****。**你需要提供：

* 用户点击特定控件时播放反馈音效
* 当用户想听到正确发音的示例时播放字词的记录

在这个应用中，声音对于主要功能是十分重要的。人们使用这个应用来听他们正学习的语言的词语与短语，因此即使当设备锁定或者被调至静音时也要能播放声音。因为用户需要清晰地听到声音，他们会期望其他他们可能播放的音频都被静音。

为了满足用户对于该应用所期望的音频体验，你应该使用播放（Playback ）类目。虽然这一类目可以被定义为与其他音频混合，但该应用应该使用默认的行为以确保其他的音频不会干扰那些用户明确选择听到的教育性内容。

**场景2：网络电话应用。**你需要提供：

* 接收音频输入的能力
* 播放音频的能力

在该应用中，声音对于主要功能是十分重要的。人们经常会在使用另一个应用时使用该应用与他人进行交流。用户期望能在他们将设备调至静音或设备被锁定时接听电话，他们希望在来电期间其他音频被静音。他们也希望应用在后台运行时也能继续打电话。

为了满足用户对于该应用所期望的音频体验，你应该使用播放和录音（Play and Record）类目，并且你要确保只有在你需要时才会激活你的音频会话，以便用户可以在打电话过程中使用其他音频。

**场景3：允许用户通过不同任务引导角色的游戏。**你需要提供：

* 不同的游戏运行音效
* 配乐

在该应用中，声音会在很大程度上提升用户体验，但对于主任务并没有那么重要。而且，用户可能会希望能在玩游戏时静音或听他们乐单中的歌曲而不听游戏配乐。

最好的策略是在你的应用启动时确定用户是否在收听其他音频。不要要求用户选择他们是要收听其他音频或是你的音效。而应该使用音频会话功能中的[AudioSessionGetProperty](https://developer.apple.com/library/ios/documentation/AudioToolbox/Reference/AudioSessionServicesReference/index.html#//apple_ref/c/func/AudioSessionGetProperty)来询问[kAudioSessionProperty_OtherAudioIsPlaying](https://developer.apple.com/library/ios/documentation/AudioToolbox/Reference/AudioSessionServicesReference/index.html#//apple_ref/c/econst/kAudioSessionProperty_OtherAudioIsPlaying)属性的状态。依据所询问的答案，你可以选择环境（Ambient）或是个人环境（Solo Ambient）类目（这两种类允许用户静音玩游戏）：

* 如果用户正在听其他音频，你应该假设他们想要继续听并且不想被强迫收听游戏音效。在这种情境下，你最好选择环境（Ambient）类目。
* 如果用户在你的应用启动时没有在收听其他音效，你最好选择个人环境（Solo Ambient）类目。

**情境4：一个为用户到达目的地提供准确、实时导航指示的应用。**你需要提供：

* 每一步旅途的语音指示
* 一些反馈音效
* 支持用户继续收听他们自己的音频的能力

在该应用中，无论应用是否是在后台运行，语音导航指示都表现为主要任务。基于这一原因，你最好使用播放（Playback）类目，它允许你的音频在设备被锁定、静音或是在后台运行时仍可以播放。

你可以通过添加[kAudioSessionProperty_OverrideCategoryMixWithOthers](https://developer.apple.com/library/ios/documentation/AudioToolbox/Reference/AudioSessionServicesReference/index.html#//apple_ref/c/econst/kAudioSessionProperty_OverrideCategoryMixWithOthers)属性来实现允许人们在使用你的应用时收听其他音频。但是你也想要确保用户在他们正在播放其他音频时能听到语音提示。你可以为音频会话添加[kAudioSessionProperty_OtherMixableAudioShouldDuck](https://developer.apple.com/library/ios/documentation/AudioToolbox/Reference/AudioSessionServicesReference/index.html#//apple_ref/c/econst/kAudioSessionProperty_OtherMixableAudioShouldDuck)属性来确保你的音频比其他音频的声音更大，除了iPhone上的电话以外。这些设置允许应用在后台运行时也可以恢复音频会话，可以确保用户能获得实时更新的导航。

**情境5：一个允许用户上传文本和图片到网站上的博客应用。**你需要提供：

* 简短的启动音效文件
* 用以补充用户行为的各式各样的短音效（例如当邮件被上传后播放的音效）
* 发送失败播放的警示音

在该应用中，声音提升了用户体验，但也不是必需的。主任务与音频并没有关系，用户也不是必须要通过收听声音来成功使用应用。在这一情境中，你最好使用系统声音服务来产生声音。这是因为应用中所有声音的音频情境都应符合本技术的目的，这意味着要遵循用户意愿制造服从于设备锁定和铃声/静音（或静音）开关的界面音效和警示音。

### 3.13.3 管理音频中断（Manage Audio Interruptions）

有时候，当前播放的音频会被来自于不同应用的音频所打断。例如，在iPhone上，来电会持续中断当前应用的音频。在多任务情境中，这种音频中断的频率会很高。

为了提供用户喜欢的音频体验，iOS系统依赖于你来：

* 识别可能会引起应用中断的音频类型
* 当应用在音频中断结束后继续运行时进行合理地反馈

每个应用需要识别会引起音频中断的类型，但不是每个应用都需要决定如何在音频中断结束后进行反馈。这是因为多数类型的应用应在音频中断结束后恢复音频。只有那些主要或部分（即那些提供媒体播放控制的应用）的媒体播放应用，才必须才用额外的步骤来决定合适的反馈。

从概念上讲，基于中断音频与中断结束后用户所期望的特别的应用反馈，有两种类型的音频中断：

* **可恢复性中断是（**resumable interruption**）**被一些音频引起的，那些音频被用户视为他们主要听觉体验的的插曲。在可恢复性中断结束后，显示媒体播放控件的应用应该恢复它被中断前的任务，无论是在播放音频还是保持暂停。没有音频播放控件的应用则应该恢复播放音频。例如，试想用户在iPhone上使用应用播放音乐时，电话在歌曲的中间接入。用户接起了电话，期望在他们通话时播放的应用能静音。在通话结束后，用户希望播放的应用自动恢复播放歌曲，因为音乐而非电话才是他们的主要听觉体验，而他们在电话接入前也没有暂停音乐。另一方面，如果用户在电话接入前暂停了音乐播放，他们将希望电话结束后音乐仍保持暂停。其他能引起可恢复性中断的应用的例子包括那些具备闹钟、音频提示（例如语音方向指示）或其他间歇性音频功能的应用。
* **不可恢复中断（**nonresumable interruption**）**是由那些被用户视为首要听觉体验的音频所引起的，比如媒体播放用用的音频。在不可恢复中断结束后，显示媒体播放控件的应用不应该恢复播放那个音频。而没有媒体播放控件的应用应该恢复播放音频。例如，假设用户正在收听一个音乐播放应用（音乐应用1），此时另一个音乐播放应用（音乐应用2）打断了它。用户终止后决定收听音乐应用2一段时间。在退出音乐应用2之后，用户不想要音乐应用1自动恢复播放，因为此时他们主动将音乐应用2作为首要的听觉体验。

下列准则可以帮助你决定支持什么信息以及如何在音频中断之后继续:

**确定你的应用引起的音频中断的类型。**在你的音频结束时，你可以通过以下两种方式中的一种禁用你的音频会话来实现这一功能：

* 如果你的应用引起了一个可恢复性中断，使用[AVAudioSessionSetActiveFlags_NotifyOthersOnDeactivation](https://developer.apple.com/library/ios/documentation/AVFoundation/Reference/AVAudioSession_ClassReference/index.html#//apple_ref/c/econst/AVAudioSessionSetActiveFlags_NotifyOthersOnDeactivation)标识禁用你的音频会话。
* 如果你的应用引起了一个不可恢复中断，不用任何标识就可以禁用你的音频会话。

倘若不这样，标识会在适宜的情况下允许iOS系统赋予被中断的应用自动恢复播放它们的音频的能力。

**决定是否应该在一个音频中断结束后恢复音频。**你应依据你应用中所提供的音频用户体验来做这一决断。

*   如果你的应用呈现了用户用于播放或暂停音频的媒体播放控件，你需要在一个音频中断结束后检查[AVAudioSessionInterruptionFlags_ShouldResume](https://developer.apple.com/library/ios/documentation/AVFoundation/Reference/AVAudioSession_ClassReference/index.html#//apple_ref/c/econst/AVAudioSessionInterruptionFlags_ShouldResume)标识，如果你的应用接受应该恢复（Should Resume）标识，你的应用应该：  

    > **·** 如果你的应用被打断时在主动播放音频，恢复播放音频；  
    > **·** 如果你的应用被打断时没有在主动播放音频，不需要恢复播放音频。

*   如果你的应用没有呈现任何用户可用于播放或暂停音频的媒体播放控件，你的应用应该在音频中断结束后总是保持恢复之前播放的音频，无论是否呈现了“应该恢复”标识。例如，播放音效的游戏应该在中断后自动恢复播放音效。

### 3.13.4 适时处理媒体远程控制事件（Handle Media Remote Control Events, if Appropriate）

当人们使用iOS媒体控制或辅助控制（如耳机线控）时，应用要能响应远程控制事件。这需要允许你的应用能接收来自于你的用户界面之外的输入，无论你的应用当前是在前台还是后台播放音频。

应用可以播放仍在进行时，通过后台向支持Airplay的硬件（如Apple TV）发送视频。这样的应用接收通过远程控制事件实现的用户输入行为，据此用户可以控制处于后台运行状态的应用中的视频播放。除此之外，这类的应用程序也能在音频会话被打断而转入后台时重新将其激活。

一个媒体播放应用，特别是它会在后台播放音频或视频时，尤其需要合理响应媒体远程控制事件。

当你的应用在后台运行时，为了满足与播放媒体特权相关的责任，要确保遵循以下这些原则：

**限制你的应用接收远程控制事件的次数。**例如，当你的应用可以帮助用户阅读内容、搜索信息或是收听音频时，它只有在用户处于音频场景中时才应该接收远程控制事件。当用户脱离音频情境时，你应该放弃接收事件的能力。如果你的应用允许用户在支持AirPlay的设备上播放音视频，它应该在媒体播放期间都可以接收远程控制事件。遵循这些原则会允许用户在你的应用中处于非媒体情境中时，可以体验到不一样的应用媒体，并能用耳机控制它。

**尽可能的使用系统原生的控件以提供AirPlay支持。**当你使用[MPMoviePlayerController](https://developer.apple.com/library/ios/documentation/MediaPlayer/Reference/MPMoviePlayerController_Class/index.html#//apple_ref/occ/cl/MPMoviePlayerController)类实现AirPlay播放功能时，你可以利用标准的控件以允许用户选择当前范围内支持AirPlay的硬件。或者你可以使用[MPVolumeView](https://developer.apple.com/library/ios/documentation/MediaPlayer/Reference/MPVolumeView_Class/index.html#//apple_ref/occ/cl/MPVolumeView)类来显示用户可选择的支持AirPlay的音频或视频设备。用户习惯于这些标准控件的外观和行为，因此他们可以理解如何在你的应用中使用它们。

**不要改变事件的用途，即使这个事件在你的应用中没有意义。**用户期望iOS系统的所有应用媒体控制和辅助控制能有功能上的统一。你不必实现你的应用所不需要的那些事件，但你所实现的事件必须产生符合用户期望的结果。如果你重新定义一个事件的意义，你会使用户困惑并冒险把他们带入一个未知的状态，他们只能通过退出你的应用来逃离。

### 3.14 VoiceOver

VoiceOver增加了对盲人、弱视用户,以及一些有学习困难的用户的辅助性。

[![05](https://isux.tencent.com/wp-content/uploads/2014/12/20141207165431849.png)](https://isux.tencent.com/wp-content/uploads/2014/12/20141207165431849.png)

为了确保VocieOver的用户能使用你的应用，你可能需要确保你的用户界面内的页面和控制器能提供一些描述性信息。对VoiceOver的支持不需要你改变你用户界面内的任何视觉设计。

当你完全遵照标准的方式使用标准的用户界面元素时，几乎不（即使有也很少）需要增加额外的工作。你的用户界面越趋向定制化，你就越需要提供更多的信息来保证VoiceOver能准确的描述你的应用。

增加你的iOS应用对VoiceOver用户的可用性，可以扩大你的用户基础并帮助你进入新的市场。支持VoiceOver也可以帮助你遵守由主流群体所制定的辅助性指导准则。

### 3.15 路线选择（Routing）

地图可以显示到达用户目的地的可选路线：

[![06](https://isux.tencent.com/wp-content/uploads/2014/12/20141207165511640.png)](https://isux.tencent.com/wp-content/uploads/2014/12/20141207165511640.png)

当人们想要获得关于某条路线的更多交通信息时，地图也可以显示能提供路线选择的应用列表——既包括安装在设备上的应用也包括应用商店中的应用。

[![07](https://isux.tencent.com/wp-content/uploads/2014/12/20141207165542397.png)](https://isux.tencent.com/wp-content/uploads/2014/12/20141207165542397.png)

**路线选择应用**可以提供当前选择的路线有关的信息。人们希望路线选择应用能够快捷、易用，特别是保证准确性。依据本章提供的指导原则能帮你为用户提供他们可信任的交通信息和他们期望的用户体验。

重要：地图能依据人们选择的路线给他们提供驾车和步行的指示。路线选择应用可以提供交通信息，它着重于使用交通工具（如公交车、火车、地铁、渡船、自行车、行人、穿梭巴士等）的模型替代实物逐步地指示方向。

如果你的应用不能提供用户指定的路线的交通信息，那么不要将你的应用定位为路线选择应用。

**实现你的应用承诺的功能。**当人们在交通列表里看到你的应用时，他们认为它可以帮助其到达目的地。但是如果你的应用不能提供所选路线的信息——或者它没能涵盖它看似应该涵盖的那些种类的交通信息——人们就不会愿意给它第二次机会。准确的表达出你的应用的能力是十分重要的；否则，你的应用会看起来像是在故意误导用户。

在你的路线选择应用中，有两种主要的方式可以给用户信心：

* 尽可能准确的定义你所支持的地理区域。例如，如果你的应用能帮助人们获得巴黎的公交线路的信息，那你所支持的地区应该是巴黎，不是法兰西岛，也不是法国。
* 明确你所支持的交通信息类型。例如，如果你专攻于地铁信息，不要暗示你仿佛支持所有的轨道交通类型

注意：虽然准确的报告你所支持的地区意味着将会减少你的应用在交通信息列表里的出现次数，但这么做却可以帮助用户更加信任它。

**为易用性合理组织界面。**易用性对于路线规划应用来说特别重要，因为用户常常会在极具挑战性的情况下使用它们——例如在明亮的阳光下、在昏暗的车厢内抑或是在颠簸的旅程中，或在非常紧急的情况下。要确保你的文字在任何光照条件下都能容易的阅读，确保按钮即使在并不平稳的旅程中也能易于准确点击。

**专注于路线。**虽然辅助信息会很有用，但你的应用应该专注于为用户提供逐步的指示以便他们能据此到达目的地。特别要强调的是，你要让用户知道他们处于哪一步，并知道如何到达下一步。你可以提供额外的数据——比如时间表或系统地图——但不要让这些数据比交通信息还重要。

**为路线的每一步提供信息****。**永远不要让用户感觉被你的应用所遗弃。即使在可以准确的报道你所支持的地区时，你也不能假定用户已经抵达的路线中的第一个交通节点或是最后一个交通节点就是他们目的地点。为了控制这一情况，首先就是测量起点到终点距离。如果距离足够短，要提供从用户当前位置到第一个交通节点及从最后一个交通节点到用户目的地的步行方向指示。如果步行不是一个合理的选择，尝试描绘用户的其他选项。如果必要的话，你可以给用户提供打开地图，获取这部分路线的步行或驾车方向指示的方式。

**当用户从地图应用切回你的应用时，不要要求他们重复输入信息。**如果用户从地图应用切入（你的应用）时，你已经获知了他们中意的起点与终点，因此你可以在应用打开时直接呈现适合的交通信息。如果用户从主屏幕中开启你的应用，要为他们提供简洁的方式用以输入路线详情。

**显示图文并茂的交通信息****。**地图页面可以帮助人们以更大的、实物性的视角查阅他们完整的线路；清晰的步骤可以帮助人们专注于他们抵达目的地所需采取的必要行动。最好可以同时支持这两个任务并能让用户便捷地进行切换。

注意：无论以什么格式，最重要的是显示与用户线路相关的相同的交通信息。例如，如果路线中包含五个步骤，在地图和路线列表页中必须描绘相同的五步。

当你的应用被从交通列表中选中时，需要以显示完整的线路做为良好的开始——包括在地图页面中显示始于或抵达交通节点的步行路线。地图页面可以为用户提供他们旅途的多步骤的总览，并能展示适于周遭地理环境的路线。

**用附加信息丰富地图页面。**人们期望你的应用中的地图可以表现的与他们使用过的其他地图相似。除了用户能放大和缩小以外，你还应该显示用户所需的那些注释信息。例如，你应该显示图钉用以代表用户当前的位置、目的地以及沿路的转乘点或重要的节点。

确保避免只显示一个单独的图钉，因为对用户来说，如果没有额外的背景，很难理解它代表什么。欲了解在你的应用中使用地图页面的更多信息，详见[_Map View._](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/ContentViews.html#//apple_ref/doc/uid/TP40006556-CH13-SW134)

尽可能的整合静态地图页面——例如在地图视图中加入地铁系统地图等。一个很好的实现方法就是在地图页面覆盖静态图片，以便用户可以看到他们的路线及他们的当前位置是如何与更大的交通系统相关的。

注意：如果你决定让应用显示一个静态的地图图片，要确保使用高分辨率的图片以保证用户在缩放时维持高质量的显示。

**给用户提供不同的方案来挑选多样的交通选择。**很多因素会影响人们交通的选择—例如不同的时间段，天气以及他们携带东西的多少—所以提供简洁地不同交通方式的对比是十分重要的。例如，你要能让用户可以依据开始或结束的时间、需要步行的数量、沿途停下的次数抑或转乘的次数或所需的不同的交通类型等来挑选交通方式。不管你显示多种交通选择的顺序如何，确保用户能立即分辨出这些选项的不同之处。

**考虑使用推送通知为人们提供与路线相关的重要信息。**尽可能的让人们了解交通情况信息的变化，以便他们可以据此调节自己的计划。例如，如果火车晚点或者巴士路线临时停滞，人们可能会需要选择不同的交通路线到达目的地。而在一条不同步骤的站点之间相隔很长距离的交通路线中，人们会希望在他们的交通工具将要抵达行程中的下一部分时能获得通知。

### 3.16 编辑菜单（Edit Menu）

用户能呼出一个编辑菜单来完成诸如在文本视图、网页或图片视图中的剪切、粘贴以及选择操作。

[![08](https://isux.tencent.com/wp-content/uploads/2014/12/20141207172156843-590x472.png)](https://isux.tencent.com/wp-content/uploads/2014/12/20141207172156843.png)

你可以调整一些菜单的行为使用户能更多的控制（活处理）你App中的内容。举个例子，你可以：

* 列举出适合当前情境的标准菜单的命令
* 在菜单显示前判定菜单的位置，以便防止你App界面中重要的信息被遮盖
* 定义当用户双击时会显示默认被选择的对象的菜单

你不能改变菜单本身的颜色和形状。

关于如何在代码中实现这些行为的相关信息，参见[Text Programming Guide for iOS](https://developer.apple.com/library/ios/documentation/StringsTextFonts/Conceptual/TextAndWebiPhoneOS/Introduction/Introduction.html#//apple_ref/doc/uid/TP40009542)中[Copy, Cut, and Paste Operations](https://developer.apple.com/library/ios/documentation/StringsTextFonts/Conceptual/TextAndWebiPhoneOS/UsingCopy,Cut,andPasteOperations/UsingCopy,Cut,andPasteOperations.html#//apple_ref/doc/uid/TP40009542-CH11)章节。

为了确保编辑菜单在你的应用中的表现符合用户期望，你应该：

**在当前情境下显示合理的命令****。**例如，当没有对象被选择的时候，菜单中不应该包括复制或剪切（命令），因为这些命令是针对选择（的内容）而操作的。相似地，如果有对象被选择的时候，菜单中不应该包括选择（命令）。如果你在自定义页面中支持编辑菜单，你就有责任确保菜单中显示的命令切合当前的情境。

**依据你的页面布局调节菜单显示****。**iOS在插入点或选择的上方或下方依据可获得的空间来放置菜单指针以显示编辑菜单，这样用户就能看到菜单命令是如何与内容相关的。必要的话，你可以通过程序在菜单显示之前决定它的位置，这样可以避免用户界面中的重要信息被遮挡。

**支持两种手势来调用菜单****。**虽然触控和长按手势是用户呼起编辑菜单的首选方式，但他们也可以在文本页面中通过双击一个单词来选择该单词并同时呼起菜单。如果你在自定义页面中支持菜单，确保它能支持两种手势。除此之外，你可以定义用户双击时默认的选择对象。

**避免在你的用户界面中创建和编辑菜单中功能相同的按钮****。**例如，使用编辑菜单让用户进行复制操作远比提供一个复制按钮要好，因为用户将会想知道为什么在你的应用中会有两种方法做同样的事。

**如果静态文本的选择对用户来说是有用的，那么可以考虑使用它****。**用户可能想要复制图片的标题，但他们不可能想复制选项卡的标签或是屏幕的标题，比如“账户（Account）”。在文本页面内，文字的选择应该是默认设置的。

**不要使按钮标题可选择****。**如果按钮的标题是可选择的，用户很难在不激活按钮的情况下呼出编辑菜单。通常来说，像按钮这样操作的元素不需要是可选择的。

**将对撤销与重做的支持与对复制与粘贴的支持组合到一起****。**人们经常希望在他们改变主意的时候能撤销最近的操作。由于编辑菜单在它操作执行的时候是不需要确认的，你应该给用户提供撤销或重做这些操作的机会。

如果你需要创建自定义的编辑菜单项，需要像下面展示的这个例子一样遵循这些指导原则：

[![09](https://isux.tencent.com/wp-content/uploads/2014/12/20141207172336450.png)](https://isux.tencent.com/wp-content/uploads/2014/12/20141207172336450.png)

**创建直接作用于用户选择的包含编辑、修改或其他操作的编辑菜单。**人们期望在当前的情境内用标准的编辑菜单项操作文本或对象，那么你的自定义菜单项最好能有相似的表现。

**将自定义项列在所有系统提供的项的后面。**不要将你的自定义项与系统提供的项混置在一起。

**保持自定义菜单项的数量在合理的范围内。**你不应该用太多选择淹没你的用户。

**使用简洁的名称命名你的自定义菜单项**并确保名称能准确的描述命令的作用。通常，项的名字应该是一个可以描述行为如何执行的动词。虽然你通常会使用单个的大写单词作为名字，但如果你必须使用一个短语（作为名字）时，就应使用标题式大写短语。（简洁的、标题性的大写词就是将除了文章、四字及四字以下的并列连词与介词之外的每个单词都要大写。）

### 3.17 撤销与重做（Undo and Redo）

用户通过摇晃设备触发撤销操作，会显示提醒框以允许他们：

* 撤销他们刚才输入的内容
* 重做先前撤销的输入
* 取消撤销操作

[![10](https://isux.tencent.com/wp-content/uploads/2014/12/20141207173116902.png)](https://isux.tencent.com/wp-content/uploads/2014/12/20141207173116902.png)

你可以在你的应用中通过以下说明用更为通用的方式来支持撤销操作：

* 用户可以撤销或重做的行为
* 在你的应用下晃动事件是作为晃动撤销手势的
* 支持多少级的撤销

欲了解如何用代码实现这一行为，参见[Undo Architecture](https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/UndoArchitecture/UndoArchitecture.html#//apple_ref/doc/uid/10000010i)。如果在你的应用中支持撤销和重做，遵循以下准则以提供好的用户体验:

**为用户提供简洁的描述性短语使其能准确的获知他们正在撤销或重做的内容。**iOS系统自动提供了“撤销”和“重做”的字符串（包括词语后面的空格）作为撤销警示按钮的标题，但你需要提供一或两个词语用于辅助描述用户的重做或撤销操作。例如，你可能提供文本的“命名”或“地址更改”之类的词语用以创建像“撤销命名”或“重新更改地址”这样的按钮标题。（要注意，在提醒框中，“取消”按钮是不能改变或移除的）。

[![11](https://isux.tencent.com/wp-content/uploads/2014/12/20141207173141124.png)](https://isux.tencent.com/wp-content/uploads/2014/12/20141207173141124.png)

**避免提供太长的文本。**太长的按钮标题容易被断章取义并且很难被用户解读。由于这个文本是存在于按钮的标题之内，要使用标题样式的大写形式并且不能添加标点。

**避免过度使用摇晃手势。**即使你能程式化的设定你的应用将摇晃事件作为摇动撤销操作，你也是在冒着混淆用户视听的风险，因为他们也可能使用摇晃执行一个不同的操作。分析你的应用中的人机交互以避免创建那些用户无法可靠地预测摇晃手势结果的场景。

**如果撤销和重做在你的应用中是基础性任务，尽量使用系统原生的撤销与重做按钮。**记住摇晃手势是用户触发撤销与重做操作的主要方式，而如果提供两种不同方式完成同样的任务则会使用户困惑。如果你认为很有必要提供直观专有的撤销与重做操作，你可以在导航栏中放置系统原生的按钮。（欲了解更多关于这些按钮的信息，参见[Toolbar and Navigation Bar Buttons](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Bars.html#//apple_ref/doc/uid/TP40006556-CH12-SW33)）。

**将撤销与重做能力与用户当下的情境进行清晰地关联，而非过早地介入情境。**仔细考虑你允许进行撤销与重做操作的情境。通常来说，用户期望他们的改变和操作可以立即被有效的执行。

### 3.18 键盘和输入页面（Keyboards and Input Views）

在iOS8与之后的系统中，你可以创建自定义键盘的扩展来替代系统原生键盘。欲了解更多关于管理应用内扩展（包括键盘）的信息，参见 [应用扩展](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/AppExtensions.html#//apple_ref/doc/uid/TP40006556-CH67-SW1)章节；欲了解如何开发自定义键盘扩展的信息，参见[App Extension Programming Guide](https://developer.apple.com/library/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214)中的[Custom Keyboard](https://developer.apple.com/library/ios/documentation/General/Conceptual/ExtensibilityPG/Keyboard.html#//apple_ref/doc/uid/TP40014214-CH16)章节。

在合适的情况下，你也可以在你的应用内设计自定义的输入页面来替代系统原生的屏幕键盘。例如，Numbers（译者注：iWork中的电子表单应用程序）中提供了多种输入页面，这些页面的设计用以简单高效地完成数量、日期和其他值的输入。

[![12](https://isux.tencent.com/wp-content/uploads/2014/12/20141207173226542-590x204.png)](https://isux.tencent.com/wp-content/uploads/2014/12/20141207173226542.png)

如果你提供自定义输入页面，确保它的功能对于来用户来说是清晰易懂的。

你也可以提供自定义的输入辅助视图，这种视图通常表现为显示在键盘（或你的自定义输入页面）上方的一个独立元素。例如，在某些情境中，Numbers会显示一个输入辅助视图用以帮助用户执行针对电子表格中的值的标准或自定义计算。

[![13](https://isux.tencent.com/wp-content/uploads/2014/12/20141207173301737-590x34.png)](https://isux.tencent.com/wp-content/uploads/2014/12/20141207173301737.png)

当用户在你的输入页面中敲击自定义控件时，使用标准的键盘敲击声提供声音反馈。欲了解在代码中如何使用这一声音，参见[_UIDevice Class Reference_](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIDevice_Class/index.html#//apple_ref/doc/uid/TP40006902)文件中的[playInputClick](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIDevice_Class/index.html#//apple_ref/occ/instm/UIDevice/playInputClick)章节