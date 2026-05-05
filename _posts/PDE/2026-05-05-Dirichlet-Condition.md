--- 
title: Dirichlet Condition
date: 2026-05-05
categories: [Mathematics, PDE]
tags: []
math: true
---

## Wave equation
We consider the problem

$$\begin{cases}
u_{tt} = c^2u_{xx} \\
u(0, t) = 0 = u(l, t) \\
u(x, 0) = \phi(x), \quad u_t(x, 0) = \psi(x)
\end{cases}$$

for $0 < x < l$ and $t > 0$. 

Suppose that a solution is given by the seperated form $u(x, t) = X(x)T(t)$. Plugging this form into the wave equation, we get 

$$XT'' = c^2X''T.$$

By dividing $-c^2XT$, we have 

$$-\frac{T''}{c^2T} = - \frac{X''}{X} = \lambda.$$

This defines a quantity $\lambda$, which must be a constant. ($\lambda$ does not depend on both $x$ and $t$.) 