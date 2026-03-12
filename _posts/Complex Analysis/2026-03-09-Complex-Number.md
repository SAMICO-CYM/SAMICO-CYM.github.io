---
title: Complex Number
date: 2026-03-09
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Introduction
복소해석학은 복소 공간 $\mathbb{C}$에서 함수의 미분, 적분과 같은 해석학적 성질을 다루는 과목이다. 실해석학에서 그랬듯이, 미분과 적분에 앞서 연속성이나 극한과 같은 개념이 먼저 정의되어야 하고, 그러한 개념들은 필연적으로 복소수들 사이의 연산이나 크기과 같은 개념들을 요구한다. 따라서 복소해석학은 '복소수'란 체계가 어떤 구조를 가지고 있는지, 그 안에서 연산은 어떻게 정의되는지와 같은 대수적 성질을 다루는 것으로 시작한다.

## Definition 1
**(i)** ***Complex number set*** $\mathbb{C}$ is the set $\mathbb{C} = \\{ (x, y) \mid x, y \in \mathbb{R} \\}$ with the two binary operations, addition $+$ and multiplication $\cdot$, defined as follows:

Let $z_1 = (x_1, y_1)$ and $z_2 = (x_2, y_2)$ in $\mathbb{C}$. Then

$$
\begin{align*}
z_1 + z_2 &= (x_1, y_1) + (x_2, y_2) = (x_1 + x_2, y_1 + y_2) \\
z_1 \cdot z_2 &= (x_1, y_1) \cdot (x_2, y_2) = (x_1x_2 - y_1y_2, y_1x_2 + x_1y_2)
\end{align*}
$$

**(ii)** Let $z = (x, y) \in \mathbb{C}$. The real numbers $x$ and $y$ are called the ***real parts*** and the ***imaginary parts*** of $z$, denoted by 

$$\text{Re}(z) = x, \quad \text{Im}(z) = y$$

**(iii)** The ***real axis*** is the line in the complex plane consisting of points $(x, 0)$, which is the set $\mathbb{R} \times \\{ 0 \\}$.

**(iv)** The ***imaginary axis*** is the line in the complex plane consisting of points $(0, y)$, which is the set $\\{ 0 \\} \times \mathbb{R}$. The numbers $(0, y)$ in the imaginary axis is also called ***pure imaginary numbers*** if $y \neq 0$.

**(v)** Two complex numbers $z_1 = (x_1, y_1)$ and $z_2 = (x_2, y_2)$ are said to be ***equal*** if $x_1 = x_2$ and $y_1 = y_2$.

우리는 고등학교 때부터 실수 공간 $\mathbb{R}$이 복소 공간 $\mathbb{C}$의 부분집합이 된다는 사실을 배워왔다. 그런데 연산은 잠시 빼놓고 $\mathbb{C}$가 정의되는 방식만 놓고 본다면 사실상 그 원소들의 모양은 $\mathbb{R}^2$와 다를 바가 없고, 당연하게도 $\mathbb{R}$을 부분집합으로 가질리가 없다.

복소 공간과 그 안에서의 연산을 위와 같이 정의한 이유는 실수 공간에서의 연산과 성질을 그대로 유지하면서 자연스럽게 확장하기 위함이다. 고등학교 때 실수 $x$를 허수부가 $0$인 복소수로 간주할 수 있음을 배웠을 것이다. 즉 $x = x + 0 \cdot i$이다. 이걸 위의 정의대로 해석하면 실수 $x$는 복소 공간의 원소 $(x, 0)$으로 볼 수 있다. 다르게 말하면 $\mathbb{R}$과 $\mathbb{R} \times \\{ 0 \\}$ 사이의 isomorphism이 존재해서 두 공간의 연산이 모두 보존된다고 할 수 있다. 이러한 관점에서 $\mathbb{R}$은 $\mathbb{C}$의 부분집합이라고 할 수 있고, 덧셈과 곱셈은 위에서 정의한 연산이 그대로 적용된다. 동일하게 순허수들의 집합, 즉 $\\{ 0 \\} \times \mathbb{R}$ 또한 $\mathbb{C}$의 부분집합으로 간주할 수 있다. 따라서 앞으로 우리는 실수 혹은 순허수 $x$를 가져오면 자연스럽게 $(x, 0)$ 혹은 $(0, x)$로 둘 수 있다.

$$ \begin{gather*}
x, y \in \mathbb{R} \\ 
\implies x + y = (x, 0) + (y, 0) = (x + y, 0) = x + y \\
\text{and} \\ 
x \cdot y = (x, 0)(y, 0) = (xy, 0) = xy
\end{gather*}$$

## Remark
위와 같은 정의에 대해 다음이 성립한다.

**(i)** $(0, 1)(y, 0) = (0, y)$

**(ii)** $(0, 1)(0, y) = (-y, 0)$

따라서 $(0, 1)(0, 1) = (-1, 0) = -1$을 얻고, $i = (0, 1)$로 정의하면 $i^2 = -1$이 성립함을 알 수 있다. 

## Definition 2
The ***imaginary number*** is the complex number $i = (0, 1)$. 

따라서 모든 복소수 $z = (x, y)$는 다음과 같은 방법으로도 쓸 수 있다. 

$$z = (x, y) = (x, 0) + (0, y) = (x, 0) + (0, 1)(y, 0) = x + iy$$

## Remark
The ***multiplicative inverse*** $z^{-1}$ of $z \in \mathbb{C}$ is the complex number

$$z^{-1} = \left( \frac{x}{x^2 + y^2}, -\frac{y}{x^2 + y^2} \right)$$