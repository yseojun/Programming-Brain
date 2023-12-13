### 정의 및 특징
>RTMP에서 전송되는 단위인 Chunk Stream과 그것을 이루는 Chunk는 정해진 형식이 존재한다
>
>Basic Header, Message Header, Extend Timestamp로 이루어져있고, 순서와 종류에 따라 정보를 포함할 수도 있고, 포함하지 않고 앞선 Chunk의 정보를 따르기도 한다
---
### Chunk Format
> Basic Header | Message Header | Extended Timestamp | Chunk Data
### 1. [[Basic Header]] (1~3 bytes)
- Chunk Stream ID와 Chunk type을 저장
- 길이는 Chunk Stream ID에 따라 결정된다
- 맨 앞 2 bit는 fmt로 구성
- 2~63 th : 1 byte
- 64~319 th : 2 byte
- 64~655 th
	- Chunk Stream ID와 Chunk type을 저장
	- 길이는 Chunk Stream ID에 따라 결정된다
	- 맨 앞 2 bit는 fmt로 구성
	- 2~63 th : 1 byte
	- 64~319 th : 2 byte
	- 64~65599 th : 3 byte
### 2. [[Mesasge Header]] (0, 3, 7, 11 bytes)
##### 4개의 type이 있는 이유?
- header를 압축하기 위해

- type은 message header로 정의한다
- Chunk Stream의 초반 Chunk에만 message steam ID와 message type, message length 정보가 필요 (2~63 th)
- timestamp는 이전 time에 대한 delta만 제공
##### Type 0 (11 bytes)
> timestamp | message length | message length | message type id | message stream id | message stream id 
- Chunk Stream의 시작에 무조건 사용된다
- timestamp가 뒤로 갈 때 사용된다
- Extend Timestamp (0, 4 bytes)
##### Type 1 (7 bytes)
> timestamp delta | message length | messge length | message type id
- message stream ID가 포함되지 않는데, 자동으로 앞선 Chunk의 정보를 가진다
##### Type 2 (3 bytes)
> timestamp delta
- timestamp delta 정보를 가진다
- Stream ID, message length가 포함되지 않는데, 자동으로 앞선 Chunk의 정보를 가진다
##### Type 3 (0 bytes)
- Message header가 존재하지 않는다
- 자동으로 앞선 Chunk와 같은 Chunk Stream ID를 가진다
### 3. [[Extend Timestamp]] (0, 4 bytes)


---
#통신 