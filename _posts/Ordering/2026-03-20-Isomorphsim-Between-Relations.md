---
title: Isomorphism Between Relations
date: 2026-03-20
categories: [Mathematics, Ordering]
tags: []
math: true
---

## Definition
Let $(X, \le)$ and $(X', \le')$ be [posets](<{% post_url Ordering/2026-03-15-Order %}>). We say that $(X, \le)$ and $(X', \le')$ are ***isomorphic*** if there exists a [bijection](<{% post_url Set Theory/2026-03-09-Function %}#definition-2>) $\phi: X \to X'$ satisfying that for any $x, y \in X$,

$$x \le y \iff \phi(x) \le' \phi(y).$$ In this case, the function $\phi$ is called an ***isomorphism*** from $(X, \le)$ to $(X', \le')$.

---

## Theorem
Let $n \in \mathbb{N}$. Then the [boolean lattice](<{% post_url Ordering/2026-03-20-Boolean-Lattice %}>) $\mathcal{B}_n = (B_n, \prec)$ and the poset $(2^{[n]}, \le)$ are isomorphic.

## Proof
For each $a = (a_1, ..., a_n) \in B_n = \\{ 0, 1 \\}^n$, define a function $\phi: B_n \to 2^n$ by 

$$\phi(a) = \\{ i \\in \\{ 1, ..., n \\} \\mid a_i = 1 \\}.$$ 

Then $\phi$ is clearly well-defined and bijective. 

Let $a, b \in B_n$. Then clearly we have $a \prec b \iff \phi(a) \le \phi(b)$. Thus $\mathcal{B}_n$ and $(2^{[n]}, \le)$ are isomorphic. $\blacksquare$