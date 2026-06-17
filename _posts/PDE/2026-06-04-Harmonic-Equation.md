--- 
title: Harmonic Equation
date: 2026-06-04
categories: [Mathematics, PDE]
tags: []
math: true
---

## Definition
**(i)** The equation 

$$\Delta u = u_{xx} + u_{yy} + u_{zz} = 0$$

is called the ***Laplace equation***. 

**(ii)** A solution of the Laplace equation is called a ***harmonic function***.

**(iii)** The inhomogeneous version of Laplace equation 

$$\Delta u = f$$

with $f$ a given function, is called ***Poisson equation***.

---
## Maximum Principle
Let $D$ be a connected bounded open subset of $\mathbb{R}^2,$ and let $u : \mathbb{R}^2 \to \mathbb{R}$ be a harmonic function in $D$ which is continuous on $\overline{D} = D \cup \partial D.$ Then the maximum and minimum values of $u$ are attained on $\partial D$ and nowhere inside, unless $u$ is a constant. 

### Proof

---
## Uniquness
The Dirichlect Problem

$$\begin{cases}
\Delta u = f & \text{in } D \\
u = h & \text{on } \partial D
\end{cases}$$

has the unique solution.

### Proof
Let $u, v$ be the two solutions of the given problem, that is,

$$\begin{cases}
\Delta u = f & \text{in } D \\
u = h & \text{on } \partial D
\end{cases} \quad  \text{and} \quad \begin{cases}
\Delta v = f & \text{in } D \\
v = h & \text{on } \partial D.
\end{cases}$$

Let $w := u - v.$ Then $w$ satisfies

$$\begin{cases}
\Delta w = 0 & \text{in } D \\
w = 0 & \text{on } \partial D.
\end{cases}$$

By the maximum principle, we have 

$$0 = \min_{x \in D} w \le w(x) \le \max_{x \in D} w(x) = 0,$$

so $w \equiv 0.$ Thus, $u = v.$ $\blacksquare$

---
## Invariance
The Laplace equation is invariant under all rigid motions; translation and rotation. Furthermore,

**(i)** $2$-$D:$ In the polar coordinate $(r, \theta),$

$$\Delta_2 = \frac{\partial^2}{\partial x^2} + \frac{\partial^2}{\partial y^2} = \frac{\partial^2}{\partial r^2} + \frac{1}{r} \frac{\partial}{\partial r} + \frac{1}{r^2} \frac{\partial^2}{\partial \theta^2}.$$

**(ii)** $3$-$D:$ In the spherical coordinate $(r, \theta, \phi),$

$$\Delta_3 = \frac{\partial^2}{\partial x^2} + \frac{\partial^2}{\partial y^2} + \frac{\partial^2}{\partial z^2} = \frac{\partial^2}{\partial r^2} + \frac{2}{r} \frac{\partial}{\partial r} + \frac{1}{r^2 \sin \theta} \frac{\partial}{\partial \theta} \sin \theta \frac{\partial}{\partial \theta} + \frac{1}{r^2 \sin \theta} \frac{\partial^2}{\partial \phi^2}.$$

### Proof
First, we consider the translation. By the translation, the coordiante is changed as 

$$\begin{cases}
x' = x + a \\
y' = y + b,
\end{cases}$$

so 

$$u_{x'x'} + u_{y'y'} = u_{xx} + u_{yy}.$$

Thus, the Laplace equation is invariant under the translation.

Next, we consider the rotation. For the convenience, we only treat the two-dimensional rotation. By the rotation, we have 

$$\begin{bmatrix}
x' \\
y'
\end{bmatrix} = \begin{bmatrix}
\cos \theta & \sin \theta \\
-\sin \theta & \cos \theta
\end{bmatrix} \begin{bmatrix}
x \\
y
\end{bmatrix},$$

so 

$$\begin{cases}
x' = x \cos \theta + y \sin \theta \\
y' = -x \sin \theta + y \cos \theta.
\end{cases}$$

By the chain rule, we have

$$\begin{align*}
u_x &= u_{x'} \cos \alpha - u_{y'} \sin \alpha \\
u_y &= u_{x'} \sin \alpha + u_{y'} \cos \alpha \\
u_{xx} &= (u_{x'} \cos \alpha - u_{y'} \sin \alpha)_{x'} \cos \alpha - (u_{x'} \cos \alpha - u_{y'} \sin \alpha)_{y'} \sin \alpha \\
u_{yy} &= (u_{x'} \sin \alpha + u_{y'} \cos \alpha)_{x'} \sin \alpha + (u_{x'} \sin \alpha + u_{y'} \cos \alpha)_{y'} \cos \alpha,
\end{align*}$$

so

$$\begin{align*}
u_{xx} + u_{yy} &= (u_{x'x'} + u_{y'y'})(\cos^2 \alpha + \sin^2 \alpha) + u_{x'y'} \cdot (0) \\
&= u_{x'x'} + u_{y'y'}.
\end{align*}$$

