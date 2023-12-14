### 정의 및 특징
>프로세서와 메인 메모리 사이에 있는, 메모리의 상위 계층
---
### 내용

#### Address
> Tag | Data | Offset

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
엔트리를 비교할 ****Comparator***, ****Multiplexor***가 필요하기 때문에 비용이 비싸진다는 단점이 있다
또한 적중 시간도 증가한다는 단점이 있다

#### Cache & Memory inconsistent
- 데이터를 데이터 캐시에만 쓰고 메모리에 쓰지 않으면 메인 메모리는 캐시와 다른 값을 갖게 됨
- Write-through : 항상 데이터를 메모리와 캐시에 같이 쓰는 방식
	- Write buffer : 항상 데이터를 같이 쓰면 성능 저하가 심하게 일어나므로, 데이터가 메모리에 써질 때까지 기다리는 동안 buffer에 데이터를 저장해둠
- Write-Buffer : 일단 버퍼에 데이터를 써두고, 버퍼가 가득 찼을 때만 지연을 시켜 메모리 계층에 쓰는 방식
- Write-back : 쓸 때는 캐시에만 쓰고, 나중에 캐시에서 쫓겨날 때 메모리 계층에 쓰는 방식

#### Cache의 성능 측정
>$MemoryStallCycles$
>$= \frac{Memory Access}{Program} \times Miss Rate \times Miss Penalty$
>$=\frac{Instructions}{Program}\times\frac{Misses}{Instruction}\times MissPenalty$

ex)
I-cache miss rate = 2% (insturction)
D-cache miss rate = 4% (Data)
Miss panalty = 100 cycles
Base CPI = 2
Load & Store -> 36% of instructions

I-cache -> - $0.02 \times 100 = 2$
D-cache -> $0.36 \times 0.04 \times 100 = 1.44$
Actual CPI = Base CPI + Ideal + D $= 2 + 2 + 1.44 = 5.44$


#### [[Memory Access Time]] 계산
**평균 메모리 접근 시간 = hit time + miss rate X [[Miss penalty]]

#### Multilevel Caches
클럭속도 4GHz -> 0.25ns/클럭 사이클
Base CPI = 1

Miss Panalty = 100ns
Miss rate = 2%

100/0.25 = 400 클럭 사이클
- 1 + 2% $\times$ 400 = 9

2차 Cache 접근 5ns, Miss rate = 0.5%
5ns / 0.25 = 20 클럭 사이클
- 1 + 2% $\times$ 20 + 0.5% $\times$ 400 = 3.4

##### [[Cache Coherence]]
여러개의 Cache를 사용하면 Cache 일관성 문제가 생길 수 있다

---
#컴퓨터구조 