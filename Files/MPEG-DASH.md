### 정의 및 특징
> `Dynamic Adative Streaming over HTTP`
>MPEG-DASH이전의 adaptive [[Multimedia Streaming]]은 표준화된 protocol이 없었는데, 이를 해결해 일관된 서비스를 제공할 수 있게 개발된 표준 protocol
---
### 내용
작은 시간 단위로 쪼개진 주기에 Adaptation set이 각각 존재한다
Adaptation set은 video, audio, 자막 등으로 각각 나누어져 있고, Adaptation set 내부에 여러 품질의 media가 존재하고, 사용자의 입력 또는 사용자의 환경에 따라 품질을 변환하며 제공된다
### MPD (Media Presentation Description)
>계층 구조 : MPD - Period - Adpataton set - Representation - Segment
- XML 파일
- 사용가능한 content, URL 주소를 제공
- MPD 내부는 segment로 이루어져있고, Client는 이를 MPD parser, Segment parser를 이용해 합친다
- Period : period id, start time
- representation 내부의 segment에 URL 정보가 포함되어 있다



---
#통신 