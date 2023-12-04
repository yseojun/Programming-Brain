### 정의 및 특징
>Cache의 각각의 block에 저장할 수 있는 memory의 index가 `block number % blocks in cache` 인 Cache의 한 종류
---
###  내용
#### Address
Address : `Tag | Index | offset`
Cache에 `valid bit | Tag | Data`를 저장
Tag끼리 비교하여 일치하면 Hit, 불일치하면 Miss


---
