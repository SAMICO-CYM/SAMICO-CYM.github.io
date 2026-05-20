---- 
title: Laurent Series
date: 2026-05-20
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Theorem
Suppose that a function $f$ is analytic throughout an annular domain $R_1 < \vert z - z_0 \vert < R_2$, centered at $z_0$, and let $C$ denote any positively oriented simple closed contour around $z_0$ and lying in that domain. Then $f$ has the series representation 

$$f(z) = \sum_{n=0}^\infty a_n(z-z_0)^n + \sum_{n=1}^\infty \frac{b_n}{(z-z_0)^n}$$

at each point $z$ in the domain $R_1 < \vert z - z_0 \vert < R_2$, where

$$\begin{align*}
a_n &= \frac{1}{2\pi i} \int_C \frac{f(z)}{(z-z_0)^{n+1}} \, dz \quad (n= 0, 1, 2, \cdots)\\
b_n &= \frac{1}{2\pi i} \int_C \frac{f(z)}{(z-z_0)^{-n+1}} \, dz \quad (n= 1, 2, \cdots).
\end{align*}$$

This series is called the ***Laurent series*** for $f$ about $z_0$.

### Proof


---
## Remark
**(i)** Note that 

$$b_{-n} = \frac{1}{2\pi i} \int_C \frac{f(z)}{(z-z_0)^{n+1}} \quad (n = -1, -2, \cdots).$$

If we let 

$$c_n = \begin{cases}
a_n & \text{if } n \ge 0 \\
b_{-n} & \text{if }n < 0,
\end{cases}$$

then the Laurent series of $f$ about $z_0$ becomes 

$$f(z) = \sum_{n=-\infty}^\infty c_n(z-z_0)^n$$

where

$$c_n = \frac{1}{2\pi i} \int_C \frac{f(z)}{(z-z_0)^{n+1}}, \forall n \in \mathbb{Z}.$$

**(ii)** If $f$ is analytic throughtout the disk $\vert z - z_0 \vert < R_2$, then we have 

$$\begin{align*}
b_n &= \frac{1}{2\pi i} \int_C \frac{f(z)}{(z-z_0)^{-n+1}} \, dz \\
&= \frac{1}{2\pi i} \int_C f(z) (z-z_0)^{n-1} \, dz \\
&= 0,
\end{align*}$$

for all $n \in \mathbb{N}$, by the Cauchy-Goursat theorem. Thus, the Laurent series of $f$ is reduced to the Taylor series of $f$: 

$$\begin{align*}
f(z) &= \sum_{n=0}^\infty a_n(z-z_0)^n + \sum_{n=1}^\infty \frac{b_n}{(z-z_0)^n} \\
&= \sum_{n=0}^\infty a_n(z-z_0)^n
\end{align*}$$

where

$$a_n = \frac{1}{2\pi i} \int_C \frac{f(z)}{(z-z_0)^{n+1}} \, dz \quad (n= 0, 1, 2, \cdots).$$

**(iii)** Although $f$ is analytic everywhere in the complex plane $\mathbb{C}$ except at $z_0$, the Laurent series is valid at each point $z$ with $0 < \vert z-z_0 \vert < \infty$. 