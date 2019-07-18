Android图片
===

[Android Activity之间传递图片(Bitmap)的方法](https://www.jb51.net/article/40747.htm) 
传递失败 放大有效

[安卓开发小技巧：Activity之间传递图片](https://www.jianshu.com/p/e7e856bd17f2)  
传递成功

~~~~
                                    ByteArrayOutputStream baos = new ByteArrayOutputStream();
                                    bitmap.compress(Bitmap.CompressFormat.PNG, 100, baos);
                                    byte[] b = baos.toByteArray();
                                    mIvPic.setOnClickListener(new View.OnClickListener() {
                                        @Override
                                        public void onClick(View v) {
                                            ShowBigPictureActivity.startAction(ABCActivity.this, b);
                                        }
                                    });
                                    
                                    
    public static void startAction(Context context, byte[] b) {
        Intent intent=new Intent(context, ShowBigPictureActivity.class);
        intent.putExtra("bite", b);
        context.startActivity(intent);
    }
    
        Bundle extras = getIntent().getExtras();
        if(extras!=null) {
            byte[] b = extras.getByteArray("bite");
            bitmap = BitmapFactory.decodeByteArray(b, 0, b.length);
            Matrix matrix = new Matrix();
            matrix.postScale(2f, 2f);
            bitmap = Bitmap.createBitmap(bitmap, 0, 0, bitmap.getWidth(),
                    bitmap.getHeight(), matrix, true);
            mPhotoView.setImageBitmap(bitmap);
        }

~~~~

[体验非常好的Android图片手势控件PinchImageView](http://www.codesocang.com/kj-imageview/36647.html)  

[GitHub 上受欢迎的 Android UI Library整理(part_two)](https://blog.csdn.net/longxuanzhigu/article/details/93590773)  


[PhotoView实现图片随手势的放大缩小的效果](https://www.cnblogs.com/ruichenblogs/p/5192893.html)  

[android 开源photoView的使用](https://www.jianshu.com/p/6e38712e310f)  
https://github.com/chrisbanes/PhotoView   


[显示大图Activity（支持手势放大）](https://www.cnblogs.com/zyandroid/p/5013212.html)  

[超自然的点击图片放大](https://www.jianshu.com/p/d59d683609e1)  

-------------------------------

[Android背景模糊话模糊、高斯模糊（FastBlur）](https://blog.csdn.net/blank__box/article/details/80099359)  

[ Android 背景模糊](https://www.csdn.net/gather_2e/MtTakgwsNzgwNC1ibG9n.html)  


[android 获取当前屏幕作为毛玻璃模糊背景Acitivity作为弹出框。](https://www.cnblogs.com/CharlesGrant/p/4813735.html)  




