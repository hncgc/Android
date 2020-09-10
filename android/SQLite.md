## SQLite

[SQLite 简介 | 菜鸟教程](https://www.runoob.com/sqlite/sqlite-intro.html)  

[SQLite 数据库的一些基本操作](http://www.nowamagic.net/academy/detail/50280108)  

[SQLite Home](https://www.sqlite.org/index.html)  

--------------

[Android 使用SQLite本地数据库](https://www.cnblogs.com/gisoracle/p/5212663.html)

[搭建Android本地数据库(SQLite)的详细讲解](https://blog.csdn.net/qq_36903042/article/details/79772268)  

[在android项目里使用自带的SQLite数据库](https://blog.csdn.net/lsh869/article/details/51536985)  

[在Android程序中使用已有的SQLite数据库](https://blog.csdn.net/naturebe/article/details/40718521)  



-------------

[Windows下安装SQLite记录](https://github.com/hncgc/Android/blob/master/android/Windows%E4%B8%8B%E5%AE%89%E8%A3%85SQLite%E8%AE%B0%E5%BD%95.md)  

-------------

[android实现raw文件夹导入数据库代码](https://www.jb51.net/article/45080.htm)  

[Android导入现有的数据库方法示例](https://www.jb51.net/article/106790.htm)

[android读取assets中Excel表格并显示](https://www.jb51.net/article/104588.htm)  

[android通过jxl读excel存入sqlite3数据库](https://www.xp.cn/b.php/67477.html)  

[android通过jxl读excel存入sqlite3数据库](https://www.jb51.net/article/47469.htm)  

[Android开发实现的导出数据库到Excel表格功能【附源码下载】](https://www.jb51.net/article/136440.htm)  

[Android 使用存放在存assets文件夹下的SQLite数据库](https://blog.csdn.net/u011494050/article/details/38427089)  

[android导入外部的数据库sqlite](https://download.csdn.net/download/dianqiugg/7475771)  
~~~
public class MainActivity extends Activity
{
// 注意：同名覆盖要关闭数据库
    /**
     * 如果数据库文件较大，使用FileSplit分割为小于1M的小文件
     *      要被导入的数据库，置于工程assets目录下wordLibrary.001
     */
    public String RESOURCE_DB = "wordLibrary";

    /**
     * 导入到这个数据库里
     */
    public String DB_NAME = "wordLibrary1.db";

   void init() {
        // 数据库文件目标存放的路径(本例为系统默认位置)
        String db_path = getDataDir().getPath() + "/databases/";
        new DBUtils(this, RESOURCE_DB, DB_NAME, db_path).createDataBase();
   }

}

2020-09-08 23:41:56.720 29693-29693/com.mywords.app D/MainActivity: db_path = /data/user/0/com.mywords.app/filesdata/com.mywords.app/databases/

~~~

Filesplit(文件分割合并工具) 
[文件分割（FileSplit）](https://jingyan.baidu.com/article/ed15cb1b94c7a01be3698181.html)  

[scimence / fileSplit](https://gitee.com/scimence/fileSplit?utm_source=aladin&utm_campaign=repo)  


[Android导入外部数据库](https://blog.csdn.net/chaoyu168/article/details/50467913)  

[android下如何获取当前应用下的databases数据库路径](https://zhidao.baidu.com/question/2201288240098644148.html)  

路径测试
~~~

        String db_path00 = getFilesDir().getPath() + "data/" + getPackageName()
                + "/databases/";
        String db_path0 = getFilesDir().getPath();
        Log.d(TAG, "db_path = getFilesDir().getPath() = " + getFilesDir().getPath());
        Log.d(TAG, "db_path = " + db_path0);
        //String db_path1 = "/data/data/" + getPackageName() + "/databases/";
        //Log.d(TAG, "db_path = " + db_path1);
        String db_path = getDataDir().getPath() + "/databases/";
        Log.d(TAG, "db_path = getDataDir().getPath()=" + getDataDir().getPath());
        Log.d(TAG, "db_path = " + db_path);
2020-09-10 00:04:25.153 15509-15509/com.mywords.app D/MainActivity: db_path = getFilesDir().getPath() = /data/user/0/com.mywords.app/files
2020-09-10 00:04:25.153 15509-15509/com.mywords.app D/MainActivity: db_path = /data/user/0/com.mywords.app/files
2020-09-10 00:04:25.153 15509-15509/com.mywords.app D/MainActivity: db_path = getDataDir().getPath()=/data/user/0/com.mywords.app
2020-09-10 00:04:25.153 15509-15509/com.mywords.app D/MainActivity: db_path = /data/user/0/com.mywords.app/databases/



        // 数据库文件目标存放的路径(本例为系统默认位置)
        String db_path = getDataDir().getPath() + "/databases/";
        Log.d(TAG, "db_path = getDataDir().getPath()=" + getDataDir().getPath());
        Log.d(TAG, "db_path = " + db_path);
	
2020-09-10 00:04:25.153 15509-15509/com.mywords.app D/MainActivity: db_path = getDataDir().getPath()=/data/user/0/com.mywords.app
2020-09-10 00:04:25.153 15509-15509/com.mywords.app D/MainActivity: db_path = /data/user/0/com.mywords.app/databases/

~~~

[Android 文件外/内部存储的获取各种存储目录路径](https://blog.csdn.net/csdn_aiyang/article/details/80665185)  

[Android 常用路径的获取](https://www.jianshu.com/p/e8a11d23513b)  

[GreenDao 连接与关闭Sqlite数据库](https://blog.csdn.net/printlnout/article/details/83030089)  

[使用greenDao关闭数据库](https://mlog.club/article/1729704)  
~~~
daoMaster.getDatabase().close()
或
daoSession.getDatabase().close()
~~~







