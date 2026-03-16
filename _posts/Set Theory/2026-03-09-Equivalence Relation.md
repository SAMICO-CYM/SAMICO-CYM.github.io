---
title: Equivalence Relation
date: 2026-03-09 00:01:29
categories: [Mathematics, Set Theory]
tags: []
math: true
---

## Definition
Let $R$ be a relation in a set $X$. Then we say that 

**(i)** $R$ is ***reflexive*** $\iff$ $xRx, \forall x \in X$.

**(ii)** $R$ is ***symmetric*** $\iff$ $xRy \Longrightarrow yRx, \forall x, y \in X$.

**(iii)** $R$ is ***transitive*** $\iff$ $xRy \wedge yRz \Longrightarrow xRz, \forall x, y, z \in X$. 

**(iv)** $R$ is ***antisymmetric*** $\iff$ $xRy \wedge yRx \implies x = y$.
 
**(iv)** $R$ is an ***equivalence relation*** $\iff$ $R$ is reflexive, symmetric, and transitive. 

## Theorem
Let $R$ be a relation on $X$. 

**(i)** $R$ is reflexive $\iff$ $\triangle_X \subset R$

**(ii)** $R$ is symmetric $\iff$ $R = R^{-1}$

**(iii)** $R$ is antisymmetric $\iff$ $R \cap R^{-1} = \triangle_X$

**(iv)** $R$ is transitive $\iff$ $R \circ R = R$

### Proof
$\blacksquare$