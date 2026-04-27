---
title: Adjacency Matrix
date: 2026-04-27
categories: [Mathematics, Graph Theory]
tags: []
math: true
---

## Definition
Let $G$ be a graph with $V(G) = \{ v_1, ..., v_n \}$. The ***adjacency matrix*** of $G$, denoted by $A_G = [a_{ij}]$, is an $n \times n$ matrix defined by 

$$a_{ij} = \begin{cases} 1 & \text{if } \{ v_i, v_j \} \in E(G) \\ 0 & \text{otherwise} \end{cases}, \forall i, j.$$

---

## Theorem
Let $G$ be a graph, and let $A_G$ be the adjacency matrix of $G$. Then there is a walk of length $\ell$ from $v_i$ to $v_j$ if and only if the $(i, j)$-entry of $A^\ell_G$ is nonzero.