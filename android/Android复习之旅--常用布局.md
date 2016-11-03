# Android复习之旅--常用布局

作为菜鸟，以下只是总结了一些布局中的属性和一些不成熟的见解，并没有对各种布局进行更高级更详细的分析，而且我也不会。后面倒有一个大神stormzhang对Android布局方式优化的博文，大家可以去看看。

对于Android的布局方式，其实常用到的布局也就三种（LinearLayout、RelativeLayout、FrameLayout）。

##### LinearLayout(线性布局)

> 布局层次如果和使用RelativLayout的层次一样，建议使用LinearLayout，因为LinearLayout的性能要好一些

常用属性：

```
orientation：布局中组件的排列方式，有horizontal(水平)、vertical(竖直,默认)两种方式
gravity：控制组件所包含的子元素的对齐方式,可多个组合,如(left|bottom)
layout_gravity：控制该组件在父容器里的对齐方式
background：为给组件设置一个背景颜色或背景图片
```

** layout_weight(权重)：用来等比例划分区域 **

> 比例：权重值/布局中的权重值之和

(分割线)：

```
divider：为LinerLayout设置分割线的图片
showDividers：设置分割线的位置，有四个可选值(none，middle，begining，end)
dividerPadding：设置分割线的padding
```

##### RelativeLayout(相对布局)

> 对于一些复杂的布局方式，使用相对布局是最容易实现的

常用属性：

```
gravity：设置容器内组件的对齐方式
ignoreGravity：设置该属性为true的组件，将不受gravity属性的影响
```

** 相对布局里的控件定位属性：**
根据父容器定位：

```
layout_alignParentLeft：左对齐(true|false)
layout_alignParentRight：右对齐(true|false)
layout_alignParentTop：顶部对齐(true|false)
layout_alignParentBottom：底部对齐(true|false)
layout_centerHorizontal：水平居中(true|false)
layout_centerVertical：垂直居中(true|false)
layout_centerInParent：中间位置(true|false)
```

根据兄弟组件定位：

```
layout_toLeftOf：参考组件的左边( @id/..)
layout_toRightOf：参考组件的右边(@id/..)
layout_above：参考组件的上方(@id/..)
layout_below：参考组件的下方(@id/..)
layout_alignTop：对齐参考组件的上边界(@id/..)
layout_alignBottom：对齐参考组件的下边界(@id/..)
layout_alignLeft：对齐参考组件的左边界(@id/..)
layout_alignRight：对齐参考组件的右边界(@id/..)
```

##### FrameLayout(帧布局)：

> 可以动态地为帧布局添加View或者一个布局文件。帧布局的子控件式以栈的形式进行存放的，最后添加到布局中的子控件在栈的顶部，可以实现刮刮乐等的效果

常用属性：

```
foreground：设置该帧布局容器的前景图像
foregroundGravity：设置前景图像显示的位置（* 前景图像永远处于帧布局的最上面，直接面对用户的图像，就是不会被覆盖的图片* ）
```

##### GridLayout(网格布局)

> 可以实现控件的交错显示，例如计算器等

常用属性：

```
orientation(排列方式)：vertical(竖直，默认)、horizontal(水平)
rowCount：设置网格的行数
columnCount：设置网格的列数
layout_row：设置组件位于第几行(以0开始计算)
layout_column：设置组件位于第几列(以0开始计算)
layou_rowSpan：横跨多少行(合并行)
layout_column：横跨多少列(合并列)
```

** TableLayout(表格布局) **

> 较少使用

常用属性：

```
collapseColumns：设置需要隐藏的列的序号
shrinkColumns：设置允许被收缩的列的列序号
stretchColumns：设置允许被拉伸的列的列序号
layout_span="2"：合并两个单元格
```

**AbsoluteLayout(绝对布局) **

> 一般不会使用它来布局，知道就可以了

常用属性：

```
layout_x：设置组件的X坐标
layout_y：设置组件的y坐标
```

** 布局优化 **
尽量多使用RelativeLayout和LinearLayout, 不要使用绝对布局AbsoluteLayout，在布局层次一样的情况下， 建议使用LinearLayout代替RelativeLayout, 因为LinearLayout性能要稍高一点，但往往RelativeLayout可以简单实现LinearLayout嵌套才能实现的布局。

- 将可复用的组件抽取出来并通过include标签使用；
- 使用ViewStub标签来加载一些不常用的布局；
- 使用merge标签减少布局的嵌套层次；

文／飘渺云轩（简书作者）
原文链接：http://www.jianshu.com/p/48606be23ee2
著作权归作者所有，转载请联系作者获得授权，并标注“简书作者”。