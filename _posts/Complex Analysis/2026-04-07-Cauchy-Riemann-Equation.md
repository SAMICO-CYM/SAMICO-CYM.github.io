---
title: Cauchy-Riemann Equation
date: 2026-04-07
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Theorem
Suppose that $f(z) = u(x, y) + i v(x, y)$ is differentiable at $z_0 = x_0 + i y_0$. Then 

**(i)** $u_x, u_y, v_x, v_y$ exist at $(x_0, y_0)$

**(ii)** $u_x, u_y, v_x, v_y$ satisfy the Cauchy-Riemann equations:

$$
\begin{cases}
u_x = v_y \\
u_y = -v_x
\end{cases}
$$

### Proof
Denote $\Delta z = \Delta x + i \Delta y$. Note that 

$$\begin{align*}
\Delta w &= f(z + \Delta z) - f(z) \\
&= u(x_0 + \Delta x, y_0 + \Delta y) - u(x_0, y_0) + i [v(x_0 + \Delta x, y_0 + \Delta y) - v(x_0, y_0)] 
\end{align*}$$

Then we have 

$$\begin{align*}
\frac{\Delta w}{\Delta z} &= \frac{u(x_0 + \Delta x, y_0 + \Delta y) - u(x_0, y_0)}{\Delta x + i \Delta y} + i \frac{v(x_0 + \Delta x, y_0 + \Delta y) - v(x_0, y_0)}{\Delta x + i \Delta y}
\end{align*}$$

Along the horizontal line $\Delta y = 0$, we have 

$$\begin{align*}
f'(z_0) &= \lim_{\Delta x \to 0} \frac{\Delta w}{\Delta z} \\
&= \lim_{\Delta x \to 0} \frac{u(x_0 + \Delta x, y_0) - u(x_0, y_0)}{\Delta x} + i \lim_{\Delta x \to 0} \frac{v(x_0 + \Delta x, y_0) - v(x_0, y_0)}{\Delta x} \\
&= u_x(x_0, y_0) + i v_x(x_0, y_0)
\end{align*}$$

Along the vertical line $\Delta x = 0$, we have 

$$\begin{align*}
f'(z_0) &= \lim_{\Delta y \to 0} \frac{\Delta w}{\Delta z} \\
&= \lim_{\Delta y \to 0} \frac{u(x_0, y_0 + \Delta y) - u(x_0, y_0)}{i \Delta y} + i \lim_{\Delta y \to 0} \frac{v(x_0, y_0 + \Delta y) - v(x_0, y_0)}{i \Delta y} \\
&= -i u_y(x_0, y_0) + v_y(x_0, y_0)
\end{align*}$$

Thus we have 

$$\begin{align*}
u_x = v_y \\
u_y = -v_x \blacksquare
\end{align*}$$
