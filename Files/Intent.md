```Java
public class ActivityOne extends Activity {  
	@Override protected void onCreate(Bundle savedInstanceState) {
	
	super.onCreate(savedInstanceState);
	setContentView(R.layout.activity_one);  
	⋯  
	someView1.setOnClickListener(new View.OnClickListener() {
	
		@Override public void onClick(View arg0) {  
			Intent intent = new Intent(getApplicationContext(), 
			ActivityTwo.class); 
			startActivity(intent);
		}
	}
}
```
``` java
public class ActivityTwo extends Activity {  
	@Override protected void onCreate(Bundle savedInstanceState) {
		super.onCreate(savedInstanceState);
		setContentView(R.layout.activity_two);
		⋯  
		someView2.setOnClickListener(new View.OnClickListener() {
			@Override public void onClick(View arg0) {  
				finish();
			}
		}
}
```

[[Extra]]