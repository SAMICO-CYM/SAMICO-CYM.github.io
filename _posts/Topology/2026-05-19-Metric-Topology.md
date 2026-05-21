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
> The $\varepsilon$-ball centered at $x$ is defined by $B_d(x, \varepsilon) = \\{ y \in X \mid d(x, y) < \varepsilon \\}$.
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
The following give the metrics on $\mathbb{R}^n$:

**(i)** ***The Euclidean metric***: $\displaystyle d(x, y) = \sqrt{\sum_{i=1}^n (x_i - y_i)^2}$.

**(ii)** ***The discrete metric***: 

$$d(x, y) = \begin{cases}
1 & \text{if } x = y \\
0 & \text{if } x \neq y.
\end{cases}$$

**(iii)** ***The taxicab metric***: $\displaystyle d(x, y) = \sum_{i=1}^n \vert x_i - y_i \vert$.

**(iv)** ***The square metric***: $\displaystyle d(x, y) = \max _{1 \le i \le n} \\{ \vert x_i - y_i \vert \\}$.

---
## Definition
Let $X$ be a topological space.

**(i)** $X$ is said to be ***metrizable*** if there exists a metric $d: X \times X \to \mathbb{R}$ that induces the topology of $X$. 

**(ii)** Let $\mathcal{T}_d$ be the metric topology induced by $d$. We call $(X, \mathcal{T}_d)$ a ***metric space***.

