## Android二维码

[Android利用zxing生成二维码，识别二维码，中间填充图片超详细、超简易教程](https://blog.csdn.net/mountain_hua/article/details/80646089)  
https://github.com/zxing/zxing  

[Android 基于google Zxing实现二维码、条形码扫描，仿微信二维码扫描效果](http://blog.csdn.net/xiaanming/article/details/10163203)  

[Android 使用Zxing实现二维码的生成，扫描](http://blog.csdn.net/qq_28057541/article/details/52034988)  
https://github.com/zxing/zxing  

[一个非常好用的android工具 zxing-android-embedded](https://github.com/journeyapps/zxing-android-embedded)

[ZXing二维码扫描Demo QrCodeScan](https://github.com/HappyMiao/QrCodeScan)  

[十个Android的另类库，快来看看吧！](http://www.apkbus.com/blog-822721-75850.html)  

[使用开源的card.io 扫描识别银行卡](http://blog.csdn.net/niu0147/article/details/73618375)  
https://www.card.io/  
https://github.com/card-io/card.io-Android-SDK  
https://github.com/card-io/card.io-Android-SDK/tree/master/SampleApp  

    compile 'io.card:android-sdk:5.5.1'  

[Android平台银行卡识别--慧视银行卡号识别SDK](http://blog.sina.com.cn/s/blog_7a21a0b10102wag2.html)

[Android平台证件识别系统](http://blog.sina.com.cn/s/blog_7a21a0b10102w9z7.html)  

[Android OCR识别身份证，银行卡等证件信息](http://www.apkbus.com/blog-927424-75847.html)  
[百度云OCR识别身份证，银行卡，驾驶证，车牌等证件](https://github.com/zhouxu88/OCRDemo)  

[Android 银行卡扫描识别获取卡号  用card.io 实现的银行卡扫描，免费](http://blog.csdn.net/a53657561/article/details/64982411)  
eclipse上面运行的Demo：  
http://download.csdn.net/detail/liqingmiao123/9492343  
AndroidStudio上运行的Demo：  
http://download.csdn.net/detail/rjliulei/8766921  

[android ocr——身份证识别的功能实现](http://www.jb51.net/article/97505.htm)
google 开源的项目tesseract-ocr 
https://github.com/justin/tesseract-ocr

二维码扫描项目
http://www.jb51.net/article/53487.htm

[Android 笔记：识别银行卡，获取银行卡卡号](http://blog.csdn.net/xiaoyu940601/article/details/54575866)  
Android笔记(翻译)：card.io SDK for Android银行卡扫描   
http://blog.csdn.net/xiaoyu940601/article/details/54575387  

https://github.com/paypal/PayPal-Java-SDK  
https://github.com/paypal/PayPal-Android-SDK  
compile 'com.paypal.sdk:paypal-android-sdk:2.15.3'  

    dependencies {
        compile('com.paypal.sdk:paypal-android-sdk:2.15.3') {
           exclude group: 'io.card'
        }
    }
