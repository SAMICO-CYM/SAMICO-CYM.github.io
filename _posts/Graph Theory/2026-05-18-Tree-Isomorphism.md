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
## Remark
Each label has the same number of $0$s as $1$s and the same is not true of any nontrivial initial sublabel.

---
## Theorem
For planted trees $T$ and $T'$, $A(T) = A(T') \iff T \cong T'$, that is, a given code uniquely determines the planted tree up to isomorphisms.

### Proof
If $T \cong T'$, then clearly $A(T) = A(T')$. 

Conversely, we first proceed by induction on $n$, the number of vertices of $T$, to show that a given code $A(T)$ of the planted tree $T$ uniquely determines $T$ up to isomorphisms.

The basic case $n=1$ gives us that $A(T) = 01$ and $T$ is the planted tree with a single vertex.

Suppose that for a given code of length greater than $2$ and less than $2n$, it corresponds to a unique planted tree up to isomorphisms. Let $C$ be a code of length $2n$ of a planted tree $(T, r, \nu)$. Then $C$ must be written as $C = 0L_1 \cdots L_t 1$ where each $L_i$ is a code of a planted tree $T_i$ with a root $r_i$ and $t$ is the number of children of $r$. We claim that the decomposition $C = 0L_1 \cdots L_t 1$ is unique. 

$\big[(\because)$ Since each $L_i$ is a code of a planted tree, it has the same number of $0$s as $1$s, and the same is not true of any non-trivial initial sublabel of $L_i$. Therefore, if we read the inner sublabel $L_1 \cdots L_t$ from left to right, the first sublabel $L_1$ must terminate exactly at the first position $j$ such that the sublabel $s_1 \cdots s_j$ of $L_i$ has the same number of $0$s as $1$s. This uniquely determines $L_1$. Applying this argument repeatedly to the remaining sublabel uniquely determines $L_2, \dots, L_t$ in sequence. Thus, the decomposition $C = 0L_1 \cdots L_t 1$ is unique.$\big]$ 

By the inductive hypothesis, each $T_i$ is uniquely determined up to isomorphism by $L_i$. Suppose $T'$ is another planted tree with $A(T') = C$. By the unique decomposition proven above, $T'$ also has a root $r'$ with $t$ children, and the codes of its subtrees $T'_i$ are exactly $L_1, \dots, L_t$. Thus, by the inductive hypothesis, there exists a rooted tree isomorphism $\phi_i : V(T_i) \to V(T'_i)$ for each $i = 1, \dots, t$.We construct a mapping $\Phi : V(T) \to V(T')$ by setting $\Phi(r) = r'$ and $\Phi(v) = \phi_i(v)$ for all $v \in V(T_i)$. Since each $\phi_i$ is an isomorphism and we preserve the corresponding linear ordering of $\nu$ and $\nu'$ for the children, $\Phi$ perfectly preserves the adjacency, the roots, and the left-to-right orderings. Thus, $\Phi$ is a planted tree isomorphism between $(T, r, \nu)$ and $(T', r', \nu')$. Consequently, the code uniquely determines the planted tree up to isomorphisms. $\blacksquare$