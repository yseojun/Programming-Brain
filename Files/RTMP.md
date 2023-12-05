### 정의 및 특징
>Real-Time Messaging Protocol
>[[TCP]]기반의 지속적, 실시간 통신을 수행할 수 있는 통신 protocol
---
### 특징
1. TCP를 기반으로 지속적, 실시간 통신이 가능
2. 양방향 stream 통신 가능
3. Multi-Stream
	  여러 데이터 묶음을 한번의 연결로 통신 가능
4. Stream fragmentation
	  데이터를 조각으로 나누어 전송, 이 조각들의 크기는 서버 상황에 따라 유동적으로 결정한다
5. Virtual Channels
	  여러개의 가상 channel들을 두어 각각 packet들을 보낸다
	  이는 재전송을 요구할 상황, 즉 error확률을 줄여 [[TCP]]기반이지만 error처리 시간을 줄일 수 있게 한다

### 종류
- RTMP
	- [[TCP]]의 1935번 port를 사용
	- 1935 시도에 실패하면 433(RTMPS) 혹은 80(RTMPT)로 재시도
- RTMPT (Tunneled)
	- [[HTTP]]의 80번 port를 사용
	- 방화벽 통과를 위해 데이터를 [[HTTP]]로 감싼 것을 의미 
	- [[HTTP]] 헤더로 인해 기본 RTMP보다는 크기가 크다
- RTMPS (Secure)
	- 데이터를 [[HTTPS]]로 감싼 것
	- TLS/SSL connection상에서 동작한다
- RTMPE (Encrypted)
	- 128비트로 암호화 된 RTMP
	- SSL 인증 절차가 없다
	- 암호화 채널을 사용하기 떄문에 기본형보다 성능에 영향을 줄 수 있다
- RTMPTE (Encrypted & Tunneled)
	- 80번 port 사용
	- Flash Player 필요
	- 성능에 영향을 줄 수 있다
- RTMFP (Flow protocol)
	- 기본형과 다르게 [[UDP]]에서 동작한다
	- 낮은 지연 스트리밍
	- 여러 Adobe Flash Player 간 P2P 통신이 가능하다
	- 항상 암호화된 상태로 데이터를 전송

### 동작 과정
- Handshake
	- 컨텐츠의 복제를 방지
	- Client가 0x03을 보내고 임의의 byte들을 전송하게 되면, Server가 Client에게 0x03과 수신받은 동일한 임의의 byte들로 응답하여 통신을 시작한다
- [[Chunk Stream]]
	- 데이터를 종류별로 나누어 종류별로 Chunk Stream을 만들고, Chunk Stream은 Chunk들로 이루어져있다
	- 이렇게 보내진 Chunk Stream은 동일한 timestamp로 demutiplex 되는데, 각각의 Chunk들을 Chunk stream ID를 근거로 하나의 Chunk Stream으로 합친다

---
#통신