### 정의 및 특징
>사각형의 window를 만들어 미세하게 상하좌우로 이동시킬 때, window 내부의 픽셀 차이가 크다면 특징점일 확률이 높다고 판단하는 방식
---
### 내용
### 판단의 종류
- Flat
	모든 방향으로 window를 움직였을 때 변화가 없다면 Flat
- Edge
	edge 방향으로 변화가 없다면 Edge
- Corner
	모든 방향에서 큰 변화가 있다면 Corner

판단을 내릴 때 x축, y축 방향으로 각각 변화의 정도를 측정이 가능한데, 이 두 값으로 flat, edge, corner를 판단

## [[R (Harris Corner Detector)|R]]
- 세로 변화, 가로 변화율로 'R'을 계산해 이 값으로 Flat, Edge, Corner를 판단
- 이 R에 대한 threshold를 주어 Corner의 범위를 제한하고 Feature Point를 예측

# 속성에 따른 Harris Corner Detector의 효과
### Rotation
- 두 이미지에서 특징점을 비교할 때, 한 이미지에 대한 다른 이미지의 기울기가 '90도, 180도'에 가까우면 정확도가 높지만, '45도, 135도'와 같은 회전이 일어났을 때는 정확도가 떨어짐
### Scale
- 이미지의 크기를 키워서 특징점을 비교하면(Zoom), 이미지의 크기를 키울 수록 특징점을 찾기가 힘들어짐
- 이를 해결하기 위해 Window Circle의 크기를 바꿈
- 원의 크기에 대한 함수를 확인, 그 함수에서 Peak에 해당하는 원의 크기가 가장 적절한 크기
	- 이 원에 대한 함수는 각각의 이미지에서 독립적으로 뽑아내야 함
	- 함수의 Peak의 범위가 크거나, 여러개의 Peak가 있다면 좋지않은 함수

---
#이미지처리 #Feature_Point #HarrisCornerDetector