
AIDL（Android 接口定义语言）
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
