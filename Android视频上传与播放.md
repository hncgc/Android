Android视频上传与播放
===

[Android视频开发基础(一）](https://blog.csdn.net/goodlixueyong/article/details/62058805)  

[Android视频开发基础(二)](https://blog.csdn.net/goodlixueyong/article/details/62447452)  

[Android视频开发基础(三)](https://blog.csdn.net/goodlixueyong/article/details/84711569)

[Android视频开发基础(四)](https://blog.csdn.net/goodlixueyong/article/details/62447486)  

http-flv协议
直播协议: rtmp、 http-flv、 hls

[Android实现视频播放的3种实现方式](https://blog.csdn.net/liuzhi0724/article/details/81318816)  

[Android视频播放实现的三种办法](https://blog.csdn.net/wozuihaole/article/details/60867076)  
vitamio的library下载地址是：https://www.vitamio.org/Download/  
以上三种方法完整案例demo下载地址：http://download.csdn.net/detail/wozuihaole/9773883  


[这些优秀的音视频开源框架你值得收藏](http://blog.csdn.net/androidstarjack/article/details/68954614)  

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

开源的播放库 ijkplayer的github地址: https://link.jianshu.com/?t=https://github.com/Bilibili/ijkplayer  

完整版的ijkplayer  https://github.com/thiagooo0/lmnplayer  

[ijkplayer视频播放器](https://blog.csdn.net/weixin_41701790/article/details/81459387)  

[Android 超好用的播放器——ijkplayer](https://www.jianshu.com/p/c5d972ab0309)  

[开源播放器 ijkplayer (一) ：使用Ijkplayer播放直播视频](http://www.cnblogs.com/renhui/p/6420140.html)  

[Android 实现视屏播放器、边播边缓存功能、外加铲屎（IJKPlayer）](https://www.jianshu.com/p/9fe377dd9750)  

GSYVideoPlayer
---
[GSYVideoPlayer项目说明](https://www.jianshu.com/p/49831e5e2cd6)  

[基于IJKPlayer（兼容系统MediaPlayer与EXOPlayer2），实现了多功能的视频播放器](https://github.com/CarGuo/GSYVideoPlayer)  

[Android蹲坑的疑难杂症集锦一](https://www.jianshu.com/p/e015269e3478)  

[Android蹲坑的疑难杂症集锦（兼Gradle） 二](https://www.jianshu.com/p/86e4b336c17d)  

JieCaoVideoPlayer 节操 (JiaoZiVideoPlayer 饺子)
---
[Android JieCaoVideoPlayer 使用入门指南](https://blog.csdn.net/yaya_xiong/article/details/75213346)  
github 地址：JieCaoVideoPlayer: https://github.com/lipangit/JieCaoVideoPlayer  最正宗的  

[jiecaovideoplayer最简单的使用](https://blog.csdn.net/Star_Q/article/details/78849610)  

[仿今日头条视频播放JieCaoVideoPlayer](https://blog.csdn.net/w_l_s/article/details/53132179)  

[高仿今日头条ListView视频播放和优酷视频播放悬浮窗](https://github.com/open-android/JieCaoVideoPlayer) 
https://github.com/open-android/JieCaoVideoPlayer

[视频播放---jiecaovideoplayer的使用](https://blog.csdn.net/u012216899/article/details/57186467)  

[详解demo中自定义播放器的实现](https://github.com/lipangit/JiaoZiVideoPlayer/wiki/%E8%AF%A6%E8%A7%A3demo%E4%B8%AD%E8%87%AA%E5%AE%9A%E4%B9%89%E6%92%AD%E6%94%BE%E5%99%A8%E7%9A%84%E5%AE%9E%E7%8E%B0)  

[Android中节操播放器JieCaoVideoPlayer使用](https://blog.csdn.net/zhaihaohao1/article/details/78029766)  
转载地址：https://github.com/lipangit/JiaoZiVideoPlayer  
参考视频：http://ke.atguigu.com/course/149/learn#lesson/1978  
~~~
1.添加类库
compile 'cn.jzvd:jiaozivideoplayer:6.0.0'
2.添加布局

<cn.jzvd.JZVideoPlayerStandard
    android:id="@+id/videoplayer"
    android:layout_width="match_parent"
    android:layout_height="200dp"/>
    
3.设置视频地址、缩略图地址、标题

JZVideoPlayerStandard jzVideoPlayerStandard = (JZVideoPlayerStandard) findViewById(R.id.videoplayer);
jzVideoPlayerStandard.setUp("http://jzvd.nathen.cn/c6e3dc12a1154626b3476d9bf3bd7266/6b56c5f0dc31428083757a45764763b0-5287d2089db37e62345123a1be272f8b.mp4"
                            , JZVideoPlayerStandard.SCREEN_LAYOUT_NORMAL, "嫂子闭眼睛");
jzVideoPlayerStandard.thumbImageView.setImage("http://p.qpic.cn/videoyun/0/2449_43b6f696980311e59ed467f22794e792_1/640");

~~~



[一个强悍而优美的Android视频播放器 JieCaoVideoPlayer](https://blog.csdn.net/androidstarjack/article/details/69526279)  
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

[Android 拍摄（横\竖屏）视频的懒人之路](https://www.jianshu.com/p/752f0dd842f8)  

[视频直播技术资源整理](https://www.cnblogs.com/renhui/p/6394988.html)  

[几个不错的Android开源音视频播放器](https://blog.csdn.net/Guofengpu/article/details/72911846)  

[【Android 视频，音频开源框架】](https://blog.csdn.net/da_caoyuan/article/details/73188626)  


[快速将Android项目发布的JCenter](https://www.jianshu.com/p/748d59aa6567)  

[通用RecylerAdapter，内置XRecyclerView，兼容上下拉与动画，高复用，一个Adapter通用所有页面，支持空页面，懒人专属](https://www.jianshu.com/p/9c9aede9a19a)  

[让Gradle放飞你的apk构建](https://www.jianshu.com/p/50134707bc46)  




