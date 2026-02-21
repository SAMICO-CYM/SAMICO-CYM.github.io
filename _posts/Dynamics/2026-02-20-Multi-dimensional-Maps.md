--- 
title: Multidimensional Maps
date: 2026-02-20 15:00:00 +0900
categories: [Mathematics, Dynamics]
tags: []
math: true
---

## Definition 1
Let $f$ be a map on $\mathbb{R}^m$, and let $p \in \mathbb{R}^m$ be a fixed point of $f$. 
- We call $p$ a ***sink*** or ***attracting fixed point*** if $\exists \varepsilon > 0$ such that $\lim_{k\to\infty} f^k(v) = p, \forall v \in N_\varepsilon(p).$
- We call $p$ a ***source*** or ***repeller*** if $\exists \varepsilon > 0$ such that for each $v \in N_\varepsilon(p)$ except for $p$, $\exists N \in \mathbb{N}$ such that $f^N(v) \notin N_\varepsilon(p)$.

---

## Theorem 1
Let $\mathsf{T}_A$ be a linear map on $\mathbb{R}^m$, and let $\lambda_1, ..., \lambda_m$ be the eigenvalues of $A$. Then
- The origin $\mathbf{0}$ is a sink if $|\lambda_i| < 1, \forall i \in \\{ 1, ..., m \\}$.
- The origin $\mathbf{0}$ is a source if $|\lambda_i| > 1, \forall i \in \\{ 1, ..., m \\}$.

---
## Definition 2
Let $\mathsf{T}_A$ be a linear map on $\mathbb{R}^m$, and let $\lambda_1, ..., \lambda_m$ be the eigenvalues of $A$. 
- We say $A$ is ***hyperbolic*** if $|\lambda_i| \neq 1, \forall i \in \\{ 1, ..., m \\}$. 
- If $A$ is hyperbolic and $|\lambda_i| > 1$ or $|\lambda_i| < 1$ for some $i \in \\{ 1, ..., m \\}$, then the origin $\mathbf{0}$ is called a ***saddle***.

---