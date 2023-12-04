### 정의 및 특징
>[[Data hazard]] 를 해결하기 위한 하나의 방법
> Execution 직후 값을 전달하거나, Load 직후 불러온 값을 전달한다
---
###  내용
![[Control & forwarding data path.png]]
#### 1. Execution

#### 2. Load

이런 forwarding을 활용해도 어쩔수 없이 지연해야하는 상황도 존재한다
이런 지연을 [[Bubble]] 이라고 컴퓨터구조에서 부른다

#### Forwarding Unit
Forwarding unit은 ID/EX에서 Rs1, Rs2를 전달 받고,
EX/MEM 혹은 MEM/WB에서 Rd, WB비트를 전달 받는다
이 때 WB 비트이면서 Rs1 혹은 Rs2가 ***이전 instrutcion의 Rd***와 같다면, Forwarding을 해야한다

Forwarding이 필요하다면 Forwarding Unit은 어디에서 forward 되었는지, 어떤 Resister를 대체할 지 Mux에 전달한다


---
#컴퓨터구조 