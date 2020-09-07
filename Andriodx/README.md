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

[]()   







