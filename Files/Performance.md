- Algorithm에 따른 instruction의 수
- Programming language, compiler, architechure에 따른 instruction의 수
- Processor, memory에 따른 instruction의 속도
- I/O system의 연산의 속도
위와 같은 내용으로 컴퓨터의 성능을 측정할 수 있다

#### 성능 측정의 지표
- Reponse time (실행 시간, 지연 시간)
- Throughput (대역폭)
프로세서 추가의 경우는 Throughput만 증가됨

$$Perfomnace = 1/Execution Time$$

#### 시간 측정
- Elapsed time (Total time)
- CPU time
	- I/O, OS overhead등을 제외한 순수하게 주어진 명령을 수행하는 시간
	- CPU Clock Cycle $\times$ Clock Cycle Time
	- CPU Clock Cycle / Clock Rate
ex) 2GHz clock, 10s CPU time

#### Instruction Count
$$ClockCycle=InstructionCount\times CPI$$
$$CPUTime=InstructionCount\times CPI \times ClockCycleTime$$

#### CPI
$$ClockCycle=\sum_{i=1}^{n} CPI_i\times Instruction Count_i$$

#### [[Benchmarks]]
동일한 프로그램을 실행해서 성능을 측정할 때, 기준이 되는 프로그램

---
