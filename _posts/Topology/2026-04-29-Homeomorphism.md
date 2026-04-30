--- 
title: Homeomorphism
date: 2026-04-29
categories: [Mathematics, Topology]
tags: []
math: true
---

## Definition 1
Let $(X, \mathcal{T}_X)$ and $(Y, \mathcal{T}_Y)$ be topological spaces. 

**(i)** A function $f: X \to Y$ is called a ***homeomorphism*** if $f$ is bijective and both $f$ and $f^{-1}$ are continuous. If such a function exists, then we say that $X$ and $Y$ are ***homeomorphic***, denoted by $X \cong Y$. 

**(ii)** Suppose that $X \cong Y$. A property $P$ of $X$ is called a ***topological property*** if $Y$ also possesses $P$ as well. 

**(iii)** Let $f: X \to Y$ be an injective continuous function. If $X \cong f(X)$, where $f(X)$ is a subspace of $Y$, then $f$ is called an ***embedding*** of $X$ in $Y$. 

---
## Remark
**(i)** $f: X \to Y$ is a homeomorphism $\iff$ $[f(U) \in \mathcal{T}_Y \iff U \in \mathcal{T}_X]$. 

---
## Theorem 1
Let $(X, \mathcal{T}_X)$ and $(Y, \mathcal{T}_Y)$ be topological spaces, and let $f: X \to Y$ be a homeomorphism. If $\mathcal{B}$ is a basis for $\mathcal{T}_X$, then $f(\mathcal{B})$ is a basis for $\mathcal{T}_Y$. 

### Proof
Since each $B$ in $\mathcal{B}$ is open in $X$, each $f(B)$ is open in $Y$, which means that $f(\mathcal{B}) \subset \mathcal{T}_Y$.

Let $V \in \mathcal{T}_Y$ and let $y \in V$. Since $f$ is continuous, $f^{-1}(V) \in \mathcal{T}_X$. Since $f$ is surjective, $y = f(x)$ for some $x \in X$. Then $x \in f^{-1}(V)$, and $x \in B \subset f^{-1}(V)$ for some $B \in \mathcal{B}$. Then $y = f(x) \in f(B) \subset f(f^{-1}(V)) = V$. Thus, [$f(\mathcal{B})$ is a basis for $\mathcal{T}_Y$.](<{% post_url Topology/2026-03-17-Basis-Of-Topology %}#theorem-3>) $\blacksquare$