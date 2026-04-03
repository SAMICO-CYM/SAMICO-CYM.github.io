--- 
title: Continuous Functions
date: 2026-04-03
categories: [Mathematics, ]
tags: []
math: true
---

## Definition
Let $f: D \to \mathbb{C}$ be a complex function defined on a domain $D \subset \mathbb{C}$, and let $z_0 \in D$. We say that $f$ is ***continuous*** at $z_0$ if 

$$\forall \varepsilon > 0, \exists \delta > 0 \text{ s.t. } \vert z - z_0 \vert \implies \vert f(z) - f(z_0) \vert < \varepsilon.$$

If $f$ is continuous at each point in $D$, then $f$ is said to be ***continuous*** in $D$. 

---

## Theorem 1
Suppose that complex functions $f$ and $g$ are continuous at $z_0$. Then

(i) $f+g$ is continuous at $z_0$.

(ii) $cf$ is continuous at $z_0$ for any constant $c$.

(iii) $fg$ is continuous at $z_0$.

(iv) $\frac{f}{g}$ is continuous at $z_0$, provided $g \neq 0$. 

(v) If $g$ is continuous at $f(z_0)$, then $g \circ f$ is continuous at $z_0$. 

---

## Theorem 2
If a function $f(z)$ is continuous and nonzero at $z_0$, then $f(z) \neq 0$ throughout some neighborhood of $z_0$.

---

## Theorem 3
Let $f(z) = u(x, y) + iv(x, y)$ for $z = x+iy$. Then 

$$u \text{ and } v \text{ are continuous at } z_0 = x_0 + i y_0 \iff f \text{ is continuous at } z_0.$$

---

## Theorem 4
If a function $f$ is continuous in a compact region $R$, then $\exists M \ge 0$ such that $\vert f(z) \vert \le M, \forall z \in R$, where equality holds for at least one such $z$.