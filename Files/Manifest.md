### 정의 및 특징
>
---
### 내용
- markup langauge
- package 이름
- [[Activity]], services, broadcast receivers, content providers
- app이 필요한 권한
- app에 요구되는 하드웨어, 소프트웨어

### [[Intent]]-filter
- 제일 처음 실행되는 [[Activity]] 설정
```XML
<manifest ⋯ >  
	<application android:label=“APP_NAME”>
		<activity android:name=“.ACTIVITY_CLASS_NAME” android:label=“LABEL_NAME”> 
			<intent-filter> ***
				<action android:name=“android.intent.action.MAIN” />
				<category android.name=“android.intent.category.LAUNCHER” />
			</intent-filter> ***
		</activity>
	
		<activity ⋯ > ⋯ </activity>
	</application>

</manifest>
```

`finish()` 가 실행되면 이전 [[Activity]]로 돌아간다

### Application permission
```XML
<manifest ... >
	<uses-permission android:name="android.permission.MANAGE_EXTERNAL_STORAGE"/>
	<activity android:name=".MainActivity" ...>
		<intent-filter> ... </intent-filter>
	</activity>
</manifest>

```


---
