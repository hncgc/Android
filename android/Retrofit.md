Retrofit 2.0
---

[很详细的 Retrofit 2.0 使用教程](http://www.apkbus.com/blog-822717-76639.html)  

[Android：手把手带你 深入读懂 Retrofit 2.0 源码](https://www.jianshu.com/p/0c055ad46b6c)  

[Retrofit 2.0 超能实践（一），okHttp完美支持Https传输](http://blog.csdn.net/sk719887916/article/details/51597816)  

[Retrofit2.0 ，OkHttp3完美同步持久Cookie实现免登录(二)](http://blog.csdn.net/sk719887916/article/details/51700659)  

[Retrofit 2.0 超能实践（三），轻松实现文件/多图片上传/Json字符串](http://blog.csdn.net/sk719887916/article/details/51755427)  

[Retrofit 2.0 超能实践（四），完成大文件断点下载](http://www.jianshu.com/p/582e0a4a4ee9)  

[Retrofit，Okhttp对每个Request统一动态添加header和参数（五）](http://blog.csdn.net/sk719887916/article/details/52189602)

    //API网络请求注解库    代码地址-----> https://github.com/square/retrofit
    compile 'com.squareup.retrofit:retrofit:1.9.0'

[Retrofit2使用（非常简洁易懂）](http://blog.csdn.net/baidu_31093133/article/details/51759452)  
[Android Retrofit 2.0使用](http://wuxiaolong.me/2016/01/15/retrofit/)  
[Retrofit2 源码解析](http://bxbxbai.github.io/2015/12/13/retrofit2/)  

[Android Retrofit 2.0使用](http://www.open-open.com/lib/view/open1465993338254.html)  
[Android Retrofit 2.0 使用-补充篇](http://www.mobile-open.com/2016/965159.html)  

RetrofitClient
---
[Android基于Retrofit2.0 +RxJava 封装的超好用的RetrofitClient工具类（六）](http://blog.csdn.net/sk719887916/article/details/51958010)  

[玩转IOC，教你徒手实现自定义的Retrofit框架（七）](http://blog.csdn.net/sk719887916/article/details/51957819)
Android 玩转IOC，Retfotit源码解析，教你徒手实现自定义的Retrofit框架


[Rxjava和Retrofit 需要掌握的几个实用技巧,缓存问题和统一对有无网络处理问题（八）](http://blog.csdn.net/sk719887916/article/details/52132106)  
Rxjava +Retrofit 你需要掌握的几个技巧，Retrofit缓存，RxJava封装，统一对有无网络处理,异常处理， 返回结果问题


[Novate：对Retrofit2.0的又一次完美改进加强！（九）](http://blog.csdn.net/sk719887916/article/details/52195428)  
Novate 网络库：Retrofit2.0和RxJava的又一次完美改进加强(Tamic博客 -CSDN)  
GitHub:https://github.com/Tamicer/Novate/


Retrofit
---
官网 http://square.github.io/retrofit/ 
Github https://github.com/square/retrofit

 Platform calls Class.forName on types which do not exist on Android to determine platform.
-dontnote retrofit2.Platform
 Platform used when running on RoboVM on iOS. Will not be used at runtime.
-dontnote retrofit2.Platform$IOS$MainThreadExecutor
 Platform used when running on Java 8 VMs. Will not be used at runtime.
-dontwarn retrofit2.Platform$Java8
 Retain generic type information for use by reflection by converters and adapters.
-keepattributes Signature
 Retain declared checked exceptions for use by a Proxy instance.
-keepattributes Exceptions

[Retrofit源码分析](http://blog.csdn.net/duanyy1990/article/details/52071954)  
https://github.com/square/okhttp

[Android 介绍Retrofit的简单使用](http://blog.csdn.net/bitian123/article/details/51899716)  
[Retrofit用法详解](http://blog.csdn.net/duanyy1990/article/details/52139294)

compile 'com.squareup.retrofit2:retrofit:2.1.0'
compile 'com.squareup.retrofit2:converter-gson:2.1.0'
compile 'com.squareup.retrofit2:adapter-rxjava:2.1.0'


compile 'com.squareup.retrofit2:retrofit:2.0.0-beta4'//Retrofit2所需要的包
compile 'com.squareup.retrofit2:converter-gson:2.0.0-beta4'//ConverterFactory的Gson依赖包
compile 'com.squareup.retrofit2:converter-scalars:2.0.0-beta4'//ConverterFactory的String依赖包


[Retrofit — Getting Started and Creating an Android Client](https://futurestud.io/tutorials/retrofit-getting-started-and-android-client)  

[是时候客观评价Retrofit了，Retrofit这几点你必须明白！](http://blog.csdn.net/sk719887916/article/details/53613263)  

rrd结构 ：Retrofit + Rxjava + Dagger2
ReactiveX是Reactive Extensions的缩写，一般简写为Rx
ReactiveX 是一个使用可观察数据流进行异步编程的编程接口，ReactiveX结合了观察者模式、迭代器模式和函数式编程的精华

The Reactive Extensions 简称Rx 反应式扩展 

[RxJava+Retrofit 简单结合](http://www.tuicool.com/articles/qQFVven)  
git地址： https://github.com/meijius/RxRetrofitDemo
[【知识必备】RxJava+Retrofit二次封装最佳结合体验，打造懒人封装框架~](http://www.cnblogs.com/liushilin/p/6164901.html)  
代码地址: https://github.com/nanchen2251/RetrofitRxUtil

[RxJava+Retrofit+OkHttp 封装](http://www.tuicool.com/articles/eiyUziM)  


[Android中Retrofit+OkHttp进行HTTP网络编程的使用指南](http://www.jb51.net/article/88542.htm)  

[Android app开发中Retrofit框架的初步上手使用](http://www.jb51.net/article/79729.htm)  

[Retrofit自定义GsonConverter处理所有请求错误情况](http://www.jianshu.com/p/5b8b1062866b)  

RxJava RxAndroid RxBus Retrofit2 OkHttp3 Dagger2
---
[聊聊对RxJava与Retrofit的封装](http://www.jianshu.com/p/93f8c9ae8819)  

