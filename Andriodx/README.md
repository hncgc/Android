# Androidx

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
~~~











