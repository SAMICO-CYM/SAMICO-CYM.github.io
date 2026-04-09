---
title: Solution To Diffusion Equation
date: 2026-04-09
categories: [Mathematics, PDE]
tags: []
math: true
---

## Theorem 1
The solution to the diffusion equation with the initial condition

$$ \begin{cases} 
u_t = k u_{xx} \\
u(x, 0) = \phi(x)
\end{cases} $$

is given by

$$
u(x, t) = \frac{1}{\sqrt{4 \pi k t}} \int_{-\infty}^{\infty} e^{-\frac{(x - y)^2}{4 k t}} \phi(y) dy.
$$

### Proof