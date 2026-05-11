--- 
title: De Bruijn Graph
date: 2026-05-11
categories: [Mathematics, Graph Theory]
tags: []
math: true
---

## Definition
For each $k \ge 2$, the ***De Bruijn graph*** $D_k$ is a digraph having $V(D_k) = \\{ 0, 1 \\}^{k-1}$ and edges defined by 

$$(a_1, a_2, \cdots, a_{k-1}) \to (a_2, a_3, \cdots, a_k), \forall (a_1, \cdots, a_k) \in \\{ 0, 1 \\}^k.$$

We refer to the edge $(a_1, a_2, \cdots, a_{k-1}) \to (a_2, a_3, \cdots, a_k)$ as $a_1a_2\cdots a_k.$