--- 
title: Maximum Modulus Principle
date: 2026-05-16
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Lemma
Suppose that $\vert f(z) \vert \le \vert f(z_0) \vert$ at each point $z$ in some neighborhood $\vert z - z_0 \vert < \varepsilon$ in which $f$ is analytic. Then $f(z)$ has the constant value $f(z_0)$ throughout that neighborhood.

### Proof

---
## Maximum Modulus Principle
If a function $f$ is analytic and not constant in a given domain $D$, then $\vert f(z) \vert$ has no maximum value in $D$. That is, there is no point $z_0 \in D$ such that $\vert f(z) \vert \le \vert f(z_0) \vert, \forall z \in D$. 

### Proof

---
## Corollary
Suppose that a function $f$ is continuous on a closed bounded region $R$ and that it is analytic and not constant in the interior of $R$. Then the maximum value of $\vert f(z) \vert$ in $R$, which is always reached, occurs somewhere on the boundary of $R$ and never in the interior.

즉 최대값은 항상 경계에서 일어날 수 밖에 없음을 보장해준다. 이는 Lagrange multiplier의 직관과도 잘 일치함을 알 수 있다.

### Proof