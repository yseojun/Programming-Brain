### 정의 및 특징
>메인 메모리의 일부를 사용하여 Cache로 동작 시키는 기술
---
###  내용
>Virtual page number | Virtual page offset

가상 메모리 블록은 [[Page (virtual memory)|Page]]라고 불리며, 가상 메모리 실패는 Page Fault라고 불린다
Page는 연속적으로 할당할 필요가 없고, 이때문에 적은 메모리로 많은 프로세스에 분배가 가능하다
### [[TLB]]
Page Table이 메인 메모리에 있기 때문에 모든 메모리 접근은 2배의 시간이 걸리는데, `실제 주소를 얻기 위한 메모리 접근`또한 지역성을 가져 변환에 사용되는 특별한 캐시가 사용된다


---
#컴퓨터구조 