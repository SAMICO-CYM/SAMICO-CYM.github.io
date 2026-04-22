--- 
title: Wave on the Half Line
date: 2026-04-22
categories: [Mathematics, PDE]
tags: []
math: true
---

## Dirichlet Condition

Consider the wave equation on the half-line $(0, \infty)$ with the Dirichlet condition 

$$\begin{cases}
v_{tt} - c^2v_{xx} = 0 \\
v(x, 0) = \phi(x), \quad v_t(x,0) = \psi(x) \\
v(0, t) = 0
\end{cases}$$

for $0 < x < \infty$ and $0 < t < \infty$. 

Let define the ***odd extensions*** $\phi _ {\text{odd}}$ and $\psi _ {\text{odd}}$ of $\phi$ and $\psi$ by 

$$\phi _ {\text{odd}}(x) = \begin{cases}
\phi(x) & \text{for } x > 0 \\
-\phi(-x) & \text{for } x < 0 \\
0 & \text{for } x = 0.
\end{cases} \quad \text{and} \quad \psi _ {\text{odd}}(x) = \begin{cases}
\psi(x) & \text{for } x > 0 \\
-\psi(-x) & \text{for } x < 0 \\
0 & \text{for } x = 0.
\end{cases}$$

Let $u(x, t)$ be the solution of the initial value problem

$$\begin{cases}
u_{tt} - c^2u_{xx} = 0 \\
u(x, 0) = \phi _ {\text{odd}}(x), \quad u_t(x, 0) = \psi _ {\text{odd}}(x) 
\end{cases}$$

for $- \infty < x < \infty$ and $0 < t < \infty$. Then $u(x, t)$ is given by 

$$u(x, t) = \frac{1}{2}[\phi _ {\text{odd}}(x+ct) + \phi _ {\text{odd}}(x-ct)] + \frac{1}{2c} \int_{x-ct}^{x+ct} \psi _ {\text{odd}}(s) \, ds.$$

Let $v(x, t)$ be the restriction of $u(x, t)$ for $x \ge 0$. Note that 

1. $v(x, t)$ solves the wave equation because $u(x, t)$ solves it.
2. $v(x, 0) = u(x, 0) = \phi _ {\text{odd}}(x) = \phi(x)$ and $v_t(x, 0) = u_t(x, 0) = \psi _ {\text{odd}}(x) = \psi(x)$.
3. Since $u(-x, t) = -u(x, t)$, we have $v(0, t) = u(0, t) = 0$.

Thus, $v(x, t)$ is a solution of the half-line problem. 

Note that for $x > ct$, we have 

$$\begin{cases}
\phi _ {\text{odd}}(x+ct) = \phi(x+ct) \\
\phi _ {\text{odd}}(x - ct) = \phi(x-ct) \\
\psi _ {\text{odd}}(s) = \psi(s) \quad (x-ct \le s \le x+ct)
\end{cases}$$

Thus, in this case, we have
$$\begin{align*}
v(x, t) &= \frac{1}{2} [\phi(x + ct) + \phi(x - ct)] + \frac{1}{2c} \int_{x - ct}^{x + ct} \psi(s) ds.
\end{align*}$$

Note that for $0 < x < ct$, we have 

$$\begin{cases}
\phi _ {\text{odd}}(x+ct) = \phi(x+ct) \\
\phi _ {\text{odd}}(x - ct) = -\phi(ct-x) \\
\psi _ {\text{odd}}(s) = \begin{cases} \psi(s) & \text{for } 0 < s \le x + ct \\ 
-\psi(-s) & \text{for } x - ct \le s < 0. \end{cases}
\end{cases}$$

Thus, in this case, we have
$$\begin{align*}
v(x, t) &= \frac{1}{2} [\phi(ct + x) - \phi(ct - x)] + \frac{1}{2c} \left[ \int_{0}^{x + ct} \psi(s) \, ds - \int_{x-ct}^0 \psi(-s) \, ds \right] \\
&= \frac{1}{2} [\phi(ct + x) - \phi(ct - x)] + \frac{1}{2c} \left[ \int_{0}^{ct + x} \psi(s) \, ds + \int_{ct - x}^0 \psi(s) \, ds \right] \\ 
&= \frac{1}{2} [\phi(ct + x) - \phi(ct - x)] + \frac{1}{2c} \int_{ct - x}^{ct + x} \psi(s) \, ds.
\end{align*}$$

---

