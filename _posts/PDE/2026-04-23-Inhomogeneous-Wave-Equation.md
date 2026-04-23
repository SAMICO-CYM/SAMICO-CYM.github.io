---
title: Inhomogeneous Wave Equation
date: 2026-04-23
categories: [Mathematics, PDE]
tags: []
math: true
---

## Theorem 1
The solution of the initial value problem

$$ \begin{cases} 
u_{tt} - c^2 u_{xx} = f(x, t) \\
u(x, 0) = \phi(x), \quad u_t(x, 0) = \psi(x)
\end{cases} $$

for $-\infty < x < \infty, t >0$, where $f, \phi$ and $\psi$ are given functions, is given by

$$
u(x, t) = \frac{1}{2} [\phi(x-ct) + \phi(x+ct)] + \frac{1}{2c} \int_{x-ct}^{x+ct} \psi(s) \, ds + \frac{1}{2c} \iint_{\triangle} f,
$$ 

where $\triangle$ is the charateristic triangle, that is,

$$\frac{1}{2c} \iint_{\triangle} f = \frac{1}{2c} \int_0^t \int_{x - c(t - s)}^{x + c(t - s)} f(y, s) \, dy ds$$

### Proof

