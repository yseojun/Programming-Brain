### Feature Detector
- ##### [[Harris Corner Detector]]
- ##### [[SIFT]]
### Feature Matching
- ##### [[RANSAC]]
# Good Feature Point
- 두 이미지에서 같게 보여야 함
- 충분한 texture 변화가 필요하지만, 그렇다고 너무 변화가 심하면 안됨
- '진짜' 표면이여야 함
	![[Pasted image 20231213180142.png]]
- 시간이 지나더라도 변형이 일어나면 안됨

# 예시 : Photo Tourism
여러 사진들에서 [[Feature Points]]들을 탐색, 

각각의 pair 사이의 변환 [[homography]]들을 구하고 RANSAC을 활용해 데이터셋을 정제

여러 사진들 중 연관성 있는 사진끼리 묶어 구현