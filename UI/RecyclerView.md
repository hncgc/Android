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


