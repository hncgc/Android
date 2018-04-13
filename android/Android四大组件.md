Android 四大组件
---
[Android 四大组件](https://www.jianshu.com/u/383970bef0a0) 

Activity
---
[Android基础：最易懂的Activity启动模式详解 ](https://www.jianshu.com/p/399e83d02e33)  

[Android：Fragment最全面介绍 & 使用方法解析](https://www.jianshu.com/p/2bf21cefb763)  

[Android：手把手教你 实现Activity 与 Fragment 相互通信（含Demo）](https://www.jianshu.com/p/825eb1f98c19)  

[Android开发：5分钟解析Activity&Fragment生命周期](https://www.jianshu.com/p/b1ff03a7bb1f)  

BroadcastReceiver
---
[Android四大组件：BroadcastReceiver史上最全面解析](https://www.jianshu.com/p/ca3d87a4cdf3)  

ContentProvider
---
[ndroid：关于ContentProvider的知识都在这里了！](https://www.jianshu.com/p/ea8bc4aaf057)  

Service
---

[Android 四大组件：一份全面 & 简洁的 Service 知识讲解攻略](https://www.jianshu.com/p/d963c55c3ab9)  

[Android：Service生命周期 完全解析](https://www.jianshu.com/p/8d0cde35eb10)  

[Android：（本地、可通信的、前台、远程）Service使用全面介绍](https://www.jianshu.com/p/e04c4239b07e)  
https://github.com/Carson-Ho/Demo_Service/tree/5e2a70cf2d75c56bbfa1abc0ead16c5ad8cae83f  
https://github.com/Carson-Ho/Demo_Service  
https://github.com/Carson-Ho/Demo_Service/tree/719e3b9ffd5017c334cdfdaf45b6a72776a2066a  

[Android：远程服务Service（含AIDL & IPC讲解）](https://www.jianshu.com/p/34326751b2c6)  
[客户端:Github_RemoteService_Client](https://github.com/Carson-Ho/Service_Client)  
[服务端:Github_RemoteService_Server](https://github.com/Carson-Ho/Service_Server)  

[Android 多线程 解析：IntentService（含源码解析）](https://www.jianshu.com/p/8a3c44a9173a)  

[Java Message Service （JMS）介绍](http://blog.csdn.net/lucifer821031/article/details/2064541)  

IPC
---

Android跨进程通信IPC
---
[•1、Android跨进程通信IPC之1——Linux基础](https://www.jianshu.com/p/36b488863bc0)  
[•2、Android跨进程通信IPC之2——Bionic](https://www.jianshu.com/p/25a908c7eefa)  
[•3、Android跨进程通信IPC之3——关于"JNI"的那些事](https://www.jianshu.com/p/cd038167d896)  
[•4、Android跨进程通信IPC之4——AndroidIPC基础1](https://www.jianshu.com/p/f5e103674953)  
[•4、Android跨进程通信IPC之4——AndroidIPC基础2](https://www.jianshu.com/p/28406f85e266)  
[•5、Android跨进程通信IPC之5——Binder的三大接口](https://www.jianshu.com/p/3c71473e7305)  
[•6、Android跨进程通信IPC之6——Binder框架](https://www.jianshu.com/p/b4a8be5c6300)  
[•7、Android跨进程通信IPC之7——Binder相关结构体简介](https://www.jianshu.com/p/5740a8447324)  
[•8、Android跨进程通信IPC之8——Binder驱动](https://www.jianshu.com/p/2efc0971c3e0)  
[•9、Android跨进程通信IPC之9——Binder之Framework层C++篇1](https://www.jianshu.com/p/b72c67e09653)  
[•9、Android跨进程通信IPC之9——Binder之Framework层C++篇2](https://www.jianshu.com/p/c8580977f132)  
[•10、Android跨进程通信IPC之10——Binder之Framework层Java篇](https://www.jianshu.com/p/e360b00d0d29)  
[•11、Android跨进程通信IPC之11——AIDL](https://www.jianshu.com/p/375e3873b1f4)  
[•12、Android跨进程通信IPC之12——Binder补充](https://www.jianshu.com/p/e360b00d0d29)  
[•13、Android跨进程通信IPC之13——Binder总结](https://www.jianshu.com/p/485233919c15)  
[•14、Android跨进程通信IPC之14——其他IPC方式](https://www.jianshu.com/p/485233919c15)  
[•15、Android跨进程通信IPC之15——感谢](https://www.jianshu.com/p/1136e8fed186)  

AIDL（Android接口定义语言）
---

> 用于两个APP间通讯  

[Android中AIDL的使用详解](https://www.jianshu.com/p/d1fac6ccee98)  

[Android中AIDL的工作原理](https://www.jianshu.com/p/e0c583ea9289)  

[Android 中AIDL的使用与理解](http://blog.csdn.net/u011974987/article/details/51243539)  

[Android：学习AIDL，这一篇文章就够了(上)](http://blog.csdn.net/luoyanglizi/article/details/51980630)  

```
package com.pccb.app.net;

// Declare any non-default types here with import statements

interface IMyAidlInterface {
    /**
     * Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}
```

[你真的理解AIDL中的in，out，inout么？](http://blog.csdn.net/luoyanglizi/article/details/51958091)  

[Android中的Service：默默的奉献者 (1)   ](http://blog.csdn.net/luoyanglizi/article/details/51594016)  

[Android中的Service：Binder，Messenger，AIDL（2）](http://blog.csdn.net/luoyanglizi/article/details/51594016)  

[Android AIDL -通过一个比较完整的Demo快速运用](http://blog.csdn.net/Singleton1900/article/details/8434643)  

[Android跨进程通信IPC之11——AIDL](https://www.jianshu.com/p/375e3873b1f4)  
---

runOnUiThread()
---
[android Activity runOnUiThread() 方法使用](https://www.cnblogs.com/zhaoyanjun/archive/2016/05/11/5483221.html)  

[runOnUiThread更新主线程](https://www.cnblogs.com/wanqieddy/p/4153203.html)  
