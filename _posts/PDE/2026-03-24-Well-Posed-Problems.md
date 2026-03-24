--- 
title: Well-Posed Problems
date: 2026-03-24
categories: [Mathematics, PDE]
tags: []
math: true
---

## Definition
***Well-posed problems*** consist of a PDE in a domain together with a set of initial and/or boundary conditions (or other auxiliary conditions) that enjoy the following properties:

**(i)** ***Existence***: There exists at least one solution $u(x, t)$ satisfying the given PDE and a set of initial and/or boundary conditions.

**(ii)** ***Uniqueness***: There is at most one solution.

**(iii)** ***Stability***: The unique solution $u(x, t)$ depends in a stable manner on the data of the problem. This means that if the data are changed a little, the corresponding solution changes only a little.

## Example
**(i)** Consider the vibrating string with an external force $f(x, t)$ on the interval $(0, L)$ and initial and boundary condtions as follows:

$$\begin{cases}
Tu_{tt} - \rho u_{xx} = f(x, t) \\
u(x, 0) = \phi(x), \quad u_t(x, 0) = \psi(x) \\
u(0, t) = g(t), \quad u(L, t) = h(t)
\end{cases}$$

for $0 < x < L$ and $t > 0$. The data for this problem consist of the five functions $f, \phi, \psi, g, h$. This problem is well-posed.

**(ii)** Consider the Laplace equation 

$$\Delta u = u_{xx} + u_{yy} = 0$$

in the region $D = \mathbb{R} \times \mathbb{R}^+$. This problem is not well-posed because it is not stable.

The solution of the problem is given by

$$u_n(x, y) = \frac{1}{n} e^{-\sqrt{n}} \sin nx \sinh ny.$$

for each positive integer $n$. Note that 

$$\lim_{n \to \infty} \frac{\partial u_n}{\partial y}(x, 0) = 0,$$ 

but 

$$\begin{align*}
\lim_{n \to \infty} \frac{\partial u_n}{\partial y}(x, 1) &= \lim_{n \to \infty} e^{-\sqrt{n}} \sin nx \cosh n \\
&= \lim_{n \to \infty} \sin nx \frac{e^{n - \sqrt{n}} + e^{-n - \sqrt{n}}}{2} = \infty.
\end{align*}$$ 

Thus, the solution is not stable. 