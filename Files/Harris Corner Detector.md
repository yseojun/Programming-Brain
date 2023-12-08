### 정의 및 특징
>사각형의 window를 만들어 미세하게 상하좌우로 이동시킬 때, window 내부의 픽셀 차이가 크다면 특징점일 확률이 높다고 판단하는 방식
---
### 내용
### 판단의 종류
- flat
	모든 방향으로 window를 움직였을 때 변화가 없다면 flat
- edge
	edge 방향으로 변화가 없다면 edge
- corner
	모든 방향에서 큰 변화가 있다면 corner

판단을 내릴 때 x축, y축 방향으로 각각 변화의 정도를 측정이 가능한데, 이 두 값으로 flat, edge, corner를 판단


---
#이미지처리 #Feature_Point