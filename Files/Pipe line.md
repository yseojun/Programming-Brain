### 정의 및 특징
> RISC-V와 같은 컴퓨터의 프로그램 단계를 5단계로 나누고, 각각의 단계별로 개별 instruction의 해당 단계를 수행하도록 하는 시스템
---
###  내용
#### pipe line Speedup
`명령어 사이의 시간(pipe lined) = 명령어 사이의 시간(non-pipe lined) / 파이프 단계
이상적인 파이프 라인 시스템은 위 식에 따른 성능 향상을 보이지만, 단계가 완벽하게 균형잡혀있지 않고, 실제로는 오버헤드의 발생으로 실제 성능 향상값은 이보다 낮다
#### RISC-V의 5단계 pipe line
1. IF (Instructrion Fetch)
2. ID (Instruction Decode)
3. EX (Excution)
4. MEM (Memory)
5. WB (Write Back)

각각의 단계에서 쓰기와 읽기는 사용하는 부분이 달라 동시에 수행할 수 있고, 이를 활용해 hazard 해결에 활용한다

#### Pipeline Control
![[instruction Control data path.png]]
instruction에 따라 RegWrite, ALUSRC, PCSrc, MemRead, MemWrite, MemtoReg 비트를 설정하고, 이 비트들이 필요로 할 때까지 계속 전달한다

- EX : ALUOp, ALUSrc 신호
	- ALUSrc - 인가된 경우 명령어의 12비트 변위가 부호확장되어 ALU의 두번째 피연산자가 된다 (lw,sw일 때)
- M : Branch, MemRead, MemWrite
- WB : MemtoReg, RegWrite
#### [[Hazard]]
다음 명령어가 다음 클럭 사이클에 실행될 수 없는 상황이 있는데 이를 [[Hazard]]라고 부른다.

- pipe line Data path
![[Pipe line data path.png]]


---
#컴퓨터구조