---
## Theorem 2
Let $d, d'$ be two metrics on a set $X$, and let $\mathcal{T} _d, \mathcal{T} _{d'}$ be two topologies induced by $d, d'$, respectively. Then $\mathcal{T} _{d'}$ is finer than $\mathcal{T} _d$ $\iff$ $\forall x \in X$ and $\forall \varepsilon > 0$, $\exists \delta > 0$ such that $B _{d'}(x, \delta) \subset B _d(x, \varepsilon)$.

### Proof
$(\Longrightarrow)$

Suppose that $\mathcal{T} _{d} \subset \mathcal{T} _{d'}$. Let $x \in X$ and $\varepsilon > 0$. Since $B _d(x, \varepsilon)$ is a basis element of $\mathcal{T} _{d}$, [there exists a basis element $B'$ of $\mathcal{T} _{d'}$ such that $x \in B' \subset B _d(x, \varepsilon)$.](<{% post_url Topology/2026-03-17-Basis-Of-Topology %}#theorem-4>) Then $B' = B _{d'}(x, \delta)$ for some $\delta > 0$. Thus, we have $B _{d'}(x, \delta) \subset B _d(x, \varepsilon)$.

$(\Longleftarrow)$

Suppose that $\forall x \in X$ and $\forall \varepsilon > 0$, $\exists \delta > 0$ such that $B _{d'}(x, \delta) \subset B _d(x, \varepsilon)$. Let $B$ be a basis element of $\mathcal{T} _{d}$. Then $B = B _{d}(x, \varepsilon)$ for some $x \in X$ and $\varepsilon > 0$. By assumption, $\exists \delta > 0$ such that $B _{d'}(x, \delta) \subset B _d(x, \varepsilon)$. Since $B _{d'}(x, \delta)$ is a basis element of $\mathcal{T} _{d'}$ and it contains $x$, we conclude that $\mathcal{T} _{d} \subset \mathcal{T} _{d'}$. $\blacksquare$

---
## Corollary 1
Let $d, d', d''$ be the Euclidean metric, the taxicab metric, and the square metric, respectively, on $\mathbb{R}^n$. Then $\mathcal{T} _d = \mathcal{T} _{d'} = \mathcal{T} _{d''}$. Furthermore, these topologies are the same as the usual topology of $\mathbb{R}^n$.

### Proof
Let $x \in \mathbb{R}^n$ and $\varepsilon > 0$.

**(i)** $\mathcal{T} _d \subset \mathcal{T} _{d'}$

We claim that $B _{d'}(x, \varepsilon) \subset B _{d}(x, \varepsilon)$.

To verify this, let $y \in B _{d'}(x, \varepsilon)$. Then we have

$$d(x, y) = \sqrt{\sum_{i=1}^n (x_i - y_i)^2} \le \sum_{i=1}^n \vert x_i - y_i \vert = d'(x, y) < \varepsilon,$$ 

so that $y \in B_d(x, \varepsilon)$. Thus, we have $B _{d'}(x, \varepsilon) \subset B _{d}(x, \varepsilon)$, and therefore $\mathcal{T} _d \subset \mathcal{T} _{d'}$ by Theoerm 2.

**(ii)** $\mathcal{T} _{d'} \subset \mathcal{T} _{d''}$

Take $\delta = \frac{\varepsilon}{n}$. We claim that $B _{d''}(x, \delta) \subset B _{d'}(x, \varepsilon)$.

To verify this, let $y \in B _{d''}(x, \delta)$. Then we have

$$\vert x_i - y_i \vert \le \max_{1 \le i \le n} \vert x_i - y_i \vert < \delta,$$

for all $i = 1, 2, \cdots, n$, which implies that 

$$d'(x, y) = \sum_{i=1}^n \vert x_i - y_i \vert < n \max_{1 \le i \le n} \vert x_i - y_i \vert < n \delta = n \frac{\varepsilon}{n} = \varepsilon.$$

Hence, $y \in B_{d'}(x, \varepsilon)$, so that $B_{d''}(x, \delta) \subset B_{d'}(x, \varepsilon)$. Therefore, $\mathcal{T} _{d'} \subset \mathcal{T} _{d''}$ by Theoerm 2.

**(iii)** $\mathcal{T} _{d''} \subset \mathcal{T} _{d}$

Take $\delta = \frac{\varepsilon}{\sqrt{n}}$. We claim that $B _{d}(x, \delta) \subset B _{d''}(x, \varepsilon)$.

To verify this, let $y \in B _{d}(x, \delta)$. Then we have

$$\vert x_i - y_i \vert \le \sqrt{\sum_{i=1}^n (x_i - y_i)^2} < \delta = \frac{\varepsilon}{\sqrt{n}}$$

for all $i = 1, 2, \cdots, n$, which implies that 

$$d''(x, y) = \max_{1 \le i \le n} \vert x_i - y_i \vert < \sqrt{\sum_{i=1}^n (x_i - y_i)^2} < \delta = \frac{\varepsilon}{\sqrt{n}} < \varepsilon$$

Hence, $y \in B_{d''}(x, \varepsilon)$, so that $B_{d}(x, \delta) \subset B_{d''}(x, \varepsilon)$. Therefore, $\mathcal{T} _{d''} \subset \mathcal{T} _{d}$ by Theoerm 2. 

Thus, we have $\mathcal{T} _d = \mathcal{T} _{d'} = \mathcal{T} _{d''}$. 

To show that these topologies are the same as the usual topology of $\mathbb{R}^n$, it suffices to show for the case $\mathcal{T}_d$. 

Let 

$$B := \prod_{i=1}^n (a_i, b_i)$$

be a basis element of the usual topology of $\mathbb{R}^n$, and let $x \in B$. For each $i = 1, 2, ..., n$, there exists $\varepsilon_i > 0$ such that $x_i \in (x_i - \varepsilon_i, x_i + \varepsilon_i) \subset (a_i, b_i)$. Let $\varepsilon := \min _{1 \le i \le n} \varepsilon_i$. Then we claim that $x \in B_d(x, \varepsilon) \subset B$. 

To see this, let $y \in B_d(x, \varepsilon)$. Then $d(x, y) < \varepsilon$, which means that 

$$\vert x_i - y_i \vert \le \sqrt{\sum_{i=1}^n (x_i-y_i)^2} < \varepsilon \le \varepsilon_i$$

for each $i = 1, 2, ..., n$. Then $y_i \in (x_i - \varepsilon_i, x_i + \varepsilon_i) \subset (a_i, b_i)$ for each $i = 1,2, ..., n$, which implies that $y \in B$. Thus, $x \in B_d(x, \varepsilon) \subset B$, and therefore $\mathcal{T}_d$ is finer than the usual topology.

Conversely, let $B_d(x, \varepsilon)$ be a basis element of $\mathcal{T}_d$, and let $y \in B_d(x, \varepsilon)$. Then $y \in B_d(y, \delta) \subset B_d(x, \varepsilon)$ for some $\delta > 0$. Take 

$$B := \prod_{i=1}^n \left(y_i - \frac{\delta}{\sqrt{n}}, y_i + \frac{\delta}{\sqrt{n}} \right).$$

Then $B$ is open in the usual topology, and $y \in B$. We claim that $y \in B \subset B_d(y, \delta) \subset B_d(x, \varepsilon)$, so that the usual topology is finer than $\mathcal{T}_d$.

To see this, let $z \in B$. Then we have that $z_i \in \left(y_i - \frac{\delta}{\sqrt{n}}, y_i + \frac{\delta}{\sqrt{n}} \right)$, which means that $\vert z_i - y_i \vert < \frac{\delta}{\sqrt{n}}$, for each $i = 1, 2, ..., n$. Then we obtain

$$\begin{align*}
d(z, y) = \sqrt{\sum_{i=1}^n (z_i - y_i)^2} < \sqrt{n\left( \frac{\delta}{\sqrt{n}} \right)^2} = \delta,
\end{align*}$$

so that $z \in B_d(y, \delta)$. Thus, $B \subset B_d(y, \delta)$, and therefore $\mathcal{T}_d$ and the usual topology of $\mathbb{R}^n$ are the same. Hence, all of $\mathcal{T}_d, \mathcal{T}_{d'}, \mathcal{T}_{d''}$ and the usual topology are the same. $\blacksquare$

---
## Corollary 2
Let $d$ be a discrete metric on a set $X$. Then the metric topology induced by $d$ is the discrete topology on $X$.

### Proof
Let $U$ be an open set of the discrete topology on $X$, and let $x \in U$. Note that 

$$B_d(x, \varepsilon) = \begin{cases}
\{ x \} & \text{if } \varepsilon \le 1 \\
X & \text{of } \varepsilon > 1
\end{cases}$$

by the definition of the discrete metric. [Thus, we always have $x \in B_d(x, 1) = \\{ x \\} \subset U$, and therefore, the discrete topology on $X$ is the metric topology induced by $d$.](<{% post_url Topology/2026-03-17-Basis-Of-Topology %}#theorem-3>) $\blacksquare$

---
## Theorem 3
Every metric space is Hausdorff.

### Proof
Let $X$ be a metric space with the metric $d$. Let $x, y \in X$ with $x \neq y$. Then $d(x, y) > 0$. Take $\varepsilon = \frac{1}{2}d(x, y)$. Since

$$B_d(x, \varepsilon) \cap B_d(y, \varepsilon) = \emptyset$$

and each $B_d(x, \varepsilon), B_d(y, \varepsilon)$ is open in $X$, $X$ is Hausdorff. $\blacksquare$

---
## Theorem 4
Let $X, Y$ be metrizble with metrics $d_X, d_Y$, respectively. Let $f: X \to Y$ be a function. Then 

$$f \text{ is continuous } \iff \forall x \in X, \forall \varepsilon > 0, \exists \delta >0 \text{ such that } d_X(x, y) < \delta \implies d_Y(f(x), f(y)) < \varepsilon.$$

### Proof
$(\Longrightarrow)$

Suppose that $f$ is continuous. Let $x \in X$ and $\varepsilon > 0$. Note that $B _{d_Y}(f(x), \varepsilon)$ is open in $Y$ and $f(x) \in B _{d_Y}(f(x), \varepsilon)$. Since $f$ is continuous, there exists a neighborhood $U$ of $x$ such that $f(U) \subset B _{d_Y}(f(x), \varepsilon)$. Since $x \in U$, $x \in B _{d_X}(x, \delta) \subset U$ for some $\delta > 0$. If $y \in B _{d_X}(x, \delta) \subset U$, which implies that $d_X(x, y) < \delta$, then we have $f(y) \in f(U) \subset B _{d_Y}(f(x), \varepsilon)$, so that $d_Y(f(x), f(y)) < \varepsilon$. 

$(\Longleftarrow)$

Suppose that $\forall x \in X, \forall \varepsilon > 0, \exists \delta >0$ such that $d_X(x, y) < \delta \implies d_Y(f(x), f(y)) < \varepsilon.$ 



<style>
/* 아이콘 숨기기 및 아이콘이 있던 왼쪽 빈 여백 줄이기 */
.no-icon {
  padding-left: 1rem !important; 
}
.no-icon::before {
  display: none !important; 
}
</style>