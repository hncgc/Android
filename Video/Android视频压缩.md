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

----------------

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


--------------

[完美解决Android 6.0+运行时权限问题](https://www.jianshu.com/p/52795b5dab3a)  
https://github.com/tangpeng/EsayPermissions












