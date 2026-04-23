---
title: Inhomogeneous Wave Equation
date: 2026-04-23
categories: [Mathematics, PDE]
tags: []
math: true
---

## Theorem
The solution of the initial value problem

$$ \begin{cases} 
u_{tt} - c^2 u_{xx} = f(x, t) \\
u(x, 0) = \phi(x), \quad \u_t(x, 0) = \psi(x)
\end{cases} $$

where $f, \phi$ and $\psi$ are given functions, is given by

$$
u(x, t) = \frac{1}{\sqrt{4 \pi k t}} \int_{-\infty}^{\infty} e^{-\frac{(x - y)^2}{4 k t}} \phi(y) dy + \int_0^t \int_{-\infty}^{\infty} \frac{1}{\sqrt{4 \pi k (t - s)}} e^{- \frac{(x - y)^2}{4 k (t - s)}} f(y, s) dy ds.
$$

### Proof

