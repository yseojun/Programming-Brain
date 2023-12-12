>`res/layout` 폴더에 저장

```XML
<ViewGroup
	xmlns:android="http://schemas.android.com/apk/res/android" // 필수
	android:orientation="vertical" // 필수
	android:layout_width="match_parent"
	android:layout_height="wrap_content" >
	
	<View ... />
	...
	
</ViewGroup>
```

```XML
<View
	android:id="@" // refer
	android:id="@+" // 추가
	android:id="@+id/" // R.id에 추가
	android:layout_width="match_parent"
	android:layout_height="wrap_content"/>
```


### Grid
```XML
<GridLayout
	android:columnCount="5"
	android:rowCount="9">
	<EditText
		android:layout_column="0" android:layout_row="0"
		android:layout_columnSpan="5"
		android:layout_gravity="fill_horizontal"
		android:hint="Number 1" />
	...
</GridLayout>
```


### 비율
heigth, width : 0dp
weight : 1이상의 값 -> 비율 세팅 가능