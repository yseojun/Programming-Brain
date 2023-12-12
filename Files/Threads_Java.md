```java
@Override protected void onCreate(Bundle savedInstanceState) {
	⋯
	buttonStart.setOnClickListener(new View.OnClickListener() { 
		@Override public void onClick(View view) {
			new Thread() {  
				public void run() {
					for (int i = probressBar1.getProgress(); i < probressBar1.getMax(); i++) { 
					runOnUiThread(new Runnable() {
						public void run() {
							progressBar1.setProgress(progressBar1.getProgress() + 1);
							textView1.setText(“Progress: ” + progressBar1.getProgress() + “%”);
						} 
					});
					SystemClock.sleep(100); // update for every 100 millisecs }
				}  
			}.start();  
			⋯ // spawns second thread and do tasks for the thread

		} 
	});
}
```