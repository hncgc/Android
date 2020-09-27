LitePal
---

[LitePal的简单使用[一]](https://blog.csdn.net/wj9966/article/details/80695207)  

[Android数据库框架 - LitePal学习笔记](https://www.jianshu.com/p/bc68e763c7a2)  

GitHub：https://github.com/LitePalFramework/LitePal

郭霖       https://github.com/guolindev  

          《第一行代码 第2版》全书源代码  

[LitePal详解](http://blog.csdn.net/fuzhongbin/article/details/51217944)  

[开源数据库 LitePal 学习，强大好使的 CRUD](https://segmentfault.com/p/1210000008884257/read)  

[Litepal使用详解](https://blog.csdn.net/pigdreams/article/details/69330946)  



GreenDao3.0
---

[GitHub项目地址](https://github.com/greenrobot/greenDAO)  

[greenDAO官方文档](http://greenrobot.org/greendao/documentation)  

GreenDao托管地址：https://github.com/greenrobot/greenDAO

官方文档：http://greenrobot.org/greendao/documentation/updating-to-greendao-3-and-annotations

[greendao使用详解](https://blog.csdn.net/yang_niuxxx/article/details/88851489)  

[greenDAO数据本地化](https://www.jianshu.com/p/c0015f0e9e73)  

[GreenDao 3.X之注解](https://blog.csdn.net/IO_Field/article/details/52213972)  

[GreenDao 3.X之基本使用](https://blog.csdn.net/io_field/article/details/52214099)  

GreenDao3.0简单使用
http://www.jianshu.com/p/4986100eff90
http://greenrobot.org/greendao/
https://github.com/anye0803/GreenDao/

GreenDao 3.0采用注解的方式来定义实体类，通过gradle插件生成相应的代码。

F:\pccb_app_3_1_6_new\app\build.gradle

apply plugin: 'org.greenrobot.greendao'

自定义路径:
    greendao {
        schemaVersion 1
        daoPackage 'com.pccb.app.greendao.gen'
        targetGenDir 'src/main/java'
    }
schemaVersion--> 指定数据库schema版本号，迁移等操作会用到;
daoPackage --> dao的包名，包名默认是entity所在的包；
targetGenDir --> 生成数据库文件的目录;

    compile 'org.greenrobot:greendao:3.2.2'
    compile 'org.greenrobot:greendao-generator:3.2.2'

F:\pccb_app_3_1_6_new\build.gradle

buildscript {
    repositories {
        jcenter()
        mavenCentral()
    }

    dependencies {
......
        classpath 'org.greenrobot:greendao-gradle-plugin:3.2.2'
......
    }

1. 增

mUser = new User((long)2,"anye3");
mUserDao.insert(mUser);//添加一个

2. 删

mUserDao.deleteByKey(id);

3. 改

mUser = new User((long)2,"anye0803");
mUserDao.update(mUser);

4. 查

List<User> users = mUserDao.loadAll();
String userName = "";
for (int i = 0; i < users.size(); i++) {
    userName += users.get(i).getName()+",";
}
mContext.setText("查询全部数据==>"+userName);


greendao中的注解

(一) @Entity 定义实体
@nameInDb 在数据库中的名字，如不写则为实体中类名
@indexes 索引
@createInDb 是否创建表，默认为true,false时不创建
@schema 指定架构名称为实体
@active 无论是更新生成都刷新
(二) @Id
(三) @NotNull 不为null
(四) @Unique 唯一约束
(五) @ToMany 一对多
(六) @OrderBy 排序
(七) @ToOne 一对一
(八) @Transient 不存储在数据库中
(九) @generated 由greendao产生的构造函数或方法

greenDAO 3.2 初探
http://blog.csdn.net/zone_/article/details/69054997

GreenDao 3.X之注解
http://blog.csdn.net/io_field/article/details/52213972

GreenDao 3.X之基本使用
http://blog.csdn.net/io_field/article/details/52214099

Gradle各版本下载地址：
https://pan.baidu.com/s/1pLEkm4F?errno=0&errmsg=Auth%20Login%20Sucess&&bduss=&ssnerror=0#list/path=%2FAndroid%2FDeveloper%20Tools%2FGradle&parentPath=%2FAndroid%2FDeveloper%20Tools

Android 笔记：GreenDao3.2的使用，爱不释手
http://blog.csdn.net/qq_30379689/article/details/54410838
https://github.com/AndroidHensen/GreenDaoDemo

Android 4.0新增Space及GridLayout初谈
http://tech.it168.com/a2011/1122/1277/000001277274.shtml

git丢弃本地修改的所有文件（新增、删除、修改）
http://blog.csdn.net/leedaning/article/details/51304690
git checkout . #本地所有修改的。没有的提交的，都返回到原来的状态
git stash #把所有没有提交的修改暂存到stash里面。可用git stash pop回复。
git reset --hard HASH #返回到某个节点，不保留修改。
git reset --soft HASH #返回到某个节点。保留修改

git clean -df #返回到某个节点
git clean 参数
    -n 显示 将要 删除的 文件 和  目录
    -f 删除 文件
    -df 删除 文件 和 目录1


[GreenDao 3.2.0 的基本使用](https://www.cnblogs.com/tonycheng93/p/6295724.html)  

[GreenDao3.2使用详解（增，删，改，查，升级）](https://blog.csdn.net/wzgbgz/article/details/79140056)




[Android studio 4.0 使用greenDAO](https://blog.csdn.net/luckywujl/article/details/106834352)  


[GreenDao使用总结](https://www.jianshu.com/p/967d402d411d)  

~~~
F:\ReciteWords\app\build.gradle

apply plugin: 'org.greenrobot.greendao'

android {
......
    // 自定义数据库路径
    greendao {
        schemaVersion 1
        daoPackage 'com.mywords.app.greendao.gen'
        targetGenDir 'src/main/java'
    }

}

.....
repositories {
......
}

dependencies {
......

    // 数据库GreenDao
    implementation 'org.greenrobot:greendao:3.3.0'
    implementation 'org.greenrobot:greendao-generator:3.3.0'

......
}

F:\ReciteWords\build.gradle

buildscript {
    repositories {
        google()
        jcenter()
        mavenCentral()
    }
    dependencies {
        classpath 'com.android.tools.build:gradle:4.0.1'
        
        classpath 'org.greenrobot:greendao-gradle-plugin:3.3.0'
        
        // NOTE: Do not place your application dependencies here; they belong
        // in the individual module build.gradle files
    }
}

F:\ReciteWords\app\src\main\java\com\mywords\app\base\BaseApplication.java

class BaseApplication extends Application {
    public static final String DB_NAME = "word.db";
    public static Context mContext;
    private static DaoSession mDaoSession;
    private static BaseApplication instance;

    /**
     * 单一实例
     */
    public static BaseApplication getInstance() {
        if (null == instance) {
            instance = new BaseApplication();
        }
        return instance;
    }


    @Override
    public void onCreate() {
        super.onCreate();
        mContext = getApplicationContext();
        initGreenDao();
    }

    public static Context getAppContext() {
        return mContext;
    }

    /**
     * 初始化数据库
     */
    private void initGreenDao() {
        DaoMaster.DevOpenHelper mHelper = new DaoMaster.DevOpenHelper(this, DB_NAME, null);
        SQLiteDatabase db = mHelper.getWritableDatabase();
        DaoMaster mDaoMaster = new DaoMaster(db);
        mDaoSession = mDaoMaster.newSession(IdentityScopeType.None);
    }

    public DaoSession getDaoSession() {
        return mDaoSession;
    }

}


~~~

GreenDao查询
---

[学习GreenDAO的QueryBuilder的使用](https://blog.csdn.net/flybamboo/article/details/52846110)  

[GreenDao简明教程（查询，Querying）](https://blog.csdn.net/yuyuanhuang/article/details/42751469)  

[Day5 greenDao的List存储与查询方法大全](https://www.jianshu.com/p/7e66d95b098a)  

[GreenDao讲义3：带你了解查询生成器和更加复杂的查询](https://blog.csdn.net/huangjiamingboke/article/details/52123993)  


GreenDao 分页
---

[GreenDao 分页条件查询排序](https://blog.csdn.net/nuonuonuonuonuo/article/details/81234168)  

[GreenDao的简单使用说明(三)多表的操作1:n](https://blog.csdn.net/chenguang79/article/details/50460718)  

[greenDao分页加载](https://blog.csdn.net/haowei0708/article/details/51596837)  
~~~
分页加载20条数据，getTwentyRec(int offset)中控制页数offset++即可
    public List<UserEntity> getTwentyRec(int offset){
        UserDao dao = openReadableDb().getUserDao();
        List<UserEntity> listMsg = dao.queryBuilder()
                .offset(offset * 20).limit(20).list();
        return listMsg;
    }
~~~


[分页加载（类似网页）](https://blog.csdn.net/nihaozhanghua/article/details/78142487)  


GreenDao 多表
---

[GreenDAO 3.2.2 简单入门（一）增删改查](https://www.jianshu.com/p/aa4e172f7d47)  

[GreenDAO 3.2.2 简单入门（二）多表查询和多表关联](https://www.jianshu.com/p/e6ac52498576)  

[GreenDao的简单使用说明(三)多表的操作1:n](https://blog.csdn.net/chenguang79/article/details/50460718/)  

[GreenDao的简单使用[一]之增删改查](https://blog.csdn.net/wj9966/article/details/79272564)  

[GreenDao的简单使用[二]之升级数据库](https://blog.csdn.net/wj9966/article/details/79280215)  

[GreenDao的简单使用[三]之多表关系操作](https://blog.csdn.net/wj9966/article/details/81545827)  

[使用GreenDao创建表、关联表（一对一，一对多，多对多）、CURD、升级数据库等操作](https://blog.csdn.net/zhanlv/article/details/82425709)  


[视频【安卓开发】Android 开发教程初级—第十六讲 项目开发 GreenDao应用—](https://www.bilibili.com/video/av498277248)  





[greendao用完需要手动关闭数据库吗](https://zhidao.baidu.com/question/2120401707570803067.html)  
~~~
点开baigreendao某方法

private void deleteInTxInternal(Iterable<T> entities, Iterable<K> keys) {
    //此处打开
    db.beginTransaction();
    try {
       ...
    } finally {
        //此处关闭
        db.endTransaction();
    }
}
greendao不需要手du动去打zhi开和关闭数据库，已经帮我们做dao好了
~~~


[使用greenDao关闭数据库](https://mlog.club/article/1729704)  
~~~
    private static DaoMaster daoMaster;
    private static DaoSession daoSession;

daoMaster.getDatabase().close()
或
daoSession.getDatabase().close()
~~~





