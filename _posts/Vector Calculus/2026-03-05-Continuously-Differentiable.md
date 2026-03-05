--- 
title: Class $C^1$ Functions
date: 2026-03-05
categories: [Mathematics, Vector Calculus]
tags: []
math: true
---

## Theorem 1
Let $E \subset \mathbb{R}^n$ be a [convex]({% post_url 2026-03-05-Convexity %}#Definition) open set, and let $\mathbf{f} : E \to \mathbb{R}^m$ be a differentiable map in $E$.
Suppose that $\exists M \in \mathbb{R}$ such that 

$$\| \mathbf{f}'(\mathbf{x}) \| \le M, \forall \mathbf{x} \in E.$$

Then 

$$\| \mathbf{f}(\mathbf{b}) - \mathbf{f}(\mathbf{a}) \| \le M \| \mathbf{b} - \mathbf{a} \|, \quad \forall \mathbf{a}, \mathbf{b} \in E.$$

### Proof
$\blacksquare$

## Corollary
If $\mathbf{f}'(\mathbf{x}) = \mathbf{0}, \forall \mathbf{x} \in E$, then $\mathbf{f}$ is constant.

### Proof
$\blacksquare$

## Definition 1
**(i)** A differentiable mapping $\mathbf{f}$ of an open set $E \subset \mathbb{R}^n$ into $\mathbb{R}^m$ is said to be ***continuously differentiable*** in $E$ if $\mathbf{f}'$ is a continuous mapping of $E$ into $\mathcal{L}(\mathbb{R}^n, \mathbb{R}^m)$. More explicitly, it is required that to every $\mathbf{x} \in E$ and to every $\varepsilon > 0$ corresponds a $\delta > 0$ such that $$||\mathbf{f}'(\mathbf{y}) - \mathbf{f}'(\mathbf{x})|| < \varepsilon$$ if $\mathbf{y} \in E$ and $\| \mathbf{x} - \mathbf{y} \| < \delta$. 
\
If $\mathbf{f}$ is cotinuously diffenrentiable in $E$, then we also say that $\mathbf{f}$ is a $C^1$-mapping, or $\mathbf{f}$ is of class $C^1$, and denoted by $\mathbf{f} \in C^1(E)$.

**(ii)** If the partial derivatives of the functions $f_i$ of order less than or equal to $r$ exist and are continuous on $E$, we say that $\mathbf{f}$ is ***of class $C^r$*** on $E$. (The function $\mathbf{f}$ is of class $C^r$ on $E$ $\iff$ each $D_j f_i$ is of class $C^{r-1}$ on $E$.)

(iii) We say that $\mathbf{f}$ is ***of class $C^{\infty}$*** on $E$ if the partial derivatives of $f_i$ of all orders exist and are continuous on $E$

## Theorem 2
Let $E \subset \mathbb{R}^n$ be open, and let $\mathbf{f} : E \to \mathbb{R}^m$. Then $\mathbf{f} \in C^1(E)$ $\iff$ the partial derivatives $D_j f_i$ exist and are continuous on $E$ for $1 \le i \le m$, $1 \le j \le n$.

### Proof
$\blacksquare$

## Lemma
Suppose $f$ is defined in an open set $E \subset R^2$, and $D_1f$ and $D_{21}f$ exist at every point of $E$. Suppose $Q \subset E$ is a closed rectangle with sides parallel to the coordinate axes, having $(a, b)$ and $(a + h, b + k)$ as opposite vertices ($h \ne 0, k \ne 0$). Put 

$$\Delta(f, Q) = f(a + h, b + k) - f(a + h, b) - f(a, b + k) + f(a, b).$$

Then there is a point $(x, y)$ in the interior of $Q$ such that 

$$\Delta(f, Q) = hk(D_{21}f)(x, y).$$


## Theorem 3
Suppose $f$ is defined in an open set $E \subset R^2$, suppose that $D_1f$, $D_{21}f$, and $D_2f$ exist at every point of $E$, and $D_{21}f$ is continuous at some point $(a, b) \in E$. Then $D_{12}f$ exists at $(a, b)$ and 

$$(D_{12}f)(a, b) = (D_{21}f)(a, b).$$

## Corollary
$D_{21}f = D_{12}f$ if $f \in C^2(E)$.