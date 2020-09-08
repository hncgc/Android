# Audio

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

[]






