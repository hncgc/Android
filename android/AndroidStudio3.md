Android Studio 3
---

升级AS3.0随记 
http://blog.csdn.net/iamzgx/article/details/72862509

迁移到Android Studio 3.0
http://blog.csdn.net/ncuboy045wsq/article/details/73521856

AndroidStudio3.0 Canary 的使用记录
http://blog.csdn.net/j550341130/article/details/72818066

Android studio 3.0上进行多渠道打包遇到的问题
http://blog.csdn.net/small_technical/article/details/72782671
-----------------------------------
Rendering Problems
Failed to load platform 
rendering library
--------------------------------
failed to load platform rendering library的解决方案   
http://blog.csdn.net/qq_37118873/article/details/78138163

----------------------------------------------
可视化的方式来编写界面
Android新特性介绍，ConstraintLayout完全解析   
http://blog.csdn.net/guolin_blog/article/details/53122387

compile 'com.android.support.constraint:constraint-layout:1.0.2'

安卓约束控件(ConstraintLayout)扁平化布局入门
http://www.jianshu.com/p/792d2682c538

----------------------------------------------------

多渠道打包之动态修改App名称，图标，applicationId，版本号，添加资源   
http://blog.csdn.net/abc6368765/article/details/52786509
https://github.com/AFinalStone/MultiChannel-master

Gradle 实战（1）—— 配置环境变量
http://blog.csdn.net/lw_power/article/details/51241187

AndroidStudio gradle配置
http://www.cnblogs.com/wxishang1991/p/5457878.html

[Android Studio系列(五)] Android Studio手动配置Gradle的方法   
http://blog.csdn.net/fuchaosz/article/details/51567808

Android构建与配置Gradle脚本综述
http://www.jianshu.com/p/49bb7fb43f90

本地安装gradle-3.3-all.zip
http://www.cnblogs.com/yasepix/p/6958105.html

Maven中央仓库信息速查
com.google.guava/guava/19.0 Guava: Google Core Libraries for Java maven依赖
http://maven.outofmemory.cn/com.google.guava/guava/19.0/

https://stackexchange.com/


android studio 更新 Gradle
http://www.orzapp.com/?p=269


github开源项目：https://github.com/google/guava/wiki/Release19

Android Studio使用笔记（1）使用android studio时避免每次启动都进行网络gradle sync的方法
http://blog.csdn.net/hwwlovejws/article/details/50888051


可视化的方式来编写界面

Android新特性介绍，ConstraintLayout完全解析   
http://blog.csdn.net/guolin_blog/article/details/53122387

compile 'com.android.support.constraint:constraint-layout:1.0.2'

Android ConstraintLayout详解
http://www.jianshu.com/p/a8b49ff64cd3


Butter Knife添加依赖 不生效 
http://blog.csdn.net/zheng548/article/details/51722973

ButterKnife的使用以及不能自动生成代码问题的解决
http://www.cnblogs.com/zhengjunfei/p/5910497.html

Android Butter Knife 框架——最好用的View注入
http://www.jianshu.com/p/9ad21e548b69
http://jakewharton.github.io/butterknife/

https://github.com/JakeWharton/butterknife

class ExampleActivity extends Activity {
  @BindView(R.id.user) EditText username;
  @BindView(R.id.pass) EditText password;

  @BindString(R.string.login_error) String loginErrorMessage;

  @OnClick(R.id.submit) void submit() {
    // TODO call server...
  }

  @Override public void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.simple_activity);
    ButterKnife.bind(this);
    // TODO Use fields...
  }
}
