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

## Definition 2
A saddle with at least one negative eigenvalue is sometimes called a ***flip saddle***. Otherwise it is a ***regular saddle***. For a flip saddle, successive images flip from one side of the origin to the other along the line. 

## Example

Consider the map 

$$f(x,y) = \begin{bmatrix} \frac{x}{2} \\ 2y - 7x^2 \end{bmatrix}.$$

The fixed point is $\mathbf{0} = (0,0)$. Since $$D \mathbf{f}(\mathbf{0}) = \begin{bmatrix} \frac{1}{2} & 0 \\ 0 & 2 \end{bmatrix}$$ has eigenvalues $\lambda\_1 = \frac{1}{2}$ and $\lambda\_2 = 2$, the fixed point is a saddle point. 

Clearly $\mathbf{f}^n(\mathbf{0}) = \mathbf{0}$ for all $n \in \mathbb{N}$. Let $\mathbf{v} = (x, y)$. Then we can show that 

$$f^n(\mathbf{v}) = \begin{bmatrix} \frac{x}{2^n} \\ 2^ny - 7 \cdot 2^{n+2} \left( \sum_{k=1}^n 2^{-3k} \right) x^2 \end{bmatrix}.$$ 

For $\mathbf{v} \in S(\mathbf{0})$, we have $\mathbf{v} = (x, 4x^2)$ for arbitrary $x \in \mathbb{R}$. Thus $S(\mathbf{0}) = \\{(x, 4x^2) \mid x \in \mathbb{R}\\}$.  

Similarly, $U(\mathbf{0}) = \\{ (0, y) \mid y \in \mathbb{R} \\}.$

## Remark
- When a map is linear, the stable and unstable manifolds of a saddle are always linear subspaces. 
- The stable and unstable manifolds of saddles in the plane are always one-dimensional sets: lines or curves.

## Definition 3
If $\mathbf{p}$ is a fixed or periodic point, and if $\mathbf{h}\_0 \neq \mathbf{p}$ is a point of intersection of the stable and unstable manifold of $\mathbf{p}$, then $\mathbf{h}\_0$ is called a ***homoclinic point***. 

## Remark
- An intersection of the stable and unstable manifolds of a single fixed point immediately forces infinitely many such intersections. First notice that a stable manifold, by definition, is an ***invariant set*** under the map $\mathbf{f}$. This means that if $\mathbf{h}\_0$ is a point on the stable manifold of a fixed point $\mathbf{p}$, then so are $\mathbf{h}\_1 = \mathbf{f}(\mathbf{h}\_0)$ and $\mathbf{h}\_{-1} = \mathbf{f}^{-1}(\mathbf{h}\_0)$. By the same reasoning, the unstable manifold of a fixed point is also invariant. 
- Once a point like $\mathbf{h}\_0$ lies on both the stable and unstable manifolds of a fixed point, then the entire orbit of $\mathbf{h}\_0$ must lie on both manifolds, because both manifolds are invariant. Remember that the stable manifold is directed toward the fixed point, and the unstable manifold leads away from it.