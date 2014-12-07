2.实现原理:用HorizontalScrollView作为ListView的item，然后让内容区的宽度和屏幕宽度一样，把操作区挤出去，就可以实现这个功能了。
3.先写前端布局文件
  * listView的item布局文件

   	```markup
    <!--item_swipe-->
    <?xml version="1.0" encoding="utf-8"?>
	<HorizontalScrollView
    	xmlns:android="http://schemas.android.com/apk/res/android"
    	android:id="@+id/hsv"
    	android:layout_width="match_parent"
    	android:layout_height="wrap_content"
    	android:scrollbars="none" >
    	<LinearLayout
        	android:id="@+id/item_view_container"
        	android:layout_width="wrap_content"
        	android:layout_height="match_parent"
        	android:orientation="horizontal"
            >
    	</LinearLayout>
	</HorizontalScrollView>
   	```