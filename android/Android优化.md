Android 优化
===

Android App优化系列
---

[1.背景:Android App优化, 要怎么做?](https://www.jianshu.com/p/f7006ab64da7)  

[2.Android App优化之性能分析工具](https://www.jianshu.com/p/da2a4bfcba68)  

[3.Android App优化之提升你的App启动速度之理论基础](https://www.jianshu.com/p/98c1656a357a)  

[4.Android App优化之提升你的App启动速度之实例挑战](https://www.jianshu.com/p/4f10c9a10ac9)  

[5.Android App优化之Layout怎么摆](https://www.jianshu.com/p/4943dae4c333)  

[6.Android App优化之ANR详解](https://www.jianshu.com/p/6d855e984b99)  

[7.Android App优化之消除卡顿](https://www.jianshu.com/p/1fb065c806e6)  

[8.Android App优化之内存优化](https://www.jianshu.com/p/48475df838d9)  

[9.Android App优化之持久电量](https://www.jianshu.com/p/c55ef05c0047)  

[10.Android App优化之如何高效网络请求](https://www.jianshu.com/p/d4c2c62ffc35)  

性能优化
---

[App性能优化系列结语篇](http://blog.lmj.wiki/2016/11/06/app-opti/app_opt_summary/)  

[小细节，大用途，35 个 Java 代码性能优化总结！](https://segmentfault.com/p/1210000008638186/read)  

[Android的性能优化](http://www.jianshu.com/p/be05874965d4)  

去除重复依赖
---
[android studio去除重复依赖](https://www.csdn.net/gather_20/MtTakg2sOTg0MC1ibG9n.html)  

[AndroidStudio添加多依赖导致依赖重复的解决办法](https://blog.csdn.net/zhang721677/article/details/79752433)  


去除无用资源
---
[Android APK瘦身经验总结](http://www.jianshu.com/p/bfe44ef18aca)  
AndResGuard: https://github.com/shwenzhang/AndResGuard

[Android Studio 检查并去除无用资源文件](https://www.jianshu.com/p/51da2d4492e1)  
~~~
Analyze --> run inspaction by Name ...
在弹出的搜索窗口中输入想执行的检查类型，如“Unused Resources”。不必全部输入就应该自动找到
点击后会弹出“inspaction scope”选择窗口
inspaction scope 可以设置文件过滤，选择好后点ok就开始检查
~~~

[android之as自动化删除无用资源为apk瘦身](http://blog.csdn.net/zhongwn/article/details/52769927)  

[使用Android Studio的lint清除无用的资源文件](http://waychel.com/shi-yong-android-studiode-lintqing-chu-wu-yong-de-zi-yuan-wen-jian/)  

[Android studio 之ANalyze 清理无用资源](http://blog.csdn.net/qulonglong110/article/details/51911261)  

[Android 性能优化：使用 Lint 优化代码、去除多余资源](http://blog.csdn.net/u011240877/article/details/54141714)  

[如何获取Android唯一标识（唯一序列号）](http://blog.csdn.net/ljz2009y/article/details/22895297)  

65K的问题
---
[彻底解决Android 应用方法数不能超过65K的问题](http://www.itnose.net/detail/6168594.html)  

[Android开发方法数超过64k（65k）解决办法](http://www.jianshu.com/p/271668909cc6)  

[Android Studio 运行出现 Multiple dex files define Landroid/support/annotation/AnimRes 解决方法](http://www.cnblogs.com/liulipeng/p/4345179.html)  

流量  
---
自己开发的Android APP消耗流量过多，如何解决？
http://bbs.csdn.net/topics/390790742

安卓居然比苹果更费流量?轻松几招教你如何节省流量
http://www.360doc.com/content/16/0404/22/11613470_547885459.shtml

ANR(Application Not Responding)
---

[ANR](https://baike.baidu.com/item/ANR/1585630?fr=aladdin)  

[Android App优化之ANR详解](https://www.jianshu.com/p/6d855e984b99)  

 OOM(out of memory)内存泄露
---

[什么是java OOM？如何分析及解决oom问题？](https://www.cnblogs.com/ThinkVenus/p/6805495.html)  
```
内存泄露：申请使用完的内存没有释放，导致虚拟机不能再次使用该内存，此时这段内存就泄露了，因为申请者不用了，而又不能被虚拟机分配给别人用。  
内存溢出：申请的内存超出了JVM能提供的内存大小，此时称之为溢出。
```

[OOM问题总结](https://blog.csdn.net/lj19851227/article/details/44018465)  

[异常、堆内存溢出、OOM的几种情况](https://blog.csdn.net/sinat_29912455/article/details/51125748)  

[一次解决OOM的经历](https://segmentfault.com/a/1190000005180612)  

[常见OOM异常](https://blog.csdn.net/qq_33450379/article/details/53731318)  

[Android 关于OOM的解决方案](https://blog.csdn.net/leehong2005/article/details/8056608)  

[Android如何避免OOM总结](https://blog.csdn.net/ljx19900116/article/details/50037627)  

[Android OOM出现常见原因及解决办法](https://blog.csdn.net/hudfang/article/details/51781997)  

[解决Android解析图片的OOM问题!!!](https://blog.csdn.net/Android_Tutor/article/details/8099918)  

[【Android性能优化】内存泄露和内存溢出（OOM）的引发原因及优化方案](https://blog.csdn.net/mxm691292118/article/details/51020023)  

[内存泄漏和内存溢出的区别和联系](https://blog.csdn.net/ruiruihahaha/article/details/70270574)  

[内存溢出和内存泄漏的区别，产生原因以及解决方案](https://blog.csdn.net/ShanYu1198124123/article/details/52414392)  

[Android手机提示“内部存储空间不足”产生原因及解决方案](https://blog.csdn.net/iteye_11192/article/details/82614601)   
[Android O 版本（Android 8.0） 存储空间不足时提醒](https://blog.csdn.net/rzc0525/article/details/85759819)  
[android中内存不足及Activity恢复的情况](https://www.jianshu.com/p/04a8d85807ca)  
[Android OutOfMemoryError：内存不足问题的排查与解决](https://www.jianshu.com/p/db98a40e0455)  
[Android 内存泄漏 - 做一个有“洁癖”的开发者](https://www.jianshu.com/p/44d26d355a56)  



