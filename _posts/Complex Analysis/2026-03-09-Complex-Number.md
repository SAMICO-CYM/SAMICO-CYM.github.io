---
title: Complex Number
date: 2026-03-09
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Introduction
복소해석학은 복소 공간 $\mathbb{C}$에서 함수의 미분, 적분과 같은 해석학적 성질을 다루는 과목이다. 실해석학에서 그랬듯이, 미분과 적분에 앞서 연속성이나 극한과 같은 개념이 먼저 정의되어야 하고, 그러한 개념들은 필연적으로 복소수들 사이의 연산이나 크기과 같은 개념들을 요구한다. 따라서 복소해석학은 '복소수'란 체계가 어떤 구조를 가지고 있는지, 그 안에서 연산은 어떻게 정의되는지와 같은 대수적 성질을 다루는 것으로 시작한다.

## Definition
**(i)** ***Complex number set*** $\mathbb{C}$ is the set $\mathbb{C} = \\{ (x, y) \mid x, y \in \mathbb{R} \\}$ with the two binary operations, addition $+$ and multiplication $\cdot$, defined as follows:

Let $z_1 = (x_1, y_1)$ and $z_2 = (x_2, y_2)$ in $\mathbb{C}$. Then

$$
\begin{align*}
(x_1, y_1) + (x_2, y_2) &= (x_1 + x_2, y_1 + y_2) \\
(x_1, y_1)(x_2, y_2) &= (x_1x_2 - y_1y_2, y_1x_2 + x_1y_2)
\end{align*}
$$


that are to be interpreted as points in the ***complex plane***, with rectangular coordinates $x$ and $y$. 

**(ii)** The ***imaginary number*** is the complex number $i = (0, 1)$. We also write $z = x + iy$ for $z = (x, y)$. 

**(iii)** Let $z = (x, y) \in \mathbb{C}$. The real numbers $x$ and $y$ are called the real parts and the imaginary parts of $z$, denoted by 

$$\text{Re}(z) = x, \quad \text{Im}(z) = y$$

**(iv)** The ***real axis*** is the line in the complex plane consisting of points $(x, 0)$.

**(v)** The ***imaginary axis*** is the line in the complex plane consisting of points $(0, y)$. The numbers $(0, y)$ in the imaginary axis is also called pure imaginary numbers if $y \neq 0$.

**(vi)** Two complex numbers $z_1 = (x_1, y_1)$ and $z_2 = (x_2, y_2)$ are said to be ***equal*** if $x_1 = x_2$ and $y_1 = y_2$.

## Remark
**(i)** Note that the operations defined above become the usual operations of addition and multiplication when restricted to the real numbers:

$$
\begin{align*}
(x_1, 0) + (x_2, 0) &= (x_1 + x_2, 0) \\
(x_1, 0)(x_2, 0) &= (x_1x_2, 0)
\end{align*}
$$

The complex number system is, therefore, a natural extension of the real number system.

**(ii)** Any complex number $z = (x, y)$ can be written $z = (x, 0) + (0, y)$, and it is
easy to see that $(0, 1)(y, 0) = (0, y)$. Hence

$$z = (x, 0) + (0, 1)(y, 0) = (x, 0) + i(y, 0) = (x, y).$$

If we denote the real numbers$ (x,0)$ by $x$, then we can write $z = x + iy$ for $z = (x, y)$. Also, with the convention that $z^2 = zz$, $z^3 = z^2z$, etc., we have

$$i^2 = (0, 1)(0, 1) = (-1, 0) = -1.$$

Because $(x, y) = x + iy$, the operations become

$$
\begin{align*}
(x_1 + iy_1) + (x_2 + iy_2) &= (x_1 + x_2) + i(y_1 + y_2), \\
(x_1 + iy_1)(x_2 + iy_2) &= (x_1x_2 - y_1y_2) + i(y_1x_2 + x_1y_2).
\end{align*}
$$

Observe that the right-hand sides of these equations can be obtained by formally manipulating the terms on the left as if they involved only real numbers and by replacing $i^2$ by $-1$ when it occurs. 

**(iii)** The ***multiplicative inverse*** $z^{-1}$ of $z \in \mathbb{C}$ is the complex number

$$z^{-1} = \left( \frac{x}{x^2 + y^2}, -\frac{y}{x^2 + y^2} \right)$$