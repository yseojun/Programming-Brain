### Application framwork
- Activity manager
- Content providers
- View system
- Notification manager
- Resource manager

### AVD (Android virtual device)
- SDK Tools
- HAXM (hardware accelerated execution manager)

### 구조
>Application - Acticvity - View

- `Application` class
	- app이 실행될 때 자동으로 생성됨
- [[Activity]] class
	- activity manager에 의해 생성되며, activity가 실행될 때 생성된다
	- inherit가 필요
	- 모든 앱은 [[Manifest]] file을 가지고, 시작 activity 등 세팅이 가능
- [[Log]] class
	- `System.out.println()`은 안드로이드에서 사용 불가
	- VERBOSE : `Log.v(String tag, String msg)`로 log message를 커스텀 가능
- [[Toast]] class
	- 빠르게 작은 message를 띄워줄 수 있음

### Layout & View
- MVP pattern (Model-View-Presenter pattern)
- [[View_Java|View]]
	- TextView, EditText
	- Button, CompoundButton, CheckBox
	- ImageView, ImageButton
- [[Layout_Java|Layout]]

- ### [[Intent]]
- ### [[Threads_Java||Threads]]
- ### [[File_Java|File]]
- ### [[Menu_Java|Menu]]
- ### [[Dialog_Java|Dialog]]
---
#java #android