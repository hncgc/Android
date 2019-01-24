Android视频压缩
===

[android视频压缩(七牛短视频-转码功能)](https://blog.csdn.net/qq_31796651/article/details/79154072)  
~~~
demoApk下载（自己将官方demo打了一个包）：链接:[点击打开链接](https://pan.baidu.com/s/1kVZPqEb) 密码: rxkx
官网链接：https://developer.qiniu.com/pili/sdk/3734/short-video-android-sdk#6
sdk下载地址：https://developer.qiniu.com/sdk#official-sdk
~~~

[android视频压缩：兼容7.0版本(ffmpeg)](https://blog.csdn.net/qq_35373333/article/details/77765605)  
github地址：https://github.com/jczmdeveloper/XCVideoCompressor  
ffmpeg命令参数详解：https://segmentfault.com/a/1190000002502526  
再放一个官网的连接：http://ffmpeg.org/  

[视频录制 视频压缩（使用FFMpeg）Android Video Recorder/Video Compressor ](https://github.com/chenzhihui28/VideoRecorderAndCompressor)  
https://github.com/chenzhihui28/VideoRecorderAndCompressor

[Android 视频压缩](https://blog.csdn.net/Lamphogani/article/details/80513452)  
使用开源库SiliCompressor，最终采用的一种方案  
开源库地址 https://github.com/Tourenathan-G5organisation/SiliCompressor  
~~~
public static void compressVideo(Context mContext, final String videoPath) {
    try {
        String newVideoPath = SiliCompressor.with(mContext).compressVideo(videoPath,
                new File(Environment.getExternalStoragePublicDirectory(Environment.DIRECTORY_PICTURES), TAG).getPath(),
                960, 544, 1000000);
    } catch (URISyntaxException e) {
        e.printStackTrace();
    }
}
~~~

[在Android上使用FFmpeg压缩视频](https://www.jianshu.com/p/ceaa286d8aff)  
https://github.com/voiddog/FFmpeg-Android  

[Android本地视频压缩方案](https://www.jianshu.com/p/4f82b058c8ec)  
开源库：https://github.com/WritingMinds/ffmpeg-android-java  

----------------

[Android视频压缩（硬解）](https://blog.csdn.net/qq_36421691/article/details/79113392)  
https://github.com/wuxiaoqiang625/VideoCompress  

[VideoRecorderAndCompressor(FFMpeg压缩)](https://github.com/chenzhihui28/VideoRecorderAndCompressor)  
https://github.com/chenzhihui28/VideoRecorderAndCompressor  

[SiliCompressor(没有progress)](https://github.com/Tourenathan-G5organisation/SiliCompressor)  
https://github.com/Tourenathan-G5organisation/SiliCompressor  

[选择本地视频通过](https://github.com/LuckSiege/PictureSelector)  
https://github.com/LuckSiege/PictureSelector  

[VideoCompressor(有progress)](https://github.com/fishwjy/VideoCompressor)  
https://github.com/fishwjy/VideoCompressor  

SiliCompressor
---

[使用开源库SiliCompressor对视频进行压缩处理](https://www.jianshu.com/p/b3b7c73893be)  
~~~
<1> 视频压缩压缩视频文件并返回新视频的文件路径
StringfilePath=SiliCompressor.with(Context).compressVideo(videoPath, destinationDirectory);
<2> 图片压缩压缩图像并返回新图像的文件路径
StringfilePath=SiliCompressor.with(Context).compress(imagePath, destinationDirectory);
压缩图像并在删除源图像时返回新图像的文件路径
StringfilePath=SiliCompressor.with(Context).compress(imagePath, destinationDirectory,true);
~~~

[Silicompressor源码学习（一） 基本架构和图片压缩](https://blog.csdn.net/zhang___yong/article/details/79697146)  

[Android 视频压缩](https://blog.csdn.net/lamphogani/article/details/80513452)  
~~~
public static void compressVideo(Context mContext, final String videoPath) {
    try {
        String newVideoPath = SiliCompressor.with(mContext).compressVideo(videoPath,
                new File(Environment.getExternalStoragePublicDirectory(Environment.DIRECTORY_PICTURES), TAG).getPath(),
                960, 544, 1000000);
    } catch (URISyntaxException e) {
        e.printStackTrace();
    }
}

~~~


----------------

[Android视频录制与压缩](https://www.jianshu.com/p/cdae476087d4)  

[android 本地视频压缩](https://blog.csdn.net/fangjingjingll/article/details/79808744)  
~~~
1.https://download.csdn.net/download/qq_33129625/9901480  （没有整合成功）
2.http://www.jb51.net/article/133902.htm
3.https://github.com/chenzhihui28/VideoRecorderAndCompressor
4.https://blog.csdn.net/qq_31796651/article/details/79154072
5.https://blog.csdn.net/qq_35373333/article/details/79564991


可以用
https://github.com/jczmdeveloper/XCVideoCompressor  （github）
https://blog.csdn.net/qq_36421691/article/details/79113392 （整合步骤）
https://github.com/wuxiaoqiang625/VideoCompress

~~~

[Android 使用自带的MediaCodec 框架进行本地视频压缩，速度嗖嗖的，亲测有效！！！](https://github.com/tangpeng/VideoCompressor)  
https://github.com/tangpeng/VideoCompressor

[Android使用FFmpeg框架进行本地视频压缩，扩展性高，效果好，亲测有效！！！](https://github.com/tangpeng/FFmpegDemo)  

[android 视频裁切，拼接和合成，添加滤镜，修改视频播放速度，插入音频，添加文字，贴图，标注](https://www.jianshu.com/p/b2b35d0e7bce)  
https://github.com/tangpeng/Filmr

[Android 集成 FFmpeg (一) 基础知识及简单调用](https://blog.csdn.net/yhaolpz/article/details/76408829)  

[Android 集成 FFmpeg (二) 以命令方式调用 FFmpeg](https://blog.csdn.net/yhaolpz/article/details/77146156)  

[Android 集成 FFmpeg (三) 获取 FFmpeg 执行进度](https://blog.csdn.net/yhaolpz/article/details/77146156)  



[Android从相册选取视频](https://www.cnblogs.com/wzqnxd/p/10011664.html)  

[Android视频压缩并且上传](https://blog.csdn.net/heishuai123/article/details/84634834)  
地址：https://download.csdn.net/download/heishuai123/10816897  
github链接地址：https://github.com/Tourenathan-G5organisation/SiliCompressor  
~~~
new Thread() {
            @Override
            public void run() {
                super.run();
                try {
                    /**
                     * 视频压缩
                     * 第一个参数:视频源文件路径
                     * 第二个参数:压缩后视频保存的路径
                     */
                    String comPressPath = SiliCompressor.with(getActivity()).compressVideo(filePath, dirPath);
//                    if (!StringUtil.isEmpty(comPressPath)) {
//                        notCompressedVideo.setCompressPath(comPressPath);
//                        compressVideo();
//                    } else {
//                        stopCompress("失败");
//                    }
                } catch (URISyntaxException e) {
                    e.printStackTrace();
                }
            }
        }.start();
        
注意：1，就是要放到子线程执行
     2. 第二个参数是压缩后保存的路径，注意这个地址一定要是你目录中存在的
     
     String path= SiliCompressor.with(activity).compressVideo(videopath ,Environment.getExternalStoragePublicDirectory(Environment.DIRECTORY_PICTURES).getPath());
~~~

[Android实现本地视频+录制视频+视频压缩上传](https://blog.csdn.net/weixin_39706415/article/details/84636625)  


[Android实现视频硬编码](https://blog.csdn.net/matrix_laboratory/article/details/58237903)  

--------------


阿里云帮助文档
---

[阿里云帮助文档](https://help.aliyun.com/?spm=5176.8050858.1280361.4.2bb0a1a9LTLtS6)  

[视频点播](https://help.aliyun.com/product/29932.html?spm=a2c4g.750001.17.1.1b6e7b13aoEHbG)  

[媒体处理](https://help.aliyun.com/product/29194.html?spm=a2c4g.750001.17.3.1b6e7b13RgMKcO)  

[提交转码作业](https://help.aliyun.com/document_detail/29208.html?spm=a2c4g.11174283.3.3.72c0556exHnpCr)  

[Android 短视频SDK](https://help.aliyun.com/document_detail/99289.html?spm=a2c4g.11174283.3.3.6579149bD7j19d)  




--------------

[完美解决Android 6.0+运行时权限问题](https://www.jianshu.com/p/52795b5dab3a)  
https://github.com/tangpeng/EsayPermissions

[Android创建本地文件夹、创建本地文件以及访问本地文件](https://blog.csdn.net/s1455364690/article/details/79477536)  
https://github.com/1455364690/Android_LocalDocument  
~~~
    public void newDirectory(String _path,String dirName){
        File file = new File(_path+"/"+dirName);
        try {
            if (!file.exists()) {
                file.mkdir();
            }
        }catch (Exception e){
            e.printStackTrace();
        }
    }
~~~

[android获取存储目录(路径)的几种方式和注意事项](https://blog.csdn.net/yan_startwith2015/article/details/77931389)  

[android获取各种系统路径的方法](https://blog.csdn.net/qq_26296197/article/details/51909423)  

[android 8.0系统创建文件夹失败](https://blog.csdn.net/liuxiaopang520/article/details/84032595)  

--------------------------

[Android 写文件,及手机和SD卡根目录](https://www.cnblogs.com/onone/articles/6496047.html)  

[android 删除整个文件夹里面的文件](https://blog.csdn.net/m940034240/article/details/76473770)  
~~~
使用时记得添加操作文件的权限！
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
<uses-permission android:name="android.permission.MOUNT_UNMOUNT_FILESYSTEMS" />
<uses-permission android:name="android.permission.WRITE_MEDIA_STORAGE" />

//flie：要删除的文件夹的所在位置
private void deleteFile(File file) {
    if (file.isDirectory()) {
        File[] files = file.listFiles();
        for (int i = 0; i < files.length; i++) {
            File f = files[i];
            deleteFile(f);
        }
        file.delete();//如要保留文件夹，只删除文件，请注释这行
    } else if (file.exists()) {
        file.delete();
    }
}
~~~

[Android删除文件夹（文件夹以及文件夹下所有的文件）](https://www.cnblogs.com/zhangfeitao/p/6733872.html)  

[java android 删除文件和文件夹的函数__函数](https://yq.aliyun.com/ziliao/276447)  

[android 获取本地缓存文件大小，删除功能](https://blog.csdn.net/huang15984/article/details/53103146)  

[android 获取文件夹、文件的大小 以B、KB、MB、GB 为单位](https://blog.csdn.net/qq_34329508/article/details/55101635)  


[Android笔记:存储相关,getExternalCacheDir, getExternalFilesDir,getExternalStorageDirectory等](http://blog.51cto.com/glblong/1699245)  
~~~
File cacheDir = mContext.getExternalCacheDir();
if(null != cacheDir){
   mCacheDirPath = cacheDir.getAbsolutePath() + "/images/";
}


if(TextUtils.isEmpty(mCacheDirPath)){
   if(Environment.MEDIA_MOUNTED.equals(Environment.getExternalStorageState())){
      mCacheDirPath = Environment.getExternalStorageDirectory().getPath() + "/Android/data/com.meiyaapp.meiya/cache/images/";
   }else{
      Toast.makeText(mContext,"SD卡状态错误,请调整后重试哦。",Toast.LENGTH_SHORT).show();
   }
}
~~~

[getExternalCacheDir getCacheDir getExternalStorageDirectory 区别](https://blog.csdn.net/LOLYIKU/article/details/81628771)  

~~~
记录下：

File externalCacheDir = getExternalCacheDir();
File cacheDir = getCacheDir();
File externalStorageDirectory = Environment.getExternalStorageDirectory();
这个三个文件，getAbsolutePath（）之后，获取绝对路径；

1）getExternalCacheDir()；一般文件路径： /storage/emulated/0/Android/data/com.common.dn_jni_lsn9/cache

2）getCacheDir()；一般路径：/data/user/0/com.common.dn_jni_lsn9/cache

3）getExternalStorageDirectory()；一般路径：/storage/emulated/0

相对而言，SD卡存在的时候，作为Android开发人员，应该把自己的文件操作，在第一个的相对的目录下，因为这个目录下操作，当当前App卸载的时候，也会随着清理掉；当SD卡不存在用第二种也会被清掉；第三种这里只是比对下，路径就是sd卡根目录，如果你在这个里面直接新建文件是不会被清理掉的，不建议使用；

了解更多参考：https://blog.csdn.net/a910626/article/details/51470866这里有一些不常用的路径，应用开发没有特殊需求，几乎不用；
~~~

[getCacheDir()、getFilesDir()、getExternalFilesDir()、getExternalCacheDir()的作用](https://blog.csdn.net/a910626/article/details/51470866)  
~~~
Environment.getDataDirectory() = /data
Environment.getDownloadCacheDirectory() = /cache
Environment.getExternalStorageDirectory() = /mnt/sdcard
Environment.getExternalStoragePublicDirectory(“test”) = /mnt/sdcard/test
Environment.getRootDirectory() = /system
getPackageCodePath() = /data/app/com.my.app-1.apk
getPackageResourcePath() = /data/app/com.my.app-1.apk
getCacheDir() = /data/data/com.my.app/cache
getDatabasePath(“test”) = /data/data/com.my.app/databases/test
getDir(“test”, Context.MODE_PRIVATE) = /data/data/com.my.app/app_test
getExternalCacheDir() = /mnt/sdcard/Android/data/com.my.app/cache
getExternalFilesDir(“test”) = /mnt/sdcard/Android/data/com.my.app/files/test
getExternalFilesDir(null) = /mnt/sdcard/Android/data/com.my.app/files
getFilesDir() = /data/data/com.my.app/files
~~~

[Android 缓存目录 Context.getExternalFilesDir()和Context.getExternalCacheDir()方法](https://blog.csdn.net/zhaoyanjun6/article/details/72283289)  
















