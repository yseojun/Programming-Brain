### 정의 및 특징
>프로세서가 요구하는 정보가 상위 메모리에 있다면 이를 `Hit`라고 부르고, 없다면 `Miss`라고 부른다
---
###  내용
### Miss의 종류
	1. Compulsory misses - 제일 처음 miss
	2. Capacity misses - 용량 부족
	3. Conflict misses - 충돌, 덮어쓰기

###  Hit rate & Miss rate
Hit와 Miss의 비율을 측정해 `Hit rate`, `Miss rate`라고 한다
#### Block Size
64 block, 16 bytes / block인 cache를 예를 들면, 
주소가 1200인 memory의 block address는 1200/16 = 75, block number는 75%64=11 이다

고정된 Cache size에서 block의 크기를 키우면 block의 개수가 적어지고, 이는 miss rate를 높이게 된다
![[Pasted image 20231205205948.png]]
이렇게 block size가 커질 수록 Miss rate가 줄어드는 듯 하다가도, 일정 수준 이상 올라가면 효과가 없고, 오히려 Miss rate가 높아지기까지 한다

### Hit time
`Hit time`은 메모리 구조에서 상위 계층에 접근하는 시간이며, Hit/Miss를 결정하는데 필요한 시간이 포함된다

### [[Miss penalty]]
`Miss penalty`는 Miss일 때 하위 계층으로부터 상위 계층에 저장하고, 프로레서까지 전달하는 시간을 말한다

---
#컴퓨터구조 