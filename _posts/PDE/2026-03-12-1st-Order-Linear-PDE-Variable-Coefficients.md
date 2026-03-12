---
title: 1st Order Linear PDE with Variable Coefficients
date: 2026-03-12
categories: [Mathematics, PDE]
tags: []
math: true
---

## Theorem
The general solution of a follwing PDE

$$u_x + f(x,y)u_y = 0$$ 

is given by solving the following ODE

$$\frac{dy}{dx} = f(x,y).$$

The solution of the above ODE is called the ***characteristic curve*** of the PDE.

### Proof
Note that 

$$u_x + f(x,y)u_y = \nabla u \cdot \mathbf{v} = D_\mathbf{v}u = 0$$

where $\mathbf{v} = (1, f(x,y))$. 

Then $u(x, y)$ must be a constant along the direction $\mathbf{v} = (1, f(x,y))$ at each point $(x, y)$. Let $C$ be a curve which is tangent to $\mathbf{v}$ at each point $(x, y)$. Then we have 

$$\frac{dy}{dx} = f(x,y)$$

Suppose that the solution of this ODE exists and is implicitly given by $h(x, y) = c$, where $c$ is a constant. Then $u(x, y)$ must be a constant along the curve defined by the equation $h(x, y) = c$, which means that the value of $u$ is determined by the constant $c$. Thus the solution is given by 

$$u(x, y) = F(c)$$

where $F$ is an arbitrary function. 

Now we check the solution $u(x, y) = F(c)$ satisfies the PDE $u_x + f(x,y)u_y = 0$. Note that

$$\begin{align*} u_x &= F' \cdot \frac{\partial h}{\partial x} \\
u_y &= F' \cdot \frac{\partial h}{\partial y},\end{align*}$$

and

$$\begin{align*} 
&\frac{d}{dx} h(x, y) = \frac{d}{dx} c \\
\implies &h_x + h_y \frac{dy}{dx} = h_x + h_y f(x,y) = 0.
\end{align*}$$

Thus we have 

$$\begin{align*}
u_x + f(x,y)u_y &= F' \cdot \frac{\partial h}{\partial x} + F' \cdot \frac{\partial h}{\partial y} \cdot f(x,y) \\
&= F' \cdot (h_x + h_y f(x,y)) \\
&= F' \cdot 0 = 0.
\end{align*}$$

Hence $u(x, y) = F(c)$ satisfies the PDE $u_x + f(x,y)u_y = 0$. $\blacksquare$