---
title: Cauchy-Riemann Equation in Polar Coordinates
date: 2026-04-09
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Remark
Suppose that for $f(z) = u(x, y) + i v(x, y)$, $u(x, y)$ and $v(x, y)$ satisfy the Cauchy-Riemann equations 

$$
\begin{cases}
u_x = v_y \\
u_y = -v_x
\end{cases}
$$

Let substitute $x = r \cos \theta$ and $y = r \sin \theta$. Note that 

$$
\begin{cases}
u_r = u_x \cos \theta + u_y \sin \theta \\
u_\theta = -u_x r \sin \theta + u_y r \cos \theta \\
v_r = v_x \cos \theta + v_y \sin \theta \\
v_\theta = -v_x r \sin \theta + v_y r \cos \theta
\end{cases}
$$

Then we have 

$$\begin{bmatrix} u_r \\ u_\theta \end{bmatrix} = \begin{bmatrix} \cos \theta & \sin \theta \\ -r \sin \theta & r \cos \theta \end{bmatrix} \begin{bmatrix} u_x \\ u_y \end{bmatrix}$$

If $z \neq 0$, then the coefficient matrix has the determinant $r \cos^2 \theta + r \sin^2 \theta = r \neq 0$. Thus we have 

$$\begin{bmatrix} u_x \\ u_y \end{bmatrix} = \frac{1}{r} \begin{bmatrix} r \cos \theta & -r \sin \theta \\ \sin \theta & \cos \theta \end{bmatrix} \begin{bmatrix} u_r \\ u_\theta \end{bmatrix}$$

Similarly, we have 

$$\begin{bmatrix} v_x \\ v_y \end{bmatrix} = \frac{1}{r} \begin{bmatrix} r \cos \theta & -r \sin \theta \\ \sin \theta & \cos \theta \end{bmatrix} \begin{bmatrix} v_r \\ v_\theta \end{bmatrix}$$

Applying the Cauchy-Riemann equations in Cartesian coordinates, we have 

$$\begin{cases} \cos \theta - \frac{1}{r} \sin \theta = u_x = v_y = \frac{1}{r} v_\theta \\ \sin \theta + \frac{1}{r} \cos \theta = u_y = -v_x = -\frac{1}{r} v_r \end{cases}$$

By multipliying $r$ to the both sides, we have 

$$\begin{cases} \cos \theta (ru_r - v_\theta) - \sin \theta (ru_y + v_r) = 0 \\ \sin \theta (ru_r - v_\theta) + \cos \theta (ru_y + v_r) = 0 \end{cases}$$

so that 

$$\begin{bmatrix}
 \cos \theta & - \sin \theta \\ 
 \sin \theta & \cos \theta
\end{bmatrix} \begin{bmatrix}
 ru_r - v_\theta \\ 
 ru_y + v_r
\end{bmatrix} = \begin{bmatrix}
 0 \\ 
 0
\end{bmatrix}$$

Thus we obtain the Cauchy-Riemann equations in polar coordinates:

$$
\begin{cases}
ru_r = v_\theta \\ 
rv_r = -u_\theta
\end{cases}
$$

## Theorem 1
Let $f(z) = u(r, \theta) + i v(r, \theta)$ be defined throughout some $\varepsilon$ neighborhood of $z_0 = r_0 e^{i \theta_0}$. Suppose that $u_r, u_\theta, v_r, v_\theta$ exist in this neighborhood, are continuous at $(r_0, \theta_0)$, and satisfy the Cauchy-Riemann equations in polar coordinates at $(r_0, \theta_0)$:

$$
\begin{cases}
r u_r = v_\theta \\
r v_r = -u_\theta
\end{cases}
$$

Then $f$ is differentiable at $z_0$ and

$$
f'(z_0) = e^{-i \theta_0} (u_r + i v_r)
$$

### Proof

---

## Theorem 2