--- 
title: Directed Graph
date: 2026-05-11
categories: [Mathematics, Graph Theory]
tags: []
math: true
---

## Definition
**(i)** A ***directed graph***, or ***digraph*** is a pair $(V, E)$, where $V$ is a set of vertices and $E \subseteq V \times V$ is a set of edges. We write $u \to v$ if $(u, v) \in E$. 

**(ii)** For a digraph $G = (V, E)$, the ***symmetrization*** $\mathrm{sym}(G)$ underlying $G$ is a graph $G'$ with vertex set $V(G') = V(G)$ and edge set $E(G') = \\{ \\{ u, v \\} \mid (u, v) \in E(G) \\}$. 

**(iii)** A digraph $G$ is called ***connected*** if $\mathrm{sym}(G)$ is connected.

**(iv)** A ***directed closed Eulerian trail*** in a digraph $G$ is a closed Eulerian trail in $\mathrm{sym}(G)$.

**(v)** A digraph $G$ is called ***Eulerian*** if $\mathrm{sym}(G)$ is Eulerian.

**(vi)** For a digraph $G$, the ***indegree*** of a vertex $v$ is $\mathrm{deg}^+(v) = \vert \\{ u \in G \mid u \to v \\}$ and the ***outdegree*** of a vertex $v$ is $\mathrm{deg}^-(v) = \vert \\{ u \in G \mid v \to u \\}$.

---
## Theorem
Let $G$ be a connected digraph. Then $G$ is Eulerian $\iff \mathrm{deg}^+(v) = \mathrm{deg}^-(v)$ for all $v \in V(G)$.

### Proof

---
