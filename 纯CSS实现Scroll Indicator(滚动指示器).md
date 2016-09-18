# 纯CSS实现Scroll Indicator(滚动指示器)

Scroll Indicator称之为滚动指示器，是Web中常见的一种效果。用户滚动垂直滚动内容时，页面顶部有一个类似进度条的效果，当内容滚动到页面最低端，进度条效果填满整个进度条。感觉描述得有点绕，还是录制一个动效图，用图来说明这种效果，毕竟一图胜过千言万语：

![Scroll Indicator](http://cdn2.w3cplus.com/cdn/farfuture/jbJ19Vf6qKO2iUkxID5pbzBIjckFYQRWnMPpCPrqzec/mtime:1470830065/sites/default/files/blogs/2016/1608/scroll-indicator-1.gif)

以前实现这种效果都需要借助于JavaScript，或者说是采用jQuery的插件。网上有关于这方面的介绍的文章也很多，比如：

- [@PANKAJ PARASHAR](https://css-tricks.com/author/pankajparashar/)的《[Reading Position Indicator](https://css-tricks.com/reading-position-indicator/)》
- [@Jonathan Cutrell](http://tutsplus.com/authors/jonathan-cutrell)的《[How to Build a Page Scroll Progress Indicator With jQuery and SVG](http://webdesign.tutsplus.com/tutorials/how-to-build-a-page-scroll-progress-indicator-with-jquery-and-svg--cms-20881)》

但今天咱们要说的是使用纯CSS制作Scroll Indicator效果。说到这里，大家或许会问，这样的效果用CSS实现，吹了吧。其实使用纯CSS实现一点也没有问题。如果你感兴趣，欢迎接着往下阅读。

## Scroll Indicator几个关键点

先来看JavaScript的做法：

![Scroll Indicator](http://cdn2.w3cplus.com/cdn/farfuture/HoJZnIWNVaSegNtw-_235n1PNKo6tuL9DrYs6A6MrwY/mtime:1470831282/sites/default/files/blogs/2016/1608/scroll-indicator-2.gif)

看代码变化就清楚，通过JavaScript改变容器`scroll-line`的`width`值。也就是在滚动内容的时候，`width`值从`0%`变化到`100%`。其中最重要的是要知道滚动条位置的计算。在整个计算中，要知道两个重要的参数:

- **document height**:文档的高度`$(document).height()`
- **window height**: 视窗高度`$(window).height()`

如下图所示：

![Scroll Indicator](http://cdn2.w3cplus.com/cdn/farfuture/iMfpZEBr6RcTOg5inLoNVmz4i0TS9alCo5jUJPiud10/mtime:1470832204/sites/default/files/blogs/2016/1608/scroll-indicator-3.png)

文档高度和视窗高度有一个差值`max`，其实这个差值就是需要滚动的值，简单的理解就是`scroll-line`宽度为`100%`时候的宽度值。这样一来，咱们就知道了全宽的`width`值，另外还需要知道的另一个关键值是滚动条的位置的值`$(window).scrollTop()`。有了这两个值，通过`($(window).scrollTop() / ($(document).height() - $(window).height())) * 100%`就知道进度条的当前值。

![Scroll Indicator](http://cdn.w3cplus.com/cdn/farfuture/ZRcF1MQXQbsS7-gUhsajfmHLnNV83aWhcvR23Ypvpo8/mtime:1470832204/sites/default/files/blogs/2016/1608/scroll-indicator-4.gif)

最终效果可以看看[@Derek Palladino](http://codepen.io/derekjp)在CodePen写的一个示例：

另外再看一个[@Dan Eden](http://daneden.me/styleguide/)写的一个示例：

有关于JavaScript实现方案相关介绍，可以仔细阅读上面的两篇文章。

## CSS实现方案

纯CSS实现Scroll Indicator效果最难的是不知道滚动条距顶部的距离，而且也不知道文档高度和视窗高度的差值。要按前面的方案实现，是不太可能。不过我们可以通过别的方案来模拟。

同样的需要两个容器：

```
<div class="scroll-process">
    <div class="scroll-line"></div>
</div>

```

其中`scroll-process`是全屏宽，也就是相当于`($(document).height() - $(window).height())`,里面`scroll-line`的宽度就是`($(window).scrollTop() / ($(document).height() - $(window).height())) * 100%`。如下图所示：

![Scroll Indicator](http://cdn2.w3cplus.com/cdn/farfuture/EMVxO28YoKPaZQ_JSRXrrQ_EFCuMLaJTAqX56ntrBwQ/mtime:1470833044/sites/default/files/blogs/2016/1608/scroll-indicator-5.png)

上图蓝色区域是`scroll-line`，灰色区域是`scroll-process`。

原理是一样，只是实现我们不能借助JavaScript实现，而是需要使用CSS来模拟JavaScript效果。

仔细思考一下，在Web中，自带滚动功能的是`body`元素，或者说某个限制大小尺寸，设置了`overflow`属性为`scroll`值也会出现滚动条效果。另外，要随着滚动条滚动，`scroll-line`要出现类似进度条的效果。

![Scroll Indicator](http://cdn1.w3cplus.com/cdn/farfuture/ll5U28gb9B7bGE2oTXumfTZv4VlwAkH-tRCTcGHLEf0/mtime:1470834485/sites/default/files/blogs/2016/1608/scroll-indicator-6.gif)

上图简单的模拟出来进度条的效果了，而实现上现的效果，在CSS中是很容易的，我们只需要在容器中使用CSS的[`line-gradient`](http://www.w3cplus.com/content/css3-gradient)属性。比如说在`body`中使用：

```
background: linear-gradient(to right top, #0089f2 50%, #DDD 50%);

```

这样的效果还不能满足我们的需求：

上面示例演示的是`100vh`的高度，也就是视窗高度，按上面的方式，先看下面的动图：

![Scroll Indicator](http://cdn.w3cplus.com/cdn/farfuture/kIur7FsVhj0fHE4xpyfChItM-8u7Ojdi_JH2M5NWO84/mtime:1470835502/sites/default/files/blogs/2016/1608/scroll-indicator-7.gif)

这个效果才是我们想要的。当然并不是完美。不过先忽略这一点。如果要实现上图的效果，还要做一下处理。在CSS中有一个[`background-size`](http://www.w3cplus.com/content/css3-background-size)属性，这个属性可以帮助我们控制背景图大小，也就是渐变图的大小。而对于[`background-size`](http://www.w3cplus.com/content/css3-background-size)需要的是其`y`轴的值。那问题又来了，`y`轴的值怎么确定。

在CSS中要得到视窗高度，也就是前面所说的`$(window).height()`。它就是`100vh`。而我们进度的值是`($(window).scrollTop() / ($(document).height() - $(window).height())) * 100%`。要对于`background-size`的`y`与其一样，那么可以通过`100%-100vh`。要得到`100% - 100vh`的值还需要使用CSS中的[`calc()`](http://www.w3cplus.com/css3/how-to-use-css3-calc-function.html)：

```
body{
  background: linear-gradient(to right top, #0089f2 50%, #DDD 50%);
  background-size: 100% calc(100% - 100vh);
}

```

离需要的效果越来越近了：

最近需要一个蒙层，让进度条看上去更美一些。

```
body:before {
  content: '';
  position: fixed;
  top: 5px;
  bottom: 0;
  width: 100%;
  z-index: -1;
  background: white;
}

```

效果如下：

现在效果出来了，是不是和使用JavaScript的非常类似了。最后再给大家贴一效果：

这个效果是[@Mike](http://codepen.io/MadeByMike)写的一个效果。

## 总结

这篇文章主要通过CSS的几个属性的结合来模拟Scroll Indicator的一个效果。主要通过CSS的[`linear-gradient`](http://www.w3cplus.com/content/css3-gradient)配合[`background-size`](http://www.w3cplus.com/content/css3-background-size)的属性模拟进度条的效果，模拟这个效果还需要借助CSS的视窗单位[`vh`](http://www.w3cplus.com/blog/tags/485.html)和[`calc()`](http://www.w3cplus.com/css3/how-to-use-css3-calc-function.html)得到滚动条位置。

如果你有更好的方案，欢迎在下面的评论中一起分享。