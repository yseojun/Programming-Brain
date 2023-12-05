### 정의 및 특징
>프로세서와 메인 메모리 사이에 있는, 메모리의 상위 계층
---
###  내용

#### Address
- Memory Address는 Tag, Data, Offset으로 이루어져있다
- Cache에는 Valid bit, Tag, Data를 저장한다
- Tag
	 8 block Direct mapped cache를 예를 들면, 
	 십진수 22는 이진수로 바꾸면 `10 110` 인데, 8 block 이므로 8로 나눈 `10`을 Tag에 저장한다
	 Memory와 Cache의 Tag를 비교하여 같다면 Hit, 다르면 Miss로 판별해 Cache에 저장할 지 결정한다

#### Cache의 종류
1. [[Direct Mapped Cache]]
2. [[Set Associative Cache]]
3. [[Fully Associative Cache]]
종류마다 Cache Block의 저장할 수 있는 index의 제한이 다르다
제한을 풀수록 [[Hit&Miss|Miss rate]]는 올라가는 장점이 있지만, 
엔트리를 비교할 Comparator가 필요하기 때문에 비용이 비싸진다는 단점이 있다

#### Multilevel Caches

#### Cache Performance

#### Snoopy Protocol


---
#컴퓨터구조 