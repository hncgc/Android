Android 键盘
---

[ChatKeyboard](https://github.com/CPPAlien/ChatKeyboard)  

[XhsEmoticonsKeyboard 最良心的开源表情键盘解决方案](https://github.com/w446108264/XhsEmoticonsKeyboard)  

[Android 软键盘监听事件](http://blog.csdn.net/breeze666/article/details/27082419)  

[Android监听键盘弹出收起](https://blog.csdn.net/u011181222/article/details/52043001)  

~~~~~~
软键盘关闭后编辑辑修改行数

    @BindView(R.id.et_description)
    EditText mEtDescription;

    @BindView(R.id.v_free)
    View mVFree;
    
        /**
         * 软键盘监听
         */
        SoftKeyBoardListener.setListener(this, new SoftKeyBoardListener.OnSoftKeyBoardChangeListener() {
            @Override
            public void keyBoardShow(int height) {
                mEtDescription.setLines(10);
            }

            @Override
            public void keyBoardHide(int height) {
                mEtDescription.setLines(18);
                mVFree.setVisibility(View.VISIBLE);
            }
        });
        
------------

    <EditText
        android:id="@+id/et_description"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:background="@color/transparent"
        android:gravity="top"
        android:hint="@string/share_description"
        android:lines="10"
        android:maxLength="1000"
        android:paddingLeft="@dimen/px14"
        android:paddingTop="@dimen/px15"
        android:paddingRight="@dimen/px14"
        android:paddingBottom="5dp"
        android:textColor="@color/black_3"
        android:textColorHint="@color/gray"
        android:textSize="@dimen/px14" />

    <View
        android:id="@+id/v_free"
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:visibility="gone"/>

    <include layout="@layout/common_view_line_gray" />
    
-----------
/**
 * 监听键盘弹出收起
 */
public class SoftKeyBoardListener {
    private View rootView;//activity的根视图
    int rootViewVisibleHeight;//纪录根视图的显示高度
    private OnSoftKeyBoardChangeListener onSoftKeyBoardChangeListener;

    public SoftKeyBoardListener(Activity activity) {
        //获取activity的根视图
        rootView = activity.getWindow().getDecorView();

        //监听视图树中全局布局发生改变或者视图树中的某个视图的可视状态发生改变
        rootView.getViewTreeObserver().addOnGlobalLayoutListener(new ViewTreeObserver.OnGlobalLayoutListener() {
            @Override
            public void onGlobalLayout() {
                //获取当前根视图在屏幕上显示的大小
                Rect r = new Rect();
                rootView.getWindowVisibleDisplayFrame(r);

                int visibleHeight = r.height();
                System.out.println(""+visibleHeight);
                if (rootViewVisibleHeight == 0) {
                    rootViewVisibleHeight = visibleHeight;
                    return;
                }

                //根视图显示高度没有变化，可以看作软键盘显示／隐藏状态没有改变
                if (rootViewVisibleHeight == visibleHeight) {
                    return;
                }

                //根视图显示高度变小超过200，可以看作软键盘显示了
                if (rootViewVisibleHeight - visibleHeight > 200) {
                    if (onSoftKeyBoardChangeListener != null) {
                        onSoftKeyBoardChangeListener.keyBoardShow(rootViewVisibleHeight - visibleHeight);
                    }
                    rootViewVisibleHeight = visibleHeight;
                    return;
                }

                //根视图显示高度变大超过200，可以看作软键盘隐藏了
                if (visibleHeight - rootViewVisibleHeight > 200) {
                    if (onSoftKeyBoardChangeListener != null) {
                        onSoftKeyBoardChangeListener.keyBoardHide(visibleHeight - rootViewVisibleHeight);
                    }
                    rootViewVisibleHeight = visibleHeight;
                    return;
                }

            }
        });
    }

    private void setOnSoftKeyBoardChangeListener(OnSoftKeyBoardChangeListener onSoftKeyBoardChangeListener) {
        this.onSoftKeyBoardChangeListener = onSoftKeyBoardChangeListener;
    }

    public interface OnSoftKeyBoardChangeListener {
        void keyBoardShow(int height);

        void keyBoardHide(int height);
    }

    public static void setListener(Activity activity, OnSoftKeyBoardChangeListener onSoftKeyBoardChangeListener) {
        SoftKeyBoardListener softKeyBoardListener = new SoftKeyBoardListener(activity);
        softKeyBoardListener.setOnSoftKeyBoardChangeListener(onSoftKeyBoardChangeListener);
    }
}


~~~~~~

[Android windowSoftInputMode软键盘显示和隐藏的监听和实现](http://blog.csdn.net/u010852801/article/details/43198313)  

[KeyboardView 自定义安全键盘](https://github.com/GitPhoenix/KeyboardView)  

[Keyboard 仿京东，支付宝密码键盘和密码输入框](https://github.com/GitPhoenix/Keyboard)  




-----------------------------
[EditText的setSelection属性](https://www.aliyun.com/jiaocheng/21703.html)  

[控件EditText的setOnEditorActionListener方法的使用](https://blog.csdn.net/u010041075/article/details/65445043)  
编辑完之后点击软键盘上的各种键才会触发  

Android 键盘表情符过滤
---

[Android 过滤特殊字符和emoji表情](https://blog.csdn.net/luckrr/article/details/53784066)  

[Android过滤emoji表情](https://blog.csdn.net/b1480521874/article/details/53887029)  

[Android 准确过滤(禁止) Emoji表情](https://www.jianshu.com/p/1c04c3617469)  

[Android过滤emoji表情](https://blog.csdn.net/b1480521874/article/details/53887029)  

[android edittext如何过滤掉Emoji表情](https://ask.csdn.net/questions/340898)  

[Android禁止输入表情符号](https://blog.csdn.net/XiNanHeiShao/article/details/73252891)  















