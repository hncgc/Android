# Androidx

[AndroidX 概览](https://developer.android.google.cn/jetpack/androidx/)  

[迁移到 AndroidX](https://developer.android.google.cn/jetpack/androidx/migrate)  

[Androidx官方文档](https://developer.android.com/jetpack/androidx/versions)  



[一次解决找不到 android.support.v7.XXX 问题](https://www.jianshu.com/p/f0bbae225cac)  

~~~
    implementation "com.android.support:appcompat-v7:$supportVersion"
改为：
    implementation 'androidx.appcompat:appcompat:1.0.0'

<android.support.v7.widget.Toolbar
改为：
<androidx.appcompat.widget.Toolbar


import android.widget.Toolbar;
改为：
import androidx.appcompat.widget.Toolbar;
~~~

[Android:你好,androidX！再见,android.support](https://www.jianshu.com/p/41de8689615d)  

~~~
    implementation 'com.android.support.constraint:constraint-layout:2.0.1'
    implementation "com.android.support:support-v4:28.0.0"
    implementation "com.android.support:recyclerview-v7:$supportVersion"
    implementation "com.android.support:appcompat-v7:$supportVersion
    implementation "com.android.support:cardview-v7:$supportVersion"
    implementation "com.android.support:design:$supportVersion"
迁移为：
    implementation 'androidx.constraintlayout:constraintlayout:2.0.1'
    implementation 'androidx.legacy:legacy-support-v4:1.0.0'
    implementation 'androidx.recyclerview:recyclerview:1.1.0'
    implementation 'androidx.appcompat:appcompat:1.2.0'
    implementation 'androidx.cardview:cardview:1.0.0'
    implementation 'com.google.android.material:material:1.2.1'
    
F:\ReciteWords\gradle.properties

android.useAndroidX=true
# Automatically convert third-party libraries to use AndroidX
android.enableJetifier=true

~~~

[Android AndroidX的迁移](https://www.jianshu.com/p/7dc111353328)   

[Androidx迁移——弃用support库指南](https://www.jianshu.com/p/1113c81ad57f)   

[详解Android Studio3.5及使用AndroidX的一些坑](https://www.jb51.net/article/173941.htm)   

[慎用 AndroidX 库](https://www.jianshu.com/p/641d683f78d5)   

[Androidx的使用](https://www.jianshu.com/p/6c5c17fc574a)    

[AndroidX从入门到放弃...](https://www.jianshu.com/p/ee3484c8eb9a)  

[迁移到 androidx后 android.support.v4.content.FileProvider找不到问题](https://blog.csdn.net/zcl875921355/article/details/88053119)  
~~~
android.support.v4.content.FileProvider修改为
androidx.core.content.FileProvider
~~~

[android 解决setbackgrounddrawable过时](https://blog.csdn.net/bzlj2912009596/article/details/79662398)   

[在JAVA中注解@SuppressWarnings("deprecation")的Deprecation是什么意思](https://blog.csdn.net/Jerry_an/article/details/88104184)  
~~~
过期的
@SuppressWarnings(“deprecation”)
表示不检测过期的方法

假设：
List list = {“1”,“2”} ;
@SuppressWarnings(“deprecation”)
list.count();
在这里假设 list.count() 这个方法是被弃用了的方法，加上这个注解就表示不去检测这个方法是否被弃用
~~~

[@SuppressWarnings注解用法详解](https://blog.csdn.net/tiantangdizhibuxiang/article/details/79012178)  
~~~
·   @SuppressWarnings("unchecked")
  告诉编译器忽略 unchecked 警告信息，如使用List，ArrayList等未进行参数化产生的警告信息。
·   @SuppressWarnings("serial")
  如果编译器出现这样的警告信息：The serializable class WmailCalendar does not declare a static final serialVersionUID field of type long，使用这个注释将警告信息去掉。
·  @SuppressWarnings("deprecation")
  如果使用了使用@Deprecated注释的方法，编译器将出现警告信息。使用这个注释将警告信息去掉。
·   @SuppressWarnings("unchecked", "deprecation")
  告诉编译器同时忽略unchecked和deprecation的警告信息。
·   @SuppressWarnings(value={"unchecked", "deprecation"})
  等同于@SuppressWarnings("unchecked", "deprecation")

~~~












