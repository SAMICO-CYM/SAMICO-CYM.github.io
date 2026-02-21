--- 
title: Multidimensional NonLinear Maps
date: 2026-02-21 15:00:00 +0900
categories: [Mathematics, Dynamics]
tags: []
math: true
---

## Remark



---

## Theorem 1
Let $\mathbf{f}$ be a map on $\mathbb{R}^n$, and let $\mathbf{p}$ be a fixed point of $\mathbf{f}$. Let $\lambda_1, ..., \lambda_n$ be the eigenvalues of the Jacobian $D\mathbf{f}(p)$ of $\mathbf{f}$ at $\mathbf{p}$.
- $\mathbf{p}$ is a sink if $|\lambda_i| < 1, \forall i \in \\{ 1, ..., n \\}$.
- $\mathbf{p}$ is a source if $|\lambda_i| > 1, \forall i \in \\{ 1, ..., n \\}$.

---

## Definition 1
Let $\mathbf{f}$ be a map on $\mathbb{R}^n$, and let $\mathbf{p}$ be a fixed point of $\mathbf{f}$. Let $\lambda_1, ..., \lambda_n$ be the eigenvalues of the Jacobian $D\mathbf{f}(p)$ of $\mathbf{f}$ at $\mathbf{p}$.
- We say 
$\mathbf{p}$
is ***hyperbolic*** if $|\lambda_i| \neq 1, \forall i \in \\{ 1, ..., m \\}$. 
- If 
$\mathbf{p}$ 
is hyperbolic and $|\lambda_i| > 1$ or $|\lambda_i| < 1$ for some $i \in \\{ 1, ..., m \\}$, then $\mathbf{p}$ is called a ***saddle***. (For a periodic point of period $k$, replace $\mathbf{f}$ by $\mathbf{f}^k$.)