Java 接口
===

[Java 中的接口有什么作用？](https://www.zhihu.com/question/20111251)  
链接：https://www.zhihu.com/question/20111251/answer/14760353  
```
    接口只是一个规范，所以里面的方法都是空的。假如我开了一个宠物粮店，声明所有宠物都可以来我这里买粮食，这就相当于一个接口，public interface PetRestaurant { public void buy();}当一只狗看到了，知道自己是宠物，所以它去实现这个接口public class DogPet implements PetRestaurant { @Override public void buy() {  System.out.println("我是狗，我要买狗粮"); }}当一只猫看到了，知道自己也是宠物，所以也去实现这个接口public class CatPet implements PetRestaurant { @Override public void buy() {  System.out.println("我是猫，我要买猫粮"); }}当狗和猫来我的店之前，我是不知道他们到底是什么，但是当他们来到我的店，我就知道一个要猫粮食，一个要狗粮食。因为他们都实现了 我这个接口，都可以买。下面这个类相当于一个接待顾客的类，即店小二，他接待所有实现了我这个宠物店接口的动物，传进来一个PetRestaurant 类型的宠物，注意，这个PetRestaurant 是接口public class test { public void buy(PetRestaurant pet) {  pet.buy(); }}好了，这个时候我这个老板出现了，我可以给他们卖粮食了，相当于测试类public class Tests { public static void main(String[] args) {  PetRestaurant dog = new DogPet();  //实例化一个狗，相当于把狗顾客实例化  PetRestaurant cat = new CatPet();//实例化一个猫，相当于把猫顾客实例化  test t = new test();  //实例化一个店小二  t.buy(cat);  //把猫交给店小二  t.buy(dog); //把狗交给店小二 }}这样运行的结果就是我是猫，我要买猫粮我是狗，我要买狗娘你知道吗，整个过程我这个店主其实根本不知道来的到底是猫是狗还是其他什么，我只要有一个店小二，把这些来的不知什么动物都全部交给店小二，店小二就知道怎么去卖了，因为这些狗啊猫啊都实现了我这个宠物店的接口，而店小二就负责接待所有实现了我这个接口的动物。这就有一个好处，假如明天来了一头小猪，只要它实现了我这个接口，我只管交给店小二处理就OK了，我这个店小二根本不需要变化，我这个店主也只需要实例化一下这个动物就OK你想，假如没有接口，会怎么办，来一个猫，我要去创造一个猫，还要实例化，来一只狗，我要创建一只狗，同样要实例化，还要配备专门的店小二去接待，就会相当麻烦
```

[Java 接口](http://www.runoob.com/java/java-interfaces.html)  


[Java接口 详解（一）](http://blog.csdn.net/wei_zhi/article/details/52738471)  

[Java接口 详解（二）](http://blog.csdn.net/wei_zhi/article/details/52743109)  

[java接口简单例子](http://blog.csdn.net/Clarissatt/article/details/51263696)  

[【java】:java接口详解](http://blog.csdn.net/qq_23100787/article/details/62887348)  

[Java接口详解](http://blog.csdn.net/zdwzzu2006/article/details/4567957)  

[java中嵌套接口](http://blog.csdn.net/zhugewendu/article/details/72792529)  

[ Java之嵌套接口和嵌套类了解和简单实例](http://blog.csdn.net/huangwenyi1010/article/details/53873457)  

[java中外部接口与内部接口的使用](http://blog.csdn.net/u012842688/article/details/50939533)  

[Java中的内部接口](http://blog.csdn.net/hspingcc/article/details/54922771)  

[Java 内部接口、回调](http://blog.csdn.net/dsc114/article/details/39893357)  

[Java在类中定义接口](http://blog.csdn.net/liuhaiabc/article/details/53352006)  

[Java基础课程-接口、内部类、回调函数讲解](http://blog.csdn.net/redarmy_chen/article/details/52105805)  

[java 接口、抽象类、具体类、内部类、匿名内部类的区别及它们之间的关系](http://blog.csdn.net/vlqin1/article/details/48809297)  

[内部类（闭包与回调）](http://blog.csdn.net/eyeooo/article/details/11971145)  

[第十章 内部类 内部类的作用、闭包、内部类继承、覆盖重写内部类、局部内部类、内部类标识符](http://blog.csdn.net/sinat_32955803/article/details/52298564)  










