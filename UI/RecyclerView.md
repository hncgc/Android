RecyclerView
===

[RecyclerView实现Item点击事件处理](https://www.jianshu.com/p/4e5631a5c9bc)  


[RecyclerView系列之三：处理item的点击事件](https://www.jianshu.com/p/971396467a62)  


------------------

通过在adapter中提供回调来实现item的点击事件

~~~

public class ChooseAndSearchEntitySimpleAdapter extends BaseRvAdapter {

    private OnRecyclerViewItemClickListenter mClickListenter;
    
    public void setClickListenter(OnRecyclerViewItemClickListenter clickListenter) {
        mClickListenter = clickListenter;
    }
    
    
    @Override
    public void onBindViewHolder(final RecyclerView.ViewHolder holder, int position) {
        ViewHolder viewHolder = (ViewHolder) holder;
        ......
        
                viewHolder.itemView.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                if (mClickListenter != null) {
                    mClickListenter.OnItemClick(view, viewHolder.getAdapterPosition());
//-----------------------------------------------------------------------------
//注意：viewHolder.getAdapterPosition()在RecyclerView不-1，在LRecyclerView中要-1
//------------------------------------------------------------------------------
                }
            }
        });
        
D:\gongwei-app2\app\src\main\java\com\gong_wei\ui\community\AddProductActivity.java


    @BindView(R.id.rv_brand_specialty)
    RecyclerView mRvBrandSpecialty;
    
    private ChooseAndSearchEntitySimpleAdapter mAdapter;
    
        mAdapter = new ChooseAndSearchEntitySimpleAdapter(this);
        //GwUtils.initRecyclerView(mRvBrandSpecialty, mAdapter, new LinearLayoutManager(this));
        mRvBrandSpecialty.setHasFixedSize(true);
        mRvBrandSpecialty.setLayoutManager(new LinearLayoutManager(this));
        mRvBrandSpecialty.setAdapter(mAdapter);
        mAdapter.setClickListenter(new OnRecyclerViewItemClickListenter() {
            @Override
            public void OnItemClick(View v, int position) {
                Log.d(TAG, "AddProductActivity OnItemClick position = " + position);
......
            }
        });
    }
~~~

------------------

[RecyclerView的Item以及子View点击事件](https://www.jianshu.com/p/8d5288b56f45)  

[android RecyclerView适配器实现多布局item+item内部控件点击事件](https://blog.csdn.net/qq_38225558/article/details/80627273)  

[Android中解决RecyclerView各种点击事件的方法](https://www.jb51.net/article/140578.htm)  

RecyclerView分割线
---

~~~

方法一:
RecyclerView分割线 包含上线与下线
        mRvReply.addItemDecoration(new GridItemDecoration(0, 2, ContextCompat.getColor(getApplicationContext(), R.color.gray_ligth)));

方法二:
添加自定义分割线加细线 包含上线与下线
        //添加自定义分割线加细线  
        DividerItemDecoration divider = new DividerItemDecoration(getContext(), DividerItemDecoration.VERTICAL);
        divider.setDrawable(ContextCompat.getDrawable(getContext(), R.drawable.custom_divider_thin_line));
        mRvProductRelation.addItemDecoration(divider);

D:\gongwei-app2\app\src\main\res\drawable\custom_divider_thin_line.xml

<shape xmlns:android="http://schemas.android.com/apk/res/android">
    <corners android:radius="0.5dp" />
    <solid android:color="@color/gray_ligth" />
    <size android:height="1dp" />
</shape>

方法三:
        //添加自定义分割粗线
        DividerItemDecoration divider = new DividerItemDecoration(getContext(), DividerItemDecoration.VERTICAL);
        divider.setDrawable(ContextCompat.getDrawable(getContext(), R.drawable.custom_divider));
        mRvQuestion.addItemDecoration(divider);
        
D:\gongwei-app2\app\src\main\res\drawable\custom_divider.xml
<shape xmlns:android="http://schemas.android.com/apk/res/android">
    <corners android:radius="5dp" />
    <solid android:color="@color/gray_ligth" />
    <size android:height="5dp" />
</shape>

方法四:
ReleaseAdapter.java

    private boolean dividerIsThick = false;
    private int dividerSize = 5;
    
    public void setDividerIsThick() {
        this.dividerIsThick = true;
    }

    public void setDividerIsThick(int dividerSize) {
        this.dividerIsThick = true;
        this.dividerSize = dividerSize;
    }
    
    /**
     * 设置粗分割线
     * @param viewDivider
     */
    private void setViewDivider(View viewDivider) {
        LinearLayout.LayoutParams params = (LinearLayout.LayoutParams) viewDivider.getLayoutParams();
        params.height = SystemUtils.dip2px(dividerSize, context);
        viewDivider.setLayoutParams(params);
        viewDivider.setBackgroundColor(ContextCompat.getColor(context, R.color.divider_gray_thick));
    }
    
    @Override
    public void onBindViewHolder(final RecyclerView.ViewHolder holder, int position) {
......
            BusinessViewHolder viewHolder = (ViewHolder) holder;
            if(dividerIsThick) {
                setViewDivider(viewHolder.mVDivider);
            }

    
    static class ViewHolder extends RecyclerView.ViewHolder {
    ......
        @BindView(R.id.v_divider)
        View mVDivider;
        
        ViewHolder(View view) {
            super(view);
            ButterKnife.bind(this, view);
        }
    }
    
D:\gongwei-app2\app\src\main\res\layout\fragment_release_business_item.xml
    <View
        android:id="@+id/v_divider"
        android:layout_width="match_parent"
        android:layout_height="0.5dp"
        android:layout_marginTop="@dimen/px8"
        android:background="@color/divider_gray_thin" />
    
    
~~~





