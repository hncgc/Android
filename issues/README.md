Issues
===

OOM
---
[Fixing issues with Multidex on pre-lollipop devices on Windows](https://www.jimbobbennett.io/fixing-issues-with-multidex-on-pre-lollipop-devices-on-windows/)  

[什么是OOM？如何解决OOM问题!](https://www.jianshu.com/p/41ffbf31b20c)  

[什么是java OOM？如何分析及解决oom问题？](https://www.cnblogs.com/ThinkVenus/p/6805495.html)  

[OOM 内存溢出的原因和处理方法](https://blog.csdn.net/dakaniu/article/details/80747754)  

[Android系统进程Zygote启动过程的源代码分析](https://blog.csdn.net/luoshengyang/article/details/6768304)  


--------

[Android Studio引用另一个模块module的方法](https://blog.csdn.net/lyf970419/article/details/80762821)  

[java（Android）跨Module调用对应类方法需求解决方案](https://blog.csdn.net/sunlit_6/article/details/80942137)  

[Android组件化之不同模块间 交互（activity互相跳转，数据互相传递，互相调用函数）](https://blog.csdn.net/gaolei1201/article/details/77601027)  




Multidex
---

[Android Dex分包](https://www.jianshu.com/p/e96f345e822f)  
https://github.com/Qcwxx123/MultiDex/tree/master/MultiDexTest  

[mainDexClasses脚本分析](http://coolpers.github.io/multidex/maindexclasses/2015/04/23/mainDexClasses%E8%84%9A%E6%9C%AC%E5%88%86%E6%9E%90.html)  

[Android Multidex正确使用方式（你可能也会遇到的坑）](https://www.jianshu.com/p/78f2e2d9484a)  


[如何解决java.io.IOException：找不到dex位置的原始dex文件？](https://cloud.tencent.com/developer/ask/192762)  

[Unable to instantiate application 解决办法](https://blog.csdn.net/adobe2000/article/details/78262960)  

[安卓- apk安装出现闪退java.lang.RuntimeException: Unable to instantiate application](https://blog.csdn.net/daxue_haha/article/details/76919120)  

[Android Apk包安装应用闪退，出现 java.lang.RuntimeException Unable to instantiate application Caused by: java](https://blog.csdn.net/wjr1949/article/details/80493051)  


[Android打包生成的APK安装包，安装后一打开软件就闪退问题](https://blog.csdn.net/rabbit_ding0810/article/details/78260374)  

[Android java.io.IOException异常情况整理](https://blog.csdn.net/zhufuing/article/details/38312441)  

[Android版本兼容性问题](https://blog.csdn.net/calvin_zhou/article/details/78466800)  

[android 调试崩溃Unable to instantiate application的解决方法](https://www.2cto.com/kf/201803/725461.html)  

[Android应用闪退异常java.lang.RuntimeException: Unable to instantiate application](https://blog.csdn.net/lijueqing/article/details/80854823)  

[MultiDex后java.lang.NoClassDefFoundError异常解决](https://blog.csdn.net/m00123456789/article/details/60767351)  

[android.dexOptions.incremental属性已被弃用](https://www.jianshu.com/p/da861a89ade7)  

[Android报unable to instantiate application怎么解决？](https://www.aliyun.com/jiaocheng/53238.html)  

[OS--›Gradle3.3 修改APK生成路径和文件名(附AAR修改方式以及分析过程)](https://blog.csdn.net/angcyo/article/details/78357512)  

[android 兼容性测试](https://www.testin.cn/account/login.htm)  

[Android MultiDex实践：如何绕过那些坑？](https://blog.csdn.net/richie0006/article/details/51103976)  

[Android 分Dex (MultiDex)](https://www.cnblogs.com/wingyip/p/4496028.html)  

[multiDex分包时指定主dex的class列表](https://www.cnblogs.com/zzq-include/p/6370500.html)  
~~~
在gradle中我们使用了如下代码可以将指定类型分配到主dex中：
afterEvaluate {
    tasks.matching {
        it.name.startsWith('dex')
    }.each { dx ->
       def listMain = project.rootDir.absolutePath+'/app/maindexlist.txt'
        if (dx.additionalParameters == null) {
            dx.additionalParameters = []
        }
       //改变dex方法数上线为50000，超过后进行拆分
       dx.additionalParameters += '--set-max-idx-number=50000'
        //方法数越界时则生成多个dex文件
        dx.additionalParameters += '--multi-dex'
        //maindexlist.txt文件为主dex中的类型配置文件
        dx.additionalParameters += '--main-dex-list=' + listMain
        //-main-dex-list指定的所有class会打包到主dex中
       dx.additionalParameters += '--minimal-main-dex'
　　
    }
}
高版本的gradle需要使用如下方式配置：
 dexOptions {
        javaMaxHeapSize "4g"
        preDexLibraries = false
        additionalParameters = ['--multi-dex', '--main-dex-list=' + project.rootDir.absolutePath + '/app/maindexlist.txt', '--minimal-main-dex',
                                '--set-max-idx-number=1000']
    }
    
其实我们可以直接参考app\build\intermediates\legacy_multidex_main_dex_list\debug\transformClassesWithMultidexlistForDebug\mainDexL目录下的maindexlist.txt文件

 别忘了把这个文件复制到项目目录下app/maindexlist.txt才会生效！
~~~

[multidex分包续：将指定的类打包到主dex中](https://blog.csdn.net/qq_24451593/article/details/79554372)  

[Android dex 进行手动分包,可以指定类进行分包](https://blog.csdn.net/zcv5and/article/details/78413684)  


[构建神器Gradle](http://jiajixin.cn/2015/08/07/gradle-android/)  

[【性能优化】65535方法数超出](https://blog.csdn.net/www1575066083/article/details/80938378)  


[Android关于Dex拆分(MultiDex)技术详解](https://blog.csdn.net/tan6458/article/details/54315037)  

---------------------

~~~
设置preDexLibraries = false的影响
=================================

D:\gongwei-app2\build.gradle
    dexOptions {
        javaMaxHeapSize "4g"
        preDexLibraries = false
    }

测试包dex大小(preDexLibraries = false)：
classes.dex    8857KB （不包含com.gong_wei.base.BaseApplication, 不包含com.gong_wei.ui）
classes2.dex   9231KB
classes3.dex   1074KB



    dexOptions {
        javaMaxHeapSize "4g"
        //preDexLibraries = false
    }
测试包dex大小(去掉preDexLibraries = false)：
classes.dex    1074KB （包含com.gong_wei.base.BaseApplication, 包含com.gong_wei.ui）
classes2.dex   8857KB
classes3.dex   9231KB

D:\gongwei-app2\app\build\intermediates\legacy_multidex_main_dex_list\release\transformClassesWithMultidexlistForRelease\mainDexList.txt
D:\gongwei-app2\app\build\intermediates\legacy_multidex_main_dex_list\debug\transformClassesWithMultidexlistForDebug\mainDexList.txt

    dexOptions {
        javaMaxHeapSize "4g"
        preDexLibraries = false
        additionalParameters = ['--multi-dex', '--main-dex-list=' + project.rootDir.absolutePath + '/app/maindexlist.txt', '--minimal-main-dex',
                                '--set-max-idx-number=1000']
    }

~~~

[Android Too many classes in --main-dex-list 优化方法](https://www.jianshu.com/p/b4c179ad137e)  


---------------------

[Android项目该如何选择targetSdkVersion](https://blog.csdn.net/zhangjin12312/article/details/78211328)  
~~~
compileSdkVersion定义应用程序编译选择哪个Android SDK版本，通常compileSDKVersion属性值被设置为最新的API版本
compileSDKVersion的属性值不会影响Android系统运行行为
targetSdkVersion、minSdkVersion和CompileSdkVersion之间的关系:
Android系统平台的行为变更，只有targetSdkVersion的属性值被设置为大于或等于该系统平台的API版本时，才会生效；compileSdkVersion属于Android编译项目时其中的一项配置，主要区别是compileSDKVersion在不会被打包的APK文件中，targetSdkVersion和minSdkVersion将被打包到APK文件中，具体可以解压APK文件后，查看AndroidManifest.xml文件
minSdkVersion <= targetSdkVersion <= compileSdkVersion
~~~

[Android targetSdkVersion你真的了解吗？](https://blog.csdn.net/qq_23062979/article/details/81294550)  

去除重复依赖
---

[Android Gradle依赖管理、去除重复依赖、忽略](https://blog.csdn.net/wapchief/article/details/84974219)  

[Android Studio 引用第三方包时，com.android.support 因版本冲突问题](https://blog.csdn.net/qq_34983989/article/details/82746642)  

[android studio去除重复依赖](https://www.csdn.net/gather_20/MtTakg2sOTg0MC1ibG9n.html)  

[AndroidStudio添加多依赖导致依赖重复的解决办法](https://blog.csdn.net/zhang721677/article/details/79752433)  

[Android Studio/Gradle/重复依赖](https://blog.csdn.net/u014587769/article/details/71214973)  

[gradle 编译忽略警告](https://blog.csdn.net/dounine/article/details/64129415)  

[android studio 解决重复依赖的问题](https://blog.csdn.net/xzp297988064/article/details/70708434)  
~~~
在build.gradle里面添加上
configurations {
　　all*.exclude group: 'com.android.support', module: 'support-v4'
}
~~~

[【android】Gradle配置之ResolutionStrategy](https://www.jianshu.com/p/0a60a78648bf)  
~~~
比如统一替换SupportVersion版本
configurations.all {
    resolutionStrategy.eachDependency { DependencyResolveDetails details ->
        def requested = details.requested
        if (requested.group == 'com.android.support') {
            if (!requested.name.startsWith("multidex")) {
                details.useVersion SupportVersion
            }
        }
    }
}
~~~

[Android7.0拍照失败FileUriExposedException,你的拍照代码升级了吗](https://blog.csdn.net/yunboxiang/article/details/54017121)  

-----------

[设置Application ID](https://www.jianshu.com/p/28a12dc7bfba)  

[Multiple APK Support(相同的应用程序有多个APKs支持)](https://blog.csdn.net/dblackde/article/details/7804544)  


-------------------------

[修改TabLayout下划线宽度，以及在Api28下遇到的问题—— tabLayout.getDeclaredField 空指针以及水波纹背景问题](https://blog.csdn.net/shanshan_1117/article/details/84319012)  
~~~
    public void setIndicator(TabLayout tabs, int leftDip, int rightDip) {
        Class<?> tabLayout = tabs.getClass();
        Field tabStrip = null;
        try {
            tabStrip = tabLayout.getDeclaredField("mTabStrip");
改为：
            tabStrip = tabLayout.getDeclaredField("slidingTabIndicator");

        } catch (NoSuchFieldException e) {
            e.printStackTrace();
            return;
        }

API28下mTextView改名为textView
tabLayout.getDeclaredField("mTextView")，在API28下记得改为：tabLayout.getDeclaredField("textView")；

    public static void setTablayoutIndicatorEqualTitle(final TabLayout tabLayout){
    ......
                            Field mTextViewField = tabView.getClass().getDeclaredField("mTextView");
改为：
                            Field mTextViewField = tabView.getClass().getDeclaredField("textView");

TabTab的点击有水波纹的背景样式
在布局文件中我已经加上了 tabBackground 属性
app:tabBackground="@null"
在API28下还需要加上一句属性：

    app:tabBackground="@null"
    app:tabRippleColor="@null"
~~~
