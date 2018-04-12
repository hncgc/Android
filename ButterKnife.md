Butter Knife
---
Butter Knife添加依赖 不生效 
http://blog.csdn.net/zheng548/article/details/51722973

ButterKnife的使用以及不能自动生成代码问题的解决
http://www.cnblogs.com/zhengjunfei/p/5910497.html

Android Butter Knife 框架——最好用的View注入
http://www.jianshu.com/p/9ad21e548b69
http://jakewharton.github.io/butterknife/

https://github.com/JakeWharton/butterknife

class ExampleActivity extends Activity {
  @BindView(R.id.user) EditText username;
  @BindView(R.id.pass) EditText password;

  @BindString(R.string.login_error) String loginErrorMessage;

  @OnClick(R.id.submit) void submit() {
    // TODO call server...
  }

  @Override public void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.simple_activity);
    ButterKnife.bind(this);
    // TODO Use fields...
  }
}


资源绑定
--------
绑定资源到类成员上可以使用@BindBool、@BindColor、@BindDimen、@BindDrawable、@BindInt、@BindString。使用时对应的注解需要传入对应的id资源，例如@BindString你需要传入R.string.id_string的字符串的资源id。

例如在Fragment中：


public class FancyFragment extends Fragment {
    @BindView(R.id.button1) Button button1;
    @BindView(R.id.button2) Button button2;

    @Override public View onCreateView(LayoutInflater inflater, ViewGroup container, Bundle savedInstanceState) {
        View view = inflater.inflate(R.layout.fancy_fragment, container, false);
        ButterKnife.bind(this, view);
        // TODO Use fields...
        return view;
    }
}

在ListView的Adapter中，我们常常会使用ViewHolder
    static class ViewHolder {
        @BindView(R.id.title)
        TextView name;
        @BindView(R.id.job_title) TextView jobTitle;

        public ViewHolder(View view) {
            ButterKnife.bind(this, view);
        }
    }

监听器绑定

@OnClick(R.id.submit)
public void submit(View view) {
  // TODO submit data to server...
}

而监听器方法的参数可选的：
@OnClick(R.id.submit)
public void submit() {
    // TODO submit data to server...
}

可以指定多个View ID到一个方法上，这样，这个方法就成为了这些View的共同事件处理。

@OnClick({ R.id.door1, R.id.door2, R.id.door3 })
public void pickDoor(DoorView door) {
    if (door.hasPrizeBehind()) {
        Toast.makeText(this, "You win!", LENGTH_SHORT).show();
    } else {
        Toast.makeText(this, "Try again", LENGTH_SHORT).show();
    }
}


重置绑定:

Fragment的生命周期与Activity不同。在Fragment中，如果你在onCreateView中使用绑定，那么你需要在onDestroyView中设置所有view为null。为此，ButterKnife返回一个Unbinder实例以便于你进行这项处理。在合适的生命周期回调中调用unbind函数就可完成重置。

public class FancyFragment extends Fragment {
    @BindView(R.id.button1) Button button1;
    @BindView(R.id.button2) Button button2;
    private Unbinder unbinder;

    @Override public View onCreateView(LayoutInflater inflater, ViewGroup container, Bundle savedInstanceState) {
        View view = inflater.inflate(R.layout.fancy_fragment, container, false);
        unbinder = ButterKnife.bind(this, view);
        // TODO Use fields...
        return view;
    }

    @Override public void onDestroyView() {
        super.onDestroyView();
        unbinder.unbind();
    }
}

-------


[Butterknife](https://github.com/JakeWharton/butterknife)  

[ButterKnife：8.1.0的使用](http://www.jianshu.com/p/0392199a682b)  

[Android Butter Knife 框架——最好用的View注入](http://www.jianshu.com/p/9ad21e548b69)  

