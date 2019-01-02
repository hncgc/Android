Pay  
===

支付宝官方文档
---

[支付宝开发指南](https://docs.open.alipay.com/200/)  

[支付宝沙箱环境使用说明](https://docs.open.alipay.com/200/105311/)  
~~~
 1. 生成并上传RSA2(SHA256)的应用公钥，详见生成RSA密钥；配置RSA2(SHA256)的应用公钥后，不需要配置RSA(SHA1)密钥，RSA和RSA2签名算法区别可以参考此处；
      2. 编写代码时，请将
          a.请求网关修改为：https://openapi.alipaydev.com/gateway.do
          b.appid切换为沙箱的appid
          c.签名方式使用RSA2
          d.应用私钥使用第1步生成的RSA2(SHA256)的私钥(请根据开发语言进行选择原始或pkcs8格式)
          e.支付宝公钥切换为第1步配置后应用公钥后，点击查看支付宝公钥看到的公钥 
          
选看部分作为进阶使用，非必填项；
应用网关：该地址用于接收开放平台的异步通知。目前沙箱环境不需要配置此参数；
授权回调地址；第三方应用授权或获取用户信息中用于接收授权回调信息的地址。使用相关产品时再进行配置；
         1. 第三方应用授权：
             授权url中的redirect_uri必须与此值相同。
         2. 获取用户信息：
             授权url中的redirect_uri的域名必须与此值相同。(例如：授权回调地址配置：https://auth.example.com/authCallBack 高亮部分需和授权url相同)

RSA(SHA1)密钥：目前推荐使用RSA2(SHA256)密钥，请参考第1步进行配置；
AES密钥：目前不再使用；

~~~

[支付宝App支付快速接入](https://docs.open.alipay.com/204/105297)  

[App支付客户端DEMO&SDK](https://docs.open.alipay.com/54/104509)  

[Android移动支付（支付宝支付2017最新接入详解）](https://blog.csdn.net/mr_jianrong/article/details/78995580)  

[单笔转账到支付宝账户产品介绍(给客户转账)](https://docs.open.alipay.com/309)  

----------------------

[支付宝Pay，一个类直接搞定](https://blog.csdn.net/woaiheima/article/details/50982851)  

[Android集成支付宝支付功能](https://www.jianshu.com/p/304ced0a23ba)  

[关于Android在线支付Alipay（支付宝）开发的经验分享](https://blog.csdn.net/ht_android/article/details/45307165)  

[支付宝集成过程详解——运行DEMO](https://blog.csdn.net/harvic880925/article/details/49779061)  

[超详细Android接入支付宝支付实现，有图有真相](https://www.jianshu.com/p/2aa2e8748476)  

[Android App支付系列（二）：支付宝SDK接入详细指南(附官方支付demo)](https://www.jb51.net/article/98280.htm)  

[支付宝支付](https://www.aliyun.com/jiaocheng/36063.html)  

[一步一步带你完成支付宝支付功能的集成（超详细）](https://blog.csdn.net/fjnu_se/article/details/72973220)  



[android 支付宝的植入 《曾经踩过的坑》](https://blog.csdn.net/androidstarjack/article/details/52808705)  

[支付宝 app支付异常摘记 -- ALI40247](https://blog.csdn.net/luojinbai/article/details/52753660)  


[支付宝支付和微信支付](https://www.jianshu.com/p/66a7fe2effaf)  













[阿里云  >   教程中心  >   Android教程](https://www.aliyun.com/jiaocheng/android?spm=5176.100033.1.3.6fab6aa1Jdym0h)  

