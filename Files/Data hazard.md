### 정의 및 특징
> 어떤 단계가 다른 단계가 끝나기를 기다려야 하기 때문에 파이프라인이 지연되는 경우 발생하는 [[Hazard]]
> ***Read-After-Write hazard*** 라고도 부른다
---
###  내용
```
add x19, x0, x1
sub x2, x19, x3
```
위 예시 instruction code는 `sub`를 수행할 때 앞선 `add`에서 저장하는 resister 값을 사용한다
`add` 명령어는 write back을 수행하는 5단계 까지는 결과값을 수행하지 않기 때문에, 이 경우 3개의 클럭 사이클을 낭비하게 된다

#### 해결방법
1. 컴파일러 스케쥴링 강화
	```
	lw  x1, 0(x0)
	lw  x2, 4(x0)
	add x3, x1, x2 - hazard
	sw  x2, 12(x0)
	lw  x4, 8(x0)
	add x5, x1, x4 - hazard
	sw  x5, 16(x0)
	```
	
	```
	lw  x1, 0(x0)
	lw  x2, 4(x0)
	lw  x4, 8(x0)
	add x3, x1, x2
	sw  x3, 12(x0)
	add x5, x1, x4
	sw  x5, 16(x0)
	```
	위와 같이 동일한 연산도 컴파일러 스케쥴링을 바꿔 hazard를 해결할 수 있다

2. [[forwarding]] (bypassing)
	Load forwarding
	![[Write back forward Data path.png]]

---
#컴퓨터구조