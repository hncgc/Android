Android 签名
---
[Android Studio 使用Eclipse中的keystore为App签名](http://blog.csdn.net/kangear/article/details/52069726)  
>最终在Project Structure中配置一个Signing，store文件还是Eclipse中使用的那个

[Android 获取签名证书的详细信息（Eclipse和Android studio通用）](http://www.bkjia.com/Androidjc/1012685.html)  
> 今天要用到签名证书的MD5,但是这个只有在第一次生成的时候我看到了，这可怎么办呢，幸亏我们有google,我们运行下面的命令就OK了。
> keytool -list -v -keystore 签名证书的路径
> Eclipse 生成的签名证书是.keystore结尾的，Android Studio 生成的签名证书是.jks结尾的，这一点要注意哦

[eclipse打包和android studio打包使用同一签名文件](http://www.bubuko.com/infodetail-1000864.html)  
>当我们把eclipse 项目转到到android studio中时，打包会有所不同，在eclispe中打包时只需要选择签名文件和输入密码就可以了，但是在android stuido中打包是需要输入key.alias（别名），可能这个keystore不是你生成的或已经忘记了key.alias，你可以通过以下命令查看keystore的key.alias（别名），

>命令进入keystore文件所在的目录 运行 keytool -list  -v -keystore xxxx.keystore -storepass xxxxxxxxxx（密码） 　签名的信息就有了
>这样就可以顺利的打包了！

eclipse 迁移 Android Studio 证书问题

>Android 获取签名证书的详细信息（Eclipse和Android studio通用）
>今天要用到签名证书的MD5,但是这个只有在第一次生成的时候我看到了，这可怎么办呢，幸亏我们有google,我们运行下面的命令就OK了。
>keytool -list -v -keystore 签名证书的路径
>
>Eclipse 生成的签名证书是.keystore结尾的，Android Studio 生成的签名证书是.jks结尾的，这一点要注意哦



Android几种常见的多渠道(批量)打包方式介绍
http://www.itnose.net/detail/6614021.html

通过ant脚本，编译打包android工程
http://blog.csdn.net/chenzhiqin20/article/details/8191889

#下面这句是自动生成的
sdk.dir=D:\\Program Files\\Android\\android-sdk
#数字签名文件
key.store=jingchen.keystore
#别名alias
key.alias=jingchen
#数字签名的密码
key.store.password=111111
#alias的密码
key.alias.password=111111
#这里设置混淆代码，在当前项目的proguard-project.txt中编写混淆规则
proguard.config=${sdk.dir}/tools/proguard/proguard-android.txt:proguard-project.txt

[ProGuard代码混淆技术详解](http://www.cnblogs.com/cr330326/p/5534915.html)  

Eclipse下Ant自动打包，混淆和签名
http://www.aiuxian.com/article/p-1675466.html

Eclipse下使用Ant多渠道批量打包
http://www.aiuxian.com/article/p-1675467.html


