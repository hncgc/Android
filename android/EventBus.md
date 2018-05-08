EventBus
---------

EventBus 3.0使用
http://www.th7.cn/Program/Android/201607/901646.shtml

首先添加引用
compile 'org.greenrobot:eventbus:3.0.0'

#EventBus 3.0
-keepattributes *Annotation*
-keepclassmembers class ** {
    @org.greenrobot.eventbus.Subscribe <methods>;
}
-keep enum org.greenrobot.eventbus.ThreadMode { *; }

# Only required if you use AsyncExecutor
-keepclassmembers class * extends org.greenrobot.eventbus.util.ThrowableFailureEvent {
    <init>(java.lang.Throwable);
}

android EventBus 3.0 混淆配置
http://blog.csdn.net/yangzs516/article/details/51776576
https://github.com/greenrobot/EventBus  

使用的这个库在github的官网README中没有写明相应混淆的配置.

经过对官网的查询，在一个小角落还是被我找到了。

-keepattributes *Annotation*
-keepclassmembers class ** {
    @org.greenrobot.eventbus.Subscribe <methods>;
}
-keep enum org.greenrobot.eventbus.ThreadMode { *; }

# Only required if you use AsyncExecutor
-keepclassmembers class * extends org.greenrobot.eventbus.util.ThrowableFailureEvent {
    <init>(Java.lang.Throwable);
}
链接：http://greenrobot.org/eventbus/documentation/proguard/


EnevtBus 发布、订阅消息--android
http://blog.csdn.net/shareus/article/details/50748804

实例讲解EventBus for Android
http://blog.csdn.net/bigconvience/article/details/46278719
https://github.com/greenrobot/EventBus


org.greenrobot.eventbus.EventBus
https://github.com/greenrobot/EventBus

Gradle:

compile 'org.greenrobot:eventbus:3.0.0'

EventBus in 3 steps

Define events:

public static class MessageEvent { /* Additional fields if needed */ }
Prepare subscribers: Declare and annotate your subscribing method, optionally specify a thread mode:

@Subscribe(threadMode = ThreadMode.MAIN)  
public void onMessageEvent(MessageEvent event) {/* Do something */};
Register and unregister your subscriber. For example on Android, activities and fragments should usually register according to their life cycle:

@Override
public void onStart() {
    super.onStart();
    EventBus.getDefault().register(this);
}

@Override
public void onStop() {
    super.onStop();
    EventBus.getDefault().unregister(this);
}
Post events:

EventBus.getDefault().post(new MessageEvent());


Android EventBus框架（一）之使用详细介绍
http://blog.csdn.net/happy_horse/article/details/51565441
EventBus是一款针对Android优化的发布/订阅事件总线
源码：https://github.com/greenrobot/EventBus

EventBus使用详解(二)——EventBus使用进阶
http://blog.csdn.net/harvic880925/article/details/40787203

Android EventBus详解其使用
http://www.apkbus.com/blog-705730-61398.html


[Eventbus 详解，Activity和fragment通讯，相互发送接收数据](https://blog.csdn.net/u013790519/article/details/49181857)  
EventBus在github上源码：https://github.com/greenrobot/EventBus  

[Activity和Fragment的三种通信以及EventBus通信](https://blog.csdn.net/jianesrq0724/article/details/54909911)  

[ANDROID中使用开源框架EVENTBUS3.0实现FRAGMENT之间的通信交互](https://www.cnblogs.com/panhouye/p/6420727.html)  

[Android中EventBus3.0的使用](https://blog.csdn.net/Captain_Magicer/article/details/54413786)  

[Android实现fragment向Activity实时传递信息](https://blog.csdn.net/s1674521/article/details/78318525)  

[Activity，Fragment绑定生命周期，实现EventBus的自动注册、自动注销](https://blog.csdn.net/u010755087/article/details/75308014)  

[EventBus 3.0，让事件订阅更简单，从此告别组件消息传递烦恼~](https://www.cnblogs.com/liushilin/p/6089785.html)  

[EventBus3.0使用总结](https://www.2cto.com/kf/201602/489989.html)  





