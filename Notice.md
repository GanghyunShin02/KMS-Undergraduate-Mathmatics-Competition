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
 ### 2 \times n 행렬에 대한 예시 ($n$차원 벡터 $a, b, c, d$ 활용)

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



    dratic form)과 준정부호 행렬(semi difinite)
## 2차형식(qudratic form) 과 준정부호행렬(semi difinite)

2차형식이란 모든 차수가 동일한 함수를

$$
 \underline{x^T} \underline{\underline{A}} \underline{x} 
$$ 

꼴로 나타낸것.


# 이차형식(Quadratic Form)과 준정부호 행렬(Semidefinite Matrix)

## 1. 이차형식(Quadratic Form)

이차형식은 모든 항의 차수가 2인 다항식을 의미한다.

2변수의 경우 일반적인 형태는

$$
Q(x,y)=ax^2+bxy+cy^2
$$

이다.

예를 들어,

$$
Q(x,y)=x^2-xy+y^2
$$

는 이차형식이다.

---

## 2. 행렬을 이용한 표현

이차형식은 항상 다음과 같이 표현할 수 있다.

$$
Q(\mathbf{x})=\mathbf{x}^T A \mathbf{x}
$$

여기서

$$
\mathbf{x}
==========

\begin{bmatrix}
x\
y
\end{bmatrix}
$$

이고,

$$
A=
\begin{bmatrix}
a & \frac{b}{2}\
\frac{b}{2} & c
\end{bmatrix}
$$

이다.

예를 들어

$$
Q(x,y)=x^2-xy+y^2
$$

는

$$
Q(x,y)
======

\begin{bmatrix}
x & y
\end{bmatrix}
\begin{bmatrix}
1 & -\frac12\
-\frac12 & 1
\end{bmatrix}
\begin{bmatrix}
x\
y
\end{bmatrix}
$$

로 표현된다.

실제로 전개하면

$$
x^2-xy+y^2
$$

가 된다.

---

## 3. 정부호와 준정부호

행렬 (A)에 대해

$$
Q(\mathbf{x})=\mathbf{x}^T A \mathbf{x}
$$

의 부호에 따라 행렬을 분류한다.

### 양의 정부호 (Positive Definite)

모든 (\mathbf{x}\neq0)에 대하여

$$
\mathbf{x}^T A \mathbf{x}>0
$$

이면 (A)를 양의 정부호라고 한다.

예:

$$
A=
\begin{bmatrix}
1&0\
0&1
\end{bmatrix}
$$

이면

$$
Q=x^2+y^2>0
$$

이다.

---

### 양의 준정부호 (Positive Semidefinite)

모든 (\mathbf{x})에 대하여

$$
\mathbf{x}^T A \mathbf{x}\ge0
$$

이면 (A)를 양의 준정부호라고 한다.

예:

$$
A=
\begin{bmatrix}
1&0\
0&0
\end{bmatrix}
$$

이면

$$
Q=x^2
$$

이고 항상 음수가 되지 않는다.

다만

$$
(x,y)=(0,1)
$$

에서는

$$
Q=0
$$

이 된다.

따라서 양의 정부호는 아니지만 양의 준정부호이다.

---

## 4. 고유값과의 관계

대칭행렬은 항상 직교대각화가 가능하다.

$$
A=P\Lambda P^T
$$

여기서

$$
\Lambda=
\begin{bmatrix}
\lambda_1 & & \
& \lambda_2 & \
& & \ddots
\end{bmatrix}
$$

는 고유값 행렬이다.

새 변수

$$
\mathbf{y}=P^T\mathbf{x}
$$

를 정의하면

$$
Q(\mathbf{x})
=============

# \mathbf{x}^T A \mathbf{x}

\mathbf{y}^T \Lambda \mathbf{y}
$$

가 되고,

$$
Q(\mathbf{x})
=============

\lambda_1 y_1^2
+\lambda_2 y_2^2
+\cdots
+\lambda_n y_n^2
$$

로 표현된다.

따라서

* 모든 고유값이 양수이면 양의 정부호
* 모든 고유값이 0 이상이면 양의 준정부호
* 음의 고유값이 하나라도 존재하면 준정부호가 아님

을 알 수 있다.

즉,

$$
A \text{ 가 양의 준정부호}
\iff
\lambda_i\ge0
\quad
(\forall i)
$$

이다.

---



## 6. 최소값과 행렬식

(m)을 증가시키면 어느 순간 행렬의 가장 작은 고유값이 0이 된다.

이때가 최소값을 결정하는 경계점이다.

고유값 중 하나가 0이면

$$
\det(A)=0
$$

이므로

$$
\left(1-2m\right)\left(1-m\right)-\frac14=0
$$

을 풀면

$$
8m^2-12m+3=0
$$

을 얻는다.

따라서

$$
m
=

\frac{3\pm\sqrt3}{4}.
$$

이 중 작은 값이 함수의 최소값이므로

$$
\boxed{
m=
\frac{3-\sqrt3}{4}
}
$$

가 된다.

---

## 결론

이차형식은 행렬로 표현할 수 있으며, 이차형식의 부호는 행렬의 고유값과 직접적으로 연결된다.

특히

$$
\mathbf{x}^T A \mathbf{x}\ge0
$$

가 모든 (\mathbf{x})에 대해 성립하는지 확인하는 문제는

행렬의 모든 고유값이 0 이상인지 확인하는 문제와 동치이다.

이를 이용하면 다변수 함수의 최소값 문제를 고유값 또는 행렬식 문제로 변환하여 효율적으로 해결할 수 있다.



  
