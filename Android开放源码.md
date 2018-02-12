Android开放源码
===

[Xiaomi Open Source](https://github.com/XiaoMi)  

[几乎所有开源安卓app的列表](https://github.com/pcqpcq/open-source-android-apps)  

[Android开源库汇总](http://xybcoder.github.io/ANDROID/)  

[Android 开源项目分类汇总](https://github.com/Trinea/android-open-project)  


[android企业级商城源码](http://www.apkbus.com/thread-462905-1-1.html)  

[android砸金蛋](http://download.csdn.net/download/wt0731/5009525)  

[Android 原生 轮盘抽奖](http://www.apkbus.com/blog-851511-76989.html)  


[Android开发人员不得不收集的代码(持续更新中)](http://www.diycode.cc/projects/Blankj/AndroidUtilCode)  
https://github.com/Blankj/AndroidUtilCode  
```
Gradle:
compile 'com.blankj:utilcode:1.3.3'
Proguard
-keep class com.blankj.utilcode.** { *; }
-keep classmembers class com.blankj.utilcode.** { *; }
-dontwarn com.blankj.utilcode.**
```

[http://grepcode.com/ Android sdk源码](http://grepcode.com/search/?query=ActivityThread)  
https://github.com/huangkunkun/AndroidUtilCode  


[開源安卓](https://www.gitbook.com/book/yongjhih/feed/details)  
https://github.com/yongjhih/android-gitbook/


阿里云开源项目
-------------
http://code.taobao.org/project/explore/ 
http://code.taobao.org/newest/

http://code.taobao.org/p/YuanWen/diff/66/trunk/app/src/main/java/com/smile/yuanwen/fragment/DynamicDetailFragment.java
```
+
+    /**
+     * 填充webview内容
+     */
+    private void fillWebViewBody() {
+        StringBuffer body = new StringBuffer();
+        body.append(ThemeSwitchUtils.getWebViewBodyString());
+        body.append(UIHelper.WEB_STYLE + UIHelper.WEB_LOAD_IMAGES);
+
+        StringBuilder tweetbody = new StringBuilder(mDynamic.getBody());
+
+        String tweetBody = TextUtils.isEmpty(mDynamic.getImgSmall()) ? tweetbody
+                .toString() : tweetbody.toString() + "<br/><img src=\""
+                + mDynamic.getImgSmall() + "\">";
+        body.append(setHtmlCotentSupportImagePreview(tweetBody));
+
+        UIHelper.addWebImageShow(getActivity(), mContent);
+        // 封尾
+        body.append("</div></body>");
+        mContent.loadDataWithBaseURL(null, body.toString(), "text/html",
+                "utf-8", null);
+    }
+
+    /**
+     * 添加图片放大支持
+     *
+     * @param body
+     * @return
+     */
+    private String setHtmlCotentSupportImagePreview(String body) {
+        // 过滤掉 img标签的width,height属性
+        body = body.replaceAll("(<img[^>]*?)\\s+width\\s*=\\s*\\S+", "$1");
+        body = body.replaceAll("(<img[^>]*?)\\s+height\\s*=\\s*\\S+", "$1");
+        return body.replaceAll("(<img[^>]+src=\")(\\S+)\"",
+                "$1$2\" onClick=\"javascript:mWebViewImageListener.showImagePreview('"
+                        + mDynamic.getImgBig() + "')\"");
+    }
+

```
