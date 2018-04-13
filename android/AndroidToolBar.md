Android ToolBar
---
[Android中Toolbar的使用](http://blog.csdn.net/wsdssss/article/details/51276715)  
android.support.v7.widget.Toolbar  

[android之Toolbar使用详解](http://blog.csdn.net/listeners_gao/article/details/52736008)  

[Android5.0之Toolbar详解](http://blog.csdn.net/leonduhua/article/details/54604208)  
基本属性设置  
    <android.support.v7.widget.Toolbar
        android:id="@+id/toolbar"
        android:layout_width="match_parent"
        android:layout_height="?attr/actionBarSize"
        android:background="@color/colorPrimary"
        app:navigationIcon="@mipmap/title_bar_back"//左侧图标
        app:subtitle="子标题"
        app:subtitleTextColor="#fff" //标题颜色
        app:title="标题"
        app:titleTextColor="#fff"/> //子标题颜色

[Android ToolBar 使用完全解析](http://www.jianshu.com/p/ae0013a4f71a)  
创建了android.support.v7.widget.Toolbar，同时我们在内部放了一个TextView，这是与ActionBar最大的不同，因为ToolBar实际上是一个ViewGroup，支持在其内部放入子View。

修改标题和子标题的字体大小、颜色等，可以调用 setTitleTextColor 、 setTitleTextAppearance 、 setSubtitleTextColor 、 setSubtitleTextAppearance

    <FrameLayout xmlns:android="http://schemas.android.com/apk/res/android"  
        xmlns:toolbar="http://schemas.android.com/apk/res-auto" ...
        >  
        <android.support.v7.widget.Toolbar 
        ...  
            toolbar:logo="@mipmap/ic_launcher"  
            toolbar:title="Title"  
            toolbar:subtitle="Sub Title"  
            toolbar:titleTextColor="#ffffff">  
     </android.support.v7.widget.Toolbar>

[Android Toolbar样式定制详解] (http://blog.csdn.net/cnpath/article/details/47980871)   
https://github.com/oyjt/android-toolbar

[android：ToolBar详解（手把手教程）] (http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2014/1118/2006.html)   https://github.com/mosil/Android-Mosil-Sample-Toolbar

[Android 初识AppBarLayout 和 CoordinatorLayout](http://www.jianshu.com/p/ab04627cce58 https://github.com/Mike-bel/MDStudySamples)

