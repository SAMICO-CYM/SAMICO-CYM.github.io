--- 
title: Stable and Unstable Manifold
date: 2026-02-26
categories: [Mathematics, Dynamics]
tags: []
math: true
---

## Definition 1
Let $\mathbf{f}$ be a smooth one-to-one map on $\mathbb{R}^2$, and let $\mathbf{p}$ be a saddle fixed point or periodic saddle point for f. 
- The ***stable manifold*** of $\mathbf{p}$, denoted $S(\mathbf{p})$, is the set of points $\mathbf{v}$ such that 

$$\lim_{n \to \infty} \vert \mathbf{f}^n(\mathbf{v}) - \mathbf{f}^n(\mathbf{p}) \vert = 0.$$

- The ***unstable manifold*** of $\mathbf{p}$, denoted $U(\mathbf{p})$, is the set of points $\mathbf{v}$ such that 

$$\lim_{n \to \infty} \vert \mathbf{f}^{-n}(\mathbf{v}) - \mathbf{f}^{-n}(\mathbf{p}) \vert = 0.$$

## Remark
A saddle with at least one negative eigenvalue is sometimes called a ***flip saddle***. Otherwise it is a ***regular saddle***. For a flip saddle, successive images flip from one side of the origin to the other along the line. 

## Example

Consider the map 

$$f(x,y) = \begin{bmatrix} \frac{x}{2} \\ 2y - 7x^2 \end{bmatrix}.$$

The fixed point is $\mathbf{0} = (0,0)$. Since $$D \mathbf{f}(\mathbf{0}) = \begin{bmatrix} \frac{1}{2} & 0 \\ 0 & 2 \end{bmatrix}$$ has eigenvalues $\lambda_1 = \frac{1}{2}$ and $\lambda_2 = 2$, the fixed point is a saddle point. 

Clearly $\mathbf{f}^n(\mathbf{0}) = \mathbf{0}$ for all $n \in \mathbb{N}$. Let $\mathbf{v} = (x, y)$. Then we can show that 

$$f^n(\mathbf{v}) = \begin{bmatrix} \frac{x}{2^n} \\ 2^ny - 7 \cdot 2^{n+2} \left( \sum_{k=1}^n 2^{-3k} \right) x^2 \end{bmatrix}.$$ For $\mathbf{v} \in S(\mathbf{0})$, we have $\mathbf{v} = (x, 4x^2)$ for arbitrary $x \in \mathbb{R}$. Thus $S(\mathbf{0}) = \{(x, 4x^2) \mid x \in \mathbb{R}\}$.  

Similarly, $U(\mathbf{0}) = \{ (0, y) \mid y \in \mathbb{R} \}.$