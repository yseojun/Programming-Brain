### 정의 및 특징
>
---
### Event Listner
- onClickListner()
- onLongClickListner()
- onTouchListner()
- onCreateContextMenuListner()

### Event handler
- onClick()
- onLongClick()
- onFocusChange()
- onKey()
- onTouch()
- onCreateContextMenu()

### UI
- View : widget
- ViewGroup : layouts

- UI의 요소는 [[Layout_Java|XML]] 파일에서 선언
- Java 파일에서 요소들을 run-time에 객체 인스턴스화

```Java
Activity.setContentView(int layoutResID);

Activity.findViewById(int id);
```

```java
String[] array = {"asd", ..., "ssd"};

adapter = new android.widget.ArrayAdapter<String>(this, android.R.layout.simple_list_item_1, array);

listView1.setAdapter(adapter);
```


---
