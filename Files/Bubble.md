### 정의 및 특징
>컴퓨터 구조 pipe line에서 단계의 지연을 의미하는 별칭
>Stall이라고도 부른다
---
###  내용
#### Stall을 명령하는 방법
ID/EX의 Control value를 0으로 만든다
EX, MEM, WB는 `nop`(no-operation)를 실행한다

#### Hazard Detection Unit
`lw` 직후에 `add`를 한다고 할 때, 데이터 메모리에서 load할 때 까지 기다려야한다
이 때 input Resister와 load하는 Resister를 비교해 같다면, Hazard Detection Unit이 control signal을 0으로 만들어 다음 instruction을 nop로 만든다
이렇게 한차례 연기한 후 forwarding을 활용해 instruction을 정상적으로 동작시킨다

---
#컴퓨터구조 