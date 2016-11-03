# Android弹性布局(FlexboxLayout)

### Flexbox简介

flexbox是属于CSS的一种布局方案，可以简单、完整、响应式的实现各种页面布局。谷歌将其引入以提高复杂布局的能力。
[源码传送门](https://github.com/google/flexbox-layout)

### Flexbox的布局和相关名称

![img](http://upload-images.jianshu.io/upload_images/693110-53c5ca883d4326ca.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

上图模型中包含以下概念

1. flex container 父容器，用来包含子元素，对应于FlexboxLayout类。
2. flex item 子元素，父容器直接包裹的元素。
3. main axis 主轴，子元素通过主轴来排列，如上图是从左往右。
4. corss axis 副轴，垂直于主轴的第二个轴
5. main start,main end 父容器中主轴开始和结束的边界，子元素从main start往main end的方向排列（如果主轴是水平，起点在左端，main start,main end 用来控制子元素从左向右排列）
6. cross start,corss end 父容器中副轴开始和结束的边界。子元素从cross start往cross end方向排列(如果主轴是水平的，那么副轴就是垂直的，假设如上图，cross start 在上，cross end 在下，那么子元素就是从上往下排列)

### Flexbox 布局示例

```
<com.google.android.flexbox.FlexboxLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    app:flexWrap="wrap"
    app:alignItems="stretch"
    app:alignContent="stretch" >

    <TextView
        android:id="@+id/textview1"
        android:layout_width="120dp"
        android:layout_height="80dp"
        app:layout_flexBasisPercent="50%"
        />

    <TextView
        android:id="@+id/textview2"
        android:layout_width="80dp"
        android:layout_height="80dp"
        app:layout_alignSelf="center"
        />

    <TextView
        android:id="@+id/textview3"
        android:layout_width="160dp"
        android:layout_height="80dp"
        app:layout_alignSelf="flex_end"
        />
</com.google.android.flexbox.FlexboxLayout>
```

或者代码

```
FlexboxLayout flexboxLayout = (FlexboxLayout) findViewById(R.id.flexbox_layout);
flexboxLayout.setFlexDirection(FlexboxLayout.FLEX_DIRECTION_COLUMN);

View view = flexboxLayout.getChildAt(0);
FlexboxLayout.LayoutParams lp = (FlexboxLayout.LayoutParams) view.getLayoutParams();
lp.order = -1;
lp.flexGrow = 2;
view.setLayoutParams(lp);
```

### 属性介绍

#### Contatiner的属性

1. flexDirection：子元素的排列方向，决定主轴和副轴的方向，有以下四个值，文字太鸡肋，直接看图结合demo一目了然。

   - row (default)

     ​

     ![img](http://upload-images.jianshu.io/upload_images/693110-0536099bbe149ba5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

   - row_reverse

     ​

     ![img](http://upload-images.jianshu.io/upload_images/693110-e9eb3fee830e8ed5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

   - column

     ​

     ![img](http://upload-images.jianshu.io/upload_images/693110-879a594fa6c76ab1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

   - column_reverse

     ​

     ![img](http://upload-images.jianshu.io/upload_images/693110-a9e6afd3c2303338.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

2. flexWrap：控制单行和多行，以及副轴的方向

   - nowrap (default) 不换行
   - wrap 换行
   - wrap_reverse 副轴方向置反

3. justifyContent 控制沿主轴对齐

   - flex-start（default）：左对齐
   - flex-end：右对齐
   - center： 居中
   - space-between：两端对齐，项目之间的间隔都相等。
   - space-around：每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍。

4. alignItems 控制沿副轴对齐(**单行起作用**)

   - stretch（default）：如果项目未设置高度或设为auto，将占满整个容器的高度。
   - flex-start：交叉轴的起点对齐。
   - flex-end：交叉轴的终点对齐。
   - center：交叉轴的中点对齐。
   - baseline: 项目的第一行文字的基线对齐。

5. alignContent ：控制沿副轴对齐(**多行起作用**)

   - stretch（default）：轴线占满整个交叉轴。
   - flex-start：与交叉轴的起点对齐。
   - flex-end：与交叉轴的终点对齐。
   - center：与交叉轴的中点对齐。
   - space-between：与交叉轴两端对齐，轴线之间的间隔平均分布。
   - space-around：每根轴线两侧的间隔都相等。所以，轴线之间的间隔比轴线与边框的间隔大一倍。

#### 子元素的属性

1. layout_order： 控制子元素布局的顺序，默认值为1，顺序为XML中元素的顺序
2. layout_flexGrow 类似于weight。
3. layout_flexShrink 空间不足时，子元素缩小，如果为0，不变化
4. layout_alignSelf 允许单个元素有不一样的对齐方式，会覆盖align-item,除auto外，其他取值都和align-item的含义一致。
   - auto (default) 继承父元素的align-item
   - flex_start
   - flex_end
   - center
   - baseline
   - stretch
5. layout_flexBasisPercent 只能为百分比的值，只有父元素是MeasureSpec.EXACTLY的模式时才有效。

### 与传统CSS弹性布局不同之处

1. 没有flex-flow属性 ：因为没必要
2. 没有flex属性：同样没必要
3. layout_flexBasisPercent 替代了flexBasis。如果子元素宽高确定了，可以指定具体值或百分比，如果是包裹内容，那只能是百分比
4. 不能确定min-width和min-height：因为谷歌还没实现

> 相关链接：
> [https://css-tricks.com/snippets/css/a-guide-to-flexbox/](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
> [https://github.com/google/flexbox-layout/wiki](https://github.com/google/flexbox-layout/wiki)
> [https://blog.stylingandroid.com/flexboxlayout-part-1/](https://blog.stylingandroid.com/flexboxlayout-part-1/)