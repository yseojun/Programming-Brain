### 정의 및 특징
>프로세서와 메인 메모리 사이에 있는, 메모리의 상위 계층
---
### 내용

#### Address
- Memory Address는 Tag, Data, Offset으로 이루어져있다
- Cache에는 Valid bit, Tag, Data를 저장한다
- Tag
	 8 block Direct mapped cache를 예를 들면, 
	 십진수 22는 이진수로 바꾸면 `10 110` 인데, 8 block 이므로 8로 나눈 `10`을 Tag에 저장한다
	 Memory와 Cache의 Tag를 비교하여 같다면 Hit, 다르면 Miss로 판별해 Cache에 저장할 지 결정한다
 - Valid bit
	 - 엔트리에 유효한 주소가 있는지 표시
	  - 0이면 유효한 블록이 없음

#### Cache의 종류
1. [[Direct Mapped Cache]]
2. [[Set Associative Cache]]
3. [[Fully Associative Cache]]
종류마다 Cache Block의 저장할 수 있는 index의 제한이 다르다
제한을 풀수록 [[Hit&Miss|Miss rate]]는 올라가는 장점이 있지만, 
엔트리를 비교할 ****Comparator***가 필요하기 때문에 비용이 비싸진다는 단점이 있다
또한 적중 시간도 증가한다는 단점이 있다

#### Cache & Memory inconsistent
- 데이터를 데이터 캐시에만 쓰고 메모리에 쓰지 않으면 메인 메모리는 캐시와 다른 값을 갖게 됨
- Write-through : 항상 데이터를 메모리와 캐시에 같이 쓰는 방식
	- Write buffer : 항상 데이터를 같이 쓰면 성능 저하가 심하게 일어나므로, 데이터가 메모리에 써질 때까지 기다리는 동안 buffer에 데이터를 저장해둠
- Write-back : 쓸 때는 캐시에만 쓰고, 나중에 캐시에서 쫓겨날 때 메모리 계층에 쓰는 방식

#### Cache의 성능 측정
>$Memory Stall Cycles$
>$= \frac{Memory Access}{Program} * Miss Rate * Miss Penalty$
>$=\frac{Instructions}{Program}*\frac{Misses}{Instruction}*MissPenalty$

#### [[Memory Access Time]] 계산
**평균 메모리 접근 시간 = hit time + miss rate X [[Miss penalty]]

#### Multilevel Caches

#### Cache Performance

#### Snoopy Protocol


---
#컴퓨터구조 