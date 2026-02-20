--- 
title: Two Dimensional Maps
date: 2026-02-20 15:00:00 +0900
categories: [Mathematics, Dynamics]
tags: []
math: true
---

## Definition
Let $f$ be a map on $\mathbb{R}^m$, and let $p \in \mathbb{R}^m$ be a fixed point of $f$. 
- We call $p$ a ***sink*** or ***attracting fixed point*** if $\exists \varepsilon > 0$ such that $\lim_{k\to\infty} f^k(v) = p, \forall v \in N_\varepsilon(p).$
- We call $p$ a ***source*** or ***repeller*** if $\exists \varepsilon > 0$ such that for each $v \in N_\varepsilon(p)$ except for $p$, $\exists N \in \mathbb{N}$ such that $f^N(v) \notin N_\varepsilon(p)$.