### 정의 및 특징
>Virtual memory에서 가상 주소를 저장하는 공간
>Cache에서의 Block과 동일한 의미이다
---
### 내용
#### Page Table
>Valid bit | Physical page number

- Page table은 가장 주소의 Page 번호롤 인덱스되어 대응되는 실제 페이지 번호를 찾아준다
	각 프로그램은 Page table을 갖고 있고, 이 Page table은 가상 주소 공간을 메인 메모리로 사용한다
- Page table은 블록 주소 전부를 갖고 있기 때문에, Cache와는 다르게 Tag가 필요없다

- Page에 메모리가 존재한다면, PTE는 실제 주소와 status bit를 저장하고 있다
- Page에 메모리가 존재하지 않는다면, PTE는 메모리의 swap space를 가리키고 있다

---
