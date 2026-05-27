--- 
title: Convergence Theorem
date: 2026-05-27
categories: [Mathematics, Fourier Series]
tags: []
math: true
---

## Definition
**(i)** An infinite series $\displaystyle \sum_{n=1}^\infty f_n$ ***converges pointwise*** to $f(x)$ in $(a, b)$ if it converges to $f(x)$ for each $a < x < b.$ That is, for each $x \in (a, b)$, for a given $\varepsilon > 0$, there exists a positive integer $N$ such that 

$$\left \vert \sum_{n=1}^k f_n(x) - f(x) \right \vert < \varepsilon, \forall k \ge N.$$

**(ii)** An infinite series $\displaystyle \sum_{n=1}^\infty f_n$ ***converges uniformly*** to $f(x)$ in $[a, b]$ if for a given $\varepsilon > 0$, there exists a positive integer $N$ such that 

$$\max _{a \le x \le b} \left \vert f(x) - \sum_{n=1}^k f_n(x) \right \vert < \varepsilon, \forall k \ge N.$$

**(iii)** An infinite series $\displaystyle \sum_{n=1}^\infty f_n$ ***converges $L^2$-sense*** to $f(x)$ in $(a, b)$ if for a given $\varepsilon > 0$, there exists a positive integer $N$ such that 

$$\int_a^b \left \vert f(x) - \sum_{n=1}^k f_n(x) \right \vert^2 \, dx < \varepsilon, \forall k \ge N.$$

---
## Remark

$$\text{uniform convergence} \implies \text{pointwise, } L^2\text{-convergence}$$

---
## Theorem
**(i)** The Fourier series $\sum_{n=1}^\infty A_n X_n(x)$ converges uniformly to $f(x)$ on $[a, b]$ if $f \in C^2[a, b]$ and $f$ satisfies the boundary conditions.

**(ii)** The Fourier series converges in $L^2$-sence to $f(x)$ in $(a, b)$ $\iff$ $\displaystyle \int_a^b \vert f(x) \vert^2 \, dx < \infty.$

**(iii)** The Fourier series converges pointwise to $f(x)$ in $(a, b)$ if $f$ and $f'$ is piecewise continuous on $[a, b]$. In this case, 

$$\sum_{n=1}^\infty A_nX_n(x) = \frac{1}{2}\left[ f(x+) + f(x-) \right], \forall x \in (a, b).$$