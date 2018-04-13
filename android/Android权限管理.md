Android 权限管理
--------
[EffortlessPermissions](http://p.codekk.com/detail/Android/DreaminginCodeZH/EffortlessPermissions)  
项目地址：https://github.com/DreaminginCodeZH/EffortlessPermissions  
简介：基于 Google EasyPermissions 进行扩展的动态权限库

[AndroidPermission6.0](http://p.codekk.com/detail/Android/C-isCoder/AndroidPermission6.0)  
项目地址：https://github.com/C-isCoder/AndroidPermission6.0  
简介：一句解决 6.0 动态权限问题，支持 Rxjava、lambda  

[实战项目：Android6.0权限管理 工具，我用java重写别人的kotlin项目；地址： ](https://github.com/a1018875550/PermissionDispatcher)  

[Android开源项目-Easypermissions](http://www.jianshu.com/p/2b3661928e66)  
官方文档：https://github.com/googlesamples/easypermissions

动态权限
--------
Android6.0动态获取权限

[在Android 6.0 设备上动态获取权限](http://www.open-open.com/lib/view/open1447236259272.html)  

[Android 6.0: 动态权限管理的解决方案](http://www.2cto.com/kf/201601/487781.html)  
http://www.wangchenlong.org/2016/03/20/1603/204-manage-permission/
https://github.com/SpikeKing/wcl-permission-demo


[Android M Permission 运行时权限 学习笔记](http://www.cnblogs.com/mengdd/p/4892856.html)  

[打造简洁高效的动态权限管理器](http://www.tuicool.com/articles/M3q6ny)

[android 6.0权限问题处理的核心代码--shouldShowRequestPermissionRationale正确用法](http://blog.csdn.net/u011266694/article/details/52330364)  
private void requestPermission(String[] permissions) {
    boolean isMinSdkM = Build.VERSION.SDK_INT < Build.VERSION_CODES.M;
    if (isMinSdkM || permissions.length == 0) {
        PermissionHelper.getInstance().onAllPermissionGranted();
        return;
    }
    ActivityCompat.requestPermissions(this, permissions, 1);
}

@Override
public void onRequestPermissionsResult(int requestCode, @NonNull String[] permissions, @NonNull int[] grantResults) {
    super.onRequestPermissionsResult(requestCode, permissions, grantResults);
    for (int i = 0; i < grantResults.length; i++) {
        boolean isTip = ActivityCompat.shouldShowRequestPermissionRationale(this, permissions[i]);
        if (grantResults[i] != PackageManager.PERMISSION_GRANTED) {
            if (isTip) {//表明用户没有彻底禁止弹出权限请求
                requestPermission(PermissionHelper.getInstance().filterPermissions(permissions));
            } else {//表明用户已经彻底禁止弹出权限请求
             //   PermissionMonitorService.start(this);//这里一般会提示用户进入权限设置界面
            }
            return;
        }
    }
    PermissionHelper.getInstance().onAllPermissionGranted();
}

[Android6.0动态权限申请步骤以及需要注意的一些坑](http://www.jianshu.com/p/a51593817825)  
本demo github下载地址！！！  https://github.com/qianxiaoai/RuntimePermissionsDemo/tree/dev
Google提供的demo的下载地址 
https://github.com/googlesamples/android-RuntimePermissions

[Android 6.0 运行时权限处理完全解析](http://blog.csdn.net/lmj623565791/article/details/50709663)  
hongyangAndroid/MPermissions https://github.com/hongyangAndroid/MPermissions

[Android 6.0 动态权限申请注意事项](http://blog.csdn.net/uana_777/article/details/51211535)  

[Android6.0动态获取权限](http://blog.csdn.net/q4878802/article/details/50419004)  
动态获取权限

[谈谈Android 6.0 的动态权限管理](http://blog.csdn.net/qq_17766199/article/details/52013501)  
hotchemi/PermissionsDispatcher  
https://github.com/hotchemi/PermissionsDispatcher  
hongyangAndroid/MPermissions  
https://github.com/hongyangAndroid/MPermissions  
tbruyelle/RxPermissions  
https://github.com/tbruyelle/RxPermissions  

[Android M 新的运行时权限开发者需要知道的一切](http://www.jianshu.com/p/e1ab1a179fbb)  
hotchemi/PermissionsDispatcher
https://github.com/hotchemi/PermissionsDispatcher

[高德地图定位API Android 6.0权限说明](http://lbs.amap.com/api/android-location-sdk/guide/utilities/permission/)  

[targetSdkVersion 23以下6.0中调用checkSelfPermission的问题](https://my.oschina.net/u/990728/blog/549914)  

Android6.0的通讯录获取

每次在用到摄像头等，这样需要权限的操作的时候，都要动态判断一下权限
// 扫描功能
if (ContextCompat.checkSelfPermission(this, Manifest.permission.CAMERA) != PackageManager.PERMISSION_GRANTED) {
    //申请CAMERA权限
    ActivityCompat.requestPermissions(this, new String[]{Manifest.permission.CAMERA}, 3);
} else {
    Intent openCameraIntent = new Intent(this, CaptureActivity.class);
    startActivityForResult(openCameraIntent, 0);
}
如果没有权限，会弹窗提示用户，由用户来决定，是否给予该权限

用户选择完以后，会执行下面的回调
@Override
public void onRequestPermissionsResult(int requestCode, String[] permissions, int[] grantResults) {
    super.onRequestPermissionsResult(requestCode, permissions, grantResults);
    if (3 == requestCode) {
        if (grantResults[0] == PackageManager.PERMISSION_GRANTED) {
            // 授权
            Intent openCameraIntent = new Intent(this, CaptureActivity.class);
            startActivityForResult(openCameraIntent, 0);
        } else {
            // 未授权
        }
    }
}

[Android拍照，相册选择图片以及Android6.0权限管理](http://blog.csdn.net/zahngjialiang/article/details/52723236)  

[Android数据存储之Android 6.0运行时权限下文件存储的思考](http://www.cnblogs.com/whoislcj/p/6137398.html)  

<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"/>
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE"/>

总李写代码
http://www.cnblogs.com/whoislcj/

[Android 启动系统相机，相册，裁剪图片及6.0权限管理](http://www.jianshu.com/p/f38ee1d9098e)  

[Android 获取手机联系人实例代码详解](http://www.jb51.net/article/77047.htm)  
需要添加权限：

     <uses-permission android:name="android.permission.READ_CONTACTS" />
     <uses-permission android:name="android.permission.WRITE_CONTACTS" />

package com.org.demo.demo;
import com.org.wangfeng.R;
import android.app.Activity;
import android.content.Intent;
import android.os.Bundle;
import android.util.Log;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

public class GetPhoneActivity extends Activity {
	private EditText editText;
	private Button button;
	@Override
	protected void onCreate(Bundle savedInstanceState) {
		// TODO Auto-generated method stub
		super.onCreate(savedInstanceState);
		setContentView(R.layout.getphoneactivity);
		editText = (EditText) findViewById(R.id.et_getphone);
		button = (Button) findViewById(R.id.bb_getphone);
		button.setOnClickListener(new View.OnClickListener() {
			@Override
			public void onClick(View arg0) {
				// TODO Auto-generated method stub
				Intent intent = new Intent(GetPhoneActivity.this,ContactActivity.class);
				startActivityForResult(intent, 1);
			}
		});
	}

	@Override
	protected void onActivityResult(int requestCode, int resultCode, Intent data) {
		// System.out.println("resultCode:" + resultCode);
		// System.out.println("requestCode:" + requestCode);
		Log.d("jiejie", "被调用了");
		if (resultCode == Activity.RESULT_OK) {
			String phone = data.getStringExtra("phone");
			Log.d("jiejie", "_______________"+phone);
			phone = phone.replaceAll("-", "").replaceAll(" ", "");// 替换-和空格

			editText.setText(phone);// 把电话号码设置给输入框
		}
		super.onActivityResult(requestCode, resultCode, data);
	}
}

package com.org.demo.demo;

import java.util.ArrayList;
import java.util.HashMap;
import com.org.wangfeng.R;
import android.app.Activity;
import android.content.Intent;
import android.database.Cursor;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.AdapterView;
import android.widget.ListView;
import android.widget.SimpleAdapter;
import android.widget.AdapterView.OnItemClickListener;
import android.widget.TextView;

public class ContactActivity extends Activity {
	private ListView lvList;
	private ArrayList<HashMap<String, String>> readContact;
	private TextView back;
	@Override
	protected void onCreate(Bundle savedInstanceState) {
		super.onCreate(savedInstanceState);
		setContentView(R.layout.activity_contact);
		back =(TextView)findViewById(R.id.back);
		back.setOnClickListener(new View.OnClickListener() {   
			@Override
			public void onClick(View arg0) {
				// TODO Auto-generated method stub
				finish();
			}
		});
		lvList = (ListView) findViewById(R.id.lv_list);
		readContact = readContact();
		// System.out.println(readContact);
		lvList.setAdapter(new SimpleAdapter(this, readContact,R.layout.contact_list_item, new String[] { "name", "phone" },
			new int[] { R.id.tv_name, R.id.tv_phone }));
		lvList.setOnItemClickListener(new OnItemClickListener() {
			@Override
			public void onItemClick(AdapterView<?> parent, View view,int position, long id) {
				String phone = readContact.get(position).get("phone");// 读取当前item的电话号码
				Intent intent = new Intent();
				intent.putExtra("phone", phone);
				setResult(Activity.RESULT_OK, intent);// 将数据放在intent中返回给上一个页面
				finish();
			}
		});
	}

	private ArrayList<HashMap<String, String>> readContact() {
		// 首先,从raw_contacts中读取联系人的id("contact_id")
		// 其次, 根据contact_id从data表中查询出相应的电话号码和联系人名称
		// 然后,根据mimetype来区分哪个是联系人,哪个是电话号码
		Uri rawContactsUri = Uri.parse("content://com.android.contacts/raw_contacts");
		Uri dataUri = Uri.parse("content://com.android.contacts/data");
		ArrayList<HashMap<String, String>> list = new ArrayList<HashMap<String, String>>();
		// 从raw_contacts中读取联系人的id("contact_id")
		Cursor rawContactsCursor = getContentResolver().query(rawContactsUri,new String[] { "contact_id" }, null, null, null);
		if (rawContactsCursor != null) {
			while (rawContactsCursor.moveToNext()) {
				String contactId = rawContactsCursor.getString(0);
				// System.out.println(contactId);
				// 根据contact_id从data表中查询出相应的电话号码和联系人名称, 实际上查询的是视图view_data
				Cursor dataCursor = getContentResolver().query(dataUri,
					new String[] { "data1", "mimetype" }, 
					"contact_id=?",
					new String[] { contactId }, null);
				if (dataCursor != null) {
					HashMap<String, String> map = new HashMap<String, String>();
					while (dataCursor.moveToNext()) {
						String data1 = dataCursor.getString(0);
						String mimetype = dataCursor.getString(1);
						// System.out.println(contactId + ";" + data1 + ";"
						// + mimetype);
						if ("vnd.android.cursor.item/phone_v2".equals(mimetype)) {
							map.put("phone", data1);
						} else if ("vnd.android.cursor.item/name".equals(mimetype)) {
							map.put("name", data1);
						}
					}
					list.add(map);
					dataCursor.close();
				}
			}
			rawContactsCursor.close();
		}
		return list;
	}
}



