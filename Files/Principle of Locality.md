### 정의 및 특징
>메모리에서 어떤 항목이 참조될 때, 참조된 항목과 그 근처의 항목에 대해 또 다시 참조될 가능성이 있는데 이를 Principle of Locality (지역성의 원칙)이라고 한다
---
###  내용

지역성에는 두가지 종류가 있는데

1. [[Temporal Locality]] (시간적 지역성)
	  한 번 참조된 항목은 또다시 참조될 가능성이 크다
2. [[Spatial Locality]] (공간적 지역성)
	  어떤 항목이 참조됐다면, 그 항목 근처의 항목이 참조될 가능성이 크다

예를 들면 `sum` 이라는 변수에 배열을 차례로 저장하는 프로그램을 작성했을 때, 
sum을 계속 호출해 연산을 하는 것은 Temporal Locality
배열을 차례로 호출에 연산을 하는 것은 Spatial Locality라고 할 수 있다

또 어떤 loop instruction을 수행한다면
특정 instruction을 순서대로 수행하는 것은 Spatial Locality
반복해서 특정 instruction들을 수행하는 것은 Temporal Locality라고 할 수 있다

---
#컴퓨터구조 