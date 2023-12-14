### Register 종류
- Command Register
	- CPU가 명령을 내릴 때, write, read등의 명령어를 전달하기 위한 register
- Data Register
	- 실제 데이터를 저장하는 register
- Status Register
	- 기기가 어떤 상태인지, 어떤 이벤트를 수행하는지 정보를 포함하는 register
I/O Device는 status register에 write 권한을 가지는데, 이런 상태를 전부 CPU가 처리하기에 부담이다
CPU의 처리와 I/O device의 읽기/쓰기 처리를 비동기적으로 처리하기 위해 [[DMA controller]]가 사용된다