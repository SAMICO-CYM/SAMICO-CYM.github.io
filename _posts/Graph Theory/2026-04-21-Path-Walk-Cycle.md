---
title: Path, Walk, and Cycle
date: 2026-04-21
categories: [Mathematics, Graph Theory]
tags: []
math: true
---

## Definition
Let $G$ be a graph, and let $v_1, v_2, ..., v_n \in V(G)$.

**(i)** A ***path*** of length $\ell$ in $G$ is a subgraph that is isomorphic to $P_\ell$. It is a sequence of distinct vertices $v_1, v_2, ..., v_\ell$ of $G$ such that $\\{ v_{i}, v_{i+1} \\} \in E(G), \forall i \in [\ell]$, and it is called a path from $v_1$ to $v_\ell$. 

**(ii)** A ***walk*** between $v_1$ and $v_n$ in $G$ is a sequence of not necessarily distinct vertices $v_1, v_2, ..., v_n$ such that $\\{ v_{i}, v_{i+1} \\} \in E(G), \forall i \in [n]$.

**(iii)** A ***cycle*** in $G$ is a subgraph isomorphic to $k$-cycle $C_k$ for some $k \le \vert V(G) \vert$.

**(iv)** The ***distance*** between two vertices $u$ and $v$ in $G$, denoted by $d_G(u, v)$, is the length of the shortest $uv$-path in $G$. If $u$ and $v$ are not connected in $G$, we write $d_G(u, v) = \infty$.

---

## Remark

**(i)** For any graph, there are infinitely many walks between two vertices.

---

## Theorem 1
If a graph contains a $uv$-walk, then it contains a $uv$-path.

### Proof
Suppose that a graph $G$ have a $uv$-walk. Then it has a shortest $uv$-walk, say $W = (v_1, v_2, ..., v_n)$, where $v_1 = u$ and $v_n = v$. If $W$ is a path, then we are done. Suppose that $W$ is not a path, that is, there is some repeated vertex $v_i$ in $W$. Let $j$ be the first index for which there is $i < j < n$ such that $v_i = v_j$. Then we have a $uv$-walk $W' = (v_1,v_2,...,v_i,v_{j+1},...,v_n)$ of length $j - i + n - j = n - (j - i) < n$. This contradicts the assumption that $W$ is the shortest $uv$-walk. Therefore, $W$ must be a path. $\blacksquare$

---

## Theorem
The number of $k$-cycles in a graph $G$ with $\vert V(G) \vert = n$ is 

$$\binom{n}{k} \frac{(k-1)!}{2}.$$

### Proof
By choosing the $k$ vertices and arrange them in order, we have 

$$\binom{n}{k} k!.$$

Since the cycle does not depend on the starting vertex and the direction of the cycle, we should divide by $2k$. Thus, we obtain 

$$\binom{n}{k} \frac{k!}{2k} = \binom{n}{k} \frac{(k-1)!}{2}. \blacksquare$$ 

---

## Corollary
The number of $k$-cycles in $K_n$ is given by 

$$\sum_{i=3}^n \binom{n}{i} \frac{(i-1)!}{2}.$$