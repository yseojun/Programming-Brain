### 정의 및 특징
>[[RTMP]]에서 여러 종류의 데이터들을 multiplex해서 보내는데, 이 단위를 Chunk Stream이라고 한다
>Chunk Stream은 여러개의 Chunk들로 이루어져있다
---
### Chunk Stream
- 데이터를 종류별로 Chunk stream들로 나누어 전송하는데, 이렇게 나누어진 Chunk Stream들은 동일한 timestamp를 가지게 된다
- ex) Video, Audio, Metadata

### Chunk
- 각각의 chunk들은 Chunk Stream ID를 가지는데, 이를 기반으로 수신부에서 Chunk Stream으로 합친다

### Size
- Chunk의 크기가 클수록 보내는 개수가 줄어 CPU의 사용량은 줄어들지만, 크기가 크기 떄문에 열악한 환경에서 delay가 일어날 수 있다
- Chunk의 크기가 작을수록 고주사율 streaming에는 좋지 않다. 각각의 Chunk 마다 [[PCI]] 정보가 붙게 되는데, 똑같은 정보를 계속 보내기 때문에 비효율적이다.

### [[Chunk Format]]
- Chunk마다 Chunk Header가 붙어 전송된다
- Chunk Header는 Basic Header, Message Header, Extend Timestamp로 이루어져 있다

### Control Message
- Chunk Stream ID 2
- Message Stream ID 0

---
#통신