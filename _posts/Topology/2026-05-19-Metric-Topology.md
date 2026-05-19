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
> The $\varepsilon$-ball centered at $x$ is defined by $B_d(x, \varepsilon) = \{ y \in X \mid d(x, y) < \varepsilon \}$.
{: .prompt-info .no-icon }

### Proof

---
## Remark
A set $U$ is open in the metric topology induced by $d$ $\iff$ $\forall x \in U, \exists \delta > 0$ such that $B_d(x, \delta) \subset U$.

---
## Definition
Let $X$ be a topological space.

**(i)** $X$ is said to be ***metrizable*** if there exists a metric $d: X \times X \to \mathbb{R}$ that induces the topology of $X$. 

**(ii)** Let $\mathcal{T}_d$ be the metric topology induced by $d$. We call $(X, \mathcal{T}_d)$ a ***metric space***.

---
## Theorem 2
Let $d, d'$ be two metrics on a set $X, and let $\mathcal{T}_d, \mathcal{T}_{d'}$ be two topologies induced by $d, d'$, respectively. Then $\mathcal{T}_{d'}$ is finer than $\mathcal{T}_d$ $\iff$ $\forall x \in X$ and $\forall \varepsilon > 0$, $\exists \delta > 0$ such that $B_{d'}(x, \delta) \subset B_d(x, \varepsilon)$.

### Proof

---
## Corollary
Let $d, d', d''$ be the Euclidean metric, the taxicab metric, and the square metric, respectively, on $\mathbb{R}^n$. Then $\mathcal{T}_d = \mathcal{T}_{d'} = \mathcal{T}_{d''}$.

### Proof


<style>
/* 아이콘 숨기기 및 아이콘이 있던 왼쪽 빈 여백 줄이기 */
.no-icon {
  padding-left: 1rem !important; 
}
.no-icon::before {
  display: none !important; 
}
</style>