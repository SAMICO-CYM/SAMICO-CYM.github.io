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
u(x, t) = \frac{1}{2} [\phi(x-ct) + \phi(x+ct)] + \frac{1}{2c} \int_{x-ct}^{x+ct} \psi(s) \, ds + \frac{1}{2c} \iint_{\Delta} f,
$$ 

where $\Delta$ is the characteristic triangle, that is,

$$
\frac{1}{2c} \iint_{\Delta} f = \frac{1}{2c} \int_0^t \int_{x - c(t - s)}^{x + c(t - s)} f(y, s) \, dy ds
$$

### Proof
We already know that when $f \equiv 0$, $u(x, t) = \frac{1}{2} [\phi(x-ct) + \phi(x+ct)] + \frac{1}{2c} \int_{x-ct}^{x+ct} \psi(s) \, ds$ is a solution to the wave equation $u_{tt} - c^2 u_{xx} = 0$. Since the equation is linear, we only need to consider the case where $\phi(x) = 0$ and $\psi(x) = 0$, that is, 

$$u(x, t) = \frac{1}{2c} \iint_{\Delta} f = \frac{1}{2c} \int_0^t \int_{x - c(t - s)}^{x + c(t - s)} f(y, s) \, dy ds$$

is a solution of the given initial value problem.

$(\because)$ Substituting 

$$\begin{cases}
\xi = x + ct \\
\eta = x - ct,
\end{cases}$$

we have 

$$\begin{align*}
u_{tt} - c^2u_{xx} = -4c^2u_{\xi \eta} = f \left( \frac{\xi + \eta}{2}, \frac{\xi - \eta}{2c} \right).
\end{align*}$$

Integrating this with respect to $\eta$ and then with respect to $\xi$, we get 

$$u(\xi, \eta) = -\frac{1}{4c^2} \int^{\xi} \int^{\eta} f \, d\eta \, d \xi$$

where the lower limits of integration here are arbitrary. (They correspond to constants of integration.) 

Fix $P_0 = (x_0, t_0)$ and let $\xi_0 = x_0 + ct_0$ and $\eta_0 = x_0 - ct_0$. 