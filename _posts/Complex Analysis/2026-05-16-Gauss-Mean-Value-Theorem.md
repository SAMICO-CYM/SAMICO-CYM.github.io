--- 
title: Gauss's Mean Value Theorem
date: 2026-05-16
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Gauss's Mean Value Theorem
Suppose that a function $f$ is analytic inside and on the closed circle $C\rho: \vert z - z_0 \vert = \rho$, centered at $z_0$ and with radius $\rho$. Then 

$$f(z_0) = \frac{1}{2 \pi} \int_0^{2\pi} f(z_0 + \rho e^{i\theta}) \, d\theta.$$

### Proof
By Cauchy integral formula, 

$$f(z_0) = \frac{1}{2 \pi i} \int _ {C_\rho} \frac{f(z)}{z-z_0} \, dz.$$

Since $C_\rho$ can be parametrized by $z = z_0 + \rho e^{i\theta} (0 \le \theta \le 2\pi)$, we have 

$$\begin{align*}
f(z_0) &= \frac{1}{2 \pi i} \int_0^{2\pi} \frac{f(z_0 + \rho e ^{i \theta})}{(z_0 + \rho e^{i \theta}) - z_0} i \rho e^{i \theta} \, d \theta \\
&= \frac{1}{2 \pi} \int_0^{2\pi} f(z_0 + \rho e ^{i \theta}) \, d \theta. \quad \blacksquare
\end{align*}$$