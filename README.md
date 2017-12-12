
资源
---

百度云干货资源
http://blog.csdn.net/wcqwcq123/article/details/53408789

Android 免费学习
----------------

http://sem.shiguangkey.com/shiguang/it/android/pc/

java 下载
---------
http://www.oracle.com/technetwork/java/javase/downloads/index.html

Download IntelliJ IDEA
https://www.jetbrains.com/idea/download/?fromIDE=#section=windows

Android Studio 版本：3.0.0.18 发布日期：OCTOBER 25, 2017
http://www.android-studio.org/

博客精华
-------
【新版】Android技术博客精华汇总
http://www.apkbus.com/thread-313856-1-1.html

Code Review 
-----------
https://baike.baidu.com/item/Code%20Review/8466134?fr=aladdin

Code Review是轻量级代码评审

程序员必备的代码审查（Code Review）清单
http://blog.jobbole.com/83595/

从零开始Code Review
http://blog.csdn.net/uxyheaven/article/details/49773619

Markdown
--------
https://www.zybuluo.com/mdeditor

MarkdownView-Android
MarkdownView-Android是一个可以加载markdown或者普通文件并显示成html格式。
项目地址：https://github.com/mukeshsolanki/MarkdownView-Android

Material Design
---------------
Material Design 中文版
http://wiki.jikexueyuan.com/project/material-design/


baoyongzhang/android-PullRefreshLayout
https://github.com/baoyongzhang/android-PullRefreshLayout


Android中Activity与AppCompatActivity的理解
http://blog.csdn.net/wsdssss/article/details/51276379


