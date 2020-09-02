LitePal
---
[Android数据库框架 - LitePal学习笔记](https://www.jianshu.com/p/bc68e763c7a2)  
github:https://github.com/LitePalFramework/LitePal  
郭霖       https://github.com/guolindev  
          《第一行代码 第2版》全书源代码  

[LitePal详解](http://blog.csdn.net/fuzhongbin/article/details/51217944)  

[开源数据库 LitePal 学习，强大好使的 CRUD](https://segmentfault.com/p/1210000008884257/read)  

GreenDao3.0
---

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
    
[Android studio 4.0 使用greenDAO](https://blog.csdn.net/luckywujl/article/details/106834352)  


[GreenDao使用总结](https://www.jianshu.com/p/967d402d411d)  





