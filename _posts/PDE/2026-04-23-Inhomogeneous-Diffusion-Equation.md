---
title: "Inhomogeneous Diffusion Equation"
date: 2026-04-23
categories: [Mathematics, PDE]
tags: []
math: true
---

## Theorem 1
The solution of the initial value problem

$$ \begin{cases} 
u_t - k u_{xx} = f(x, t) \\
u(x, 0) = \phi(x)
\end{cases} $$

for $-\infty < x < \infty, t >0$, where $f$ and $\phi$ are given functions, is given by

$$
\begin{align*}
u(x, t) &= \int_{-\infty}^{\infty} S(x- y, t) \phi(y) \, dy + \int_0^t \int_{-\infty}^{\infty} S(x- y, t - s) f(y, s) \, dy ds
\\ &= \frac{1}{\sqrt{4 \pi k t}} \int_{-\infty}^{\infty} e^{-\frac{(x - y)^2}{4 k t}} \phi(y) \, dy + \int_0^t \int_{-\infty}^{\infty} \frac{1}{\sqrt{4 \pi k (t - s)}} e^{- \frac{(x - y)^2}{4 k (t - s)}} f(y, s) \, dy ds.
\end{align*}
$$

### Proof
We already know that when $f \equiv 0$, $u(x, t) = \int_{-\infty}^{\infty} S(x-y, t) \phi(y) \, dy$ is a solution to the equation $u_t - ku_{xx} = 0$. Since the equation is linear, we only need to consider the case where $\phi(x) = 0$, that is, 

$$u(x,t) = \int_0^t \int_{-\infty}^{\infty} S(x- y, t - s) f(y, s) \, dy ds$$

is a solution of the given initial value problem.

$(\because)$ Let 

$$g(x, t-s) := \int_{-\infty}^{\infty} S(x-y, t-s) f(y, s) \, dy.$$

Then 

$$\begin{align*}
u(x, t) &= \int_0^t \int_{-\infty}^{\infty} S(x- y, t - s) f(y, s) \, dy ds \\
&= \int_0^t g(x, t-s) \, ds.
\end{align*}$$

Note that 

$$\begin{align*}
\frac{\partial u}{\partial t} &= \frac{\partial}{\partial t} \int_0^t g(x, t-s) \, ds \\
&= \int_0^t \frac{\partial g}{\partial t}(x, t-s) \, ds + \lim_{s \nearrow t} g(x, t-s) \\
&= \int_0^t \int_{-\infty}^{\infty} \frac{\partial S}{\partial t}(x- y, t - s) f(y, s) \, dy ds + \lim_{s \nearrow t} \int_{-\infty}^{\infty} S(x- y, t - s) f(y, s) \, dy \\
&= \int_0^t \int_{-\infty}^{\infty} \frac{\partial S}{\partial t}(x- y, t - s) f(y, s) \, dy ds + f(x, t).
\end{align*}$$



Since $S(x-y, t-s)$ satisfies the diffusion equation $S_t = kS_{xx}$, we have 

$$\begin{align*}
\frac{\partial u}{\partial t} &= \int_0^t \int_{-\infty}^{\infty} \frac{\partial S}{\partial t}(x- y, t - s) f(y, s) \, dy ds + f(x, t) \\
&= \int_0^t \int_{-\infty}^{\infty} k\frac{\partial^2 S}{\partial x^2}(x- y, t - s) f(y, s) \, dy ds + f(x, t) \\
&= k \frac{\partial^2}{\partial x^2} \left[ \int_0^t \int_{-\infty}^{\infty} S(x- y, t - s) f(y, s) \, dy ds \right] + f(x, t) \\
&= ku_{xx} + f(x, t),
\end{align*}$$

which means that $u$ satisfies the inhomogeneous diffusion equation. Clearly, $u(x, 0) = 0$. Thus, $u$ is the solution of the given initial value problem. $\blacksquare$

--- 

## Theorem 2 (Half-Line Problem)

The solution of the half-line problem

$$ \begin{cases} 
u_t - k u_{xx} = f(x, t) \\
u(x, 0) = \phi(x) \\
u(0, t) = h(t)
\end{cases} $$

for $0 < x < \infty, t > 0$, where $f, \phi$ and $h$ are given functions, is given by

$$
\begin{align*}
u(x, t) &= \int_{-\infty}^{\infty} S(x- y, t) \phi(y) \, dy + \int_0^t \int_{-\infty}^{\infty} S(x- y, t - s) f(y, s) \, dy ds
\\ &= \frac{1}{\sqrt{4 \pi k t}} \int_{-\infty}^{\infty} e^{-\frac{(x - y)^2}{4 k t}} \phi(y) \, dy + \int_0^t \int_{-\infty}^{\infty} \frac{1}{\sqrt{4 \pi k (t - s)}} e^{- \frac{(x - y)^2}{4 k (t - s)}} f(y, s) \, dy ds.
\end{align*}
$$

### Proof
Let $u(x,t)$ be a solution of the given initial value problem. Let $U(x, t) := u(x, t) - h(t)$ for $0 < x < \infty$ and $t > 0$. Then $U(x, t)$ satisfies 

$$\begin{cases}
U_t - k U_{xx} = F(x, t) \\
U(x, 0) = \psi(x) \\
U(0, t) = 0 
\end{cases}$$

for $0 < x < \infty, t > 0$, where $F(x, t) := f(x, t) - h'(t)$ and $\psi(x) := \phi(x) - h(0)$. We consider the whole-line problem 

$$\begin{cases}
V_t - k V_{xx} = F _ {\text{odd}}(x, t) \\
V(x, 0) = \psi _ {\text{odd}}(x)
\end{cases}$$ 

where $F _ {\text{odd}}$ and $\psi _ {\text{odd}}$ are the odd expansions of $F$ and $\psi$ respectively for the whole-line of $x$. Then the solution of the whole-line problem is given by 

$$\begin{align*}
V(x, t) &= \int_{-\infty}^\infty S(x-y, t) \psi_\text{odd}(y) \, dy + \int_0^t \int_{-\infty}^\infty S(x-y, t-s) F(y, s) \, dy ds \\
&= \int_{0}^\infty [S(x-y, t) - S(x+y, t)] \psi(y) \, dy + \int_0^t \int_{-\infty}^\infty S(x-y, t-s) F(y, s) \, dy ds.
\end{align*}$$

We take $U(x, t)$ to be the restriction of $V(x, t)$ for $x \ge 0$. Note that 

1. $U(x,t)$ solves the inhomogeneous diffusion equation $U_t - k U_{xx} = F(x, t)$ because $V(x, t)$ solves it.
2. $U(x, 0) = V(x, 0) = \psi _ {\text{odd}}(x) = \psi(x) = \phi(x) - h(0)$.
3. Since $V(-x, t) = -V(x, t)$, we have $U(0, t) = V(0, t) = 0$.

Thus, $U(x, t)$ is the unique solution of the half-line problem. 