--- 
title: Contour Integral
date: 2026-04-29
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Definition 1
Let $f: \mathbb{C} \to \mathbb{C}$ be a function and let $C$ be a contour represented by the equation $z = z(t), a \le t \le b$. Suppose that $f(z)$ is piecewise continuous on $[a ,b]$. We define the ***contour integral*** of $f$ along $C$ as 

$$\int_C f(z) \, dz := \int_a^b f[z(t)] z'(t) \, dt$$

---

## Remark
**(i)** Since $C$ is a contour, $z'(t)$ is piecewise continuous on $[a, b]$, so that the integral is well-defined.

**(ii)** The value of a contour integral is invariant under a change in the representation of its contour. 

---

## Theorem
**(i)** $\displaystyle \int_{-C} f(z) \, dz = -\int_C f(z) \, dz$. 

**(ii)** If $C = C_1 + C_2$, then $\displaystyle \int_C f(z) \, dz = \int_{C_1} f(z) \, dz + \int_{C_2} f(z) \, dz$.

### Proof
**(i)** Let $C$ be a contour represented by the equation $z = z(t), a \le t \le b$. Then the contour $-C$ is represented by $z = z(-t), a \le t \le b$. Then we have

$$\begin{align*}
\int_{-C} f(z) \, dz &= \int_a^b f[z(-t)] z'(-t) \, dt \\
&= -\int_{-a}^{-b} f(z(\tau)) z'(\tau) \, d\tau \\
&= -\int_C f(z) \, dz. 
\end{align*}$$

**(ii)** Let $C_1$ be represented by $z = z(t), a \le t \le c$ and $C_2$ be represented by $z = z(t), c \le t \le b$. Since $C = C_1 + C_2$, $C$ is represented by $z = z(t), a \le t \le b$. Then we have

$$\begin{align*}
\int_C f(z) \, dz &= \int_a^b f[z(t)] z'(t) \, dt \\
&= \int_a^c f[z(t)] z'(t) \, dt + \int_c^b f[z(t)] z'(t) \, dt \\
&= \int_{C_1} f(z) \, dz + \int_{C_2} f(z) \, dz. \blacksquare
\end{align*}$$