## Neumann Condition
Consider the wave equation on the half-line $(0, \infty)$ with the Neumann condition 

$$\begin{cases}
v_{tt} - c^2v_{xx} = 0 \\
v(x, 0) = \phi(x), \quad v_t(x,0) = \psi(x) \\
v_x(0, t) = 0
\end{cases}$$

for $0 < x < \infty$ and $0 < t < \infty$. 

Let define the ***even extensions*** $\phi _ {\text{even}}$ and $\psi _ {\text{even}}$ of $\phi$ and $\psi$ by 

$$\phi _ {\text{even}}(x) = \begin{cases}
\phi(x) & \text{for } x \ge 0 \\
\phi(-x) & \text{for } x < 0 \\
\end{cases} \quad \text{and} \quad \psi _ {\text{even}}(x) = \begin{cases}
\psi(x) & \text{for } x \ge 0 \\
\psi(-x) & \text{for } x < 0 \\
\end{cases}$$

Let $u(x, t)$ be the solution of the initial value problem

$$\begin{cases}
u_{tt} - c^2u_{xx} = 0 \\
u(x, 0) = \phi _ {\text{even}}(x), \quad u_t(x, 0) = \psi _ {\text{even}}(x) 
\end{cases}$$

for $- \infty < x < \infty$ and $0 < t < \infty$. Then $u(x, t)$ is given by 

$$u(x, t) = \frac{1}{2}[\phi _ {\text{even}}(x+ct) + \phi _ {\text{even}}(x-ct)] + \frac{1}{2c} \int_{x-ct}^{x+ct} \psi _ {\text{even}}(s) \, ds.$$

Let $v(x, t)$ be the restriction of $u(x, t)$ for $x \ge 0$. Note that 

1. $v(x, t)$ solves the wave equation because $u(x, t)$ solves it.
2. $v(x, 0) = u(x, 0) = \phi _ {\text{even}}(x) = \phi(x)$ and $v_t(x, 0) = u_t(x, 0) = \psi _ {\text{even}}(x) = \psi(x)$.
3. Since $u(-x, t) = u(x, t)$, we have $u_x(-x, t) = -u_x(x, t)$. In particular, $u_x(0, t) = -u_x(0, t)$, so that $u_x(0, t) = 0$. Thus, 

$$\begin{align*} v_x(0, t) &= \lim_{x \to 0^+} u_x(x, t) \\
&= \lim_{x \to 0^+} -u_x(-x, t) \\
&= -u_x(0, t) \\
&= 0. \end{align*}$$  

Thus, $v(x, t)$ is the unique solution of the half-line problem. 

Note that for $x > ct$, we have 

$$\begin{cases}
\phi _ {\text{even}}(x+ct) = \phi(x+ct) \\
\phi _ {\text{even}}(x - ct) = \phi(x-ct) \\
\psi _ {\text{even}}(s) = \psi(s) \quad (x-ct \le s \le x+ct)
\end{cases}$$

Thus, in this case, we have
$$\begin{align*}
v(x, t) &= \frac{1}{2} [\phi(x + ct) + \phi(x - ct)] + \frac{1}{2c} \int_{x - ct}^{x + ct} \psi(s) ds.
\end{align*}$$

Note that for $0 < x < ct$, we have 

$$\begin{cases}
\phi _ {\text{even}}(x+ct) = \phi(x+ct) \\
\phi _ {\text{even}}(x - ct) = \phi(ct-x) \\
\psi _ {\text{even}}(s) = \begin{cases} \psi(s) & \text{for } 0 < s \le x + ct \\ 
\psi(-s) & \text{for } x - ct \le s < 0. \end{cases}
\end{cases}$$

Thus, in this case, we have
$$\begin{align*}
v(x, t) &= \frac{1}{2} [\phi(ct + x) + \phi(ct - x)] + \frac{1}{2c} \left[ \int_{0}^{x + ct} \psi(s) \, ds + \int_{x-ct}^0 \psi(-s) \, ds \right] \\
&= \frac{1}{2} [\phi(ct + x) + \phi(ct - x)] + \frac{1}{2c} \left[ \int_{0}^{ct + x} \psi(s) \, ds - \int_{ct-x}^{0} \psi(s) \, ds \right] \\
&= \frac{1}{2} [\phi(ct + x) + \phi(ct - x)] + \frac{1}{2c} \left[ \int_{0}^{ct + x} \psi(s) \, ds + \int_{0}^{ct-x} \psi(s) \, ds \right]
\end{align*}$$