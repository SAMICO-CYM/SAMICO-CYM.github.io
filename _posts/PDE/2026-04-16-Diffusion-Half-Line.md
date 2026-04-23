--- 
title: Diffusion on the Half Line
date: 2026-04-16
categories: [Mathematics, PDE]
tags: []
math: true
---

## Dirichlet Condition
Consider the diffusion equation on the half-line $(0, \infty)$ with the Dirichlet condition 

$$\begin{cases}
v_t - kv_{xx} = 0 \\
v(x, 0) = \phi(x) \\
v(0, t) = 0
\end{cases}$$

for $0 < x < \infty$ and $0 < t < \infty$. 

Let define the ***odd extension*** $\phi _ {\text{odd}}$ of $\phi$ by 

$$\begin{cases}
\phi(x) & \text{for } x > 0 \\
-\phi(-x) & \text{for } x < 0 \\
0 & \text{for } x = 0.
\end{cases}$$

Let $u(x, t)$ be the solution of the initial value problem

$$\begin{cases}
u_t - ku_{xx} = 0 \\
u(x, 0) = \phi _ {\text{odd}}(x)
\end{cases}$$

for $- \infty < x < \infty$ and $0 < t < \infty$. Then $u(x, t)$ is given by 

$$u(x, t) = \int_{-\infty}^{\infty} S(x - y, t) \phi _ {\text{odd}}(y) \, dy.$$

Let $v(x, t)$ be the restriction of $u(x, t)$ for $x \ge 0$. Note that 

1. $v(x, t)$ solves the diffusion equation because $u(x, t)$ solves it.
2. $v(x, 0) = u(x, 0) = \phi _ {\text{odd}}(x) = \phi(x)$.
3. Since $u(-x, t) = -u(x, t)$, we have $v(0, t) = u(0, t) = 0$.

Thus, $v(x, t)$ is the unique solution of the half-line problem. 

Note that 

$$\begin{align*}
u(x, t) &= \int_{-\infty}^{\infty} S(x - y, t) \phi _ {\text{odd}}(y) \, dy \\
&= \int_0^{\infty} S(x-y, t) \phi(y) \, dy - \int_{-\infty}^0 S(x-y, t)\phi(-y) \, dy \\
&= \int_0^{\infty} S(x-y, t) \phi(y) \, dy + \int_{\infty}^0 S(x + y, t) \phi(y) \, dy \\
&= \int_0^{\infty} \left[ S(x-y, t) - S(x+y, t) \right] \phi(y) \, dy.
\end{align*}$$

Hence, for $0 < x < \infty$ and $0 < t < \infty$, we have 

$$v(x, t) = \frac{1}{\sqrt{4 \pi kt}} \int_0^{\infty} \left[ e^{-\frac{(x-y)^2}{4kt}} - e^{-\frac{(x+y)^2}{4kt}} \right] \phi(y) \, dy.$$

---

## Neumann Condition

Consider the diffusion equation on the half-line $(0, \infty)$ with the Neumann condition 

$$\begin{cases}
v_t - kv_{xx} = 0 \\
v(x, 0) = \phi(x) \\
v_x(0, t) = 0
\end{cases}$$

for $0 < x < \infty$ and $0 < t < \infty$. 

Let define the ***even extension*** $\phi _ {\text{even}}$ of $\phi$ by 

$$\begin{cases}
\phi(x) & \text{for } x \ge 0 \\
\phi(-x) & \text{for } x < 0 \\
\end{cases}$$

Let $u(x, t)$ be the solution of the initial value problem

$$\begin{cases}
u_t - ku_{xx} = 0 \\
u(x, 0) = \phi _ {\text{even}}(x)
\end{cases}$$

for $- \infty < x < \infty$ and $0 < t < \infty$. Then $u(x, t)$ is given by 

$$u(x, t) = \int_{-\infty}^{\infty} S(x - y, t) \phi _ {\text{even}}(y) \, dy.$$

Let $v(x, t)$ be the restriction of $u(x, t)$ for $x \ge 0$. Note that 

1. $v(x, t)$ solves the diffusion equation because $u(x, t)$ solves it.
2. $v(x, 0) = u(x, 0) = \phi _ {\text{even}}(x) = \phi(x)$.
3. Since $u(-x, t) = u(x, t)$, we have $-u_x(-x, t) = u_x(x, t)$. In particular, $u_x(0, t) = -u_x(0, t)$, so that $u_x(0, t) = 0$. Thus, 

$$\begin{align*} v_x(0, t) &= \lim_{x \to 0^+} u_x(x, t) \\ 
&= \lim_{x \to 0^+} -u_x(-x, t) \\ 
&= -u_x(0, t) \\ 
&= 0. \end{align*}$$  

Thus, $v(x, t)$ is the unique solution of the half-line problem. 

Note that 

$$\begin{align*}
u(x, t) &= \int_{-\infty}^{\infty} S(x - y, t) \phi _ {\text{even}}(y) \, dy \\
&= \int_0^{\infty} S(x-y, t) \phi(y) \, dy + \int_{-\infty}^0 S(x-y, t)\phi(-y) \, dy \\
&= \int_0^{\infty} S(x-y, t) \phi(y) \, dy - \int_{\infty}^0 S(x + y, t) \phi(y) \, dy \\
&= \int_0^{\infty} \left[ S(x-y, t) + S(x+y, t) \right] \phi(y) \, dy.
\end{align*}$$

Hence, for $0 < x < \infty$ and $0 < t < \infty$, we have 

$$v(x, t) = \frac{1}{\sqrt{4 \pi kt}} \int_0^{\infty} \left[ e^{-\frac{(x-y)^2}{4kt}} + e^{-\frac{(x+y)^2}{4kt}} \right] \phi(y) \, dy.$$ 