---
title: 1st Order Linear PDE with Constant Coefficients
date: 2026-03-10
categories: [Mathematics, PDE]
tags: []
math: true
---

## Theorem
The general solution of a follwing PDE

$$au_x + bu_y = 0$$ 

where $a, b$ are constants, not both zero, is given by 

$$u(x, y) = f(bx - ay)$$

for some function of one variable.

### Proof
**(i) Geometric Method**

Let $v = (a, b)$. Note that 

$$au_x + bu_y = \nabla u \cdot v = D_vu = 0.$$

Then $u(x, y)$ must be a constant in the direction $v = (a, b).$ Since the lines parallel to $v$ are given by $bx - ay = c$, ($c$ is a constant) the solution $u$ has a constant value, say $f(c)$, on the line $bx - ay = c$. Thus the solution is given by 

$$u(x, y) = f(bx - ay).$$

**(ii) Coordinate Method**

Change variables to 

$$\begin{align*}
x' & = ax + by \\
y' & = bx - ay
\end{align*}$$

By the chain rule, we have 

$$\begin{align*}
u_x &= \frac{\partial u}{\partial x'} \frac{\partial x'}{\partial x} + \frac{\partial u}{\partial y'} \frac{\partial y'}{\partial x} \\
&= au_{x'} + bu_{y'}
\end{align*}$$

and similarly, 

$$\begin{align*}
u_y &= \frac{\partial u}{\partial x'} \frac{\partial x'}{\partial y} + \frac{\partial u}{\partial y'} \frac{\partial y'}{\partial y} \\
&= bu_{x'} - au_{y'}.
\end{align*}$$

Thus

$$\begin{align*} 
au_x + bu_y & = a(au_{x'} + bu_{y'}) + b(bu_{x'} - au_{y'}) \\
& = (a^2 + b^2) u_{x'} = 0,
\end{align*} $$

so that 

$$
\begin{align*}
&u_{x'} = 0 \\ 
\implies &u(x, y) = u(x', y') = f(y') = f(bx - ay).
\end{align*}
$$

Thus the solution is given by 

$$u(x, y) = f(bx - ay). \blacksquare$$