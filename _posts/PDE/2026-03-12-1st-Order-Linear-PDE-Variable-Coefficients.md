---
title: 1st Order Linear PDE with Variable Coefficients
date: 2026-03-12
categories: [Mathematics, PDE]
tags: []
math: true
---

## Theorem
The general solution of the follwing PDE

$$a(x, y)u_x + b(x,y)u_y = 0$$ 

where $a(x, y)$ and $b(x, y)$ are functions of $x$ and $y$, is given by

$$u(x, y) = F(c) = F(f(x, y))$$

where $F$ is an arbitrary function and $c = f(x, y)$ is an implicit solution to the ODE

$$\frac{dy}{dx} = \frac{b(x, y)}{a(x, y)}$$

whenever $a(x, y) \neq 0$. The solution of the above ODE is called the ***characteristic curve*** of the PDE.

### Proof
Note that 

$$a(x, y)u_x + b(x,y)u_y = \nabla u \cdot \mathbf{v} = D_\mathbf{v}u = 0$$

where $\mathbf{v} = (a(x, y), b(x,y))$. 

Then $u(x, y)$ must be a constant along the direction $\mathbf{v} = (a(x, y), b(x,y))$ at each point $(x, y)$. Let $C$ be a curve which is tangent to $\mathbf{v}$ at each point $(x, y)$. Then we have 

$$\frac{dy}{dx} = \frac{b(x, y)}{a(x, y)}$$

whenever $\mathbf{v} \neq \mathbf{0}$ and $a(x, y) \neq 0$. 

Suppose that the solution of this ODE exists and is implicitly given by $f(x, y) = c$, where $c$ is a constant. Then $u(x, y)$ must be a constant along this curve $C$, which means that the value of $u$ is determined by the constant $c$. Thus the solution is given by 

$$u(x, y) = F(c) = F(f(x, y))$$

where $F$ is an arbitrary function and whenever $a(x, y) \neq 0$. 

Now we check the solution $u(x, y) = F(c)$ satisfies the PDE $a(x, y)u_x + b(x,y)u_y = 0$. Note that

$$\begin{align*} u_x &= F' \cdot \frac{\partial f}{\partial x} \\
u_y &= F' \cdot \frac{\partial f}{\partial y},\end{align*}$$

and

$$\begin{align*} 
\frac{d}{dx} c &= \frac{d}{dx} f(x, y) \\
&= f_x + f_y \frac{dy}{dx} \\
&= f_x + f_y \frac{b(x, y)}{a(x, y)} \\
&= 0.
\end{align*}$$

Thus we have 

$$\begin{align*}
a(x, y)u_x + b(x,y)u_y &= a(x, y)F' \cdot \frac{\partial f}{\partial x} + b(x,y)F' \cdot \frac{\partial f}{\partial y} \\
&= F' \cdot (a(x, y) \frac{\partial f}{\partial x} + b(x,y) \frac{\partial f}{\partial y}) \\
&= F' \cdot 0 = 0.
\end{align*}$$

Hence $u(x, y) = F(c)$ satisfies the PDE $a(x, y)u_x + b(x,y)u_y = 0$. $\blacksquare$