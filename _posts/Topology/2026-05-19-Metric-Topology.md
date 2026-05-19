---
title: Metric Topology
date: 2026-05-19
categories: [Mathematics, Topology]
tags: []
math: true
---

## Theorem 1
Let $(X, d)$ be a metric space. The collection $\mathcal{B} = \\{ B_d(x, \varepsilon) \mid x \in X, \varepsilon > 0 \\}$ is a basis for a topology on $X$, called ***the metric topology induced by $d$.***

> A function $d : X \times X \to \mathbb{R}$ is said to be a ***metric*** on $X$ if it satisfies the following conditions:
> 1. $d(x, y) \geq 0, \forall x, y \in X$, and $d(x, y) = 0$ if and only if $x = y$.
> 2. $d(x, y) = d(y, x), \forall x, y \in X$.
> 3. $d(x, z) \leq d(x, y) + d(y, z), \forall x, y, z \in X$.
{: .prompt-info .no-icon }

