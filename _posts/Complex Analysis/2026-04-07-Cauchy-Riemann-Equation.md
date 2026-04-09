---
title: Cauchy-Riemann Equation
date: 2026-04-07
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Theorem 1
Suppose that $f(z) = u(x, y) + i v(x, y)$ is differentiable at $z_0 = x_0 + i y_0$. Then $u_x, u_y, v_x, v_y$ exist and satisfy the Cauchy-Riemann equations at $(x_0, y_0)$:

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

$$\begin{cases}
u_x = v_y \\
u_y = -v_x. \blacksquare
\end{cases}$$

---

## Theorem 2
Let $f(z) = u(x, y) +iv(x, y)$ be defined throughout some $\varepsilon$ neighborhood of $z_0 = x_0 + i y_0$. Suppose that $u_x, u_y, v_x, v_y$ exist in this neighborhood, are continuous at $(x_0, y_0)$, and satisfy the Cauchy-Riemann equations at $(x_0, y_0)$. Then $f$ is differentiable at $z_0$ and $f'(z_0)$ is given by

$$ \begin{align*}
f'(z_0) &= u_x(x_0, y_0) + i v_x(x_0, y_0) \\
&= v_y(x_0, y_0) - i u_y(x_0, y_0)
\end{align*}
$$

### Proof
Let $\Delta z = \Delta x + i \Delta y$ where $0 < \vert \Delta z \vert < \varepsilon$. Since the first order partial derivatives exist and are continuous at $(x_0, y_0)$, we have 

$$\Delta u = u(x_0 + \Delta x, y_0 + \Delta y) - u(x_0, y_0) = u_x \Delta x + u_y \Delta y + \varepsilon_1 \Delta x + \varepsilon_2 \Delta y$$ 

for some $\varepsilon_1, \varepsilon_2 > 0$ such that $\varepsilon_1, \varepsilon_2 \to 0$ as $(\Delta x, \Delta y) \to 0$. Then we have 

$$\begin{align*}
\Delta w &= \Delta u + i \Delta v \\
&= u_x \Delta x + u_y \Delta y + \varepsilon_1 \Delta x + \varepsilon_2 \Delta y + i (v_x \Delta x + v_y \Delta y + \varepsilon_3 \Delta x + \varepsilon_4 \Delta y) \\
&= (u_x - v_y) \Delta x + (u_y + v_x) \Delta y + \varepsilon_1 \Delta x + \varepsilon_2 \Delta y + i \varepsilon_3 \Delta x + i \varepsilon_4 \Delta y \\
\end{align*}$$