--- 
title: Maximum Modulus Principle
date: 2026-05-16
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Lemma
Let $z_0 \in \mathbb{C}$ be a given point. Suppose that $\vert f(z) \vert \le \vert f(z_0) \vert$ at each point $z$ in some neighborhood $\vert z - z_0 \vert < \varepsilon$ in which $f$ is analytic. Then $f(z)$ has the constant value $f(z_0)$ throughout that neighborhood.

### Proof
Let $0 < \rho < \varepsilon$. If $C_\rho$ denotes the positively oriented circle $\vert z- z_0 \vert = \rho$, centered at $z_0$ with radius $\rho$, then the Gauss's mean value theorem tells us that 

$$f(z_0) = \frac{1}{2 \pi} \int_0^{2\pi} f(z_0 + \rho e^{i\theta}) \, d\theta.$$

Then we have 

$$\begin{align*}
\vert f(z_0) \vert &= \frac{1}{2 \pi} \left \vert \int_0^{2\pi} f(z_0 + \rho e^{i\theta}) \, d\theta \right \vert \\
& \le \frac{1}{2 \pi} \int_0^{2\pi} \vert f(z_0 + \rho e^{i\theta}) \vert \, d\theta.
\end{align*}$$

Since $\vert f(z_0 + \rho e^{i\theta}) \vert \le \vert f(z_0) \vert$ for all $\theta$ by assumption, we see that

$$\begin{align*}
\vert f(z_0) \vert & \le \frac{1}{2 \pi}\int_0^{2\pi} \vert f(z_0 + \rho e^{i\theta}) \vert \, d\theta \\
& \le \frac{1}{2 \pi}\int_0^{2\pi} \vert f(z_0) \vert \, d\theta \\
&= \frac{1}{2 \pi}2\pi \vert f(z_0) \vert \\
&= \vert f(z_0) \vert.
\end{align*}$$

Thus, we have

$$\begin{align*}
\vert f(z_0) \vert = \frac{1}{2 \pi}\int_0^{2\pi} \vert f(z_0 + \rho e^{i\theta}) \vert \, d\theta \\
\implies \int_0^{2\pi} \left[ \vert f(z_0) \vert - \vert f(z_0 + \rho e^{i\theta}) \vert \right] \, d\theta = 0
\end{align*}$$

The integrand in the last integral is continuous in the variable $\theta$, and is nonnegative for all $\theta$ by assumption. Since the value of integral is zero, we must have that the integrand is equal to zero. That is, 

$$\vert f(z_0) \vert = \vert f(z_0 + \rho e^{i\theta}) \vert, \forall \theta \in [0, 2\pi],$$

which means that $\vert f(z) \vert = \vert f(z_0) \vert$ for all $z$ on the circle $C_\rho$. 

Since we have chosen $\rho$ arbitrarily, it follows that $\vert f(z) \vert = \vert f(z_0) \vert$ in the neighborhood $\vert z - z_0 \vert < \varepsilon$. By Theorem 2, $f(z)$ is constant throughout that neighborhood, which means that $f(z) = f(z_0)$ for each point $z$ in the neighborhood. $\blacksquare$

---
## Maximum Modulus Principle
If a function $f$ is analytic and not constant in a given domain $D$, then $\vert f(z) \vert$ has no maximum value in $D$. That is, there is no point $z_0 \in D$ such that $\vert f(z) \vert \le \vert f(z_0) \vert, \forall z \in D$. 

### Proof

---
## Corollary
Suppose that a function $f$ is continuous on a closed bounded region $R$ and that it is analytic and not constant in the interior of $R$. Then the maximum value of $\vert f(z) \vert$ in $R$, which is always reached, occurs somewhere on the boundary of $R$ and never in the interior.

즉 최대값은 항상 경계에서 일어날 수 밖에 없음을 보장해준다. 이는 Lagrange multiplier의 직관과도 잘 일치함을 알 수 있다.

### Proof