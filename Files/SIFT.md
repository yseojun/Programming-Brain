### 정의 및 특징
>Scale Invariant Feature Transform
>Scale과 Rotation에 대한 특징점을 추출하기 위한 알고리즘
---
### 내용
각 픽셀에 대한 여러 Orientation의 변화값을 구하는데, 이를 이미지에서 여러 dimension으로 나누어 각 dimension에서 변화값들을 각각 측정한다

이 벡터는 1로 평준화되어 표시한다

이렇게 구한 값이 비슷하면 같은 Feature임을 얘기한다
![[SIFT.png]]

### SIFT의 특징
- Orientation (방향) 의 개수
	- subregion의 개수, 즉 dimension의 크기가 4 $\times$ 4일 때부터 정확도가 안정화 된다
	- Orientation의 개수는 8개가 적당
- Noise에 강함
- 어느 정도의 Affine에 강함 (40도 이상을 넘어가면 정확도가 50% 아래로 떨어지기 시작)
- 특징점 구별 정확도가 높음

---
