RecyclerView
===

[RecyclerView实现Item点击事件处理](https://www.jianshu.com/p/4e5631a5c9bc)  

------------------
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
