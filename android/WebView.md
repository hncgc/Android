WebView
---
[oschina-app源码解析-webview重组html](http://blog.csdn.net/xiangxue336/article/details/20062347)  

[Android实现点击WebView界面中图片滑动浏览与保存图片功能](http://www.jb51.net/article/112028.htm)  

[从WebView中点击一张图片，转换成一个可缩放，可旋转的图片。](http://www.jianshu.com/p/e24ee6d67f01)  
https://segmentfault.com/t/android  
http://code.taobao.org/p/YuanWen/src/trunk/  

[android webview里设置cookie](http://blog.csdn.net/encienqi/article/details/7912733)  

[[Android] WebView删除缓存](http://blog.csdn.net/s278777851/article/details/6534316)  
1.删除保存于手机上的缓存.
    // clear the cache before time numDays
    private int clearCacheFolder(File dir, long numDays) {
        int deletedFiles = 0;
        if (dir!= null && dir.isDirectory()) {
            try {
                for (File child:dir.listFiles()) {
                    if (child.isDirectory()) {
                        deletedFiles += clearCacheFolder(child, numDays);
                    }
                    if (child.lastModified() < numDays) {
                        if (child.delete()) {
                            deletedFiles++;
                        }
                    }
                }
            } catch(Exception e) {
                e.printStackTrace();
            }
        }
        return deletedFiles;
    }

com.xxxx.app.ui.webview.OpenWebActivity.class

    @Override
    protected void onDestroy() {
        super.onDestroy();
        ////删除此时之前的缓存
        clearCacheFolder(OpenWebActivity.this.getCacheDir(), System.currentTimeMillis());
    }

2. 打开关闭使用缓存：

    优先使用缓存，WebView.getSettings().setCacheMode(WebSettings.LOAD_CACHE_ELSE_NETWORK);

    不使用缓存，WebView.getSettings().setCacheMode(WebSettings.LOAD_NO_CACHE);


[Android Webview清除缓存和Cookie](http://blog.csdn.net/ronaldong99/article/details/40392847)  

