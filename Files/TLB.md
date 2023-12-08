### 정의 및 특징
> Translation-lookaside buffer
> Page Table에 접근하는 것을 피하기 위해 최근에 사용된 주소 사상을 보관하고 있는 캐시
---
### 내용
메모리를 참조할 때마다 TLB에서 가상 페이지 번호를 찾아보고, 적중되면 실제 페이지 번호는 주소를 만드는 데 쓰이고 그 엔트리의 참조 비트는 1이 된다
TLB 실패가 발생하면 이 실패가 페이지 부재인지, TLB 실패인지 알아야 한다
![[Pasted image 20231208191400.png]]


---