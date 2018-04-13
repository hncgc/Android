Android 动画
-----------
[Android 动画之AlphaAnimation应用详解](http://www.jb51.net/article/32337.htm)  
```
android中提供了4中动画： 
AlphaAnimation 透明度动画效果 
ScaleAnimation 缩放动画效果 
TranslateAnimation 位移动画效果 
RotateAnimation 旋转动画效果  
```

[Android 动画之TranslateAnimation应用详解](http://www.jb51.net/article/32339.htm)  

[Android 动画之ScaleAnimation应用详解](http://www.jb51.net/article/32340.htm)  

[Android 动画之RotateAnimation应用详解](http://www.jb51.net/article/32341.htm)  

[Android 动画 - AlphaAnimation渐变动画](http://blog.csdn.net/shibin1990_/article/details/51602498)  
```
创建AlphaAnimation有两种方式
1.XML文件+Java代码
文件目录：res/anim/alpha.xml
<?xml version="1.0" encoding="utf-8"?>
<alpha xmlns:android="http://schemas.android.com/apk/res/android"
      android:duration="3000"
      android:fillAfter="true"
      android:fillBefore="false"
      android:fromAlpha="1.0"
      android:interpolator="@android:anim/linear_interpolator"
      android:repeatCount="-1"
      android:repeatMode="restart"
      android:startOffset="2000"
      android:toAlpha="0.3"/>

•android:duration：动画持续的时长，单位是毫秒 
•android:fillAfter：动画结束之后是否保持动画的最终状态；true，表示保持动画的最终状态 
•android:fillBefore：动画结束之后是否保持动画开始前的状态；true，表示恢复到动画开始前的状态 
•android:fromAlpha：动画开始的透明度，取值0.0~1.0，0.0表示完全透明，1.0表示保持原有状态不变 
•android:interpolator：动画插值器。是实现动画不规则运动的一种方式，后面讲到 
•android:repeatCount：动画重复的次数。指定动画重复播放的次数，如果你需要无限循环播放，请填写一个小于0的数值，我一般写-1
•android:repeatMode：动画重复的Mode，有reverse和restart两种，效果看后面 
•android:startOffset：动画播放延迟时长，就是调用start之后延迟多少时间播放动画 
•android:toAlpha：动画最终的透明度，取值和android:fromAlpha一样

Java代码加载XML文件动画

Toast.makeText(XmlViewAnimationActivity.this, "startAnimation", Toast.LENGTH_SHORT).show();
     AlphaAnimation alphaAnimation = (AlphaAnimation) AnimationUtils.loadAnimation(XmlViewAnimationActivity.this, R.anim.alpha);
     mIvImg.startAnimation(alphaAnimation);


2.Java代码方式：
public void startAlphaAnimation(){
        /**
         * @param fromAlpha 开始的透明度，取值是0.0f~1.0f，0.0f表示完全透明， 1.0f表示和原来一样
         * @param toAlpha 结束的透明度，同上
         */
        AlphaAnimation alphaAnimation = new AlphaAnimation(1.0f, 0.2f);
        //设置动画持续时长
        alphaAnimation.setDuration(3000);
        //设置动画结束之后的状态是否是动画的最终状态，true，表示是保持动画结束时的最终状态
        alphaAnimation.setFillAfter(true);
        //设置动画结束之后的状态是否是动画开始时的状态，true，表示是保持动画开始时的状态
        alphaAnimation.setFillBefore(true);
        //设置动画的重复模式：反转REVERSE和重新开始RESTART
        alphaAnimation.setRepeatMode(AlphaAnimation.REVERSE);
        //设置动画播放次数
        alphaAnimation.setRepeatCount(AlphaAnimation.INFINITE);
        //开始动画
        mIvImg.startAnimation(alphaAnimation);
        //清除动画
        mIvImg.clearAnimation();
        //同样cancel()也能取消掉动画
        alphaAnimation.cancel();
   }
```

-------------------------------------------
   
矢量图 & 动画
---
[Android Loading动画分析设计](http://www.jianshu.com/p/646b3b42c471)  
https://github.com/dinuscxj/LoadingDrawable  

[Android自定义加载动画库zLoading](http://blog.csdn.net/littlesmallless/article/details/70041810)  
https://github.com/zyao89/ZLoading  

------------------

矢量图库
----
[阿里巴巴矢量图库](http://www.iconfont.cn/collections?spm=a313x.7781069.0.0.fEW4eG&personal=1)  

---------

[Android Vector曲折的兼容之路](http://blog.csdn.net/eclipsexys/article/details/51838119)  

[Android中VectorDrawableCompat的使用注意事项](http://blog.csdn.net/lgtianxiawudi/article/details/54860888)  

[android开发游记：VectorDrawable矢量图兼容性问题的解决方案](https://www.2cto.com/kf/201605/506588.html)  

[APP开发实战92-静态Vector兼容性处理](http://blog.csdn.net/xjbclz/article/details/51925238)  

[关于android中矢量图如何用，有坑，爬坑，如何替代的另一些看法](http://www.jianshu.com/p/313912ff2f37)  

[Android矢量图之VectorDrawable类自由填充色彩](http://www.jb51.net/article/84613.htm)

[VectorDrawable怎么玩](http://www.jianshu.com/p/456df1434739)  
https://github.com/Damonzh/VectorDrawableDemo  

[VectorDrawable矢量图](http://blog.csdn.net/king1425/article/details/70034065)  
动画Demo库https://github.com/xuyisheng/VectorDemo  
```
矢量图详细介绍

1、支持的指令： 
M = moveto 相当于 android Path 里的moveTo(),用于移动起始点 
L = lineto 相当于 android Path 里的lineTo()，用于画线 
H = horizontal lineto 用于画水平线 
V = vertical lineto 用于画竖直线 
C = curveto 相当于cubicTo(),三次贝塞尔曲线 
S = smooth curveto 同样三次贝塞尔曲线，更平滑 
Q = quadratic Belzier curve quadTo()，二次贝塞尔曲线 
T = smooth quadratic Belzier curveto 同样二次贝塞尔曲线，更平滑 
A = elliptical Arc 相当于arcTo()，用于画弧 
Z = closepath 相当于closeTo(),关闭path 
2、使用原则： 
①坐标轴为以(0,0)为中心，X轴水平向右，Y轴水平向下。 
②所有指令大小写均可。大写绝对定位，参照全局坐标系；小写相对定位，参照父容器坐标系 
③指令和数据间的空格可以省略 
④同一指令出现多次可以只用一个 
 注意，’M’处理时，只是移动了画笔， 没有画任何东西。 它也可以在后面给出上同时绘制不连续线。 

3、详细指令分析 
3.1、L H V指令 
 绘制直线的指令是“L”，从当前点划线到给定点。 “L”之后的参数是一个点坐标，如“L 200 400”。 如果画水平线或垂直线，可以使用“H”和“V”指令，后面的参数是x（H指令）或y坐标（V指令）。 
M　起点X，起点Y　L（直线）终点X，终点Y　H（水平线）终点X　V（垂直线）终点Y 
如：M 10,20 L 80,50 M 10,20 V 50 M 10,20 H 90 

3.2、A指令 
 允许不闭合。可以想像成是椭圆的某一段，共七个参数 
A RX,RY,XROTATION,FLAG1,FLAG2,X,Y 
 RX,RY指所在椭圆的半轴大小 
XROTATION指椭圆的X轴与水平方向顺时针方向夹角，可以想像成一个水平 的椭圆绕中心点顺时针旋转XROTATION的角度。 
FLAG1只有两个值，1表示大角度弧线，0为小角度弧线。 
FLAG2只有两个值，确定从起点至终点的方向，1为顺时针，0为逆时针 
X,Y为终点坐标。 
M 20,50 A 30,30,0,1 0 80,50 这个就是画一个下半圆。 
3.3 C指令 三次贝塞尔曲线。相关博客很多，不在追述
```

[网上找的一个开源的Vector的动画Demo库](https://github.com/xuyisheng/VectorDemo)  


