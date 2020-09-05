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

-----------------------------


[Key was created with errors: Warning: JKS 密钥库使用专用格式。android Studio打包报错](https://blog.csdn.net/qq_42221857/article/details/105975431)

[Android APK签名 JKS 密钥库使用专用格式。建议使用 “keytool -importkeystore -srckeystore E:\xxxxxx- pkcs12“ 迁移到行业标准格式](https://blog.csdn.net/xkai007/article/details/106073091)

[Java证书工具keytool用法总结](https://blog.csdn.net/w47_csdn/article/details/87564029)

[JDK自带的keytool证书工具详解](https://www.cnblogs.com/zhi-leaf/p/10418222.html)

[android 使用signingConfigs进行打包](https://blog.csdn.net/bzlj2912009596/article/details/78188570)

[android signingConfigs打包配置](https://www.jianshu.com/p/62ac145ee0ad)

[AS3.6.1版apk签名打包Warning-JKS密钥库使用专用格式](https://www.tqwba.com/x_d/jishu/11788.html)

[Warning:JKS 密钥库使用专用格式。建议使用 "keytool -importkeystore -srckeystore...pkcs12" 迁移到行业标准格式 PKCS12](https://blog.csdn.net/csdnzouqi/article/details/105882034)

[jks与keystore区别](https://blog.csdn.net/qq_15509421/article/details/91870944)

[Android jks文件签名转换keystore文件签名](https://blog.csdn.net/ONLYMETAGAIN/article/details/78781316)


[Android-解放双手之Gradle自动化打包实战（原创）](https://www.jianshu.com/p/38eb97d3477e)  

[Android-V1、V2签名包和快速集成美团多渠道打包（原创）](https://www.jianshu.com/p/332525b09a88)  

[Android Studio gradle打包实践](https://www.jianshu.com/p/c5f69437100a)  

[最全的命令行（gradle）打包安卓apk](https://www.cnblogs.com/peng-lan/p/11097117.html)  

[android studio打包导出未签名apk](https://blog.csdn.net/u010111268/article/details/105053649)  

[Android 使用 Gradle 打包之签名配置](https://www.jianshu.com/p/8dc154f0f89f)  

~~~
android {
    ......
    // 配置 release 的签名信息
    signingConfigs {
        release {
            storeFile
            storePassword
            keyAlias
            keyPassword
        }
    }

    // 读取签名配置
    getSigningProperties()

    buildTypes {
        // debug 和 release 使用同样的签名
        debug {
            signingConfig signingConfigs.release
        }

        release {
            minifyEnabled true
            shrinkResources true
            zipAlignEnabled true
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
            signingConfig signingConfigs.release
            // 修改生成的 apk 文件名，输出 apk 名称：MyApp_v1.0.0_2017-11-10_debug.apk
            applicationVariants.all { variant ->
                def suffix
                if (variant.buildType.name == 'release') {
                    suffix = 'release'
                } else {
                    suffix = 'debug'
                }
                variant.outputs.each { output ->
                    def outputFile = output.outputFile
                    if (outputFile != null && outputFile.name.endsWith('.apk')) {
                        def fileName = "MyApp_v${defaultConfig.versionName}_${releaseTime()}_${suffix}.apk"
                        output.outputFile = new File(outputFile.parent, fileName)
                    }
                }
            }
        }
    }
    ......
}

// 读取签名配置
def getSigningProperties() {
    def propFile = file('../signing.properties')
    if (propFile.exists() && propFile.canRead()) {
        def props = new Properties()
        props.load(new FileInputStream(propFile))
        if (props.containsKey('STORE_FILE') && props.containsKey('STORE_PASSWORD') &&
                props.containsKey('KEY_ALIAS') && props.containsKey('KEY_PASSWORD')) {
            android.signingConfigs.release.storeFile = file('../' + props['STORE_FILE'])
            android.signingConfigs.release.storePassword = props['STORE_PASSWORD']
            android.signingConfigs.release.keyAlias = props['KEY_ALIAS']
            android.signingConfigs.release.keyPassword = props['KEY_PASSWORD']
        } else {
            println 'signing.properties are found but some entries are missed!'
            android.buildTypes.release.signingConfig = null
        }
    } else {
        println 'signing.properties are not found!'
        android.buildTypes.release.signingConfig = null
    }
}

// 定义打包时间
static def releaseTime() {
    return new Date().format("yyyy-MM-dd", TimeZone.getTimeZone("UTC"))
}
~~~
























