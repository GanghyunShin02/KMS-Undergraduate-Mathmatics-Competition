# 알아두어야할것들

기본적인 선형대수학.

## 일반화된 코시-슈바르츠 부등식.
   
$$ \int_{a}^{b} f(x)dx \int_{a}^{b}g(x)dx >=(\int_{a}^{b}f(x)g(x)dx)^2 $$
$$\{||}v\{||} \{||}u\{||}>=|v\cdot u|^2 $$

## 비네-코시 정리 (Binet-Cauchy Theorem)

$$
\underline{\underline{A}} = \underline{\underline{U}} \, \underline{\underline{V}} \text{ 로 분해했을 때,}
$$
$$
\det(\underline{\underline{A}}) = \sum_{1 \le i < j \le n} |\underline{\underline{P_{ij}}}| |\underline{\underline{Q_{ij}}}|
$$
$$
\begin{cases} 
\underline{\underline{P_{ij}}} : \text{행렬 } U \text{에서 } i, j \text{번째 열들로 만든 정사각행렬} \\
\underline{\underline{Q_{ij}}} : \text{행렬 } V \text{에서 } i, j \text{번째 행들로 만든 정사각행렬} 
\end{cases}
$$



$n \times m$ 행렬 $U$와 $m \times n$ 행렬 $V$의 곱 $A = UV$ ($n < m$)에 대하여:

$$
\det(A) = \sum_{1 \le i_1 < i_2 < \dots < i_n \le m} \det(U_{i_1 \dots i_n}) \det(V_{i_1 \dots i_n})
$$

여기서 각 항의 의미는 다음과 같습니다:
*   $\det(U_{i_1 \dots i_n})$ : $U$에서 **$i_1, \dots, i_n$번째 열**만 뽑아서 만든 $n \times n$ 행렬식
*   $\det(V_{i_1 \dots i_n})$ : $V$에서 **$i_1, \dots, i_n$번째 행**만 뽑아서 만든 $n \times n$ 행렬식

> **핵심 직관:** 
> "전체 행렬식은 가능한 모든 $n \times n$ 크기의 **'짝꿍 조각'**들의 행렬식을 곱해서 더한 것과 같다."
>
> ### 2 \times n 행렬에 대한 예시 ($n$차원 벡터 $a, b, c, d$ 활용)

행렬 
$A = \begin{pmatrix} a^T \\ b^T \end{pmatrix} \begin{pmatrix} c & d \end{pmatrix}$
일 때:

$$
\det(A) = \sum_{1 \le i < j \le n} 
\underbrace{
\begin{vmatrix} a_i & a_j \\ b_i & b_j \end{vmatrix}
}_{\text{U의 i, j열}}
\underbrace{
\begin{vmatrix} c_i & d_i \\ c_j & d_j \end{vmatrix}
}_{\text{V의 i, j행}}
$$

*   **좌변:** 전체 공간에서의 내적 정보 (Gram Determinant)
*   **우변:** 각 $i, j$ 좌표 평면으로 투영된 평행사변형 넓이들의 곱
