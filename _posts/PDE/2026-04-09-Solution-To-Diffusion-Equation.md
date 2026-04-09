---
title: Solution To Diffusion Equation
date: 2026-04-09
categories: [Mathematics, PDE]
tags: []
math: true
---

## Lemma
There are five invariance properties of the diffusion equation:

**(i)** The ***translate*** $u(x - y, t)$ of any solution $u(x, t)$ is another solution, for any fixed $y$.

**(ii)** Any ***derivative*** ($u_x$ or $u_t$ or $u_{xx}$, etc.) of a solution is again a solution.

**(iii)** A ***linear combination*** of solutions is again a solution.

**(iv)** An ***integral*** of solutions is again a solution. Thus if $S(x, t)$ is a solution, then so is $S(x - y, t)$ and so is

$$
v(x, t) = \int_{-\infty}^{\infty} S(x - y, t)g(y) dy
$$

for any function $g(y)$, as long as this improper integral converges appropriately.

**(v)** If $u(x,t)$ is a solution, so is the ***dilated*** function $u(\sqrt{a}x, at)$, for any $a > 0$.

### Proof

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

To construct a solution, we first look for the particular solution $Q(x, t)$ which satisfies the initial condition 

$$Q(x, 0) = \begin{cases}
1 & x > 0 \\
0 & x < 0
\end{cases}$$

That is, $Q(x, 0)$ is the Heaviside function $H(x)$. Note that this initial condition does not change under dilation, i.e., $Q(x, 0) = Q(\sqrt{a}x, 0)$ for any $a > 0$. Since $Q(\sqrt{a}x, at)$ is also a solution for any $a > 0$, we consider $a = \frac{1}{t}$ for $t > 0$ and obtain the solution $Q(x, t) = Q(\frac{x}{\sqrt{t}}, 1) =: g(p)$, where 

$$p = \frac{x}{\sqrt{4kt}},$$

for some one variable function $g$. 

Note that 

$$ \begin{align*}
Q_t(x, t) &= g'(p) \frac{\partial p}{\partial t} = -\frac{1}{2t} \frac{x}{\sqrt{4kt}} g'(p), \\
Q_{xx}(x, t) &= g''(p) \left( \frac{\partial p}{\partial x} \right)^2 = \frac{1}{4kt} g''(p).
\end{align*} $$

Substituting these into the diffusion equation, we get

$$\begin{align*}
0 &= Q_t - k Q_{xx} \\
&= -\frac{1}{2t} \frac{x}{\sqrt{4kt}} g'(p) - k \frac{1}{4kt} g''(p) \\
&= -\frac{1}{4kt} \left( 2 p g'(p) + g''(p) \right).
\end{align*}$$

Thus, we get the second-order linear ODE $g'' + 2pg' = 0$. By solving this ODE, we have $g'(p) = C_1 e^{-p^2}$ and therefore, $g(p) = C_1 \int e^{-p^2} \, dp + C_2$ for some constants $C_1$ and $C_2$. 

Suppose that 

$$Q(x, t) = C_1 \int_0^p e^{-s^2} \, ds + C_2$$

to find explicit formula for $Q$. If $x > 0$, then we have

$$1 = \lim_{t \to 0^+} Q(x, t) = C_1 \int_0^\infty e^{-s^2} \, ds + C_2 = C_1 \frac{\sqrt{\pi}}{2} + C_2.$$

If $x < 0$, then we have

$$0 = \lim_{t \to 0^+} Q(x, t) = C_1 \int_0^ {-\infty} e^{-s^2} \, ds + C_2 = -C_1 \frac{\sqrt{\pi}}{2} + C_2.$$

Thus, we get $C_1 = \frac{1}{\sqrt{\pi}}$ and $C_2 = \frac{1}{2}$ which gives 

$$Q(x, t) = \frac{1}{\sqrt{\pi}} \int_0^p e^{-s^2} \, ds + \frac{1}{2}.$$

We now define 

$$S(x, t) = \frac{\partial Q}{\partial x}(x, t).$$

By Lemma (ii), $S$ is also a solution. By Lemma (iv), we have 

$$u(x, t) = \int_{-\infty}^{\infty} S(x - y, t) \phi(y) dy$$

is a solution. 

Let's check the initial condition, i.e., $u(x, 0) = \phi(x)$. Assume that $\phi(y) = 0$ for sufficiently large $|y|$. Note that

$$\begin{align*}
u(x, t) &= \int_{-\infty}^{\infty} S(x - y, t) \phi(y) dy \\
&= \int_{-\infty}^{\infty} \frac{\partial Q}{\partial x}(x - y, t) \phi(y) dy \\
&= -\int_{-\infty}^{\infty} \frac{\partial Q}{\partial y}(x - y, t) \phi(y) dy \\
&= -\left[ Q(x - y, t) \phi(y) \right]_{-\infty}^{\infty} + \int_{-\infty}^{\infty} Q(x - y, t) \phi'(y) dy \\
&= \int_{-\infty}^{\infty} Q(x - y, t) \phi'(y) dy.
\end{align*}$$

Thus we have 

$$\begin{align*}
u(x, 0) &= \int_{-\infty}^{\infty} Q(x-y, 0) \phi'(y) dy \\
&= \int_{-\infty}^{x} \phi'(y) dy \\
&= \phi(x), 
\end{align*}$$

which means that $u$ is a solution to the diffusion equation with the initial condition $u(x, 0) = \phi(x)$. $\blacksquare$