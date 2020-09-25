## Spinner

[Android 之 下拉框(Spinner)的使用](https://www.cnblogs.com/hualuoshuijia/p/10250226.html)  

[Android 下拉列表Spinner--AppCompatSpinner ](https://www.jianshu.com/p/7d1094a38597)  

[android Spinner控件详解](https://www.cnblogs.com/aademeng/articles/11072182.html)  

[android项目中spinner设置默认值](https://blog.csdn.net/u014624241/article/details/77963244)  

几种下拉框测试
---

~~~
中心显示弹窗
            List<String> spList = new ArrayList<>();
            spList.add("未定");
            spList.add("很生");
            spList.add("较熟");
            spList.add("很熟");
            SpinnerCommonAdapter spinnerCommonAdapter = new SpinnerCommonAdapter(mContext, spList);
            viewHolder.mSpinner.setAdapter(spinnerCommonAdapter);


Spinner下拉选框：功能正常

F:\AndroidSDK\platforms\android-28\data\res\layout\simple_spinner_item.xml

<?xml version="1.0" encoding="utf-8"?>
<TextView xmlns:android="http://schemas.android.com/apk/res/android" 
    android:id="@android:id/text1"
    style="?android:attr/spinnerItemStyle"
    android:singleLine="true"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:ellipsize="marquee"
    android:textAlignment="inherit"/>


F:\AndroidSDK\platforms\android-28\data\res\layout\simple_spinner_dropdown_item.xml
<?xml version="1.0" encoding="utf-8"?>
<!--
......
-->
<CheckedTextView xmlns:android="http://schemas.android.com/apk/res/android"
    android:id="@android:id/text1"
    style="?android:attr/spinnerDropDownItemStyle"
    android:singleLine="true"
    android:layout_width="match_parent"
    android:layout_height="?android:attr/dropdownListPreferredItemHeight"
    android:ellipsize="marquee"/>


            <Spinner
                android:id="@+id/spinner"
                android:layout_width="match_parent"
                android:layout_height="@dimen/dp_40"
                android:spinnerMode="dialog" />
改为：
                android:spinnerMode="dropdown" />


            String[] optionTypes = {" 未定  ", " 很生 ", " 较熟 ", " 很熟 "};
            List<String> stringList = Arrays.asList(optionTypes);;
            ArrayAdapter<String> adapter = new ArrayAdapter<String>(mContext,android.R.layout.simple_spinner_item,optionTypes);
            adapter.setDropDownViewResource(android.R.layout.simple_spinner_dropdown_item);
            viewHolder.mSpinner.setAdapter(adapter);

            viewHolder.mSpinner.setSelection(words.getSkillLevel(), true);

            // int spinnerPosition = viewHolder.mSpinner.getSelectedItemPosition();
            viewHolder.mSpinner.setOnItemSelectedListener(new AdapterView.OnItemSelectedListener() {
                @Override
                public void onItemSelected(AdapterView<?> parent, View view, int position, long id) {
                    setWordSkillLevel(wordId,position);
                    LogUtils.d("WordListAdapter mSpinner = " + position);
                }

                @Override
                public void onNothingSelected(AdapterView<?> parent) {

                }
            });
            viewHolder.mTvSkillSelect.setVisibility(View.GONE);


///////////////////////////////////////////////////////////////
// 弹窗式下拉选框，在底部的显示不完整，功能正常

F:\ReciteWords\app\src\main\java\com\mywords\app\view\popupwindow\SkillLevelSelectionPopupWidow.java

            <TextView
                android:id="@+id/tv_skill_select"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:textSize="@dimen/dp_15"
                android:text="选择" />

            viewHolder.mSpinner.setVisibility(View.GONE);
            List<String> spList = new ArrayList<>();
            spList.add("未定");
            spList.add("很生");
            spList.add("较熟");
            spList.add("很熟");

            viewHolder.mTvSkillSelect.setText(spList.get(words.getSkillLevel()));

            final  SkillLevelSelectionPopupWidow skillPopupWindow = new SkillLevelSelectionPopupWidow(mActivity, spList, new SkillLevelSelectionPopupWidow.SelectionListener() {
                @Override
                public void skillLevel0(String skillLevel0) {
                    viewHolder.mTvSkillSelect.setText(skillLevel0);
                    setWordSkillLevel(wordId,0);
                }

                @Override
                public void skillLevel1(String skillLevel1) {
                    viewHolder.mTvSkillSelect.setText(skillLevel1);
                    setWordSkillLevel(wordId,1);
                }

                @Override
                public void skillLevel2(String skillLevel2) {
                    viewHolder.mTvSkillSelect.setText(skillLevel2);
                    setWordSkillLevel(wordId,2);
                }

                @Override
                public void skillLevel3(String skillLevel3) {
                    viewHolder.mTvSkillSelect.setText(skillLevel3);
                    setWordSkillLevel(wordId,3);
                }

            });

            skillPopupWindow.setInitSelect(words.getSkillLevel());
            viewHolder.mTvSkillSelect.setOnClickListener(new View.OnClickListener() {
                @Override
                public void onClick(View v) {
                    skillPopupWindow.show(v);
                }
            });
///////////////////////////////////////////////////////////////

~~~

[Android自定义的下拉列表框控件](https://blog.csdn.net/u013068887/article/details/78294580)  



NiceSpinner
---

https://github.com/wolfking0608/nice-spinner  

[Android 下拉框第三方控件 NiceSpinner](https://blog.csdn.net/lilihan12358/article/details/79855138)  

[Android 中Nice Spinner 在项目的使用](https://www.jianshu.com/p/56daa08df95a)  

[Android第三方开源下拉框NiceSpinner使用详解](https://www.jb51.net/article/118503.htm)  

~~~
NiceSpinner

    implementation 'com.github.arcadefire:nice-spinner:1.3.4'

            <org.angmarch.views.NiceSpinner
                android:id="@+id/nice_spinner"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_margin="5dp"
                android:textSize="14sp"
                app:arrowTint="@color/colorPrimary"
                app:textTint="@color/colorAccent"/>

        @BindView(R.id.nice_spinner)
        NiceSpinner mNiceSpinner;

            // NiceSpinner
            final String[] selectValue = new String[1];
            String[] optionTypes = {"未定", "很生", "较熟", "很熟"};
            final List<String> stringList = Arrays.asList(optionTypes);
            viewHolder.mNiceSpinner.attachDataSource(stringList);
            viewHolder.mNiceSpinner.setSelectedIndex(words.getSkillLevel());
            viewHolder.mNiceSpinner.setTextColor(ContextCompat.getColor(mContext, R.color.colorPrimaryDark));
            viewHolder.mNiceSpinner.addOnItemClickListener(new AdapterView.OnItemClickListener() {
                @Override
                public void onItemClick(AdapterView<?> parent, View view, int position, long id) {
                    selectValue[0] = stringList.get(position);
                    setWordSkillLevel(wordId,position);
                    LogUtils.d("WordListAdapter mSpinner = " + position);
                }
            });


~~~


