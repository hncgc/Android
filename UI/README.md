Android UI
===

[Android UI基本技术点](https://www.androidos.net.cn/article/fSJJNVeeqg.html)  

[安卓720*1280界面尺寸规范参考](https://www.25xt.com/appdesign/9712.html)  

[安卓1080P界面设计规范解读](https://www.25xt.com/appdesign/9487.html)  

[Android 应用项目工程规范](https://www.androidos.net.cn/article/fSxmyVeeqq.html)  

[app设计字体大小规范](https://www.25xt.com/guidelines/20689.html)  



Android 控件
===

[EditText](https://github.com/hncgc/Android/blob/master/UI/EditText.md)  

[WebView](https://github.com/hncgc/Android/blob/master/android/WebView.md)  

[Dialog](https://github.com/hncgc/Android/blob/master/UI/Dialog.md)  

[PopupWindow](https://github.com/hncgc/Android/blob/master/UI/PopupWindow.md)    

[SwitchCompat与Switch](https://github.com/hncgc/Android/blob/master/UI/SwitchCompat.md)  

[Android 自定义控件](https://github.com/hncgc/Android/blob/master/android/Android%E8%87%AA%E5%AE%9A%E4%B9%89%E6%8E%A7%E4%BB%B6.md)  


[Android 键盘](https://github.com/hncgc/Android/blob/master/android/Android%E9%94%AE%E7%9B%98.md)  




[Android ToolBar](https://github.com/hncgc/Android/blob/master/android/AndroidToolBar.md)  

[下拉刷新上拉加载](https://github.com/hncgc/Android/blob/master/android/%E4%B8%8B%E6%8B%89%E5%88%B7%E6%96%B0%E4%B8%8A%E6%8B%89%E5%8A%A0%E8%BD%BD.md)  

[底部菜单 & 头部导航栏](https://github.com/hncgc/Android/blob/master/android/%E5%BA%95%E9%83%A8%E8%8F%9C%E5%8D%95%26%E5%A4%B4%E9%83%A8%E5%AF%BC%E8%88%AA%E6%A0%8F.md)  

[Material Design](https://github.com/hncgc/Android/blob/master/android/MaterialDesign.md)  

[RecyclerView](https://github.com/hncgc/Android/blob/master/UI/RecyclerView.md)  

[下拉框](https://github.com/hncgc/Android/blob/master/UI/%E4%B8%8B%E6%8B%89%E6%A1%86.md)  

[ExpandableTextView](https://github.com/hncgc/Android/blob/master/UI/ExpandableTextView.md)  

----------------

[Tablayout使用全解，一篇就够了](https://www.jianshu.com/p/fde38f367019)  

[关于tablayout的tab点击事件](https://blog.csdn.net/wlxfxy/article/details/72820440)  

[TabLayout默认某个选项卡选中](https://blog.csdn.net/qq_29897079/article/details/77969617)  
~~~
tabLayout.getTabAt(postision).select(); //默认选中某项放在加载viewpager之后
~~~

[TabLayout设置下划线(Indicator)宽](https://blog.csdn.net/lmy820200104/article/details/79583924)  

[API 28下的TabLayout的差异](https://www.jianshu.com/p/cf4ed386efe9)  

[TabLayout的高级用法（自定义tab和修改指示器宽度）](https://blog.csdn.net/Jiang_Rong_Tao/article/details/85247988)  

---------------------

[Android布局中的空格以及占一个汉字宽度的空格的实现](https://blog.csdn.net/u014651216/article/details/52411113)  
~~~
空格：&#160;
窄空格：&#8201;
一个汉字宽度的空格：&#160;&#160;&#8201;【用两个空格（&#160;&#160;）占一个汉字的宽度时，两个空格比一个汉字略窄，三个空格（&#160;&#160;&#160;）比一个汉字略宽】

TextView实现首行缩进的方法：

在string资源文件中，在文字的前面加入”\u3000\u3000”即可实现首行缩进
在Java代码中，使用setText("\u3000\u3000"+xxxxx);
~~~

[Android TextView设置空格](https://blog.csdn.net/zhe_ge_sha_shou/article/details/80066954)  

[TextView设置行间距、行高，以及字间距](https://blog.csdn.net/shanshan_1117/article/details/79564271)  
~~~
设置行间距
1、android:lineSpacingExtra 设置行间距，如”10dp”。
2、android:lineSpacingMultiplier 设置行间距的倍数，如”1.5或者2″
3. android:lineSpacingExtra和android:lineSpacingMultiplier 
setLineSpacing (float add, float mult)
tv_textview.setLineSpacing(15,3);
设置字间距
android:textScaleX 水平方向放大
~~~



[ExpandableTextView——一个可折叠的Textview](https://blog.csdn.net/qq_37237245/article/details/73559055)

[android ExpandableTextView-自定义可以动态展开/收缩显示长文本的TextView](https://blog.csdn.net/yeah0126/article/details/52060210)  

[关于ExpandableTextView几点优化](https://www.jianshu.com/p/f5e5e579796f)  




[Android Study 之真正解决TextView字间距，那些扯淡的边儿去吧](https://blog.csdn.net/u012400885/article/details/71599497)  
https://github.com/HLQ-Struggle/TextViewSetWordSpace

[android:如何在TextView实现图文混排](https://blog.csdn.net/su20145104009/article/details/50667838)  

[Android TextView加载Html图文混排](https://blog.csdn.net/Vermouth_alone/article/details/76502302)  

[Android TextView使用HTML处理图片文字混合显示](https://blog.csdn.net/qq_36455052/article/details/78734734)  

[Android图文混排实现方式详解](https://blog.csdn.net/p19900618/article/details/78468025)  



----------------------



[Android-TextView 默认字体大小](https://blog.csdn.net/yanjunhui2011/article/details/72818237)  

源码中的textSize为15，单位是sp

[android改变全局字体大小](https://blog.csdn.net/apple_xiangsiyu/article/details/50896401)  

[填填Android lineSpacingExtra 的坑,解决行间距兼容性问题](https://blog.csdn.net/etwge/article/details/72818859)  

[android:textIsSelectable="true"引起的RecyclerView自动滚动问题](https://www.jianshu.com/p/4fbfd8442cbc)  

[控件的textIsSelectable属性引起的血案](https://www.cnblogs.com/epmouse/p/6857208.html)  
android中为了让控件上的文字可以选择复制，会加入
android:textIsSelectable="true"属性
但是假如你给这个控件设置了点击事件，你会发现第一次点击时，事件不会触发

[Android触摸事件（续）——点击长按事件](https://www.jianshu.com/p/f57bab1db012)  

[Android开发：在onTouchEvent中处理任意时间的长按事件](https://www.cnblogs.com/Free-Thinker/p/4795922.html)  

[Android onTouchEvent, onClick及onLongClick的调用机制](https://www.cnblogs.com/Free-Thinker/p/4795288.html)  

[Android Clipboard(复制/剪贴板)](https://www.cnblogs.com/exmyth/p/4603496.html)  

[设置点击效果foreground](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2017/1029/8655.html)  

~~~
            <RelativeLayout
                android:id="@+id/rl_password_management"
                android:layout_width="match_parent"
                android:layout_height="@dimen/px45"
                android:background="@color/white"
                
                android:foreground="@drawable/bg_ripple_themecolor"
                
                android:gravity="center_vertical"
                android:paddingLeft="@dimen/px14"
                android:paddingRight="@dimen/px14">
                
                
D:\App1\app\src\main\res\drawable\bg_ripple_themecolor.xml
<?xml version="1.0" encoding="utf-8"?>
<selector xmlns:android="http://schemas.android.com/apk/res/android">

    <item android:drawable="@color/color_6000" android:state_pressed="true"/>
    <item android:drawable="@color/transparent" android:state_pressed="false"/>

</selector>
~~~

[小Demo小知识-android:foreground与android:background](https://www.jianshu.com/p/b5ecd39ed494)  

---------------------

[Android之AutoCompleteTextView用法详解](https://www.jianshu.com/p/8b91cc1c0fd4)  

[AutoCompleteTextView](https://www.jianshu.com/p/aeae6a201a7b)  

[AutoCompleteTextView：自己主动完毕输入内容的控件（自己主动补全）](https://www.cnblogs.com/zsychanpin/p/7218369.html)  

[动态匹配输入内容AutoCompleteTextView](https://www.jianshu.com/p/300cd948001e)  

[Android UI系列-----EditText和AutoCompleteTextView](https://www.cnblogs.com/xiaoluo501395377/p/3411359.html)  

[Android中的AutoCompleteTextView的使用](https://www.cnblogs.com/wlming/p/5420133.html)  

[Android-使用AutoCompleteTextView进行动态匹配](https://blog.csdn.net/acm_th/article/details/50986569)  

[AutoCompleteTextView获取其内容](https://wang-peng1.iteye.com/blog/748061)  

[关于AutoCompleteTextView中调用setOnItemClickListener中参数调用介绍](https://bbs.csdn.net/topics/370231828)  

[自定义AutoCompleteTextView的点击事件]https://blog.csdn.net/jloveben/article/details/50494559()  

[AutoCompleteTextView监听器的一些用法](https://blog.csdn.net/qice675563721/article/details/22430467)  

[AutoCompleteTextView监听输入内容并显示](https://blog.csdn.net/u010002184/article/details/49886517)  


--------------------

[Android-StickyNavLayout 一个Android库用于创建可置顶的导航条](https://python.ctolib.com/hongyangAndroid-Android-StickyNavLayout.html)  

[悬浮导航栏StickyNavLayout的实现--基本滑动的实现](https://www.jianshu.com/p/e5ef7e36cbd3)  

[悬浮导航栏StickyNavLayout的实现--适配任意数据量](https://www.jianshu.com/p/daff3b4de3a4)  

[Android 实现酷炫的顶部栏](https://www.2cto.com/kf/201609/544183.html)  

[Android：下拉上滑显示与隐藏导航栏和状态栏](https://blog.csdn.net/u011343735/article/details/53761170)  

[Android实现上下滑动隐藏/显示工具栏](https://blog.csdn.net/futureshine1/article/details/50768735)  

[Android 底部导航栏动态显示和隐藏(上滑,下拉)](https://blog.csdn.net/xfhy_/article/details/78584459)  

[Android 动态隐藏显示导航栏，状态栏](https://blog.csdn.net/zhoumushui/article/details/51792568)  


[Android 沉浸式状态栏与隐藏导航栏](https://blog.csdn.net/Chen_xiaobao/article/details/80985923)  

[Android动态控制状态栏以及系统导航栏显示和隐藏](https://blog.csdn.net/Maiduoudo/article/details/77239557)  

[在Android 7.0隐藏导航栏和状态栏的一些方法](https://blog.csdn.net/maetelibom/article/details/78656021)  

[Android9.0 完全隐藏导航栏、状态栏](https://blog.csdn.net/u011386173/article/details/84104971)  

悬浮按钮
---

[android ——悬浮按钮及可交互提示](https://www.cnblogs.com/xxbbtt/p/7470287.html)  

[Android中FloatingActionButton实现悬浮按钮](https://www.jianshu.com/p/4ef788fe0624)  

[Android 可拖拽悬浮按钮](https://www.jianshu.com/p/ba3e5fc5cff1)  

[Android自定义可拖动的悬浮按钮](http://www.cnblogs.com/zhujiabin/p/9165641.html)  


--------------------

沉浸式状态栏
---

[Android适配---沉浸式状态栏](https://blog.csdn.net/black_bread/article/details/79832514)  

[Android 沉浸式状态栏完美解决方案](https://blog.csdn.net/u014418171/article/details/81223681)  

https://github.com/jgilfelt/SystemBarTint/blob/master/library/src/com/readystatesoftware/systembartint/SystemBarTintManager.java  

[android:fitsSystemWindows属性](https://blog.csdn.net/alex01550/article/details/86521132)  

[Android中fitsSystemWindows属性的用法总结](https://blog.csdn.net/baidu_32472003/article/details/79925766)  

[android沉浸式状态栏、fitsSystemWindows、标题栏折叠](https://blog.csdn.net/smileiam/article/details/61643006)  

[解决Android7.0下沉浸式状态栏变灰问题](https://blog.csdn.net/hmmhhmmhmhhm/article/details/77840604)  

[沉浸式状态栏--让你的状态栏和主题色一样](https://blog.csdn.net/wangye21323/article/details/79408435)  


[Android手机Rom类型判断的工具类](https://github.com/hncgc/Android/blob/master/android/Rom%E7%B1%BB%E5%9E%8B%E5%88%A4%E6%96%AD%E5%B7%A5%E5%85%B7%E7%B1%BB.md)  
---

[兼容4.x以上沉浸透明状态栏的 一个兼容类](https://github.com/hncgc/Android/blob/master/android/%E5%85%BC%E5%AE%B94%E4%BB%A5%E4%B8%8A%E6%B2%89%E6%B5%B8%E9%80%8F%E6%98%8E%E7%8A%B6%E6%80%81%E6%A0%8F%E5%85%BC%E5%AE%B9%E7%B1%BB)  
---


[Android状态栏适配，fitsSystemWindows分析](https://www.jianshu.com/p/353074f1d155)  


-------------------

[GitHub上受欢迎的Android UI Library](https://www.jianshu.com/p/da1ca645b95c)  
https://hndeveloper.github.io/2017/github-android-ui.html  

[Android开源项目库汇总](https://www.jianshu.com/p/86541dc33bc4)  


[NestedScrolling 嵌套滑动机制：简单实践（一）](https://blog.csdn.net/happy_horse/article/details/54619526)  

[如何避免在使用setNestedScrollingEnable(False)时阻止滚动本身？](https://cloud.tencent.com/developer/ask/60689)  






