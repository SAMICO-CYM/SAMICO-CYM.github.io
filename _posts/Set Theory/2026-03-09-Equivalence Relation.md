---
title: Equivalence Relation
date: 2026-03-09 00:01:28
categories: [Mathematics, Set Theory]
tags: []
math: true
---

## Definition
Let $R$ be a relation in a set $X$.

**(i)** $R$ is an ***equivalence relation*** $\iff$ $R$ is reflexive, symmetric, and transitive. 

**(ii)** Let $x \in X$. Then the equivalence class of $x$ is 

$$R[x] = \{ y \in X \mid xRy \}.$$

The set of all equivalence classes of $R$ is called the ***quotient set*** of $X$ by $R$, and denoted by $X/R$.

## Theorem 1
Let $R$ be an equivalence relation on a set $X$.

**(i)** $\forall x \in X, x \in R[x]$.

**(ii)** $\forall x, y \in X, xRy \iff R[x] = R[y]$.

**(iii)** $\forall x, y \in X, (x, y) \notin R \iff R[x] \cap R[y] = \emptyset$.

### Proof
$\blacksquare$

## Theorem 2
Let $R$ be an equivalence relation on a set $X$. Then $X/R$ is a partition of $X$.

### Proof
$\blacksquare$

## Theorem 3
Let $P$ be a partition of a nonempty set $X$. Then there exists an equivalence relation $R$ on $X$ such that $X/R = P$.

### Proof
$\blacksquare$