EditText
===

[EditText 基本用法](https://www.cnblogs.com/yishaochu/p/5785234.html)  

[Android开发之EditText属性详解](http://www.cnblogs.com/weixing/p/3257058.html)  

[EditText，这篇就够了](https://blog.csdn.net/thanksforandroid/article/details/70859894)  

[Android UI系列-----EditText和AutoCompleteTextView](https://www.cnblogs.com/xiaoluo501395377/p/3411359.html)  

[Android TextWatcher三个回调详解，监听EditText的输入](https://blog.csdn.net/zengsidou/article/details/78665301)  

[Android 文本监听接口TextWatcher详解](https://blog.csdn.net/zhuwentao2150/article/details/51546773)  

[用TextWatcher限制输入长度并弹出提示](https://blog.csdn.net/max2005/article/details/78325009)  

[android 代码设置EditText的hint字符](https://blog.csdn.net/bzlj2912009596/article/details/79549312)  

[EditText显示明文与密码](https://www.cnblogs.com/liunanjava/p/5744088.html)  

[控件EditText的setOnEditorActionListener方法的使用](https://blog.csdn.net/u010041075/article/details/65445043)  
~~~
各种属性对应:
imeOptions=”actionUnspecified” –> EditorInfo.IME_ACTION_UNSPECIFIED
imeOptions=”actionNone” –> EditorInfo.IME_ACTION_NONE
imeOptions=”actionGo” –> EditorInfo.IME_ACTION_GO
imeOptions=”actionSearch” –> EditorInfo.IME_ACTION_SEARCH
imeOptions=”actionSend” –> EditorInfo.IME_ACTION_SEND
imeOptions=”actionNext” –> EditorInfo.IME_ACTION_NEXT
imeOptions=”actionDone” –> EditorInfo.IME_ACTION_DONE
~~~

[Android Studio 软键盘的监听事件setOnEditorActionListener](https://blog.csdn.net/i_love_program__19/article/details/80135946)  

[EditText软键盘弹出关闭等使用总结](https://blog.csdn.net/lnn368/article/details/51201148)  

[android EditText光标位置(定位到最后)](https://www.cnblogs.com/jenson138/p/4342699.html)  
http://blog.csdn.net/sww_simpcity/article/details/8949374  

~~~
方法：edittext.setSelection(int);
et.setText(content);//设置EditText控件的内容
et.setSelection(content.length());//将光标移至文字末尾

editText.requestFocus();获取焦点

如果对edittext组件设置了editText.setFocusable(false);需要重新获取焦点则必须执行：

    editText.setFocusable(ture);
    editText.setFocusableInTouchMode(true);
    editText.requestFocus();

注意：这种情况下，当重新点击文本框，是无法打开软键盘，必须点击第二次才能打开。

如果改为：
editText.clearFocus(); 失去焦点
~~~










