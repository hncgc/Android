Android 技巧与经验
===

[一个多年安卓开发者的一些感悟与忠告](http://www.apkbus.com/blog-847095-72728.html)  

[所有开源安卓app的列表](https://github.com/pcqpcq/open-source-android-apps)  

[Android奇技淫巧：隐藏APP图标](http://blog.liangruijun.com/2016/01/24/Android%E5%A5%87%E6%8A%80%E6%B7%AB%E5%B7%A7%EF%BC%9A%E9%9A%90%E8%97%8FAPP%E5%9B%BE%E6%A0%87/)  

[Android UI 大全 里面包含所以特效大全的项目，都是每个特效一个项目的结构](https://gitee.com/bob4j/Android-UI)  

[安卓巴士Android开发者门户](http://mp.sohu.com/profile?xpt=c29odW1wNDI3dXhwQHNvaHUuY29t)

[Android开发之脚本替换PackageName](http://www.jianshu.com/p/dca9c323c686)  

[关于Android SDK里的compileSdk、minSdk、targetSdk、buildTools、Tools、Platform-tools](http://www.jianshu.com/p/544d9f72883d)  

PayPal
---

[PayPal Android SDK 2.0 支付](http://blog.csdn.net/adongqin/article/details/38781329)  

[PayPal Android SDK的接入和开发、与服务器对接IPN](http://blog.csdn.net/carmideychen/article/details/72420467)  

引入SDK  
>   compile('com.paypal.sdk:paypal-android-sdk:2.15.3')
>       { exclude group:'io.card'}
>   exclude group:'io.card'表明不允许直接用卡支付，如果不添加这一行，在支付时用卡支付的按钮选项出现

[算是目前PAYPAL最全最完整的开发方式了](http://blog.csdn.net/a53657561/article/details/64982411)  

------

[ThinkAndroid](https://github.com/white-cat/ThinkAndroid)  

[DataBinding初认识](http://www.apkbus.com/blog-927424-72831.html)  

[安卓零基础](http://www.apkbus.com/misc.php?mod=tag&id=6169)  

[Android开发路上那些小技巧与经验，一起聚沙成塔！](http://www.apkbus.com/thread-463317-1-1.html)  
```
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
```

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
```
edtRemark.setFilters(new InputFilter[]{new UIHelper.EmojiExcludeFilter()});
```
