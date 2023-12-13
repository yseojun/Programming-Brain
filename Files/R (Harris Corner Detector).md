$\lambda_1$:가로 변화율, $\lambda_2$:세로 변화율
$$R=detM-k(traceM)^2$$
$$R=\lambda_1\times\lambda_2-k(\lambda_1+\lambda_2)^2$$
![[Harris Corner R.png]]

이렇게 구한 R 값의 크기에 따라 
>Flat : 0에 가깝게 작음
>Edge : R < 0
>Corner : R > 0 (충분히 큼)

여기서 R에 대한 threshold를 증가시켜 Corner의 범위를 제한 시킬 수 있는데
범위를 점에 가깝게 제한 시켜 나온 점들을 Feature Point로 예상한다

---
#HarrisCornerDetector