### 정의 및 특징
>메모리가 저장될 수 있는 n개의 엔트리를 포함한 set을 두고, Cache block개수 대신 set의 개수로 index를 나누어 set 내부에 정보를 저장하는 방식의 Cache 종류
---
###  내용
### [[Hit&Miss|Miss rate]] vs Set Associativity
Set을 n개로 나눌 때 Cache 전체의 크기가 크다면 엔트리가 많아 Miss rate가 애초에 낮다
하지만 Cache의 크기가 적을 때는 이런 Set Associative 전략의 효율이 커지게 되고
Cache의 크기가 적을수록 큰 폭으로, Set의 엔트리 개수가 늘어날 수록 Miss rate를 줄이게 된다

---
#컴퓨터구조 