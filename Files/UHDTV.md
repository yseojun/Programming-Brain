### 정의 및 특징
>ATSC 3.0 기반으로 제정된 방송 서비스
>IP 기반 방송 서비스를 제공한다
---
### 내용
- 기존 지상파 디지털 TV 방송 송수신 정합 규격과 역호환성이 보장되지 않는다
- Internet Protocol 기반으로 방송 서비스를 제공
	- IP망간의 이종 서비스(Broadcast & Broadband), 고정 및 이동 단말에서 방송 수신을 제공할 수 있는 프레임워크를 포함
	- HEVC 코덱, OFDM 방식을 채택
![[Pasted image 20231212174742.png]]
### [[ROUTE]] (Real-time Object delivery over Unidirectional Transport)
[[MPEG-DASH]]의 DASH-IF 프로파일 기반으로 세그먼트 단위로 구선되며, 전송 및 시그널링 방법을 정의한다

### MMTP (MPEG Media Transport Protocol)
- [[MPEG-DASH|MPEG-2 TS]], [[RTP]](UDP 기반)를 대체하는 protocol
- MPEG-2 TS는 IP network의 발전으로 호환성, 효율성이 떨어지는 문제가 있음
- RTP protocol
	- component당 하나의 media session만 가지는 문제
	- multiplexing없이 2개의 port를 제공
	- 비실시간 media에 제한된 지원
- Signaling
	- 수신 측에서 받은 package를 소비하는데 필요한 제어 정보를 전달
	- 전달만에서 MMTP packet들을 효율적으로 전달하는데 필요한 제어 정보 전달
	- 수신 측에서 받은 MMTP packet들로부터 멀티미디어 압축 데이터를 획득하는데 필요한 전송 parameter 전달
### MPU (Media Processing Unit)
- segment 단위
- 미디어 코덱의 종류와 무관하게 사용 가능

---
#통신 