Thus, the Laplace equation is invariant under the rotation.

Furthermore, we can induce the rotational form of the Laplace operator in $2$-$D$ and $3$-$D.$

In $2$-$D$, we change the coordinate

$$\begin{cases}
x = r\cos \theta \\
y = r \sin \theta.
\end{cases}$$

The Jacobian matrix is given by 

$$J = \begin{bmatrix}
\frac{\partial x}{\partial r} & \frac{\partial y}{\partial r} \\
\frac{\partial x}{\partial \theta} & \frac{\partial y}{\partial \theta}
\end{bmatrix} = \begin{bmatrix}
\cos \theta & \sin \theta \\
-r\sin \theta & r \cos \theta
\end{bmatrix},$$

and the inverse matrix is 

$$J^{-1} = \frac{1}{r} \begin{bmatrix}
r \cos \theta & - \sin \theta \\
r \sin \theta & \cos \theta
\end{bmatrix} = \begin{bmatrix}
\cos \theta & - \frac{1}{r} \sin \theta \\
\sin \theta & \frac{1}{r} \cos \theta
\end{bmatrix} = \begin{bmatrix}
\frac{\partial r}{\partial x} & \frac{\partial \theta}{\partial x} \\
\frac{\partial r}{\partial y} & \frac{\partial \theta}{\partial y}
\end{bmatrix}.$$

By the chain rule, we have 

$$\begin{align*}
\frac{\partial}{\partial x} &= \cos \theta \frac{\partial}{\partial r} - \frac{\sin \theta}{r} \frac{\partial}{\partial \theta} \\
\frac{\partial}{\partial y} &= \sin \theta \frac{\partial}{\partial r} + \frac{\cos \theta}{r} \frac{\partial}{\partial \theta}
\end{align*}$$

so

$$\begin{align*}
\frac{\partial^2}{\partial x^2} &= \left[ \cos \theta \frac{\partial}{\partial r} - \frac{\sin \theta}{r} \frac{\partial}{\partial \theta} \right]^2 \\
&= \cos^2 \theta \frac{\partial^2}{\partial r^2} - 2 \left( \frac{\sin \theta \cos \theta}{r} \right) \frac{\partial^2}{\partial r \partial \theta} + \frac{\sin^2 \theta}{r^2} \frac{\partial^2}{\partial \theta^2} + \frac{2 \sin \theta \cos \theta}{r^2} \frac{\partial}{\partial \theta} + \frac{\sin^2 \theta}{r} \frac{\partial}{\partial r} \\
\frac{\partial^2}{\partial y^2} &= \left( \sin \theta \frac{\partial}{\partial r} + \frac{\cos \theta}{r} \frac{\partial}{\partial \theta} \right)^2 \\
&= \sin^2 \theta \frac{\partial^2}{\partial r^2} + 2 \left( \frac{\sin \theta \cos \theta}{r} \right) \frac{\partial^2}{\partial r \partial \theta} + \frac{\cos^2 \theta}{r^2} \frac{\partial^2}{\partial \theta^2} - \frac{2 \sin \theta \cos \theta}{r^2} \frac{\partial}{\partial \theta} + \frac{\cos^2 \theta}{r} \frac{\partial}{\partial r}.
\end{align*}$$

Thus, we obtain

$$\begin{align*}
\Delta_2 = \frac{\partial^2}{\partial x^2} + \frac{\partial^2}{\partial y^2} = \frac{\partial^2}{\partial r^2} + \frac{1}{r} \frac{\partial}{\partial r} + \frac{1}{r^2} \frac{\partial^2}{\partial \theta^2}.
\end{align*}$$

Simlarly, we can obtain the $3$-$D$ version:

$$\Delta_3 = \frac{\partial^2}{\partial x^2} + \frac{\partial^2}{\partial y^2} + \frac{\partial^2}{\partial z^2} = \frac{\partial^2}{\partial r^2} + \frac{2}{r} \frac{\partial}{\partial r} + \frac{1}{r^2 \sin \theta} \frac{\partial}{\partial \theta} \sin \theta \frac{\partial}{\partial \theta} + \frac{1}{r^2 \sin \theta} \frac{\partial^2}{\partial \phi^2}. \quad \blacksquare$$

---
## Corollary
**(i)** If a $2$-$D$ harmonic function $u$ is rotationally invariant, then 

$$0 = u_{rr} + \frac{1}{r}u_r,$$

so the solution is 

$$u(r, \theta) = C_1 \log r + C_2$$

for some constants $C_1, C_2.$

**(ii)** If a $3$-$D$ harmonic function $u$ is rotationally invariant, then 

$$0 = u_{rr} + \frac{2}{r}u_r,$$

so the solution is 

$$u(r, \theta) = -\frac{C_1}{r} + C_2$$

for some constants $C_1, C_2.$