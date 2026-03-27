---
title: Wave Equation
date: 2026-03-26
categories: [Mathematics, PDE]
tags: []
math: true
---

## Definition
The ***wave equation*** is a second order linear partial differential equation given by

$$
u_{tt} = c^2 u_{xx} \quad \text{for } -\infty < x < \infty
$$

where $c$ is a constant.

---

## Theorem 1
The general solution of the wave equation $u_{tt} = c^2 u_{xx}$ is given by

$$
u(x, t) = f(x + ct) + g(x - ct)
$$

where $f$ and $g$ are arbitrary twice differentiable functions.

### Proof 1
Note that 

$$\partial_{tt} - c^2 \partial_{xx} = (\partial_t - c \partial_x)(\partial_t + c \partial_x)$$

Let $v = u_t + c u_x$. Then the wave equation can be written as

$$
v_t - cv_x = 0,
$$

[which solution is given by $v(x, t) = h(x + ct)$ for some arbitrary function $h$.](<{% post_url PDE/2026-03-10-1st-Order-Linear-PDE-Constant-Coefficients %}#theorem-1>)

Thus, we have

$$
v = u_t + cu_x = h(x + ct)
$$

We can easily verify that $u(x, t) = f(x + ct)$ where $f$ is a function such that $f'(s) = \frac{h(s)}{2c}$. 

$\Big[$ $(\because)$ Since $u_x = f'(x+ct)$ and $u_t = c f'(x+ct)$, we have

$$\begin{align*}
u_t + c u_x &= c f'(x+ct) + c f'(x+ct) \\
&= 2c f'(x+ct) \\
&= h(x+ct) \Big]
\end{align*}$$

Since the homogeneous equation $u_t + cu_x = 0$ has the solution $u(x, t) = g(x - ct)$ and the wave equation is linear, we have the general solution

$$u(x, t) = f(x + ct) + g(x - ct). \blacksquare$$

### Proof 2
We can derive the general solution by the method of change of variables. Let 

$$\begin{align*}
\xi &= x + ct \\
\eta &= x - ct
\end{align*}$$

Then we have

$$\begin{align*}
u_x &= u_\xi + u_\eta \\
u_t &= c(u_\xi - u_\eta)
\end{align*}$$

so that

$$\begin{align*}
u_{xx} &= u_{\xi \xi} + 2 u_{\xi \eta} + u_{\eta \eta} \\
u_{tt} &= c^2 (u_{\xi \xi} - 2 u_{\xi \eta} + u_{\eta \eta}).
\end{align*}$$

Thus the wave equation can be written as

$$\begin{gather*}
u_{tt} - c^2 u_{xx} = -4c^2 u_{\xi \eta} = 0 \\
\implies u_{\xi \eta} = 0.
\end{gather*}$$

The solution to the above equation is $u(x, y) = u(\xi, \eta) = f(\xi) + g(\eta) = f(x+ct) + g(x-ct)$ for some arbitrary twice differentiable functions $f$ and $g$. $\blacksquare$

---

## Theorem 2
The initial value problem for the wave equation

$$\begin{cases}
u_{tt} = c^2 u_{xx} \\
u(x, 0) = \phi(x) \\
u_t(x, 0) = \psi(x)
\end{cases}$$

for $-\infty < x < \infty, t > 0$, where $\phi$ and $\psi$ are given functions, has the solution

$$
u(x, t) = \frac{1}{2} [\phi(x + ct) + \phi(x - ct)] + \frac{1}{2c} \int_{x - ct}^{x + ct} \psi(s) ds$$

### Proof
By Theorem 1, the general solution to the wave equation is given by

$$
u(x, t) = f(x + ct) + g(x - ct)$$

Then

$$u_t = cf'(x + ct) - cg'(x - ct)$$

Taking $t = 0$, we have

$$\begin{align*}
&\begin{cases}
f(x) + g(x) = \phi(x) \\
cf'(x) - cg'(x) = \psi(x)
\end{cases}
\\
\implies &\begin{cases}
f'(x) + g'(x) = \phi'(x) \\
f'(x) - g'(x) = \frac{\psi(x)}{c}
\end{cases}
\\
\implies &\begin{cases}
f'(x) = \frac{1}{2} \left( \phi'(x) + \frac{\psi(x)}{c} \right) \\
g'(x) = \frac{1}{2} \left( \phi'(x) - \frac{\psi(x)}{c} \right)
\end{cases}
\\
\implies &\begin{cases}
f(x) = \frac{1}{2} \phi(x) + \frac{1}{2c} \int^x \psi(s) ds  + C_1 \\
g(x) = \frac{1}{2} \phi(x) - \frac{1}{2c} \int^x \psi(s) ds  + C_2
\end{cases}
\end{align*}$$

Since $\phi(x) = f(x) + g(x) = \phi(x) + C_1 + C_2$, we have $C_1 + C_2 = 0$.

Thus the particular solution is

$$
\begin{align*}
u(x, t) &= f(x + ct) + g(x - ct) \\
&= \frac{1}{2} [\phi(x + ct) + \phi(x - ct)] + \frac{1}{2c} \int_{x - ct}^{x + ct} \psi(s) ds. \blacksquare
\end{align*}
$$