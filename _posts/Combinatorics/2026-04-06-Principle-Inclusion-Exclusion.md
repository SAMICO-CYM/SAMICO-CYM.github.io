---
title: Principle of Inclusion-Exclusion
date: 2026-04-06
categories: [Mathematics, Combinatorics]
tags: []
math: true
---

## Theorem
For $A_1, ..., A_d \subset X$, 

$$\left\vert \bigcup_{i=1}^d A_i \right\vert = \sum_{k=1}^d (-1)^{k-1} \sum_{I \in \binom{[d]}{k}} \left\vert \bigcap_{i \in I} A_i \right\vert.$$

### Proof