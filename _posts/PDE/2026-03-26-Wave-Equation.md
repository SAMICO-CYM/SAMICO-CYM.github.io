---
title: Wave Equation
date: 2026-03-26
categories: [Mathematics, PDE]
tags: []
math: true
---

## Definition
The ***wave equation*** is a second order linear partial differential equation given by

$$
u_{tt} = c^2 u_{xx} \quad \text{for } -\infty < x < \infty
$$

where $c$ is a constant.

---

## Theorem
The initial value problem for the wave equation

$$\begin{cases}
u_{tt} = c^2 u_{xx} \\
u(x, 0) = \phi(x) \\
u_t(x, 0) = \psi(x)
\end{cases}$$

for $-\infty < x < \infty, t > 0$, where $\phi$ and $\psi$ are given functions, has the solution

$$
u(x, t) = \frac{1}{2} [\phi(x + ct) + \phi(x - ct)] + \frac{1}{2c} \int_{x - ct}^{x + ct} \psi(s) ds$$

### Proof

---

## Example

---

## Remark