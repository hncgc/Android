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

