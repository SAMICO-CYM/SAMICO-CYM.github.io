---
title: Taylor Series
date: 2026-05-19
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Theorem 1
Suppose that a function $f$ is analytic throughout a disk $\vert z - z_0 \vert < R_0$ centered at $z_0$ and with radius $R_0$. Then $f$ has the power series expansion 

$$f(z) = \sum_{n=0}^\infty a_n(z-z_0)^n \quad (\vert z - z_0 \vert < R_0),$$

where

$$a_n = \frac{f^{(n)}(z_0)}{n!}, \quad n = 0, 1, 2, \cdots,$$

for each point in the open disk $\vert z - z_0 \vert < R_0$.

This series is called the ***Taylor series*** for $f$ about $z_0$. When $z_0 = 0$, the series is also called the ***Maclaurin series*** for $f$.

### Proof

---
## Remark
(i) Any function which is analytic at a point $z_0$ must have a Taylor series about $z_0$.

(ii) An entire function has a Taylor series everywhere.