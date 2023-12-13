### 정의 및 특징
>서로 다른 두 이미지의 관계를 표현한 행렬

---
### 내용
- 점의 변환
$$
p' = H \times p
$$
$$
\begin{bmatrix}wx'\\wy'\\w\end{bmatrix}=\begin{bmatrix}h_{00}&h_{01}&h_{02}\\h_{10}&h_{11}&h_{12}\\h_{20}&h_{21}&h_{22} \end{bmatrix}\begin{bmatrix}x\\y\\1\end{bmatrix}$$
### Homography 구하기
$x'$와 $y'$를 아는 상태에서 H를 구할 때
$$
\begin{bmatrix}x'\\y'\\1\end{bmatrix}=\begin{bmatrix}h_{00}&h_{01}&h_{02}\\h_{10}&h_{11}&h_{12}\\h_{20}&h_{21}&h_{22} \end{bmatrix}\begin{bmatrix}x\\y\\1\end{bmatrix}
$$
- 위 식으로부터 $x'$와 $y'$를
$$
x' = \frac{h_{00}x+h_{01}y+h_{02}}{h_{20}x+h_{21}y+h_{22}}
$$
$$
y' = \frac{h_{10}x+h_{11}y+h_{12}}{h_{20}x+h_{21}y+h_{22}}
$$
위 두식을 만족하는 H 행렬을 구할 수 있다

이런 $(x_n,y_n)$ 의 여러 개의 점에 대한 H는 $||Ah-0||^2$ 값이 최소화 되는 h를 구해야 한다

---

