---
title: 2nd Order Linear PDE
date: 2026-03-24
categories: [Mathematics, PDE]
tags: []
math: true
---

## Definition
A ***second order linear PDE*** in two independent variables $x$ and $y$ is given by

$$
a_{11}u_{xx} +2a_{12}u_{xy} + a_{22}u_{yy} + a_1u_x + a_2u_y + a_0u = f(x, y)
$$

where $a_{11}, a_{12}, a_{22}, a_1, a_2, a_0$ and $f$ are functions of $x$ and $y$. 

$u_{xy} = u_{yx}$로 가정하기 때문에 $a_{12}$가 아니라 $2a_{12}$로 정의됨을 주의하자.

---

## Theorem
By a linear transformation of the independent variables, the equation can be reduced to one of three forms, as follows:

**(i)** Elliptic case: If $a_{12}^2 < a_{11}a_{22}$, it is reducible to 

$$u_{xx} + u_{yy} + \cdots = 0$$

where $\cdots$ denotes terms of order less than 2.

**(ii)** Hyperbolic case: If $a_{12}^2 > a_{11}a_{22}$, it is reducible to 

$$u_{xx} - u_{yy} + \cdots = 0$$

**(iii)** Parabolic case: If $a_{12}^2 = a_{11}a_{22}$, it is reducible to 

$$u_{xx} + \cdots = 0$$

unless $a_{11} = a_{12} = a_{22} = 0$.

위 정의에서 우리는 $u_{xy}$의 계수를 그냥 $a_{12}$가 아닌 $2a_{12}$로 설정했으므로 정리를 사용할 때 반드시 $2$로 나눠줘야 함을 주의하자. 

### Proof
**(i)** For convenience, we assume $a_{11} = 1$ and $a_1 = a_2 = a_0 = 0$. Then

$$\begin{align*}
0 &= u_{xx} + 2a_{12}u_{xy} + a_{22}u_{yy} \\
&= u_{xx} + 2a_{12}u_{xy} + a_{12}^2u_{yy} + (a_{22} - a_{12}^2)u_{yy} \\
&= (\partial_x + a_{12} \partial_y)^2u + (a_{22} - a_{12}^2)\partial^2_y u \quad \cdots \quad (\ast)
\end{align*}$$
 
Since $a_{12}^2 < a_{11}a_{22}$, we let $b = \sqrt{a_{22} - a_{12}^2}$. Let substitute

$$\begin{align*}
x &= \xi \\
y &= a_{12} \xi + b \eta
\end{align*}$$ 

Then

$$\begin{align*}
\partial_\xi &= \partial_x + a_{12} \partial_y \\
\partial_\eta &= b \partial_y
\end{align*}$$ 

so that

$$(\ast): 0 = \partial^2_\xi u + \partial^2_\eta u. \blacksquare$$

---

## Example

---

## Remark
위 정의에서는 변수가 $x, y$로 두 개인 경우에 대해서만 정의했지만, 항상 변수가 두 개인 법은 없고 그러한 경우에도 위와 같은 내용의 논의를 할 수 있어야 한다. 

변수가 $x_1, ..., x_n$으로 총 $n$개 주어져 있다고 할 때 second order linear PDE는 실수 계수 $a_{ij}, a_i, a_0$에 대해서 다음과 같이 작성할 수 있다.

$$\sum_{i, j = 1}^n a_{ij} u_{x_i x_j} + \sum_{i=1}^n a_i u_i + a_0u = 0 \quad \cdots \quad (\ast)$$

마찬가지로 $a_{ij} = a_{ji}, \forall i, j$가 성립한다. 즉 행렬 $A = [a_{ij}] \in \mathbb{R}^{n \times n}$은 실수 대칭행렬이므로 Hermitian이고, 따라서 orthogonally diagonalizable하다. 즉 직교행렬 $B \in \mathbb{R}^{n \times n}$이 존재해서 

$$B^TAB = D = \begin{bmatrix} \lambda_1 & & 0 \\ & \ddots & \\ 0 & & \lambda_n \end{bmatrix}$$

가 성립한다. 여기서 $\lambda_i$는 행렬 $A$의 고유값이다.

**(i)** The PDE $(\ast)$ is called ***elliptic*** if $A$ is positive definite or negative definite.

**(ii)** The PDE $(\ast)$ is called ***hyperbolic*** if none of the eigenvalues are zero and one of them has the opposite sign from the $(n-1)$ others.

**(iii)** The PDE $(\ast)$ is called ***parabolic*** if exactly one of the eigenvalue is zero and all others have the same sign.