--- 
title: Multidimensional NonLinear Maps
date: 2026-02-21 15:00:00 +0900
categories: [Mathematics, Dynamics]
tags: []
math: true
---

## Remark
Let $\mathbf{f}$ be a map on $\mathbb{R}^n$ and let $p \in \mathbb{R}^n$. For a small vector $\mathbf{h}$, the increment in $\mathbf{f}$ due to $\mathbf{h}$ is approximated by the Jacobian $D \mathbf{f}(p)$ times the vector $\mathbf{h}$: $$\mathbf{f}(\mathbf{p} + \mathbf{h}) - \mathbf{f}(\mathbf{p}) \approx D \mathbf{f}(\mathbf{p}) \cdot \mathbf{h}$$ As long as this deviation remains small, the action of the map near $\mathbf{p}$ is essentially the same as the linear map $\mathbf{h} \mapsto A \mathbf{h}$, where $A = D\mathbf{f}(\mathbf{p})$, with fixed point $\mathbf{h} = \mathbf{0}$.


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