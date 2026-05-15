--- 
title: Morera Theorem
date: 2026-05-16
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Morera's Theorem
Let $f$ be continuous on a domain $D$. If 

$$\int_C f(z) \, dz = 0$$

for every closed contour $C$ in $D$, then $f$ is analytic throughout $D$.

[코시 정리](<{% post_url Complex Analysis/2026-05-08-Cauchy-Theorem %}#cauchy's-theorem>)가 $f$가 analytic일 때 모든 closed contour에 대해서 적분이 $0$인 것을 보인 것과 반대로, 모레라 정리는 적분이 $0$일 때 $f$가 analytic임을 보인다. 

### Proof

---
## Cauchy's Inequality
Suppose that a function $f$ is analytic inside and on a positively oriented circle $C_R$, centered at $z_0$ and with radius $R$. If we define $\displaystyle M_R := \max _ {z \in C_R} \vert f(z) \vert$, then 

$$\left\vert f^{(n)}(z_0) \right\vert \le \frac{n! M_R}{R^n}, \forall n \in \mathbb{N}.$$

### Proof
