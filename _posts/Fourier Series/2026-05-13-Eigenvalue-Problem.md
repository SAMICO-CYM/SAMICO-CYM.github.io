--- 
title: Eigenvalue Problem
date: 2026-05-13
categories: [Mathematics, Fourier Series]
tags: []
math: true
---

구간 $(a, b)$에서 정의된 고유값 문제 

$$X'' + \lambda X = 0$$

을 고려하자. 연산자를 $\mathcal{L} = -D^2$으로 두면 $\mathcal{L}X = \lambda X$의 형태가 된다.

한편 위 문제는 사실상 2계 선형 미분방정식이기도 하므로, 경계조건을 부여해서 생각할 수 있다. 이때 각각의 경계조건 

$$\begin{cases}
\text{Dirichlet BD: } X(a) = 0 = X(b) \\
\text{Newmann BD: } X'(a) = 0 = X'(b) \\
\text{Periodic BD: } X(a) = X(b), \quad X'(a) = X'(b)
\end{cases}$$

을 부여하면 각각에 대해서 연산자 $\mathcal{L} = -D^2$은 항상 Hermitian이다.

$\big[(\because)$ 함수 $X$와 $Y$에 대해서 위 경계조건이 적용된다고 가정하자. 이때 다음이 성립한다.

$$\begin{align*}
\langle -D^2 X, Y \rangle &= \int_a^b -X''Y \\
&= -X'Y \Bigg \vert_a^b + \int_a^b X'Y' \\
&=-X'Y \Bigg \vert_a^b +XY' \Bigg \vert_a^b - \int_a^b XY'' \\
&= -X'Y \Bigg \vert_a^b +XY' \Bigg \vert_a^b + \langle X, -D^2Y \rangle \\
&= [-X'(b)Y(b) + X'(a)Y(a)] + [X(b)Y'(b) - X(a)Y'(a)] + \langle X, -D^2Y \rangle.
\end{align*}$$

이때 $[-X'(b)Y(b) + X'(a)Y(a)] + [X(b)Y'(b) - X(a)Y'(a)]$ 항은 각각의 경계조건을 적용해주면 항상 $0$이 됨을 쉽게 알 수 있다. 따라서 

$$\langle -D^2 X, Y \rangle  = \langle X, -D^2Y \rangle $$

이므로 연산자 $-D^2$은 Hermitian이다.$\big]$

따라서 다음의 사실들이 성립한다.

**(i)** All the eigenvalues $\lambda$ are real.

**(ii)** All the eigenfunctions can be chosen to be real-valued.

**(iii)** There are infinite number of eigenvalues $\lambda_n$ such that $\lambda_n \to \infty$ with the corresponding eigenfunctions $X_n$ which are pairwise orthogonal. 