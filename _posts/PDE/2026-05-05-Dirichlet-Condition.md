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

By dividing $-c^2XT$ (we assume $X(x), T(t) \neq 0$), we have 

$$-\frac{T''}{c^2T} = - \frac{X''}{X} = \lambda.$$

This defines a quantity $\lambda$, which must be a constant. ($\lambda$ does not depend on both $x$ and $t$.) 

1. $\lambda > 0$

We obtain $X''(x) = 0$, so $X(x) = C + Dx$ for some constants $C, D$. From the Dirichlet condition $u(0, t) = 0 = u(l, t)$, we have $X(0) = 0 = X(l)$, which implies that $C = 0 = D$. Thus, $X(x) = 0$, so that $u(x, t) = 0$.  It could not satisfy the initial condition. 

2. $\lambda < 0$

Let $\lambda = - \gamma^2$. Then we have $X'' = \gamma^2 X$, which has a solution $X(x) = C\cosh(\gamma x) + D \sinh(-\gamma x)$ for some constants $C, D$. Since $X(0) = 0 = X(l)$, we can obtain $C = 0 = D$. Thus, $X(x) = 0$, so that $u(x, t) = 0$. It could not satisfy the initial condition. 

3. $\lambda = 0$

We write $\lambda = \beta^2 (\beta > 0)$. Then we have $X'' + \beta^2 X = 0$ and $T'' + c^2\beta^2 T = 0$. Then we get $X(x) = C \cos \beta x + D \sin \beta x$ and $T(t) A \cos \beta c t + B \sin \beta c t$ for some constants $A, B, C, D$. Since $X(0) = 0 = X(l)$, we get $C = 0$ and $D\sin \beta l = 0$. Since we are not interested in the obvious solution $C = 0 = D$, we must have $\beta l = n \pi$ where $n \in \mathbb{N}$. Then we have

$$\lambda_n = \left( \frac{n \pi}{l} \right)^2, \quad X_n(x) = \sin \frac{n \pi x}{l}, \quad \text{and} \quad T_n(t) = A_n \cos \frac{n \pi ct}{l} + B_n \sin \frac{n \pi ct}{l}$$

for $n = 1, 2, \cdots$. 

Since

$$u_n(x, t) = X_n(x) T_n(t) = \left( A_n \cos \frac{n \pi ct}{l} + B_n \sin \frac{n \pi ct}{l} \right)\sin \frac{n \pi x}{l}$$

is a solution for each $n = 1, 2, \cdots$, their infinite sum 

$$u(x, t) = \sum_{n=1}^\infty \left( A_n \cos \frac{n \pi ct}{l} + B_n \sin \frac{n \pi ct}{l} \right)\sin \frac{n \pi x}{l}$$

is also a solution. 

By the initial conditions $u(x, 0) = \phi(x)$ and $u_t(x, 0) = \psi(x)$, we have 

$$\begin{align*}
\phi(x) &= u(x, 0) = \sum_{n=1}^\infty A_n \sin \frac{n \pi x}{l} \\
\psi(x) &= u_t(x, 0) = \sum_{n=1}^\infty \frac{n \pi c}{l} B_n \sin \frac{n \pi x}{l}.
\end{align*}$$

