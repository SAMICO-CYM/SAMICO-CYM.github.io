---
title: "Separation Axioms"
date: 2026-04-23
categories: [Mathematics, Topology]
tags: []
math: true
---

## Definition
Let $(X, \mathcal{T})$ be a topological space. Let $x, y \in X$ with $x \neq y$, and let $C, D$ be closed subsets of $X$ with $C \cap D = \emptyset, x \notin C$. Then $X$ is called a

**(i)** ***$T_0$-space*** if $\exists U \in \mathcal{T}$ such that $x \in U$ and $y \notin U$.

**(ii)** ***$T_1$-space*** if $\exists U, V \in \mathcal{T}$ such that $x \in U, y \notin U, y \in V, x \notin V$.

**(iii)** ***$T_2$-space*** or ***Hausdorff space*** if $\exists U, V \in \mathcal{T}$ such that $x \in U, y \in V$ and $U \cap V = \emptyset$.

**(iv)** ***regular space*** if $\exists U, V \in \mathcal{T}$ such that $x \in U, C \subset V$ and $U \cap V = \emptyset$.

**(v)** ***$T_3$-space*** or ***regular Hausdorff*** if $X$ is regular and $T_1$.

**(vi)** ***normal space*** if $\exists U, V \in \mathcal{T}$ such that $C \subset U, D \subset V$ and $U \cap V = \emptyset$.

**(vii)** ***$T_4$-space*** or ***normal Hausdorff*** if $X$ is normal and $T_1$.