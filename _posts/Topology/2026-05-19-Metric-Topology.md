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
>
> The $\varepsilon$-ball centered at $x$ is defined by $B_d(x, \varepsilon) = \{ y \in X \mid d(x, y) < \varepsilon \}$.
{: .prompt-info .no-icon }

### Proof
Let $x \in X$. Since $d(x, x) = 0$, we have $x \in B_d(x, \varepsilon), \forall \varepsilon > 0$. Thus, there is $B \in \mathcal{B}$ such that $x \in B$.

Let $x \in B_1 \cap B_2$ for some $B_1, B_2 \in \mathcal{B}$. Then $B_1 = B_d(x_1, \delta_1)$ and $B_2 = B_d(x_2, \delta_2)$ for some $x_1, x_2 \in X$ and $\delta_1, \delta_2 > 0$. Then we see that $x \in B_d(x_1, \delta_1)$ and $x \in B_d(x_2, \delta_2)$, which means that $d(x, x_1) < \delta_1$ and $d(x, x_2) < \delta_2$. Let $\delta = \min \{ \delta_1 - d(x, x_1), \delta_2 - d(x, x_2) \}$. Clearly $\delta > 0$. Then we must have $x \in B_d(x, \delta) \subset B_1 \cap B_2$.

To see this, let $y \in B_d(x, \delta)$. Then $d(x, y) < \delta$, so that $d(x, y) < \delta_1 - d(x, x_1)$ and $d(x, y) < \delta_2 - d(x, x_2)$. Thus, we have 

$$d(y, x_1) \le d(y, x) + d(x, x_1) < \delta_1 \quad \text{and} \quad d(y, x_2) \le d(y, x) + d(x, x_2) < \delta_2,$$

so that $y \in B_d(x_1, \delta_1) \cap B_d(x_2, \delta_2) = B_1 \cap B_2$. Therefore, $B_d(x, \delta) \subset B_1 \cap B_2$. It follows that $\mathcal{B}$ is a basis for a topology on $X$. $\blacksquare$

---
## Remark
A set $U$ is open in the metric topology induced by $d$ $\iff$ $\forall x \in U, \exists \delta > 0$ such that $B_d(x, \delta) \subset U$.

---
## Example


---
## Definition
Let $X$ be a topological space.

**(i)** $X$ is said to be ***metrizable*** if there exists a metric $d: X \times X \to \mathbb{R}$ that induces the topology of $X$. 

**(ii)** Let $\mathcal{T}_d$ be the metric topology induced by $d$. We call $(X, \mathcal{T}_d)$ a ***metric space***.

---
## Theorem 2
Let $d, d'$ be two metrics on a set $X$, and let $\mathcal{T}_d, \mathcal{T}_{d'}$ be two topologies induced by $d, d'$, respectively. Then $\mathcal{T}_{d'}$ is finer than $\mathcal{T}_d$ $\iff$ $\forall x \in X$ and $\forall \varepsilon > 0$, $\exists \delta > 0$ such that $B_{d'}(x, \delta) \subset B_d(x, \varepsilon)$.

### Proof
$(\Longrightarrow)$

Suppose that $\mathcal{T}_{d} \subset \mathcal{T}_{d'}$. Let $x \in X$ and $\varepsilon > 0$. Since $B_d(x, \varepsilon)$ is a basis element of $\mathcal{T}_{d}$, [there exists a basis element $B'$ of $\mathcal{T}_{d'}$ such that $x \in B' \subset B_d(x, \varepsilon)$.](<{% post_url Topology/2026-03-17-Basis-Of-Topology %}#theorem-4>) Then $B' = B_{d'}(x, \delta)$ for some $\delta > 0$. Thus, we have $B_{d'}(x, \delta) \subset B_d(x, \varepsilon)$.

$(\Longleftarrow)$

Suppose that $\forall x \in X$ and $\forall \varepsilon > 0$, $\exists \delta > 0$ such that $B_{d'}(x, \delta) \subset B_d(x, \varepsilon)$. Let $B$ be a basis element of $\mathcal{T}_{d}$. Then $B = B_{d}(x, \varepsilon)$ for some $x \in X$ and $\varepsilon > 0$. By assumption, $\exists \delta > 0$ such that $B_{d'}(x, \delta) \subset B_d(x, \varepsilon)$. Since $B_{d'}(x, \delta)$ is a basis element of $\mathcal{T}_{d'}$ and it contains $x$, we conclude that $\mathcal{T}_{d} \subset \mathcal{T}_{d'}$. $\blacksquare$

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