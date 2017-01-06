# iOS 9人机界面指南

## 1. UI设计基础

### 1.1 为iOS而设计(Designing for iOS)

**iOS** 表现了以下三大设计原则：

* **遵从****(****Deference)**：UI应该有助于用户更好地理解内容并与之交互，并且不会分散用户对内容本身的注意力。
* **清晰(****Clarity)**：各种尺寸的文字清晰易读；图标应该精确醒目，去除多余的修饰，突出重点，以功能驱动设计。
* **深度(****Depth)**：视觉的层次感和生动的交互动画会赋予UI新的活力，有助于用户更好地理解并让用户在使用过程中感到愉悦。

[![视频插图11](https://isux.tencent.com/wp-content/uploads/2015/10/2015102117064336.jpg)](https://isux.tencent.com/wp-content/uploads/2015/10/2015102117064336.jpg)

无论你是重新设计现有的应用，还是重新开发一个新应用，请基于下列方法进行设计考虑：

* 首先，去除掉UI元素让应用的核心功能突显出来，并明确之间的相关性。
* 然后，使用iOS的主题来定义UI并进行用户体验设计。完善细节设计，以及适当合理的修饰。
* 最后，保证你设计的UI可以适配各种设备和各种操作模式，使得用户在不同场景下都可以享受你的应用。

在整个设计过程中，时刻准备着推翻先例，质疑各种假设，并以内容和功能视为重点来驱动每个细节的设计。

### 1.1.1 设计跟随内容 (Defer to Content)

尽管清新美观的UI和流畅的动态效果都是iOS体验的亮点，但内容始终是iOS的核心。

这里有一些方法可以确保你的设计既可以提升功能体验，又可以关注内容本身。

**充分利用整个屏幕。**系统天气应用是这个方法的绝佳范例：用漂亮的全屏天气图片呈现现在的天气，直观地向用户传递了最重要的信息，同时也留出空间呈现了每个时段的天气数据。

[![20140922141637148](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161354587.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161354587.png)

**重新考虑(尽量减少)拟物化设计的使用。**遮罩、渐变和阴影有时会让UI元素显得很厚重，导致影响到了对内容的关注。相反，应该以内容为核心，让用户界面成为内容的支撑。

[![20140922141636135](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161347236.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161347236.png)

**用半透明****UI****元素样式来暗示背后的内容。**半透明的控件元素(比如控制中心)可以提供了上下文的使用场景，帮助用户看到更多可用的内容，并可以起到短暂的提示作用。在iOS中，半透明的控件元素只让它遮挡住的地方变得模糊——看上去像蒙着一层米纸——它并没有遮挡屏幕剩余的部分。

[![20140922141633495](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161332324.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161332324.png)

### 1.1.2 保证清晰(Provide Clarity)

确保你的应用始终是以内容为核心的另一个方法是保证清晰度。这里有几种方法可以让最重要的内容和功能清晰可见，且易于交互。

**使用大量留白。**留白可以使重要的内容和功能更加醒目、更易理解。留白还可以传达一种平静和安宁的心理感受，它可以使一个应用看起来更加聚焦和高效。

[![20140922141636668](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161350996.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161350996.png)

**让颜色简化****UI****。**使用一个主题色——比如Notes中用了黄色——高亮了重要区块的信息并巧妙地用样式暗示可交互性。同时，也让应用有了一致的视觉主题。内置的应用使用了同系列的系统颜色，这样一来，无论在深色或浅色背景上看起来都很干净，纯粹。

[![notes_color_2x](https://isux.tencent.com/wp-content/uploads/2015/10/20151021162313271.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151021162313271.png)

**通过使用系统字体确保易读性。**iOS的系统字体(San Francisco)使用动态类型(Dynamic Type)来自动调整字间距和行间距，使文本在任何尺寸大小下都清晰易读。无论你是使用系统字体还是自定义字体，一定要采用动态类型，这样一来当用户选择不同字体尺寸时，你的应用才可以及时做出响应。

[![2014092214163585](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161314104.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161314104.png)

**使用无边框的按钮。**默认情况下，所有的栏(bar)上的按钮都是无边框的。在内容区域，通过文案、颜色以及操作指引标题来表明该无边框按钮的可交互性。当它被激活时，按钮可以显示较窄的边框或浅色背景作为操作响应。

[![2014092214163313](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161310540.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161310540.png)

### 1.1.3 用深度层次来进行交流(Use Depth to Communicate)

iOS经常在不同的视图层级上展现内容，用以表达层次结构和位置，这样可以帮助用户了解屏幕上对象之间的关系。

对于支持3D触控的设备，轻压(Peek)、重压(Pop)，以及快捷操作(Quick Actions)能让用户在不离开当前界面的情景下预览其他重要内容。

[![webview_peek-30_2x](https://isux.tencent.com/wp-content/uploads/2015/10/20151021162648184.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151021162648184.png)

通过使用一个在主屏幕上方的半透明背景浮层，这样文件夹就能清楚地把内容和屏幕上其他内容区分开来。

[![20140922141633945](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161335961.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161335961.png)

如图所示，备忘录(Reminders)以不同的层级展示内容条目。用户在使用备忘录里的某个条目时，其他条目会被集中收起在屏幕下方。

[![20140922141634411](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161339644.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161339644.png)

日历具有较深的层级，当用户在翻阅年、月、日时，增强的转场动画效果给用户一种层级纵深感。在滚动年份视图时，用户可以即时看到今天的日期以及其他日历任务。

[![20140922141632512](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161328758.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161328758.png)

当用户选择了某个月份，年份视图会局部放大该月份，过渡到月份视图。今天的日期依然处于高亮状态，年份会显示在返回按钮处，这样用户可以清楚地知道他们在哪儿，他们从哪里进来以及如何返回。

[![2014092214163266](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161306786.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161306786.png)

类似的过渡动画也出现在用户选择某个日期时：月份视图从所选位置分开，将所在的周日期推向内容区顶端并显示以小时为单位的当天时间轴视图。这些交互动画增强了年、月、日之间的层级关系以及用户的感知。

[![20140922141631619](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161325202.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161325202.png)

### 1.2 iOS应用解析(iOS App Anatomy)

几乎所有的iOS应用都应用了UIKit framework中定义的组件。了解这些基本组件的名称、作用和功能可以帮助你在应用的界面设计过程中做出更好的决策。

[![插图11](https://isux.tencent.com/wp-content/uploads/2015/10/20151021163632758.jpg)](https://isux.tencent.com/wp-content/uploads/2015/10/20151021163632758.jpg)

UIKit提供的UI组件可以大致分为以下4种类型：

* **栏(****Bars)**：包含了上下文信息来指引用户他们所在的位置，以及控件来帮助用户导航或执行操作。
* **内容视图(****Content Views)**：包含了应用的具体内容以及某些操作行为，比如滚动、插入、删除、排序等等。
* **控件(****Controls)**：用于执行操作或展示信息。
* **临时视图(****Temporary Views)**：短暂出现给予用户重要信息或提供更多的选择和功能。

UIKit除了定义UI组件元素，还定义对象如何实现功能，例如手势识别、绘图、辅助功能和打印支持。

从编程的角度来看，UI组件元素其实是视图的子类，因为它们继承了UIView。视图能绘制屏幕内容并知道用户何时在其范围内触屏。视图的所有类型有：控件(比如按钮和滑块)、内容视图(比如集合视图和表格视图)，以及临时视图(如警告提示和动作菜单)。

要在应用中管理一组或者一系列的视图，通常需要使用视图控制器。它能协调视图的内容显示，实现与用户交互的功能并能在不同屏幕内容之间切换。比如，“设置”使用了一个导航控制器来展示其视图层级。

这里有一个关于视图与视图控制器如何结合并呈现iOS应用的UI的例子，如图。

[![20140922142257717-590x556](https://isux.tencent.com/wp-content/uploads/2015/10/201510191619260.png)](https://isux.tencent.com/wp-content/uploads/2015/10/201510191619260.png)

尽管开发者认为真正起到作用的是视图和视图控制器，但一般用户感知到的iOS应用是不同屏幕内容的集合。从这个角度来看，在应用里，屏幕内容一般对应于一个独特的视觉状态或者模式。

**注：**一个iOS应用程序包含一个窗口。但是，不同于计算机程序中的窗口，iOS窗口没有可见的部分并且不能在屏幕上被移动到另一个位置。很多iOS应用程序只有一个窗口；可以支持外部显示设备器的应用程序可以有不止一个窗口。

在_iOS Human Interface Guidelines_中，屏幕(_screen)_这个词和大部分用户理解的一样。作为一个开发者，你也许需要阅读一下其他与[UIscreen](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIScreen_Class/index.html#//apple_ref/occ/cl/UIScreen)相关的章节，这样你可以更好的了解如何关联外部屏幕。

### 1.3 适应性和布局(Adaptivity and Layout)

### 1.3.1 为自适应而开发(Build In Adaptivity)

人们通常希望在他们所有的设备和多种情境中使用自己喜欢的应用程序，比如在不同的设备方向上和iPad的分屏情况下。尺寸类别( Size classes)和自动布局(Auto Layout)可以通过定义屏幕的布局、视图控制器和视图在环境变化时候应该怎么适应来帮助你实现这个愿望。(显示环境[display environment]的概念指的是设备的整个屏幕或者其中一部分，比如弹出框的区域或者iPad分屏视图中其中一侧的区域。)

iOS在特征集合(_trait collection)_的定义中包含了显示环境的概念，特征集合囊括了尺寸类别(size class)，显示比例(display scale)和用户界面语言(user interface idiom)。你可以使用一个特征集合让你的视图和视图控制器响应显示环境的变化。

iOS定义了两个尺寸类别(size class)，常规的(regular)和压缩的(compact)。常规尺寸与拓展的空间紧密相关，压缩尺寸与约束的空间相关。想要定义一种显示环境，你需要定义一种横屏尺寸类别，与一种竖屏尺寸类别。如你所想，一个iOS设备在竖屏模式可以使用一套类别，而横屏模式下可以使用另一套类别。

iOS能随着尺寸类别和显示环境变化而自动生成不同布局。举个例子，当垂直尺寸从压缩变为常规时，导航栏和工具栏会自动变高。

当你靠尺寸类别来驱动布局变化时，你的应用在任何显示环境时都能显示得很好。关于如何在Interface Builder中更好的使用尺寸类别，你可以查阅_[Size Classes Design Help](https://developer.apple.com/library/ios/recipes/xcode_help-IB_adaptive_sizes/_index.html#//apple_ref/doc/uid/TP40014436)._

**注：**在一种尺寸类别中，持续使用Auto Layout进行小的布局调整，比如拉伸或压缩内容。更多Auto Layout，参看 _[Auto Layout Guide](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/AutolayoutPG/index.html)._

下面的实例可以帮助你形象展现尺寸类型如何适配不同设备的显示环境。例如：iPad(包括iPad Pro)在长宽和横屏竖屏时都使用常规尺寸类型。换句话说，iPad显示环境一直处于垂直和水平的常规状态。

[![20140922142628708-590x287](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161955209.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161955209.png)

注：合格的iPad型号支持多任务，你的应用可能需要与其他应用共享同一个屏幕。确保使用Auto Layout，这样你可以在用户使用多任务功能时响应他，比如 分屏模式(Split View)和多任务分屏模式(Slide Over)。

除了使用Auto Layout，当你在iPad Pro上展示可读性的内容时，依靠UIView的 [readableContentGuide](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIView_Class/index.html#//apple_ref/occ/instp/UIView/readableContentGuide)属性是非常重要的，这样可以拥有让读者舒服的边距。

iPhone的显示环境可根据不同的设备和不同的握持方向而改变。

竖屏时，iPhone6 Plus使用的是压缩宽度和常规高度类型。

![20140922142510346](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161937222.png)

横屏时，iPhone6 Plus使用的是常规宽度和压缩高度类型。

![20140922142509932](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161933162.png)

其他iPhone型号，包括iPhone6使用相同的尺寸类型设置。

竖屏时，iPhone 6，iPhone 5 和iPhone 4S使用的是压缩宽度和常规高度。

[![20140922142510346](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161937222.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161937222.png)

横屏时，这些设备在宽高上使用的都是压缩类。

[![20140922142510765](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161943483.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161943483.png)

### 1.3.2 在不同环境提供良好体验(Provide a Great Experience in Each Environment)

当你使用自适应来开发UI时，你可以保证UI跟随显示环境变化而适当地响应。遵照这些指南，你可以给用户良好的设备响应体验。

**在所有环境下都保持对主体内容的专注。**这是最高优先级。人们使用应用时，浏览感兴趣的内容并与之发生互动。随着环境变化改变专注点会让用户感觉到迷失方向，让他们感觉对应用失去控制。

**避免布局上不必要的变化。**在所有环境中保持一致的使用体验，能让人们在旋转设备或在不同设备上运行你的应用时维持稳定的使用模式。例如，如果你在水平的常规模式下使用了网格来显示图像，那么无需在压缩模式下使用列表来展示同样的内容，虽然你可能调整了网格的尺寸。

**如果你的应用只在一个方向上运行，那么请直接一点。**人们希望在各种握持方式下都可以使用你的应用，能满足这个期待是最好的。但是，如果你的应用只在一个方向下运行，那么你应当注意：

* **避免出现提示人们旋转设备的相关UI元素****。**让应用在支持的方向下清晰地运行，如果需要用户旋转设备，不要给UI添加不必要的混乱。
* **支持同一个方向上的变化。**例如，如果一个应用只能横屏运行，用户无论用左手或是右手握持时都能触及到home键。如果用户在使用应用时180度旋转设备，那最好应用内容也能及时响应并旋转180度。

**如果你的应用将设备方向翻转视为用户输入(的一种指令)，那么就按照程序设定的方式来响应设备翻转。**举个例子，一个游戏让用户利用设备翻转来移动游戏中的部件，那么这个游戏应用本身(的UI)不能对翻转屏幕产生响应。在这种情况下，你必须关联两个需要变化的方向，并且允许人们在这两个方向切换直到他们开始(了解并执行)应用的主体任务。一旦人们开始执行主要任务，那就开始按程序设定的那样来响应设备的动作。

### 1.3.3 使用布局来沟通(Use Layout to Communicate)

布局包含的不仅仅是一个应用屏幕上的UI元素外观。你的布局，应该告诉用户什么是最重要的，他们的选择是什么，以及事物是如何关联起来的。

**强调重要内容或功能，让用户容易集中注意在主要任务上。**有几个比较好的办法是在屏幕上半部分放置主要内容——遵循从左到右的习惯——从靠近左侧的屏幕开始：

[![20140922142511204-590x568](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161947246.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161947246.png)

**使用不同的视觉化重量和平衡来告诉用户当前屏显元素的主次关系。**大型控件吸引眼球，比小的控件更容易在出现时被注意到。而且大型控件也更容易被用户点击，这让它们在应用中尤其有用——就像电话和时钟(上面的按钮)那样——能让用户经常在容易分心的环境下仍然保持正常使用。

[![视频插图12](https://isux.tencent.com/wp-content/uploads/2015/10/20151021171227949.jpg)](https://isux.tencent.com/wp-content/uploads/2015/10/20151021171227949.jpg)

**使用对齐来让阅读更舒缓，让分组和层次之间更有秩序。**对齐让应用看起来整洁而有序，也让用户在滑动整屏内容时更容易定位和专注于重要信息。不同信息组的缩进与对齐让它们之间的关联更清晰，也让用户更容易找到某个控件。

**确保用户在内容处于默认尺寸时便可清楚明白它的主要内容与含义。**例如，用户应当无需水平滚动就能看到重要的文本，或不用放大就可以看到主体图像。

**准备好改变字体大小。**用户期望大多数应用都可以响应他们在iOS的设置中设定的字体大小。为了适应一些文本大小的变化，你也许需要调整布局；想要得到更多文本显示相关的信息，请查阅下文“颜色与字体”中相关的内容。

**尽量避免****UI****上不一致的表现。**在一般情况下，有着相似功能的控件看起来也应该类似。用户常常认为他们看到的不同总有原因，而且他们倾向于花时间去尝试(译者按：因此为了避免用户做无用的尝试，建议类似的功能外观都保持一样。)

**给每个互动的元素充足的空间，从而让用户容易操作这些内容和控件。**常用的点按类控件的大小是44 x 44点(points)。

[![20140922162720481-590x442](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161959199.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161959199.png)

### 1.4 启动与停止(Starting and Stopping)

### 1.4.1 即时启动(Start Instantly)

我们通常认为用户不会花超过一两分钟去评价一款新应用。当你可以最大程度地利用这段极短的时间，即时呈现对用户有帮助的内容时，你就能够激发新用户的兴趣并给所有用户一种极棒的体验。

[![20140922163431595-590x393](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162003238.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162003238.png)

**重要：**不要在安装过程结束后告诉用户需要重启设备。重启需要花费时间，同时也会让人觉得你的应用不可靠且很难使用。  
如果你的应用有内存使用或其它问题，导致不重启就无法流畅运行，你必须声明这些问题。想要了解如何开发一款性能良好的应用，请参阅[Use Memory Efficiently](https://developer.apple.com/library/ios/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/PerformanceTips/PerformanceTips.html#//apple_ref/doc/uid/TP40007072-CH7-SW8).  
尽可能避免使用闪屏或者其他启动体验方式。用户能够在启动应用后立即开始使用是最好不过的。

**尽可能地，避免让用户做过多设置。**而应该如此：

* **聚焦在80%目标用户的需求上。**这样绝大部分用户就无需设置各种选项，因为你的应用已经默认处于他们想要的状态。如果有些功能仅有少部分用户想要，或者是大部分用户只需要使用一次，那就别管它了。
* **尽可能用其他方式获取更多的用户信息。**如果你能得到用户在内置应用或硬件设置中提供的信息，直接从系统中获取，不要让用户再次输入。
* **如果你必须要求用户设置用户信息，在你的应用中直接提示用户输入。**然后尽快保存这些设定(一般来说，保存到你的应用的设置模块中)。这样用户就无需强制跳出应用进入系统设置页面了。如果用户需要更改设置，他们可以在任何时候进入应用的设置模块进行修改。

**尽可能让用户晚一点再登录。**最理想的状态是，用户在无需登录的情况下就能尽量多地浏览内容并使用部分功能。例如，App Store会在用户确定进行购买商品时，才要求用户进行登录。对于那些强制用户登录后才能进行一切有用操作的应用，用户往往会直接放弃。

如果你的应用必须先登录后使用，那么你应该在登录页面有一些简短的文字，来描述为什么必须先登录，以及这样做会给用户带来什么好处。

**谨慎使用新手引导**(介绍应用的功能和如何进行操作)**。**在考虑新手引导之前，你应该努力地完善你的应用，尽可能使应用的功能直观和易于寻找。_其实，好的应用不需要新手引导_。如果你确实觉得需要新手引导，那么请参考如下的建议，设计一个简洁、有针对性并且不妨碍用户的新手引导。

* **只提供开始使用应用所必需的信息。**好的新手引导应该告诉用户第一步应该做什么，或者简短地演示大部分用户感兴趣的一些功能。如果在能够探索你的应用之前，给用户展示太多信息，让用户记住这些不是当前所必须的内容，会让用户觉得你的应用很难用。如果在某些特定场景下确实需要额外帮助，那么也应该只在用户处于这个场景之后再提供。
* **使用动画和可交互的方式来吸引用户，并让用户通过实际操作来学习如何使用。**对于文字内容的增加应该谨慎，且仅当增加文字对于提升体验有益时才这么做。不要指望用户会阅读大段的文字。例如，可以使用动画而不是文字来描述如何执行一个简单的任务。在引导用户了解较为复杂的任务时，可以通过一些引导浮层来简要说明每一个步骤用户需要做什么。尽可能避免展示应用截图，因为截图不可交互的，用户可能会混淆截图和应用的实际界面。
* **能够让用户很容易地取消或者跳过新手引导。**有些用户看完新手引导之后就不想再看，有些甚至根本就不想看新手引导。请记住用户的选择，不要强迫用户每次打开你的应用都要再选择一次。

**不要太早要求用户去给你的应用评分。**过早要求用户进行评分可能会适得其反。如果你想获得有价值的反馈和评论，在邀请用户评论之前，请给他们一点时间来使用你的应用，并对你的应用形成印象。例如，你可以等用户访问了一定数量的页面或完成了一定数量的任务之后，再邀请他们进行评价。

**一般建议按照屏幕默认的定向方式启动你的应用。**尽管如此，如果你的应用只有一种屏幕方向，那么就始终以这个方向启动，让用户在他们自己需要时再改变设备方向。例如，一个游戏或者媒体观看应用只在横屏模式下运行，那么就应该以横屏模式启动，即使设备当前处于竖屏模式。这样的话，如果用户在竖屏模式下打开应用，他们也知道应该把设备转成横屏来进行使用。

[![default_orientation_2x](https://isux.tencent.com/wp-content/uploads/2015/10/20151020105716999.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151020105716999.png)

注：最好让横屏应用支持两种方向的横屏，即home键在左或在右方都支持。如果设备当前已经处于横向状态，那么就按照当前状态启动应用，除非你有充分的理由不这么做。其他情况时，可以考虑按home键处于右侧的方式启动应用。(想要了解更多关于支持不同设备方向的内容，请参阅前文中Adaptivity and Layout相关章节。)

**提供一张与应用首页看上去一样的闪屏。**iOS会在启动应用时调用这张图，这样可以让用户觉得启动速度很快，同时，也可以让你的应用有足够的时间去加载内容。具体如何制作闪屏，请查阅Launch Files。

**如果可能，不要让用户在初次启动应用时阅读免责声明或者确认用户协议。**你可以直接在App Store展示这些内容，使用户在下载前就有所了解。如果在某些情况下你必须展示这些内容，要确保它们与界面保持统一并在产品功能与用户体验之间达成平衡。

**在应用重启后，需要恢复到用户退出使用时的状态，让他们可以从中断之处继续使用。**无需让用户记住是如何回到此状态的。了解更多关于保持和恢复应用状态的有效方式，请查阅Preserving Your App’s Visual Appearance Across Launches。

### 1.4.2 时刻准备好停止(Always Be Prepared to Stop)

**iOS 应用不存在关闭或退出选项。**当用户切换到另一个应用，回到主屏幕或者将设备调至睡眠模式的时候，其实就是停止了当前应用的使用。  
当用户切换应用时，iOS的多任务系统会将其放置到后台并将新应用的UI替换上来。在这种情况下，你必须做到以下几点：

**随时并尽快保存用户信息。**因为在后台的应用随时有可能被终止或退出。

**当应用停止的时候保存尽可能多的当前状态的详细信息。**这样使用户可以在回到应用时能从中断之处继续使用。例如，在使用可滚动的数据列表时，退出后保存列表所在的位置。了解更多关于保持和恢复应用状态的有效方式，请查阅[Preserving Your App’s Visual Appearance Across Launches](https://developer.apple.com/library/ios/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/StrategiesforImplementingYourApp/StrategiesforImplementingYourApp.html#//apple_ref/doc/uid/TP40007072-CH5-SW2).

有些应用可能需要一直在后台运行。例如，用户可能希望能在使用一个应用的同时还能一直听歌，接着又想用另外一个应用来检查代办项或者玩游戏。关于如何正确处理多任务，请查阅[Multitasking](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Multitasking.html#//apple_ref/doc/uid/TP40006556-CH38-SW1).

**不要强制让应用退出。**因为这样会让用户误以为是系统崩溃。如果有问题产生，需要告诉用户具体状况以及如何解决。以下有两个建议，取决于出现的问题有多严重，可以酌情使用：

**如果应用中所有的功能当前都不可用，那么应该显示一些内容来解释当前的情形，并建议用户如何进行后续操作。**这部分内容给予了用户以反馈，使用户相信你的应用现在没问题。同时这也可以稳定用户情绪，让他们决定是否要采取纠正措施，继续使用应用，还是切换到另一个应用。

[![20140922163801598](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162011179.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162011179.png)

**如果只有部分功能不可用，那么只要当用户使用这些功能时显示提示即可。**其他情况下，用户就应该能正常使用应用的其他功能。如果你决定使用警告框来进行提示，请确保只在用户尝试使用不可用的功能时再显示。

[![2014092216380299](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161317906.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019161317906.png)

### 1.5 导航(Navigation)

除非导航设计不合理，不然用户应该明显察觉不到应用中的导航体验。导航设计应该能够支撑你应用结构和目的却又不分散用户注意力。  
广义来说，导航主要有以下几种类型，每个导航都有其适应的应用结构：

* 分层
* 扁平
* 内容或体验驱动

在有层级结构的应用中，用户在每个层级中都要选择一项，直到到达目的层级。如果要切换到另一个目的层级，用户必须回退一些层级，或者直接回到初始层级再次选择。系统设置和邮箱应用在这方面是很好示范，可以参考他们。

[![视频插图1](https://isux.tencent.com/wp-content/uploads/2015/10/20151020153806891.jpg)](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Art/navigation_hierarchy.m4v)

**译者注：**以上为视频截图，完整视频可[点击观看](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Art/navigation_hierarchy.m4v)。

在扁平信息架构的应用中，用户可以从首页目录直接切换到另一个，因为所有的分类都可以从主屏直接访问。音乐和App Store是两个使用扁平结构的好例子。

[![视频插图2](https://isux.tencent.com/wp-content/uploads/2015/10/2015102015434520.jpg)](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Art/navigation_flat.m4v)

**译者注：**以上为视频截图，完整视频可[点击观看](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Art/navigation_flat.m4v)。

在内容或体验驱动的信息架构应用中，导航也会根据内容或体验来设计。例如，在阅读一本电子书时，用户会一页接一页的进行阅读，或者直接从目录中选中某一个指定的页码；同样，在游戏中导航也是体验的重要组成部分。

[![视频插图3](https://isux.tencent.com/wp-content/uploads/2015/10/20151020154550662.jpg)](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Art/navigation_contents.m4v)

**译者注：**以上为视频截图，完整视频可[点击观看](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Art/navigation_contents.m4v)。

在某些情况下，在一个应用中结合多种导航类型会有很好的效果。例如，对于扁平信息结构中某一分类下的内容，用分层导航的方式来显示可能会更好。

**应该让用户时刻清楚自己当前在应用中所处的位置，及如何前往目的页面。**无论使用哪种适合你的应用结构的导航，最重要的是用户访问内容的路径要有逻辑、可预期和易于追溯。

UIKit定义了一些标准的UI元素，以方便地构建分层或扁平导航，还有一些元素可以构建以内容为中心的导航，例如电子书或者媒体观看类应用。游戏或者其他体验驱动的应用通常需要一些自定义的元素和行为。

**使用导航栏(Navigation Bar)帮助用户轻松访问分层内容。**导航栏的标题可以显示用户当前所处的层级，而后退按钮可以回到上一层级。想要了解更多内容，请查看[Navigation Bar](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Bars.html#//apple_ref/doc/uid/TP40006556-CH32-SW3).

**使用标签栏(Tab Bar)显示同类型的内容或功能。**标签栏很适合于扁平信息结构，可以让用户在分类之间随意切换，而不用在意当前所处的位置。想要了解更多内容，请查看<u>[Tab Bar](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Bars.html#//apple_ref/doc/uid/TP40006556-CH32-SW52).</u>

**在应用中，如果每屏显示的都是同类项或同类页，可以使用页面控件(Page Control)。**页面控件的优点是可以直观地告诉用户有多少个项目或页面，以及当前所处位置。想要了解更多内容，请查看[Page Control](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Controls.html#//apple_ref/doc/uid/TP40006556-CH35-SW6)。

**一般来说，最好能给用户提供到达每一屏的唯一路径。**如果某屏内容用户需要在不同场景下查看，可以考虑使用临时视图，例如模态视图、动作菜单或警告框。想要了解更多，请查看[Modal View](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Alerts.html#//apple_ref/doc/uid/TP40006556-CH34-SW3)、[Action Sheet](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Alerts.html#//apple_ref/doc/uid/TP40006556-CH34-SW36)和[Alert](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Alerts.html#//apple_ref/doc/uid/TP40006556-CH34-SW2)。

UIKit同时还提供了以下相关控件：

* [分段控件(Segmented Control](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Controls.html#//apple_ref/doc/uid/TP40006556-CH15-SW27))。分段控件让用户在一屏内就可以查到不同分类的内容，而不需要切换到其他屏幕。
* [工具栏(Toolbar](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Bars.html#//apple_ref/doc/uid/TP40006556-CH12-SW4))。尽管工具栏和导航栏或标签栏相似，但是工具栏不具导航作用。相反，工具栏为用户提供了可以控制当前屏幕内容的控件。

(**译者注：**上文提到的Navigation Bar, Tab Bar, Page Control, Modal View, Action Sheet, Alert, Segmented Control和Toolbar均处在iOS Human Interface Guidelines的第4章 UI Elements部分，翻译将在后续更新中放出，烦请各位耐心等候。若有需要，亦可先参考先前已翻译的iOS7 UI Elements章节：[上](https://isux.tencent.com/ios-human-interface-guidelines-ui-design-ios7-ui-1.html)，[下](https://isux.tencent.com/ios-human-interface-guidelines-ui-design-ios7-ui-2.html)。)

### 1.6 模态情境(Modal Contexts)

模态是一个承载某些连贯操作或内容的优缺点并存的模式。它可以给用户提供一种不脱离主任务的方式去完成一个任务或者获得信息，但是也会临时性的阻止用户对应用的其他部分进行交互操作。

[![20140922165024665-590x380](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162015268.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162015268.png)

理想情况下，用户可以与iOS 应用进行一种非线性的交互，所以，尽可能的减少你应用中的模态体验是最好的。通常情况，仅在以下情境可以考虑使用模态：

* 必须引起用户关注的时候
* 一个独立的任务需要完成或者很明确需要被放弃，为了避免在模棱两可的状态下遗漏用户信息的时候

**保证模态任务简单、简短和高度聚焦。**你肯定不希望用户使用模态视图时像使用应用中的一个mini应用一样。如果子任务过于复杂，用户会在进入模态情境时忽略了主要任务。在设计一个涉及视觉层次的模态任务时特别要考虑这一点，因为用户有可能迷失并且忘记如何回到之前的操作中去。如果一个模态任务必须包含不同视图的子任务，确保给用户一个独立、清晰的导航路径，并避免迂回。更多关于模态试图的信息请参考[Modal View](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Alerts.html#//apple_ref/doc/uid/TP40006556-CH14-SW3).

**始终提供明显、安全的退出模态任务的途径。**确保用户在退出模态视图时可以预期操作的结果。

**一个任务需要多层级的模态视图时，**确保用户理解点击非最高层级下的完成按钮的结果。点击一个低层级视图上的完成按钮是完成这个视图中任务的一部分，还是整个任务。因为有可能存在这种困惑，所以要尽可能避免在下级视图中添加完成按钮。

**保证提醒对话框的内容都是必要且可操作的。**提醒对话框会打断用户的体验并且要点击才会消失，所以要让用户感到提醒信息是有用的，打断是有价值的。想要了解更多请参考[Alert](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Alerts.html#//apple_ref/doc/uid/TP40006556-CH14-SW2).

(**译者注：**上文提到的Modal View与Alert均处在iOS Human Interface Guidelines的第4章 UI Elements部分，翻译将在后续更新中放出，烦请各位耐心等候。若有需要，亦可先参考先前已翻译的iOS7 UI Elements章节：[上](https://isux.tencent.com/ios-human-interface-guidelines-ui-design-ios7-ui-1.html)，[下](https://isux.tencent.com/ios-human-interface-guidelines-ui-design-ios7-ui-2.html)。)

**尊重用户关于接收通知的偏好设置。**用户会设置接收应用通知的形式，确保遵重用户的喜好设置，否则可能会触怒用户，导致其关闭应用中所有的推送通知。

### 1.7 交互性与反馈(Interactivity and Feedback)

### 1.7.1 可交互元素吸引用户点击(Interactive Elements Invite Touch)

为了暗示交互性，设计时会使用很多线索，包括点击的反馈、颜色、位置、上下文、表意明确的图标和标签等。并不需要过于修饰元素来向用户展示可交互性。

在支持3D Touch的设备上，当用户按压主屏上的图标时，背景会虚化以此来暗示可以进行更多功能的选择。

[![视频插图4](https://isux.tencent.com/wp-content/uploads/2015/10/20151020163745675.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151020163745675.png)

一个关键的颜色可以给用户提供很强的视觉指引，尤其是没有冗余的其它颜色时。为了对比，使用蓝色来标记可交互的元素，同时能提供统一的、易识别的视觉风格。

[![20140922172948543](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162023210.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162023210.png)

返回按钮使用多个线索指明其可交互并传达其功能:它出现在导航中，显示了一个指向后方的图标，使用了关键色，并且显示了上一级页面的标题。

[![视频插图6](https://isux.tencent.com/wp-content/uploads/2015/10/20151020164006886.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151020164006886.png)

一个图标或者标题提供了清晰的名称指引用户点击它。例如，地图中的标题“Flyover Tour”，“Directions to Here”，清晰的说明了用户可做的操作。结合关键色，就可以省去按钮边界或其他多余的修饰。

[![20140922173046882](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162031255.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162031255.png)

**在内容区域，必要时可以给按钮添加边界或背景。**位于栏(Bar)、动作列表(Action Sheet)和警告框(Alert)中的按钮可以不需要边界，因为用户知道在这种区域中大多数选项是可交互的。但是在内容区域，有必要使用边界或背景将按钮从其他内容中区分出来。例如，音乐，时钟，照片，App Store在一些特别的场景中使用这种按钮。

照片管理中给分享按钮增加了边框，从其他解释性文本中区分出来。

[![20140922173119490](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162037922.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162037922.png)

时钟在秒表和计时页面中给按钮增加背景来强调开始和暂停按钮，并且使按钮在易分散注意力的内容中更容易点击。

[![20140922173143910](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162042242.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162042242.png)

应用商店中使用有边界的按钮，将按钮和整个内容条区分开来，点击整条内容查看详细信息，点击按钮进行下载安装。

[![视频插图7](https://isux.tencent.com/wp-content/uploads/2015/10/20151020164556244.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151020164556244.png)

### 1.7.2 用户所知道的标准手势(Users Know the Standard Gestures)

用户使用点击、拖拽、捏合等手势与应用和他们的IOS设备进行交互。使用手势拉近了用户和设备之间的距离，并且增强了直接操纵感。用户通常期待手势在不同应用之间都是通用的。

用户在使用3D Touch时不需要学习额外的手势操作。当用户轻按屏幕并得到反馈时，很容易就能发现3D Touch提供的额外的交互方式。

[![视频插图8](https://isux.tencent.com/wp-content/uploads/2015/10/20151020170540654.jpg)](https://isux.tencent.com/wp-content/uploads/2015/10/20151020170540654.jpg)

除了用户熟悉的标准手势，iOS还定义了一些系统范围内的操作，例如呼出控制中心(Control Center)或消息中心(Notification Center)。用户可以在任意应用下都使用这些手势。

**不要给标准手势赋予不同的行为。**除非你的应用是游戏，否则重新定义标准手势会使用户迷惑，且增加使用难度。

**不要创建和标准手势功能相似的手势操作。**用户已经习惯了标准手势的行为，没有必要让用户额外学习不同的操作手势来达到同样的操作结果。

**可以用复杂手势作为完成某任务的快捷方式，但不能是唯一触达方式。**最好给用户提供一些简单，直接的方式完成某操作，即使这种方法需要他们额外地多点击一到两次。简单的手势能让用户集中于当前的体验和内容，而不是交互操作本身。

**除非是游戏，否则避免定义新的手势。**在游戏或其他沉浸式的应用中，操作手势也是有趣体验的一部分。但是在普通应用中，帮助用户达成目标要比操作本身重要的多，所以最好使用标准手势，尽量避免让用户去发觉和记忆新的操作。

**在特定的环境中，可以考虑使用多指操作。**虽然复杂的操作并不一定适用于所有应用，但对用户会花大量时间使用的应用来说可以丰富体验，例如游戏或创建内容环境。但因为非标准手势可发现性差，要尽量少用，并且不要让这类手势成为完成任务的唯一方式。

### 1.7.3 反馈有助于理解(Feedback Aids Understanding)

反馈帮助用户了解应用当前在做什么，发现接下来可以做什么以及理解他们动作产生的结果。UIKit的操作和视图提供了很多反馈类型。

**尽可能将状态或其他的反馈信息整合到UI中。**用户不进行操作或不跳出当前内容就能获得需要的信息是最好的。例如，邮箱将当前的状态显示在不影响当前内容的工具栏上。

[![20140922173243598](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162050207.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162050207.png)

**避免显示不必要的提醒对话框。**对话框是很强的反馈机制，只有在传递非常重要，且可操作的信息时才需要使用它。如果用户常看到很多没有重要信息的对话框，他们很快就会忽略所有对话框提醒。想要了解更多信息，请参考[Alert](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Alerts.html#//apple_ref/doc/uid/TP40006556-CH14-SW2).(**译者注：**Alert处在iOS Human Interface Guidelines的第4章 UI Elements部分，翻译将在后续更新中放出，烦请各位耐心等候。若有需要，亦可先参考先前已翻译的iOS7 UI Elements章节：[下](https://isux.tencent.com/ios-human-interface-guidelines-ui-design-ios7-ui-2.html)。)

### 1.7.4 输入信息的方式要简单(Inputting Information Should Be Easy)

不管用户是点击控件还是使用键盘，输入信息都会花费时间和精力。如果在发挥有用的效用前就让用户输入大量信息会减弱用户继续使用的欲望。

**让用户更容易的进行选择。**例如，使用选择器或者表格代替纯文本，因为大部分用户觉得从列表中进行选择要比打字容易的多。

[![20140922173843170-590x393](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162054216.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162054216.png)

**适时地从iOS中获取信息。**设备上存储了大量的用户信息。可以的话，不要让用户提供你可以轻易找到的信息，例如联系人或日历信息。

**提供有用的反馈来平衡用户的输入。**在使用应用的过程中，付出和回报的概念可以帮助用户感到进程在被推进。

### 1.8 动画(Animation)

细微、精美的动画遍布iOS的用户界面，他们使应用的体验更具吸引力，更具动态性。适当的动画可以：

* 传达状态和提供反馈
* 增强直接的操纵感
* 将用户的操作可视化

[![视频插图9](https://isux.tencent.com/wp-content/uploads/2015/10/20151020172751987.jpg)](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Art/animation_intro.m4v)

(译者注：以上为视频截图，完整视频请[点击观看](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Art/animation_intro.m4v))

**谨慎地增加动画，特别是在那些无法提供沉浸式体验的应用中。**过多和无理由的动画会阻碍应用的流畅性，降低性能，还会分散用户在操作中的注意力。

尤其是要有目的地，合理地应用动效和UIKit中的动态控件，并确保对结果进行测试。合理地使用动效可以提升用户的理解程度和愉悦感；应用过度使用动效会给用户带来迷惑和难以掌控的感觉。

**如果可以，保持自定义动画和内置动画的一致性。**用户习惯于内置iOS应用使用的精细动画。事实上，用户倾向于把视图之间的平滑切换，对设备方向改变的流畅相应和基于物理的滚动效果看做是iOS体验的一部分。除非，你的应用要给用户提供类似游戏应用的沉浸式体验，这种情况下自定义的动画可以区别于内置动画。

**使用风格类型一致的动画。**自定义动画之间也需要保持一致性，这样可以让用户在使用应用以之前建立的经验为基础。

**一般来说，自定义的动画要考虑动画的现实性和可信性。**人们乐意接受自由的艺术创作，但是当动效不合理或者违反物理学时，用户会感到困惑。例如，当你从屏幕顶部下滑拖出一个视图的时候，你也要上滑将它收起，因为这么做可以帮助用户记住这个视图从何而来。如果你下滑到屏幕底部关闭这个视图，用户关于从屏幕上方呼起的心理模型就会被打破。

### 1.9 品牌推广(Branding)

成功的品牌推广不仅仅包括在应用中添加品牌元素。优秀的应用应该通过创建独特的外观和感觉来为用户提供愉悦、难忘的体验。

在iOS系统之下可以很容易地使用自定义的图标、颜色和字体来创建区别于其他应用的UI。当你进行这些元素的设计时，牢记以下两点：

* 每个自定义的元素本身都需要具备良好的观感和功能性，但它也应该与应用中其他元素保持一致，无论应用中其他元素是自定义的还是标准的。
* 为了在iOS中感觉舒适，你的应用虽然不必看起来跟内置的一样，但是需要对它的遵从、清晰度和深度(如欲了解更多，参见1 为iOS而设计(Design for iOS))进行整合。花些时间弄清楚在你的应用中遵从、清晰和深度所代表的意味，并把它们在你的自定义元素中表达出来。

当你需要让用户意识到你的品牌时，你应该遵循以下几点：

**以精致优雅不唐突的方式植入品牌元素。**用户使用你的应用来完成事务或者进行娱乐，他们不希望被强迫着去观看广告。为了获得最好的用户体验，你可以通过字体、颜色和图像的设计来潜移默化地地提醒用户你的品牌身份。

[![20140922174634433-590x442](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162058243.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162058243.png)

**避免远离用户关心的内容。**不要像上图中的反例那样将仅有品牌意义的内容放在屏幕顶部二级栏上持续展示，使正文内容空间被压缩，而是考虑以其他低侵入性的方法无处不在地展示品牌，如使用自定义颜色、字体，或巧妙地定制屏幕的背景。

**抵抗住诱惑，不要把你的****logo****贯穿整个应用。**移动设备的屏幕多数相当小，logo的每一次出现都会占据空间，从而将用户与他们想看的内容隔离开。而且，在应用中显示logo并不能像在网页中显示logo那样达到相同的目的：对于用户来说通常会很容易在不知道网页所属的情况下访问一个网页，但却极少有用户会在完全不看一个iOS系统中的应用图标的情况下就打开它。

### 1.10 颜色与字体(Color and Typography)

### 1.10.1 色彩有助于增进沟通(Color Enhances Communication)

在iOS系统中，颜色会用于表明交互，传递活性以及提供视觉连续性。内置的应用程序选择使用那些看起来更具个性的、纯粹、干净的颜色，并辅以或亮或暗的背景组合。

[![视频插图13](https://isux.tencent.com/wp-content/uploads/2015/10/20151021171938542.jpg)](https://isux.tencent.com/wp-content/uploads/2015/10/20151021171938542.jpg)

**如果你要创建多样的自定义颜色，要确保它们能够和谐共存。**例如，如果你的应用的基本风格是柔和的色调，你就应该创建一个协调的柔和色调的色板用于整个应用。

**注意在不同情境下的颜色对比。**例如，如果在导航栏的背景与栏按钮标题之间没有足够的对比，按钮就会很难被用户看到。一个快速但不严谨的方法是通过将设备置于不同的光照环境之中(包括晴朗的室外)来测试设备上的颜色是否具有足够的对比度。

虽然在设备上查看你的应用能够在一定程度上帮助你找到需要调整的地方，但这仍代替不了能产生可靠结果的更科学客观的方法。这种方法涉及到判定前景色和背景色的亮度值是否符合一定的比率。这个比率值可以通过在线对比度计算器或者根据WCAG2.0标准中提供的公式自己计算获得。你应用中理想的颜色对比度应该是4.5:1或更高。

**当你使用自定义的栏颜色时，着重考虑半透明的栏和应用内容。**当你需要创建能匹配特别颜色的栏颜色时(比如一个已有品牌中的颜色)，可能在你获得你想要的结果之前，你需要用各种颜色进行实验。栏的显示将会同时受到iOS系统所提供的半透明栏与藏在栏后面的应用内容的呈现所影响。

**API****注：**使用浅色(tintColor)的属性值给予栏按钮颜色，使用栏浅色(barTintColor)的属性值为栏本身赋色。欲了解更多关于栏属性的内容，可参见[_UINavigationBar Class Reference_](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UINavigationBar_Class/index.html#//apple_ref/doc/uid/TP40006887),，[_UI__TabBar Class Reference_](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITabBar_Class/index.html#//apple_ref/doc/uid/TP40007521)，[_UIToolbar Class Reference_](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIToolbar_Class/index.html#//apple_ref/doc/uid/TP40006927)和 [_UISearchBar Class Reference_](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UISearchBar_Class/index.html#//apple_ref/doc/uid/TP40007529)_._

**注意颜色的盲区。**多数色盲的人很难区分红色与绿色。需要对你的应用进行测试以确保在其中你没有将红色与绿色作为区分两个不同状态或值的唯一方式，一些图像编辑软件或工具能够有效的帮你验证颜色的盲区。通常意义来说，使用多种方式来表征原色的交互性是非常好的(需要了解更多关于在iOS系统中表征交互性的信息，请参阅_[Interactive Elements Invite Touch](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/InteractivityInput.html#//apple_ref/doc/uid/TP40006556-CH55-SW4))_。

**考虑选择一种基准色颜色来表征交互性与状态。**内置的应用里的基准色包括比如备忘录中的黄色，和日历中的红色等等。如果你定义一种用于表征交互和状态的基准色，要确保你的应用中的其他颜色不会与它发生冲突。

**避免给可交互和不可交互的元素使用相同的颜色。**色彩是表明UI元素交互属性的方式之一。如果可交互和不可交互的元素使用相同的颜色，用户将会难以判断哪些区域是可点的。

**色彩可以向用户传达信息，但不一定会以你希望的方式。**每个人眼中的色彩是不一样的，不同的文化为色彩赋予的意义也是不相同的。花时间来研究如何使用色彩才可能会被其他国家或者文化接受。你要尽可能确定应用中运用的色彩向用户传达了恰当的信息。

**大多数情况下，不能让颜色喧宾夺主，让用户分心。**除非色彩是应用的目的和本质所在，通常情况下色彩应该用来从细微细节之处提升用户体验。

### 1.10.2 优秀的排版提供清晰的传达(Great Typography Enables Clear Communication)

Apple为全平台设计了San Francisco字体以提供一种优雅的、一致的排版方式和阅读体验。在iOS 9及未来的版本中，San Francisco 是系统字体。

San Francisco搭配Dynamic Type，可以为您提供：

* 一系列的字号大小，在任何用户设置，包括可访问性设置下，可获得优质的清晰度和极佳的阅读体验。
* 自动调整文字的粗细，字母间距以及行高的能力。
* 为语义上有区别的文本模块指定不同的文本样式，比如正文、脚注或者标题。
* 文本可以根据用户在字号设置和可访问性设置中指定字体大小的变化作出适当的响应的能力

下载San Francisco可访问 [https://developer.apple.com/fonts/.](https://developer.apple.com/fonts/)(注意：iOS9中的San Francisco字体取名为SF-UI)。当你在你的app中采用San Francisco时，你可以调整模拟器>设置中的值来测试在不同尺寸下你的app的文本。

注：如果你是用自定义字体，你仍然可以采用Dynamic Type或根据系统的字号设置来规划字体范围。当用户改变设置时，你的应用也必须响应式的配合。如需了解如何使用文字样式并确保当用户改变文字型号设置时你的应用能够获取通知，可以参考[Text Styles](https://developer.apple.com/library/ios/documentation/StringsTextFonts/Conceptual/TextAndWebiPhoneOS/CustomTextProcessing/CustomTextProcessing.html#//apple_ref/doc/uid/TP40009542-CH4-SW65).

San Francisco 有两类尺寸: 文本模式(Text)和 展示模式(Display)。 文本模式适用于小于20点(points)的尺寸，展示模式适用于大于20点(points)的尺寸。当你在你的app中使用San Francisco时，iOS会自动在适当的时机在文本模式和展示模式中切换。

**注：**如果你使用应用程序如Sketch或Photoshop来生成你的设计，那么当你设置的字体不小于20点的时候，你需要切换到展示模式。iOS会根据字体大小为San Francisco自动调整字间距。(字间距是以用作于修改文字间距)。表格10-1 和 10-2分别是文本模式(Text)和展示模式(Display) 在不同字号下的间距值。

[![视频插图9](https://isux.tencent.com/wp-content/uploads/2015/10/20151021130548308.jpg)](https://isux.tencent.com/wp-content/uploads/2015/10/20151021130548308.jpg)

[![视频插图10](https://isux.tencent.com/wp-content/uploads/2015/10/2015102113055262.jpg)](https://isux.tencent.com/wp-content/uploads/2015/10/2015102113055262.jpg)

为了突出某些文字或者为了在内容块之间建立视觉关联，你可以依赖由Dynamic Type支持的语义化样式，如标题、正文，你也可以指定字体权重，如细体或者半粗。使用 Dynamic Type样式使得你的内容能更好地表达含义，但如果你想要对你的设计有更好的把控能力，你可以对特定的文字设置特定的权重。(想要了解更多关于调整字体权重， 可以参阅_[UIFont Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIFont_Class/index.html#//apple_ref/doc/uid/TP40006891)_.)

例如，你可能想要增加某些文字的权重，来帮助用户可视化你的内容的层次结构，或者把用户的注意力吸引到特定的词或短语。另外，你可以通过增加较小文字的权重和减小较大文字的权重，在多个不同字号的、相邻的标签中建立视觉凝聚。字体权重在内容的整体风格和表达中有重要影响，因此你可以选择特定的权重来达到设计目的。

**文本尺寸的响应式变化需要优先考虑内容。**并不是所有的内容对于用户都是同等重要的。当用户选择更大的文本尺寸时，他们是想要使他们关注的内容更容易阅读；他们并不总是想要屏幕上的每个单词都更大。

例如，当用户选择具备更大易用性的文本尺寸时，邮件将会以更大的尺寸显示邮件的主题和内容，而对于那些没那么重要的信息——如时间和收件人——则采用较小的尺寸。

[![mail_message_axlarge_2x](https://isux.tencent.com/wp-content/uploads/2015/10/20151021144846744.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151021144846744.png)

**确保一个自定义字体在不同尺寸下的所有类型都具备可读性。**实现这一效果的方法之一是效仿在不同的文本尺寸下iOS系统呈现字体样式的一些方法。例如：

* 文本永远都不应该小于11点(points)，即使是用户选择极小的文本尺寸。相较而言，内容样式使用17点的字号作为大尺寸，这也是默认的文本字号。
* 通常来说，字号与行距值在每一档的文本尺寸设置中差别为1点。唯一例外的是两种标题的样式，它们在极小、小和中尺寸的设置中均使用相同的字号、行距和字距。
* 在最小的三种文本尺寸中，字间距相对较大；而在最大的三中文本尺寸中，字间距相对紧凑。
* 标题和内容的样式使用相同的字体尺寸，同时，为了区分标题与内容样式，标题样式使用更重的值。
* 导航控制栏的文本使用相同的字号，而内容文本的样式则使用大尺寸的设置(值为17点)。
* 文本总是使用常规或者中重，一般不适用轻或者加粗。

**通常情况下，应用中整体应该使用单一字体。**多种字体的混杂会使你的应用看上去支离破碎和草率。相反，使用一种字体和少数样式。根据语义用途，使用[UIFont](https://developer.apple.com/library/prerelease/ios/documentation/UIKit/Reference/UIFont_Class/Reference/Reference.html#//apple_ref/occ/cl/UIFont)类的API来定义不同文本区域的样式，比如正文或者标题。

[![20140922175243391-590x442](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162110211.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162110211.png)

### 1.11 图标和图形(Icons and Graphics)

### 1.11.1 应用图标(The App Icon)

每个应用都需要一个漂亮的图标。用户常常会在看到应用图标的时候便建立起对应用的第一印象，并以此评判应用的品质、作用以及可靠性。

以下几点是你在设计应用图标时应当记住的。当你确定要开始设计时，请参考[App Icon](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/AppIcons.html#//apple_ref/doc/uid/TP40006556-CH19-SW1)来获取更详细的设计规格与指导。(译者注：App Icon处在iOS Human Interface Guidelines的Icon and Image Design部分，翻译将在后续更新中放出，烦请各位耐心等候。)

* 应用图标是整个应用品牌的重要组成部分。将图标设计当成一个讲述应用背后的故事，以及与用户建立情感连接的机会。
* 最好的应用图标是独特的，整洁的，打动人心的，让人印象深刻的。
* 一个好的应用图标应该在不同的背景以及不同的规格下都同样美观。为了丰富大尺寸图标的质感而添加的细节有可能让图标在小尺寸时变得不清晰。

### 1.11.2 小图标(Small Icons)

iOS提供了一系列小的icon，用以代表各种常见任务与操作，它们常用在标签栏(Tab Bar)、工具栏(Toolbars)与导航栏(Navigation Bar)中。用户通常都已经了解这些内置图标的含义了，因此可以尽可能的多使用它们。

[![视频插图14](https://isux.tencent.com/wp-content/uploads/2015/10/2015102117194299.jpg)](https://isux.tencent.com/wp-content/uploads/2015/10/2015102117194299.jpg)

如果需要自定义动作或者内容，你也可以设计自定义图标。设计这些小的线性图标与设计应用图标有很大的区别，请参考[Bar Button Icons](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/BarIcons.html#//apple_ref/doc/uid/TP40006556-CH21-SW1)来了解更多内容。(**译者注：**Bar Button Icons章节处在iOS Human Interface Guidelines的Icon and Image Design部分，翻译将在后续更新中放出，烦请各位耐心等候。)

请注意，你有时候也可以用文字来代替工具栏和导航栏的图标。 就像iOS的日历里面，工具栏上便是使用”今天”,”日历”和”收件箱”来代替图标进行表意的。

[![text_in_toolbar_2x](https://isux.tencent.com/wp-content/uploads/2015/10/20151021151546839.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151021151546839.png)

想要决定在工具栏和导航栏中到底是用图标还是文字，可以优先考虑一屏中最多会同时出现多少个图标。同一屏幕中图标的数量过多可能会让整个应用看起来难以理解。使用图标还是文字还取决于屏幕方向是横向还是纵向，因为水平视图下通常会拥有更多的空间，可以承载更多的文字。

### 1.11.3 图形(Graphics)

iOS应用大多数图形丰富。无论是你需要展示用户的照片，还是需要创建自定义图片，以下这些需求都应该遵守：

* **支持****Retina****显示屏。**确保你应用中的所有图片资源都提供了高分辨率规格。尤其需要注意的是，iPhone 6 Plus需要提供@3x规格的图片，而所有其他的高分辨率iOS设备都需要提供@2x规格的图片。
* **显示照片或图片时请使用原始尺寸，并不要将它拉伸到大于****100%****。**你不会希望在你的应用中看到拉伸和变形的图片。可以让用户自己来选择他们是否想要缩放图片。

**不要使用从苹果系列产品中复制的图形。**这些图形均受版权保护，而且产品的设计可能会频繁改变。

**不要将苹果的应用图标，图像或者截图用于你的设计中。**所有苹果的设计均受版权保护并且不允许出现在你的UI中，除非它们是由系统直接提供的。

### 1.12 术语和措辞(Terminology and Wording)

你在应用中呈现的每一个字都是与用户进行对话的一部分。把握这样的对话机会，为你的用户提供清晰的表意与愉悦的体验。

设置是面向全体用户的一个基础应用，因此它使用了简明扼要的语言来描述用户可以进行的操作。举个例子，设置→勿扰模式(Do Not Disturb)就没有使用难以理解的复杂技术术语，而是用了简单的语言，给用户描述了里头的一系列操作。

[![20140922180325192](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162122290.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162122290.png)

**保证你使用的术语是用户能理解的。**根据你对用户群的理解来决定在应用中使用什么样的词汇。举个例子，在一款针对小白用户的应用中使用技术术语是不合适的，但对于针对高端用户的应用来说，使用技术术语是很自然的事情。

**使用非正式的友好语气，但不需要太过卑微。**避免太正式太僵化，或者太过嘻嘻哈哈，傲慢无礼。请记住，用户可能会反复阅读这些文本，因此有些起初看上去很俏皮的语句，多看几次之后可能会显得烦人。

**像新闻编辑一般遣词造句，避免不必要的冗余语句。**当你的文案足够简明扼要，用户就可以很轻松地阅读和理解它。确定最重要的信息，精炼它并且突出它，让用户不需要读一大段文字才能了解他们在找什么，以及下一步要做什么。

**给控件加上短标签或者容易理解的图标。**让用户只扫一眼就能知道这个控件是干什么的。

**描述时间时要注意准确性。**今天和明天这些词汇确实显得比较友好，但有时候会让用户费解，因为你可能没有办法确定用户当前的时区和时间。举个例子，假如有一项活动会在半夜12点前开始，对于在同一个时区的用户而言，这个活动是在今天开始的，但对于那些在早一点的时区里的用户而言，这个活动在昨天就已经开始了。

**为你的应用写一则漂亮的App Store描述，最大程度地把握住这个与潜在用户沟通的绝佳机会。**除了准确描述你的应用、强调应用的品质与亮点以外，你还需要：

* **修正所有的拼写、语法与标点符号错误。**这些小错误也许不会影响用户正常使用，但是可能会让他们对应用的整体品质产生负面印象。
* **尽量少用全大写的词汇。**虽然大写单词有时候可以吸引注意力，但是全大写的段落不适合阅读，而且会产生一种朝用户扯着嗓子吼的感觉。
* **可以描述****bug****修复情况。**如果您的应用新版包含用户一直期待的bug修复，那在你的软件描述中提到这一点就是个很好的做法。

### 1.13 与iOS的整合(Integrating with iOS)

与iOS整合，指的是在当前平台上给用户提供一种舒适的、宾至如归般的体验，当然这并不意味着我们要把每一个应用做的和内置应用一模一样。

最好的与iOS整合的方式便是深刻地了解iOS的主题与核心——这一部分在上文为iOS而设计(Designing for iOS)部分中已有详细描述，并寻求出如何在你的应用中融合与表达这种主题。当你这么做的时候，遵循本章中的指引可以帮助你为你的用户提供他们想要的体验。

### 1.13.1 正确使用标准UI元素(Use Standard UI Elements Correctly)

尽可能使用UIkit提供的标准UI元素是一个好主意。多使用标准元素而非自定义元素，你与你的用户都将受益：

* 标准UI元素会根据iOS官方的更新而自动更新——而自定义元素不会。
* 标准UI元素对于你自定义外观和行为来说拥有优秀的扩展性。举个例子，iOS中所有的视图(Views，从[UIView](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIView_Class/index.html#//apple_ref/occ/cl/UIView)中继承的对象)都是可以使用[TintColor](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIView_Class/index.html#//apple_ref/occ/instp/UIView/tintColor)属性来定义颜色的，它让应用配色变得很简单。
* 用户更熟悉和习惯标准的元素，因为他们可以立刻明白你的应用中这些元素的用途。

想要充分地利用标准UI元素的优点，有一些关键点需要特别注意：

**严格遵循每个****UI****元素的设计规范。**当你应用中的UI元素的外观与功能都是用户所熟悉的，他们可以很容易地根据先前的经验来使用他们，进而更好地使用你的应用。你可以从这些章节中找到各种UI元素的设计规范：[Bars](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Bars.html#//apple_ref/doc/uid/TP40006556-CH12-SW1), [Content Views](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/ContentViews.html#//apple_ref/doc/uid/TP40006556-CH13-SW1), [Controls](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Controls.html#//apple_ref/doc/uid/TP40006556-CH15-SW1), [Temporary Views](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Alerts.html#//apple_ref/doc/uid/TP40006556-CH14-SW1).

(译者注：上文提到的章节均处在iOS Human Interface Guidelines的第4章，翻译将在后续更新中放出，烦请各位耐心等候。若有需要，亦可先参考先前已翻译的iOS7 UI Elements章节：[上](https://isux.tencent.com/ios-human-interface-guidelines-ui-design-ios7-ui-1.html)，[下](https://isux.tencent.com/ios-human-interface-guidelines-ui-design-ios7-ui-2.html)。)

**不要混用不同版本的****iOS****里的****UI****元素。**你一定不希望让用户觉得你的UI元素来自于与当前用户的设备版本不同的iOS系统。

**大体来说，请避免创造自定义****UI****元素来表现标准交互行为。**先问问你自己为什么一定要创建一个与标准UI元素行为完全相同的自定义元素。如果你只是想改变标准UI元素的外观，可以考虑使用UIKit外观定制API(UIKit appearance customization APIs)，或者给元素填充别的颜色。如果你需要定义一个与标准控件稍有不同的行为，请确保你在改变了这个UI元素的属性和行为之后，这个元素仍然能完成你所希望的操作。如果你需要完全自定义一个行为，最好是设计一个与标准元素完全不相像的自定义元素。

提示：Interface Builder让获取标准UI元素，使用外观定制API(the appearance customization APIs)，获取属性，以及在你的应用里使用自定义和系统自带图标变得很简单。想要了解更多Interface Builder的内容，请参阅_[Xcode Overview](https://developer.apple.com/library/ios/documentation/ToolsLanguages/Conceptual/Xcode_Overview/index.html#//apple_ref/doc/uid/TP40010215)_.

**不要用系统自带的按钮和图标表达其他含义。**iOS提供了多种可用的按钮和图标。请确认你了解它们的准确表意；不要单纯凭借你看到这些图标样式的猜测和理解来解读和使用它们。(你可以在[Toolbar and Navigation Bar Buttons](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Bars.html#//apple_ref/doc/uid/TP40006556-CH12-SW33)和[Tab Bar Icons](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Bars.html#//apple_ref/doc/uid/TP40006556-CH12-SW34)中了解到这些按钮和图标的准确含义。)

如果你所需要的功能无法用系统提供的按钮和图标来表现，你也可以设计自定义按钮。自定义按钮的设计可以参考 [Bar Button Icons](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/BarIcons.html#//apple_ref/doc/uid/TP40006556-CH21-SW1).

(译者注：上文提到的章节均处在iOS Human Interface Guidelines的第4章，翻译将在后续更新中放出，烦请各位耐心等候。若有需要，亦可先参考先前已翻译的iOS7 UI Elements章节：[上](https://isux.tencent.com/ios-human-interface-guidelines-ui-design-ios7-ui-1.html)，[下](https://isux.tencent.com/ios-human-interface-guidelines-ui-design-ios7-ui-2.html)。)

**如果你的****app****是沉浸式体验，那么创造全新的自定义****UI****是合理的。**因为你在创造一个统一的体验环境，让用户在其中能够有所期待并探索如何控制应用。

### 1.13.2 弱化文件和文档处理(Downplay File and Document Handing)

iOS应用可以帮助用户创建和处理文件，但这并不意味着用户需要过分考虑iOS设备的文件系统如何运作。

如果你的应用中支持用户创建和编辑文档，那么提供一个清晰的图形库视图(document library view)让用户能够方便地打开或者新建文档是一个好的做法。理想状况下，这样的图形库视图拥有以下特征：

* **高度图形化。**用户通过屏幕上的缩略图就可以一目了然，快速找出自己想要的文件。
* **让用户用最少的动作完成自己的任务。**比如说，用户可以快速地水平滚动文件列表，然后轻点一下自己想要的文件来打开它。
* **包含新建文档功能。**一个图形库视图应该支持让用户点击一个新建文档的占位图便完成新建文档操作，而不是让用户通过访问别的地方来新建文档。

举个例子，Pages的图形库视图里面，既展示了用户已存在的文档，也加入了便捷的新建文档操作。

[![20140922180411133-590x293](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162126242.png)](https://isux.tencent.com/wp-content/uploads/2015/10/20151019162126242.png)

提示：你可以使用Quick Look Preview功能来让用户预览你的应用中的文件，哪怕你的应用不能打开这些文件。想要了解如何在你的应用中提供这个功能，请参阅[Quick Look](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/QuickLook.html#//apple_ref/doc/uid/TP40006556-CH43-SW1).

如果你的应用允许用户使用在其他应用中创建的文档，你可以通过模态文档选择视图控制器(modal document picker view controller)来帮助用户触达它们。这个控制器可以提取用户在iCloud中的文档，还可以通过文档提供者扩展(Document Provider extensions)来提取在其它应用中创建和储存的文件。想要了解更多文档提供者扩展的内容，可以参考[Document Provider Extensions](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/AppExtensions.html#//apple_ref/doc/uid/TP40006556-CH67-SW5); 想要了解更多文档提取视图控制器，请参考[_Document Picker Programming Guide_](https://developer.apple.com/library/ios/documentation/FileManagement/Conceptual/DocumentPickerProgrammingGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP4001445).

**给用户足够的信心，让他们相信除非主动取消或者删除，他们的成果会被随时妥善保存****。**如果你的应用帮助用户创建于管理文档，不能要求用户每次都能及时保存。无论是打开另一个文档或切换应用的时候，iOS应用都应当承担起帮助用户保存输入内容的责任。

如果你的应用的主要功能不是创造内容，但又允许用户查看或编辑信息，这种情况下你需要询问用户是否要保存修改。在这种场景下，比较好的做法是提供“编辑”按钮，点击后进入编辑状态，同时编辑按钮变成“保存”和“取消”按钮，这种变化可以提示用户当前处于编辑模式。“保存”可以保留修改内容，“取消”则退出编辑模式。

### 1.13.3 必要时提供可配置选项(Be Configurable If Necessary)

某些应用需要用户手动安装或设置选项，但是大部分应用不需要如此。一个好的应用可以让大部分用户快速上手，并通过主界面给用户提供便捷的调整体验的方式。

当你的应用在默认状态下就能满足大部分用户的期望，用户对设置的需求就减少了。如果你需要储存用户的基本资料，可以优先向系统请求和拉取相关信息，而不是上来就让用户自己填写它。如果你一定要提供用户鲜少用到的设置项，请参考[_App Programming Guide for iOS_](https://developer.apple.com/library/ios/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40007072)中的[The Setting Bundle](https://developer.apple.com/library/ios/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/Inter-AppCommunication/Inter-AppCommunication.html#//apple_ref/doc/uid/TP40007072-CH6-SW7)部分来了解如何在代码中定义它们。

**尽可能在主UI中提供设置选项。**如果这个设置项代表着用户一个基本任务，又或者用户在进行主线任务时有可能频繁改变设置，那么将设置项放在主UI中会很方便。如果用户只是偶尔才会用到设置项，那么可以将其放在独立的视图中。

**如果应用内相关设置需要在系统设置中改变，帮助用户直接访问系统设置。**尤其是，如果你要用一段文字来描述如何改变这个设置，比如“设置>隐私>定位服务”，倒不如直接放置一个按钮，点击后即可到达设置中的定位服务。想要了解如何实现，请参考 [Settings Launch URL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html#//apple_ref/doc/constant_group/Settings_Launch_URL).

### 1.13.4 充分利用iOS技术(Take Advantage of iOS Technologies)

iOS提供了丰富的技术方式来支持用户完成他们所期望的各种任务和场景。这意味着在绝大多数情况下，将系统提供的技术整合到你的应用中，往往比自定义一种新的技术更为可靠。

某些iOS技术，比如多任务并行([Multitasking](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Multitasking.html#//apple_ref/doc/uid/TP40006556-CH38-SW1))与语音向导([VoiceOver](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/VoiceOverAccessibility.html#//apple_ref/doc/uid/TP40006556-CH45-SW1))等等，是所有应用都应该包含的系统级特性。而另外一些技术是否整合到应用中，则取决于应用本身的功能性。比如处理门票和礼品卡的应用([Wallet](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Passbook.html#//apple_ref/doc/uid/TP40006556-CH33-SW1))支持用户在应用内内购([In-App Purchase](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/InAppPurchase.html#//apple_ref/doc/uid/TP40006556-CH36-SW1))，展示应用内置广告([iAd Rich Media Ads](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/iAdRichMediaAds.html#//apple_ref/doc/uid/TP40006556-CH41-SW1))则可以整合 [Game Center](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/GameCenter.html#//apple_ref/doc/uid/TP40006556-CH37-SW1)，同时支持[iCloud](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/iCloud.html#//apple_ref/doc/uid/TP40006556-CH35-SW1).

## 2. 设计策略

### 2.1 设计原则(Design Principles)

### 2.1.1 美学完整性(Aesthetic Integrity)

美学完整性不评判应用的视觉设计，也不是用来描述应用的风格特征。美学完整性是指在一款应用的视觉表现和交互行为与功能结合后所传达出的整体一致性。

[![aesthetic_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151102205944549-590x307.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151102205944549.png)

人们关心应用是否提供了应有的功能，但是也会潜移默化甚至是很直接地被应用的视觉表现和交互行为所影响。举个例子，一款协助用户完成任务的应用，可以通过使用精美而又无干扰的装饰性元素、标准的控件和可预期的交互行为很好地帮助用户聚焦在任务本身上。这样，应用就能传达出清晰而一致的信息，使得人们信任它。但是，如果应用使用干扰的、琐碎的或随意的UI来呈现任务，那么人们可能会对其可靠性和可信赖度产生怀疑。

另一方面，在沉浸式应用中—例如游戏—用户期待惊艳的视觉表现，为用户带来乐趣和刺激，并鼓励用户进行探索。用户不是要在游戏中完成严肃的或程序式的任务，他们更期待游戏的视觉表现和交互行为与当前的目的进行整合。

### 2.1.2 一致性(Consistency)

一致性可以让人们在一款应用中的不同部分甚至不同应用间复用使用同样的认知和技能。一款具备一致性的应用不应盲从地复制其他应用，也不应在风格上一成不变。相反，它们专注于让人们觉得舒适的标准和范例，并提供应用内部统一的体验。

[![consistency_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210013279-590x235.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210013279.png)

在判断一款iOS应用是否要遵守一致性原则时，请思考如下问题：

- 应用是否和iOS标准一致？是否正确地使用了系统提供的控件、视图和图标？是否按照用户所预期的方式整合了设备的特性？
- 应用是否内部统一？文案是否使用了一致的措辞和风格？同样的图标是否表意相同？在不同的位置执行同样的操作时，人们是否能能预期会发生什么？应用中自定义的UI元素是否在外观和行为上保持一致？
- 应用是否和先前的版本保持一致？条款和意义是否保持不变？基本概念和主要功能是否发生了变化？

### 2.1.3 直接操作(Direct Manipulation)

当人们不再使用一堆控件进行操作，而是直接在屏幕上操作对象时，他们能更集中精力完成任务，也更容易理解这些行为所产生的结果。

[![manipulation_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210039758-590x287.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210039758.png)

使用多点触摸界面，人们可以通过捏合操作来直接放大和缩小图片或文本内容。在游戏中，玩家可以直接与屏幕上的对象进行交互。例如，游戏中可能会显示密码锁，用户可以通过转动它来打开。

在一款iOS应用中，如下情况中人们应该能够进行直接操作：

- 旋转或者移动设备来影响屏幕上的对象
- 使用手势来操作屏幕上的对象
- 显示即时可视的操作反馈

### 2.1.4 反馈(Feedback)

反馈可以明示人们的行为，呈现操作结果，并更新于任务进程之中。

[![feedback_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210115815-590x386.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210115815.png)

 

iOS内置的应用对用户的每个行为都提供了可感知的反馈。当人们点击列表项和控件时，它们会被临时高亮，并会在操作过程中持续一段时间，以此展示控件被执行的过程。

精细的动画会给人们带来有意义的反馈，帮助阐明行为的结果。例如，列表中新增一项时的动画可以从视觉上帮助人们发现列表的变化。

音效同样可以为人们提供有效的反馈，但不应成为唯一的反馈方式，因为人们不一定能听到。

### 2.1.5 隐喻(Metaphors)

当应用中的虚拟对象和交互行为与用户已经熟悉的体验相似时—无论这些体验是来源于真实或数字生活—用户就可以快速地掌握如何来使用这个应用。

当应用使用隐喻来传达某种用法或体验时，最好不要让隐喻突破所依赖的对象或交互行为本身的限制。(译者注：此处可理解为对于隐喻的使用应量力而为，不要过于牵强。)

由于人们实际上是和屏幕进行物理上的交互，所以iOS应用有很大的余地来使用隐喻。iOS中的隐喻包括：

- 移动分层视图来显示被遮挡的内容
- 拖曳、轻扫和滑动游戏中的对象
- 点击开关，滑动滑块，转动选择器
- 轻扫来翻阅书本或杂志

### 2.1.6 用户控制(User Control)

是人—而不是应用—发起和控制行为。应用可以对用户进行操作建议，对有危害的后果予以警示，但是不应替用户来做决策。好的应用会在用户需要时给予帮助和避免不必要的结果之间作出平衡。

[![user_control_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210148356.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210148356.png)

当对应用的交互行为和控件都较为熟悉和可预期时，用户会觉得应用更易上手。那些简单直白的交互行为更容易被用户所理解和记住。

人们会希望在一个操作被执行之前有足够的机会来取消，也希望在执行一个不可逆的操作之前可以有机会来进行确认。最后，人们还会希望能够停止正在执行中的操作。

 

### 2.2 从概念到产品(From Concept to Product)

### 2.2.1 定义应用(Define Your App)

应用的定义是对应用主要功能和目标用户的简明具体的描述。

尽可能早的创建应用的定义可以帮助你将一个想法和功能清单转换为用户想要的条理清晰的产品。在开发过程中，可以使用定义来决定某些功能和行为是否合理。使用以下几个步骤来创建一个可靠的应用定义。

**1.列出所有你认为用户可能喜欢的功能**

可以直接进行头脑风暴。此时，你需要列出所有与产品核心想法有关的任务。不用担心清单太长，因为接下来会进行删减。

假设你一开始的想法是开发一个帮助人们购买食品杂货的应用。你可以思考在进行这项活动时，会涉及到那些相关的任务，这些就是用户可能感兴趣的潜在功能。例如：

- 创建清单
- 查找食谱
- 比较价格
- 定位商店
- 给食谱做注释
- 查找并使用的优惠劵
- 查看烹饪演示
- 探索不同的烹调方法
- 寻找某些食材的替代物

**2.****确定目标用户**

现在你需要清楚的将你的应用用户与其他iOS用户区分开来。确定在此情此景下，什么是对你的用户最重要的。在食品杂货例子中，你可能需要问问你的用户：

- 通常是在家里做饭还是更喜欢现成的食物
- 是忠实的优惠券用户还是认为优惠券没多大价值
- 喜欢寻找特别的食材还是喜欢基本食材
- 严格的按照食谱做菜还是只把食谱当做灵感来源
- 喜欢少量多次购买还是一次性购买大量食物
- 希望能保留多个不同目的的购物清单还是只希望记录回家路上需要购买的几个东西
- 坚持使用固定的品牌还是会使用方便的替代品
- 习惯于购买固定的一些物品还是会按照食谱来购买

思考过这些问题之后，假设你可以提取出目标用户的三个特征：喜欢按照食谱进行尝试，时常很匆忙，通常情况下比较节俭。

**3.****根据目标用户过滤功能清单**

如果在确定了一些用户特征后，你最终得到几个主要功能，恭喜你在做正确的事情：好的iOS应用应该是高度聚焦在能帮用户完成的任务上的。

例如，即使第一步想出的那些可能需要的功能都是有用的，也不一定是第二步定义的目标用户需要的。

当你在目标用户的使用情境下检查功能清单时，就可以判断你的应用应该聚焦在三个主要功能上：创建清单，获得并使用优惠劵，获得食谱。

此时你就可以给出应用定义了，总结该应用为谁做和做什么。食品杂货购买应用的定义可能如下：

“为热爱烹饪且节俭的用户订制的创建购物清单工具。”

**4.****不止于此**

应用定义应该贯穿于整个开发过程，使用应用定义确定功能，控件，措辞的合理性。例如：

**当你想要新增一个功能时**，问问自己这对应用的主要目的和目标用户是否非常重要。如果不是，可以置之不理。例如，你已经确定了你的用户对大胆新颖的烹饪方法感兴趣，那么着重展示盒装蛋糕和现成的食物就不太合适。

**当你考虑用户界面的外观和操作时**，问问你自己你的用户更喜欢简单的、流线型的风格，还是有明显主题的风格。以用户目标为指导，理解用户期望通过你的应用完成什么，例如快速找到答案，找到深入而全面的内容或者娱乐。例如，尽管你的食品杂货清单应用需要易于理解和快速上手，但你的用户还是可能倾向于一个有关食物的主题界面。

**当你考虑应该使用怎样的措辞时，**考虑用户在这个领域的专业程度。例如，尽管你的用户可能不是由专业的大厨组成，但你也可以肯定他们希望看到有关食材和技术专用的措辞。

### 2.2.2 为任务量身订制界面(Tailor Customization to the Task)

最好的iOS应用根据清晰的目标和易用性来平衡用户界面的设计。为了达到这种平衡，要确保在设计阶段前期就考虑定制化。因为考虑品牌性，原创性和适销性通常会影响定制化的决策，所以专注于定制化怎样影响用户体验是难的。

开始考虑应用中的任务：用户执行这些任务的频率如何，在什么样的环境下进行？

举个例子，想象一个计算器应用使用的是精心设计的，充满艺术感的风格，并且使用了创新的层级去显示大家熟悉的计算元素。这像艺术品一样的细节渲染和创新层级并不会影响用户去理解怎样点击按钮和查看计算结果。但是对于只是简单的需要完成工作的用户，这种新奇的体验和美丽的界面很快就会失去效用，并且可能成为一种妨碍。

[![fancy_calculator_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210520761.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210520761.png)

相反，随身录音室应用(GarageBand)可以不展示好看的、逼真的乐器来帮助用户制作音乐，但这样会使应用缺少身临其境的愉悦感。在随身录音室里，界面不只是向用户展示了如何使用，同样使得制作音乐的主任务更容易完成。

[![completely_custom_garageband_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210543478-590x333.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210543478.png)

当你思考定制化如何增强或减弱用户完成任务的注意力时，记住以下几点：

**定制总要有缘由。**理想情况下，定制化的用户界面能促进用户完成任务并增强他们的体验。你最好尽可能的用任务驱动定制化决策。

**尽量避免增加用户的认知负担。**用户对标准界面元素的外观和行为都已经很熟悉了，所以他们不用停下来思考如何使用它们。当用户面对外观和行为与标准不同的元素时，他们就失去了经验的优势。除非你的独一无二的元素能够使任务更容易完成，否则用户很可能不喜欢被强制学习一些在其他应用都不通用的步骤。

**保持内部的一致性。**你的应用中自定义元素越多，保持这些元素外观和行为的一致性就越重要。如果用户花费时间去学习了你创建的那些不熟悉的控件，那么他们会希望新学到的这些操作能够在整个应用中通用。

**总是以内容为重点。**因为标准元素很熟悉，所以它们不会分散用户在内容上的注意力。当你自定义用户界面时，注意确保界面元素不会抢走用户对内容的注意力。例如，如果你的应用允许用户观看视频，你可能选择设计一个自定义的重播控件。但是不管你用的是自定义还是标准的重播控件，都没有它是否在用户开始观看后隐藏点击屏幕后出现来的重要。

**在对标准控件进行重设计时再三思考。**如果你不只是想自定义标准控件，而是想重设计，确保你的重设计能提供尽可能多的信息。例如，你设计了一个开关控件，它没有可以指明相反状态存在的信息，那么用户很可能意识不到这是个有两个状态的控件。

**一定要彻底测试自定义的界面元素。**在测试过程中，近距离的观察用户是否能预测你的元素如何使用以及是否能容易的与它们交互。例如，如果你创建的控件的可点击区域小于44 x 44像素，用户点击时就会有困难。或者如果你创建了一个视图对点击和滑动的反馈不一样，确保这个视图提供的功能值得用户去额外关注交互的不同。

### 2.2.3 原型 & 迭代(Prototype & Iterate)

在你投入工程资源实现设计之前，最好先创建原型来进行用户测试。即使只有几个同事来帮你测试原型，你也会收获一些关于应用功能和用户体验的新鲜观点。

在设计的早期阶段，你可以使用纸质的原型或者线框图去呈现主要的视图和控件，并且标明每个页面之间的跳转关系。你可以从线框图测试中获得一些有用的反馈，但是线框图的稀疏性有可能会误导用户。因为用户很难想象当线框被实际内容填满时体验会有什么样的变化。

如果你有一个可以在设备上运行的原型，那你可以得到更多有用的反馈。当用户能在设备上与你的原型进行交互时，他们能更容易的发现应用中哪里功能不满足预期，哪里体验过于复杂。

创建可靠原型的最简单的方法是使用基于故事版的Xcode模板创建一个基础应用，然后使用一些类似于占位符的内容来进行填充。(故事版可以涵盖应用中的所有界面，并且包括界面之间的跳转关系。)接着，将这个原型导入到设备中，这样被测者就可以有一个尽可能真实的体验了。

你不需要在原型中提供大量的实际内容或者使每一个控件都可用，但是你确实需要营造足够的情境来保证真实的体验。并且需要在典型用户体验和非典型的边缘情况之间做好平衡。例如，如果你的应用需要处理很长的列表项，你的原型就不能只显示一两个条目。而且在用户测试交互中，只要被测者能够点击屏幕上的一个区域进入到下一个逻辑页面或者完成主任务，那他们就可能提供更有建设性的反馈。

当你使用Xcode应用模板来创建原型时，你可以免费使用很多功能，并且它可以相对容易的进行设计中的响应反馈调节。在你确定设计方案并投入资源进行实现之前，应该对原型进行多次迭代测试。想要开始学习Xcode，请参考[Xcode Overview](https://developer.apple.com/library/ios/documentation/ToolsLanguages/Conceptual/Xcode_Overview/chapters/about.html#//apple_ref/doc/uid/TP40010215).

 

### 2.3 案例学习：从桌面到iOS(Case Study: From Desktop to iOS)

### 2.3.1 iPad版Keynote应用(Keynote on iPad)

桌面版的Keynote 应用是一个十分强大而又灵活的应用，可以创建非常优秀的幻灯片。人们喜爱Keynote将简单易用与细粒度的操作结合进而控制无数精确细节的方式，如动画和文本属性等。

[![keynote_desktop_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210617922-590x356.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210617922.png)

iPad版的Keynote提取了桌面版Keynote的核心要素，并通过创造以下的用户体验使它在iPad上更舒适：

- 专注于用户输入的内容
- 通过削减功能降低系统的复杂度
- 提供有用而又令人愉悦的快捷操作
- 延续桌面版本的体验
- 利用动人的动画提供良好的反馈与交流

Keynote用户能很快理解如何使用iPad版，是因为它使用了iPad原生的范例，符合了用户对功能上的预期。新用户可以用简单、自然的方式直接操控内容，所以可以很容易学会如何使用iPad版的Keynote.

Keynote从桌面版向iPad版的转变是基于从细节到整体的大量修改和重新设计的。以下是一些明显的修改：

**流线型的工具栏。**工具栏中只有少数的元素，但是它们是用户在创建内容时所需的所有功能和工具的统一入口。

[![keynote_toolbar_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210649867-590x25.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210649867.png)

**简化并优先响应用户焦点的检查器。**对于用户所选的需要修改的对象，iPad版的Keynote能自动控制其工具和属性。(译者注：特别是根据当前的操作对象而有限选择某些工具。)通常，人们可以在第一检查器视图中完成他们需要的所有修改操作。如果他们需要修改那些不常用的属性，他们可以下拉另一个检查器视图来进行。

[![keynote_inspector_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210710109.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210710109.png)

**丰富的预设样式集。**人们可以利用预设的样式很简单地改变对象(如表格或图表)的外观或者感觉。除了颜色之外，每个集中，例如表格的标题和轴区分标识等的预设属性都被设计得与整体的主题和谐一致。

[![keynote_presets_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210729757.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210729757.png)

**直接操作内容，丰富有意义的动画。**在iPad版的Keynote中，用户可以拖动滑块到一个新的位置，可以扭动旋转一个对象，也可以轻击图片来选中它。iPad版Keynote的响应动画进一步加强了这种可直接操作的印象。例如，用户在移动某个滑块时它通常会暂停，而当它被放置在一个新的位置时，环绕在周围的滑块将会向外扩散给它留出空间。

### 2.3.2 iPhone版邮件应用(Mail on iPhone)

邮件应用是OS X中一款好用而又广受好评的常见应用。它也是一个很强大的程序，可以允许用户撰写、接收、分类和存储邮件，追踪行动和事件，也可以编写备忘录和邀请等。桌面版的邮件应用通过一系列的窗口提供了这些强大的功能。

[![ds_mailondesktop](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210759227.jpg)](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210759227.jpg)

iPhone版的邮件专注于桌面版邮件的核心功能，帮助人们接收、撰写、发送和组织他们的信息。为了塑造移动iPhone版的邮件应用，将这些功能浓缩在为其量身定制的界面之中，做了如下的工作：

- 将人们的内容前置和居中的合理化呈现
- 专为处理不同任务而设计的不同视图
- 易于浏览并符合认知的信息结构
- 适时提供强大的编辑和组织性工具
- 用微妙且动人的动画来传达动作和提供反馈

必须明白的是，相对于桌面版的邮件应用来说，iPhone版的邮件应用不是(注：或者说并不需要是)一个更好的应用，而是为移动端用户重新设计的邮件应用。iPhone版的邮件应用专注于桌面版的功能子集并将它们呈现在一个吸引人的精简界面之中，据此为移动端的用户提供了核心的邮件体验。

为了使邮件应用的体验能适应移动场景，iPhone版的邮件应用在几个关键的方面革新了用户界面。

**直接、高度专注的页面。**每个页面显示了邮件应用体验的一个方面：账户列表、邮箱列表、消息列表、消息查看和编辑视图。用户可以在一个屏幕内滑动查看完整的内容。

[![ds_mailscreens_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210832802-590x321.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151102210832802.png)

**简单、可预期的导航。**通过每屏的一次点击，用户可以逐层展开综合内容(账户列表)进入具体页面(一封消息)。每个页面会显示一个标题用以指示用户所在的位置，以及一个返回按钮用以更容易地回溯到他们之前的步骤。

**需要时即可获取的、简单的点击性控件。**基本上在任何场景之下，编写邮件和查阅新邮件都是人们首要希望进行的操作，因此iPhone版的邮件应用保证了这两个功能在多个页面中都可以便利地进行。当用户查看一封消息时，就会显示诸如回复、移动和删除等对消息的操作。

**针对不同任务的不同类型的反馈。**当人们删除一封消息时，它会动态地进入垃圾桶图标中。当人们发送一封消息时，可以看到它的发送过程；而当发送结束时，人们可以听到一个特别的声音提示。通过消息列表页面工具栏的副标题，用户通过简单一瞥就可以查看邮箱上次更新的时间。

### 2.3.3 iOS系统内的网页内容(Web Content in iOS)

iOS版的Safari应用在iOS设备上提供了出众的移动网页浏览体验。人们喜欢阅读清晰的文字和图片，也希望能通过旋转设备或者捏合和点击屏幕来调整视图。

基于标准建立的网站可以在iOS设备上显示得很好。特别是那些能侦测设备并不需要插件的网站可以同时在iPhone和iPad上都表现得很好，两者之间不会需要太多的修改，即使有也很小。

除此之外，成功的网站应具备以下的特性：

- 如果页面宽度需要匹配设备宽度，可以设置合适的视窗(viewport)来适应设备
- 避免CSS中固定的定位，以便当用户缩放或拖动页面时内容无法被移出屏幕
- 拥有一套基于触控操作的用户界面，而不是依赖基于传统点击操作的交互

有时候，额外的一些修改可以(使页面)更合理。例如，在iOS系统中，很多网页应用会设置合适的视窗(viewport)宽度并通常隐藏Safari的UI。如欲了解如何进行这些修改，参见[Safari Web Content Guide](https://developer.apple.com/library/ios/documentation/AppleApplications/Reference/SafariWebContent/UsingtheViewport/UsingtheViewport.html#//apple_ref/doc/uid/TP40006509)章节中的[Configuring the Viewport](https://developer.apple.com/library/ios/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html#//apple_ref/doc/uid/TP40002051-CH3)和[Configuring Web Applications](https://developer.apple.com/library/ios/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html#//apple_ref/doc/uid/TP40002051-CH3).

网站也可以通过其他的方法适配桌面网页到iOS端的Safari浏览器中：

**使键盘适应****iOS****端的****Safari. **当键盘和格式辅助信息出现时，iPhone上的Safari应用会将你的网页显示在URL地址下方和键盘与格式辅助信息上方。

**使弹出式菜单适应****iOS端的Safari.**在桌面版的Safari应用中，弹出式菜单会包含很多选项，就如在其他OS X应用中一样。在必要的情况下，菜单展开后可以超出应用窗口的边界以显示其中的所有选项。在iOS版的Safari应用中，弹出式菜单由原生的元素所呈现，这样能提供更好的用户体验。例如，在iPhone上，弹出式菜单会出现在选择器(picker)当中，选择器里会一个用户可选择的选项列表。(欲了解更多选择器控件的内容，可以参见[Picker](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Controls.html#//apple_ref/doc/uid/TP40006556-CH15-SW23).)

## 3. iOS 技术

### 3.1 3D触摸(3D Touch)

3D Touch 给 iOS 9 用户提供了一个新的交互维度。在所支持3DTouch的设备上，人们可以通过按压应用的图标去快速选择应用定制的操作。在应用内，人们可以使用多种按压操作去获取一个项目的预览，可以在独立的视图里打开一个项获取相关操作。(了解更多在你的代码中如何添加3D Touch支持，参阅 _[Adopting 3D Touch on iPhone](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/Adopting3DTouchOniPhone/index.html#//apple_ref/doc/uid/TP40016543) .)_

### 3.1.1 轻压和重压(Peek and Pop)

轻压让用户可以在不离开他们当前环境的情况下预览一个项和执行相关操作。支持轻压的该项会在轻压后给出一个小矩形视图作为反馈。

在Safari中的一个轻压视图

[![webview_peek_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151117192216606.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151117192216606.png)

在Safari轻压中的快速操作

[![webview_peek_quick_actions_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151117192220363.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151117192220363.png) 轻压(Peek)：

* 当用户按压在一个支持轻压的项上时出现轻压，用户手指抬起后会消失
* 当用户在轻压视图下再更加重一点的按压称之为重压，重压可以查看该项的详细视图
* 当用户在轻压视图中向上滑动，可以提供与该项相关的快速操作

当用户轻轻按压在屏幕，支持轻压的这个项会展示一个你提供的矩形视图，示意可以进行下一步交互操作。那个视图应该够大，这样才能让用户手指不会混淆内容，这个视图应该足够细节，这样可以让用户选择是否去更加重一点按压从而转换到轻压视图。

重要

你在应用中始终如一提供轻压和重压的体验是至关重要的。如果你在有些地方支持轻压和重压，在某些地方不支持，用户有可能认为你的应用或者他们的设备出现了问题。

**使用轻压去为该项提供一个生动的，内容丰富的预览。**当轻压能够给用户提供关于该项的足够信息，从而帮助他们扩展当前的任务，这样做是最好的。例如，在用户决定好是在Safari中打开信息中的网页还是分享这个链接给朋友之前，用户可以使用轻压预览信息中URL的页面。在表单视图中，轻压可以给用户提供一个行项的详细内容。

**为每个轻压提供重压。**虽然一个轻压可以提供给用户所需要的大部分信息，但是你应该可以让用户过渡到重压，从而让用户放开当前正在进行的任务，转移专注力到该项上来。重压的内容应该与用户点击该项后的内容一致。

**不要为同样一个项授予轻压和编辑菜单(****Edit menu****)两个功能**。当同一个项的这两个功能都启用的时会很混乱。(获取更多编辑菜单信息，参看 [Edit Menu](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/EditMenu.html#//apple_ref/doc/uid/TP40006556-CH46-SW1).)

**在轻压操作里，避免展现类似按钮的界面元素。**如果用户抬起手指去点击像按钮的元素，轻压会消失。

**如果可能，提供轻压快捷操作。** ****在轻压里，用户可以向上滑动去显示该项的相关操作。例如，Mail里的轻压快捷操作包括回复全部，转发和删除信息。并不是每个轻压都需要快捷操作，但是如果你已经为该项提供定制的点击并长按的操作，那么最好在轻压里提供相同的操作从而替代点击并长按操作。(注意在网页视图中，轻压快速操作是自动提供的。)

**不要将轻压作为唯一开启该项的指定操作的方式。**不是每一个设备都支持轻压和重压，一些用户可能选择关掉3D Touch, 因此在你的应用中去寻找其他方式实现轻压的功能是非常重要的。当你的应用在较旧的设备上运行时，可以把轻压的快捷操作映射到一个视图里，让用户通过点击并长按获得。

### 3.1.2 主屏幕快捷操作(Home Screen Quick Actions)

主屏幕快捷操作可以在主屏幕给用户呈现方便的、有用的、应用特定的操作。

Camara的主屏幕快捷操作

[![home_screen_quick_actions1-65_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151117193423831.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151117193423831.png)

Mail的主屏幕快捷操作

[![home_screen_quick_actions2-65_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151117193427647.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151117193427647.png) 主屏幕快捷操作：

* 当用户在主屏幕采用比点击且长按更重的按压，按压在应用图片上时，出现屏幕快捷操作
* 它会显示一个你提供的短标题，一个图标和可选的副标题
* 它不支持其他定制的内容
* 它可以随着你应用的更新，更新显示的信息

**使用主屏幕快捷操作去开启引人注目的、高价值的任务。**例如，Maps可以让用户不需要打开Maps，通过在当前位置附近搜索就可以获得回家的方向。一个应用至少需要把一个有用的任务放在主屏幕快捷操作里；你可以提供最多四个快捷操作。

**避免使用主屏幕快捷操作去减少应用里导航的内容。**如果用户访问你应用的重要区域非常困难和耗时，那么首先去修改你的应用的导航，这样做是可以让所有用户都获益的。接着，可以去为有用的深层次链接提供主屏幕快捷操作，从而开启这些有用的、创造性的任务。

**不要把主屏幕快捷操作作为通知用户的一种方式**。iOS用户期望以其他方式接收应用中的信息(更多信息参看 [Notifications](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/NotificationCenter.html#//apple_ref/doc/uid/TP40006556-CH39-SW1))。

**为主屏快捷操作提供一个简洁的标题(可有副标题)和一个模板的图标。**标题应该直接传达这个操作的结果；例如，“回家的方向”，“新建联系人”，和“新建信息”。你也可以提供一个副标题给用户更多上下文信息。例如，Mail使用一个副标题在主屏快捷操作的重要位置去告诉用户有未读信息。 不要把你的应用名字或者无关的信息放在标题和副标题里，同时要考虑到使用本地化的用语。

保持标题的简洁不会被切断从而帮助用户快速理解操作是非常重要的。如果你提供的副标题一行显示不全，系统会截断；如果你没有副标题，系统会把一行展示不完全的长标题以两行展现。

你可以从很多系统提供的模板图标中选择图标，你也可以创作定制的模板图标。更多关于图标尺寸、内边距和定位的详细引导信息，可以下载主屏快速操图标模板 https://developer.apple.com/design/downloads/Quick-Action-Guides.zip。更多关于设计模板图标的信息，参看[Template Icons](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/BarIcons.html#//apple_ref/doc/uid/TP40006556-CH21-SW1)。

系统会自动安排图标在快速操作列表中的位置是在左侧或者在右侧，这依赖于你的应用的图标在用户主屏幕的位置。(摒除图标在列表中的位置，在自左向右的语言中文字总是左对齐。)这里有主屏快捷操作的多种展现方式的例子。 [![clipboard](https://isux.tencent.com/wp-content/uploads/2015/11/2015111719395581.png)](https://isux.tencent.com/wp-content/uploads/2015/11/2015111719395581.png)

### 3.2 Live Photos

Live Photos 让用户在丰富的声音和动作环境下，捕捉和再现他们喜爱的回忆。从iOS 9开始，相机(Camera)应用可以捕捉附加的内容(拍照之前和结束后的声音和额外的画面)为传统的、静止的图片增加生活气息。[![live_photos_camera_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151117195929709.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151117195929709.png) 在iOS9.1及之后的版本中，你的应用可以让用户享受和分享Live Photos。这个指引可以帮助你给用户提供更好的体验。

**在不支持****Live Photo****的环境中，把****Live Photo****像传统照片一样展示。**不要在支持Live Photos的环境中，自定一种与Live Photo相似的体验。

**不要分开展现****Live Photo****的附加画面和声音。**要让用户在不同的应用中体验Live Photos时，有一致的视觉呈现和交互方式。把Live Photo拆分开展现是一个很坏的体验。

**确保用户可以区分Live Photo 和传统静止图片。**在用户分享照片时，帮助他们做好区分是特别重要的。最好在用户查看一个LivePhoto的时候，展现一点移动作为提示。万一这个提示没有起到作用，你可以在LivePhoto上展示一个系统提供的标记。LivePhoto不要展现一个像视频里回放按钮的界面元素。 [![live_photos_photoStream_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151117195933538.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151117195933538.png)

注意

上图这种情况，不支持像照片应用里全屏浏览滑动切换照片时的显示的

**把用户所做的调整应用到Live Photo的所有帧中。**如果你的应用可以让用户为照片添加滤镜或者调整，应确保它可以作用于整个LivePhoto中。如果你不支持调整用户想分享的LivePhoto的所有内容，要让他们知道可以以传统照片的方式分享。 **让用户在决定分享前，可以预览这个Live Photo的所有内容。**如果你的应用UI可以让用户选择照片分享，要为他们提供一个把Live Photo作为传统照片分享的方式。 如果你使用系统提供的标记，应该把它放在每个LivePhoto上同样的位置。标记可以放在一个不会影响用户查看照片的角落。确保在你的应用中采用一致的方式添加标记，这样可以让用户依靠它去识别LivePhoto。iOS有两种方式提供标记：

* 覆盖。这种覆盖的方式包含一个阴影，适合覆盖在照片上
* 纯色。这种纯色的方式(无阴影)可以被用来创建一个可调色的图片模板
* iOS也提供了很多纯色标记，其中，图片上一个删除线代表现在的LivePhoto被当做是一个传统的照片

**在用户下载一个****Live Photo****的时候给他们一个好的体验。尤其重要的是，**用户需要知道他们正在下载的是一个LivePhoto，他们需要知道什么时候可以播放它。如果你为一个Live Photo展示一个未播放的进度指示器，确保这个指示器与你的应用中其他的下载体验一致。

### 3.3 钱包(Wallet)

Wallet应用是帮助用户查看和管理各种数字化票券的，他们是一些物理个体的数字展现，例如登机牌、优惠券、会员卡、奖励卡和各种票。Wallet也可以让人们添加他们的信用卡、借记卡和储值卡结合Apple Pay使用。你可以在应用中创建一个票券，分发给用户，并且在有更改时进行更新。 [![pass_example_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151117200658941.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151117200658941.png) 使用PassKit框架可以方便地用自定义内容来收集一个票券和使用户票券库中的票券。(想要学习Passbook技术的核心概念和PassKit接口的使用方法，请参考[Passbook Programming Guide](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/PassKit_PG/Chapters/Introduction.html#//apple_ref/doc/uid/TP40012195)。)以下几点可以帮助你创建一个用户乐意保留并使用的票券。

**设计一个在各个设备上呈现很好票券。**当你选择一个票券的样式——比如登机牌，优惠券，票据，奖励卡或者通用的票券——你会获得一个特别的布局和一系列区域去处理(更加详细关于不同票券的样式，参看[Pass Style Sets the Overall Visual Appearance](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/PassKit_PG/Creating.html#//apple_ref/doc/uid/TP40012195-CH4-SW45))。这个系统在各个设备上合理展示你的票券，所以正确使用票券的区域是非常重要的。例如，在Apple Watch上，条状图(strip)和缩略图(thumbnail)图片是不显示的，所以你不希望把基本的信息放到这些元素里。更多Apple Watch票券的布局，参看[Designing Passes for Apple Watch](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/PassKit_PG/Creating.html#//apple_ref/doc/uid/TP40012195-CH4-SW25).

**使用合适的票券区域展现文本。**在你的票券中使用允许VoiceOver的用户获取票券中的所有信息的区域，保持你的票券外观的一致性。避免将文本嵌入图片或使用自定义的字体也是一个很好的方法，因为不是所有的图标会展示到所有的设备上，这样对用户来说阅读这样的文字会有困难。

**避免使用识别一个设备的语言。**你不能预料到哪些用户将会查看你的票据的设备，因此你不想使用可能在一个特别设备上不起作用的语言。比如，文字告诉用户“滑动去查看”内容，当这个发生在Apple Watch上将会不起作用。

**尽可能，不要只是简单复制已有的物理票券。**Wallet 已经建立了有美感的设计，票券也都配合这种设计以看起来更好。所以不要只是复制物理票券的外观，抓住这次机会设计一个符合Wallet 组成和功能的干净简洁的票券样式。

**对放在票券正面的信息精挑细选。**用户期望扫一眼票券就能快速获得他们需要的信息，所以票券正面的信息应该是整洁且易读的。如果有用户可能会需要的额外信息，将它们放到票券的背面要比挤在正面好得多。注意，Apple Watch上的票券没有背面。

**通常情况下，避免使用纯白色背景。**通常，一个好看的票券应该使用鲜艳的纯色背景或者使用强烈的，充满活力的图片作为背景。当然，在设计背景时还要确保内容的可读性。

**在商标文本区域显示你的公司名称。**所有票券的商标文本区域的文字都使用了统一的字体。为了避免和其他票券发生冲突，还是建议您在商标文本区域输入文字，不要使用自定义字体。

**使用白色的公司商标。**商标图片放置在票券左上角公司名称的旁边。最好提供一个白色的，单色的，不包含文字的商标。如果你想要增强商标的效果，又想要与文字风格匹配的话，可以增加一个在y轴方向上有1像素偏移，有1像素模糊和透明度为35%的黑色阴影效果。

**如果可以的话，使用矩形的条形码。**类似于PDF417这样的长方形条形码比正方形二维码更适合票券的布局。如下右图所示，正方形的二维码会使两边有空白区域并且会在垂直方向上使上下方内容变得拥挤。 [![20141123155934270](https://isux.tencent.com/wp-content/uploads/2015/11/20151117200655246.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151117200655246.png) **为性能去优化图片。**因为用户通常会通过电子邮件或者Safari接收票券，所以让下载的越快越好是非常重要的。为了提高用户体验，使用能满足视觉效果的最小的图片文件。

**在合适的时候更新票券以增强其效用。**即使一个票券代表的是一个并不会改变的物理实体，数字的票券也可以通过映射真实世界的一些事件来提供更好的用户体验。例如，当某个航班延误时你可以更新登机牌上的信息，这样用户就能够通过查看电子登机牌来获得当前的信息。

### 3.4 苹果的移动支付平台(Apple Pay)

**Apple Pay**是苹果公司面向iOS移动设备推出的一种简单、安全、个人的移动支付方式。当用户在购买实体商品和服务时时，可以使用Apple Pay快速、安全地提供个人联系方式、收货地址以及付款信息。 [![apple_pay_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119171818225.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119171818225.png) 通过用Apple Pay支付，用户无需每次购物都要创建账号或填一遍个人信息。Apple Pay显著加快了支付流程，有助于消除前期的各种信息登记，进而为用户的“无障碍”选购过程提供更好的体验。欲了解更多信息，请参阅 _[Apple Pay Programming Guide](https://developer.apple.com/library/ios/ApplePay_Guide/index.html#//apple_ref/doc/uid/TP40014764)._ Apple Pay的用户界面非常清晰、简洁高效、低调。它包含三个界面元素，各出现在不同的上下文情境中。 [![apple_pay_small_button_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119171829850.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119171829850.png) **按钮。**Apple Pay的按钮用来告诉用户，他们可以在当前的情境下(比如商品页面)完成购买。当用户点击了Apple Pay的按钮，立即显示支付上拉菜单(见下文) 开始帮助用户完成支付流程。用户通过“设置Apple Pay”的选项Apple Pay的相关银行卡信息绑定操作。通过调用PKPaymentButton API口可以找到这两个按钮(想要了解更多信息，请查阅 _[PKPaymentButton Class Reference](https://developer.apple.com/library/ios/documentation/PassKit/Reference/PKPaymentButton_Class/index.html#//apple_ref/doc/uid/TP40015149)_)。有关使用Apple Pay支付按钮的更多详情，请参阅[Identity Guidelines](https://developer.apple.com/apple-pay/Apple-Pay-Identity-Guidelines.pdf). [![apple_pay_payment_marks_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119171822334.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119171822334.png) **Apple Pay支付标识。**当用户需要在授权支付之前选择付款方式并敲定其他信息时，他们期望看到Apple Pay的支付标识。Apple Pay的支付标识应该同其他付款方式以相同或类似的格式显示。 [![apple_pay_payment_sheet_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119171826213.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119171826213.png) **支付上拉菜单。**在用户提交订单以及完成相关支付之前，Apple Pay会显示一个包含了联系方式、收货地址以及与结账相关付款信息的支付上拉菜单。尽管用户依然可以在支付上拉菜单里做些微调，比如选择不同的送货方式，但他们不用做出重大改变或输入其他信息。当用户看到该支付上拉菜单，他们应该能够立即完成交易并授权付款。

**对于可以使用****Apple Pay****付费的用户，****Apple Pay****的用户****界面应当始终显示。**如果用户的移动设备支持Apple Pay，并且他们已经激活了相关可用的银行卡因此可以通过将Apple Pay设为默认支付方式来满足用户的期望。

**如果用户无法使用****Apple Pay****服务，就不要****显示任何****Apple Pay****的****用户界面。**如果用户使用的设备不支持Apple Pay，仍强行将其作为一个支付方式选项，可能会对用户造成混淆。但是，如果用户使用的设备是支持Apple Pay，但没有绑定任何信用卡或借记卡，你可以在界面中显示“设置Apple Pay”的按钮。

**当用户点击了****Apple Pay****的按钮，立即显示支付上拉菜单****。**当用户决定使用Apple Pay来结账时，如果还要迫使用户经历额外步骤，会使支付流程显得复杂，增加不必要的矛盾，并可能会让用户感到沮丧受挫。当用户点击了Apple Pay按钮，不要显示其他警告或模态对话框视图。如果用户可以提供像打折或促销代码之类的信息，请在用户点击Apple Pay按钮之前找到一种方式来接收该信息。

**Apple Pay按钮与其他可见的支付按钮应保持相同的尺寸大小或更大。**将Apple Pay按钮放置在醒目的位置，可以帮助用户轻松找到它。 [![apple_pay_target_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119171833455.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119171833455.png) **使用****Handoff****功能****帮助用户完成在****Apple Watch****上发起的购买。** Apple Watch佩戴者可以在商店完成支付，但他们无法完成由Apple Watch第三方应用程序调用的支付行为。当Apple Watch佩戴者发起了由第三方应用程序调用的支付行为，则显示一条消息告诉他们请在iPhone上完成支付。为了更好的用户体验，还可以使用Handoff功能深层链接到你的iOS应用程序上，并立即显示包含预设好的相应付款信息的支付上拉菜单。

有关使用Apple Pay支付按钮以及Apple Pay支付标识的更多信息指南，请参阅 [Apple Pay Identity Guidelines](https://developer.apple.com/apple-pay/Apple-Pay-Identity-Guidelines.pdf).

### 3.4.1 **自定义支付上拉菜单** **(Customizing the Payment Sheet)**

根据完成交易付款所需要了解的信息，以及所要传达给用户关于本次购物的信息，来自定义Apple Pay支付上拉菜单所要显示的内容。

**支付上拉菜单仅显示对完成交易付款有必要的信息。**如果Apple Pay支付上拉菜单显示了些无关的信息，用户可能会感到困惑或焦虑。举个例子，如果商品是在线交付或通过电子方式完成，需要联系人的电子邮件地址是有意义的，而不是收货地址。在这种情况下，要求收货地址可能给用户产生会有什么东西将意外被派件到家中或公司的错觉，或许还可能导致他们对个人隐私被访问产生不必要的担忧。

**支付上拉菜单允许用户可以选择更换送件或取件方式。**用户可以从你在支付上拉菜单中设定的几种交付方式中随意选择一种。通过用文本标签控件、报价以及可选的第二行预计到达日期，来具体描述一种收货方式。另外，你还可以设定交付方式为“派件”或“取件”，让用户指定一个可接收快递送货上门或需要运输服务取件的位置。

**使用并排项来描述周期性付款和一些购买费用的小计。** 并排项包含了一个标签文本和花费数值。并排项被用来：

* 表明用户授权一个定期付款项目，比如“每月订阅 $19.99”
* 告知用户关于额外费用，比如“礼品包装 $5.00”和“税费 $4.53”
* 显示优惠券或折扣信息带来的减价，比如“周五特价 -$2.00”
* 描述某个项目需要按实际计费，比如运输服务“时间&距离 …”

不要用并排项来显示所要购买的商品的构成清单。

**创建并排项标签时，尽可能显示在同一行。**并排项标签应该具体、容易理解。如果行条目标签字符数过长，那么很难让你的用户一看就懂。

**商户名称需要紧紧跟随在同一行的“****Pay****”字符后面作为一个整体。**确保所使用的商户名称以及相应的开销支出，必须与用户检查自己的信用卡或银行对账单时的数据保持一致。这一点很重要，因为它有助于用户确信他们的开销支出是无误的。如果你的应用程序只是作为中间媒介，而不是最终的商户支付，请明确向用户表明这个具体说明“付款给 _最终的商户名称_(通过 _你的应用程序名称_)。

**如果总价花费在支付授权时还不明确，请向用户传达有可能会有额外费用的信息。**举个例子，一次汽车旅程从支付授权时刻起到驶向最终目的地，它的开销报价可能会受行车距离或时间的影响变化。或者，一个客户可能想要给点小费在商品已派件之后。对于这样的情况，在支付上拉菜单中给予一个非常明确的解释说明是很有必要的。当你使用一个并排项来配置最终总价的更新信息时，总价金额会自动显示为“总价待定”。另外，如果你是预授权支付一个具体金额的订单，确保支付上拉菜单准确地反映了这一信息。

### 3.4.2 **简化结账流程(Streamlining the Checkout Process)**

Apple Pay使得购物变得快速、简单，对此人们会欣然接受的。更少的步骤和更少的需要用户手动输入的信息，使得整个结账流程更好。

**始终使用****Apple Pay****的最新数据信息。**假设用户一直保持Apple Pay个人信息的完整性和时刻更新，那么不要依赖于任何先前收集的信息。即使你以前已收集过用户的联系方式、交付方式和支付信息，也要在结账时获取来自Apple Pay的最新信息。在结账环节，尽量避免用户输入本可以从Apple Pay获取的任何信息。

**使用****Apple Pay****加快购买。**对于单个商品项目的购买，让用户只需通过点击商品页面上的Apple Pay支付按钮，即可显示支付上拉菜单并进行即时结算。购买单个商品时，无需采取额外的步骤，也无需将商品添加到购物车，用户喜欢在应用程序中体验到这种便利性。对于多个商品被添加到购物车中会使用相同的交付方式被送到相同地址的情况，一旦用户有意向支付时，会通过显示支付上拉菜单的快速结账流程来支持。

**在显示支付上拉菜单前需提前收集好赎回代码或促销代码。**因为在Apple Pay支付上拉菜单中没有办法输入这些代码，请务必在显示支付上拉菜单之前收集好相关代码。

**如果人们可以将购买的商品派送到不同地方，或以不同的速度发货，请在显示支付上拉菜单之前提前收集好该信息。**对于这种极端情况，你需要在显示支付上拉菜单之前得到发货信息，因为在支付上拉菜单中没有办法来指定多种交付方式和地址。一般情况下，在支付上拉菜单中务必收集到交付方式和地址信息。

**显示订单确认页面或致谢页面。**在交易完成时，通过使用订单确认页，以这种直接的用户体验来显示关于商品能派送到的预计时间以及用户如何跟进订单状态的信息。

**如果合适的话，请在你的订单确认页上提到****Apple Pay****。**尽管在你的确认页面上提到Apple Pay不是必要的，如果你愿意选，可以使用其中的一种格式：

* “Visa ![▪](https://s.w.org/images/core/emoji/2/svg/25aa.svg)![▪](https://s.w.org/images/core/emoji/2/svg/25aa.svg)![▪](https://s.w.org/images/core/emoji/2/svg/25aa.svg)![▪](https://s.w.org/images/core/emoji/2/svg/25aa.svg)1234(Apple Pay)”
* “用Apple Pay已完成付款”

### 3.5 研究型应用程序(Research Apps)

研究型应用程序可以让苹果用户充分利用iOS移动设备的便利性，参与到各种研究性学习中来。通过调用开源代码ResearchKit，使用预设的几种界面视图和转场动画，可以很轻易为你的研究和参与者自定义一个美观易用的研究型应用程序，这些资源都可以在苹果的开源代码ResearchKit项目中调用。要想了解如何使用ResearchKit来为你的研究开发一个研究型应用程序，请查阅[researchkit.org](http://researchkit.org/).

**重要**

这些规范准则仅供参考之用，并不构成任何法律意见。对于与你的研究型应用程序发展以及任何法律适用的相关建议，你应该向律师咨询。

通常情况下，一个研究型应用程序是由ResearchKit定制化的界面视图以及应用程序本身具体设定的界面视图组成，可归纳为三种主要的体验：

* 参与者的就位培训(Onboarding)
* 研究性调查(Study-specific investigation)
* 管理条目信息(Management items)

设计你的研究型应用程序时务必要遵循以下每个部分的规范准则，将有助于你的用户参与者感到舒服和保持参与感。

### 3.5.1 **参与者的就位培训(Onboarding)**

就位培训的体验包含了一系列向潜在参与者介绍研究内容以及征询他们同意的环节。完成这些以后，参与者通常不会再重新访问这些就位培训的内容环节： [![111](https://isux.tencent.com/wp-content/uploads/2015/11/20151119173534329.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119173534329.png)

你应该按如图所示的这个顺序呈现就位培训的各个体验环节，也就是按介绍指引、适任、知情同意，以及授权访问数据。

**创建一个具有号召性用语的介绍指引。**指引环节应该帮助人们了解更多关于你的研究以及告诉他们如何成为一名参与者。指引环节最好也能向那些现有的参与者提供快捷登录的入口以便继续正在进行的研究。 [![introduction_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119173941664.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119173941664.png) **尽快确认招募的用户是否合格。**适任环节呈现在指引环节之后、知情同意环节之前(如果参与者并不适合该研究则没有必要让其查看知情同意环节)。请确认所呈现的适任资质要求对于你的研究来说是必要的。请使用简单、直白的语言描述这些要求，并让用户可以很容易就输入相关信息。 [![eligibility_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119173809938.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119173809938.png) **在得到参与者的同意之前，确保他们已充分了解你的研究内容。**ResearchKit有助于让知情同意流程显得简洁、友好，同时还允许将你同意的任何法律规定或由机构审查委员会和伦理审查委员会所设定的规定纳入其中。(如果你的应用程序涉及到进行人体生物学相关的研究，必须确保你的应用程序符合现有的苹果应用商店规范指南，并获得参与者的许可。)通常情况下，知情同意环节包含了：

* 说明这项研究是如何工作的
* 确保参与者了解研究内容以及各自的责任
* 获得参与者的许可

**将冗长的同意书分解成易理解消化的小节。**每个小节可以只覆盖研究内容的一个方面，比如数据采集、数据应用、潜在好处、可能的风险、时间承诺、如何撤出等等。每个小节请使用简洁、直白的语言来说明一个高度概括的内容。如果有必要，提供一个查看详情的按钮便于参与者了解该小节更详细的解释。应该让他们在同意参与之前，就查看完全部知情同意内容。 [![consent_study_description_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119173755187.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119173755187.png) **通过一个小测验来测试参与者的理解情况是有意义的****。**在获得参与者允许的情况下，你可以选择向每个参与者询问相同的问题。 [![consent_understanding_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119173758939.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119173758939.png) **你的研究必须获得参与者的同意，如果合适，还可以收集一些联系人信息****。**参与者同意参与研究后，他们需要提供个人签名以及联系方式，最后会收到一个确认对话框。对于这些信息记录，大多数的研究型应用程序会向参与者电邮一份PDF格式的同意书。

参与者需要对这个确认自愿参与研究的告警对话框给予响应

[![consent_alert_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119174258500.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119174258500.png)

参与者可以提供他们的个人签名在知情同意流程中

[![consent_signature_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119173751503.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119173751503.png) **如果你需要访问参与者的设备或数据必须得到他们的许可。**必须解释清楚你的研究型应用程序为什么需要访问他们的位置信息、健康应用程序或其他数据，并且确保避免向参与者索要对你研究并非至关重要的数据。同样地，如果你需要向参与者发送通知提醒也要获得参与者的许可。

让参与者准备授权访问数据，比如健康应用程序的数据

[![data_access_permission_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119174408215.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119174408215.png)

让参与者自己选择他们愿意与你共享的数据

[![health_data_request_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119174411936.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119174411936.png)

### 3.5.2 **具体研究的调查(Study-Specific Investigation)**

为了从参加者获得数据输入，你的研究可能会使用情况调查、活动任务，或两者的组合。根据你的研究的体系结构，参与者可能会在每个环节多次或仅需完成一次交互即可。

**问卷调查的设计应该能让参与者专注参与其中。** ResearchKit可以很容易就呈现多种答案类型的调查问题，比如对错、多选、日期和时间、比例计算，以及开放式文本填写。当你使用ResearchKit的界面视图来创建一项调查，请遵循以下准则，来保证好的用户体验：

* 告诉参与者总共有多少道问题，以及完成调查预计需要花费的时间
* 每屏只呈现一道问题
* 显示给参与者当前调查的进度
* 调查应该尽可能简短。几个简短的调查往往好于一个冗长的调查
* 对于需要额外解释的问题，问题描述请用标准字体大小，然后解释文字用略小的字体大小
* 调查结束时要告知参与者

ResearchKit提供了许多用于调查环节的可自定义界面视图。这里有一些样例。 [![ThreeQuestions_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119174557768.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119174557768.png) **使得活动任务容易理解。**活动任务需要参与者参与到一次活动中来，比如对着麦克风语音、手指在屏幕上完成点击、行走散步，以及执行一次记忆力测试。请按照以下几点准则来鼓励参与者执行活动任务，并给与他们成功的绝佳机会：

* 请用简洁易懂的语言来描述如何执行本次任务。
* 如果任务必须在特定的时间或特定情况下进行，请务必明示。
* 确保参与者可以分辨出任务何时结束。

以下是ResearchKit所支持的两个活动任务样例。 [![gait_task_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119173813550.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119173813550.png)[![voice_task_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119174903660.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119174903660.png)

### 3.5.3 **管理条目信息(Management Items)**

ResearchKit提供了个人档案的界面视图来让参与者可以管理他们的个人信息。此外，创建一个可以激励用户并能让他们追踪他们在研究中的进度的界面视图是个不错的选择。在大多数情况下，参加者应该能够随时访问这两个模块。

**使用个人档案来帮助参与者管理个人信息和与你研究相关的数据。**个人档案界面视图允许参与者在研究进程期间可以编辑相应数据，比如体重或睡眠习惯，并且可以提醒他们即将到来的活动任务。你同样可以在个人档案中给予参与者一种简单的方式离开该研究、查看知情同意书，以及查看该应用程序的隐私政策。 [![profile_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119175025781.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119175025781.png) **使用仪表盘概览视图来激励参与者，并呈现进度。**一个概览视图可以让你与参与者对信息一览无余并鼓励他们继续参与。如果你的研究内容合适的话，你可以使用该概览视图给予参与者丰富的反馈，比如每日进度、每周评估、具体活动的结果，以及同其他参与者的汇总结果进行对比。 [![dashboard_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119175035464.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119175035464.png)

### 3.6  应用扩展(App Extensions)

应用扩展可以延伸应用的使用范围。当用户使用其他应用时，应用扩展使得用户仍能使用你应用的核心功能。举个例子，当人们在Safari中浏览网页时，他们可以使用你的分享扩展来发送一张图片或一篇文章到你的社交网站上。或者当使用Photos(照片)应用时，人们可能会使用你的图片编辑扩展来为一张图片加上一个滤镜效果。(在这些场景中，Safari和照片应用承载用户使用扩展的场景，因而被称为**宿主应用(****host apps****)**。)

你需要提交包含应用扩展的完整iOS应用到App Store(包含扩展的应用被称为**容器应用(****containing app****)**)。在你的容器应用中启用扩展之后，人们就可以在使用其他应用时，使用扩展来执行快速任务。例如，在邮件中浏览某个商品时，人们可以不用离开邮件应用就使用你的动作扩展来把商品添加到购物清单中。 表[ 22-1](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/AppExtensions.html#//apple_ref/doc/uid/TP40006556-CH67-SW2) 列举了可以多个创建的iOS应用扩展类型。

**应用扩展类型**               | **人们使用扩展来做…**             
------------------------ | --------------------------
今天部件(Today widget)       | 在通知中心中获得快速更新或者在今天视图中快速完成任务
分享(Share)                | 发送到网站或者和他人分享内容            
动作(Action)               | 通过另一个应用的上下文信息来操作或查看内容     
图片编辑(Photo Editing)      | 使用照片应用编辑图片或视频             
文档提供者(Document Provider) | 进入和管理文档库                  
自定义键盘(Custom keyboard)   | 替换iOS系统键盘                 

以下指南适用于所有类型的应用扩展，针对特定类型应用扩展的指南请参阅后续章节。(如果想了解如何开发、调试和发布一个扩展，请参阅__[App Extension Programming Guide](https://developer.apple.com/library/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214).__)

**确保是单任务。**应用扩展并不是应用的精简版，它帮助用户在有全局目标的上下文中完成狭义范围内的有限任务。例如，动作扩展可以为用户提供一种不同的方式来查看当前内容。

**保证用户的交互是有限和流畅的。**好的应用扩展应该只需几步点击就可以帮助人们完成任务，这样他们就能尽快回到之前的场景中。例如，分享扩展只需一次点击即可完成一张图片的分享。

****将容器应用****及其应用扩展的名称保持一致。****一个容器应用中如果有多个扩展，需要使用不同的名称，你需要确保用户能够理解你的扩展和应用之间的关系。人们会在很多不同的情况下遇到扩展，如果他们当下没有认出来，那么他们就未必会信任这些扩展。

**大部分情况下，复用容器应用的图标。**显示用户熟悉的图标是获得用户信任的另一种方式。请注意，对于动作扩展来说，你应该使用单色版本的容器应用图标(详见[分享和动作扩展](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/AppExtensions.html#//apple_ref/doc/uid/TP40006556-CH67-SW3))。

重要：和设计图标和图形一样，不要重复使用iOS的图标和图片，不要为苹果的产品和设计再设计一套图片。

**避免在扩展上显示模态视图。**很多扩展默认以模态视图来显示，所以应避免再叠加模态视图。尽管有时候用户可能会在扩展上遇到警告框，但是在设计扩展的流程时，应避免出现模态视图。

### 3.6.1 今天部件(Today Widgets)

人们会在通知中心的今天区域中查看今天部件(Today widgets)。因为人们会设置今天区域以显示他们最关注的信息，所以在此进行设计可以有效帮助你的部件在这些用户最重要的信息中占据一席之地。 [![widget_experience_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119191103833.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119191103833.png) **设计与通知中心风格一致的外观。**当使用通知中心的默认边距和背景时，你的今天部件就会给用户以统一的体验。为获得最佳的结果，你应该重点关注你的内容而不是背景或者其他的，尤其应该避免绘制一片纯色背景。

注意：

iOS会自动在自定义的部件内容上方显示应用的图标和标题(图标会显示在标题前面的空白处)。

**将部件内容与标题对齐。**当你的部件内容与标题对齐时，人们就可以很简单地浏览今天视图中他们想要的部件。遵守今天视图中的边距规范，并将内容约束在如图的部件内容区内。[![109746](https://isux.tencent.com/wp-content/uploads/2015/11/20151119191315516.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119191315516.png)   **一般情况下，使用白色的系统字体来显示文本。**在通知中心默认背景下白色文字会看起来较好。对于二级文本，可以使用系统提供的vibrant外观样式(查看[notificationCenterVibrancyEffect](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIVibrancyEffect/index.html#//apple_ref/occ/clm/UIVibrancyEffect/notificationCenterVibrancyEffect)了解更多)。

**提供通知中心式的体验。**人们访问通知中心来获取简要的更新或者执行一个非常简单的任务，所以今天部件最好只显示适量的信息和进行有限的互动，特别是：

* 避免用户在部件中需要滚动或纵向移动来查看全部的信息。部件可以通过纵向扩展来显示更多的信息，但若部件的高度超过通知中心的高度就不是一种好的体验了，因为这样会干扰其他部件的查看
* 避免使用横向扫动或拖曳，因为这会干扰在通知中心进行导航
* 尽可能使用户只需一步操作就完成任务或打开你的应用(注意，在今天部件中键盘是不可用的)
* 优化性能以便人们可以即刻获得有用的信息。可以考虑在本地缓存信息，以便当有更新时就可显示最近信息。人们只希望在今天视图中花很少的时间，如果部件使用内存不当，iOS就可能会终止它

**在适当情况下，让人们点击你的今天部件来打开你的应用。**因为今天部件提供了专一的体验，所以就能有效引导人们去到你的应用以获取更多信息或功能。最好不要显示“打开应用”按钮，而是应该让你的整个今天部件都可被点击来打开应用。你也可以让用户点击部件中的UI对象，以打开你的应用并跳转到关于此UI对象的视图中。举个例子，日历部件显示了今天的事件，如果用户想要获得某个事件的更多信息，他们可以点击部件中的事件来打开日历应用进行查看。

注意：

虽然从部件打开应用的方式对用户来说还不错，但继续在部件中提供有用且及时的信息依然是很重要的。人们可不一定会欣赏一个功能只是打开应用的今天部件。

**如果可能，在今天部件中让人们知道他们需要登录来获取有用的信息**。如果你的今天不见需要人们登录查看信息，展示一个信息去鼓励他们登录和解释什么样的内容将会被呈现。例如，如果你的时间部件即将到来的预约是用户登录后展现的，你可能需要让用户“登录我的应用去查看即将到来的预约”。

**不要制作一个今天不见需要打开除了你自己应用外的应用。**一个模拟iOS主屏的行为的时间部件不会为你的用户提供有用的功能。

### 3.6.2 分享和动作扩展(Share and Action Extensions)

人们通过点击应用中的动作按钮(Action button)来使用分享和动作扩展。在通过动作按钮显示的动作视图控制器(activity view controller)中，动作扩展被列在底部，分享扩展被列在动作扩展之上。人们可以使用更多（More）按钮来管理显示在动作视图控制器中的分享和动作扩展。 [![share_action_appex_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151119191738140.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151119191738140.png) 分享或动作扩展通常被认为是在当前用户场景下用来输入内容之用。例如，当在Safari中阅读一篇文章时，用户可能会点击动作按钮并使用一个分享扩展来发送这篇文章到分享网站上，也可能会使用一个动作扩展来查看这篇文章的翻译。

注意：

在动作视图控制器中，iOS只会显示支持当前内容类型的动作扩展。例如，当用户当前内容是视频时，iOS就不会显示支持文本的动作扩展。

**尽可能在分享扩展中使用系统提供的UI****。**系统所提供的撰写视图控制器 (compose view controller) 提供给用户一种一致的体验，并能自动支持一些常用任务，例如预览和确认标准项，同步内容，查看动画，以及完成一封邮件。欲知更多关于使用系统提供的撰写视图控制器，请参见 [_App Extension Programming Guide_](https://developer.apple.com/library/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214)中的[Share](https://developer.apple.com/library/ios/documentation/General/Conceptual/ExtensibilityPG/ShareSheet.html#//apple_ref/doc/uid/TP40014214-CH12).

**如果上传需要一定时间，那就应考虑在分享扩展的容器应用中显示上传进度。**无论分享的文件有多大，人们都期待在点击扩展中的发送或分享按钮后，能立即返回他们之前的场景。你需要让进度状态随时更新，但是人们不想每次上传完毕后都收到通知，并且也无法自动重启扩展。在这种场景下，在容器应用中显示上传进度是一种解决方案，这样容器应用就可以在后台处理任务，并在遇到问题时发送通知。

**动作扩展使用单色的应用图标。(** 不同的是，分享扩展则应该使用其容器应用的彩色应用图标。) 要为动作扩展设计图标时，你可能需要从创建一个应用图标的模版开始着手。如有需要，可以专注图标所特有的元素来进行简化设计。

如果你在容器应用中提供了多个动作扩展，那么最好为他们设计一套图标，且确保这套图标中的每一个看起来都与容器应用的图标是有关联的。

### 3.6.3 图片编辑扩展(Photo Editing Extensions)

当人们在照片(Photos)中查看图片或视频时，可以使用图片编辑扩展。一般来说，图片编辑扩展能帮助用户筛选图片或进行一些其他的图片或视频编辑。在用户确认之后，编辑后的内容就会出现在照片应用中。

照片应用提供了一个模态视图来显示图片编辑扩展的自定义UI。当用户在确认对图片或视频的编辑时选择了取消(你必须要在代码上保证存在这个行为)，照片应用还可以显示一个确认视图。

**避免在图片编辑扩展中使用导航栏。**如图所示，承载扩展的模态视图已经包含了导航栏，若再增加另一个导航栏，既会占据更多你的界面空间，还会使用户产生困扰。(照片应用默认会以全屏高度来显示你的视图，所以你的内容会出现在内建的导航栏之下。) [![photo_filter_appex_2x](https://isux.tencent.com/wp-content/uploads/2015/11/2015111919200764.png)](https://isux.tencent.com/wp-content/uploads/2015/11/2015111919200764.png)     **如果可以，让用户能够预览编辑结果。**尽可能让用户在关闭扩展返回照片应用之前看到他们编辑的成果。

### 3.6.4 文档提供者扩展(Document Provider Extensions)

文档提供者扩展帮助人们在其他各种应用中查阅你的应用所管理的文档。在宿主应用(host app)中，文档采集视图控制器(document picker view controller)会显示你的扩展所提供的UI(想要了解更多有关文档采集视图控制器的内容，请查阅_[UIDocumentPickerViewController Class](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIDocumentPickerViewController_Class/index.html#//apple_ref/doc/uid/TP40014342)_[ Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIDocumentPickerViewController_Class/index.html#//apple_ref/doc/uid/TP40014342)).

注意：

文档提供者扩展由两个不同的部分组成：文档采集视图控制器扩展和文件提供者扩展。文档采集视图控制器扩展包括了你的自定义UI，文件提供者扩展实现对文件的访问。为了简单起见，本节所使用的术语_文档提供者扩展(__Document Provider extension)_是为了表述扩展中文档采集视图控制器部分的UI和体验。

**避免在文档提供者扩展中使用导航栏。**iOS会显示扩展的自定义UI，而自定义UI又包含在文档采集视图控制器中基于导航栏的界面之中。所以，在内建导航栏之下再显示第二个导航栏会使用户感到困惑，并且还会占据原本你的内容区域。(文档采集视图控制器默认会以全屏高度来显示你的视图，所以你的内容会出现在内建的导航栏之下。) [![852261](https://isux.tencent.com/wp-content/uploads/2015/11/201511191923206.png)](https://isux.tencent.com/wp-content/uploads/2015/11/201511191923206.png)

### 3.6.5 自定义输入法(Custom Keyboards)

人们在整个系统中使用带有自定义输入法的输入法扩展来替换iOS的自带输入法。在启用输入法扩展之后，除了受保护的文本区域(例如密码输入区)和手机键盘区(例如联系人中的电话号码区)外，当人们点击任何文本输入区域后就能使用自定义输入法。

**为用户提供明显的方式来切换输入法。**人们对于iOS的输入法切换按钮很熟悉，他们会期望在你的输入法中也有类似的体验。 [![alternate_keyboards_2x](https://isux.tencent.com/wp-content/uploads/2015/11/2015111919255797.png)](https://isux.tencent.com/wp-content/uploads/2015/11/2015111919255797.png)

如果可能，在你的容器应用中包括一个教程。如果必要，使用你的自定义键盘的容器应用去给人们讲解如何启用和使用你的键盘。不要把这个信息直接放在键盘本身，因为它可能让人们尝试使用这个键盘时感到困惑。

### 3.7  HomeKit

通过HomeKit，用户能够方便地在家中使用iOS设备上的智能家居应用来操控家中相关联的设备(无论这些设备制造商是谁)。最好的智能家居应用集成HomeKit和iOS系统来帮助用户：

* 创建家居环境、房间和区域
* 添加、寻找和移动家居设备(如灯泡或温度调节装置)
* 定义能够使一组多个家居设备响应的行为
* 管理用户
* 用Siri来操控他们的家居设施

想要了解如何在你的应用中使用HomeKit，可参阅[_HomeKIt Developer Guide_](https://developer.apple.com/library/ios/documentation/NetworkingInternet/Conceptual/HomeKitDeveloperGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40015050)。下面的指南可以帮助你做出一个容易上手、令人愉悦的智能家居程序。

**不要想当然地认为你的设备会是用户所设置的首个设备。**你的应用除了能让用户很容易就能创建家居环境、房间和区域，还需要让用户能方便地将你的设备接入之前已经设置好了的区域中。

**让添加新设备变得简单。**不要强迫用户在添加设备之前注册账号。最好让你的应用能自动发现新的设备并将他们显著地展示在用户界面上。确保所展示的信息足够充分让用户可以轻易辨识出该家居设备。

**帮助用户辨认他们正在调节的设备。**给用户一个能够帮助他们从物理属性辨认设备的控制器。例如，你可以让用户通过闪一下灯泡来确认他们正在调节的是他们想要调节的那个。

**让用户能够通过多种方式来搜寻设备。**当天的时间、季节和用户当前的位置会在特定的时刻成为判别某些设备是否重要的影响因素。因此，你的应用应该允许用户能在家中按类型、名称、或者位置的方式来搜寻设备。

**为家中已接入的设备提供推荐的操作集。**操作集允许用户设定在某种情景下让多个家居设备按照特定的方式行动。例如，一个“离开”操作集可以将房屋内的温度调低、关闭电灯和锁上所有房门。你的应用可以向用户推荐一些已经设定好了的操作集或者让用户创建自定义操作集。当用户能够基于房间或区域去创建自定义操作集时，让用户可以从你推荐的设备列表中进行选择，通常能使用户获得更好的体验。

**使用友好的交谈式语言让你的应用平易近人、易于使用。**智能家居概念可能会懵到用户，应避免使用他们可能不理解的缩写和技术术语。例如，HomeKit是指代API的专用技术术语，它就不应该在你的应用中使用。

注意：如果你是苹果MFi认证许可商，请访问MFi门户网站查看设备包装的命名及消息通知的规则。

**与****Siri****互动。**通过Siri，使用一个简单的陈述句就能控制执行复杂的操作。Siri能够识别操作集、房屋、房间和区域的名称，并且能够理解像“Siri，把前门关了”、“Siri，把楼上的灯关了”和“Siri，把多媒体房的温度调高一点”这样的陈述。遵循以下准则能帮助你为用户提供使用Siri操控设备时的良好体验：

* **使用****Siri****能够识别的功能名称，而非设备名称。**一个设备可能提供多种功能(例如，一个既有风扇功能又有照明功能的风扇吊灯)，因此，帮助用户区分这些功能是很重要的。最佳方案是让用户在一系列不包含公司名称及型号的限定的名称中进行选择，并且允许他们以后编辑。你所推荐的名称应该使用规范的、容易理解的词语来描述功能，并可选择是否包含家中的位置信息，例如“客厅灯”或者“车库门”。你还可以让用户指定一种控制插座开关的通用口令，例如“Siri，把灯关了”，来控制所有的灯具和其相关的设备
* **当用户配置操作集的时候，告诉用户如何通过****Siri****去操控它。**举个例子，当“电影”这个操作已经确认配置完毕时，让用户知道他可以通过跟Siri说“Siri，把家调成电影模式”这样的话来激活这个操作。 注意，当用户单独对Siri说出某操作的名称时，同样也能激活那个操作。Siri能够识别系统预置以及用户自定义的操作集，这些已配置的操作集至少包含一项操作

**帮助用户设置触发机制。**在iOS9中，HomeKit支持触发机制：当满足特定的时间、地点或其他设备的行为的条件时激活操作的方式。比如用户可以设置一个当太阳落山且车库门打开时，就打开厨房灯操作的触发机制。设置一个包含多个项目的条件关系容易使人感到混乱，因此，将你的设置界面做得简单易用至关重要。举例来说，使用与人们平常说话一样的表达方式来展示项目、属性和逻辑，就更容易使人理解。

### 3.8 多任务处理(Multitasking)

多任务处理让人们在屏幕上(在合适的iPad模式上)查看多个应用，可以在最近使用的应用之间进行快速切换。在iOS9,中，人们可以使用多任务处理UI(下图所示)去选择最近使用的应用。 [![multitasking-9_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151117201813171.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151117201813171.png) 能否在多任务处理中处理好取决于能否在设备中与其他应用和谐共存。从更高的层面来说，这意味着所有的应用都应：

* 仔细调整资源使用避免占用太多CPU，内存，屏幕空间和其他资源
* 处理好中断或来自其他应用的声音
* 停止和重启，即快速平滑地从后台切换到前台
* 不在前台时应恪守己任

下述指南细则可以帮助你的应用在专注应用切换的多任务处理中取得成功。更多合格的iPad模式下关于多任务环境中运行的信息，参阅 _[Adopting Multitasking Enhancements on iPad](https://developer.apple.com/library/ios/documentation/WindowsViews/Conceptual/AdoptingMultitaskingOniPad/index.html#//apple_ref/doc/uid/TP40015145)._ 

**准备好被打断，并恢复。**多任务处理增加了后台应用中断你的应用的可能性。其他特性，诸如广告出现和更快的应用切换，也会造成更频繁地打断。越快速和越精确地保存应用当前状态，人们就可以越快地重新运行应用，并从之前离开的页面继续使用。你可以通过利用UIKit的状态保存和恢复来为用户提供无缝的重新开始的体验(查看[Preserving Your App’s Visual Appearance Across Launches](https://developer.apple.com/library/ios/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/StrategiesforImplementingYourApp/StrategiesforImplementingYourApp.html#//apple_ref/doc/uid/TP40007072-CH5-SW2)了解更多信息)。

**确保你的UI****可以处理两倍高度的状态栏。**两倍高度的状态栏会在诸如通话、录音和共享等过程中出现。在未作处理的应用中，状态栏的额外高度会引起布局问题，如UI被向下挤压或者被遮住。在多任务处理环境中，使两倍高状态栏显示正常是格外重要的，因为它可能会出现在更多的应用当中。

**准备好暂停需要人们注意或主动参与的活动。**例如，如果你的应用是一款游戏或媒体观看应用，你需要确保你的用户从应用切换走时，不会丢失任何内容或事件。当人们切换回游戏或媒体播放器时，他们希望能继续之前的体验，就好像他们从未离开过应用。

**确保音频行为合适。**当你的应用正在运行时，多任务处理会使得其他媒体活动更可能地同时进行，也会有更多可能性使你的音频不得不暂停，并恢复处理中断。查看[声音](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Sound.html#//apple_ref/doc/uid/TP40006556-CH44-SW1)来帮助你确保你的音频能满足人们的期望，并与设备中的其他音频和平共处。

**适度使用本地通知。**应用可以在特定时间发送本地通知，无论应用是在暂停中还是运行中亦或是根本就没有运行。为了达到最好的用户体验，应避免用过多的通知来骚扰人们，并遵循[通知](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/NotificationCenter.html#//apple_ref/doc/uid/TP40006556-CH39-SW1)中创建通知内容的指南。

**必要时，在后台完成用户的任务。**当人们开始一个任务时，他们通常会期望即使已经从应用中切换走了任务仍能够完成。如果你的应用在执行用户任务途中，并且这个任务不需要额外的用户交互，那么你就应该在应用挂起之前就在后台完成任务。

### 3.9 通知(Notifications)

通知为人们提供即时的重要信息和功能。人们能在多种情况下收到通知，例如在锁屏界面中，或者在使用应用时，或者访问通知中心时。 通知中心有两种视图：通知(Notifications )和今天(Today)。 [![notification_ctr_today_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151117202318641.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151117202318641.png) 今天视图显示了一组可编辑的部件。今天部件是一个应用扩展，显示了少量及时和重要的信息或功能，这些信息或功能则是由用户所关注的应用所提供。举例来说，日历部件只显示了今天的事件。点击日历部件中的一个事件可以唤起日历应用，并打开该事件，用户接下来可以编辑该事件或管理其他的事件。想要了解更多关于设计今天部件的内容，请参见[今天部件](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/AppExtensions.html#//apple_ref/doc/uid/TP40006556-CH67-SW4)。 [![notification_ctr_notifications_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151117202314972.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151117202314972.png) 通知视图会显示用户感兴趣的应用所发出的最近通知。用户可以在设置(Settings)中来设置是否在通知中心显示该应用的通知。 iOS应用可以使用通知来让人们知道一些有趣的事情是什么时候发生的，例如：

* 收到一条消息
* 事件即将发生
* 有新的数据可下载了
* 某些状态发生了变化

在iOS8及之后的版本中，应用可以定义用户在通知中的操作。例如，用户可以在待办事项应用的通知中就标记该事项已完成，而无需额外打开应用。 iOS定义了两种类型的通知。

* **本地通知(local notification)**由应用安排待发送，最终通过iOS发送到同一设备中，无论该应用当前是否正在后台运行。例如，日历或待办事项应用可以安排一条本地通知来提醒人们一个即将到来的会议或者日期。
* **远程通知(remote notification)**(也称为**推送通知(push notification)**)是由应用的远程服务器通过苹果推送通知服务来发送的，这类通知最终会被推送到所有安装了该应用的设备。例如，一款在线竞技类的游戏，用户可以和其他玩家竞赛的，可以更新所有玩家的最新状态。

注意：应用扩展可能会要求远程通知必须发送到它的容器应用。在这种场景下，容器应用常常会在后台运行来处理通知。想要了解更多关于应用扩展的内容，请参见[应用扩展](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/AppExtensions.html#//apple_ref/doc/uid/TP40006556-CH67-SW1)。

如果当你的应用正在后台运行时收到了本地或远程的通知，你就应该以你的应用所特有的方式将信息传达给你的用户。 为了确保用户能够自定义他们的通知体验，你应该尽可能多地支持以下的通知类型：

* 横幅(Banner)
* 警告框(Alert)
* 小气泡(Badge)
* 声音(Sound)

注意：在iOS8及之后的版本中，你必须对所有你想发送给用户的通知类型进行注册。当你第一次进行注册动作时，用户会遇到一个警告框，他们可以在其中操作来决定允许或拒绝所有来自你的应用的通知。不管用户选择的结果是什么，他们应始终能访问应用的设置来更改此项设置，或者设置他们想要接收的通知类型。

[![notif_ctr_banner_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151117202648477.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151117202648477.png) 横幅(banner)是一个小而透明的视图，会出现在屏幕顶部并在几秒后消失。用户还可以看到在锁屏当中的横幅以及在通知中心中以通知形式出现的横幅。在横幅中，iOS会显示通知的内容和应用的小图标(欲了解更多关于小图标的内容，请参见 [App Icon](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/AppIcons.html#//apple_ref/doc/uid/TP40006556-CH19-SW1))。用户点击横幅来隐藏显示并切换到发送通知的应用。 [![notif_ctr_banner_actions_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151117202651967.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151117202651967.png) 除了默认的点击动作之外，当用户轻扫横幅时,你还可以定义两个动作按钮。点击通知动作按钮来隐藏横幅的显示并启动你的应用(可能是在后台)来执行动作。 [![notif_ctr_alert_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151117202637842.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151117202637842.png) 通知**警告框**是显示在屏幕上的标准警告框视图，需要用户操作后才会隐藏。当用户点击Options按钮后，你需要提供并显示通知消息以及任何一个默认动作，或最多四个特定动作。警告框的背景样式不能做修改。 当用户点击警告框中的一个默认或自定义动作按钮时，iOS会同时隐藏警告框并运行你的应用(可能是在后台)。点击关闭或确定按钮会隐藏警告框而不打开应用。 ![notif_ctr_alert_actions_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151117202641398.png)[![notif_ctr_badge_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151117202644948.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151117202644948.png) **小气泡(badge****)**是一个显示未读通知数量的红色小圆(小气泡显示在应用图标的右上角)。小气泡的大小和颜色不能做修改。 横幅、警告框和小气泡这三种通知都可以使用自定义或系统提供的**声音**。

**在通知中谨慎使用具破坏性的动作。**要确定用户有足够的上下文来避免意想不到的后果。为了帮助用户区分你所定义的破坏性动作，iOS会用红色来显示它。有时候，在应用执行破坏性动作之前，应该请求用户进行确认。举个例子，如果在锁屏的横幅(banner)中提供了一个破坏性动作，那么就应确保只有设备的主人才能执行该动作(你需要在代码上实现这一需求)。

**为每个动作按钮提供自定义标题。**创建一个简短的标题来描述清楚将要发生的动作。例如，游戏可能会使用“Play”作为标题来表明，点击这个按钮会打开应用来进行游戏。确保标题：

* 使用标题样式的大小写(title-style capitalization)
* 足够简短，能不被截断地显示在按钮内(也应确保测试各种语言文字的标题显示正常)

**不要为同一个事件重复发送通知。**用户可以选择处理通知项；通知项在用户未处理前会一直显示。如果为同一事件重复发送通知，通知中心列表中会满是通知，用户就有可能会关闭你的应用的通知。

**不要在通知消息中包含你的应用名称。**自定义信息会在警告框和横幅中显示，也会在通知中心中以通知的形式显示。你无需在自定义信息中显示你的应用名称，因为iOS会在显示信息的同时自动显示应用名称。 为了使本地或远程通知信息更有作用，你应该：

* 专注于信息而不是用户的行为。避免告诉人们点击哪个按钮或如何打开你的应用
* 足够简短，一两行就可以显示完整。较长的信息对于用户来说很难进行快速阅读，也会造成在警告框中需要滚动才能查看完整
* 使用句式大小写(sentence-style capitalization)，并配以合适的结束语句符号。可能的时候，可以使用一个整句

注意：如有必要，iOS会缩短你的消息以便能在各种通知发送样式下显示；为了最好的效果，你不应主动缩减你的消息。

**保持小气泡的内容是最新的。**当用户注意到新信息时，即时更新小气泡非常重要，这样用户就不会觉得收到了额外的通知。注意，当小气泡为0时也会移除通知中心中所有对应的通知项。

重要：不要使用小气泡做通知以外的用途。记住，用户能够关闭应用的小气泡，所以你无法确定他们一定能看到小气泡中的内容。

**当收到通知时，提供用户可以选择听到的音效。**当人们没有在看屏幕的时候，可以通过音效获取他们的注意。例如，日历应用可能会在显示警告框的同时播放一个音效来提醒人们一个即将到来的事件。再如，协作任务管理应用可能会在小气泡更新时播放一个音效来告知某个远程协同的同事已经完成了某个任务。

你可以提供自定义的音效，或者使用内置的警告音。如果你创建了自定义音效，请确保它是简短的、有特色的并且是经由专业制作的。(想要了解更多关于音效的技术需求，请参阅[_Local and Remote Notification Programming Guide_](https://developer.apple.com/library/ios/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/Introduction.html#//apple_ref/doc/uid/TP40008194)中的[Preparing Custom Alert Sounds](https://developer.apple.com/library/ios/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/Chapters/IPhoneOSClientImp.html#//apple_ref/doc/uid/TP40008194-CH103-SW6)。)注意，当通知发送后，你无法以编程方式来触发设备的震动，因为用户对于警告框是否伴随震动拥有支配权。

### 3.10 社交媒体(Social Media)

人们会期望在任何场景下都可以使用他们喜爱的社交媒体帐号。iOS以人们喜欢的方式将社交媒体的交互与你的应用进行了整合。 [![social_media_sharing_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151117203257779.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151117203257779.png)

注意：当用户点击动作按钮时，他们会得到一个如上图的动作视图控制器。想要了解更多关于这个视图控制器的内容，请参见[Activity View Controller](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/ContentViews.html#//apple_ref/doc/uid/TP40006556-CH13-SW121)。

动作视图控制器的中间一行显示了用户启用的和系统提供的分享应用扩展。想要了解更多关于设计分享扩展的内容，请参见[ ](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/AppExtensions.html#//apple_ref/doc/uid/TP40006556-CH67-SW3)[Share and Action Extensions](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/AppExtensions.html#//apple_ref/doc/uid/TP40006556-CH67-SW3)。

**考虑在你的应用中为用户提供一种简便的方式来撰写邮件。**用户有可能会启用分享扩展以便能在任何地方都可以发送内容。但是你也可以使用系统提供的撰写视图控制器来呈现给用户，他们可以在其中进行编辑操作。你可以在显示给用户进行编辑之前，预先加载具有自定义内容的撰写视图(在你呈现给用户之后，只有用户可以编辑这些自定义内容)。想要了解更多关于社交框架(Social framework)的编程界面，包括[SLComposeViewController](https://developer.apple.com/library/ios/documentation/NetworkingInternet/Reference/SLComposeViewController_Class/index.html#//apple_ref/occ/cl/SLComposeViewController)类，请参见[ __](https://developer.apple.com/library/ios/documentation/Social/Reference/Social_Framework/index.html#//apple_ref/doc/uid/TP40012233)__[Social Framework Reference](https://developer.apple.com/library/ios/documentation/Social/Reference/Social_Framework/index.html#//apple_ref/doc/uid/TP40012233).__

**如果可能，避免要求用户登录进入一个社交媒体账户。**社交框架(Social framework)会和帐号框架(Accounts framework)一起来支持一个单点登录模式，所以你可以获得授权来访问用户的帐号，而无需要求他们来重新授权。如果用户还没有登录进入一个帐号，你可以显示UI来让他们进行登录。

### 3.11 iCloud

iCloud可以让用户随时随地用不同的设备访问他们想要的内容。将iCloud集成到应用中，用户不用进行同步操作就可以在不同场景下使用不同的设备访问并编辑私人信息。 [![icloud_intro_2x](https://isux.tencent.com/wp-content/uploads/2015/11/20151117203432106.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151117203432106.png) 为了提供这种体验，你可能需要重新检查你的应用中现有的信息，尤其是用户自建内容的存储、访问和展示方式。想要了解如何使用iCloud，请参考[iCloud Design Guide](https://developer.apple.com/library/ios/documentation/General/Conceptual/iCloudDesignGuide/Chapters/Introduction.html).

iCloud用户体验的一个基本方向是透明性：理想情况下，用户不需要知道他们的信息存储在什么地方，也不需要去思考当前浏览的信息是哪个版本的。以下几点可以帮助你创建用户期望的iCloud体验。

**如果可能，让用户方便地在你的应用中启用iCloud。**在iOS设备上，用户可以在设置中登录iCloud账户，因此多半用户会期望应用可以自动启用iCloud。但是如果你觉得用户可能需要自主选择是否使用你应用的云服务，你可以在用户第一次进入应用时提供一个简单的选项来进行设置。大多数情况下，这个选项应该为：是否将所有内容上传到云端。

**尊重用户的iCloud空间。**一定要记住iCloud空间是用户花钱买来的有限资源。你应该使用iCloud来存储用户自己创建和可理解的信息，避免将可再生的应用资源和内容存储在云端。同样要记住，当用户登录了iCloud账户时，你的应用的文件夹内容也会自动备份到云端。所以为了节省用户云端空间，你最好只挑选必要的信息存储于文件夹中。

**避免让用户自己选择在iCloud上存储哪些文件。**一般地，用户会期望他们在意的所有信息都能够通过iCloud访问到。实际上大多数用户都不需要进行个人文件存储的管理，所以你的应用也可以不用考虑这个问题。为了提供更好的用户体验，你可能想要重新构建处理和展示内容的方式，这样就可以给用户提供更多的文件管理功能。

**决定哪种类型的信息需要存储在云端。**除了存储用户自建的文件和内容，你还可以存储少量的其他信息在云端，例如用户当前的状态，用户的偏好设置等等。你可以使用iCloud的关键值存储来保存这类信息。例如，用户使用你的应用看了一个杂志，你可以使用iCloud的关键值存储来保存用户浏览到的位置，这样用户在别的设备上重新打开这个杂志时就能从上次离开的地方继续浏览了。

如果你使用iCloud的关键值存储来保存用户的偏好设置，确保用户在每个设备上都是想这样设置的。例如，有些偏好设置在工作环境中比在家里要更好用。在某些情况下，将偏好设置保存在应用服务器上要比保存在云端更合理，这样偏好设置就不会受iCloud的限制。

**确保iCloud无法使用时应用的行为是合理的。**例如，用户退出iCloud账户，关闭应用的iCloud或者进入飞行模式时，iCloud都是无法使用的。在这些情况下，用户都进行了某些操作来禁止iCloud服务，所以你的应用可以不用再进行提醒。但是，需要告诉用户在打开iCloud之前，当前做的修改在其他设备上都无法看到。

**避免给用户创建“本地”文件的选项。**不管你的应用是否支持iCloud，都不应该给用户提供因设备而区分的文件系统。相反，你应该希望用户关注通过iCloud访问文件的普适性。

**在合适的时候自动更新信息。**最好不需要用户来确认他们正在访问的是最新的内容。但是，也需要在用户设备存储空间和带宽限制之间做出平衡。如果你的用户要使用非常大的文件，那么让他们自己选择是否要从云端下载一个更新的文件可能更合适。如果需要这样做的话，可以设计一种方式来指出当前在云端有一个该文件的最新版本。当用户选择更新时，如果下载时间较长最好给用户明显的反馈。

**告知用户删除某文件的后果。**当用户从有iCloud服务的应用上删除文件的时候，这个文件同样会从用户的iCloud账号和其他设备上删除。所以最好在执行删除操作之前告知用户删除的后果，让用户进行确认。

**必要时尽可能早地告知用户冲突问题。**使用iCloud编程接口，你需要在不打扰到用户的情况下解决大多数不同版本之间的冲突问题。但在有些情况下，你需要尽可能早地检测出冲突问题来避免用户在错误版本上浪费太多时间。你需要设计一种自然的方式来告诉用户有冲突存在，接着给用户提供方便的方式来区分不同版本以及做出决策。

**确保在搜索中包括用户在云端的信息。**使用iCloud的用户趋向于认为云端的信息是普遍可访问的，所以他们会期望搜索结果中也有云端的信息。如果你的应用允许用户搜索他们的信息，确保你使用了将搜索扩展到iCloud账户的接口。

### 3.12 HealthKit

在iOS 8及之后的版本中，使用HealthKit构建的应用可以利用从健康应用中获取的数据为用户提供更强大、更完整的健康及健身服务。在用户允许的情况下，应用可以通过HealthKit来读写健康应用(用户健康相关数据的存储中心)中的数据。

举例来说，用户可以允许营养应用从健康应用中获取体重及活动数据，用于告诉他们为了达到既定目标一天应该消耗多少卡路里。这个营养应用还可以通过HealthKit更新健康应用上实际消耗的卡路里数据，让用户能更容易地跟踪他们的健康计划的进展。想要了解如何将HealthKit整合进你的应用中，请参阅_[HealthKit Framework Reference](https://developer.apple.com/library/ios/documentation/HealthKit/Reference/HealthKit_Framework/index.html#//apple_ref/doc/uid/TP40014707)._

下面的指南能够帮助你设计出让人信任且喜爱的健康类应用：

**当且仅当你有令人信服的理由时才去访问健康应用中的数据。**HealthKit是为了专注于健康及健身服务的应用而设计的。如果一个应用请求获取与其不相关的健康信息，用户不太可能会放心地将个人数据提供给这个应用。因此，你需要确保用户能够理解你的应用需要获取他们某些具体的个人健康数据的原因，并告诉他们共享这些数据的好处。

**避免在用户还不知道用途前就向他们请求访问私人健康数据。**当用户能够看到当前的任务和你需要访问的数据的关联性时，会更乐意给予你访问权限。举例来说，当用户在给一个减肥应用填写资料时，让他允许你访问健康应用中储存的体重数据是合理的。但如果那个减肥应用在启动时就立即提出访问体重数据的请求，用户更可能会选择拒绝分享该个人数据。

**使用系统提供的用户界面来请求访问用户的数据。**当用户想要向应用授予访问他们的数据的权限时，一般会期望看到如下图所示的系统权限许可列表。为了确保给用户提供良好的用户体验，应避免在应用的其他页面中重复使用权限许可列表上的信息。而是应该在权限列表中添加些自定义信息来说明为什么你的应用需要访问特定的数据(参阅[_HKHealthStore Class Feference_](https://developer.apple.com/library/ios/documentation/HealthKit/Reference/HKHealthStore_Class/index.html#//apple_ref/doc/uid/TP40014708)可获取更多信息)的原因。确保这些信息简洁且能清晰地说明你的应用是如何利用健康应用中的数据，以及收集这些数据的好处。

[![HealthKit](https://isux.tencent.com/wp-content/uploads/2015/12/2015120117223587.png)](https://isux.tencent.com/wp-content/uploads/2015/12/2015120117223587.png)

注意：当用户决定停止与你的应用共享数据时，让他们可以在系统设置中即可完成变更，而不需要通过你的应用界面。

**不要在你的应用界面中使用健康应用的图标、图片或者截图。**和苹果所有的系统设计一样，这些图像都是受到版权保护的，不应该在你的应用中出现。

**不要在你的应用中使用****“HealthKit”****这个专用术语。**HealthKit是代表能够获取健康应用中储存的数据的技术框架的专用技术术语。如果你需要向用户解释你的应用和健康应用中的数据的联系，请使用“健康应用”这个用语。例如，你可以说你的应用“将保存信息至健康应用中”或“所使用的数据是从健康应用中获取的”。

### 3.13 应用内购买服务(In-App Purchase)

应用内购买服务使得用户可以在你的应用中、你所设计的商店中购买到数字产品。

[![1](https://isux.tencent.com/wp-content/uploads/2015/12/20151201181720966.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151201181720966.png)

例如，用户可以做这些事：

* 将一个应用从基础版本升级到高级版本。
* 每月订阅新内容。
* 购买虚拟商品，比如游戏中的等级或道具。
* 购买并下载新的书籍。

你可以使用StoreKit框架以嵌入的方式将商店添加到你的应用中，并且用来支持应用内购买服务。当用户进行购买时，StoreKit会连接到应用商店进行安全支付，然后再告知你的应用以便它可以提供用户已购买的商品。

重要:应用内购买服务只提供支付功能，其他功能由你自己提供，例如向用户展示商品，解锁内置功能，从你自己的服务器上下载内容等等。当然，你所提供的所有商品都必须在应用商店注册过。

想要了解关于在应用中添加商店的技术要求，请查看_[In-App Purchase Programming Guide](https://developer.apple.com/library/ios/documentation/NetworkingInternet/Conceptual/StoreKitGuide/Introduction.html#//apple_ref/doc/uid/TP40008267)._想要了解更多关于应用内购买的商业需求信息，请查看[App Store Resource Center](http://developer.apple.com/appstore/).当然，你还应该查看相关许可协议来确定你的应用可以出售哪些商品以及如何提供商品。

遵循以下几点规范，可以帮助你设计出用户喜欢的购买体验。

**将商店的使用体验优雅地集成到你的应用中。**在展示商品和处理交易时，给用户提供一种熟悉、一致的体验。你一定不希望用户在访问你的商店时感觉像是进入别的应用。

**使用简单明了的标题和说明。**最好能让用户在扫过一组项目时，可以快速发现感兴趣的内容。文案上不要截断隐晦，简单直白的语言和标题更容易让用户理解你所要展示的商品。

**不要更改默认的确认对话框。**当用户购买一个商品时，StoreKit会提供一个确认对话框(如上图所示)。这个确认对话框可以帮助用户避免买错东西，所以不要修改它。

### 3.14 游戏中心(Game Center)

游戏中心给用户提供玩游戏、组织多人在线游戏以及其他更多功能。玩家可以使用内置的游戏中心应用来注册账户、发现新游戏、添加好友、浏览玩家排名和战绩。

[![2](https://isux.tencent.com/wp-content/uploads/2015/12/20151201181743246.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151201181743246.png)

作为一名游戏开发人员，你可以使用GameKit应用接口来发布分数和战绩到游戏中心的服务器上，在你的游戏页面中显示玩家排名，帮助用户找到其他玩家。想要了解如何将游戏中心集成到你的应用中，请查看[Game Center Programming Guide](https://developer.apple.com/library/ios/documentation/NetworkingInternet/Conceptual/GameKit_Guide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40008304).

遵循以下几点规范，有助于你的应用给用户提供好的游戏中心体验。

**不要使用自定义的用户界面来提示用户登录到游戏中心。**如果用户在未登录到游戏中心的情况下打开了一个需要启用游戏中心的应用，系统会自动提醒他们去登录。所以没必要自定义一个登录界面，而且有可能还会让用户感到困惑。

**一般情况下，使用标准的游戏中心界面。**在少数情况下，可能自定义游戏中心的界面是合理的，但是这样做会有让用户感到困惑的风险。标准的游戏中心界面对于iOS和OS X的用户是熟悉的，而且它会给用户一种置身于一个庞大游戏社区的感觉。

**允许用户关闭语音聊天。**有些用户可能不想在进入游戏时就自动开启语音聊天，而且大多数用户希望在特定情境下可以关闭语音聊天。

### 3.15 iAd富媒体广告(iAd Rich Media Ads)

如果你允许你的应用中出现广告，那么你可以通过用户浏览或者点击这些广告获得收益。(如图所示，这个底部预留位置就是用来放置iAd横幅广告。)

[![3](https://isux.tencent.com/wp-content/uploads/2015/12/20151201181809653.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151201181809653.png)

通过iAd网络你可以在你的用户界面中以特定的视图投放一则广告。最初，这种视图可以用来承载目标横幅广告，起到引导用户进入查看全面广告详情的作用。当用户点击该横幅广告时，广告就会执行预先设定的动作，例如播放一段影片、展示可交互的内容，或者启动Safari打开目标网页。该动作所展示的内容可以遮挡住你当前的用户界面，或者使你的应用转换到后台运行。

有三种类型的横幅广告供你在应用中使用：标准(standard)、中等矩形(medium rectangle) 和全屏(full screen)。所有类型的横幅虽然在外观和行为上存在差异，但都提供同样的功能，就是引导用户进入广告。

**标准横幅(****standard banner)**占用屏幕较少的空间，通常从始至终都可见。你可以选择在应用的哪些页面展示标准横幅，并在给这些页面设计布局时预留出空间。

![4](https://isux.tencent.com/wp-content/uploads/2015/12/20151201182127534.png)所有的iOS应用都可以展示标准横幅。你可以使用[ADBannerView](https://developer.apple.com/library/ios/documentation/UserExperience/Reference/ADBannerView_Ref/index.html#//apple_ref/occ/cl/ADBannerView)类中的广告视图来显示标准横幅广告。

**中等矩形横幅** **(medium rectangle banner)** 的行为同标准横幅类似，同样也可以选择展示中等矩形横幅的位置。

[![5](https://isux.tencent.com/wp-content/uploads/2015/12/20151201182255304.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151201182255304.png)

中等矩形横幅只能在iPad的应用中使用。你可以使用[ADBannerView](https://developer.apple.com/library/ios/documentation/UserExperience/Reference/ADBannerView_Ref/index.html#//apple_ref/occ/cl/ADBannerView)类中的广告视图来显示中等矩形横幅广告。

**全屏横幅** **(full screen banner)** 会占用屏幕的大部分甚至是全屏空间，并且通常只在应用程序流的特定时间或特定位置显示。你可以选择使用模态视图来显示横幅广告，或者用独立页来展示可滚动的广告内容。(在下面的示例中，应用提供了一种杂志阅读的体验，通过翻页离开或回到全屏广告页面。)

[![6](https://isux.tencent.com/wp-content/uploads/2015/12/20151201182419357.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151201182419357.png)

你可以使用[ADInterstitialAd](https://developer.apple.com/library/ios/documentation/iAd/Reference/ADInterstitialAd_Ref/index.html#//apple_ref/occ/cl/ADInterstitialAd)类中的广告视图在你的应用中显示全屏横幅广告。

iAd框架包含了所有类型的横幅广告，并且会在右下角显示iAd的标识。iAd框架的设计固定在屏幕底部时看起来效果最佳。

为了保证广告无缝植入，并且要提供最好的用户体验，可以遵循以下几点规范。

**将标准横幅广告视图尽量放置在屏幕底部或底部附近。**这个位置的差别取决于屏幕底部是否包含栏(bar)以及是什么样的栏。

| col 1                      | col 2       |
| -------------------------- | ----------- |
| **栏**                      | **标准横幅的位置** |
| 屏幕底部没有栏                    | 屏幕底部        |
| 屏幕任何地方都没有栏                 | 屏幕底部        |
| 有工具栏(toolbar)或标签栏(tab bar) | 底部栏的上方      |

**将中等矩形横幅广告视图放置在不会干扰内容的地方。**和标准横幅一样，中等矩形横幅也最好放置在屏幕底部或底部附近。放在底部附近也能减少干扰用户的可能性。

**当用户体验存在中断时请使用模态视图来展示全屏横幅广告。**如果你的应用中有自然中断或情景转换，用模态样式来展示会更合适。当你使用模态样式来展示全屏横幅时(通过用[presentFromViewController](https://developer.apple.com/library/ios/documentation/iAd/Reference/ADInterstitialAd_Ref/index.html#//apple_ref/occ/instm/ADInterstitialAd/presentFromViewController:)实现)，用户要么进入广告，要么关闭它。出于这个原因，当用户有做出转变的预期时 (比如完成了一个任务后) 用模态视图的形式来展示比较好。

**应用的界面视图进行转场切换时不要使用模态样式展示全屏横幅。**如果用户在使用你的应用时会频繁的进行屏幕切换操作，例如杂志翻页或翻阅一些画册图片合集，此时使用非模态的形式会更合适。当你使用非模态来显示全屏横幅时(通过使用[presentInView](https://developer.apple.com/library/ios/documentation/iAd/Reference/ADInterstitialAd_Ref/index.html#//apple_ref/occ/instm/ADInterstitialAd/presentInView:)实现)，可以在用户界面中保留栏 (bar) 使得用户可以通过应用中的控件进入或退出广告。同其他横幅广告一样，点击全屏横幅广告也会触发iAd体验，但是如果条件允许的话，你的应用也可以对横幅广告区域支持其他手势操作 (比如拖动或滑动)。

确保使用合适的动画效果来显示和隐藏非模态的全屏横幅视图。例如，杂志阅读应用可以用和杂志翻页一样的动画效果。

**确保横幅广告在应用中出现的时间和位置是合理的。**用户只有在不觉得广告会打扰他们正常的工作流程时才有可能去体验iAd.这点对于游戏这样的沉浸式应用尤其重要：你肯定不想将横幅放置在影响用户玩游戏的位置。

**避免将横幅放置在用户只会一扫而过的页面。**最好不要将横幅广告放置在用户会快速略过的页面，比如用户正要深入挖掘或前往他们所关注的内容。通常用户在一个页面停留至少1、2秒后才有可能会点击广告。

**尽可能的支持双向展示横幅广告。**最好让用户在使用应用时不必旋转设备就能浏览广告。当然，支持双向也能给你的广告提供更大的展示区域。想要了解如何确保转换方向时横幅广告能正常响应，请查看[iAd Programming Guide](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/iAd_Guide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40009881).

**不要让标准或中等矩形横幅广告滚出屏幕。**如果你的应用需要滚动来展示更多内容，确保横幅广告一直固定在它的位置上。

**当用户浏览或与广告进行交互时，暂停那些吸引用户注意力或需要操作的活动。**当用户选择浏览广告时，他们不想因此错过应用中正发生的事件，也同样不想让应用打断广告体验。一个好的经验方法是像应用程序转入后台运行那样暂停当前活动。

**除非有特殊情况，否则不要中断广告。**一般情况下，当用户浏览并与广告进行交互时，应用还是会继续运行并接收事件，所以也有可能突然出现一个事件需要获得用户的注意力。然而，需要打断广告的场景其实非常少。有一种情景是有的应用会提供互联网语音协议服务(VoIP).在这种应用中，有电话接入时可能会取消正在运行的广告。

注意:取消广告可能会对应用能接受的广告类型以及能获取的收益有不好的影响。

### 3.16 无线打印 (AirPrint)

用户可以通过AirPrint无线打印应用中的内容，还可以使用打印中心应用检查打印任务。

[![7](https://isux.tencent.com/wp-content/uploads/2015/12/20151201182531197.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151201182531197.png)

你可以利用内置的支持程序来打印图片和PDF文件，或者可以使用特定的打印程序接口来完成自定义的格式设置和渲染设置。iOS可以处理打印机的发现、任务排序以及在指定打印机上执行打印任务。

通常来讲，用户想要打印文件的时候，只需要点击应用中的标准动作按钮(Action button)。当他们在界面视图中选择了要打印的项目后，可以接着选择打印机，设置打印属性，最后点击打印按钮开始打印。

打印中心应用是一个只有在处理打印任务时才可见的后台系统应用，用户可以用它来查看打印任务。用户可以在打印中心浏览当前打印队列，查看某个打印任务的详情，还可以取消某个任务。

只需添加少量代码就可以支持基本打印功能 (想要了解在代码中添加打印功能，请查看[Drawing and Printing Guide for iOS](https://developer.apple.com/library/ios/documentation/2DDrawing/Conceptual/DrawingPrintingiOS/Introduction/Introduction.html#//apple_ref/doc/uid/TP40010156)).想要确保好的打印体验，可以遵循以下几点规范：

**使用系统提供的动作按钮。**用户对系统提供的按钮的含义和行为都很熟悉，所以尽可能的使用系统动作按钮。如果你的应用没有工具栏或导航栏，那就要另当别论了。在这种情况下，你就需要自己设计一个可以出现在应用主界面的打印按钮，因为动作按钮只能在工具栏和导航栏中使用。

**在当前情境下打印操作是基本功能时才显示打印项****(Print item).****如果当前情境并不适合打印，或者用户并不想打印，就不要在由动作按钮显示的视图中将打印项显示出来。**

**合适的话，给用户提供更多打印选项。**例如，让用户设置打印页码范围或打印份数。

**如果用户不能打印，则不要显示特定的打印用户界面。**在向用户展示有打印项的界面前，确保用户的设备是支持打印的。想要了解如何在代码中实现，请查看[UIPrintInteractionController Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIPrintInteractionController_Class/index.html#//apple_ref/doc/uid/TP40010141).

### 3.17 访问用户数据(Accessing User Data)

位置服务允许应用获取用户当前大致的地理位置，设备指向的方向以及用户移动的方向。其他系统服务，例如通讯录、日历、备忘录和相册等，同样也允许应用访问用户存储在里面的数据。

[![8](https://isux.tencent.com/wp-content/uploads/2015/12/20151202124418779.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151202124418779.png)

虽然获取了用户数据的应用能带来一定的方便，但还是需要为用户提供维持信息私密性的功能。例如，用户喜欢应用自动给内容加上位置标签，或者可以找到附近的好友，但用户也需要能在不想分享位置的时候关闭这些功能。(想要学习如何给应用增加获取位置功能，请参阅_[Location and Maps Programming Guide](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/LocationAwarenessPG/Introduction/Introduction.html#//apple_ref/doc/uid/TP40009497)._)

以下几点可以帮助您以用户不反感的方式获取用户数据。

**确保使用户理解分享私人数据的原因。**如果没有明显的需要，用户自然会对私人信息的请求感到怀疑。为了避免用户反感，确保在用户使用明显需要个人信息的功能时再进行提醒。例如，即使没有打开位置服务用户也可以使用地图，但是在用户使用定位或导航功能时就会有提醒。

**应用需要个人信息的原因不明显时向用户做出解释。**你可以在提醒框中给出文字性的描述，例如“这个应用需要访问你的通讯录”或者“是否允许应用获取你的地理位置？”。这些文案最好明确且有礼貌以让用户无压力的理解为什么需要访问他们的信息。

讲述原因的文案应该遵循以下原则：

* 不要包含你的应用名称，因为系统提供的提醒框已经包含了。
* 清楚地描述你的应用为什么需要这些数据。如果可以的话，你也可以解释不会用这些数据做什么。
* 使用以用户为中心的术语并且进行本地化。
* 在易于理解的情况下越短越好。尽可能避免超过一句话。
* 使用句式大小写(sentence-style capitalization).(句式大小写指的是第一个单词大写，除了专有名词和专有形容词以外的词都小写。)

**只有当你的应用没有用户数据就无法提供基础服务时，才在一开始就征求用户的许可。**如果你的应用在知道了用户私人信息后才能提供主要功能是显而易见的话，用户不会因此觉得烦扰。

**避免在用户选择需要数据的功能之前调用触发提醒框的程序。**这样，就可以避免用户疑惑为什么在使用不需要私人数据的功能时有请求提醒。(注意，检查用户位置服务的设置并不会触发提醒。)

**检查位置服务的设置来避免触发没必要的提醒。**你可以使用核心位置的程序接口来实现(想要学习如何做，请参阅_[Core Location Framework Reference](https://developer.apple.com/library/ios/documentation/CoreLocation/Reference/CoreLocation_Framework/index.html#//apple_ref/doc/uid/TP40007123)_).使用这些知识，可以尽可能地在使用需要位置信息的功能时才进行提醒，或者完全避免提醒。

### 3.18 快速查看(Quick Look)

通过使用Quick Look，用户可以在你的应用内预览文件，即使你的应用是打不开这个文件的。举例来说，你可以允许用户预览一些从网站上下载或从其他来源获得的文件。

[![quicklook1](https://isux.tencent.com/wp-content/uploads/2015/12/2015120117354253.png)](https://isux.tencent.com/wp-content/uploads/2015/12/2015120117354253.png)

想要学习如何在应用中加入Quick Look文件预览功能，请参阅[Document Interaction Programming Topics for iOS](https://developer.apple.com/library/ios/documentation/FileManagement/Conceptual/DocumentInteraction_TopicsForIOS/Introduction/Introduction.html#//apple_ref/doc/uid/TP40010403).

在你的应用内预览文件之前，用户可在你定制的视图中查看该文件的信息。例如，用户从一封邮件中下载了附件之后，邮件应用(Mail)会在邮件中使用定制的视图展示文件的图标、标题和大小。用户可以通过点击它来预览文件。

[![quicklook2](https://isux.tencent.com/wp-content/uploads/2015/12/20151201173604707.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151201173604707.png)

你可以在应用中用一个新的视图来展示文件预览，或者使用全屏模态视图。展示的形式取决于你的应用运行在什么设备上。

**在****iPad****上使用模态视图来显示文件预览。**iPad的大屏幕适合在一个方便用户离开的沉浸式环境中展示文件预览。缩放操作(zoom transition)很适合展示预览。

**在****iPhone****上使用专用的视图，最好是导航视图来显示文件预览。**这样可以使用户在应用情境中通过导航进入文件预览，不至于迷失。虽然也可以在iPhone应用中使用模态显示，但不推荐这样做。(注意缩放操作在iPhone上并不适用。)

另外要注意的是，在导航视图中显示文件预览意味着允许Quick Look在导航栏上放置特定的预览控件。(如果你的视图中包含工具栏，Quick Look会将预览控件放在工具栏上。)

### 3.19 声音(Sound)

无论声音在你的应用中是主要体验的一环，还是锦上添花的元素，你都需要知道用户对声音表现的期望以及与如何满足这些期望。

### 3.19.1 理解用户期望(Understand User Expectations)

人们可以使用设备控件来调整声音，他们还可能使用有线或无线的耳机和听筒。人们也会对于他们的行为如何作用于他们听到的声音有各种各样的期望。虽然你可能会发现有一些期望很让人意外，但它们都会遵循用户控制的原则，即应是用户而非设备掌控听到声音的时机。

**用户会依据需要将设备静音：**

* 避免被突兀的音效打断，比如手机铃声和信息接收音等
* 避免听到用户操作所产生的副产品的声音，比如键盘或其他反馈音、偶然的声音或应用启动的声音
* 避免听到那些在玩游戏时非必要出现的声音，如音效和配乐

例如，在剧院中，用户将他们的设备调至静音以避免打扰剧院中的其他人。在这一情境下，用户仍然希望能在他们的设备上使用应用，但他们不希望被无预期或突兀的声音所打断，如手机铃声或新消息音。

当用户操作的明确目的就是听到声音时，铃音/静音开关(或静音开关)不会屏蔽这些操作所产生的声音。例如：

* 在仅有媒体播放功能的应用中的进行媒体播放是不会被静音的，因为播放媒体是用户明确期望的。
* 闹钟不能被静音，因为闹钟是用户明确设定使用的。
* 语言学习应用中的音效素材不能被静音，因为用户进行了明确的操作希望听到它。
* 音频对话应用中的对话不被静音，因为用户打开这个应用的唯一目的就是进行音频对话。

**用户使用设备音量调节按键可调节他们的设备所能发出的所有声音的音量**，包括歌曲、应用音效和设备声音。不管铃声/静音(或静音)的开关在什么位置，用户都能使用音量调节按键屏蔽所有声音，使用音量调节按键调节应用当前所播放的音频时同样调整了全局系统的音量，铃声音量除外。

对于iPhone：当没有音频播放时使用音量键可以调整铃声音量。

**用户使用耳机的目的在于能够私密地收听声音以及解放他们的双手。**不管这些配件是有线的还是无线的，用户对这个体验都有特定的期待。

当用户插入耳机或连接无线音频设备时，他们期望能以私密的状态继续收听当前播放的音频。因此，他们希望应用能够不中断地继续播放当前正在播放的音频。

当用户拔出耳机或断开与无线设备的连接时(抑或设备超出范围或关闭时)，他们不希望他们刚刚收听的内容被自动地与他人分享。因此，他们希望正在播放音频的应用暂停播放，让他们能够在自己想要继续播放的时候再开启。

### 3.19.2 定义应用的音频行为(Define the Audio Behavior of Your App)

**如果必要的话，你可以通过调整相关的、独立的音量水平以在你的应用中制造最好的混音输出效果。**但最终音效输出的音量也应该能由系统音量控制，可以通过音量键或音量滑块进行调节。这意味着应用的音频输出的控制权仍然归属在用户手中。

**确保你的应用能适时地显示音频路径选择。**(音频路径(audio route)是指音频信号的电子通路，例如从设备到耳机或是从设备到扬声器。)即使人们没有物理性的插入或拔出音频设备，他们也仍希望能选择其他不同的音频路径。为了实现这一诉求，iOS能自动显示可让用户选择输出音频路径的控件(使用[MPVolumeView](https://developer.apple.com/library/ios/documentation/MediaPlayer/Reference/MPVolumeView_Class/index.html#//apple_ref/occ/cl/MPVolumeView)类能允许这个控件显示在你的应用中)。由于选择不同的音频路径是用户主动的行为，用户期望当前播放的音频能继续不中断。

**如果你需要显示音量滑块，**在使用[MPVolumeView](https://developer.apple.com/library/ios/documentation/MediaPlayer/Reference/MPVolumeView_Class/index.html#//apple_ref/occ/cl/MPVolumeView)类时，确保使用的是系统提供的可用的音量滑块。注意，当正在使用的音频输出设备不支持音量控制时，音量滑块会被合适的设备名称所替代。

**如果你的应用只产生一些与其功能无必要关系的界面音效时，****(****尽量****)****使用系统音效服务****(****System Sound Services****)****。**系统音效服务是一种能产生警示音、界面音效和发出振动的iOS技术；它不适合任何其他用途。当你使用系统音效服务(System Sound Services)来产生音效时，你不能干涉你的音频与设备的音频的交互方式，也不能干涉它处理干扰和设备配置变化的方式。想了解如何使用这一技术，请参阅[_Audio UI Sounds (SysSound)_](https://developer.apple.com/library/ios/samplecode/SysSound/Introduction/Intro.html#//apple_ref/doc/uid/DTS40008018)中的范例项目。

**如果音效在你的应用中扮演重要的角色，使用音频会话服务****(****Audio Session Services****)**或是[AVAudioSession](https://developer.apple.com/library/ios/documentation/AVFoundation/Reference/AVAudioSession_ClassReference/index.html#//apple_ref/occ/cl/AVAudioSession)类。这些程序接口不产生音效；相反，它们会帮助你了解你的音频应该如何与设备的音频进行交互以及如何响应设备配置的干扰与变化。

对于iPhone：无论你使用什么样的技术来制作音频，无论你如何定义来它的行为，电话总是可以中断当前运行的应用。这是因为任何应用都不应该阻止人们接收来电。

在音频会话服务(Audio Session Service)中，音频会话(audio session)执行了你的应用与系统之间音频中介的功能。音频会话中最重要的方面之一就是类目(category)，它定义了你的应用的音频行为。

为了实现音频会话服务带来的好处并提供用户期望的音频体验，你需要选择可以完美描述应用音频行为的类目(category)。具体情况取决于你的应用只在前台播放音频还是也要在后台播放音频。在你做这一选择的时候，遵循以下这些原则：

* **依据其语义而非精确的行为来选择音频会话类目。**通过选择目的清晰的类目，你可以确保你的应用能表现得符合用户期望。除此之外，当以后行为的精确集合被重新定义时，它可以为你的应用提供最佳的机会使其合理运行。
* **在极少数情况下，可以添加属性到音频会话中以修正一个类别的标准行为。**一个类别的标准行为代表多数用户的期望，因此在你改变那个行为之前你应该仔细地考虑。例如，你可以添加闪避(ducking)属性以确保你的音频声音能比其他所有的音频都大(除了电话音频)，如果这就是用户所期望的。(欲了解更多关于音频会话属性的内容， 请参见的[Fine-Tuning the Category](https://developer.apple.com/library/ios/documentation/Audio/Conceptual/AudioSessionProgrammingGuide/AudioSessionBasics/AudioSessionBasics.html#//apple_ref/doc/uid/TP40007875-CH3-SW2)。)
* **依据设备当前的音频环境来考虑你的类目选择。**这应该是合理的，举个例子，用户可以在使用你的应用的同时听其他音频而非你的配乐。如果要这样做，须确保避免当你的应用启动时，迫使用户停止收听当前的内容或要需要额外地在两者之间做出选择。
* **通常情况下，避免在你的应用运行时改变类目。**改变类目的首要依据是你的应用是否需要在不同的时机支持录音和播放。在这种情况下，更好的选择是依据需要在录音类目与播放类目之间转换，而非同时选择播放和录音类目。这是因为选择录音类目可以确保正在录音时不会听到提示音，比如收到信息的提示音。

表35-1列举了你可以使用的音频会话类目。不同的类目可以允许通过铃声/静音开关或静音开关(或设备锁)来实现静音、与其他的音频混合或者控制应用在后台播放。(欲了解编程界面上所呈现的类目和属性的准确名称，请参见_[Audio Session Programming Guide](https://developer.apple.com/library/ios/documentation/Audio/Conceptual/AudioSessionProgrammingGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40007875)._)

表35-1 音频会话类目及其相关行为

| col 1  | col 2                 | col 3  | col 4   | col 5    |
| ------ | --------------------- | ------ | ------- | -------- |
| **类目** | **意义**                | **静音** | **混合**  | **后台播放** |
| 个人环境   | 声音增强了应用的功能且应该静音其他音频   | 支持     | 不支持     | 不支持      |
| 环境     | 声音增强了应用的功能但不应该静音其他音频。 | 支持     | 支持      | 不支持      |
| 播放     | 声音对应用来说很重要且可以与其他音频混合。 | 不支持    | 不支持(默认) |          |

支持(当“与其他音频混合”属性被添加时) | 支持      
录音     | 音频是用户记录的。             | 不支持    | 不支持                             | 支持      
播放和录音  | 声音代表音频输入与输出，按顺序地或同时地。 | 不支持    | 不支持(默认)

支持(当“与其他音频混合”属性被添加时) | 支持      
音频处理   | 应用执行硬件辅助音频编码(不播放或录音)。 | 不适用    | 不支持                             | 支持*     

\*如果你选择音频处理类目并且你希望在后台运行音频进程，你需要在完成音频处理之前防止你的应用被暂停。欲了解如何实现这一功能，参见[_《__iOS__应用编程指南》_](https://developer.apple.com/library/ios/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40007072)中的执行长时间运行的后台任务。

以下是一些示例情境，其中指示了如何选择音频会话类目以提供用户喜欢的音频体验。

**情境****1****：一个帮助人们学习新语言的教育类应用。**你需要提供：

* 用户点击特定控件时播放反馈音效
* 当用户想听到正确发音的示例时播放字词的录音

在这个应用中，声音对于主要功能是十分重要的。人们使用这个应用来听他们正学习的语言的词语与短语，因此即使当设备锁定或者被调至静音时也要能播放声音。因为用户需要清晰地听到声音，他们会期望其他他们可能播放的音频都被静音。

为了满足用户对于该应用所期望的音频体验，你应该使用播放(Playback )类目。虽然这一类目可以被定义为与其他音频混合，但该应用应该使用默认的行为以确保其他的音频不会干扰那些用户明确选择听到的教育性内容。

**场景****2****：网络协议电话****(VoIP)****应用。**你需要提供：

* 接收音频输入的能力
* 播放音频的能力

在该应用中，声音对于主要功能是十分重要的。人们经常会在使用另一个应用时使用该应用与他人进行交流。用户期望能在他们将设备调至静音或设备被锁定时接听电话，他们希望在来电期间其他音频被静音。他们也希望应用在后台运行时也能继续打电话。

为了满足用户对于该应用所期望的音频体验，你应该使用播放和录音(Play and Record)类目，并且你要确保只有在你需要时才会激活你的音频会话，以便用户可以在打电话过程中使用其他音频。

**场景****3****：允许用户在不同任务中操作角色的游戏。**你需要提供：

* 不同的游戏运行音效
* 配乐

在该应用中，声音会在很大程度上提升用户体验，但对于主任务并没有那么重要。而且，用户可能会希望能在玩游戏时静音或听他们乐单中的歌曲而不听游戏配乐。

最好的策略是在你的应用启动时确定用户是否在收听其他音频。不要要求用户选择他们是要收听其他音频或是你的音效。而应该使用音频会话功能中的[AudioSessionGetProperty](https://developer.apple.com/library/ios/documentation/AudioToolbox/Reference/AudioSessionServicesReference/index.html#//apple_ref/c/func/AudioSessionGetProperty)来请求[kAudioSessionProperty_OtherAudioIsPlaying](https://developer.apple.com/library/ios/documentation/AudioToolbox/Reference/AudioSessionServicesReference/index.html#//apple_ref/c/econst/kAudioSessionProperty_OtherAudioIsPlaying)属性的状态。依据所请求的答案，你可以选择环境(Ambient)或是个人环境(Solo Ambient)类目(这两种类目都允许用户静音玩游戏)：

* 如果用户正在听其他音频，你应该假设他们想要继续听并且不想被强迫收听游戏音效。在这种情境下，你最好选择环境(Ambient)类目。
* 如果用户在你的应用启动时没有在收听其他音效，你最好选择个人环境(SoloAmbient)类目。

**情境****4****：一个为用户到达目的地提供准确、实时导航指示的应用。**你需要提供：

* 路途中每一步的语音指示
* 一些反馈音效
* 支持用户继续收听他们自己的音频的能力

在该应用中，无论应用是否是在后台运行，语音导航指示都表现为主要任务。基于这一原因，你最好使用播放(Playback)类目，它允许你的音频在设备被锁定、静音或是在后台运行时仍可以播放。

你可以通过添加[kAudioSessionProperty_OverrideCategoryMixWithOthers](https://developer.apple.com/library/ios/documentation/AudioToolbox/Reference/AudioSessionServicesReference/index.html#//apple_ref/c/econst/kAudioSessionProperty_OverrideCategoryMixWithOthers)属性来实现允许人们在使用你的应用时收听其他音频。但是你也想要确保用户在他们正在播放其他音频时能听到语音提示。你可以为音频会话添加[kAudioSessionProperty_OtherMixableAudioShouldDuck](https://developer.apple.com/library/ios/documentation/AudioToolbox/Reference/AudioSessionServicesReference/index.html#//apple_ref/c/econst/kAudioSessionProperty_OtherMixableAudioShouldDuck)属性来确保你的音频比其他音频的声音更大( iPhone上的电话音频除外)。这些设置允许应用在后台运行时也可以恢复音频会话，可以确保用户能获得实时更新的导航。

**情境****5****：一个允许用户上传文本和图片到网站上的博客应用。**你需要提供：

* 简短的启动音效文件
* 伴随用户行为产生的各式各样的短音效(例如当邮件被上传后播放的音效)
* 发送失败时播放的提示音

在该应用中，声音提升了用户体验，但也不是必需的。主任务与音频并没有关系，用户也不是必须要通过收听声音才能成功使用应用。在这一情境中，你最好使用系统声音服务来产生声音。这是因为这个应用中所有声音的音频情境都符合本技术想要达到的目的，也就是说应制作符合用户所期待的、能通过设备和铃声/静音(或静音)开关来调节的界面音效和提示音。

### 3.19.3 管理音频中断(Manage Audio Interruptions)

有时候，当前播放的音频会被来自于不同应用的音频所打断。举个例子，在iPhone上，来电会持续中断当前应用的音频。在多任务情境中，这种音频中断的频率可能会很高。

为了提供用户喜欢的音频体验，iOS系统依赖于你能做到下面几点：

* 识别可能会引起应用中断的音频类型
* 当应用在音频中断结束后继续运行时进行合理地反馈

每个应用需要识别会引起音频中断的类型，但不是每个应用都需要决定如何在音频中断结束后进行反馈。这是因为多数类型的应用应在音频中断结束后恢复音频。只有那些主要或部分由媒体播放组成(以及提供媒体播放控制)的应用，才必须用额外的步骤来决定什么是合适的反馈。

从概念上讲，基于中断当前音频的音频类型以及中断结束后用户所期望的特定的应用反馈方式，有两种类型的音频中断：

* **可恢复性中断是****(****resumable interruption****)**被用户视为临时穿插在他们的主要聆听体验中的音频引起的。

在可恢复性中断结束后，有媒体播放控件的应用应该恢复它被中断前的任务，无论是继续播放音频还是保持暂停。没有媒体播放控件的应用则应该恢复播放音频。

举个例子，试想用户在iPhone上使用应用播放音乐时，在播一首歌的中间来了一个网络电话。用户接起了电话，期望在他们通话时播放的应用能静音。在通话结束后，用户希望播放的应用自动恢复播放歌曲，因为音乐而非电话才是他们的主要聆听体验，而他们在电话接入前也没有暂停音乐。另一方面，如果用户在电话接入前暂停了音乐播放，他们会希望电话结束后音乐仍保持暂停。

其他能引起可恢复性中断的应用的例子还有那些具备闹钟、音频提示(例如语音方向指示)或其他间歇性音频功能的应用。

* **不可恢复中断****(****nonresumable interruption****)**是由那些被用户视为首要听觉体验的音频所引起的，比如媒体播放产生的音频。在不可恢复中断结束后，显示媒体播放控件的应用不应该恢复播放原来的音频。而没有媒体播放控件的应用应该恢复播放音频。例如，假设用户正在收听一个音乐播放应用(音乐应用1)，此时另一个音乐播放应用(音乐应用2)打断了它。用户终止后决定收听音乐应用2一段时间。在退出音乐应用2之后，用户不想要音乐应用1自动恢复播放，因为此时他们主动将音乐应用2作为首要的听觉体验。

下面的指南可以帮助你决定当一个音频中断后如何继续以及提供什么信息:

**确定由你的应用引起的音频中断的类型。**在你的音频结束时，你可以通过以下任意一种方式去禁用你的音频会话来做到这一点：

* 如果你的应用引起了一个可恢复性中断，使用[AVAudioSessionSetActiveFlags_NotifyOthersOnDeactivation](https://developer.apple.com/library/ios/documentation/AVFoundation/Reference/AVAudioSession_ClassReference/index.html#//apple_ref/c/econst/AVAudioSessionSetActiveFlags_NotifyOthersOnDeactivation)标识禁用你的音频会话。
* 如果你的应用引起了一个不可恢复中断，不用任何标识就可以禁用你的音频会话。

无论提供与否，标识会在适宜的情况下允许iOS系统赋予被中断的应用自动恢复播放它们的音频的能力。

**决定是否应该在一个音频中断结束后恢复音频。**你应依据你应用中所提供的音频体验来做这一决断。

* 如果你的应用给用户呈现了用于播放或暂停音频的媒体播放控件，你需要在一个音频中断结束后检查[AVAudioSessionInterruptionFlags_ShouldResume](https://developer.apple.com/library/ios/documentation/AVFoundation/Reference/AVAudioSession_ClassReference/index.html#//apple_ref/c/econst/AVAudioSessionInterruptionFlags_ShouldResume)标识，如果你的应用接受应该恢复(Should Resume)标识，你的应用应该：
* 恢复播放音频(你的应用被打断时在主动播放音频)  
    **·**不恢复播放音频(你的应用被打断时没有在主动播放音频)
* 如果你的应用没有呈现任何用户可用于播放或暂停音频的媒体播放控件，你的应用无论是否有“应该恢复”标识，都始终应在音频中断结束后恢复之前播放的音频。例如，播放配乐的游戏应该在被中断后自动恢复播放配乐。

### 3.19.4 适时处理媒体远程控制事件(Handle Media Remote Control Events, if Appropriate)

当人们使用iOS媒体控制器或辅助控制器(如耳机线控)时，应用要能响应远程控制。使你的应用能接收来自于你的用户界面之外的输入，无论你的应用当前是在前台还是后台播放音频。

应用可以在播放媒体的过程中，通过后台向支持Airplay的硬件(如Apple TV)发送视频。这样的应用可以接收通过远程控制事件实现的用户输入行为，因此用户可以控制处于后台运行状态的应用中的视频播放。除此之外，这类应用在后台运行时也能恢复被中断的音频。

当一个媒体播放应用在后台播放音频或视频时，尤其需要合理响应媒体远程控制事件。

当你的应用在后台运行时，为了满足与播放媒体特权相关的责任，要确保遵循以下这些原则：

**限制你的应用接收远程控制事件的次数。**例如，当你的应用可以帮助用户阅读内容、搜索信息或是收听音频时，它只有在用户处于音频场景中时才应该接收远程控制事件。当用户脱离音频情境时，你应该放弃接收事件的能力。如果你的应用允许用户在支持AirPlay的设备上播放音视频，它应该在媒体播放期间都可以接收远程控制事件。遵循这些原则能使用户在你的应用中处于非媒体情境中时，通过耳机控制获得另一个应用的媒体体验。

**尽可能地使用系统原生的控件以提供****AirPlay****支持。**当你使用[MPMoviePlayerController](https://developer.apple.com/library/ios/documentation/MediaPlayer/Reference/MPMoviePlayerController_Class/index.html#//apple_ref/occ/cl/MPMoviePlayerController)类实现AirPlay播放功能时，你可以利用标准的控件使用户可以选择当前范围内支持AirPlay的硬件。或者你可以使用[MPVolumeView](https://developer.apple.com/library/ios/documentation/MediaPlayer/Reference/MPVolumeView_Class/index.html#//apple_ref/occ/cl/MPVolumeView)类来显示用户可选择的支持AirPlay的音频或视频设备。用户习惯于这些标准控件的外观和行为，因此他们可以理解如何在你的应用中使用它们。

**不要改变事件的用途，即使这个事件在你的应用中没有意义。**用户期望iOS系统的所有应用媒体控制和辅助控制能有功能上的统一。你不必实现你的应用所不需要的那些事件，但你所实现的事件必须产生符合用户期望的结果。如果你重新定义一个事件的意义，你会使用户困惑并冒险把他们带入一个未知的状态，他们只能通过退出你的应用来逃离。

### 3.20 VoiceOver

VoiceOver增加了对盲人、弱视用户以及一些有特定学习困难的用户的可用性。

[![1](https://isux.tencent.com/wp-content/uploads/2015/11/20151126162834978.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151126162834978.png)

为了确保VocieOver的用户能使用你的应用，你需要在你的用户界面中提供一些有关视图和控件的描述信息。对VoiceOver的支持不需要你改变你用户界面内的任何视觉设计。

当你完全遵照标准的方式使用标准的用户界面元素时，几乎不(即使有也很少)需要增加额外的工作。你的用户界面越趋向定制化，你就越需要提供更多的信息来保证VoiceOver能准确的描述你的应用。

增加你的iOS应用对VoiceOver用户的可用性，可以扩大你的用户基础并帮助你进入新的市场。支持VoiceOver也可以帮助你遵守由主流群体所制定的可用性指导准则。

### 3.21 路线选择(Routing)

地图可以显示到达用户目的地的可选路线：

[![2](https://isux.tencent.com/wp-content/uploads/2015/11/2015112616283910.png)](https://isux.tencent.com/wp-content/uploads/2015/11/2015112616283910.png)

当人们想要获得关于某条路线的更多交通信息时，地图也可以显示能提供路线选择的应用列表(包括安装在设备上的应用也包括应用商店中的应用)。

[![3](https://isux.tencent.com/wp-content/uploads/2015/11/20151126162842696.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151126162842696.png)

**路线选择应用**可以提供当前选择的路线有关的信息。人们希望路线选择应用能够快捷、易用，特别是保证准确性。依据本章提供的指导原则能帮你为用户提供他们可信任的交通信息和他们期望的用户体验。

重要：地图能依据人们选择的路线给他们提供驾车和步行的指示。路线选择应用可以提供交通信息，它着重于使用交通工具(如公交车、火车、地铁、渡船、自行车、行人、穿梭巴士等)的模型替代实物逐步地指示方向。

如果你的应用不能提供用户指定的路线的交通信息，那么不要将你的应用定位为路线选择应用。

**实现你的应用所承诺的功能。**当人们在交通列表里看到你的应用时，他们认为它可以帮助其到达目的地。但是如果你的应用不能提供所选路线的信息，或者它没能涵盖它看似应该涵盖的那些种类的交通信息，人们就不会愿意给它第二次机会。准确的表达出你的应用的能力是十分重要的；否则，你的应用会看起来像是在故意误导用户。

在你的路线选择应用中，有两种主要的方式可以给用户信心：

* 尽可能准确的定义你所支持的地理区域。例如，如果你的应用能帮助人们获得巴黎的公交线路的信息，那你所支持的地区应该是巴黎，不是法兰西岛，也不是法国。
* 明确你所支持的交通信息类型。举个例子，如果你专攻于地铁信息，不要暗示你仿佛支持所有的轨道交通类型

注意：虽然准确的报告你所支持的地区可能意味着会减少你的应用在交通信息列表里的出现次数，但这么做却可以帮助用户更加信任它。

**为易用性合理组织界面。**易用性对于路线规划应用来说特别重要，因为用户常常会在极具挑战性的情况下使用它们——例如在明亮的阳光下、在昏暗的车厢内抑或是在颠簸的旅程中，或在非常紧急的情况下。要确保你的文字在任何光照条件下都能容易的阅读，确保按钮即使在并不平稳的旅程中也能易于准确点击。

**专注于路线。**虽然辅助信息会很有用，但你的应用应该专注于为用户提供逐步的指示以便他们能据此到达目的地。特别要强调的是，你要让用户知道他们处于哪一步，并知道如何到达下一步。你可以提供额外的数据(比如时间表或系统地图)，但不要让这些数据比交通信息还重要。

**为路线的每一步提供信息。**永远不要让用户感觉被你的应用所遗弃。即使在可以准确的报道你所支持的地区时，你也不能假定用户已经抵达的路线中的第一个交通节点或是最后一个交通节点就是他们目的地点。为了控制这一情况，首先就是测量起点到终点距离。如果距离足够短，要提供从用户当前位置到第一个交通节点及从最后一个交通节点到用户目的地的步行方向指示。如果步行不是一个合理的选择，尝试描绘用户的其他选项。如果必要的话，你可以给用户提供打开地图，获取这部分路线的步行或驾车方向指示的方式。

**当用户从地图应用切回你的应用时，不要要求他们重复输入信息。**如果用户从地图应用切入(你的应用)时，你已经获知了他们中意的起点与终点，因此你可以在应用打开时直接呈现适合的交通信息。如果用户从主屏幕中开启你的应用，要为他们提供简洁的方式用以输入路线详情。

**显示图文并茂的交通信息。**地图页面可以帮助人们以更大的、实物性的视角查阅他们完整的线路；清晰的步骤可以帮助人们专注于他们抵达目的地所需采取的必要行动。最好可以同时支持这两个任务并能让用户便捷地进行切换。

注意：无论以什么格式，最重要的是显示与用户线路相关的相同的交通信息。例如，如果路线中包含五个步骤，在地图和路线列表页中必须描绘相同的五步。

当你的应用被从交通列表中选中时，需要以显示完整的线路做为良好的开始(包括在地图页面中显示始于或抵达交通节点的步行路线)。地图页面可以为用户提供他们旅途的多步骤的总览，并能展示适于周遭地理环境的路线。

**用附加信息丰富地图页面。**人们期望你的应用中的地图可以表现的与他们使用过的其他地图相似。除了用户能放大和缩小以外，你还应该显示用户所需的那些注释信息。例如，你应该显示图钉用以代表用户当前的位置、目的地以及沿路的转乘点或重要的节点。

确保避免只显示一个单独的图钉，因为对用户来说，如果没有额外的背景，很难理解它代表什么。欲了解在你的应用中使用地图页面的更多信息，请参阅[_Map View._](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/ContentViews.html#//apple_ref/doc/uid/TP40006556-CH13-SW134)

尽可能地整合静态地图页面，例如在地图视图中加入地铁系统地图等。一个很好的实现方法就是在地图页面覆盖静态图片，以便用户可以看到他们的路线及他们的当前位置是如何与更大的交通系统相关联的。

注意：如果你决定让应用显示一个静态的地图图片，要确保使用高分辨率的图片以保证用户在缩放时维持高质量的显示。

**给用户提供不同的方案来挑选多样的交通选择。**很多因素会影响人们交通的选择，例如不同的时间段，天气以及他们携带东西的多少，所以提供简洁的不同交通方式的对比是十分重要的。例如，你要能让用户可以依据开始或结束的时间、需要步行的数量、沿途停下的次数抑或转乘的次数或所需的不同的交通类型等来挑选交通方式。不管你显示多种交通选择的顺序如何，确保用户能立即分辨出这些选项的不同之处。

**考虑使用推送通知为人们提供与路线相关的重要信息。**尽可能的让人们了解交通情况信息的变化，以便他们可以据此调节自己的计划。例如，如果火车晚点或者巴士路线临时停滞，人们可能会需要选择不同的交通路线到达目的地。而在一条不同步骤的站点之间相隔很长距离的交通路线中，人们会希望在他们的交通工具将要抵达行程中的下一部分时能获得通知。

### 3.22 编辑菜单(Edit Menu)

用户能呼出一个编辑菜单来完成诸如在文本视图、网页或图片视图中的剪切、粘贴以及选择操作。

[![4](https://isux.tencent.com/wp-content/uploads/2015/11/20151126162846274.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151126162846274.png)

你可以通过调整一些菜单的行为使用户对你应用中的内容有更多的控制权。举个例子，你可以：

* 列举出适用于当前情境的标准菜单的命令
* 在菜单显示前判定菜单的位置，以避免你应用的用户界面中的重要信息被遮盖
* 定义当用户双击展开菜单时会被默认选中的对象

你不能改变菜单本身的颜色和形状。

欲了解如何在代码中实现这些行为的相关信息，请参阅[Copy, Cut, and Paste Operations](https://developer.apple.com/library/ios/documentation/StringsTextFonts/Conceptual/TextAndWebiPhoneOS/UsingCopy,Cut,andPasteOperations/UsingCopy,Cut,andPasteOperations.html#//apple_ref/doc/uid/TP40009542-CH11).

为了确保编辑菜单在你的应用中的表现符合用户期望，你应该：

**显示在当前情境下合理的命令。**例如，当没有对象被选择的时候，菜单中不应该包括复制或剪切(命令)，因为这些命令是针对选择(的内容)而操作的。相似地，如果有对象被选择的时候，菜单中不应该包括选择(命令)。如果你在自定义页面中支持编辑菜单，你就有责任确保菜单中显示的命令切合当前的情境。

**依据你的页面布局调节菜单显示。**iOS依据可获得的空间大小选择在插入点的上方或下方来放置菜单指针以显示编辑菜单，这样用户就能看到菜单命令是如何与内容相关的。在必要的情况下，你可以通过程序在菜单显示之前决定它的位置，这样可以避免用户界面中的重要信息被遮挡。

**支持两种手势来调用菜单。**虽然点击和长按手势是用户呼起编辑菜单的首选方式，但他们也可以在文本页面中通过双击一个单词来选择该单词并同时呼起菜单。如果你在自定义页面中支持菜单，确保它能支持两种手势。除此之外，你可以定义用户双击时默认的选择对象。

**避免在你的用户界面中创建和编辑菜单中功能相同的按钮。**例如，使用编辑菜单让用户进行复制操作远比提供一个复制按钮要好，因为用户将会想知道为什么在你的应用中会有两种方法做同样的事。

**如果静态文本的选择对用户来说是有用的，那么可以考虑使用它。**用户可能想要复制图片的标题，但他们不可能想复制选项卡的标签或是屏幕的标题，比如“账户(Account)”。在文本页面内，文字的选择应该是默认设置的。

**不要使按钮标题可选择。**如果按钮的标题是可选择的，用户很难在不激活按钮的情况下呼出编辑菜单。通常来说，像按钮这样操作的元素不需要是可选择的。

**将对撤销与重做的支持与对复制与粘贴的支持组合到一起。**人们经常希望在他们改变主意的时候能撤销最近的操作。由于编辑菜单在它操作执行的时候是不需要确认的，你应该给用户提供撤销或重做这些操作的机会。

如果你需要创建自定义的编辑菜单项，需要像下面展示的这个例子一样遵循这些指导原则：

[![5](https://isux.tencent.com/wp-content/uploads/2015/11/2015112616285047.png)](https://isux.tencent.com/wp-content/uploads/2015/11/2015112616285047.png)

**创建直接作用于用户选择的包含编辑、修改或其他操作的编辑菜单。**人们期望在当前的情境内用标准的编辑菜单项操作文本或对象，那么你的自定义菜单项最好能有相似的表现。

**将自定义项列在所有系统提供的项的后面。**不要将你的自定义项与系统提供的项混置在一起。

**保持自定义菜单项的数量在合理的范围内。**你不应该用太多选择迷惑你的用户。

**使用简洁的名称命名你的自定义菜单项**并确保名称能准确的描述命令的作用。通常，项的名字应该是一个可以描述行为如何执行的动词。虽然你通常会使用单个的大写单词作为名字，但如果你必须使用一个短语(作为名字)时，就应使用标题式大写短语。(简洁的、标题性的大写词就是将除了文章、四字及四字以下的并列连词与介词之外的单词都大写。)

### 3.23 撤销与重做(Undo and Redo)

用户通过摇晃设备触发撤销操作，显示提醒框让他们可以：

* 撤销他们刚才输入的内容
* 重做先前撤销的输入
* 取消撤销操作

[![6](https://isux.tencent.com/wp-content/uploads/2015/11/20151126162853676.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151126162853676.png)

你可以通过在你的应用中定义出更通用的方式来支持撤销操作：

* 允许用户撤销或重做的行为
* 在你的应用的哪种情形下晃动手势是用于撤销操作的
* 支持多少步的撤销

欲了解如何用代码实现这一行为，请参阅[Undo Architecture](https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/UndoArchitecture/UndoArchitecture.html#//apple_ref/doc/uid/10000010i).如果在你的应用中支持撤销和重做，请遵循以下准则以提供好的用户体验:

**为用户提供简洁的描述性短语使其能准确的获知他们正在撤销或重做的内容。**iOS系统自动提供了“撤销”和“重做”的字符串(包括词语后面的空格)作为撤销警示按钮的标题，但你需要提供一或两个词语用于辅助描述用户的重做或撤销操作。例如，你可能提供文本的“命名”或“地址更改”之类的词语用以创建像“撤销命名”或“重新更改地址”这样的按钮标题。(要注意，在提醒框中，“取消”按钮是不能改变或移除的)。

[![7](https://isux.tencent.com/wp-content/uploads/2015/11/20151126162857383.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151126162857383.png)

**避免提供的文本过长。**太长的按钮标题容易被断章取义并且很难被用户解读。由于这个文本用于按钮的标题中的，要使用标题样式的大写形式并且不能添加标点。

**避免过度使用摇晃手势。**即使你能程式化地设定你的应用将摇晃事件作为用户激活撤销操作的途径，你也在冒着混淆用户视听的风险，因为他们也可能使用摇晃执行另一个不同的操作。分析你应用中的人机交互以避免创建那些用户无法可靠地预测摇晃手势结果的场景。

**如果撤销和重做在你的应用中是基础性的任务，尽量使用系统原生的撤销与重做按钮。**记住摇晃手势是用户触发撤销与重做操作的主要方式，而如果提供两种不同方式完成同样的任务则会使用户困惑。如果你认为很有必要提供直观专有的撤销与重做操作，你可以在导航栏中放置系统原生的按钮。(欲了解更多关于这些按钮的信息，参见[Toolbar and Navigation Bar Buttons](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Bars.html#//apple_ref/doc/uid/TP40006556-CH12-SW33)).

**将撤销与重做能力与用户当下的情境进行清晰地关联，而非过早地介入情境。**仔细考虑你允许进行撤销与重做操作的情境。通常来说，用户期望他们的改变和操作可以立即被有效的执行。

### 3.24 键盘和输入页面(Keyboards and Input Views)

在iOS8与之后的系统中，你可以创建自定义的键盘扩展内容来替代系统的原生键盘。欲了解更多关于管理应用内扩展(包括键盘)的信息，请参阅[APP Extensions](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/AppExtensions.html#//apple_ref/doc/uid/TP40006556-CH67-SW1)；欲了解如何开发自定义的键盘扩展内容的信息，请参阅[Custom Keyboard](https://developer.apple.com/library/ios/documentation/General/Conceptual/ExtensibilityPG/Keyboard.html#//apple_ref/doc/uid/TP40014214-CH16).

在合适的情况下，你9也可以在你的应用内设计自定义的输入页面来替代系统原生的屏幕键盘。例如，Numbers(译者注：iWork中的电子表单应用程序)中提供了多种输入页面，这些页面设计使数量、日期和其他值的输入能简单高效地完成。

[![8](https://isux.tencent.com/wp-content/uploads/2015/11/20151126162900925.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151126162900925.png)

如果你提供自定义输入页面，确保它的功能对于来用户来说是清晰易懂的。

你也可以提供自定义的输入辅助视图，这种视图通常表现为显示在键盘(或你的自定义输入页面)上方的一个独立元素。例如，在某些情境中，Numbers会显示一个输入辅助视图用以帮助用户执行针对电子表格中的值的标准或自定义计算。

[![9](https://isux.tencent.com/wp-content/uploads/2015/11/20151126162904433.png)](https://isux.tencent.com/wp-content/uploads/2015/11/20151126162904433.png)

当用户在你的输入页面中敲击自定义控件时，使用标准的键盘敲击声提供声音反馈。欲了解在代码中如何使用这一声音，请参阅[_UIDevice Class Reference_](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIDevice_Class/index.html#//apple_ref/doc/uid/TP40006902)中的[playInputClick](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIDevice_Class/index.html#//apple_ref/occ/instm/UIDevice/playInputClick)章节

注意：标准的敲击音效只适用于当前屏幕上的自定义输入页面。人们可以在设置-声音中关闭所有的键盘音效(包括你的自定义输入页面中的那些)。

## 4. UI元素

## 4.1 栏

### 4.1.1 状态栏

状态栏展示了关于设备及其周围环境的重要信息。

默认(深色)内容[](https://isux.tencent.com/wp-content/uploads/2015/12/20151223190426168.png) ![status_bar_default_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223190426168.png)

浅色

![status_bar_light_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223190508294.png)

状态栏：

- 是透明的
- 始终固定在整个屏幕的上边缘

API注释

你可以将全应用的状态栏风格设计成统一的，或者给不同的视图控制器定义不同的状态栏风格。想要了解更多内容，你可以通过[UIApplication Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40006728)来了解[UIStatusBarStyle](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html#//apple_ref/c/tdef/UIStatusBarStyle)常数，以及通过[UIViewController Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40006728)来了解更多关于[preferredStatusBarStyle](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIViewController_Class/index.html#//apple_ref/occ/instm/UIViewController/preferredStatusBarStyle)属性的内容。

**不要创建自定义状态栏。**用户依赖系统默认状态栏的一致性。就算你可能会在应用中隐藏它，也不宜定制一个新的UI来代替原有系统状态栏。

**避免滚动内容直接透过状态栏显示。**你不会希望用户在滚动的时候看到五花八门的内容和状态栏自身的元素混合在一起。想要让用户感受到内容区域够大的同时，最大限度地保证可读性，请保证在状态栏后面添加一块背景，用以模糊出现在状态栏后的内容。以下有一些方法可以让滚动的内容能正常显示在状态栏后面：

- 使用导航控制器(navigation controller)来展示内容。导航控制器自动展示状态栏背景，同时能确保内容视图不会出现在状态栏后面。（了解更多请参考 [Navigation Controllers](https://developer.apple.com/library/ios/documentation/WindowsViews/Conceptual/ViewControllerCatalog/Chapters/NavigationControllers.html#//apple_ref/doc/uid/TP40011313-CH2)）。


- 在状态栏后面放一个低调的、不会抢走用户注意力的自定义图形——比如一道渐变。想要保证这样的图形始终固定在状态栏后面，你可以用视图控制器(view controller)来让它固定在滚动内容上一层，又或者可以用滚动视图(scrolling view)来保证图形固定在屏幕的顶部。
- 让内容固定在导航栏区域外显示（这个区域由应用的[statusBarFrame](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html#//apple_ref/occ/instp/UIApplication/statusBarFrame)属性来定义）。如果你确定要这样做的话，请给导航栏区域添加固定的、与屏幕背景色相同的背景色。

**千万千万，避免在状态栏后面叠加会分散注意力的内容。**尤其是，你不能让用户觉得轻击状态栏之后可以获取内容或激活你的应用中的控件。

**隐藏状态栏时请慎重。**由于状态栏是透明的，通常情况下不需要隐藏它。始终隐藏状态栏意味着用户必须退出你的应用才能知道现在的时间，或者了解当前环境下是否有Wi-Fi连接。

**在用户全屏观看媒体时，考虑隐藏状态栏以及所有页面UI。**当你这么做的时候，请确保用户在轻击屏幕时即可重新唤起状态栏以及相关的UI。而除非你有充分的理由，否则最好不要重新定义一个手势来让用户唤起状态栏，因为用户不会发现，就算发现了也难以记住。

**为你的应用选择配色协调的状态栏颜色。**默认的状态栏内容是黑色的，在浅色应用中效果出色，而相应的浅色状态栏则更适用于颜色较深的应用。

**在适当的时候展示网络活动指示器(network activity indicator)。**这可以提醒用户显示长时间的网络接入状态。更多详情请参考本章第三节控件部分的网络活动指示器部分([Network Activity Indicator](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/Controls.html#//apple_ref/doc/uid/TP40006556-CH15-SW44))。

### 4.1.2 导航栏

导航栏能够实现在应用不同信息层级结构间的导航，有时候也可用于管理当前屏幕内容。

![nav_bar_iphone_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223194729322.png)

![nav_bar_ipad_7_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223194728844-590x55.png)

导航栏：

- 是半透明的


- 通常位于屏幕的上方，状态栏正下方。在横屏视图中，导航栏也可以包含在某一视图中，不需要与整个屏幕等宽，比如说它可以出现在对分视图控制器(split view controller)的其中一侧。


- 当键盘被唤起、用户使用了手势、或者当前视图变为竖屏的情况下，导航栏可以隐藏。
- 可以填充颜色(使用[tintColor](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIBarButtonItem_Class/index.html#//apple_ref/occ/instp/UIBarButtonItem/tintColor)来定义导航栏中的图标与文字颜色；使用 [barTintColor](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UINavigationBar_Class/index.html#//apple_ref/occ/instp/UINavigationBar/barTintColor)来填充导航栏背景色)

API注释

导航栏包含于导航控制器（一个管理显示自定义视图层级结构的程序对象）中。想要了解更多关于如何在代码中定义一个导航栏的信息，请参阅[Navigation Controllers](https://developer.apple.com/library/ios/documentation/WindowsViews/Conceptual/ViewControllerCatalog/Chapters/NavigationControllers.html#//apple_ref/doc/uid/TP40011313-CH2), *UINavigationController Class Reference*和 *UINavigationBar Class Reference*.

你可以用导航栏在不同视图间提供导航，或在上面放置管理当前视图内容的相关控件。如果你需要提供导航栏难以承载的大量控件同时又不是非要提供导航不可，你可以考虑使用工具栏(Toolbar)。

当用户到达一个新的层级，导航栏需要做出这样的改变：

- 导航栏标题应该变成当前层级的标题。
- 当前标题左侧放置应有返回按钮，需要的话，返回按钮可以以前一层级的标题命名。

** 使用当前视图的标题作为导航栏标题。**若觉得标题冗余，你也可以将标题留空。举个例子，备忘录的导航栏中就没有当前备忘录的标题，因为备忘录的第一行就已经提供了所有用户需要的内容。

![nav_bar_title_not_required_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223195203477.png)

**考虑在应用最高层级的导航栏中放置一个分段控件**。它能够帮助你更好地扁平信息层级，也会让用户更容易找到所需内容。如果在导航栏中使用了分段控件，请确保返回按钮标题命名的准确。（更多使用指引请参阅本章第三节中的分段控件。）

![prompt_stocks_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223195424737.png)

如果需要的话，可以考虑在导航栏位置使用提示语(prompt)来告诉用户在当前屏幕中他们可以做什么。提示语是一句出现在导航栏顶部的短句。举个例子，股票应用(Storcks)中就给用户提供了这么一句提示，来确保用户知道怎么去搜索自己想要的信息。

如果你需要用到提示语，请设计一句简明扼要的单句，并在句末配以适当的标点符号。

**即使空间充足，也应当避免让过多的控件填满你的导航栏。**一般来说，导航栏上应该不多于以下三个元素：当前视图的标题、返回按钮和一个针对当前的操作控件。而当你在导航栏中使用了分段控件，就不要再放标题以及其它多余控件了。

**确保文字按钮之间拥有足够的空间。**如果导航栏左边或右边的文字按钮之间的间距太小，那些文字看起来会像挤在一起一样，让用户难以区分。如果按钮在导航栏中显得太过拥挤，你可以使用UIBarButtonSystemItemFixedSpace常数来给他们增加适当的间距。（想要了解更多关于这个常数的内容，请参考 [UIBarButtonItem Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIBarButtonItem_Class/index.html#//apple_ref/doc/uid/TP40007519).）

**确保你自定义的导航栏在你的应用的每个视图中都拥有一致的外观与体验。**举个例子，不要在同一个应用中使用不透明导航栏和半透明工具栏。在屏幕处于同一方向时，最好不要改变不同屏上导航栏的背景图片、颜色和透明度。

**确保你自定义的返回按钮的外观与操作仍然像一个返回按钮。**用户知道系统默认的返回按钮能帮助他们在信息层级中追踪自己的路径，如果你想重新设计它，请确保使用一个自定义的蒙版图层 (custom mask image)，它可以在iOS中让这些按钮标题在系统各转场中出现或者消失。

重要

不要创建多段式(multisegment)返回按钮。返回按钮通常是用来帮助用户回到当前层级的父层级中去的。如果你担心用户在没有了这种多节式的、如同面包屑一般的返回按钮后会迷路，那么你也许该好好考虑如何扁平你的信息层级了。

**在用户需要专注于内容的时候，可以考虑隐藏导航栏。**当你这么做的时候，请确保用户通过一个简单的手势（比如一下轻击）即可重新唤起导航栏。

![nav_bar_map_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223195651759-590x375.png)

### 4.1.3 工具栏

工具栏上放置着用于操作当前屏幕中各对象的控件。

![mail_toolbar_iphone_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223195738136.png)

[![mail_toolbar_ipad_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223195737636-590x33.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223195738136.png)

工具栏：

- 是半透明的
- 在iPhone上，工具栏始终位于屏幕底部，而在iPad上则有可能出现在顶部
- 当键盘被唤起、用户使用了手势、或者当前视图变为竖屏的情况下，工具栏可以隐藏。

API注释

工具栏包含在导航控制器(navigation controller)中，该控制器用于管理定制视图中信息层级的展示形式。 想要了解如何在代码中定义工具栏，请参考[Displaying a Navigation Toolbar](https://developer.apple.com/library/ios/documentation/WindowsViews/Conceptual/ViewControllerCatalog/Chapters/NavigationControllers.html#//apple_ref/doc/uid/TP40011313-CH2-SW4)以及[UIToolbar Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIToolbar_Class/index.html#//apple_ref/doc/uid/TP40006927).

你可以在工具栏里提供一系列让用户对当前视图内容进行操作的工具。

**在工具栏里放置用户在当前情景下最常用的指令。**尽量避免在工具栏里提供一些仅会偶尔用到的指令。

**可以在工具栏里放置分段控件以方便用户快速切换当前内容的不同视图或模式。**在工具栏中提供应用全局的任务或者模式分段控件是不恰当的，因为工具栏中的所有操作都应当是针对当前屏幕和视图的。如果你需要让用户可以快速唤起应用全局的任务、或改变全局视图和模式，可以使用标签栏(Tab Bar)。想要了解更多分段控件的内容，请参考下文的分段控件(Segmented Control)部分；想要了解更多标签栏的内容，请参考下文中的标签栏(Tab Bar)部分。

**如果需要在工具栏上展示3个以上的项目，可以使用图标。**由于文本按钮通常会比图标更占空间，所以用图标可以避免文字标题们挤在一起。

**保证工具栏文字按钮之间有足够的间距。**如果按钮之间间距过小，会让蚊子看起来挤在一起，让用户觉得它们难以区分。如果按钮在导航栏中显得太过拥挤，可以用UIBarButtonSystemItemFixedSpace常数来增加他们之间的间距。（想要了解更多关于这个常数的内容，请参考 [UIBarButtonItem Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIBarButtonItem_Class/index.html#//apple_ref/doc/uid/TP40007519).）

### 4.1.4 工具栏与导航标准按钮

iOS提供了一系列工具栏与导航栏上的内置标准按钮。想要了解如何设计自定义图标，请参考本文第五章栏按钮图标(Bar Button Icons)部分。工具栏和导航栏图标的颜色可以通过tintColor属性来设定。

想要了解每一个按钮所对应的标志名称及其含义，请参阅[UIBarButtonItem Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIBarButtonItem_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40007519)中的[UIBarButtonSystemItem](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIBarButtonItem_Class/Reference/Reference.html#//apple_ref/c/tdef/UIBarButtonSystemItem)部分。

重要

跟所有标准按钮和图标相同，应当根据文档中说明的图标含义，而不是只凭图标外观来使用这些工具栏图标和导航栏图标。这样能够保证在关联特定意义的按钮改变了外观的情况下，你的应用中的UI仍然是可用而有意义的。

表格 **41-1 工具栏与导航栏标准按钮 ****(**Standard buttons available for toolbars and navigation bars)

| 按钮                                       | 名称               | 含义                                       |
| ---------------------------------------- | ---------------- | ---------------------------------------- |
| [![UIBarButtonAction_2x](https://isux.tencent.com/wp-content/uploads/2015/12/2015122320010464.png)](https://isux.tencent.com/wp-content/uploads/2015/12/2015122320010464.png) | 动作(Action)       | 唤起一个模态视图(modal view)，视图中包含系统级和应用自定义级的、针对当前内容的动作 |
| [![UIBarButtonCamera_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200116855.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200116855.png) | 相机(Camera)       | 唤起一个包含相机模式下的图片选择器的操作列表                   |
| [![UIBarButtonCompose_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200130803.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200130803.png) | 编写(Compose)      | 打开一个新的消息编辑视图                             |
| [![UIBarButtonBookmarks_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200143983.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200143983.png) | 书签(Bookmarks)    | 展示应用书签                                   |
| [![UIBarButtonSearch_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200200866.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200200866.png) | 搜索(Search)       | 展示搜索字段                                   |
| [![UIBarButtonAdd_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200211766.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200211766.png) | 添加(Add)          | 新建一个项                                    |
| [![UIBarButtonTrash_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200226312.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200226312.png) | 回收站(Trash)       | 删除当前项                                    |
| [![UIBarButtonOrganize_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200238372.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200238372.png) | 归档(Organize)     | 将某个项移动到应用内其他位置，比如另一个文件夹                  |
| [![UIBarButtonReply_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200251437.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200251437.png) | 回复(Reply)        | 将某个项发送或转发到另外一个位置                         |
| [![UIBarButtonRefresh_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200304306.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200304306.png) | 刷新(Refresh)      | 刷新当前内容（请尽量自动刷新，在必要时才使用刷新按钮）              |
| [![UIBarButtonPlay_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200316641.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200316641.png) | 播放(Play)         | 播放当前媒体内容                                 |
| [![UIBarButtonFastForward_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200332381.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200332381.png) | 快进(Fast Forward) | 快进当前多媒体或幻灯片                              |
| [![UIBarButtonPause_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200345732.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200345732.png) | 暂停(Pause)        | 暂停多媒体或者幻灯片播放（注意这意味着要保存当前内容）              |
| [![UIBarButtonRewind_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200403969.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200403969.png) | 回退(Rewind)       | 回退当前多媒体或幻灯片                              |

除了表格41-1里展示的标准按钮之外，你还可以使用系统提供的编辑、取消、保存、完成、撤销、重做等等按钮来支持编辑或其它操作。这些按钮的标题即是按钮的操作内容。想要了解每一个按钮的名称及其含义，请参阅[UIBarButtonItem Class Reference](http://www.cocoachina.com/newbie/basic/2013/0819/6827.html)中的[UIBarButtonSystemItem](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIBarButtonItem_Class/Reference/Reference.html#//apple_ref/c/tdef/UIBarButtonSystemItem).
另外，你还可以在工具栏中放置系统提供的信息按钮(info button).

![info_button_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200625282.png)

### 4.1.5 标签栏

标签栏让用户在不同的子任务、视图和模式中进行切换。

![music_tab_bar_iphone_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200655464.png)

![music_tab_bar_ipad_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200654942-590x37.png)

API注释

标签栏包含在标签栏控制器中，该控制器用于管理自定义视图的展示形式。想要了解如何在代码中定义标签栏，请参考[Tab Bar Controllers](https://developer.apple.com/library/ios/documentation/WindowsViews/Conceptual/ViewControllerCatalog/Chapters/TabBarControllers.html#//apple_ref/doc/uid/TP40011313-CH3)和[UITabBar](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITabBar_Class/index.html#//apple_ref/occ/cl/UITabBar).

标签栏位于屏幕底部，并应该保证在应用内任何位置都可用。标签栏是半透明的，展示图标和文字内容，每一项均保持等宽。当用户选中某个标签时，该标签呈现适当的高亮状态。

标签栏：

- 是半透明的
- 始终出现在屏幕的底部
- 一个标签栏一次最多可承载5个标签（多于5个标签的时候，可以展示前4个标签和一个“更多”，并将其他的标签以列表形式收纳到“更多”里面）
- 在横屏与竖屏情况下，高度均保持一致
- 你可以在标签上加上红底白字，显示数字或者省略号的小气泡(badge)以展示特定的应用信息

你可以使用标签栏来切换对同一组数据的不同视图模式，或者整体功能下不同的子任务。

**一般而言，使用标签栏来组织整个应用层面的信息结构**。标签栏非常适合用于应用的主界面中，因为它可以很好地扁平信息层级，并且同时提供多个触达同级信息类目与模式的入口。

**不要使用标签来让用户执行对于当前应用与屏幕内容的操作。**如果你需要给用户提供操作控件，请使用工具栏。

**即使标签当前不可用，也不要把它从标签栏中删除。**让某些标签时而出现时而隐藏，会让用户觉得你的应用UI不稳定而且难以预测。最好的解决方式是确保每个标签都可用，然后给用户解释某个标签的内容不可用的原因。举个例子，当用户没有在设备中保存任何歌曲，在系统音乐应用的歌曲标签页里就可以教育用户如何去下载一首歌。

**考虑在tab上加入红色的小气泡(Badge)以低调地传达信息。**你可以通过添加小气泡来告知用户该标签中包含新的内容。

**根据控件的标准含义来选择系统提供****的图标。**详情请查看下文中的标签栏标准图标(Tab Bar Icons)。如果想自定义标签栏图标，请参考文档第五章中Bar Buttons Icons里给出的建议。

**在横屏视图中，你可能会在对分视图(split view pane)或者浮出层****(popover)****内使用标签栏以切换或筛选视图中的内容。**如果这些标签是用于切换或者过滤当前视图中的内容的话，你可以这么做。然而通常情况下，在对分视图和浮出层底部使用分段控件效果会更好，因为视觉上看起来更为协调。更多详情请参考文档本章第三节中的分段控件。

**避免让过多的标签填满你的标签栏。**放置太多标签会让用户难以选中他想要点击的那一个。而同时每添加一个标签，意味着你的应用程序又复杂了一分。

**尽可能地在横屏与竖屏情况下都展示相同数量的标签。**在不同的屏幕方向下提供同样的标签可以让用户对应用建立很好的视觉稳定感。在横屏中，你应该将与竖屏时数量相同的标签居中展示。**在横屏中，避免使用“更多”标签。**如果应用是横屏的，那么把额外的操作都塞到一个“更多”里面是对空间一种糟糕的浪费。

### 4.1.6 标签栏标准图标

iOS提供了一系列标签栏标准图标，在下面的表格35-2中有详细展示。想要了解如何设计自定义图标，请参考文档第五章栏标准按钮部分。标签栏图标的颜色可以通过[tintColor](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIView_Class/index.html#//apple_ref/occ/instp/UIView/tintColor)属性来设定。

想要了解每一个图标的名称及其含义，请参阅[UIBarItem Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITabBarItem_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40006928)中的[UITabBarSystemItem](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITabBarItem_Class/index.html#//apple_ref/c/tdef/UITabBarSystemItem)部分。

重要

跟所有的标准按钮与图表相同，根据文档说明的图表含义而不是仅凭图表外观来使用这些图标是很关键的。这样能够保证在关联特定含义的按钮改变了外观的情况下，你的应用中的UI仍然是可用而有意义的。

表格 **41-2 标签栏标准按钮 **(Standard icons for use in the tabs of a tab bar)

| 按钮                                       | 名称                | 含义              |
| ---------------------------------------- | ----------------- | --------------- |
| [![UITabBarBookmarks_2x](https://isux.tencent.com/wp-content/uploads/2015/12/2015122320094490.png)](https://isux.tencent.com/wp-content/uploads/2015/12/2015122320094490.png) | 书签(Bookmarks)     | 显示应用书签          |
| [![UITabBarContacts_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200956882.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223200956882.png) | 通讯录(Contacts)     | 显示通讯录           |
| [![UITabBarDownloads_2x](https://isux.tencent.com/wp-content/uploads/2015/12/2015122320100859.png)](https://isux.tencent.com/wp-content/uploads/2015/12/2015122320100859.png) | 下载(Downloads)     | 显示下载内容          |
| [![UITabBarFavorites_2x](https://isux.tencent.com/wp-content/uploads/2015/12/2015122320102163.png)](https://isux.tencent.com/wp-content/uploads/2015/12/2015122320102163.png) | 个人收藏(Favorites)   | 显示用户的个人收藏       |
| [![UITabBarFeatured_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201032204.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201032204.png) | 精选(Featured)      | 显示应用推荐的精选内容     |
| [![UITabBarHistory_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201042914.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201042914.png) | 历史记录(History)     | 显示用户操作的历史记录     |
| [![UITabBarMore_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201057676.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201057676.png) | 更多(More)          | 显示更多标签项         |
| [![UITabBarMostRecent_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201112983.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201112983.png) | 最新(Most Recent)   | 显示最新的项          |
| [![UITabBarMostViewed_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201125935.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201125935.png) | 浏览最多(Most Viewed) | 显示所有用户最常浏览的热门内容 |
| [![UITabBarRecents_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201136312.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201136312.png) | 最近使用(Recents)     | 显示用户在指定时间内访问过的项 |
| [![UITabBarSearch_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201148931.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201148931.png) | 搜索(Search)        | 进入搜索模式          |
| [![UITabBarTopRated_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201159451.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201159451.png) | 评分最高(Top Rated)   | 显示用户评分最高的项      |

### 4.1.7 搜索栏

搜索栏获取用户键入的文本，用以作为搜索的关键字(下图中显示的文本为占位符，非用户输入文本)。

[![search_bar_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201236777.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201236777.png)

API注释

想要了解如何在代码中定义搜索栏，请参考[UISearchBar](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UISearchBar_Class/index.html#//apple_ref/occ/cl/UISearchBar).想要了解更多如何显示搜索栏，请参考[UISearchDisplayController](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UISearchDisplayController_Class/index.html#//apple_ref/occ/cl/UISearchDisplayController).

搜索栏可能包含以下这些可选元素：

- **占位符文本(Placeholder text)**。占位符文本通常会写明控件的功能（比如上图里的 “Search”字样），或者提示用户输入的文本将在哪里搜索（如“Google”）。


- 书签按钮(The* Bookmarks button)*。书签按钮可以让用户方便地找到他们需要的内容。例如在地图中搜索时，用户可以通过书签按钮快速选中书签地址、最近搜索记录、或通讯录。

![search_bar_bookmarks_2x](https://isux.tencent.com/wp-content/uploads/2015/12/2015122320154690.png)

书签按钮只有当搜索栏中没有占位符或用户输入内容时才会出现，当搜索栏中已有文本时，书签按钮会被清除按钮(Clear button)所代替。

- **清除按钮(The Clear button)**。大多数搜索栏都会提供清除按钮，方便用户一键清空输入内容。

![search_bar_clear_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201303787.png)

一旦用户在文本框中输入内容，清除按钮就会出现，用户可以用它来一键清空输入内容；而当搜索框中没有任何文本内容时，清空按钮将被隐藏。

- 结果列表图标(The* results list icon)*。结果图标说明此次搜索有搜出结果。当用户点击它时会出现用户最近一次搜索的搜索结果。

[![search_bar_prompt_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201630736.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223201630736.png)

- **提示(Prompt)****。描述性标题**，我们称之为提示。描述性标题是一个短而完整的句子，为搜索栏提供介绍或指引应用特定信息。

**在你的应用中使用搜索栏让用户进行搜索。不要使用文本框，**因为文本框的外观不符合用户对搜索的预期。

在iOS 8以及之后的版本里，你可以通过[UISearchDisplayController](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UISearchDisplayController_Class/Reference/Reference.html#//apple_ref/occ/cl/UISearchDisplayController)简单快捷地把搜索栏放在导航栏中。请注意，当搜索的视图控制器包含在导航控制器里面的时候——比如在邮件应用(Mail)中那样，当用户激活搜索时，搜索栏会自动上浮，平铺到原来导航栏的位置上。
**根据搜索功能在你的应用中的重要程度来选择搜索栏的样式。**如果搜索在你的应用中是最基础的功能，请使用突出样式(the prominent style)；如果搜索不是用户常用的功能，那么可以使用弱化样式(the minimal style)。

[![prominentstyle](https://isux.tencent.com/wp-content/uploads/2015/12/2015122320175323.png)](https://isux.tencent.com/wp-content/uploads/2015/12/2015122320175323.png)

### 4.1.8 范围栏

范围栏只有在与搜索栏一起时才会出现，它让用户可以定义搜索结果的范围。

API注释

想要了解如何在代码中定义搜索栏与范围栏，请参考[UISearchBar](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UISearchBar_Class/index.html#//apple_ref/occ/cl/UISearchBar).

当搜索栏出现时，范围栏会出现在它的附近。范围栏的外观与你所指定的搜索栏的外观兼容。

当用户想在明确的分类范围内进行搜索时，使用范围栏是非常有用的。然而，更好的选择是优化您的搜索结果，让用户不需要使用范围栏对搜索结果进行筛选，便可以找到他们所需要的内容。

 

## 4.2 内容视图

### 4.2.1 活动

每个活动表示一个系统提供的或自定义的服务——它可以通过访问活动视图控制器(Activity view controller)来作用于某些特定的内容。

![activity_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223202334295.png)

API注释

想要了解如何在代码中定义活动，请参考[UI Activity Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIActivity_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40011974).想要了解如何将活动视图控制器整合到你的应用中，请参考[Activity View Controller](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/ContentViews.html#//apple_ref/doc/uid/TP40006556-CH13-SW121).

动作与分享扩展程序也可以在活动视图控制器中展示。想要了解更多关于这些扩展程序的内容，请参考[Share and Action Extensions](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/AppExtensions.html#//apple_ref/doc/uid/TP40006556-CH67-SW3).

活动是：

- 一种可定制对象，代表着某个可以让用户在app中执行操作的服务
- 以图标的形式呈现，外观与栏按钮图标相似

[![activity_view_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223202412418.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223202412418.png)

用户通过点击活动的图标来启动某样活动。点击之后该项服务通常会立刻执行，当这项服务过于复杂时，系统将会进一步索取更多的信息之后才会为用户执行该服务。

使用活动来让用户执行你的应用所提供的服务。请注意，iOS本身提供了若干内置的服务，如打印，转发到Twitter，发送信息和Airplay等等，你不需要再额外为这些内置任务创建活动。

为你应用的各种服务设计一套精简的线性模板图标(Template image)。后台会将会把这种模板图标作为剪影遮罩，组合成用户最终看到的图标效果。想设计出好看的模版图标，可以遵循以下原则：

- 使用透明度适当的黑色或白色
- 不要使用阴影
- 进行抗锯齿处理

一个活动模版图大小应该保持在70×70像素左右(高分辨率下)，在区域里居中显示。

**为每一个活动设计清晰简练的文字标题。**标题将会出现在活动菜单图标的下方。一般来说短标题效果最好，因为它在屏幕上的显示效果更好并且更容易本地化。如果你的标题文字过长，iOS会将缩小文本，仍然过长的话则会被截断。一般而言，最好能避免在活动标题中提及你的公司或产品名称。

### 4.2.2 活动视图控制器

活动视图控制器是一个临时视图，当中罗列了一系列可以针对页面特定内容的系统服务和定制服务。

[![activity_view_controller_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223202540438.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223202540438.png)

API注释

想要了解如何在代码中定义活动视图控制器，请参考[UIActivityView Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIActivityViewController_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40011976).想要了解如何设计一个提供自定义服务的活动菜单，请参阅上文中关于活动彩蛋的内容。

活动视图控制器：

- 显示了让用户可以针对当前内容执行操作的一系列的可配置服务
- 根据所处的场景不同，可能出现在操作列表或浮出层中

使用活动视图控制器来为用户提供一系列针对当前内容的服务。这些服务可以是系统自带的，比如复制，分享到twitter，打印等等，也可以是自定义的。活动视图控制器通常用作让用户把他们选中的内容复制到他们的社交媒体账户上。

**不要创建一个自定义按钮来触发活动视图控制器。**用户更习惯点击动作按钮后使用系统提供的服务。你应该学会如何更好地利用用户这一既定习惯，而不是强迫他们以一种全新的方式来完成同样的事情。

**确保控制器中的操作适用于当前场景。**你可以适当地在活动视图控制器中增减系统操作，或增加自定义操作。例如，如果你不希望用户打印某张图片，你可以把打印功能从控制器中删除。

注意

你不能改变系统默认服务在控制器中的顺序。同时，所有系统服务都应该出现在自定义服务之前。

### 4.2.3 集合视图

集合视图用于管理一系列有序的项，并以一种自定义的布局来呈现它们。

[![collection_view_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223202617437.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223202617437.png)

API注释

想要了解如何在代码中定义集合视图，请参考[Collection View Programming Guide for iOS](https://developer.apple.com/library/ios/documentation/WindowsViews/Conceptual/CollectionViewPGforIOS/Introduction/Introduction.html#//apple_ref/doc/uid/TP40012334).

集合视图：

- 可包含装饰视图，以从视觉上区分项的子集或者提供装饰性项目，例如自定义背景。
- 布局切换时支持自定义转场动画。（默认情况下，当用户导入、移动或者删除项的时候，会出现系统默认的动画效果。）
- 支持开发者额外定义手势识别来执行自定义操作。默认情况下，集合视图可以识别轻击(tap)某项以选中，和长按(touch-and-hold)某项进行编辑。

使用集合视图来让用户查看和操作一系列不适合以列表形式呈现的项。由于集合视图的布局不是一个严格的线性布局，因此尤其适合用来展示一些尺寸不一致的项。

集合视图支持广泛的自定义，因此我们要尽量避免把心思都放在进行全新的设计上。集合视图是用来帮助用户更好地完成任务的，视图本身并不是用户体验的焦点所在。以下指南可以帮助你设计出用户体验更好的集合视图：

**表格视图(table view)更适用的时候，不要使用集合视图。**有时候用户会觉得以列表呈现的信息更容易阅读和理解，例如将文本信息放在滚动列表中的时候，用户阅读和处理起来会更为简单和高效。

**让视图中的项更容易选中。**如果用户很难点中集合视图中的项，他们是不会愿意用你的应用的。跟所有用户可以点击的UI对象一样，请确保你的集合视图中每一个项的最小点击区域有44×44pt，尤其是在iPhone上。

**当你要让整个布局进行动态变化时，请务必谨慎。**集合视图允许你在用户浏览和操作项的时候调整视图的布局。但当你决定调整它的时候，请确保这个动态变化是有意义且容易跟踪的。没有明确目的而贸然改变集合视图的布局会让用户对应用留下难用、不符合预期等负面的印象。更有甚者，如果用户此时关注的项在变化中消失了，用户会觉得这个应用超出了他们的控制能力。

### 4.2.4 容器视图控制器

容器视图控制器采用自定义的方式来管理和呈现它的视图控制器或一系列子视图。系统定义的容器视图控制器典型例子包括标签栏视图控制器(Tab bar view controller)、导航视图控制器(navigation view controller)和对分视图控制器(split view controller)。

API注释

想要了解如何在代码中定义容器视图控制器，请参考[UIViewController Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIViewController_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40006926).

容器视图控制器不存在任何预先定义好的外观或者行为。

用容器视图控制器来呈现内容，使用户可以通过控制器来以自定义的方式进行导航。

**先问问你自己是不是必须用到容器视图控制器。**用户会更习惯诸如对分视图、或者是标签栏视图这类他们所熟知的东西。你必须确保你设计的控制器的优点不会由于用户不熟悉、不认识、不会用而白费功夫。

**确保你的容器内容控制器在横屏与竖屏模式都可用。**很重要的一点是，你的容器视图控制器无论在横屏还是竖屏中，体验都应该是一致的。

**一般来说，避免太过花哨的转场动画。**如果你采用了故事板(storyboard)的设计方法来设计你的视图控制器，你往往自然而然地会为它自定义一些动画。但绝大多数情况下，这些花哨的转场动画会让用户分心，让他们忘记了当前要做的事，还可能降低你的应用整体的美感。

### 4.2.5 图片视图

图片视图用以展示一张单独的图片，或者一系列动态图片。

API注释

想要了解如何在代码中定义图片视图，请参考[UIImageView](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIImageView_Class/index.html#//apple_ref/occ/cl/UIImageView).

图片视图：

- 不存在任何预先定义好的外观，同时在默认状态下它不支持用户的交互行为。
- 可以检测图片本身及其父视图(parent view)的属性，并决定这个图片是否应该被拉伸、缩放、调整到适合屏幕的大小，或者固定在一个特定的位置。

在iOS 7及以上版本里，包含了模版图片(template image)的图片视图会把当前的色调(tint color)应用到图片上。

请务必确保图片视图中的每一张图片都保持相同的尺寸和比例。如果你的图片尺寸各不相同，图片视图将会逐一对它们进行调整；而当你的图片比例不一，渲染的时候很可能会出错。

### 4.2.6 地图视图

地图视图呈现地理数据，同时支持系统内置地图应用的大部分功能（如下图所示）。

[![map_view_photos_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223202704558.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223202704558.png)

API注释

想要了解如何在代码中定义图片视图，请参考[*MapKit Framework Reference*](https://developer.apple.com/library/ios/documentation/MapKit/Reference/MapKit_Framework_Reference/index.html#//apple_ref/doc/uid/TP40008210).

地图视图：

- 通常以标准地图、卫星图像、或两者结合的形式来展示地理区域
- 可以展示以单点标注的备注，以及叠加图层（绘制路径或二维区域绘制轮廓的）
- 支持编程时定义的，或用户所控制的缩放和移动

利用地图视图可以给用户提供一个可交互的地理区域视图。如果你在开发一个导航类应用(routing app)，可以使用地图视图来展示你给用户的路径。

**一般来说，允许用户在视图中进行交互行为。**用户习惯了在系统内置地图中进行交互，因此他们会有预期，能在你所提供的地图中进行类似的行为。

**使用标准的地图标注颜色。**地图上标注了一系列地点。因为用户习惯了内置地图的各个标注的颜色，所以最好避免在你的应用中重新定义这些颜色的含义。定义颜色时，请遵循以下这些标准：

- 红色表示目的地
- 绿色表示起点
- 紫色表示用户指定的地点(User-Specified Point)

### 4.2.7 页面视图控制器

页面视图控制器通过滚动(Scrolling)或翻页 (Page-curl transition style)两种方式来处理长度超过一页的内容。下图是iOS模拟器中的翻页样式：

[![page_view_controller_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223202743501.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223202743501.png)

API注释

想要了解如何在代码中定义图片视图，请参考[Page View Controllers](https://developer.apple.com/library/ios/documentation/WindowsViews/Conceptual/ViewControllerCatalog/Chapters/PageViewControllers.html#//apple_ref/doc/uid/TP40011313-CH4).

页面视图控制器：

- 带滚动条的页面视图控制器没有默认的外观。

带翻页效果的控制器可以在两页中间增加书脊(book spine)的效果

- 可以根据指定的转场来模拟出页面切换时的动画。

使用滚动条效果的时候，当前页面将滚动到下一页；而使用翻页效果时，页面上会出现一个模拟实体书或笔记本翻页效果的翻页动画

使用页面视图控制器来展示那些线性的内容（比如一个故事的文本），或者是一些可以被自然地拆分成块的内容（比如日历）。

**如果需要的话，设计一种自定义的方式让用户可以以非线性的方式来获取内容。**页面视图控制器让用户从一页移动到前一页或者后一页，而并不支持用户在并不相邻的页面间快速切换。如果你希望在页面视图控制器中展示一些非线性的内容——比如说字典，或者书籍的目录——那么你就需要自定义一种方式，让用户可以随意地到达不同的内容区块。

### 4.2.8 浮出层

浮出层是当用户轻点某个控件或页面中的某一区域时浮出的，半透明的临时视图。

[![popover_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223202805723-540x1136.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223202805723.png)

API注释

在iOS 8以及以上版本里，你可以使用[UIPopoverPresentationController](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIPopoverPresentationController_class/index.html#//apple_ref/occ/cl/UIPopoverPresentationController)来展示一个浮出层。UIPopoverPresentationController定义了一种委托，让你可以调整浮出层的内容样式，让它能够更好地适应当前的屏幕内容。举个例子，在横屏视图中，你的内容可能会全部承载在浮出层内部；而在竖屏的情况下，浮出层可以以一种全屏模态视图的样式出现。

浮出层：

- 是一个自包含的模态视图
- 在横屏环境中，浮出层会包含一个箭头，指向其出处
- 背景是半透明的，并且会模糊其背后的内容（毛玻璃效果）
- 可以包含多种对象和视图，比如：
- 表格，图片，地图，文本，网页或者自定义视图
- 导航栏，工具栏，和标签栏
- 可以操作当前app视图中的对象的各种控件或对象

（默认情况下， 浮出层中的表格视图，导航栏和工具栏的背景都是透明的，这样会让浮出层的毛玻璃效果展示出来）

在横屏的情况下，动作列表总是出现在浮出层里。

使用浮出层来展示与当前焦点或被选中对象相关的额外信息，或者相关的一系列项。

重要

这一个部分的指引仅适用于在横屏情况下的UI与用户体验。如果你想在竖屏环境中展示全屏的浮出层，请参阅下文中的模态视图相关内容。

避免提供“取消浮出层”按钮。浮出层应当在它不需要的时候自动关闭。如果要决定什么时候不再需要浮出层，请考虑如下场景：

| 如果一个浮出层…                | 那就这样做…                                   |
| ----------------------- | ---------------------------------------- |
| 提供了可以影响主视图的选项，但又不是一个检查器 | 在用户完成选择，或者点击浮层外任何区域（包括唤起浮出层的控件本身），就关闭浮出层 |
| 作为检查器使用                 | 在用户点击浮出层外任何区域（包括唤起浮出层的控件本身），就关闭浮出层。在这个场景下，不要在用户做出选择后马上关闭浮出层，因为用户有可能要做出额外的选择，又或者改变当前选项的属性。 |
| 开启一个任务                  | 当用户通过点击“完成”或“取消”按钮来表示自己完成了或者取消了某个任务的时候，关闭浮出层。在这个场景下，最好不要在用户点击浮出层外的区域就关闭这个浮出层，因为这个时候让用户完成或者彻底放弃这个任务可能更为重要。一定要如此的话，在用户点击浮出层外面的区域的时候保存用户输入的内容，就像你会在他们点击“完成”的时候做的那样。 |

**一般来说，在用户点击浮出层以外的区域的时候，保存用户输入的内容。**不是每一个浮出层都会让用户明确地确认取消操作，因此用户可能会误操作。只有当用户点击“取消”按钮时，才清空他们在浮出层中输入的内容。

**让浮出层中的箭头尽可能直接地指向其出处。**这样有助于用户这个浮出层是从哪里来的，以及他们与哪些任务和对象相关。

**确保用户在看不到浮出层背后的内容的时候仍然能顺利使用浮出层。**浮出层会模糊背后的内容而且用户不能把它拖拽到其它位置。

确保同一时间内屏幕上只有一个浮出层。你不应该同时展示超过一个浮出层（或者外观和行为跟浮出层很相似的模态视图）。尤其应当避免同时展示一连串或者一系列浮出层，从一个浮出层中弹出另一个浮出层。

**不要在浮出层上面再展示一个模态视图。**除了告警框(alert)外，浮出层中不应当有任何模态视图。

**可能的话，让用户可以仅点击一下就关闭当前浮出层并开启一个新的浮出层。**这在若干栏按钮每个都会唤起一个浮出层的时候尤其好用，因为它减少了用户的额外点击。

不要把浮出层设计得太大。浮出层不应当占据整个屏幕。相反，它的大小应当恰好能承载当中的内容，又能清楚地指向浮出层的唤起出处。浮出层的高度是不固定的，因此你可以用它来承载一个很长的项目列表。但一般来说，还是应当避免需要滚动浮出层才能开启一个任务。请注意，系统可能会调整浮出层的宽高，以让它能够更好地适应屏幕的尺寸。

**在浮出层中使用标准的UI控件和视图。**一般来说，包含标准控件和视图的浮出层看上去最理想，而且更容易让用户理解。

**确保自定义浮出层仍然长得像一个浮出层。**尽管使用[UIPopoverBackgroundView](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIPopoverBackgroundView_class/index.html#//apple_ref/occ/cl/UIPopoverBackgroundView) API能够很容易自定义浮出层的多种外观属性，还是应当避免设计出一个用户可能无法辨识的浮出层外观。如果你对浮出层的改动过大，用户就不能凭借之前的经验来理解如何用你的app里的浮出层了。

**当浮出层可见的时候，想要改变它的尺寸的话请务必谨慎。**当你要在浮出层里展示同样信息的精简或拓展视图时，你可能需要改变浮出层的大小。当你一定要这么做的时候，使用转场动画往往是个好主意，因为这不会让人觉得一个新的弹出窗口取代了原来的窗口。

### 4.2.9 滚动视图(Scroll View)

滚动视图方便用户浏览尺寸超越滚动视图边界的图片（下图中地球的图片无论是长度还是宽度都超过了）。

[![scroll_view_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223202845873.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223202845873.png)

API注释

想要了解如何在代码里定义滚动视图，请参考[UIScrollView](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIScrollView_Class/index.html#//apple_ref/occ/cl/UIScrollView).

滚动视图：

- 没有预定义的外观
- 在刚出现或者当用户对它进行操作的时候会短暂地闪烁
- 响应速度和对各个操作手势的识别都应当让用户感到自然。当用户在视图中拖拽内容，内容随之滚动；当用户轻扫屏幕时，内容将快速滚动——直到用户再次触摸屏幕或内容已经到达底部时停止。
- 可以应用在页模式(paging mode)中，在此模式下用户可以通过拖拽和轻击等手势来浏览一页的内容

使用滚动视图来允许用户在固定的空间内浏览大尺寸或大量的视图。

**适当地支持缩放操作。**如果放大和缩小对于当前内容是有用的话，你可以支持用户通过捏或者双击来对当前视图进行缩放。而若是支持了缩放操作的话，你还应当根据用户当前的任务来设定在当前情景下允许缩放的最大值和最小值。如果你允许一个字符被放大到充满整个屏幕的话，用户会很难阅读当前内容。

**在页模式滚动视图中，可以考虑使用页面控件(page control)。**当你想要展示分页、分屏或者分块的内容，可以使用页面控件来让用户知道当前内容一共有多少块，以及他们当前浏览的是第几个。

当你在滚动视图中使用页面控件的时候，最好禁用同一方向的滚动指示器(scroll indicator)。这样一来可以让用户聚焦到页码控件上，并让他们有了一种唯一且清晰的方式来浏览当前内容。想要了解更多，请参考下文控件中的页面控件部分内容。

**一般来说，一次只展示一个滚动视图。**由于用户滚动屏幕时动作幅度经常都会很大，如果在一屏中同时存在不止一个滚动视图，他们很容易会碰到另一个。如果你确实要在同屏中放两个滚动视图，可以考虑给他们设定不同的滚动方向，来避免用户想要滚动一个视图的时候误操作。比如iPhone上的股票应用，纵向滚动上半部分会展示股票报价，横向滚动下半部分时则展示该公司的特定信息。

### 4.2.10 分栏视图控制器

分栏视图控制器是一个用于管理两个相邻视图控制器显示的全屏视图控制器。

[![split_view_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223202906606-590x431.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223202906606.png)

API注释

每一个对分视图控制器的子视图负责管理一个窗格的展现。对分视图控制器本身负责展示这些子视图控制器与管理不同屏幕方向下对分视图的转场效果。想要了解更多如何在代码里定义对分视图，请参考[UISplitViewController Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UISplitViewController_class/index.html#//apple_ref/doc/uid/TP40009277)和[SplitControllers](https://developer.apple.com/library/ios/documentation/WindowsViews/Conceptual/ViewControllerCatalog/Chapters/SplitViewControllers.html#//apple_ref/doc/uid/TP40011313-CH7).

在iOS 7及之前的版本里，对分视图控制器仅适用于iPad.

默认情况下，对分视图控制器通过当前的尺寸来管理其子视图。举个例子，对分视图：

- 可以在横屏环境中展示并排展示两个窗格
- 可以让主窗格在详情窗格上方显示，也可以在不需要的时候（尤其是竖屏情况下）隐藏主窗格。

你可以指定特殊的展示环境下对分视图的版式，并且通过请求对分视图控制器聚焦于这个版式，以此改变窗格的排列方式。

对分视图控制器包含广泛的对象和视图，诸如：

- 表格，图像，地图，文本，网络，或自定义视图
- 导航栏，工具栏，或标签栏

注意

即使左侧窗格通常被称为主窗格，右侧窗格被称为详情窗格，但在代码中并没有强制固定这种从属关系。

使用对分视图控制器，在左侧主窗格展示固定的信息，在右侧详情窗格展示相关的详情或从属信息。以这种设计模式，当用户选择类主视图中的某一项，右侧详情窗格应当展示相应与这一项相关的内容。（你应当在代码中实现这个效果。）

**避免创建一个比主窗格更窄的详情窗格。**如果右侧详情窗格比左侧主窗格窄，对分视图控制器将不能占满整个屏幕，产生视觉不平衡的整体效果。

**避免在两侧窗格中都同时展示导航栏。**这样会让用户很难分清这两个窗格的从属关系。

**一般来说，始终显示左侧主窗格中当前选中的项。**尽管右侧窗格中的内容会变化，但它应当始终保持着与当前选中窗格的相关性。这样的体验有助于用户理解左侧窗格项与右侧窗格内容的关系。

**合适的话，给用户提供不止一种获取主窗格的方式。**默认情况下，竖屏方向时只会展示右侧窗格，因此你需要向用户提供一个按钮（通常位于导航栏上）来让用户唤起和隐藏主窗格。对分视图控制器也支持轻扫手势来执行呼出和隐藏的动作。除非你的app有定义轻扫的手势执行其他功能，否则你应当支持用户轻扫以唤起左侧窗格。

### 4.2.11 表格视图

表格视图以一个可滚动的单列多行的形式来展示数据。

[![plain_table_2x](https://isux.tencent.com/wp-content/uploads/2015/12/2015122320293021.png)](https://isux.tencent.com/wp-content/uploads/2015/12/2015122320293021.png)

API注释

想要了解如何在代码中定义表格视图，请参考[Tabel View Programming Guide for the iOS](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/TableView_iPhone/TableViewStyles/TableViewCharacteristics.html#//apple_ref/doc/uid/TP40007451)以及[UITableView](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITableView_Class/index.html#//apple_ref/occ/cl/UITableView).

表格视图：

- 以容易进行分段或分组的单列形式展示数据
- 用户可以通过点击来选中某行，或通过控件来添加、移除、多选、查看详情或者展开另一个表格视图

iOS定义了两种表格样式：

**分组型****（Grouped）。**表格行以分组形式展示，可以有页眉和页脚。分组表格视图中至少含有一组列表，而每一组中至少包含一项内容。与平铺型不同，分组型表格没有索引。

[![simple_list_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223203027650.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223203027650.png)

**平铺型****（Plain）。**平铺型表格可被分为若干带标签的段落，表格右侧可能会出现垂直的表格索引。每行开头可以有页眉，尾部可以有页脚（也可以没有）。

[![grouped_list_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223203102136.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223203102136.png)

在这两种样式中，当用户选中某一行时，该行会短暂地高亮。当选中某行将展开另外一屏内容的时候，该行会短暂地高亮，然后新一屏内容滑入。当用户回到前一屏时，之前选中的那一行同样会短暂地高亮，提醒用户他们先前选中了什么（但并不会一直保持高亮）。
除了以上表格中列举的元素外，iOS定义了刷新控件，让用户可以刷新当前的表格内容。想要了解更多关于刷新控件的用法，可以参考文档本章第三节控件中的刷新控件。iOS提供了若干表格视图元素(table-view elements)来扩展表格视图的功能。除了特别标明外，这些元素只适用于表格视图。

[![table-view](https://isux.tencent.com/wp-content/uploads/2015/12/20151223203252329.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223203252329.png)

iOS定义了在平铺型表格和分组型表格中最常用到的四种单元格布局样式。每种单元格样式都有最适合展示的信息类型。

重要

从编程角度来说，这些样式应用于单元格中，用以控制表格里每一列的绘制方式。

**默认型（Default）**([UITableViewCellStyleDefault](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITableViewCell_Class/Reference/Reference.html#//apple_ref/c/econst/UITableViewCellStyleDefault))。默认型样式包括左侧的图标（可选），和图标右边左对齐的文字标题。

默认型样式适合展示一系列无须通过附加信息便可以区分的项。

[![default_cell_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223203424588.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223203424588.png)

**副标题型（Subtitled）**([UITableViewCellStyleSubtitle](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITableViewCell_Class/Reference/Reference.html#//apple_ref/c/econst/UITableViewCellStyleSubtitle))。副标题型包括左侧图标（可选），图标右边左对齐展示的文字标题，以及在标题下方同样左对齐展示的副标题。

左对齐的文本标签让用户可以更快速地扫视表格。这种样式适用于列表各项较为相似的情况，用户可以通过副标题中的详细信息来区分列表中的各项。 ([UITableViewCellStyleSubtitle](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITableViewCell_Class/Reference/Reference.html#//apple_ref/c/econst/UITableViewCellStyleSubtitle))。副标题型包括左侧图标（可选），图标右边左对齐展示的文字标题，以及在标题下方同样左对齐展示的副标题。

[![subtitle_cell_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223203510493.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223203510493.png)

**Value 1**** **([UITableViewCellStyleValue1](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITableViewCell_Class/Reference/Reference.html#//apple_ref/c/econst/UITableViewCellStyleValue1)).在Value 1样式下，标题左对齐，副标题用较细的字体右对齐。

[![value_1_cell_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223203540811.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223203540811.png)

**Value 2** [(UITableViewCellStyleValue2](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITableViewCell_Class/Reference/Reference.html#//apple_ref/c/econst/UITableViewCellStyleValue2)).Value 2样式蓝色字体标题右对齐，黑色字体的副标题左对齐，混排在同一行中。这种样式通常不包含图片。

Value 2的布局中，文本和副标题中间的垂直间距会让用户专注于副标题的第一个单词。

[![value_2_cell_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223203632816.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223203632816.png)

重要
以上四种单元格样式均支持添加表格视图元素，如勾选或展开标志。添加这些元素会缩小标题以及副标题单元格的可用宽度。

使用表格视图可以简洁而高效地展示少量或者大量信息。举例来说，你可以通过表格视图来：

- **展示用户可选的选项列表。**你可以使用选中标记来告知用户当前选中了哪些项。

无论是平铺型还是分组性，用户点击某一行中的某一项时都可以显示一个选项列表。当用户点选了一个不属于表格行的按钮或者其他UI元素的时候，可以使用平铺型表格视图来展示唤起的选项列表。

- **展示层级信息。**平铺型表格样式非常适合展示层级信息。表格中的每项都指向承载于另一个列表中的不同子信息。用户可以沿着这些层级结构的路径来点击每一层列表中的项。以展开标志告知用户点击这一列中的任何位置，都将展开新的列表以展示其子类信息。
- **展示可以在概念上进行分组的信息。**平铺型和分组型列表都允许你通过提供页眉和页脚来对信息进行分组和分段。

你可以用页眉页脚视图(header-footer view)——即UITableViewHearderFooterView中的一个实例——来展示页眉和页脚的文字，或图片。想要了解如何在代码中定义页眉页脚视图，请参考[*UITableViewHeaderFooterView Class Reference*](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITableViewHeaderFooterView_class/Reference/Reference.html#//apple_ref/doc/uid/TP40012241)*.*

**使用表格视图时，可遵循以下这些指引：**

**用户选择列表项时，始终给与反馈。**当用户点击可选的列表项时会认为被点击的项都应短暂地高亮一下。在点击后，用户期望出现新的视图，或者出现一个复选标记以表明先前点击的项已经被选中或激活。

**如果表格的内容庞大而且复杂，不要在所有数据都加载完之后才一起显示出来。**可以首先展示文本信息，图片等较为复杂的内容则在加载完后再显示。这样可以将有用的信息立即传达给用户，同时也提高了应用的响应能力。

**在等待信息加载的时候，可以考虑展示“过期”信息。**尽管我们并不推荐在数据频繁变化的应用中这样做，它还是可以帮助更多的静态应用程序立即给到用户有用的信息。当然在你这么做之前，请认真衡量你应用中数据的变化频率，并弄清楚你的目标用户有多需要立即获取最新的信息。

**如果信息加载速度很慢或者非常复杂，你需要告诉用户加载正在进行中。**如果表格中所有内容都很复杂，我们很难即时地给用户展示任何内容。在这种极端情况下，切勿显示空白的表格，因为这会让用户以为应用挂了。此时应当在屏幕中央展示一个活动指示器(activity indicator)和一个信息标签(information label)，比如“加载中…”，让用户知道加载仍然在进行。

**如果合适的话，为删除按钮自定义一个名称。**如果这能让用户更好地理解应用的相关功能的话，你可以创建一个合适的标题，来取代“删除”这个字样。

**尽量使用简洁的文字标签，以避免被截断。**繁冗的文字和词组不方便用户浏览和理解。以上所有单元格样式均会自动截断文本，而文本截断所造成的问题可大可小，取决于你采用的单元格样式，以及被截断了哪一部分文字。

**如果你想以一种非标准的形式来布局你的表格，**最好是自定义一种单元格样式，而不是在现有的表格样式上进行改动。如何创建自定义单元格样式，请参考[Table View Programming Guide for iOS](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/TableView_iPhone/AboutTableViewsiPhone/AboutTableViewsiPhone.html#//apple_ref/doc/uid/TP40007451)中的[Customizing Cells](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/TableView_iPhone/TableViewCells/TableViewCells.html#//apple_ref/doc/uid/TP40007451-CH7-SW18)部分。

### 4.2.12 文本视图

文本视图可以接收和展示多行文本。

[![text_view_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223203734108.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223203734108.png)

API注释

想了解如何在代码中定义文本视图，参考[Text Views](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/UIKitUICatalog/UITextView.html#//apple_ref/doc/uid/TP40012857-UITextView).

文本视图：

- 是一个可定义为任何高度的矩形
- 当内容太多超出视图的边框时，文本视图支持滚动
- 支持自定义字体、颜色和对齐方式（默认情况下，文本视图会以左对齐的黑色系统字体显示）
- 可以支持用户编辑，当用户轻击文本视图内部时，将唤起键盘（键盘的布局和类型取决于用户的系统语言设置）

**始终确保文字的易读性。**虽然你可以使用属性字符串将不同的字体、字色和对齐方式串联在同一个文本视图内，但保持文本的可读性是必不可少的。最好是可以支持动态文本(Dynamic Type)和UIFont method preferredFontForTextStyle来展示文本框中的文本。想要了解更多动态文本的指引，可以参阅本文第一章中颜色与字体里的部分；想要了解更多编程相关的内容，可以参阅[Text Styles](https://developer.apple.com/library/ios/documentation/StringsTextFonts/Conceptual/TextAndWebiPhoneOS/CustomTextProcessing/CustomTextProcessing.html#//apple_ref/doc/uid/TP40009542-CH4-SW65).

**根据输入内容的类型来指定不同的键盘类型。**举例来说，你希望用户能更方便地输入网址、密码或者电话号码。但请注意，由于键盘的布局以及输入方法是由用户的系统语言设置决定的，这是你不能控制的。

iOS提供了各种不同的键盘类型，以便用户输入不同类型的文本。想要了解可用键盘类型，可以参考[UIKeyboardType](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITextInputTraits_Protocol/Reference/UITextInputTraits.html#//apple_ref/c/tdef/UIKeyboardType).想要了解如何在管理你的应用中的键盘，请参考[Managing the Keyboard](https://developer.apple.com/library/ios/documentation/StringsTextFonts/Conceptual/TextAndWebiPhoneOS/KeyboardManagement/KeyboardManagement.html#//apple_ref/doc/uid/TP40009542-CH5).

### 4.2.13 网络视图

网络视图是一个可以展示丰富的HTML内容的区域。（下图是iPhone自带的邮件应用，网络视图指的是下图中导航栏和标签栏中间的区域）

[![web_view_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223203851818.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223203851818.png)

API注释

想要了解如何在代码中定义网络视图，请参考[Web Views](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/UIKitUICatalog/UIWebView.html#//apple_ref/doc/uid/TP40012857-UIWebView).

网络视图：

- 展示网络内容
- 会自动处理页面中的内容，比如把页面中的电话号码转化成电话链接（译者按：phone link，点击之后iPhone将自动拨打该号码）。

如果你有一个网页或者网络应用，你大约会用网络视图来实现一个简单的iOS App，来对你的网页或者应用进行一个封装。如果你打算用网络视图来访问你所控制的网页内容，请务必阅读[Safari Web Content Guide](https://developer.apple.com/library/ios/documentation/AppleApplications/Reference/SafariWebContent/Introduction/Introduction.html#//apple_ref/doc/uid/TP40002051).

**不要用网络视图来创建一个看起来像迷你网络浏览器的应用。**用户期望使用iOS自带的Safari来浏览网页内容，因此我们并不推荐你在自己的app里复制这种以被广泛应用的功能。

## 4.3 控件

### 4.3.1 活动指示器

活动指示器表明任务或进程正在进行中，如下图所示。

[![activity_indicator_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223204704476.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223204704476.png)

API注释

想要了解如何在代码中定义活动指示器，可以参考[UIActivityIndicatorView Class Reference.](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIActivityIndicatorView_Class/index.html#//apple_ref/doc/uid/TP40006830)

活动指示器：

- 当任务进行和加载时旋转，任务完成后自动消失
- 不支持用户交互行为

在工具栏或主视图中使用活动指示器来告知用户任务或加载正在进行中，但并不提示该过程何时会结束。

**不要使用静止的活动指示器。**用户会以为该进程停滞了。

**用活动指示器来让用户知道进程仍在进行中。**有些时候，告诉用户进程没有停止比告诉他们何时完成更加重要。

**设计一个与应用的风格协调的活动指示器。**可以的话，让活动指示器的尺寸和颜色与它所在的背景协调。

### 4.3.2 添加联系人按钮

添加联系人按钮让用户将现有联系人添加到文本框或者其它文字视图中。

[![contact_add_7_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223204734458.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223204734458.png)

API注释

想要了解如何在代码中定义添加联系人按钮，请参考[UIButton](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIButton_Class/index.html#//apple_ref/occ/cl/UIButton).

添加联系人按钮：

- 展示联系人列表
- 帮助用户将一个联系人添加到当前联系人按钮所在的视图中

使用添加联系人按钮让用户在不需要使用键盘的情况下就可以方便地访问到联系人。举个例子，在新建邮件的界面中，用户可以点击该按钮来在邮件中添加收件人，而不需要用键盘输入收件人的名字。

由于添加联系人按钮属于键盘输入联系人方法的替代品，我们不推荐在不支持键盘输入的界面中使用添加联系人按钮。

### 4.3.3 日期时间选择器

日期时间选择器展示关于日期和时间的组件，比如小时，分钟，天，以及年。

[![date_picker_2x](https://isux.tencent.com/wp-content/uploads/2015/12/2015122320475388.png)](https://isux.tencent.com/wp-content/uploads/2015/12/2015122320475388.png)

API注释

想要了解如何在代码中定义添加日期时间选择器，请参考UIDatePicker.

日期时间选择器：

- 最多可以展示4个独立的滑轮，每一个滑轮表示一个不同的值，比如月份或小时等
- 在每个滑轮的中央使用深色字体来表示当前选中的值
- 日期时间选择器的大小与iPhone键盘的大小相同，并且不可更改
- 包括四种模式，每一种模式代表了一组不同的值:


- **日期和时间**。日期和时间模式（默认模式）包含日期、小时、和分钟，以及一个可选的AM/PM值。
- **时间**。时间模式包括小时和分钟，以及可选的AM/PM值。
- **日期**。日期模式包括月份，天以及年三个值。
- **倒计时器**。倒计时器模式展示了小时和分钟值。你可以精确地设定总共的倒计时间，倒计时的最大值为23小时59分钟。

使用日期时间选择器来让用户选择时间，而不是让用户自己输入一个包含了日期、时间等多个部分的时间值。

**尽量地让用户在当前内容中使用日期选择器。**尽量地让用户在当前内容中使用日期选择器。最好避免用户在使用日期选择器的时候要进入另外一个界面。在水平方向的常规环境，日期时间选择器可能会出现在一个浮层中，或者嵌入在当前内容里。

**有必要的时候，改变分钟滑轮的单位刻度。**在默认情况下，分钟滑轮包含从0到59共60个值，如果你要展示一个颗粒度较大的时间，你可以让分钟滑轮的单位刻度变大，只要这个刻度可以整除60。比如说你可能会设定每15分钟为一个刻度，此时分钟滑轮就有4个值，0、15、30、45。

### 4.3.4 详情展开按钮

详情展开按钮展示了与该项相关的更多详细信息与功能描述。

[![detail_disclosure_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223204812996.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223204812996.png)

API注释

想要了解如何在代码中定义详情展开按钮，可以参考[UITableViewCell Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITableViewCell_Class/index.html#//apple_ref/doc/uid/TP40006938) 和[UIButton](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/UIKitUICatalog/UIButton.html#//apple_ref/doc/uid/TP40012857-UIButton).

详情展开按钮以一个单独的视图展示特定项目的更多详情信息与功能。

当详情展开按钮在表格行中出现时，点击表格行的其它区域不会激活此按钮，只会选中该行，或者触发app中其它自定义的行为。

一般来说，你会在一个表格视图中使用详情展开按钮来让用户知道更多关于这个列表项的信息。当然你也可以将这个按钮用在其它类型的视图中来为用户展示更多与特定项目相关的信息和功能。

### 4.3.5 信息按钮

信息按钮展示了app的配置信息，有时候它会出现在当前视图的背面。

[![info_button_2x (1)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223204843648.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223204843648.png)

API注释

想要了解如何在代码中定义信息按钮，可以参考[UIButton](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/UIKitUICatalog/UIButton.html#//apple_ref/doc/uid/TP40012857-UIButton).

iOS包含了两种信息按钮样式：适用于浅色内容上的深色按钮，以及适用于深色内容上的浅色按钮。

使用信息按钮来显示app的配置信息或选项。你可以根据自己app的UI风格来选择最为协调的信息按钮样式。

### 4.3.6 标签

标签用于放置静态文本。

[![labels_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223204901147.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223204901147.png)

API注释

想要了解如何在代码中定义标签，可以参考[UILabel Class Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UILabel_Class/index.html#//apple_ref/doc/uid/TP40006797).

标签可以：

- 展示任意数量的静态文本
- 禁止除了复制文本外的任何用户交互行为

你可以使用标签来命名或解释你的部分UI，又或者用它来给用户提供一些简单的信息。标签最适合拿来展示相对简单的文本信息。

**保证你的标签清晰易读。**最好支持动态文本(Dynamic Type)，并使用 [UIFont](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIFont_Class/index.html#//apple_ref/occ/cl/UIFont) 中的preferredFontForTextStyle来获得标签中的展示文本。如果你要用自定义字体的话，请慎重选择字体种类，不要以牺牲清晰度为代价来换取花哨的颜色和字体效果。（想要了解关于app中字体使用的指南，可以参考[ Color and Typography](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/ColorImagesText.html#//apple_ref/doc/uid/TP40006556-CH58-SW1);想要了解更多动态文本的内容，可以参考 [Text Programming Guide for iOS](https://developer.apple.com/library/ios/documentation/StringsTextFonts/Conceptual/TextAndWebiPhoneOS/Introduction/Introduction.html#//apple_ref/doc/uid/TP40009542) 里面 的 [Text Styles](https://developer.apple.com/library/ios/documentation/StringsTextFonts/Conceptual/TextAndWebiPhoneOS/CustomTextProcessing/CustomTextProcessing.html#//apple_ref/doc/uid/TP40009542-CH4-SW65) 部分。）

### 4.3.7 网络活动指示器

网络活动指示器在状态栏中出现，表示网络活动正在进行。

[![network_activity_indicator_7_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223204925531.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223204925531.png)

API注释

你可以在代码中使用 UIApplication的[networkActivityIndicatorVisible](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html#//apple_ref/occ/instm/UIApplication/isNetworkActivityIndicatorVisible) 来控制该活动指示器的可见性。

网络活动指示器：

- 出现在状态栏中，当网络活动正在进行时它会旋转，在活动停止时它则消失
- 不支持用户交互行为

当你的app正在链接网络，而这个连接过程将会持续好几秒的时候，你可以通过网络活动指示器来给用户以反馈。如果进程所需时间很短，则不需要用到它，因为很可能在用户注意到它之前，它就消失了。

### 4.3.8 页面控件

页面控件告诉用户当前共打开了多少个视图，还有他们正处在其中哪一个。

[![page_control_weather_2x](https://isux.tencent.com/wp-content/uploads/2015/12/2015122320494522.png)](https://isux.tencent.com/wp-content/uploads/2015/12/2015122320494522.png)

API注释

想要了解如何在代码中定义页面控件，可以参考[UIPageControls](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIPageControl_Class/index.html#//apple_ref/occ/cl/UIPageControl).

页面控件：

- 包含一系列圆点，圆点的个数代表了当前打开的视图数量（从左到右，这些圆点代表了视图打开的先后顺序）
- 默认情况下，使用不透明点来标识当前打开的视图，使用半透明点来表示所有其它视图
- 不支持用户访问不连续的视图
- 当视图数量超过页面宽度可承载的氛围时，点的大小和间距并不会因此变小（如果需要显示的点超过一定数量，系统会把它截断）
- 默认情况下不支持视图之间导航；你必须实现视图到视图之间的导航并适当地更新页面控件状态

当告知用户有多少打开的视图的需求比帮助用户选择特定的视图更重要时，使用页面控件。页面控件是为所有视图均平等的场景而设计的。

**不要使用页面控件来显示视图中的层次结构或其他复杂的排列。**页面控件不显示视图是如何相互关联的，而且不表明哪个视图对应于每个点，因此它不能帮助用户导航到特定的视图。

**避免显示太多点。**超过10个点就很难让用户一目了然，而超过20个视图在序列中访问起来非常耗时。如果用户可以在你的应用程序打开超过20个视图，请考虑给视图一个不同的展示方式，以提供关于视图的详细信息，使其支持不连续的导航。

**在打开视图的底部边缘和屏幕的底部边缘里垂直居中页面控件。**在这个位置，页面控件是始终可见的，并且不会阻挡用户的使用。

### 4.3.9 选择器

选择器展示了一组值，用户可以从中选择一个。

[![picker_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205002329.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205002329.png)

API注释

想要了解如何在代码中定义选择器，可以参考[UIPickerView Class Reference.](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIPickerView_Class/Reference/UIPickerView.html#//apple_ref/doc/uid/TP40006842)

选择器：

- 是日期时间选择器的通用模式
- 包括一个或多个滑轮，每个滑轮含有一组值
- 当前选中的值在中间，以深色标识
- 不可以自定义大小（选择器的大小与iPhone的键盘相同）

使用选择器可以让用户更容易从一系列不同的值中间进行选择。

**一般来说，当用户对整组值都比较熟悉的时候，可以使用选择器。**由于当滑轮静止的时候，大部分的数值会被隐藏，最好是在用户对所有数值均有预期的情况下才使用选择器。当你需要展示一大组用户并不熟悉的选项，此种选择器可能不太适合。

**尽可能让让用户在当前视图中使用选择器。**不要让他们在使用选择器时还要进入其它的视图。

**如果你需要展示的备选项数量很多，考虑使用表格视图(Table View)而不是选择器。**因为表格视图的高度较大，内容滚动起来会更快。

### 4.3.10 进度视图

进度视图展示了任务或进程的进度（下图是iOS默认邮件App的工具栏）。

[![progress_view_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205025696.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205025696.png)

API提示：

想要了解更多如何在代码中定义进度视图，可以参考[UIProgressView Class Reference.](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIProgressView_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40006782)

进度视图：

- 是一条轨迹，随着进程的进行从左向右进行填充
- 不支持用户交互行为

iOS定义了两种进度视图样式：

- **默认(Default)**.默认样式适合用在app的主要内容区中。

[![progress_view_default_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205044700.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205044700.png)

- **进度条(Bar).**此样式比默认样式细，适合用在工具栏中。

[![progress_view_bar_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205058427.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205058427.png)

当一个任务存在明确的进程，可以使用进度条来给与用户反馈，尤其在需要明确告诉用户这个任务大约需要多少时间完成的时候。

**可以的话，请根据你的app的风格来设计进度条的外观。**你可以自定义进度条的底色以及轨迹颜色，也可以直接使用图片。

### 4.3.11 刷新控件

刷新控件执行用户触发的内容刷新——一个典型的例子，它常在表格中出现（下图展示的是iOS默认的邮件app的mailbox列表页）。

[![refresh_control_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205111688.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205111688.png)

API提示：

想要了解更多如何在代码中定义刷新控件，可以参考[ UIRefreshControl Class Reference.](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIRefreshControl_class/Reference/Reference.html#//apple_ref/doc/uid/TP40012250)

刷新控件：

- 看起来类似活动指示器
- 可以出现在标题中
- 默认状态下不可见，当用户在表格上缘往下拖拽以刷新内容时才出现

使用刷新控件，给用户提供一个一致的方式来了解一个表格或其他视图的内容更新，而不需要等待下一个自动更新。

**就算你使用了刷新控件，也不要因此就不支持内容自动刷新。**尽管用户喜欢在执行刷新操作时内容立刻刷新，他们也同样会喜欢内容自动刷新。如果过于一来用户自己执行所有刷新操作的话，那些不会自动刷新的用户就会疑惑，为何你app中的数据永远都不更新。一般来说，刷新控件给了用户多一个选择，让他们可以立刻获得最新的内容，但同时，你也不能奢望用户会主动获取所有的更新信息。

**只有在必要的时候才加短标题。**特别需要注意的是，不要使用短标题来描述刷新控件怎么使用。

### 4.3.12圆角矩形按钮

iOS7及更新版本中已经不再使用圆角矩形按钮，而是使用了新的系统按钮——类型为UIButtonTypeSystem的UI按钮[ (UIButton)](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIButton_Class/UIButton/UIButton.html#//apple_ref/occ/cl/UIButton) 。使用指南可参考[System Button](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/mobilehig/Controls.html#//apple_ref/doc/uid/TP40006556-CH15-SW10).

### 4.3.13 分段控件

分段控件是一组分段的线性集合，每一个分段的作用类似按钮，点击之后将切换到相应的视图。

[![segmented_control_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205147522.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205147522.png)

API提示：

想要了解更多如何在代码中定义分段控件，可以参考[ Segmented Controls](https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/UIKitUICatalog/UISegmentedControl.html#//apple_ref/doc/uid/TP40012857-UISegmentedControl)

分段控件：

- 由两个或以上的分段组成，每一个分段的宽度相同，与分段的数量成比例（分段数量越多，则宽度越小）
- 可以包含文字或者图片

使用分段控件来提供密切相关而又互斥的选项。

**保证每个分段都容易点击。**为了保证每个分段的大小有至少44×44像素，请控制分段的数量。在iPhone上，1个分段控件最多包含5个分段。

**尽可能地保持每个分段中的文字长度一致。**因为每个分段都是等宽的，当文本长度差异很大时看上去会很不协调。

**不要在同一个分段控件中混用文字和图片。**每一个分段都仅可支持纯文字或纯图片。避免在同一个分段控件中，一些分段里使用纯文字，另一些分段里使用纯图。

**请在必要时调整分段控件中文本的对齐方式。**如果你给分段控件添加了自定义底图，请确保控件里自动居中的文本依然清晰美观。你可以通过bar metrics APIs 来调整分段控件内文本的对齐方式(想要了解如何定义bar metrics，可以参考[ UISegmentedControl](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UISegmentedControl_Class/index.html#//apple_ref/occ/cl/UISegmentedControl) 中关于自定义API外观(appearance-customization APIs)的描述)。

### 4.3.14 滑块

滑块允许用户在一个限定范围内调整某个数值或进程(下图展示的是iOS设置中亮度设置的滑块，滑块的左边和右边均为自定义图形)。

[![slider_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205204981.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205204981.png)

API提示：

想要了解更多如何在代码中定义滑块，可以参考[ Sliders](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/UIKitUICatalog/UISlider.html#//apple_ref/doc/uid/TP40012857-UISlider)

滑块：

- 由一条水平的轨迹和一个Thumb(滑块中支持用户水平拖拽的圆形控件)组成
- 左边和右边支持使用自定义图片来表述相对的最小值与最大值的含义
- 填充轨道左边缘最小值之间到Thumb之间的部分

使用滑块来让用户精准地选择自己想要的值，或者控制当前的进程。

**如果合适的话，自定义滑块的外观。**比如，你可以:

- 定义Thumb的外观，让用户一看就知道滑块当前的状态
- 在轨迹的左右两端使用自定义图片来告诉用户滑块的最小值和最大值所代表的含义。比如说，一个图调整图片尺寸的滑块可以在最小值的左边放一张小图，在最大值的右边放一张大图。
- 根据Thumb所在的位置和当前滑块的状态来为滑块的轨迹定义不同的颜色

**不要使用滑块来显示音量控制。**如果你需要显示一个音量滑块，当你使用[MPVolumeView](https://developer.apple.com/library/ios/documentation/MediaPlayer/Reference/MPVolumeView_Class/index.html#//apple_ref/occ/cl/MPVolumeView)类的时候请使用系统提供的音量滑块。请注意，当当前活动的音频输出设备不支持音量控制时，音量滑块以适当的设备名称替换。

### 4.3.15 步进器

步进器可以以常数为幅度来增减当前数值。

[![stepper_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205222465.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205222465.png)

API提示：

想要了解更多如何在代码中定义步进器，可以参考[UIStepper](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/UIKitUICatalog/UIStepper.html#//apple_ref/doc/uid/TP40012857-UIStepper).

步进器：

- 是一个两段控件，其中一段默认显示减号，另一端默认显示加号
- 支持自定义图片
- 不展示用户更改的值

当用户想要对数值进行小幅度调整时，可以使用步进器。

**当用户需要大幅度调整数值的时候，不要使用步进器。**用户可能会在打印机里使用步进器来确定打印份数，因为这个值的变化幅度通常并不大；而当用户需要选择打印的页码范围时，使用步进器就会让操作变得繁琐，因为用户很可能要点很多下才能选定页数。

**确保步进器所调整的值明显可见。**步进器自身不展示任何数值，所以你需要保证让用户知道他们正在调整哪一个数值。

### 4.3.16 开关按钮

开关按钮展示了两个互斥的选项或状态。

[![switch](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205443419.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205443419.png)

API提示：

想要了解更多如何在代码中定义步开关，可以参考[UISwitch](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/UIKitUICatalog/UISwitch.html#//apple_ref/doc/uid/TP40012857-UISwitch).

开关按钮：

- 显示了一个项存在二元状态
- 仅在表格视图中可用

在表格中使用开关按钮来让用户从某一项的两个互斥状态中指定一个，比如是/否(Yes/No)，开/关(On/Off)。

你可以使用开关按钮来控制视图中的其它UI元素。根据用户的选择，新的列表项可能出现或者消失，或从激活状态变为不激活状态。

### 4.3.17 系统按钮

系统按钮执行app中定义的行为。

[![system_button_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205503758.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205503758.png)

API提示：

在iOS 7中，UIButtonTypeRoundedRect已经被重新定义为 UIButtonTypeSystem. 想要了解更多如何在代码中定义系统按钮，可以参考 UIButton.

系统按钮：

- 默认状态下不含边界，也不含背景图
- 可以是图标或者文字标题
- 支持自定义样式，如描边或者加背景图(想要自定义按钮外观，可以使用 UIButtonTypeCustom 类型的按钮，并且提供背景图片)

使用系统按钮来执行某个动作。当你为系统按钮命名时，请遵循以下方法：

- **使用动词或动词短语来描述按钮所代表的动作**。这种命名方法告诉用户这个按钮是可交互的，也提示了用户点击之后会执行什么操作
- **使用标题式大写**(title-style capitalization，每个单词的首字母均大写)。除了冠词，并列连词以及少于4个字母的介词外，标题中每个单词的首字母均大写。
- **标题不要太长**。太长的标题会被截断，让用户难以理解其含义

以iPhone为例，给数字按键添加圆形边框强化了用户拨电话号码时的心理模型，而结束(End)和隐藏(Hide)按钮的背景色让用户拥有了更大的点击范围。

**合适的话，为内容区域内的系统按钮描边或者加入背景。**大多数情况下，你可以通过定义一个清晰的按钮名称、选择一个不一样的标题颜色或提供上下文情景提示来让用户知道这是一个按钮而非普通文本。但在某些特定的内容区域内，为按钮描边或者添加背景颜色，让用户迅速地把注意力放到按钮上，也是必要的。Value 2的布局中，文本和副标题中间的垂直间距会让用户专注于副标题的第一个单词。

[![phone_bordered_buttons_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205539398.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205539398.png)

### 4.3.18文本框

开关按钮展示了两个互斥的选项或状态。

[![text_field_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205601424.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205601424.png)

API提示：

想要了解如何在代码中定义文本框，以及在文本框中支持图片和按钮，可以参考[ UITextField.](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITextField_Class/index.html#//apple_ref/occ/cl/UITextField)

文本框

- 高度固定，包含圆角
- 当用户点击它时，自动唤起输入键盘
- 可以包含系统提供的按钮，如书签按钮(Bookmarks)
- 可以展示多种文字样式(了解更多请参考 [UITextView](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITextView_Class/Reference/UITextView.html#//apple_ref/occ/cl/UITextView))

使用文本框来获取用户输入的少量信息。

**你可以自定义一个文本框，帮助用户更好地理解如何使用它。**举个例子，你可以在文本框的左侧或者右侧加入自定义图形，或者加入系统按钮，如书签按钮等。一般来说，文本框的左侧用于表述文本框的含义，而右侧用于展示附加的功能，如书签。

**合适的话，在文本框右侧加入清除按钮。**轻击清除按钮变可清空当前框内输入的全部内容，无论你原本打算在这个按钮上面展示什么其它图片。

**如果可以帮助用户理解的话，可以在文本框中加入提示文字。**当文本框里没有任何其它提示文字时，会展示占位符文本(placeholder text)，如名字、地址等。

**根据输入内容的类型来指定不同的键盘类型。**举例来说，你希望用户能更方便地输入网址、密码或者电话号码。iOS提供了各种不同的键盘类型，以便用户输入不同类型的文本。想要了解可用键盘类型，可以参考 [UITextInputTraits Protocol Reference](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITextInputTraits_Protocol/index.html#//apple_ref/c/tdef/UIKeyboardType)中的[UIKeyboardType](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITextInputTraits_Protocol/index.html#//apple_ref/c/tdef/UIKeyboardType).想要了解如何在管理你的应用中的键盘，请参考[Managing the Keyboard](https://developer.apple.com/library/ios/documentation/StringsTextFonts/Conceptual/TextAndWebiPhoneOS/KeyboardManagement/KeyboardManagement.html#//apple_ref/doc/uid/TP40009542-CH5)部分。但请注意，由于键盘的布局以及输入方法是由用户的系统语言设置决定的，这是你不能控制的。

## 

## 4.4临时视图

### 4.4.1 警告框

警告框用于告知用户一些会影响到他们使用app或设备的重要信息。

[![alert_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205624887.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205624887.png)

API提示：

如需在代码中使用警告框，你可以创建[UIAlertController](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIAlertController_class/index.html#//apple_ref/occ/cl/UIAlertController)并且指定[UIAlertControllerStyleAlert](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIAlertController_class/index.html#//apple_ref/c/econst/UIAlertControllerStyleAlert).

警告框：

- 必须包含标题，有时候会包含正文文本
- 包含一个或多个按钮

一般来说，警告框警告出现的频率较低，也正因为如此，警告的出现通常会让用户额外重视。请严格控制你的app中警告的个数，并且保证每一个警告都能提供重要的信息，或者有用的选项。

**避免出现不必要的警告框。**一般来说，在以下情景中，是不需要用到警告框的：

[![alert-text](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205743472.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205743472.png)

当你在设计警告文案的时候，了解以下这些定义非常有用：

- **标题式大写(Title-style capitalization)**指的是除了冠词，并列连词以及少于4个字母且不处在第一个单词位置上的介词外，标题中每个单词的首字母均大写。
- **句子式大写(Sentence-style capitalization)**指的是第一个字母大写，其余除了专有名词和专有形容词外的字母均小写

**简明扼要地描述当前情景，并告诉用户他们可以做什么。**理想情况下，警告框中的文字应该给与用户足够的情景和上下文联想，让他们可以清楚地知道为什么警告会出现，同时帮助他们判断自己应该点哪个按钮。

**保证标题足够简短，最好在一行之内。**过长的标题让用户很难快速理解它的意思，还可能会被截断。

[![alert_title_only_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205811877.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205811877.png)

**避免单个字的标题。**单字标题，例如：错误，或警告，几乎不能提供任何有用信息。

**如果可以的话，使用句子片段而非完整的句子。**一个简洁清晰的状态描述往往比一个完整的句子更容易理解。

**尽可能的精炼你的标题文字，让警告框即使没有下面的正文信息也能完全让用户理解。**举个例子，当你使用一个问题，或者两个短句来作为警告框标题的话，很可能你并不需要添加文本信息。

**不用刻意避免在警告框中使用消极负面的文案。**用户们理解大多数警告框是为了告诉他们发生的问题，或者对他们目前的状态作出警告。因此消极但清晰直接的文案优于积极但晦涩间接的文案。

**尽可能地避免使用“你”，“你的”，“我”，“我的”这类字眼**。有时候，这些直接指向的字眼容易引起歧义，有时候甚至会被误认为是一种冒犯。
适当地使用大写和标点符号，尤其是在以下这些场景中：

[![capital-case](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205936258.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223205936258.png)

**如果你必须为警告框添加正文文本，请使用一个完整的短句。**可能的话，尽量保证句子在1到2行之间。如果句子太长，用户会需要滚动才能看完，这样的体验很糟。使用句子式大写，并在句末加上适当的标点符号。

[![alert_title_with_msg_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223210002513.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223210002513.png)

**避免在文本中详细描述“该按哪个按钮”而导致文本过长。**理想情况下，表意明确的警告文案和逻辑清晰的按钮文案已经足以让用户正确判断自己该按哪个按钮了。但如果你一定要在文案中描述这些内容，请遵循以下原则：

- 确定使用轻击(tap)来描述这个选择操作，不要用触摸(touch)、点击(click)或者选择(choose)这类字眼。
- 不要用引号，但保证大写

**确保警告框在竖屏和横屏中均显示正常。**横屏模式下警告框的高度会受到限制，其大小与竖屏下可能会有区别。我们推荐您限定好警告框的最大高度，保证在竖屏和横屏模式下文字均能不需要滚动便可完整地显示。

**一般情况下，使用两个按钮的警告框。**两个按钮的警告框是最为常见和有用的，因为它最便于用户在两个按钮中做选择。单按钮警告框不那么有用，因为它通常只是起到告知的作用，并未给予用户控制当前状态的能力。多于两个按钮的警告框太过复杂，应该尽可能地避免使用。如果你在警告框中设计了太多按钮，它也许会导致警告框被强制滚动，这也是一个非常糟糕的体验。

[![two_button_alert_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223210019302.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223210019302.png)

提示

如果你需要在警告框中给与用户超过2个选项，可以考虑使用操作列表来代替警告框。

**正确地放置按钮。**理想情况下，最容易点击也最不容易点错的按钮符合两个条件：它代表了用户最可能会选择的操作，即使用户一时不注意误点了它，也不会造成严重问题。尤其是：

- 如果这个按钮不会造成损害性结果，又是用户最有可能会选择的操作，那么它应该放在右边，取消按钮则应该放在左边。
- 如果这个按钮会造成损害性后果，又是用户最有可能会选择的操作，那么它应该被放在左边，取消按钮应该放在右边。

提示

一般来说，当警告框出现的时候，按Home键将会从该app里切回主屏幕，此时Home键的效果类似于取消按钮——当用户回到app中的时候，警告框将消失，操作也不会被执行。

**为按钮设计简短而逻辑清晰的文案。**好的按钮文案一般只有1到2个单词，描述用户点击按钮后的结果。设计文案时可以遵循以下指南：

- 跟其它所有按钮一样，使用标题式大写，而且不需要标点符号
- 尽可能的使用与警告文案直接相关的动词或动词词组，如”取消(Cancel)”，”查看全部(View All)”，”回复(Reply)”和“忽略(Ignore)”等
- 当没有更好的选择的时候，可以使用”OK”.避免使用”是(Yes)”或”否(No)”。
- 避免使用”你”，“你的”，“我”，“我的”这类字眼。含有这些字眼的文案可能会指代不清，还有可能造成冒犯。

### 4.4.2 操作列表

操作列表展示了与用户触发的操作直接相关的一系列选项。

[![替换插图1](https://isux.tencent.com/wp-content/uploads/2015/12/20151224153501458-590x251.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151224153501458.png)

API提示：

如需在代码中使用操作列表，你可以创建一个[ UIAlertController](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIAlertController_class/index.html#//apple_ref/occ/cl/UIAlertController).并指定[UIAlertControllerStyleActionSheet](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIAlertController_class/index.html#//apple_ref/c/econst/UIAlertControllerStyleActionSheet)

操作列表：

- 由用户某个操作行为触发
- 包含两个或以上的按钮

使用操作列表来：

**提供完成一项任务的不同方法。**操作列表提供一系列在当前情景下可以完成当前任务的操作，而这样的形式不会永久占用页面UI的空间。

**在用户完成一项可能有风险的操作前获得用户的确认。**操作列表让用户有机会停下来充分考虑当前操作可能导致的危险结果，并为他们提供了一些其它的选项，尤其是在以下这些情景下：

[![cancel-btn](https://isux.tencent.com/wp-content/uploads/2015/12/20151223210342790.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223210342790.png)

**使用红色文字来表示可能存在破坏性的操作。**在操作列表的顶部使用文字颜色为红色的按钮，因为越靠近列表顶部的操作越容易引起用户注意。在iPhone里，潜在风险的操作离列表底部越远，用户在关注Home键的时候就越不容易误点它。

[![action_sheet_red_button_2x](https://isux.tencent.com/wp-content/uploads/2015/12/2015122321015772.png)](https://isux.tencent.com/wp-content/uploads/2015/12/2015122321015772.png)

**避免让用户滚动操作列表。**如果你的操作列表中存在过多按钮，用户必须要滚动才能看完所有操作。这样的体验是可能让用户不安，因为他们要花更多的时间来充分理解每个选项的区别。此外，用户在滚动的过程中将很有可能误点其它按钮。

### 4.4.3模态视图

模态视图是一个以模态形式展现的视图，它为当前任务或当前工作流程提供独立的、自包含的(self-contained)功能。

[![modal_view_mail_compose_2x](https://isux.tencent.com/wp-content/uploads/2015/12/20151223210215774.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151223210215774.png)

API提示：

如需在代码中使用模态视图，你可以创建一个[ UIPresentationController](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIViewController_Class/index.html#//apple_ref/c/tdef/UIModalPresentationStylehttps://developer.apple.com/library/ios/documentation/UIKit/Reference/UIPresentationController_class/index.html). 并指定适当的样式(完整的样式列表，请参考[Modal Presentation Styles)](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIViewController_Class/index.html#//apple_ref/c/tdef/UIModalPresentationStylehttps://developer.apple.com/library/ios/documentation/UIKit/Reference/UIPresentationController_class/index.html)

模态视图：

- 能占据整个屏幕，它也可能占据整个父视图(parent view)的区域，或者是屏幕的一部分
- 包含完成当前任务所需的文字和控件
- 通常也会包含一个完成任务的按钮（点击后即可完成任务，当前模态视图也会消失），和一个取消按钮（点击后即放弃当前任务，同时当前模态视图消失）

当需要用户完成与你的app中的基础功能相关的、独立的任务的时候，可以使用模态视图。模态视图尤其适用于那些所需元素并非常驻在app主要UI中、又包含多个步骤的子任务。

**根据当前任务的种类和你的app的整体视觉风格来选择适当的模态视图。**你可以使用以下定义的任何一种模态视图样式：

[![替换插图2](https://isux.tencent.com/wp-content/uploads/2015/12/20151225114043309-590x581.png)](https://isux.tencent.com/wp-content/uploads/2015/12/20151225114043309.png)
**不要让模态视图覆盖在浮出层之上。**除了警告框外，没有任何元素应该覆盖在弹出层上面。除非极其少有的情况下，用户在弹出层内进行的操作结果必须要以模态视图的形式展现，即便是这个时候，也请先将弹出层关闭，再出现模态视图。

**确保你的模态视图看起来与你的app的整体视觉风格相协调。**举个例子，如果一个模态视图中含有导航条和取消或完成任务的按钮，这里的导航条样式应该与你的app中导航条一样。

**合适的话，在模态视图里加入可以说明任务内容的标题。**你可能还需要在模态视图里加入一些补充文字，来清楚地阐明任务内容，并提供一些任务指南。

**选择一个适当的过渡动画来展示模态视图。**使用与你的app一致的过渡动画，让用户可以准确地理解当前页面内容的转变与模态视图的出现。关于这一点，你可以指定以下任意一种过渡动画：

- **垂直出现(Vertical).**模态视图从底部边缘滑入屏幕，也同样从屏幕底部滑出（默认模式）。
- **弹出(Flip)**.当前视图从右往左水平滑动，露出模态视图。从视觉上看，模态视图好像原来就处于当前视图的下面，当前视图移开时，它便出现了。离开模态视图时，原先的父视图从左边滑回屏幕右边。

**如果你要改变当前的过渡动画样式，请确保这种改变对于用户而言是有用而且有意义的。**用户很容易便能感知到这些改变，还会认为这些改变存在特别的意义。最好能设计出一种符合逻辑并始终保持一致的过渡方式，让用户容易感知并且记忆。在没有充分理由支持的情况下，最好不要改变这些默认的过渡方式。

## 5. 图标与图形设计

### 5.1 图标与图像尺寸(Icon and Image Sizes)

每个app都需要icon，以及启动画面，此外一些app需要一些自定义图标用于导航栏、工具栏和标签栏中，来代表app特有的内容、功能或模式。表格45-1所罗列出来的尺寸可以为自定义图标和图片做参考。

**表格45-1** ：自定义图标和图像的尺寸(像素)

![iOS9_P5_01](https://isux.tencent.com/wp-content/uploads/2016/03/20160307163503547-590x1038.png)

注意：

如果你需要在主屏幕快捷操作上创建自定义icon，请参考[主屏幕快捷操作](https://isux.tencent.com/ios9-guideline-ch3-1.html#title-0) 。

除了AppStore的icon，你必须把命名为iTunesArtwork之外，你可以任意命名你的icon。在xcode工程中可以使用图片资源目录来组织你的图片icon文件。如果要添加icon，在工程图片资源目录下添加对应的图片文件。在编译时，xcode添加合适的密钥到你的应用Info.plist文件中并且把图片打包进应用中。iOS会根据设备尺寸选择一个合适的icon。关于asset catalogs想要知道更多，可以查阅*Asset Catlog Help*。

所有的图片和icon建议使用png格式，避免使用交错的png。icon和图像的标准位深(bit depth)是24位。

 

### 5.2 应用图标(App Icon)

每一个app都需要一个精美、辨识度高的icon来让自己在App Store和用户桌面中脱颖而出。在iOS中，各个不同尺寸的icon将被用于Game Center，搜索结果，设置之中，还会用于代表由这个app创建的文档。

![iOS9_P5_02](https://isux.tencent.com/wp-content/uploads/2016/03/20160307163505571.png)

**为了让icon达到最好的效果，你可以求助于专业设计师。**一个有经验的设计师可以为你的app建立统一的视觉风格，同时把这种风格延续和浓缩到icon的设计中。

**使用通用的易于辨识的图形。**一般来说，避免使用意义不明的视觉元素，或者使用元素的次要含义。举个例子，邮件App会使用信封作为icon元素，而不会用邮箱、邮递员的邮包、或者邮局的标志。

**追求简约。**尤其是避免把一大堆不同的图形都塞到你的icon中去。找到一个简单的、可以代表你的app精髓的元素，然后把它设计成一个简单而独特的图形。添加细节时请慎重，如果一个icon的样式或形状过于复杂，它的细节可能会让用户迷惑，在小尺寸的icon中更可能会显示模糊。

注意：

想要测试你的图标在小尺寸下的显示效果，可以把它移动到主屏的文件夹下。最好是再往文件夹中多放几个不同的icon，然后看看你的app icon好看是否好看和突出。

**在icon中为你的app设计一个抽象释义。**在icon设计中照片或者截图效果通常都会很糟糕，那是因为这些相片级的细节在小尺寸中非常难以辨识。因此，我们最好以艺术的方式来诠释现实，因为这样能够让用户很容易领悟到你想他们注意到的方面。

**如果你坚持完全拟物化，请务必做到十分精确。**代表真实物品的icon或者图像应该精确地描摹出实物的特征，如织物、玻璃、纸张、金属等等，还要能表达实物的重量和质感。

**保证你的icon在不同的背景图中都是好看的。**不要只是单一在浅色或者深色背景中测试你的icon效果，因为你无法预料你的用户会使用什么样的墙纸。

**避免使用透明度。**App icon必须是不透明的。如果icon的边界小于推荐尺寸，又或者你创建了透明区域，那么你的icon下面就会出现黑色背景，你的icon将会浮于黑背景之上，这在用户所用的漂亮壁纸上看起来不美观。

**不要在图标中使用iOS的界面元素。**你一定不希望用户会把你的app icon或图形与iOS的系统UI搞混。

**不要在icon中使用苹果的硬件产品标志。**代表苹果产品的各个标志都是受版权保护的，不允许复用到你的icon或者图形中。一般来说，要避免在你的icon中复用任何特定设备标志，因为这些标志的设计常常变化，而基于这些设计的icon和图形很容易就会过时。

**不要在你的界面中复用iOS自带的app icon。**同样的icon含义却有轻微不同，还同时出现在整个系统的不同位置之中，这会让用户非常困惑。

**为不同设备准备不同大小的icon。**你需要确保你的应用icon支持所有的设备。对于不同设备应该选用的icon尺寸，可以参考[表格45-1](https://isux.tencent.com/ios9-guideline-ch5.html#title-0)。

当icon出现在iOS桌面上的时候，它会自动叠加圆角。请保证你的icon四个角都是90°，这样它们在圆角处理后仍然很好看。举个例子：

![iOS9_P5_03](https://isux.tencent.com/wp-content/uploads/2016/03/20160307163506184-590x82.png)

**创建一个大尺寸的app icon，用于显示在App Store上。**虽然让你的用户能轻易认出你的icon这点很重要，但相比之前这些尺寸，这个尺寸的icon允许你添加更多精巧的细节。这个尺寸的app icon显示在App Store上时将不再额外添加任何视觉效果。

如同[表格45-1](https://isux.tencent.com/ios9-guideline-ch5.html#title-0)所示，更大尺寸1024x1024像素的icon应该被命名为iTunesArtWork@2x(如果需要支持@1x的设备，创建一个大小为512x512像素的icon，并且命名为iTunesArtWork)

注意：

iOS可能会把大尺寸icon用于其它用途。比如在iPad app中，iOS会用大尺寸icon来生成大的文档图标。

如果你正在开发一个临时发布的App(也就是说，它只是内部发布没有放在Appstor上)，你必须提供一个大尺寸的App icon,这个icon将会提高它在iTunes中的辨识度。

 

### 5.2.1 文档图标(Document Icons)

如果你的iOS app会创建自定义类型的文件，而你希望用户一眼就能看出这些文件是由你的app生成的。你不需要为这些文档重新设计图标，因为iOS会自动把你的app icon来作为这些文档的图标。

 

### 5.2.2 用于Spotlight和设置的图标(Spotlight and Settings Icons)

每个app都应该提供一个小尺寸的图标，用于在spotlight搜索结果中展示。同样地，每个app都应该提供一个小尺寸的图标，用于在系统内置的设置页面中展示。

这些icon应该易于辨识，方便用户在搜索结果列表或者设置页的app列表中一眼就可以看出来。举个例子，在下图设置界面中，这些icon虽然很小，但每一个都清晰可辨：

![iOS9_P5_04](https://isux.tencent.com/wp-content/uploads/2016/03/20160307163506756.png)

和app icons一样，你可以任意命名这些小icon，因为iOS在使用的时候通常会照惯例自动选择合适尺寸的icon。

对于所有的设备，请分别为Spotlight搜索结果和设置界面单独提供icon。如果你没有提供这些icon，在这些位置iOS可能会缩小你的应用icon。[表格45-1](https://isux.tencent.com/ios9-guideline-ch5.html#title-0)显示了不同尺寸的详细信息。

注意：

如果你的icon底色是白色的，不需要增加灰色遮罩来增强app在设置界面的可见度。iOS会自动为icon增加1像素的描边，来保证在白色背景的设置界面中所有icon都能达到良好的显示效果。

## 

### 5.3 启动画面(Launch Files)

启动画面是在你的应用启动时展示的简单占位图。由于启动画面会在用户启动你的app时立刻出现，并且很快地被app的首屏取代，它会让用户认为你的app运行和响应的速度都非常快。每一个应用都要提供一个启动文件或至少一张静态图片。

在 iOS8 以后，你可以使用一个 XIB 或故事板文件来替代静态的启动图片。在 Interface Builder 中创建启动文件后，使用尺寸归类来为不同的界面环境定义不同的层，你还可以使用自动布局来进行细节调整。利用尺寸归类和自动布局，你可以只创建一个启动文件，就可以在所有设备里都有不错的呈现。(如果要了解呈现环境和尺寸归类的概览，参见[1.3.1 为自适应而开发](https://isux.tencent.com/ios9-guideline-ch1.html#title-6) ；了解如何在 Interface Builder 中使用尺寸归类，可参见[*Size Classes Design Help*](https://developer.apple.com/library/ios/recipes/xcode_help-IB_adaptive_sizes/_index.html)* *。)

* *如果你需要支持早期的 iOS 版本，除启动文件外可以继续使用静态启动图片。

重要：

使用 XIB 或故事板的文件，表示你的应用程序在iPhone 6 Plus 或 iPhone 6上运行。

以下的设计规范，适用于启动文件及静态图片：

**简单的启动图片可以提升用户体验**。通常情况下，启动图片不需要提供如下内容：

- “进入应用的过程”，例如载入进程图。
- 带有“关于信息”的窗口。
- 品牌元素，除非它们是 app 第一屏的静态内容。

由于用户会在 app 之间频繁地切换，所以你应该尽可能地缩短加载时间，通过设计降低用户对启动过程的感知，而不是加重用户对启动的印象。

**我们也可以设计一个与APP首屏一样的启动画面**。除非：

- 文本。启动图片是静态的，所以启动图片中的任何文本都不会有局限。
- 可能会变化的 UI 元素。如果 app 启动完成后有元素发生可见的变化，用户可能会对启动画面和第一屏之间的变化感到不适应。

如果你认为遵循这些规范，往往只会设计出平凡而乏味的启动图片，倒也没说错。请记住，启动图片不意味着需要你在里面炫技，它的目标只是增强用户对应用可以被快速启动并开始使用的感受。例如系统设置和天气应用都仅仅提供了一个相当于背景的启动图片。

系统设置的启动图片

![iOS9_P5_05](https://isux.tencent.com/wp-content/uploads/2016/03/20160307163507296.png)

天气应用的启动图片

![iOS9_P5_06](https://isux.tencent.com/wp-content/uploads/2016/03/20160307163507875.png)

 

如果你需要使用静态启动图片，你需要准备尺寸不同的启动画面以适应不同的设备，且所有设备上的静态启动图片都必须包含状态栏的区域。具体尺寸请查阅[表格 45-1](https://isux.tencent.com/ios9-guideline-ch5.html#title-0) 。

虽然最好在 iPhone 6 和 iPhone 6 Plus 上使用启动文件，但需要的话，你也可以替换为静态启动图片。如果你需要为 iPhone 6 和 iPhone 6 Plus 创建静态启动图片，请使用以下尺寸：

For iPhone 6:

- 纵向： 750 x 1334 像素(@2x)
- 横向： 1334 x 750 像素(@2x)

For iPhone 6 Plus:

- 纵向： 1242 x 2208 像素 (@ 3X)
- 横向： 2208 x 1242 像素 (@ 3X)

 

### 5.4 模板图标(Template Icons)

你为工具栏或主屏幕快速操作创建的自定义图标，也就是模板图标或图片，因为当你的 app 运行时，iOS 将它作为一个 mask(iOS的一个开发相关名词)来介绍你所看到的图标。

iOS 定义了很多标准的小图标，例如刷新、操作、增加及收藏等。如果可能的话，你应当使用这些按钮和图标来表示 app 里的常规任务。(了解更多可以使用的标准按钮及图标，可参见[4.1.4 工具栏与导航标准按钮](https://isux.tencent.com/ios9-guideline-ch4.html#title-3)和[4.1.6 标签栏标准图标](https://isux.tencent.com/ios9-guideline-ch4.html#title-5)章节。)

如果你的app中包含标准按钮图标不能代表的任务或者模式——又或者标准按钮与你的app风格相差太远——你可以设计自己的栏按钮图标。以更高的要求来看，你应该以下列几点为目标来设计icon：

- **简单明了。**太多的细节会令图标看起来过于草率且识别度低。
- **不容易与系统图标混淆。**用户应该一眼就在你的图标和系统图标中区分出来 。
- **易于理解并被广泛接受**。尝试创造多数用户都能正确理解的标志，并不让它们感到攻击性。

重要：

确保你的设计中没有复用苹果官方产品的图形。这些标志受版权保护，而且相关产品的设计会频繁变化。

无论你是只使用自己设计的图标，或者是与系统标准图标混用，所有你的app中出现的图标都应该看起来属于同一种风格：它们看起来拥有同样的尺寸、细节精度以及视觉权重。

举个例子，下图中的iOS栏标准图标，你会注意到他们之间在尺寸、细节和重量上都拥有很高的相似性，从而形成了一个协调的联合体：

![iOS9_P5_07](https://isux.tencent.com/wp-content/uploads/2016/03/20160307163508447-590x148.png)

想要设计一套风格协调连贯的图标，一致性是关键：尽量让每个图标都使用相同的透视和粗细相同的线条。为了保证所有的icon尺寸视觉上统一，你可能需要设计一些实际上尺寸并不相同的icon。举个例子，下面这组系统标准图标看起来大小一致，但实际上收藏夹和语音邮箱的icon比其它三个略大一些。

![iOS9_P5_08](https://isux.tencent.com/wp-content/uploads/2016/03/2016030716350991-590x91.png)

如果你在设计用于标签栏的图标，你应该提供图标的两种状态——未选中态和选中态。通常选中态是非选中态填充了颜色的样子，但有些设计需要在此方法的前提下进行一些变化：

![iOS9_P5_09](https://isux.tencent.com/wp-content/uploads/2016/03/20160307163509629.png)

创建有内部细节的图标的选中态版本时(例如收音机图标)，将内部细节反过来填充，以确保这些细节在选中态依然突出。键区图标虽然也拥有一些内部细节，但如果对选中态的背景进行填充，并在圆圈上增加白色边线，就会令用户感到混淆。

![iOS9_P5_10](https://isux.tencent.com/wp-content/uploads/2016/03/2016030716351083.png)

有时候给予选中态一些细微的变化令其有更好的显示效果。例如计时器和播客的图标都包含一些开放的区域，所以选中态将其描边略微缩小并放在了一个圆圈内。

如果图标在填充后会让人难以辨认，好的替代方案就是使用更重的描边来表示选中态。例如语音邮箱和阅读列表的图标的选中态就是使用了 2 点的描边，而未选中态是用 1 点来描边的。

![iOS9_P5_11](https://isux.tencent.com/wp-content/uploads/2016/03/20160307163510538.png)

有些图标由于形状细节的关系，增加描边后看起来并不好。例如这几个案例——音乐和艺术家的图标——两种状态都使用填充效果。用户很简单就能分辨出选中态和未选中态，因为选中态有颜色，视觉表现更重一些。

![iOS9_P5_12](https://isux.tencent.com/wp-content/uploads/2016/03/20160307163510958.png)

设计模板图标时，需要遵循以下规则：

- 使用带的透明度的纯色来绘制图标。iOS会去除所有的颜色信息，所以不需要使用超过 1 种填充色。
- 不要使用阴影。
- 图形需要平滑无锯齿。

如果你要设计一个看起来足够有 iOS 原生感的图标，你可以使用细描边来绘制它。具体来说，使用 1-point 描边(也就是在 @2x 分辨率下是 2 像素描边)

不管图标的是怎样的视觉风格，都需要按照尺寸表[表格 45-1](https://isux.tencent.com/ios9-guideline-ch5.html#title-0)来创建自定义工具栏、导航栏以及标签栏的图标。如果你设计的是主屏幕快速操作的模板图标，详情参见[3.1.2 主屏幕快捷操作](https://isux.tencent.com/ios9-guideline-ch3-1.html#title-2) 。

不要在自定义标签栏图标中包含文本，而是使用标签栏的 API 来为每一个标签设置标题(例如[initWithTitle:image:tag:](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITabBarItem_Class/index.html) )。如果你需要调整标题的自动布局，你可以使用标题 API 例如[setTitlePositionAdjustment:](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UITabBarItem_Class/index.html) )。

 

### 5.5 网页图标(Web Clip Icons)

对于网页应用或网站，你可以提供一个定制图标，让你的用户通过网页剪辑(Web clip)将你的app展现在主屏幕上。用户只需要点击这个icon便可直接获取你的网页内容。你可以创建一个可以代表你的整个网站或某个单独网页的图标。

iOS也会在Safari的收藏夹中展示网页图标，当用户点击Safari的URL栏或者打开一个新的网页标签时，这些网页图标就会以矩阵的形式出现。

如果你的网页内容使用了常用的图像或容易辨认的配色方案，你的icon也应该融入这些特征。然而，为了确保图标在设备中更加漂亮，你应该同时遵循以下这些指南：(想要了解如何在你的网页内容中增加代码来提供自定义图标，请参考[Specifying a Webpage Icon for Web Clip](https://isux.tencent.com/ios9-guideline-ch5.html#//apple_ref/doc/uid/TP40002051-CH3-SW4))。

对于的尺寸的图标，请参考[表格 45-1](https://isux.tencent.com/ios9-guideline-ch5.html#title-0)。

注意：

尽量避免把你的icon命名为apple-touch-icon-precomposed.png.

 

### 5.6 创建可缩放图片(Creating Resizable Images)

你可以通过制作可缩放图片来定制一些标准UI元素的背景，如弹窗，按钮，导航栏，标签栏等，还包括这些栏上的项。提供这些元素的可缩放图片会优化app的整体性能。

对于许多界面元素，你可以使用端盖来替代背景。端盖可定义图像内的一个不被放大或缩小的区域。例如，你可以创建一个包含 4 个端盖的可拉伸图片，将其作为一个按钮的 4 个角。当图片被缩放来适应按钮大小时，被端盖指定的四个角则不会发生变化。

据你所提供的可缩放图片，iOS会进行拉伸或者平铺，直到图片可以正确填充当前UI元素的背景区域。拉伸指的是在不考虑图片原始比例的情况下放大图片。拉伸图片的性能较高，但对于多像素图片来说，会出现失真现象。平铺指的是按照图片的原始尺寸多次复制图片，直到填充目标区域。平铺的性能较低，但它是能够准确实现纹理和图案的唯一方法。

一般来说，提供一张不包含端盖的最小尺寸可缩放图像即可达到想要的效果，比如：

- 如果你需要不包含渐变的实色图，制作1×1像素的图片。
- 如果你需要垂直简便的效果，制作一个宽度为1像素，高度与UI元素背景区域高度相等的图像。
- 如果你需要重复的纹理效果，你需要制作一个尺寸与纹理最小重复部分尺寸相等的图像。
- 如果你需要不重复的纹理效果，你需要制作一个与你的UI元素背景区域大小相等的静态图像。