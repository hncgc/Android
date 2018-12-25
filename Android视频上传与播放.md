Android视频上传与播放
===

[Android视频开发基础(一）](https://blog.csdn.net/goodlixueyong/article/details/62058805)  

[Android视频开发基础(二)](https://blog.csdn.net/goodlixueyong/article/details/62447452)  

[Android视频开发基础(三)](https://blog.csdn.net/goodlixueyong/article/details/84711569)

开源的播放库ijkplayer

[Android视频开发基础(四)](https://blog.csdn.net/goodlixueyong/article/details/62447486)  

http-flv协议
直播协议: rtmp、 http-flv、 hls

[Android实现视频播放的3种实现方式](https://blog.csdn.net/liuzhi0724/article/details/81318816)  

[Android视频播放实现的三种办法](https://blog.csdn.net/wozuihaole/article/details/60867076)  
vitamio的library下载地址是：https://www.vitamio.org/Download/  
以上三种方法完整案例demo下载地址：http://download.csdn.net/detail/wozuihaole/9773883  


[这些优秀的音视频开源框架你值得收藏](http://blog.csdn.net/androidstarjack/article/details/68954614)  

[一个强悍而优美的Android视频播放器](https://blog.csdn.net/androidstarjack/article/details/69526279)  
GitHub链接下载：https://github.com/androidstarjack/MyGreatPalyerVideo  
~~~
        compile 'fm.jiecao:jiecaovideoplayer:5.5.2'

<fm.jiecao.jcvideoplayer_lib.JCVideoPlayerStandard
    android:id="@+id/videoplayer"
    android:layout_width="match_parent"
    android:layout_height="200dp"/>

送上一个播放地址：

http://www.jmzsjy.com/UploadFile/微课/地方风味小吃——宫廷香酥牛肉饼.mp4

http://flashmedia.eastday.com/newdate/news/2016-11/shznews1125-19.mp4

http://112.253.22.157/17/z/z/y/u/zzyuasjwufnqerzvyxgkuigrkcatxr/hc.yinyuetai.com/D046015255134077DDB3ACA0D7E68D45.flv

[https://wdl.wallstreetcn.com/41aae4d2-390a-48ff-9230-ee865552e72d]https://wdl.wallstreetcn.com/41aae4d2-390a-48ff-9230-ee865552e72d)

音乐地址：

http://o6wf52jln.bkt.clouddn.com/演员.mp3

http://abv.cn/music/红豆.mp3
~~~

Vitamio  
---

[Android视频框架--Vitamio](https://blog.csdn.net/hao54216/article/details/52437252)  
官网下载:   https://www.vitamio.org/Download/
Android Vitamio演示(Android Studio):  https://github.com/yixia/VitamioBundleStudio  
 https://www.vitamio.org/docs/  
关于官方帮助文档：https://www.vitamio.org/docs/Tutorial/2014/0210/29.html

[Android视频播放项目总结之 使用第三方Vitamio库，开发万能播放器(一)](https://blog.csdn.net/zhaihaohao1/article/details/45417571)  
Github上面：https://github.com/yixia

[Android 中的视频播放第三方库vitamio的导入的各种坑以及解决方法](https://blog.csdn.net/fucaijin/article/details/80948383)  

[安卓非常实用又坑多多的视频框架——Vitamio](https://blog.csdn.net/NKPDQZ/article/details/63690374)  

ijkplayer
---

[ijkplayer视频播放器](https://blog.csdn.net/weixin_41701790/article/details/81459387)  


[Android实现视频播放](https://blog.csdn.net/yaozhipu/article/details/80528503)  
~~~
implementation 'com.dou361.ijkplayer:jjdxm-ijkplayer:1.0.5'
PlayerView play;
String url = "https://vip.94kuyun.com/share/PcnG4qsmeZKV1ikR";
play = new PlayerView(this)
        .setTitle("什么")
        .setScaleType(PlayStateParams.fitparent)
        .hideMenu(true)
        .forbidTouch(false)
        .setPlaySource(url);
play.startPlay();
布局
<LinearLayout
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:orientation="vertical">

    <include
        layout="@layout/simple_player_view_player"
        android:layout_width="match_parent"
        android:layout_height="200dp"/>

</LinearLayout>

~~~

[Android上传附件（图片，视频，文档）](https://www.jianshu.com/p/caca4f68961d)  

[android 选择视频文件 上传到后台服务器](https://blog.csdn.net/d276031034/article/details/52652749)  

[Android实现上传本地或拍摄的视频到Bmob服务器](https://blog.csdn.net/xuanwo11/article/details/65440184)  

[关于android实时视频录制与上传](https://blog.csdn.net/lvjunwoaini/article/details/7035601)  

[Android 录制视频并上传](https://blog.csdn.net/wen_zheng/article/details/52056036)  

[Android实现本地视频+录制视频+视频压缩上传](https://blog.csdn.net/weixin_39706415/article/details/84636625)  

[七牛开发者中心](https://developer.qiniu.com/)  
https://developer.qiniu.com/pili/sdk/3734/android-short-video-sdk

[Android上传视频](https://blog.csdn.net/weixin_41701790/article/details/81977653)  

[Android多图上传](https://blog.csdn.net/weixin_41701790/article/details/82344938)  

[Picture Selector Library for Android or 多图片选择器](https://github.com/LuckSiege/PictureSelector)  




