# Audio

[Android音频技术开发之基础知识](https://www.jianshu.com/p/fd31aba3b2eb)  

[android 音频总结](https://www.jianshu.com/p/5389a9abe2b9)  

[Android端本地音乐播放器（一）---前言](https://blog.csdn.net/lvdoujack/article/details/84545289)  

[Android端本地音乐播放器（二）---应用主界面的实现](https://blog.csdn.net/lvdoujack/article/details/106447062)  

[Android端本地音乐播放器（三）---播放逻辑的控制方法](https://blog.csdn.net/lvdoujack/article/details/107523659)  

[Android怎样实现控制第三方音乐播放器暂停、播放](https://blog.csdn.net/Evahuangchen/article/details/53321670)  

[android实现音乐播放器(进度条)](https://blog.csdn.net/bfboys/article/details/53156119)  

[Android之MediaPlayer播放音乐并实现进度条实例](https://blog.csdn.net/rhljiayou/article/details/7110258)  

[android 边下边播放mp3完美实现（有缓冲和播放进度效果）](https://download.csdn.net/download/lsong89/7243497)  

[浅谈《MediaPlayer》加载进度定时刷新](https://blog.csdn.net/u014115577/article/details/47442377)  




[Android 音乐播放器](https://www.jianshu.com/p/72c4788433fb)  

~~~
            File file = new File(Environment.getExternalStorageDirectory(),"outside_the_window.mp3");
            if(file == null) //想要添加判断 是否找到music.map3
                Toast.makeText(getContext(),"the sd have not music.mp3",Toast.LENGTH_SHORT).show();
            mMediaPlayer.setDataSource(file.getPath());//指定音频路径
            Log.d(TAG, "File = " + file.getPath());
            mMediaPlayer.prepare();

2020-09-08 00:57:58.113 32444-32444/com.mywords.app D/CognitionFragment: File = /storage/emulated/0
2020-09-08 00:57:58.116 32444-32444/com.mywords.app D/CognitionFragment: File = /storage/emulated/0/outside_the_window.mp3

~~~

[Android学习--Assets资源文件读取及AssetManager介绍](https://www.cnblogs.com/jpfss/p/9876370.html)   

[Android开发之assets目录下资源使用总结](https://www.cnblogs.com/jpfss/p/9876384.html)  

[播放Assets目录下的音乐文件](https://blog.csdn.net/peachs885090/article/details/82985458)  

~~~
 MediaPlayer mediaPlayer=new MediaPlayer();
 AssetFileDescriptor afd = getAssets().openFd("musics/outside_the_window.mp3");
 mediaPlayer.setDataSource(afd.getFileDescriptor());
 mediaPlayer.prepare();
 mediaPlayer.start();

mMediaPlayer.setDataSource(afd.getFileDescriptor())无效

            AssetFileDescriptor afd = getActivity().getAssets().openFd("musics/Australian.mp3");
            Log.d(TAG, "File = " + afd.getFileDescriptor());
            mMediaPlayer.setDataSource(afd.getFileDescriptor());
            mMediaPlayer.prepare();
            
2020-09-08 00:57:58.131 32444-32444/com.mywords.app D/CognitionFragment: File = java.io.FileDescriptor@65ee0c6
            
mMediaPlayer.setDataSource(afd.getFileDescriptor(), afd.getStartOffset(), afd.getLength())成功：

            AssetManager asm = getContext().getResources().getAssets();
            AssetFileDescriptor afd = asm.openFd("Australian.mp3");
            Log.d(TAG, "FilePath = " + afd.getFileDescriptor());
            // mMediaPlayer.setDataSource(afd.getFileDescriptor());
            mMediaPlayer.setDataSource(afd.getFileDescriptor(), afd.getStartOffset(), afd.getLength());
            mMediaPlayer.prepare();
            mMediaPlayer.play();

2020-09-08 09:57:49.832 18192-18192/com.mywords.app D/CognitionFragment: FilePath = java.io.FileDescriptor@6f95f08

成功
            AssetManager asm = getContext().getResources().getAssets();
            //AssetFileDescriptor afd = asm.openFd("Australian.mp3");
            AssetFileDescriptor afd = asm.openFd("musics/outside_the_window.mp3");
            Log.d(TAG, "FilePath = " + afd.getFileDescriptor());
            // mMediaPlayer.setDataSource(afd.getFileDescriptor());
            mMediaPlayer.setDataSource(afd.getFileDescriptor(), afd.getStartOffset(), afd.getLength());
            mMediaPlayer.prepare();

afd.getFileDescriptor() 每次不一样

2020-09-08 10:22:28.298 23221-23221/com.mywords.app D/CognitionFragment: FilePath = java.io.FileDescriptor@7c525f4
2020-09-08 10:22:35.870 23221-23221/com.mywords.app D/CognitionFragment: FilePath = java.io.FileDescriptor@7135f09
2020-09-08 10:22:49.723 23221-23221/com.mywords.app D/CognitionFragment: FilePath = java.io.FileDescriptor@5db1997


~~~

[播放本地资源assets音频](https://blog.csdn.net/weixin_42376563/article/details/81145300)  

[android播放assets目录下的wav,MP3音频](http://www.voidcn.com/article/p-adfpivlw-yh.html)  

[【Android实战】播放assets或者raw文件夹下的视频文件](https://blog.csdn.net/s003603u/article/details/49700547)  
~~~
1）assets文件夹下
AssetFileDescriptor afd = getAssets().openFd("guide_video.mp4");
mediaPlayer.setDataSource(afd.getFileDescriptor(), afd.getStartOffset(), afd.getLength())；

（2）raw文件夹下
Uri mUri = Uri.parse("android.resource://" + getPackageName() + "/"+ R.raw.guide_video);
mediaPlayer.setDataSource(this, mUri);

有时候会播放不了，mediaPlayer  prepare报错，要先看一下手机的系统播放器是否支持播放，再继续找问题
~~~

[Android 使用MediaPlayer播放assets或者raw目录的音频文件](https://blog.csdn.net/liangtianmeng/article/details/107299075)  

[Android 使用MediaPlayer播放assets或者raw目录的音频文件](https://blog.csdn.net/qq_31939617/article/details/80491552)  

[Android之raw](https://www.jianshu.com/p/ef5bb5ccd88c)  

[Android raw 目录 和 assets 目录](https://www.jianshu.com/p/f8f5c3ab5bf1)  

[Android中asset文件夹与raw文件夹的区别深入解析](https://www.jb51.net/article/38531.htm)  

[Android开发之资源目录assets与res/raw的区别分析](https://www.jb51.net/article/77904.htm)  

[android 将res/raw下的文件保存至SD卡](https://blog.csdn.net/wuhongqi0012/article/details/21954321)  

[Android 拷贝文件夹到sdcard路径下](https://blog.csdn.net/lancelots/article/details/84108367)  

[Android 手机sdcard目录或文件的拷贝、移动、删除(递归)](https://blog.csdn.net/lyyn_stickto/article/details/51858379)  

[Android设备与外接U盘实现数据文件夹拷贝到android设备](https://blog.csdn.net/only_you_zj/article/details/80175254)





