有大量的Gson数据需要生成javaBean时，可以使用 GsonFormat插件，快速完成javaBean的生成。
[插件GsonFormat快速实现JavaBean](http://blog.csdn.net/dakaring/article/details/46300963)  


选择城市
--------
Android 类似美团的选择城市界面
http://blog.csdn.net/bruce_qiwei/article/details/73656964
新方案地址
https://github.com/qiwei0727/CityPicker
此框架引入了高德地图，建议将源码抽取出来，将地图SDK分离， 
 其他方面还不错。


【Android开源库】美团等APP城市选择
http://www.jianshu.com/p/b469c6f02754
https://github.com/zaaach/CityPicker

Android中使用开源框架citypickerview实现省市区三级联动选择   
http://blog.csdn.net/panhouye/article/details/60872318
https://github.com/crazyandcoder/citypicker

RxJava 创建操作符 timer与interval
http://blog.csdn.net/axuanqq/article/details/50687490

王学岗RxJava(十二)————————interval，timer，取消Observable
http://blog.csdn.net/qczg_wxg/article/details/53131146

开发框架
---
ZLayer Android企业级应用开发框架(直播代码版)
http://www.eoeandroid.com/thread-923392-1-1.html?_dsign=214604da
https://github.com/z-android/ZLayer

Android开源框架收集大全，包含描述和效果图
http://www.eoeandroid.com/thread-922412-1-1.html?_dsign=b3e2d5df
http://xybcoder.github.io/ANDROID/

DateTimePicker
--------------
日期选择部件(Google Agenda 的样式风格)
项目地址：https://github.com/flavienlaurent/datetimepicker

PickerView
------------
仿 iOS 的 PickerView 控件，有时间选择和选项选择并支持一二三级联动效果，TimePopupWindow 时间选择器，支持年月日时分，年月日，时分等格式；OptionsPopupWindow 选项选择器，支持一，二，三级选项选择，并且可以设置是否联动
项目地址：https://github.com/saiwu-bigkoo/Android-PickerView


其他  
---
Android UI 大全 里面包含所以特效大全的项目，都是每个特效一个项目的结构(https://gitee.com/bob4j/Android-UI)

[安卓巴士Android开发者门户](http://mp.sohu.com/profile?xpt=c29odW1wNDI3dXhwQHNvaHUuY29t)

Android开发之脚本替换PackageName
http://www.jianshu.com/p/dca9c323c686

关于Android SDK里的compileSdk、minSdk、targetSdk、buildTools、Tools、Platform-tools
http://www.jianshu.com/p/544d9f72883d



android砸金蛋
------------
http://download.csdn.net/download/wt0731/5009525

PayPal Android SDK 2.0 支付
http://blog.csdn.net/adongqin/article/details/38781329

PayPal Android SDK的接入和开发、与服务器对接IPN   
http://blog.csdn.net/carmideychen/article/details/72420467

引入SDK
compile('com.paypal.sdk:paypal-android-sdk:2.15.3')
 { exclude group:'io.card'}
exclude group:'io.card'表明不允许直接用卡支付，如果不添加这一行，在支付时用卡支付的按钮选项出现

算是目前PAYPAL最全最完整的开发方式了
http://blog.csdn.net/a53657561/article/details/64982411

一个多年安卓开发者的一些感悟与忠告
http://www.apkbus.com/blog-847095-72728.html

所有开源安卓app的列表
https://github.com/pcqpcq/open-source-android-apps

ProGuard代码混淆技术详解
http://www.cnblogs.com/cr330326/p/5534915.html

android-guidelines 代码风格
https://github.com/ribot/android-guidelines/blob/master/project_and_code_guidelines.md

ThinkAndroid
https://github.com/white-cat/ThinkAndroid


DataBinding初认识
http://www.apkbus.com/blog-927424-72831.html

安卓零基础
http://www.apkbus.com/misc.php?mod=tag&id=6169

技巧与经验
---
Android开发路上那些小技巧与经验，一起聚沙成塔！
http://www.apkbus.com/thread-463317-1-1.html

添加了全局的application文件一定要记得AndroidManifest里面注册一下。

全屏可以在配置文件里修改
android:theme="@android:style/Theme.NoTitleBar.Fullscreen"

也可以在setContentView(R.layout.main); 前设置：
getWindow().setFlags(WindowManager.LayoutParams.FLAG_FULLSCREEN,  
WindowManager.LayoutParams.FLAG_FULLSCREEN);

如何排除第三方传递依赖导致的aar冲突
开发过程中经常出现你需要依赖第三方的某个库,比如下面的代码所示：
dependencies {
          compile 'com.github.BolexLiu:PressScanCode:v1.0.0'
}
PressScanCode是一个长按扫描屏幕上的二维码工具库，他底层的二维码识别使用了zxing库。我们假设作者开发时使用了老版本zxing 1.0.1的版本。而我们集成进来以后却发现本身项目里也依赖Zxing 但是我们的版本是3.3.0的。由于包管理具有传递性。这时就会起冲突。gradle无法自己处理你到底是该依赖哪个。下面是处理办法。

dependencies {
    compile('com.github.BolexLiu:PressScanCode:v1.0.0'', {
       exclude group: 'com.google.zxing' //排除依赖
    })
  compile 'com.google.zxing:core:3.3.0'
}

这样做的意思排除PressScanCode原有的依赖。而选择依赖我们自己设定的3.3.0的zxing库

如何保持依赖最新的aar
这个相当容易，代码如下。你只需要将appcompat-v7:25.1.1这个版本好替换成“+”号即可每次都依赖最新的版本。
dependencies {
  // compile 'com.android.support:appcompat-v7:25.1.1'
    compile 'com.android.support:+'
｝

fragment里getActivity()空指针
重写fragment然后在onAttach方法存下一个Activity引用。在其他地方需用用到context或者Activity的时候使用该引用。而不使用getActivity()。可以规避这个问题。但请留意强引用可能会导致内存泄漏的问题。
protected Activity mActivity;
@Override
public void onAttach(Activity activity) {
    super.onAttach(activity);
    this.mActivity = activity;
}

代码new 出来的VIew没有ID
通常我们的VIew是通过布局文件依照@+id的方式在R文件中生成对映的一个Int值。这是用于运行时保证资源唯一性。但有一种情况，我们需要动态的在代码中new出一个VIew来。如果一个VIew还好。多个view的时，没有id会导致你不方便持有一个引用。那么可以 View的generateViewId() 方法来生成 id，让系统来保证唯一。而不是用随机数产生或者手写一个具体的值。注：API17++


不传递的方式巧取context
下面提供一种思路通过VIew直接获取context的api。特别是适配器中。别再传递这个对象了。注:从View上拿到的一定是Activity对象，但是如果你通过Service中或者Application中获取的Context是不能用做操作View的。本质区别就是抽象方法和对象是无法保证你要操作的具体对象是你要的对象(这句话没读懂的多读几遍，慢点读。说到底它就是依赖倒置原则问题)
View.getContext()  //任何被创建的VIEW都持有了context对象

不使用handle回到主线程（即UI线程）
通常我们使用Activity.runOnUiThread在子线程完成逻辑后更新UI。否则系统不会同意你在子线程中更新UI的。还有一种场景可以用下面的api
View.post(new Runnable() ) //同样可以切回UI线程执行。
当然现在Rxjava和EventBus可以完美的解决此类问题。我更推荐Rxjava。

防止VIew上信息被其他软件截屏或系统截图泄漏信息
在某些特殊的场景下，你的app可能和用户隐私有关系。如果需求需要禁止截图行为和覆盖你当前的Acitivity行为，可以使用 如下API。
getWindow().addFlags(WindowManager.LayoutParams.FLAG_SECURE)

想想实现禁止应用截屏，只需要一行代码，如下：
getWindow().addFlags(WindowManager.LayoutParams.FLAG_SECURE);
放置setContentView后即可


1.adapter里面的if判断,有if就一定要有else

2.使用后台返回数据,集合和对象使用前,记得要先判空

3.开发有比较复杂的业务逻辑时,先做设计再动手


很多小白还在为寻找各种应用中的图片而四处寻找，其实只需要在相应文件夹右键[New] >[Image Asset]即可打开AndroidStudio自带的图标生成器。

禁止输入特殊字符以及输入法表情，间接保护神一般后台。。。

    /**
     * 禁止输入表情以及特殊字符
     */
    public static class EmojiExcludeFilter implements InputFilter {
        @Override
        public CharSequence filter(CharSequence source, int start, int end, Spanned dest, int dstart, int dend) {
            for (int i = start; i < end; i++) {
                int type = Character.getType(source.charAt(i));
                if (type == Character.SURROGATE || type == Character.OTHER_SYMBOL) {
                    return "";
                }
            }
            String speChat = "[`~!@#$%^&*()+=|{}':;'\\[\\].<>/?~！@#￥%……&*（）——+|{}【】‘”“’？]";
            Pattern pattern = Pattern.compile(speChat);
            Matcher matcher = pattern.matcher(source.toString());
            if (matcher.find()) {
                return "";
            } else {
                return null;
            }
        }
    }

调用如下：

edtRemark.setFilters(new InputFilter[]{new UIHelper.EmojiExcludeFilter()});

Android Studio 使用
---

#### 快捷键：
    ctrl + o                        重写父类方法
    Alt+Inset                    get和set快捷键
    ctrl+shift+/                注释
    ctrl+shift+\                取消注释
    ctrl + alt + t                try catch快捷键
    Alt+Shift+↑                代码上衣一行
    Alt+Shift+↓                代码下移一行

#### 自动导包：
1 Android studio 只有import单个包的快捷键：Alt+Enter。没有Eclipse下的快速导入包的快捷键Ctrl+Shift+O。
2 但Android studio设置里有一项Auto Import自动导入功能。设置过程如下：
  Android studio --> File--> Settings --> Editor --> Auto Import:然后设置如下图。

  Add unambiguous imports on the fly：这个就是自动导入功能了，当你输入类名后，声明就被自动导入了

ArrayList<String> newList=new ArrayList<>(new TreeSet(strList));

去重 假设 strList里面有三个值 分别为：str1 str2 str1 

我们通过上面的代码 newList等于 str1 str2

#### git 操作：

强制push：
git push -u origin master -f

强制pull
git fetch --all  
git reset --hard origin/master 
git pull

Android Studio在线升级失败可以尝试用下面的方法离线升级。
Android Studio下载及离线升级方法
http://www.apkbus.com/blog-901770-72691.html


阅读器Read View

CodeView
CodeView 是一个能显示代码，并且能够进行代码高亮的一个控件。通过hightlight.js 渲染代码，可以自动识别主流的各种语言 比如java,c++,c#,python,bash,ruby等语言 并且有很多种主题风格，可以自由选择一种主题，然后将其显示。
CodeView  https://github.com/Thereisnospon/CodeView

AndroidPdfViewer
一个android版本的PDF阅读渲染器，可以用来阅读PDF文档。
项目地址：https://github.com/barteksc/AndroidPdfViewer


android-card-slide-panel
就是“探探”app实现的那种交互体验，为此我还特意下了一个探探体验了一下，卡片上展示的全是美女！左右拖动操作页非常nice，探探这个产品交互简直无可挑剔。
项目地址：https://github.com/xmuSistone/android-card-slide-panel

图片Image
---------
CircleImageView
一个非常漂亮的圆形ImageView，保持了ImageView的所有特性，可以像原生ImageView一样直接用Picasso加载图片展示。
项目地址：https://github.com/hdodenhof/CircleImageView

PhotoView
一个支持缩放功能的ImageView，通过多点触控或者双击都可以实现缩放效果。
项目地址：https://github.com/chrisbanes/PhotoView

rebound
Facebook出品，必属精品。这个库不是一个控件库，而是一个功能库，实现了点击图片，像按压弹簧一样的效果；点击图片之后，图片会先缩小，再放大，效果非常绚丽漂亮。
项目地址：http://facebook.github.io/rebound/

InstaCapture
这个库严格说起来和图片关系不大，这是一个强大的通过一行代码实现截屏的功能的库，而且可以指定当前activity截屏不包含哪些具体view组件，而且可以和当下流行的RXJava结合使用，非常简单易用，截屏之后的文件怎么处理就随便了，通常截屏文件我们还是要加载成位图显示的，所以先放在图片这里。
项目地址：https://github.com/tarek360/InstaCapture

PicassoFaceDetectionTransformation
这是一个和Picasso配合使用的图片剪裁库，特点就是自带面部识别，会把脸部剪裁到中间。
项目地址：https://github.com/aryarohit07/PicassoFaceDetectionTransformation

Luban
这又是一个功能库，实现高效率的无损图片压缩功能，作者对比了使用该库压缩和使用微信压缩的压缩比例，发现压缩效果和微信差不多！这是相当逆天的效果！有了这个库，其它的压缩库基本可以放一边了！
项目地址：https://github.com/Curzibn/Luban

Compressor
又一个无损图片压缩处理库，这个库可能没有上面那个库厉害，但是这个库可以和RXJava配合使用，实现处理链式化，所以如果是RXJava深度用户的话，可以去看看。
项目地址：https://github.com/zetbaitsu/Compressor


AndroidPhotoFilters
这叒是一个功能库，实现了灵活多样的滤镜效果，相当漂亮。
项目地址：https://github.com/Zomato/AndroidPhotoFilters?utm_campaign=explore-email&utm_medium=email&utm_source=newsletter&utm_term=weekly

MagicCamera
一个包含美颜等40余种实时滤镜的相机库，实现的是一个完整的照相机功能，可进行拍照、录像和图片修改。个人来说不喜欢这种杂合功能较多的库，我一向认为越小越精致，所以我一般不会使用这种库。但是可以学习里面的功能。
项目地址：https://github.com/wuhaoyu1990/MagicCamera

毛玻璃模糊效果Blur

Blurry
Blurry没什么好介绍的，看效果图就行。
项目地址：https://github.com/wasabeef/Blurry/raw/master/art/blurry.gif

ImageBlurring
ImageBlurring的特点是使用多种手段实现对图片的模糊处理，并比较了处理效率，可以了解使用哪种方式处理图片效率更高。
项目地址：https://github.com/qiujuer/ImageBlurring

图片裁剪

uCrop
uCrop这个项目的目标是：提供终极的、灵活的图片剪裁体验！听着就很厉害的样子，事实上也确实非常厉害，个人认为这应该是史上体验最好的剪裁库。
项目地址：https://github.com/Yalantis/uCrop

android-crop
android-crop看起来更像一个单纯的剪裁库，没有uCrop提供的那么多效果，但是就剪裁功能来说，还是很好的。
项目地址：https://github.com/jdamcd/android-crop

仿微信从文件系统加载图片

MultiImageSelector
MultiImageSelector是一个高仿微信朋友圈图片选择的功能库，提供多种选择，例如可以配置选单张还是多张，可以配置最多选几张，还可以配置是否显示拍照按钮等。
项目地址：https://github.com/lovetuzitong/MultiImageSelector

仿微博加载超长大图

LargeImage
LargeImage库，可以让你高清显示10000*10000像素的图片，轻松实现微博长图功能，怎么实现的也非常值得我们学习。
项目地址：https://github.com/LuckyJayce/LargeImage

加载动态图

GifView
GifView是一个可以播放GIF图片的自定义view，并且提供了开始／暂停／停止播放的功能。
项目地址：https://github.com/Cutta/GifView

GifImageView
GifImageView的特点是你可以针对每一帧进行操作，例如添加模糊效果等。
项目地址：https://github.com/felipecsl/GifImageView

其它黑科技
=========
android-shape-imageview
这个项目简直把ImageView玩坏了-_-#，可以把图片蹂躏成各种形状，然而项目中出了圆图和矩形／圆角矩形外，其它的基本用不到。
项目地址：https://github.com/siyamed/android-shape-imageview

FabricView
这个控件就相当于是一个playground，可以让人玩的很开心，你可以在上面写文本，加载图片，甚至可以在上面用手指乱写乱画，挺好玩呢！
项目地址：https://github.com/antwankakki/FabricView

SimpleTagImageView
这个库相对于上面的两个库，就正常了很多，也比较实用。实现的是给图片角上打倾斜的tag。
项目地址：https://github.com/wujingchao/SimpleTagImageView

MovingImageView
这个控件可以加载一个超出屏幕大小的图片，然后让这个图片在屏幕范围内四处逛荡，也比较实用。
项目地址：https://github.com/AlbertGrobas/MovingImageView

加载框LoadingView

Android-SpinKit
基于非常火爆的css库SpinKit实现的android加载库，动画效果非常棒。
项目地址：https://github.com/ybq/Android-SpinKit

LoadingDrawable
这个项目重要介绍一些酷炫的加载动画， 可以与任何View配合使用，作为加载动画或者Progressbar, 此外很适合与RecyclerRefreshLayout 配合使用作为刷新的loading 动画。
项目地址：https://github.com/dinuscxj/LoadingDrawable

LiquidButton
一个实现液体填充效果的加载提示view
项目地址：https://github.com/yoruriko/LiquidButton

LoadingView
哈哈，不多说，主要看动效，好看最重要。
项目地址：https://github.com/ldoublem/LoadingView

MetaballLoading
一个有贝塞尔曲线动画的加载提示框
项目地址：https://github.com/dodola/MetaballLoading

提示框Dialog
-----------
material-dialogs
一个简单易用的material风格的dialog
项目地址：https://github.com/afollestad/material-dialogs

sweet-alert-dialog
这个项目最后维护时间是两年前，现在可能都没人维护了，但是实现的效果还是挺好的
项目地址：[https://github.com/pedant/sweet-alert-dialog]](https://github.com/pedant/sweet-alert-dialog])

指示器Indicator
指示器用来提示用户当前操作到了哪一步。

StepView
提示操作步骤的巅峰之作，非常符合我的审美。
项目地址：https://github.com/baoyachi/StepView

stepper-indicator
一个和StepView差不多效果的步骤指示器。
项目地址：https://github.com/badoualy/stepper-indicator

SpringIndicator
一个切换使用了贝塞尔曲线的indicator，说实话作者给的示例图很丑，我不是很喜欢，但是我很喜欢贝塞尔曲线，所以这个也拿来放在这里，学习用，实际使用我还是会使用上面两个。
项目地址：https://github.com/chenupt/SpringIndicator

贝塞尔曲线
---------
BezierMaker
这个开源库演示了1-7阶贝塞尔曲线的形成过程，让我们直观的看到1-7阶贝塞尔曲线的形成动画，相当牛逼
项目地址：https://github.com/venshine/BezierMaker

Bubble-Notification
一个模仿qq未读消息小红点拖动消失效果的控件。
项目地址：https://github.com/dkmeteor/Bubble-Notification

DraggableFlagView
另一个模仿qq未读消息小红点拖动消失效果的控件。
项目地址：https://github.com/wangjiegulu/DraggableFlagView

BezierDemo
又一个模仿qq未读消息小红点拖动消失效果的控件。
项目地址：https://github.com/chenupt/BezierDemo

轻量级底部导航栏
http://www.apkbus.com/thread-463190-1-1.html
源码地址 https://github.com/chaychan/BottomBarLayout


android企业级商城源码
http://www.apkbus.com/thread-462905-1-1.html

《Android 使用RecyclerView实现（仿微信）的联系人A-Z字母排序和过滤搜索功能》 
http://blog.csdn.net/silenceoo/article/details/75661590
一个快速跳跃分组的侧边栏控件，示例中配合RecyclerView实现
https://github.com/Solartisan/WaveSideBar

RecyclerView实现顶部悬浮、字母排序、过滤搜索最优雅的方式
http://blog.csdn.net/silenceoo/article/details/77839683
http://www.apkbus.com/thread-462455-1-1.html
https://github.com/xupeng92/SortRecyclerviewList

PinyinUtils
将中文转化为拼音的工具类
--------------------------

Android编辑信息界面，组合控件的封装
http://www.jianshu.com/p/cde81809c24a
https://github.com/zhouxu88/ItemGroup

介绍几个工作开发中封装的好用的android自定义控件
http://www.cnblogs.com/Jaylong/p/3641027.html
下载地址：http://www.eoeandroid.com/forum.php?mod=attachment&aid=MTIwMDM1fDM5NTYzZjQ3fDEzOTY0Mjc4NDF8NzU4MzI1fDMyODQyNw%3D%3D

JAVA replaceAll 正则表达式(
http://blog.csdn.net/s445320/article/details/50729736

Java 正则表达式
http://www.runoob.com/java/java-regular-expressions.html

android photoview 图片放大缩放功能 ImageView
http://blog.csdn.net/aaawqqq/article/details/43128111
https://github.com/chrisbanes/PhotoView

oschina-app源码解析-webview重组html
http://blog.csdn.net/xiangxue336/article/details/20062347

Android实现点击WebView界面中图片滑动浏览与保存图片功能
http://www.jb51.net/article/112028.htm

从WebView中点击一张图片，转换成一个可缩放，可旋转的图片。
http://www.jianshu.com/p/e24ee6d67f01

https://segmentfault.com/t/android

http://code.taobao.org/p/YuanWen/src/trunk/

阿里云开源项目
-------------
http://code.taobao.org/project/explore/ 
http://code.taobao.org/newest/

http://code.taobao.org/p/YuanWen/diff/66/trunk/app/src/main/java/com/smile/yuanwen/fragment/DynamicDetailFragment.java

+
+    /**
+     * 填充webview内容
+     */
+    private void fillWebViewBody() {
+        StringBuffer body = new StringBuffer();
+        body.append(ThemeSwitchUtils.getWebViewBodyString());
+        body.append(UIHelper.WEB_STYLE + UIHelper.WEB_LOAD_IMAGES);
+
+        StringBuilder tweetbody = new StringBuilder(mDynamic.getBody());
+
+        String tweetBody = TextUtils.isEmpty(mDynamic.getImgSmall()) ? tweetbody
+                .toString() : tweetbody.toString() + "<br/><img src=\""
+                + mDynamic.getImgSmall() + "\">";
+        body.append(setHtmlCotentSupportImagePreview(tweetBody));
+
+        UIHelper.addWebImageShow(getActivity(), mContent);
+        // 封尾
+        body.append("</div></body>");
+        mContent.loadDataWithBaseURL(null, body.toString(), "text/html",
+                "utf-8", null);
+    }
+
+    /**
+     * 添加图片放大支持
+     *
+     * @param body
+     * @return
+     */
+    private String setHtmlCotentSupportImagePreview(String body) {
+        // 过滤掉 img标签的width,height属性
+        body = body.replaceAll("(<img[^>]*?)\\s+width\\s*=\\s*\\S+", "$1");
+        body = body.replaceAll("(<img[^>]*?)\\s+height\\s*=\\s*\\S+", "$1");
+        return body.replaceAll("(<img[^>]+src=\")(\\S+)\"",
+                "$1$2\" onClick=\"javascript:mWebViewImageListener.showImagePreview('"
+                        + mDynamic.getImgBig() + "')\"");
+    }
+


android 动态添加view
--------------------------

Android 在程序中动态添加 View 布局或控件
http://blog.csdn.net/q610098308/article/details/49998457
http://blog.csdn.net/a15838319826/article/details/70808771

有时我们需要在程序中动态添加布局或控件等，下面用程序来展示一下相应的方法：
1、addView
添加View到布局容器
2、removeView
在布局容器中删掉已有的View
3、LayoutParams 
设置View的大小位置

Android在布局中动态添加view的两种方法
https://www.2cto.com/kf/201407/314958.html
添加视图文件的时候有两种方式:1、通过在xml文件定义layout；2、java代码编写

1.构造xml文件

2.LayoutInflater

提到addview，首先要了解一下LayoutInflater类。这个类最主要的功能就是实现将xml表述的layout转化为View的功能。为了便于理解，我们可以将它与findViewById()作一比较，二者都是实例化某一对象，不同的是findViewById()是找xml布局文件下的具体widget控件实例化，而LayoutInflater找res/layout/下的xml布局文件来实例化的。

(1)创建

LayoutInflater inflater=(LayoutInflater)context.getSystemService(Context.LAYOUT_INFLATER_SERVICE);或

LayoutInflater inflater = LayoutInflater.from(Activity.this);或

LayoutInflater inflater = getLayoutInflater();

这三种方法本质是相同的。

(2)inflate()

用LayoutInflater.inflate() 将LayOut文件转化成VIew。

View view = inflater.inflate(R.layout.block_gym_album_list_item, null);

3.添加视图文件

三、步骤
1、通过在xml文件定义layout(block_gym_album_list_item.xml)

block_gym_album_list_item.xml

<!--?xml version="1.0" encoding="utf-8"?-->
<linearlayout xmlns:android="https://schemas.android.com/apk/res/android" 
    xmlns:core="https://schemas.android.com/apk/res/com.gxtag.gym"
    android:layout_width="fill_parent"
    android:layout_height="fill_parent"
    android:orientation="vertical"
    android:padding="5dp">
 
    <imageview 
        android:id="@+id/iv_head_album"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:src="@drawable/defaulthead">
 
    </imageview>
</linearlayout>


main.xml

<!--?xml version="1.0" encoding="utf-8"?-->
<linearlayout xmlns:android="https://schemas.android.com/apk/res/android"
    android:id="@+id/ll_parent"
    android:layout_width="fill_parent"
    android:layout_height="wrap_content"
    android:orientation="vertical">
 
    <include
        android:layout_width="fill_parent"
        android:layout_height="wrap_content"
        layout="@layout/block_head_back">
 
    </include>
</linearlayout>

DynamicViewActivity.java

package com.gxtag.gym.ui;
 
import android.app.Activity;
import android.content.Context;
import android.os.Bundle;
import android.view.LayoutInflater;
import android.view.View;
import android.view.View.OnClickListener;
import android.view.ViewGroup;
import android.widget.LinearLayout;
import android.widget.LinearLayout.LayoutParams;
import android.widget.TextView;
 
import com.gxtag.gym.R;
import com.icq.app.widget.StatedButton;
 
public class DynamicViewActivity extends Activity implements OnClickListener{
 
    private Context mContext;
    private TextView mTv_title;
    private String title = "动态添加布局";
    private StatedButton mSbtn_back;
    private LinearLayout mLl_parent;
 
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_dynamic);
        mContext=this;
        initView();
        mLl_parent.addView(addView1());
        mLl_parent.addView(addView2());
 
    }
     
    private void initView() {
        // TODO 初始化视图
        mLl_parent=(LinearLayout) findViewById(R.id.ll_parent);
        mTv_title = (TextView) findViewById(R.id.tv_title);
        mTv_title.setText(String.format(String.format(
                getResources().getString(R.string.title), title)));
        mSbtn_back = (StatedButton) findViewById(R.id.sbtn_navback);
        mSbtn_back.setOnClickListener(this);
         
         
    }
     
    private View addView1() {
        // TODO 动态添加布局(xml方式)
        LinearLayout.LayoutParams lp = new LinearLayout.LayoutParams( 
                    LayoutParams.FILL_PARENT, LayoutParams.WRAP_CONTENT); 
//      LayoutInflater inflater1=(LayoutInflater)mContext.getSystemService(Context.LAYOUT_INFLATER_SERVICE);
//      LayoutInflater inflater2 = getLayoutInflater();
        LayoutInflater inflater3 = LayoutInflater.from(mContext);
        View view = inflater3.inflate(R.layout.block_gym_album_list_item, null);
        view.setLayoutParams(lp);
        return view;
         
    }
     
    private View addView2() {
        // TODO 动态添加布局(java方式)
        LinearLayout.LayoutParams lp = new LinearLayout.LayoutParams( 
                    LayoutParams.FILL_PARENT, LayoutParams.WRAP_CONTENT); 
        LinearLayout view = new LinearLayout(this); 
        view.setLayoutParams(lp);//设置布局参数 
        view.setOrientation(LinearLayout.HORIZONTAL);// 设置子View的Linearlayout// 为垂直方向布局 
        //定义子View中两个元素的布局 
        ViewGroup.LayoutParams vlp = new ViewGroup.LayoutParams( 
                ViewGroup.LayoutParams.WRAP_CONTENT, 
                ViewGroup.LayoutParams.WRAP_CONTENT); 
        ViewGroup.LayoutParams vlp2 = new ViewGroup.LayoutParams( 
                ViewGroup.LayoutParams.WRAP_CONTENT, 
                ViewGroup.LayoutParams.WRAP_CONTENT); 
          
        TextView tv1 = new TextView(this); 
        TextView tv2 = new TextView(this); 
        tv1.setLayoutParams(vlp);//设置TextView的布局 
        tv2.setLayoutParams(vlp2); 
        tv1.setText("姓名:"); 
        tv2.setText("李四"); 
        tv2.setPadding(calculateDpToPx(50), 0, 0, 0);//设置边距 
        view.addView(tv1);//将TextView 添加到子View 中 
        view.addView(tv2);//将TextView 添加到子View 中 
        return view; 
    }
 
    private int calculateDpToPx(int padding_in_dp){ 
        final float scale = getResources().getDisplayMetrics().density; 
        return  (int) (padding_in_dp * scale + 0.5f); 
    } 
     
 
    @Override
    public void onClick(View v) {
        // TODO 控件单击事件
        switch (v.getId()) {
        case R.id.sbtn_navback:
            this.finish();
            break;
        default:
            break;
        }
    }
 
}

ANDROID 实现布局动态加载
--------------------------
http://www.cnblogs.com/Greenwood/archive/2011/03/02/1969340.html


android design library提供的TabLayout的用法
http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/0731/3247.html

Android开发之设置TabLayout下方下划线的宽度
http://blog.csdn.net/sheajin/article/details/59104205

Design库-TabLayout属性详解
http://www.jianshu.com/p/2b2bb6be83a8
在清单文件中设置如下代码即可：

android:theme="@style/Theme.AppCompat"

TabLayout用法详解及自定义样式
http://www.jb51.net/article/101912.htm

TabLayout高端用法（一）
http://www.jianshu.com/p/be1e8a1da639?nomobile=yes

Android图片加载框架Glide用法
http://www.cnblogs.com/guilin-hu/p/5706916.html
图片的缩放，centerCrop()和fitCenter()： 
1)使用centerCrop是利用图片图填充ImageView设置的大小，如果ImageView的Height是match_parent则图片就会被拉伸填充

Glide.with(context).load(imageUrl).centerCrop().into(imageView);
2)使用fitCenter即缩放图像让图像都测量出来等于或小于 ImageView 的边界范围,该图像将会完全显示，但可能不会填满整个ImageView。

Glide.with(context).load(imageUrl).fitCenter().into(imageView);

RxBus
---
Android之RxBus详解
http://blog.csdn.net/caben_/article/details/52786184



lambda
---
Java 8 Lambda表达式探险
http://www.cnblogs.com/feichexia/archive/2012/11/15/Java8_LambdaExpression.html

在Android上使用Lambda表达式 - retrolambda插件
http://blog.csdn.net/codezjx/article/details/51327164

Volley源码分析
http://bxbxbai.github.io/2014/12/24/read-volley-source-code/
Android库Volley的使用介绍
http://bxbxbai.github.io/2014/09/14/android-working-with-volley/

Android Butterknife 8.4.0 使用方法总结
http://www.apkbus.com/blog-822715-64244.html
https://github.com/JakeWharton/butterknife

漂亮的滑动效果
http://www.apkbus.com/thread-273921-1-1.html
https://github.com/Sherchen/SlideToggleHeader

Android App内部更新Library
http://www.apkbus.com/thread-273464-1-1.html
https://github.com/MZCretin/AutoUpdateProject


Scala社区
http://www.scalachina.com/

Scala 函数式程序设计原理
https://www.coursera.org/specializations/scala

Groovy
http://baike.baidu.com/link?url=OJLu44SO9onNCWpsm7zl_uDGWYvnK-M_e0PmUB6g_FgBVj153PeYvSslVfU6HDOq8rhT04M5ujLRjSXtQqiRhq

Android 软键盘监听事件
http://blog.csdn.net/breeze666/article/details/27082419

Android windowSoftInputMode软键盘显示和隐藏的监听和实现
http://blog.csdn.net/u010852801/article/details/43198313


Android studio 之ANalyze 清理无用资源
http://blog.csdn.net/qulonglong110/article/details/51911261

android之as自动化删除无用资源为apk瘦身
http://blog.csdn.net/zhongwn/article/details/52769927

如何获取Android唯一标识（唯一序列号）
http://blog.csdn.net/ljz2009y/article/details/22895297


彻底解决Android 应用方法数不能超过65K的问题
http://www.itnose.net/detail/6168594.html

Android开发方法数超过64k（65k）解决办法
http://www.jianshu.com/p/271668909cc6

List of Android UI/UX Libraries
https://github.com/wasabeef/awesome-android-ui

PhotoUpload
-----------
http://www.cnblogs.com/zhuyuliang/

Android - Camera
http://www.tutorialspoint.com/android/android_camera.htm

Android文件图片上传的详细讲解（一）HTTP multipart/form-data 上传报文格式实现手机端上传
http://topmanopensource.iteye.com/blog/1605238

Android SnackBar
http://blog.csdn.net/jdsjlzx/article/details/46892363
还在用Toast？你Out啦，试试Snackbar吧！
http://www.tuicool.com/articles/BfEbMvB
-------------------------
Android开发：Android studio 无法在可视化页面预览XML布局文件以及丢失R文件
http://blog.csdn.net/chentravelling/article/details/51316235

android studio预览视图时报错
http://www.cnblogs.com/xiaomoxian/p/5291579.html
你将右上角哪个 23改成其它你有的sdk,如22，可能就可以了。有可能是sdk升级的问题；

android studio 无法在可视化页面预览布局文件
把你的style文件中theme改一下
在Theme.AppCompat.Light.DarkActionBar前面加上Base.  如下
<!-- Base application theme. -->
<style name="AppTheme" parent="Base.Theme.AppCompat.Light.DarkActionBar">    
<!-- Customize your theme here. --></style>

Build.VERSION.SDK_INT
http://aijiawang-126-com.iteye.com/blog/1481572

Android.os包中一些类的使用
http://www.linuxidc.com/Linux/2011-11/48325.htm

添加相机的外部启用MediaStore.ACTION_IMAGE_CAPTURE
http://blog.csdn.net/wop_niaoren19870227/article/details/6531095

Java数组String []的用法详解
http://blog.csdn.net/cation/article/details/4387857/


MessageDigest简介
http://blog.csdn.net/hudashi/article/details/8394158

Java 自带的加密类MessageDigest类（加密MD5和SHA）
http://www.tuicool.com/articles/nMNVVj

StringUtils工具类的常用方法
http://www.tuicool.com/articles/am2u6fm

chrome网上商店
https://chrome.google.com/webstore/search/postman?hl=zh-CN

Postman
http://chromecj.com/web-development/2014-09/60.html
Postman是一款功能强大的网页调试与发送网页HTTP请求的Chrome插件。

Android 百分比布局库(percent-support-lib) 解析与扩展
http://blog.csdn.net/lmj623565791/article/details/46695347
compile 'com.android.support:percent:22.2.0'

Android 增强版百分比布局库 为了适配而扩展
http://blog.csdn.net/lmj623565791/article/details/46767825

開源安卓 https://www.gitbook.com/book/yongjhih/feed/details
https://github.com/yongjhih/android-gitbook/


Android 程序框架设计
http://itindex.net/detail/44207-android-程序-框架

开发中所遇问题归纳
http://www.apkbus.com/blog-719059-62993.html

优秀的（Android）软件工程师是如何练成的
http://mp.weixin.qq.com/s/NWM-OKuKCyHTlXc32h39uA

Android 知识梳理
https://gold.xitu.io/post/587dbaf9570c3522010e400e


android webview里设置cookie
http://blog.csdn.net/encienqi/article/details/7912733

[Android] WebView删除缓存
http://blog.csdn.net/s278777851/article/details/6534316
1.删除保存于手机上的缓存.
	// clear the cache before time numDays
	private int clearCacheFolder(File dir, long numDays) {
		int deletedFiles = 0;
		if (dir!= null && dir.isDirectory()) {
			try {
				for (File child:dir.listFiles()) {
					if (child.isDirectory()) {
						deletedFiles += clearCacheFolder(child, numDays);
					}
					if (child.lastModified() < numDays) {
						if (child.delete()) {
							deletedFiles++;
						}
					}
				}
			} catch(Exception e) {
				e.printStackTrace();
			}
		}
		return deletedFiles;
	}

com.pccb.app.ui.webview.OpenWebActivity.class

	@Override
	protected void onDestroy() {
		super.onDestroy();
		////删除此时之前的缓存
		clearCacheFolder(OpenWebActivity.this.getCacheDir(), System.currentTimeMillis());
	}

2. 打开关闭使用缓存：

    优先使用缓存，WebView.getSettings().setCacheMode(WebSettings.LOAD_CACHE_ELSE_NETWORK);

    不使用缓存，WebView.getSettings().setCacheMode(WebSettings.LOAD_NO_CACHE);


Android Webview清除缓存和Cookie
http://blog.csdn.net/ronaldong99/article/details/40392847

Android 动态切换全屏和非全屏模式
http://blog.csdn.net/michaelpp/article/details/7302308
	/**
	 * 动态切换全屏和非全屏模式
	 * @param isFulllScreen
	 *      2017-01-22
     */
	public void setFulllScreen(boolean isFulllScreen){
		WindowManager.LayoutParams params = getWindow().getAttributes();
		if (isFulllScreen) {
			params.flags |= WindowManager.LayoutParams.FLAG_FULLSCREEN;
			getWindow().setAttributes(params);
			getWindow().addFlags(WindowManager.LayoutParams.FLAG_LAYOUT_NO_LIMITS);
		} else {
			params.flags &= (~WindowManager.LayoutParams.FLAG_FULLSCREEN);
			getWindow().setAttributes(params);
			getWindow().clearFlags(WindowManager.LayoutParams.FLAG_LAYOUT_NO_LIMITS);
		}
	}



android图片缓存框架
---
开源选型之Android三大图片缓存原理、特性对比
http://www.csdn.net/article/2015-10-21/2825984

聊聊Android优秀的图片加载缓存的开源框架？UIL、Glide、Picasso
http://www.cnblogs.com/xianglinglong/p/5578466.html

Android四大图片缓存框架之-Fresco（一）
http://blog.csdn.net/qq_21430549/article/details/49338547

Android四大图片缓存框架之-Fresco之initialize（二）
标签： android框架图片缓存
http://blog.csdn.net/qq_21430549/article/details/49387741

Android 四大缓存框架之-Universal-Image-Loade
http://blog.csdn.net/qq_21430549/article/details/49405115
DisplayOption参数的配置
default_options = new DisplayImageOptions.Builder()
                /**
                 * 这只Uri为空、加载失败、加载时候的图片资源，可以接受Drawable 和 资源ID
                 */
                .showImageForEmptyUri(R.mipmap.ic_launcher)
                .showImageOnFail(R.mipmap.ic_launcher)
                .showImageOnLoading(R.mipmap.ic_launcher)
                //是否设置在加载之前重置view
                .resetViewBeforeLoading(false)

                .delayBeforeLoading(1000)
                //是否缓存在内存中
                .cacheInMemory(false)
                //是否缓存在文件中
                .cacheOnDisk(false)
//                .preProcessor(...)
//                .postProcessor(...)
//                .extraForDownloader(...)
                .considerExifParams(false)
                //Image的缩放类型
                .imageScaleType(ImageScaleType.IN_SAMPLE_POWER_OF_2)
                //bitmap 的config
                .bitmapConfig(Bitmap.Config.ARGB_8888)
                //decode参数
//                .decodingOptions()
                //设置显示，可以设置为圆角
                .displayer(new SimpleBitmapDisplayer())
                .handler(new Handler())
                .build();

根据自己的需求设置就好，比如说我这里想设置圆角怎么办
head_options = new DisplayImageOptions.Builder()
                .showStubImage(R.mipmap.ic_launcher)
                .showImageOnFail(R.mipmap.ic_launcher)
                .showImageForEmptyUri(R.mipmap.ic_launcher)
                //设置圆角显示
                .displayer(new RoundedBitmapDisplayer(50))
                .cacheOnDisk(true)
                .cacheInMemory(true)
                .build();

Android开源框架ImageLoader的完美例子
http://www.cnblogs.com/zgz345/p/3502315.html
很完善的一个例子下载地址：http://download.csdn.net/detail/wwj_748/5975847
        // 使用DisplayImageOptions.Builder()创建DisplayImageOptions  
        options = new DisplayImageOptions.Builder()  
            .showStubImage(R.drawable.ic_stub)          // 设置图片下载期间显示的图片  
            .showImageForEmptyUri(R.drawable.ic_empty)  // 设置图片Uri为空或是错误的时候显示的图片  
            .showImageOnFail(R.drawable.ic_error)       // 设置图片加载或解码过程中发生错误显示的图片      
            .cacheInMemory(true)                        // 设置下载的图片是否缓存在内存中  
            .cacheOnDisc(true)                          // 设置下载的图片是否缓存在SD卡中  
            .displayer(new RoundedBitmapDisplayer(20))  // 设置成圆角图片  
            .build();                                   // 创建配置过得DisplayImageOption对象  

Android四大图片缓存框架之-Picasso和Glide
http://blog.csdn.net/qq_21430549/article/details/49406575
Gilde：gGithub地址  https://github.com/bumptech/glide   用法: Google推荐的图片加载库Glide介绍 http://jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/0327/2650.html
Picasso Github地址 http://square.github.io/picasso/#features  用法: Android图片下载缓存库picasso解析 http://blog.csdn.net/xu_fu/article/details/17043231



使用AndroidStudio分析和解决ImageLoader引起内存泄露问题
http://blog.csdn.net/editor1994/article/details/50394560

UniversalImageLoader源码解读01-用来显示图片的ImageAware
http://blog.csdn.net/mtaxot/article/details/51375332

UniversalImageLoader源码解读02-图片处理和显示
http://blog.csdn.net/mtaxot/article/details/51376242

UniversalImageLoader源码解读03-一些无关紧要的小类
http://blog.csdn.net/mtaxot/article/details/51376865

UniversalImageLoader源码解读04-内存缓存
http://blog.csdn.net/mtaxot/article/details/51377287

UniversalImageLoader源码解读05-磁盘缓存
http://blog.csdn.net/mtaxot/article/details/51377546

UniversalImageLoader源码解读06-任务调度
http://blog.csdn.net/mtaxot/article/details/51381325

UniversalImageLoader源码解读07-内存泄漏和bug
http://blog.csdn.net/mtaxot/article/details/51383991

imageloader加载图片的内存泄露问题
http://tieba.baidu.com/p/3850014474

android 大量图片加载导致的内存问题
https://segmentfault.com/q/1010000004121952?_ea=497717

http://www.bootcss.com/

自己开发的Android APP消耗流量过多，如何解决？
http://bbs.csdn.net/topics/390790742

安卓居然比苹果更费流量?轻松几招教你如何节省流量
http://www.360doc.com/content/16/0404/22/11613470_547885459.shtml

Android 开源框架Universal-Image-Loader完全解析（一）--- 基本介绍及使用
http://blog.csdn.net/xiaanming/article/details/26810303/
https://github.com/nostra13/Android-Universal-Image-Loader

Android 开源框架Universal-Image-Loader完全解析（二）--- 图片缓存策略详解
http://blog.csdn.net/xiaanming/article/details/27525741

Android 图片缓存处理
http://blog.csdn.net/weiyidemaomao/article/details/21237833

Universal-Image-Loader（android图片缓存）
http://blog.csdn.net/liu1164316159/article/details/38728259

android universal-image-loader disk 缓存 存在本地什么位置
https://zhidao.baidu.com/question/1306133363278940059.html

Markdown Navigator
IntelliJ IDEA Multi-MarkDown插件安装破J全过程
http://www.jianshu.com/p/a0550f81cbd1
简单理解就是用来写文章排版的，一般 github 上面的项目默认都有一个 readme.md 文件（以".md"结尾来描述项目的说明文档）。本文就是使用简书的 markdown 语法写的。

原生Android结合H5混合开发小结
http://blog.csdn.net/leaf_130/article/details/54099173

CentOS 上的FireWallD简明指南
http://www.51xdn.net/czxt/Linux/20170109/43978.html

Jade —— 源于 Node.js 的 HTML 模板引擎
https://segmentfault.com/a/1190000000357534


@NotEmpty、@NotBlank、@NotNull的区别
http://blog.csdn.net/zz_life/article/details/51470909
@NotNull和@NotEmpty和@NotBlank区别
http://blog.csdn.net/melenpeng/article/details/50236449

Java中避免NullPointerException的一些方法
https://segmentfault.com/a/1190000002477715


Android SDK加载图片流程
-----------------------
Android SDK会根据屏幕密度自动选择对应的资源文件进行渲染加载，比如说，SDK检测到你手机的分辨率是xhdpi，会优先到xhdpi文件夹下找对应的图片资源;
如果xhdpi文件夹下没有图片资源，那么就会去分辨率高的文件夹下查找，比如xxhdpi，直到找到同名图片资源，将它按比例缩小成xhpi图片;
如果往上查找图片还是没有找到，那么就会往低分辨率的文件夹查找，比如hdpi，直到找到同名图片资源，将它按比例放大成xhpi图片。
根据加载图片的流程，可以得出理论上提供一套图片就可以了。

那么应该提供哪种分辨率规格呢?

原则上越高越好，同时结合当前主流分辨率屏幕

weight的计算
宽度 = 原来宽度 + 权重比值 * 剩余宽度
当layout_width为0dp，layout_weight分别是1和2
<LinearLayout 
      android:layout_width="match_parent" 
      android:layout_height="wrap_content" 
      android:orientation="horizontal"> 
 
      <Button 
          android:layout_width="0dp" 
          android:layout_height="wrap_content" 
          android:layout_weight="1" 
          android:text="weight = 1"/> 
 
      <Button 
          android:layout_width="0dp" 
          android:layout_height="wrap_content" 
          android:layout_weight="2" 
          android:text="weight = 2"/> 
  </LinearLayout>  
第一个按钮：宽度 = 0 + 1/3 * 屏宽 = 1/3屏宽
第二个按钮：宽度 = 0 + 2/3 * 屏宽 = 2/3屏宽

当layout_width为match_parent, layout_weight分别是1和2
<LinearLayout 
      android:layout_width="match_parent" 
      android:layout_height="wrap_content" 
      android:orientation="horizontal"> 
 
      <Button 
          android:layout_width="match_parent" 
          android:layout_height="wrap_content" 
          android:layout_weight="1" 
          android:text="weight = 1"/> 
 
      <Button 
          android:layout_width="match_parent" 
          android:layout_height="wrap_content" 
          android:layout_weight="2" 
          android:text="weight = 2"/> 
  </LinearLayout>  

第一个按钮：宽度 = 屏宽 + 1/3 (屏宽 - 2 屏宽) = 2/3屏宽
第二个按钮：宽度 = 屏宽 + 2/3 (屏宽 - 2 屏宽) = 1/3屏宽
布局使用
使用相对布局，禁用绝对布局。

屏幕适配之百分比布局
<?xml version="1.0" encoding="utf-8"?> 
  <android.support.percent.PercentRelativeLayout 
      xmlns:android="http://schemas.android.com/apk/res/android" 
      xmlns:app="http://schemas.android.com/apk/res-auto" 
      android:layout_width="match_parent" 
      android:layout_height="wrap_content"> 
 
      <Button 
          android:layout_width="0dp" 
          android:layout_height="wrap_content" 
          android:text="30%" 
          app:layout_widthPercent="30%"/> 
 
      <Button 
          android:layout_width="0dp" 
          android:layout_height="wrap_content" 
          android:layout_alignParentRight="true" 
          android:text="20%" 
          app:layout_widthPercent="20%"/> 
 
  </android.support.percent.PercentRelativeLayout>  

--------------------------------------------------------------

java中比较两个double类型的数据的大小
http://dagmom.iteye.com/blog/1616867
import java.math.BigDecimal;
public class DoubleCompare {
public String compare(BigDecimal val1, BigDecimal val2) {
    String result = "";
    if (val1.compareTo(val2) < 0) {
        result = "第二位数大！";
    }
    if (val1.compareTo(val2) == 0) {
        result = "两位数一样大！";
    }
    if (val1.compareTo(val2) > 0) {
        result = "第一位数大！";
    }
    return result;
}
public static void main(String[] args) {
    double a = 0.01;
    double b = 0.001;
    BigDecimal data1 = new BigDecimal(a);
    BigDecimal data2 = new BigDecimal(b);
    System.out.print(new DoubleCompare().compare(data1, data2));
}
}

将此 BigDecimal 与指定的 BigDecimal 比较。根据此方法，值相等但具有不同标度的两个 BigDecimal 对象（如，2.0 和 2.00）被认为是相等的。相对六个 boolean 比较运算符 (<, ==, >, >=, !=, <=) 中每一个运算符的各个方法，优先提供此方法。建议使用以下语句执行上述比较：(x.compareTo(y) <op> 0)，其中 <op> 是六个比较运算符之一。
指定者：
接口 Comparable<BigDecimal> 中的 compareTo
参数：
val - 将此 BigDecimal 与之比较的 BigDecimal。
返回：
当此 BigDecimal 在数字上小于、等于或大于 val 时，返回 -1、0 或 1。


Android 中中 String 资源文件的 format 方法方法
例一: 整数型的
<string name="alert">I am %1$d years old</string> 定义的是这样的

int nAge=23;
String sAgeFormat = getResources().getString(R.string.alert);
String sFinalAge = String.format(sAgeFormat, nAge); 


java string 去掉html标签
-----------------------
java 去掉html标签
http://www.cnblogs.com/newsouls/p/3995394.html
import java.util.regex.Matcher; 
import java.util.regex.Pattern; 

public class HTMLSpirit{ 
    public static String delHTMLTag(String htmlStr){ 
        String regEx_script = "<script[^>]*?>[\\s\\S]*?<\\/script>"; //定义script的正则表达式 
        String regEx_style = "<style[^>]*?>[\\s\\S]*?<\\/style>"; //定义style的正则表达式 
        String regEx_html = "<[^>]+>"; //定义HTML标签的正则表达式 
         
        Pattern p_script = Pattern.compile(regEx_script,Pattern.CASE_INSENSITIVE); 
        Matcher m_script = p_script.matcher(htmlStr); 
        htmlStr=m_script.replaceAll(""); //过滤script标签 
         
        Pattern p_style = Pattern.compile(regEx_style,Pattern.CASE_INSENSITIVE); 
        Matcher m_style = p_style.matcher(htmlStr); 
        htmlStr=m_style.replaceAll(""); //过滤style标签 
         
        Pattern p_html = Pattern.compile(regEx_html,Pattern.CASE_INSENSITIVE); 
        Matcher m_html = p_html.matcher(htmlStr); 
        htmlStr=m_html.replaceAll(""); //过滤html标签 

        return htmlStr.trim(); //返回文本字符串 
    } 
}

使用Spannable或Html.fromHtml设置字体、颜色、超链接等
http://blog.csdn.net/lindonghai/article/details/49613895

andorid中Html.fromHtml方法
http://blog.csdn.net/joebaby_/article/details/7954495

Otto
----
Android 事件总线OTTO用法快速入门
http://blog.csdn.net/zhangweiwtmdbf/article/details/49096615

Android Otto框架浅析
http://itindex.net/detail/50349-android-otto-框架

Android版本检测更新 使用腾讯bugly自动更新
http://www.apkbus.com/blog-705730-62592.html
https://bugly.qq.com/docs/user-guide/instruction-manual-android-upgrade/?v=20161011192545

RecyclerView 定制item 分割线
http://blog.csdn.net/jxxfzgy/article/details/43736385

https://vladsch.com/product/markdown-navigator/referrals
Markdown Navigator 2.2.0
 Now Even Faster  Spread the word & get up to 100% off enhanced edition.       Details  
Basic & Enhanced / Enhanced Edition only
Amazing typing response
Better GFM Preview emulation
Split Editor now in Basic Edition
HTML text preview now in Basic Edition
Bug Fixes, Full Version Notes
Click in Preview scrolls to source
Soft wrap at right margin
Strip trailing spaces Hard Break aware
Markdown to HTML Export
Per Project Rendering options
Per Scope Rendering options
Customizable link address mapping
Print HTML Preview for JavaFX browser
Buy a license, view Promotions. View all enhanced features.
Disable this notification.

IntelliJ IDEA Multi-MarkDown插件安装破J全过程
http://www.jianshu.com/p/a0550f81cbd1

React Native
http://reactnative.cn/

Butterknife
https://github.com/JakeWharton/butterknife
ButterKnife：8.1.0的使用
http://www.jianshu.com/p/0392199a682b
Android Butter Knife 框架——最好用的View注入
http://www.jianshu.com/p/9ad21e548b69


Okhttp Logging Interceptor
http://blog.csdn.net/u010278882/article/details/50724694
compile 'com.squareup.okhttp3:logging-interceptor:3.1.2'
该拦截器用于记录应用中的网络请求的信息

Android开发架构思考及经验总结
http://blog.csdn.net/jf_1994/article/details/53870534


另外除了 Google 列出的架构，还有 Facebook 推出的 Flux 架构也值得考虑。

DrawerLayout
android官方侧滑菜单DrawerLayout详解
http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2014/0925/1713.html

AppBar布局的使用方式
http://www.jianshu.com/p/4ce0f3419ca8
玩转AppBarLayout，更酷炫的顶部栏
http://www.jianshu.com/p/d159f0176576
CoordinatorLayout的使用如此简单
http://blog.csdn.net/huachao1001/article/details/51554608

Android vector Path Data画图详解
http://www.w2bc.com/article/132096

Android vector标签 PathData 画图超详解
http://blog.csdn.net/easyer2012/article/details/52618228


React Native 基于 JavaScript 的开源框架 React Native
React Native 中文网
http://reactnative.cn/

React Native 中文版(含新增 Android 章节)
http://wiki.jikexueyuan.com/project/react-native/

一个 2 年 Android 开发者的 18 条忠告
http://www.codeceo.com/article/18-tips-2-years-android-developer.html

一些最佳library的列表
https://snowdream.github.io/awesome-android/
几乎所有开源安卓app的列表
https://github.com/pcqpcq/open-source-android-apps

帧动画和补间动画看这篇足够了
http://www.jianshu.com/p/5163789b1591

Android属性allowBackup安全风险浅析
http://www.freebuf.com/articles/terminal/60778.html

WebView控件中的onConsoleMessage方法不被调用
https://my.oschina.net/xmlspyspring/blog/126045
http://www.blogjava.net/xmlspy/archive/2013/04/28/398522.html

shouldOverrideUrlLoading相关说明
https://my.oschina.net/u/1446273/blog/200968

Android APK瘦身经验总结
http://www.jianshu.com/p/bfe44ef18aca

使用Android Studio的lint清除无用的资源文件
http://waychel.com/shi-yong-android-studiode-lintqing-chu-wu-yong-de-zi-yuan-wen-jian/

Android的性能优化
http://www.jianshu.com/p/be05874965d4

Android实战技巧：ViewStub的应用
http://blog.csdn.net/hitlion2008/article/details/6737537/

Android布局优化之ViewStub、include、merge使用与源码分析
http://blog.csdn.net/bboyfeiyu/article/details/45869393

ActivityThread的main方法究竟做了什么？
http://www.apkbus.com/blog-705730-62523.html

http://grepcode.com/ Android sdk源码
http://grepcode.com/search/?query=ActivityThread

Android消息处理机制(Handler、Looper、MessageQueue与Message)
http://www.cnblogs.com/angeldevil/p/3340644.html

Android消息机制字典型探究（一）
http://www.jianshu.com/p/8c06b1d7ca68

Android消息机制字典型探究（二）
http://www.jianshu.com/p/8501d3b0c359

带着这篇去通关所有Handler的提问（三）
http://www.jianshu.com/p/fad4e2ae32f5

Handler可能造成内存泄漏（四）
http://www.jianshu.com/p/c0c67c2a0532

Android开发中Handler的经典总结
http://mobile.51cto.com/aprogram-442833.htm

Android Handler详细使用方法实例
http://www.codeceo.com/article/android-handler-usage.html

android设置Activity背景色为透明的3种方
http://blog.csdn.net/lily9/article/details/11983221

如何获取Android唯一标识（唯一序列号）
http://blog.csdn.net/ljz2009y/article/details/22895297
http://www.cnblogs.com/lvcha/p/3721091.html
android获取设备唯一标识完美解决方案
http://www.tuicool.com/articles/MfQBbe
Android 如何检索Android设备的唯一ID
http://blog.csdn.net/aminfo/article/details/7604451

怎样取安卓设备唯一标识来防刷
http://www.eoeandroid.com/thread-917649-1-1.html?_dsign=d27b4af2

 项目模板化
 ---------

大幅提高 Android 开发效率之 Android 项目模板化 (上)
http://www.diycode.cc/topics/410
http://www.jianshu.com/p/e8ac0c284601
测试项目和测试模板的代码已放到 github 上: AndroidStudioTemplateTest
https://github.com/zhenghuiy/AndroidStudioTemplateTest
Android Studio 模板：
F:\AndroidStudio2_2\plugins\android\lib\templates\
E:\AndroidSDK\tools\templates\activities

大幅提高Android开发效率之Android项目模板化（下）    Live Template
http://www.diycode.cc/topics/420
http://www.jianshu.com/p/cb95ce1ba336
https://www.jetbrains.com/help/idea/2016.1/live-template-variables.html#predefined_functions


统一规范
--------
Android开发之版本统一规范
http://blankj.com/874.html

Android开发人员不得不收集的代码(持续更新中)
http://www.diycode.cc/projects/Blankj/AndroidUtilCode
https://github.com/Blankj/AndroidUtilCode
Gradle:
compile 'com.blankj:utilcode:1.3.3'
Proguard
-keep class com.blankj.utilcode.** { *; }
-keep classmembers class com.blankj.utilcode.** { *; }
-dontwarn com.blankj.utilcode.**

https://github.com/huangkunkun/AndroidUtilCode


【Android】ContentValues的用法
http://www.cnblogs.com/rayray/p/3410204.html

码云平台帮助文档 V1.2
http://git.mydoc.io/
http://git.oschina.net/

注解框架的偷懒插件Android Butterknife Zelezny使用
在build.gradle中已经加入：compile 'com.jakewharton:butterknife:8.2.1'
Android Studio-> Files---> Sttrings ----> (preferences ->) plugins -> 搜索Android Butterknife Zelezny 安装

一键上传应用到fir.im
---
FIR_Plugin_Android
https://github.com/FIRHQ/FIR_Plugin_Android
jetbrains插件线上地址: https://plugins.jetbrains.com/plugin/7640?pr=androidstudio
具体安装步骤
fir.im upload 安装

方式一、 Android Studio-> preferences -> plugins -> 搜索fir.im upload
方式二、下载包进行本地安装，步骤 Android Studio-> preferences -> plugins -> install plugin from disk..

插件会在Views -> tool windows显示 FIR.im
API token:  d4b972e14b530f2d2fe5fc951d58a5d7


Android中获取系统通讯录联系人并显示在EditText
http://www.cnblogs.com/yejiurui/archive/2013/01/02/2842061.html

android 获取电话本中的联系人列表
http://leiwuluan.iteye.com/blog/1511255

Android官方培训课程中文版(v0.9.5)
http://hukai.me/android-training-course-in-chinese/index.html

Android Api中文版
http://www.embeddedlinux.org.cn/androidapi/

Android高阶之Android studio-友盟多渠道打包方式
http://blog.csdn.net/chenliguan/article/details/51066933

[Android Studio] Android studio 多渠道打包(超简洁版)
http://www.cnblogs.com/0616--ataozhijia/p/4203997.html

在AS中gradle多渠道打包应用
https://my.oschina.net/gef/blog/603991

Android Studio利用Gradle删除没有使用到的资源和代码文件
http://www.cnblogs.com/tianzhijiexian/p/4457763.html

https://www.juhe.cn/
API数据接口_开发者数据定制_免费数据调用-聚合数据

[应用源码] Android -- 热点新闻 【安卓开发经典】
http://www.androidym.com/thread-54301-1-1.html
接口地址：
http://v.juhe.cn/toutiao/index?type=top&key=cc9de92b2c3f3517fd2f5a2a566ba2f1

{
    "reason": "成功的返回",
    "result": {
        "stat": "1",
        "data": [
            {
                "title": "巫山云雨枉断肠：女摄影师Erika Lust记录的性爱",/*标题*/
                "date": "2016-06-13 10:31",/*时间*/
                "author_name": "POCO摄影",/*作者*/
                "thumbnail_pic_s": "http://09.imgmini.eastday.com/mobile/20160613/20160613103108_7b015493398e7fd13dda3a5c
e315b1c8_1_mwpm_03200403.jpeg",/*图片1*/
                "thumbnail_pic_s02": "http://09.imgmini.eastday.com/mobile/20160613/20160613103108_7b015493398e7fd13dda3a5ce315
b1c8_1_mwpl_05500201.jpeg",/*图片2*/
                "thumbnail_pic_s03": "http://09.imgmini.eastday.com/mobile/20160613/20160613103108_7b015493398e7fd13dda3a5ce315
b1c8_1_mwpl_05500201.jpeg",/*图片3*/
                "url": "http://mini.eastday.com/mobile/160613103108379.html?qid=juheshuju",/*新闻链接*/
                "uniquekey": "160613103108379",/*唯一标识*/
                "type": "头条",/*类型一*/
                "realtype": "娱乐"/*类型二*/
            },
...]}}


我的Android笔记（八）—— 使用Jsoup解析Html
http://blog.csdn.net/barryhappy/article/details/7366654

android-dynamical-loading 动态加载技术
https://github.com/kaedea/android-dynamical-loading

Android Proguard混淆打包经验总结
http://blog.csdn.net/u011459799/article/details/52637214?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io
--------------------------------------------------------------
GRADLE下载、安装、配置与检查
Gradle User Guide 中文版 https://dongchuan.gitbooks.io/gradle-user-guide-/content/index.html
DOWNLOAD GRADLE 3.1 
https://gradle.org/gradle-download/
GRADLE_HOME:D:\gradle-3.1
Path: ......;D:\gradle-3.1\bin
gradle -v
C:\Users\Administrator>gradle -v
------------------------------------------------------------
Gradle 3.1
------------------------------------------------------------
Build time:   2016-09-19 10:53:53 UTC
Revision:     13f38ba699afd86d7cdc4ed8fd7dd3960c0b1f97

Groovy:       2.4.7
Ant:          Apache Ant(TM) version 1.9.6 compiled on June 29 2015
JVM:          1.8.0_101 (Oracle Corporation 25.101-b13)
OS:           Windows 7 6.1 amd64

C:\Users\Administrator>

Android收藏夹：
Android开发者的收藏夹
https://github.com/ruijun/Android-Dev-Favorites
官方文档
Android官方培训课程中文版 http://hukai.me/android-training-course-in-chinese/
Android官方文档 http://developer.android.com/intl/zh-cn/develop/index.html
Gradle User Guide 中文版 https://dongchuan.gitbooks.io/gradle-user-guide-/content/index.html
Gradle User Guide https://docs.gradle.org/current/userguide/userguide.html
Material Design 中文版 http://design.1sters.com/
groovy 2.4.5 API http://www.groovy-lang.org/api.html
Android Plugin DSL Reference http://google.github.io/android-gradle-dsl/current/
Java API https://docs.oracle.com/javase/7/docs/api/

Android之Sensor 简介
http://wenku.baidu.com/link?url=_x3clXnKWIygI3ey362EoPII_9lZaDvNs9Y9I-424q9nZfBfwcsCl8SxcGTi9c8DnTSHgjMl9ctaK8tOLTn916om7LKbJY4mpF1U8_KwDPC

SensorEventListener 接口 摇一摇
http://284772894.iteye.com/blog/1807499

Android几种常见的多渠道(批量)打包方式介绍
http://www.itnose.net/detail/6614021.html

使用 AXMLPrinter单独反编译AndriodManifest.xml
AXMLPrinter (Android XML)

使用AXMLPrinter2.jar+BAT批处理文件批量反编译XML
http://blog.csdn.net/attmore/article/details/7241031
for /r layout %%a in (*.xml) do @java -jar AXMLPrinter2.jar "%%a" >>"%%a".txt  
将下面的代码保存成bat文件。
将此BAT文件和AXMLPrinter2.jar放在同一个目录下，将要反编译的xml都放到layout目录下。
双击运行，享受结果吧。
使用示例：
java -jar AXMLPrinter2.jar AndroidManifest.xml > AndroidManifest.txt

通过ant脚本，编译打包android工程
http://blog.csdn.net/chenzhiqin20/article/details/8191889

#下面这句是自动生成的
sdk.dir=D:\\Program Files\\Android\\android-sdk
#数字签名文件
key.store=jingchen.keystore
#别名alias
key.alias=jingchen
#数字签名的密码
key.store.password=111111
#alias的密码
key.alias.password=111111
#这里设置混淆代码，在当前项目的proguard-project.txt中编写混淆规则
proguard.config=${sdk.dir}/tools/proguard/proguard-android.txt:proguard-project.txt


Eclipse下Ant自动打包，混淆和签名
http://www.aiuxian.com/article/p-1675466.html

Ant编译提示“Unsupported major.minor version 52.0”
http://www.cnblogs.com/e007/p/5603477.html

Eclipse下使用Ant多渠道批量打包
http://www.aiuxian.com/article/p-1675467.html


你想要的安卓技术博文这里都有！（待续）
http://www.apkbus.com/forum.php?mod=viewthread&tid=256632&_dsign=08f33db1

Android Studio 权威教程
http://www.eoeandroid.com/thread-909881-1-1.html

Android Studio 运行出现 Multiple dex files define Landroid/support/annotation/AnimRes 解决方法
http://www.cnblogs.com/liulipeng/p/4345179.html

解决AndroidStudio添加ProjectLibary后在编译时遇到的各种问题之解决方式索引
http://www.ithao123.cn/content-10690193.html

Android 6.0 新功能及主要 API 变更
http://www.apkbus.com/blog-705730-61368.html

Android 6.0 发布版移除了对 Apache HTTP 客户端的支持。如果你的应用程序使用该客户端，并且目标运行版本为 Android 2.3 (API 级别9) 及以上，需要使用 HttpURLConnection 类来代替。这个 API 更加的高效，因为它通过对用户透明的压缩、响应缓存来减少网络开销，并最小化电量消耗。要继续使用 Apache HTTP 的 API，你需要在 build.gradle 文件中声明下面的编译期依赖：

android {
    ......
    useLibrary 'org.apache.http.legacy'
}


Android (Java) 编码惯例及最佳实践
http://www.apkbus.com/blog-705730-61363.html

分享链接打开客户端功能实现逻辑
https://www.zybuluo.com/wangwangheng/note/106998#1android浏览器打开客户端原理

Bus Weekly 汇总
http://www.apkbus.com/forum.php?mod=viewthread&tid=267776&page=1&extra=&_dsign=dd10d522

《Android Studio实战 快速、高效地构建Android应用》

eclipse怎样修改包(package)的显示样式、格式
http://jingyan.baidu.com/article/c1a3101eabe8a2de656debe2.html

Eclipse 中包结构展开有两种方式
http://blog.csdn.net/cxy_357/article/details/50392076
一：平坦方式（flat）
二、分层方式（hierarchical）


中秋赠书，开启“洪荒之礼”【Bus Weekly】十九期
http://www.apkbus.com/forum.php?mod=viewthread&tid=268127&extra=page%3D1%26filter%3Dauthor%26orderby%3Ddateline

Android 者开发如何选择测试机列表
http://www.apkbus.com/blog-705730-61682.html
http://kvh.io/cn/android-test-device.html

Eclipse中使用SVN
http://blog.csdn.net/v123411739/article/details/22512133

Android Small框架增量升级方案
http://blog.csdn.net/u013022222/article/details/52268526
Small框架
https://github.com/ChanJLee/Small
Android增量升级通用代码
https://github.com/ChanJLee/AndroidPatch
结合Small的增量升级方案
https://github.com/ChanJLee/SmallPatch

Android Studio 使用Eclipse中的keystore为App签名
http://blog.csdn.net/kangear/article/details/52069726
最终在Project Structure中配置一个Signing，store文件还是Eclipse中使用的那个

Android 获取签名证书的详细信息（Eclipse和Android studio通用）
http://www.bkjia.com/Androidjc/1012685.html
今天要用到签名证书的MD5,但是这个只有在第一次生成的时候我看到了，这可怎么办呢，幸亏我们有google,我们运行下面的命令就OK了。
keytool -list -v -keystore 签名证书的路径
Eclipse 生成的签名证书是.keystore结尾的，Android Studio 生成的签名证书是.jks结尾的，这一点要注意哦

eclipse打包和android studio打包使用同一签名文件
http://www.bubuko.com/infodetail-1000864.html
当我们把eclipse 项目转到到android studio中时，打包会有所不同，在eclispe中打包时只需要选择签名文件和输入密码就可以了，但是在android stuido中打包是需要输入key.alias（别名），可能这个keystore不是你生成的或已经忘记了key.alias，你可以通过以下命令查看keystore的key.alias（别名），

命令进入keystore文件所在的目录 运行 keytool -list  -v -keystore xxxx.keystore -storepass xxxxxxxxxx（密码） 　签名的信息就有了
这样就可以顺利的打包了！

eclipse 迁移 Android Studio 证书问题

Android 获取签名证书的详细信息（Eclipse和Android studio通用）
今天要用到签名证书的MD5,但是这个只有在第一次生成的时候我看到了，这可怎么办呢，幸亏我们有google,我们运行下面的命令就OK了。
keytool -list -v -keystore 签名证书的路径
1
Eclipse 生成的签名证书是.keystore结尾的，Android Studio 生成的签名证书是.jks结尾的，这一点要注意哦


极光中日文推送标签（tag）名称定义：
rxt_registered_user_group_cn, 
rxt_registered_user_group_jp

别名：用户名（手机号码）

在通知的扩展字段增加下述key/value：
bo_type : 业务对象类型（00:无关联业务对象，01:订单，02:取现，03：组团）
bo_id : 业务对象ID
推送消息增加订单类型扩展字段：order_type（00：普通，01：团购）
订单状态扩展字段：bo_status（取值参见接口文档）   2016-06-28


总共有6类点对点推送事件：组团超时，发货超时，订单完成，订单拒收，提现成功，提现失败。
因此，业务对象类型bo_type有三种类型（00:无关联业务对象，01:订单，02:提现，03：组团）。

Android学好Shape不再依赖美工
http://www.aiuxian.com/article/p-628585.html

shape和selector和layer-list的（详细说明）
http://www.aiuxian.com/article/p-1312640.html

史上最完整的Android开发工具集合
http://www.apkbus.com/thread-252748-1-1.html

Json转换利器Gson之实例一-简单对象转化和带泛型的List转化
http://blog.csdn.net/lk_blog/article/details/7685169


[Android开发经验总结:开发规范](http://www.apkbus.com/blog-705730-60906.html)  

[AppCodeArchitecture 安卓APP代码架构，包含比较常用的开源库使用](https://github.com/Frank-Zhu/AppCodeArchitecture)  

[Android项目基础规范](http://frank-zhu.github.io/android/2016/04/26/android-code-rule/)  


[Android_滑动的时候头部变化效果](http://blog.csdn.net/qiuchunjia/article/details/51094667)  

[Android App 代码架构](http://frank-zhu.github.io/2014-11-22-android-app-code-architecture.html)  

[安卓集成发布详解（二）](http://frank-zhu.github.io/android/2015/06/15/android-release_app_build_gradle/)  

    //View注解   代码地址-----> https://github.com/JakeWharton/butterknife
    compile 'com.jakewharton:butterknife:6.1.0'
    //图片加载  代码地址-----> https://github.com/square/picasso
    compile 'com.squareup.picasso:picasso:2.5.2'
    //API网络请求注解库    代码地址-----> https://github.com/square/retrofit
    compile 'com.squareup.retrofit:retrofit:1.9.0'
    //网络请求库 代码地址-----> https://github.com/square/okhttp
    compile 'com.squareup.okhttp:okhttp:2.2.0'
    compile 'com.squareup.okhttp:okhttp-urlconnection:2.2.0'
    //消息通知数据更新（类似Broadcast）  代码地址-----> https://github.com/greenrobot/EventBus
    compile 'de.greenrobot:eventbus:2.4.0'
    //圆形头像  代码地址-----> https://github.com/hdodenhof/CircleImageView
    compile 'de.hdodenhof:circleimageview:1.2.1'
    //解析JSON数据  代码地址-----> https://code.google.com/p/google-gson/
    compile 'com.google.code.gson:gson:2.3.1'
    //弹出提示信息    代码地址-----> https://github.com/johnkil/Android-AppMsg
    compile 'com.github.johnkil.android-appmsg:appmsg:1.2.0'
    //SuperRecyclerView    代码地址-----> https://github.com/Malinskiy/SuperRecyclerView
    compile 'com.malinskiy:superrecyclerview:1.1.0'
    //超强滚动效果View    代码地址-----> https://github.com/ksoichiro/Android-ObservableScrollView
    compile 'com.github.ksoichiro:android-observablescrollview:1.5.1'



http://api.pccb.com/update/pccb_android_app.apk
[Android Studio实用指南](http://yuedu.baidu.com/ebook/31beb61a9b6648d7c1c746e8)  

[拍照、相册及裁剪的终极实现（一）——拍照及裁剪功能实现](http://blog.csdn.net/harvic880925/article/details/43163175)  

[拍照、相册及裁剪的终极实现（二）——相册选择及裁剪功能实现](http://blog.csdn.net/harvic880925/article/details/43314451)  

[Android 拍照或从相册取图片并裁剪](http://www.cnblogs.com/w-y-f/p/4028379.html)  
https://github.com/ryanhoo/PhotoCropper


dp与pix:
---------
xxxhdpi:	1280x2560  1dp=4pix     48dp=192px
xxhdpi:	1080x1920  1dp=3pix     48dp=144px
xhdpi:	720x1280   1dp=2pix	48dp=96px
hdpi:	480x800    1dp=1.5pix	48dp=72px
mdpi:	320*480    1dp=1pix	48dp=48px
ldpi:	240x320    1dp=0.75pix	48dp=36pix




