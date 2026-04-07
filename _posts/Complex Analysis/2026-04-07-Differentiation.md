---
title: Differentiation
date: 2026-04-07
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Definition
Let $f$ be a function whose domain contains a neighborhood of a point $z_0$. Then $f$ is said to be ***differentiable*** at $z_0$ if the limit 

$$\lim_{z \to z_0} \frac{f(z) - f(z_0)}{z - z_0}$$

exists. If the limit exists, it is denoted by $f'(z_0)$ and said to be the ***derivative*** of $f$ at $z_0$. A function $f$ is said to be ***differentiable*** on a set $S$ if it is differentiable at every point in $S$.

---

## Remark
By expressing $\Delta z = z - z_0$ and $\Delta w = f(z) - f(z_0)$ which denotes the change in the value $w = f(z)$ of $f$ corresponding to a change $\Delta z$ in the point at which $f$ is evaluated, we can write the derivative as 

$$\frac{dw}{dz} = \lim_{\Delta z \to 0} \frac{\Delta w}{\Delta z}$$

---

## Theorem 1
If $f$ is differentiable at $z_0$, then $f$ is continuous at $z_0$.

### Proof

$$\begin{align*}
\lim_{z \to z_0} (f(z) - f(z_0)) &= \lim_{z \to z_0} \frac{f(z) - f(z_0)}{z - z_0} \cdot (z - z_0) \\
&= \lim_{z \to z_0} \frac{f(z) - f(z_0)}{z - z_0} \cdot \lim_{z \to z_0} (z - z_0) \\
&= f'(z_0) \cdot 0 \\
&= 0.
\end{align*}$$

Thus we have $\lim_{z \to z_0} f(z) = f(z_0)$, which means that $f$ is continuous at $z_0$. $\blacksquare$

---

## Theorem 2

**(i)** $\displaystyle \frac{d}{dz} [cf(z) + g(z)] = c f'(z) + g'(z)$

**(ii)** $\displaystyle \frac{d}{dz} [f(z) g(z)] = f'(z) g(z) + f(z) g'(z)$

**(iii)** $\displaystyle \frac{d}{dz} \left[ \frac{f(z)}{g(z)} \right] = \frac{f'(z) g(z) - f(z) g'(z)}{[g(z)]^2}$

**(iv)** $\displaystyle \frac{d}{dz} [f(g(z))] = f'(g(z)) g'(z)$