4.适配器(为了便于扩展，此处仅提供接口)

    ```java
    package me.shyboy.swipelayout;
	import android.app.Activity;
	import android.util.DisplayMetrics;
	import android.view.LayoutInflater;
	import android.view.MotionEvent;
	import android.view.View;
	import android.view.ViewGroup;
	import android.widget.ArrayAdapter;
	import android.widget.HorizontalScrollView;
	import android.widget.LinearLayout;
	import java.util.List;