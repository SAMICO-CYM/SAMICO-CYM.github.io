---
title: 2nd Order Linear PDE
date: 2026-03-24
categories: [Mathematics, PDE]
tags: []
math: true
---

## Definition
A ***second order linear PDE*** in two independent variables $x$ and $y$ is given by

$$
a_{11}u_{xx} +2a_{12}u_{xy} + a_{22}u_{yy} + a_1u_x + a_2u_y + a_0u = f(x, y)
$$

where $a_{11}, a_{12}, a_{22}, a_1, a_2, a_0$ and $f$ are functions of $x$ and $y$. 

---

## Theorem
By a linear transformation of the independent variables, the equation can be reduced to one of three forms, as follows:

**(i)** Elliptic case: If $a_{12}^2 < a_{11}a_{22}$, it is reducible to 

$$u_{xx} + u_{yy} + \cdots = 0$$

where $\cdots$ denotes terms of order less than 2.

**(ii)** Hyperbolic case: If $a_{12}^2 > a_{11}a_{22}$, it is reducible to 

$$u_{xx} - u_{yy} + \cdots = 0$$

**(iii)** Parabolic case: If $a_{12}^2 = a_{11}a_{22}$, it is reducible to 

$$u_{xx} + \cdots = 0$$

unless $a_{11} = a_{12} = a_{22} = 0$.

### Proof
(i) For convenience, we assume $a_{11} = 1$ and $a_1 = a_2 = a_0 = 0$. Then

$$\begin{align*}
0 &= u_{xx} + 2a_{12}u_{xy} + a_{22}u_{yy} \\
&= u_{xx} + 2a_{12}u_{xy} + a_{12}^2u_{yy} + (a_{22} - a_{12}^2)u_{yy} \\
&= (\partial_x + a_{12} \partial_y)^2u + (a_{22} - a_{12}^2)\partial^2_y u \quad \cdots \quad (\ast)
\end{align*}$$

Since $a^2_{12} < a_{11}a_{22}$, we let $b = \sqrt{a_{22} - a^2_{12}}$. Let substitute

$$\begin{align*}
x &= \xi \\
y &= a_{12} \xi + b \eta
\end{align*}$$ 

Then

$$\begin{align*}
\partial_\xi &= \partial_x + a_{12} \partial_y \\
\partial_\eta &= b \partial_y
\end{align*}$$ 

so that

$$(\ast): 0 = \partial^2_\xi u + \partial^2_\eta u$$

---

## Example