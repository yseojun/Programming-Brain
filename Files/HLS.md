### 정의 및 특징
>Apple에서 제작한 HTTP protocol로 전송되는 multimedia protocol
>live, prerecord를 둘 다 지원하며, HTTPS 기반 암호화와 유저 인증을 지원한다
---
### 내용
- 대락 10초 정도의 길이로 음성과 영상을 segment로 쪼개어 전송한다
- 'index' 파일에서 media의 URL을 제공

### 구조
#### 1. Server component
- 여러 해상도 제공을 준비
- 전송에 적합한 형식으로 압축, encapsulate
#### 2. Distribution component
- Client의 요청을 받고 준비된 media를 전송할 권한이 있다
- master index파일 -> index파일 -> ts파일 -> HTTP 통신
#### 3. Clint software
- 요청을 보낼 적절한 media를 결정한다
- 파일을 다운로드 받고, 연속적인 stream이 이루어지도록 합친다
- heuristics(경험 기반 학습) 데이터를 사용해 적절한 변환 시간을 결정한다

---
#통신 