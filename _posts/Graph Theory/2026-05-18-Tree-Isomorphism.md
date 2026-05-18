---
title: Tree Isomorphism
date: 2026-05-18
categories: [Mathematics, Graph Theory]
tags: []
math: true
---

## Definition 1
**(i)** A ***rooted tree*** $(T, r)$ is a tree $T$ with a special vertex $r \in V(T)$, called the ***root***. If $\\{ x, y \\} \in E(T)$ is an edge and a vertex $x$ lies on the unique path from $y$ to the root $r$, we say that $x$ is the ***father*** of $y$ and $y$ is the ***child*** of $x$.

**(ii)** A ***planted tree*** $(T, r, \nu)$ is a rooted tree $(T, r)$ with the collection of linear orderings, one linear ordering for the set of children of each vertex. 

**(iii)** Two rooted trees $(T, r)$ and $(T', r')$ are called ***isomorphic*** if there exists an isomorphism $\phi: V(T) \to V(T')$ such that $\phi(r) = r'$.

**(iv)** Two planted trees $(T, r, \nu)$ and $(T', r', \nu')$ are called ***isomorphic*** if there exists a rooted tree isomorphism $\phi: V(T) \to V(T')$ such that for children $a, b$ of a vertex, $a \le_\nu b \iff \phi(a) \le_{\nu'} \phi(b)$.

---

## Definition 2
For each planted tree $(T, r, \nu)$ on $n$ verticies, we define the ***code*** $A(T) \in \\{ 0, 1 \\}^{2n}$ of the tree $T$ recursively as follows:

**(i)** If $v$ is a leaf of $T$, let $L_v = 01$.

**(ii)** For a vertex $v$ with children $a_1 \le_\nu a_2 \le_\nu \cdots \le_\nu a_k$ such that each $a_i$ has a label $L_{a_i}$, let $L_v = 0L_{a_1}L_{a_2}\cdots L_{a_k}1$.

**(iii)** $A(T) = L_r$. 

---
## Theorem
For planted trees $T$ and $T'$, $A(T) = A(T') \iff T \cong T'$.

### Proof
If $T \cong T'$, then clearly $A(T) = A(T')$. 

Conversely, suppose that $A(T) = A(T')$. 

---

## Remark
Each label has the same number of $0$s as $1$s and the same is not true of any nontrivial tnitial sublabel.