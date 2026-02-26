--- 
title: Multidimensional NonLinear Maps
date: 2026-02-21 15:00:00 +0900
categories: [Mathematics, Dynamics]
tags: []
math: true
---

## Remark 1
Let $\mathbf{f}$ be a map on $\mathbb{R}^n$ and let $p \in \mathbb{R}^n$. For a small vector $\mathbf{h}$, the increment in $\mathbf{f}$ due to $\mathbf{h}$ is approximated by the Jacobian $D \mathbf{f}(p)$ times the vector $\mathbf{h}$: 

$$\mathbf{f}(\mathbf{p} + \mathbf{h}) - \mathbf{f}(\mathbf{p}) \approx D \mathbf{f}(\mathbf{p}) \cdot \mathbf{h}$$

 As long as this deviation remains small, the action of the map near $\mathbf{p}$ is essentially the same as the linear map $\mathbf{h} \mapsto A \mathbf{h}$, where $A = D\mathbf{f}(\mathbf{p})$, with fixed point $\mathbf{h} = \mathbf{0}$. Thus we can determines the stability of a map at a fixed point based on the Jacobian matrix at that point. 

---

## Theorem 1
Let $\mathbf{f}$ be a map on $\mathbb{R}^n$, and let $\mathbf{p}$ be a fixed point of $\mathbf{f}$. Let $\lambda_1, ..., \lambda_n$ be the eigenvalues of the Jacobian $D\mathbf{f}(p)$ of $\mathbf{f}$ at $\mathbf{p}$.
- $\mathbf{p}$ is a sink if $\vert\lambda_i\vert < 1, \forall i \in \\{ 1, ..., n \\}$.
- $\mathbf{p}$ is a source if $\vert\lambda_i\vert > 1, \forall i \in \\{ 1, ..., n \\}$.

---

## Definition 1
Let $\mathbf{f}$ be a map on $\mathbb{R}^n$, and let $\mathbf{p}$ be a fixed point of $\mathbf{f}$. Let $\lambda_1, ..., \lambda_n$ be the eigenvalues of the Jacobian $D\mathbf{f}(p)$ of $\mathbf{f}$ at $\mathbf{p}$.
- We say 
$\mathbf{p}$
is ***hyperbolic*** if $\vert\lambda_i\vert \neq 1, \forall i \in \\{ 1, ..., m \\}$. 
- If 
$\mathbf{p}$ 
is hyperbolic and $\vert\lambda_i\vert > 1$ or $\vert\lambda_i\vert < 1$ for some $i \in \\{ 1, ..., m \\}$, then $\mathbf{p}$ is called a ***saddle***. (For a periodic point of period $k$, replace $\mathbf{f}$ by $\mathbf{f}^k$.)

## Remark 2
Let $\mathbf{f}$ be a map on $\mathbb{R}^n$, and let $\\{ \mathbf{p}_1, ..., \mathbf{p}_k \\}$ be a periodic-$k$ orbit. Using the chain rule, 

$$D\mathbf{f}^k(\mathbf{p}_i) = D\mathbf{f}(\mathbf{p}_k) \cdot D\mathbf{f}(\mathbf{p}_{k-1}) \cdots D\mathbf{f}(\mathbf{p}_1), \forall i \in \\{ 1, ..., k \\}.$$ 

This guarantees that the eigenvalues of $D\mathbf{f}^k(\mathbf{p}_i)$ are shared by the periodic orbit, and can be measured by multiplying together the $k$ Jacobian matrices starting at any of the $k$ points.

## Theorem 2
Let $\mathbf{f}$ be a map on $\mathbb{R}^n$, and let $\\{ \mathbf{p}_1, ..., \mathbf{p}_k \\}$ be a periodic-$k$ orbit. Let $\lambda_1, ..., \lambda_n$ be the eigenvalues of $D\mathbf{f}^k(\mathbf{p}_i)$.
- $\\{ \mathbf{p}_1, ..., \mathbf{p}_k \\}$ is a sink if $\vert\lambda_i\vert < 1, \forall i \in \\{ 1, ..., n \\}$.
- $\\{ \mathbf{p}_1, ..., \mathbf{p}_k \\}$ is a source if $\vert\lambda_i\vert > 1, \forall i \in \\{ 1, ..., n \\}$.