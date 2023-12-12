# Multimedia Streaming의 방식
### Progressive Download
- HTTP protocol 사용
- 점진적으로 다운로드되어 재생되는 방식
- Client가 비디오를 클릭하면 Server로 부터 다운로드가 시작된다
- 전체 파일이 전부 다운로드 될 필요는 없지만, 중간 부분을 보려고 할 때 다운로드가 되지 않았다면 시청이 불가능하다
- 다운로드 방식이기 때문에 보안 문제가 있고, 중간에 시청을 중지할 경우 불필요한 파일 수신으로 대역폭이 낭비된다
- 고정된 비디오 품질
- 짧은 영상에 적합하다
### Pseudo Streaming
- Flash player, HTML5 player에서 지원
- 아직 다운로드 되지 않은 부분을 클릭하더라도 메타 프라임 정보를 갖고 있기 때문에 중간 부분 메타 프레임부터 다시 다운로드를 시작해 재생될 수 있다
- 화질을 Client가 선택가능하다

### [[RTMP]] (Real-Time Messaging Protocol)
- Pseudo Streaming은 지나간 부분은 삭제되지 않고 저장되지만, RTMP는 지나간 부분은 자동 삭제된다

### Adaptive HTTP Streaming
- RTMP와 pseudo streaming의 장점을 결합
- Server에 Chunk단위의 동영상을 가지고 Streaming을 하며, player가 이 Chunk조각을 연속된 Stream으로 연결한다
- 시청자의 network 환경을 인지하여 적절한 화질의 streaming을 하게 된다
##### 설계 요소
- 여러 화질로 미리 인코딩하여 저장, 전송한다
- buffer overflow 방지를 위해 fill rate를 낮추는 방법을 사용한다
	- fill rate 가 drain rate보다 낮게 설정

# [[HLS]] (HTTP Live Streaming)

# [[MPEG-DASH]]
- adaptive streaming에서 표준화된 protocol이 없는 문제점을 해결하기 위해, 일관성있는 서비스를 제공하기 위해 개발됨

---
