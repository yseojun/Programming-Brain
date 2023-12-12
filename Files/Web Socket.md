### 정의 및 특징
>Client와 Server간 지속적인, Full-Duplex 통신이 가능한 연결 형식
---
## 기존 [[HTTP]] 통신 방식
### Polling
- User 상호작용과 주기적인 polling이 필요하다
- 간단하다는 장점이 있지만, 앞선 정보들을 기록하지 않기 때문에 정보 활용이 불가능하고, 요청에 관한 중복된 정보가 전송될 수 있어 오버헤드가 발생할 수 있다
### Long Polling
- Clinet가 Server에 있는 정보를 요청하면 지정된 시간 또는 정보가 있을 때까지 연결을 열어둠
- 지속적으로 Server에 재연결 해야하는 문제가 있다

### Streaming
- Server가 지속적으로 업데이트되면 지정된 시간동안 열린 상태로 유지하고 응답을 전송하고 관리한다
- Server에서 메시지를 전달할 준비가 되면 응답을 업데이트 한다
- Client의 요청이 없어도 계속 Server가 열려있고 전송하는 문제

### [[Ajax]] (Asynchronous JavaScript and XML)
- 서버와 비동기 HTTP 통신을 하기 위한 기술
- Server에 HTTP 요청을 보낸 뒤, XML, JSON 형식 등의 응답을 받아 페이지의 일부만을 변경한다
- 전체를 새로고침하지 않아도 갱신이 가능
- Half-Duplex 통신이 가능하다

### [[jQuery]]
- 웹 브라우저 종류에 상관없이 같은 방식으로 Ajax를 구현하도록 다양한 method를 제공

## 개념
- Full duplex & bi-directional 단일 socket 연결 형식
- 한 번 요청하고 연결이 이뤄지면 Server와 Client모두 언제든지 메시지를 송신할 수 있게 되기 때문에 지연이 많이 줄어듦
- [[TCP]] 기반으로 동작
- 요청-응답의 구조에서 벗어남
- Client의 단 한가지 요구조건은 javaScript library를 실행할 수 있어야 한다
- 

---
#통신 