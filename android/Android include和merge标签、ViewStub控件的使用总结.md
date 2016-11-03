# Android include和merge标签、ViewStub控件的使用总结

在开发Android布局时，常将一些通用的视图提取到一个单独的layout文件中，然后使用``标签在需要使用的其他layout布局文件中加载进来，比如App导航栏等。这样，便于对相同视图内容进行统一的控制管理，提高布局重用性。然而，使用``标签总有一些值得我们注意的地方。

## 根容器id与include id必须相同

如果我们给include所加载的layout布局的根容器设置了id属性，也在include标签中设置了id属性，同时需要在代码中获取根容器的控件对象时，一定要将这两个id设置相同的名称！否则，将获取不到根容器对象，即为null。举个例子：

我们将应用中的Toolbar提取到一个include_toolbar.xml文件中，并设置了Toolbar设置了id属性：

```
<?xml version="1.0" encoding="utf-8"?>
<android.support.v7.widget.Toolbar
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:id="@+id/tb_toolbar"
    android:layout_width="match_parent"
    android:layout_height="?attr/actionBarSize"
    app:titleTextColor="@android:color/white"
    app:title=""
    app:theme="@style/AppTheme"
    android:background="@color/blue"/>

```

然后在其他布局文件activity_main.xml中使用include标签加载上述Toolbar视图，同时由于相对布局的需要而将include标签设置了相同值的id属性：

```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

	<!-- 这里的id属性一定要与layout属性所加载的include_toolbar.xml布局的根容器设置相同的值！ -->
    <include
        android:id="@+id/tb_toolbar"
        layout="@layout/include_toolbar"/>

```

最后在代码文件MainActivity.java中获取Toolbar对象：

```
 @Override
 protected void onCreate(@Nullable Bundle savedInstanceState) {
     super.onCreate(savedInstanceState);
     setContentView(R.layout.activity_main);

//如果include布局根容器和include标签中的id设置的是不同的值，这里获取的mToolbar值将为null
     Toolbar mToolbar = (Toolbar) findViewById(R.id.tb_toolbar);
     setSupportActionBar(mToolbar);
 }

```

## 宽高属性与其他属性的联合使用

在使用include标签时，除了使用layout属性加载布局文件时，一般不需要设置其他属性了，比如：

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical">

    <include
        layout="@layout/include_toolbar"/>

    ......

</LinearLayout>

```

但有时为了布局的需要，仍要使用诸如`layout_margin`等除id之外的其他属性，这时就要注意，为了使这些其他属性起作用，必须同时设置include标签的宽高属性，如：

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical">

    <include
        layout="@layout/include_toolbar"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="8dp"/>

    ......

</LinearLayout>

```

# ``标签

``标签存在的意义是帮助``标签排除多余的一层ViewGroup容器，减少view hierarchy的结构，提升UI performance。[Developers官网](https://developer.android.com/training/improving-layouts/reusing-layouts.html)举了一个很好的例子，大家可以自行查看一下，总结其意思就是，在主界面中，``标签的parent ViewGroup与包含的layout根容器ViewGroup是相同的类型，那么则可以将包含的layout根容器ViewGroup使用``标签代替，从而减少一层ViewGroup的嵌套，从而提升UI性能渲染。举个例子就是：

```
<merge xmlns:android="http://schemas.android.com/apk/res/android">

    <!-- re-used views -->
    ......

</merge>

```

然后再在其他界面中使用``标签加载重用布局文件即可。

# ViewStub控件

android.view.ViewStub也可以用来加载布局文件，但与include标签完全不同。ViewStub是一个不可见的View类，用于在运行时按需懒加载资源，只有在代码中调用了`viewStub.inflate()`或者`viewStub.setVisible(View.visible)`方法时才内容才变得可见。这里需要注意的一点是，当ViewStub被inflate到parent时，ViewStub就被remove掉了，即当前view hierarchy中不再存在ViewStub，而是使用对应的layout视图代替。ViewStub有几个属性和方法值得说明一下：

- `android:layout`属性
  加载包含的layout布局文件；
- `android:inflatedId`属性
  重写包含的layout布局文件的根容器id；
- `inflate()`方法
  与`setVisible(int)`方法作用类似，都可以使内容得以显示，只是`inflate()`会返回一个View对象，避免了额外使用`findViewById()`方法获取layout视图对象。

举个例子说明一下，按需加载的`viewstub_content.xml`内容如下（这里只是个例子，只有一个TextView，实际使用中一定是一个复杂的布局才用得上ViewStub）：

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:gravity="center"
    android:orientation="vertical">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Content"/>

</LinearLayout>

```

Activity界面布局文件`activity_main.xml`内容如下，只有一个Button按钮和ViewStub控件:

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical">

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_gravity="center_horizontal"
        android:text="Show"
        android:onClick="onClick"/>

    <ViewStub
        android:id="@+id/vs_viewStub"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:layout="@layout/viewstub_content"/>

</LinearLayout>

```

对应的java代码如下，点击按钮显示ViewStub的内容：

```
public void onClick(View v) {
    View view = ((ViewStub) findViewById(R.id.vs_viewStub)).inflate();
}

```

点击按钮，即可显示ViewStub的内容。我们用`Hierarchy View`观察一下视图层次的情况，当Activity初始化时，视图结构如下：

[![ViewStub-Samles-01](http://ocq7gtgqu.bkt.clouddn.com/ViewStub-Samles-01.png)](http://ocq7gtgqu.bkt.clouddn.com/ViewStub-Samles-01.png)

可以看到，当前view hierarchy中存在的是ViewStub而不是包含的layout布局。点击一下按钮，显示内容，再看一下：

[![ViewStub-Samles-01](http://ocq7gtgqu.bkt.clouddn.com/ViewStub-Samles-02.png)](http://ocq7gtgqu.bkt.clouddn.com/ViewStub-Samles-02.png)

ViewStub已经remove掉了，而包含的layout布局加入到当前view hierarchy中，即无法使用`findViewById()`方法获取ViewStub的引用。

所以，``标签与ViewStub完全不是同一个概念，ViewStub自带懒加载特性，可以理解为一个轻量级的View，自身占用资源较小，在UI初始化时所对应的layout布局视图不占用系统资源，从而可以加快当前界面的渲染过程，相比使用普通的`view.setVisible(int)`方法，性能体验提高不少，而``标签则只是用于提高布局的重用性，使用场景大有不同。