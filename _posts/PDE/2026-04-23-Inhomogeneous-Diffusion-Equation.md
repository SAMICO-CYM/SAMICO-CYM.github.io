---
title: "Inhomogeneous Diffusion Equation"
date: 2026-04-23
categories: [Mathematics, PDE]
tags: []
math: true
---

## Theorem
The solution of the initial value problem

$$ \begin{cases} 
u_t - k u_{xx} = f(x, t) \\
u(x, 0) = \phi(x)
\end{cases} $$

where $f$ and $\phi$ are given functions, is given by

$$
u(x, t) = \frac{1}{\sqrt{4 \pi k t}} \int_{-\infty}^{\infty} e^{-\frac{(x - y)^2}{4 k t}} \phi(y) dy + \int_0^t \int_{-\infty}^{\infty} \frac{1}{\sqrt{4 \pi k (t - s)}} e^{- \frac{(x - y)^2}{4 k (t - s)}} f(y, s) dy ds.
$$

### Proof

