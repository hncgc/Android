[Android 混淆查缺补漏](http://www.sohu.com/a/217384047_611601)  

[5分钟搞定android混淆](https://www.jianshu.com/p/f3455ecaa56e)  

[Android混淆总结篇(一)](http://blog.csdn.net/yk377657321/article/details/60501880)  

[Android混淆总结篇(二)](http://blog.csdn.net/yk377657321/article/details/63257783)  

[Android 混淆总结（直接copy）](http://blog.csdn.net/u012188405/article/details/51985273) 


[Android混淆从入门到精通](https://www.jianshu.com/p/7436a1a32891)  

Android Studio自身集成Java语言的ProGuard作为压缩，优化和混淆工具，配合Gradle构建工具使用很简单，只需要在工程应用目录的gradle文件中设置minifyEnabled为true即可。然后我们就可以到proguard-rules.pro文件中加入我们的混淆规则了。

    android {
        ...
        buildTypes {
            release {
                minifyEnabled true
                proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
            }
        }
    }

[为什么这么多商业Android开发者不混淆代码？](https://www.zhihu.com/question/37446729)  

[Android ProGuard 混淆 详解](http://blog.csdn.net/chen930724/article/details/49687067)  

[Android 混淆那些事儿](https://www.cnblogs.com/bugly/p/7085469.html)  

    未混淆代码的反编译操作非常简单，网上有很多教程, 也可以通过使用Android Studio自带的apk分析工具(Build---Analyze APK)直接看到未混淆Apk的源代码和原始的资源文件

----------------

生成混淆规则
---  

通过使用Android Studio自带的apk分析工具(Build---Analyze APK)生成混淆规则：

生成混淆规则：

Build---Analyze APK

F:\pccb_app_3_1_11\app\build\outputs\apk\yyb\release\pccb-v3.1.11-yyb-release.apk

classes.dex

com
   pccb
       app
          bean
右键：
     Generate Proguard keep rule

    # Add *one* of the following rules to your Proguard configuration file.
    # Alternatively, you can annotate classes and class members with @android.support.annotation.Keep
    
    # keep everything in this package from being removed or renamed
    -keep class com.pccb.app.bean.** { *; }

    # keep everything in this package from being renamed only
    -keepnames class com.pccb.app.bean.** { *; }

---------------------------------
[[Android] Proguard And DexGuard](http://blog.csdn.net/arui319/article/details/18360147)

[Android Proguard工具使用和配置详解   ](http://blog.csdn.net/ccpat/article/details/52059344)  







