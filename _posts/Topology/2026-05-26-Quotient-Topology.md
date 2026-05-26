--- 
title: Quotient Topology
date: 2026-05-26
categories: [Mathematics, Topology]
tags: []
math: true
---

## Definition 1
Let $X$ and $Y$ be topological spaces, and let $p: X \to Y$ be a surjective map. The map $p$ is said to be a ***quotient map*** if 

$$U \text{ is open in } Y \iff p^{-1}(U) \text{ is open in } X.$$

[연속함수](<{% post_url Topology/2026-04-29-Continuous-Functions %}#definition>)가 $(\Longrightarrow)$ 방향에 대해서만 정의되는 반면, quotient map은 양방향 모두 성립하면서 surjective인 함수로 정의된다. 

---
## Remark
**(i)** Every quotient map is continuous.

**(ii)** An equivalent condition is to require that 

$$C \text{ is closed in } Y \iff p^{-1}(C) \text{ is closed in } X.$$

**(iii)** Every surjective, continuous, open (or closed) map is a quotient map. However, the converse does not hold. In particular, there is a quotient map that is not an open map.

$\big[(\because)$ 

$\big]$
---
## Theorem
Let $X$ be a topological space and let $A$ be a set. Let $p: X \to A$ be a surjective map. Then the collection 

$$\mathscr{T}_p$$