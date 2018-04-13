Android 消息处理机制
---
[Android消息处理机制(Handler、Looper、MessageQueue与Message)](http://www.cnblogs.com/angeldevil/p/3340644.html)  

[Android消息机制字典型探究（一）](http://www.jianshu.com/p/8c06b1d7ca68)  

[Android消息机制字典型探究（二）](http://www.jianshu.com/p/8501d3b0c359)  

[带着这篇去通关所有Handler的提问（三）](http://www.jianshu.com/p/fad4e2ae32f5)  

[Handler可能造成内存泄漏（四）](http://www.jianshu.com/p/c0c67c2a0532)  

[Android开发中Handler的经典总结](http://mobile.51cto.com/aprogram-442833.htm)  

[Android Handler详细使用方法实例](http://www.codeceo.com/article/android-handler-usage.html)  


Java Message Service （JMS）介绍
http://blog.csdn.net/lucifer821031/article/details/2064541

[Android中Message参数传递](http://blog.csdn.net/generallizhong/article/details/53018783)  

[Bundle数据通过Message传送](http://blog.csdn.net/baidu_24169397/article/details/44921827)  

[Android中Message传递参数(bundle setData方式传递)](http://blog.csdn.net/rongwenbin/article/details/46983757)  

[Android 异步消息处理机制 让你深入理解 Looper、Handler、Message三者关系](http://blog.csdn.net/lmj623565791/article/details/38377229)

[Android 基于Message的进程间通信 Messenger完全解析](http://blog.csdn.net/lmj623565791/article/details/47017485)  

[Android事件分发机制详解：史上最全面、最易懂](https://www.jianshu.com/p/38015afcdb58)  

[android Activity runOnUiThread() 方法使用](https://www.cnblogs.com/zhaoyanjun/archive/2016/05/11/5483221.html)  

    public class MainActivity extends AppCompatActivity {
 
        @Override
        protected void onCreate(Bundle savedInstanceState) {
            super.onCreate(savedInstanceState);
            setContentView(R.layout.activity_main);
     
            //创建一个线程
            new Thread(new Runnable() {
     
                @Override
                public void run() {
 
                    //延迟两秒
                    try {
                        Thread.sleep( 2000 );
                    } catch (InterruptedException e) {
                        e.printStackTrace();
                    }
 
                    runOnUiThread(new Runnable() {
                        @Override
                        public void run() {
                            Toast.makeText(MainActivity.this, "hah", Toast.LENGTH_SHORT).show();
                        }
                    });
 
                }
            }).start();
        }
    }

[runOnUiThread更新主线程](https://www.cnblogs.com/wanqieddy/p/4153203.html) 

AsyncTask
---
[Android ：AsyncTask最详细使用教程](https://juejin.im/entry/5a78fba3f265da4e9673d4b8)  
建议先下载源码再看：Carson_Ho的Github地址：AsyncTask https://github.com/Carson-Ho/MultiThread_learning

[Android 多线程：AsyncTask的原理 及其源码分析](https://www.jianshu.com/p/37502bbbb25a)


