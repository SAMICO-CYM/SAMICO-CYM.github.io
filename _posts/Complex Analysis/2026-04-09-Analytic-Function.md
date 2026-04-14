---
title: Analytic Function
date: 2026-04-09
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Definition
Let $f$ be a complex function.

**(i)** $f$ is said to be ***analytic*** on an open set $S$ if it has a derivative everywhere on $S$. 

**(ii)** $f$ is said to be ***analytic*** at a point $z_0$ if it is analytic on some open set containing $z_0$.

**(iii)** $f$ is said to be ***entire*** if it is analytic on $\mathbb{C}$.

**(iv)** If $f$ fails to be analytic at a point $z_0$ but is analytic at some point in every neightborhood of $z_0$, then $z_0$ is called a ***singular point*** of $f$.

---

## Example
**(i)** Let $f(z) = \frac{1}{z}$. Since $f$ has a derivative at each nonzero point in $\mathbb{C}$, $f$ is analytic on $\mathbb{C} \setminus \\{ 0 \\}$ and $f$ is NOT analyic at $0$. Thus $z_0 = 0$ is a singular point of $f$.

**(ii)** Let $f(z) = \vert z \vert^2$. Since $f$ has a derivative at only $z = 0$, $f$ is NOT analytic anywhere. Thus $f$ has no singular points.

---

## Remark
Let $f$ and $g$ be analytic functions on $D \subset \mathbb{C}$. Then $f + g$, $f - g$, $f g$, $f / g$ (where $g(z) \neq 0$), and $f \circ g$ are analytic on $D$. 

---

## Theorem 1
If $f'(z) = 0, \forall z \in D$, then $f(z)$ is constant on $D$. 

### Proof

---

## Theorem 2
Let $f$ be an analytic function on $D \subset \mathbb{C}$. 

**(i)** If $\overline{f}$ is also analytic on $D$, then $f$ is constant on $D$. 

**(ii)** If $\vert f (z) \vert$ is constant in $D$, then $f$ is constant on $D$.

### Proof
