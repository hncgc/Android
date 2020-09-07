# Androidx

[Androidx官方文档](https://developer.android.com/jetpack/androidx/versions)

[Android:你好,androidX！再见,android.support](https://www.jianshu.com/p/41de8689615d)  

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











