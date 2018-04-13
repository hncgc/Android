Gradle
---
[中文官网构建指南](https://developer.android.google.cn/studio/build/index.html)  

[Gradle 详解](http://blog.csdn.net/xu_song/article/details/52050092)  
http://www.infoq.com/cn/articles/android-in-depth-gradle

[使用resConfigs去除无用语言资源](https://www.jianshu.com/p/8796ad90fcc6)  

当应用不需要支持几十种语言时，可以通过配置 resConfigs 去除无用的语言资源。
例如下面的代码就只保留了中文和英文的语言资源：  

        defaultConfig {
            resConfigs "zh","en"
        }  


[让你的APK瘦成一道闪电](https://www.cnblogs.com/tianzhijiexian/p/4505312.html)  

[Android Studio利用Gradle删除没有使用到的资源和代码文件](http://www.cnblogs.com/tianzhijiexian/p/4457763.html)  

    buildTypes {
            debug {
                minifyEnabled true // 是否混淆
                shrinkResources true // 是否去除无效的资源文件
                proguardFiles getDefaultProguardFile('proguard-android.txt'),'debug-proguard-rules.pro'
            }
            release {
                minifyEnabled true // 是否混淆
                shrinkResources true // 是否去除无效的资源文件
                // 混淆的配置文件
                proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
            }
        }
 

[在Android Stuido中使用Lint](http://www.cnblogs.com/tianzhijiexian/p/4504768.html)  

[Android Studio项目Gradle构建实践](http://blog.csdn.net/s402178946/article/details/54140200)  

[android Studio中关于Gradle的使用注解](http://blog.csdn.net/zouchengxufei/article/details/50417271)  

Gradle 教程
---
[Gradle 教程](http://ask.android-studio.org/?/topic/Gradle%E6%95%99%E7%A8%8B)  

[【Gradle教程】第一章：引言](http://ask.android-studio.org/?/article/7)  
 
[【Gradle教程】第二章：概述](http://ask.android-studio.org/?/article/6)  

[【Gradle教程】第三章：教程](http://ask.android-studio.org/?/article/15)  

Android Gradle权威指南
---
[Android Gradle权威指南](https://yuedu.baidu.com/ebook/14a722970740be1e640e9a3e)

[第八章 自定义Android Gradle工程](https://www.jianshu.com/p/560cecfb20da)  

[第九章 Android Gradle高级自定义](https://www.jianshu.com/p/8b2c3a3789e4)  

------------

[Gradle之使用BuildConfig自定义常量](http://blog.csdn.net/joy_whale/article/details/51858459)  

[Android Studio之BuildConfig类](http://blog.csdn.net/LVXIANGAN/article/details/71601451)  

[Gradle构建控制Log开关——BuildConfig\自定义](http://blog.csdn.net/xx326664162/article/details/50553945)  

[使用 gradle 在编译时动态设置 Android resValue / BuildConfig / Manifes中<meta-data>变量的值](http://blog.csdn.net/xx326664162/article/details/49247815)  

[Gradle编译生成不同的版本，动态设定应用标题 / 应用图标 / 替换常量](http://blog.csdn.net/xx326664162/article/details/51508132)  

[AndroidStudio下BuildTypes和ProductFlavors动态编译并重命名apk](http://blog.csdn.net/angusing/article/details/47721765) 

多渠道打包
---  
[Android Studio系列教程六--Gradle多渠道打包](http://blog.csdn.net/ljchlx/article/details/43059467)  

[使用gradle的productFlavors实现Android项目多渠道打包](http://blog.csdn.net/lj402159806/article/details/54947658)  

[Android Studio -使用 Gradle打包多版本APK——buildTypes和productFlavors](http://blog.csdn.net/xx326664162/article/details/48467343)

[Android高阶之Android studio-友盟多渠道打包方式](http://blog.csdn.net/chenliguan/article/details/51066933)

[[Android Studio] Android studio 多渠道打包(超简洁版)](http://www.cnblogs.com/0616--ataozhijia/p/4203997.html)  

[在AS中gradle多渠道打包应用](https://my.oschina.net/gef/blog/603991)  

[Android Proguard混淆打包经验总结](http://blog.csdn.net/u011459799/article/details/52637214?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)  

[Android Studio利用Gradle删除没有使用到的资源和代码文件](http://www.cnblogs.com/tianzhijiexian/p/4457763.html)  

---
  
GRADLE下载、安装、配置与检查
[Gradle User Guide 中文版](https://dongchuan.gitbooks.io/gradle-user-guide-/content/index.html)  

[DOWNLOAD GRADLE 3.1 ](https://gradle.org/gradle-download/)  

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


