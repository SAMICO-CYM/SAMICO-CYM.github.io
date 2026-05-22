--- 
title: Convergence of Power Series
date: 2026-05-23
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Theorem 1
If a power series 

$$\sum_{n=0}^\infty a_n(z-z_0)^n$$

converges when $z = z_1 (z_1 \neq z_0)$, then it is absolutely convergent at each point $z$ in the open disk $\vert z - z_0 \vert < R_1$ where $R_1 = \vert z_1 - z_0 \vert$. 

Furthermore, the greatest circle centered at $z_0$ such that the above series converges at each point inside is called the ***circle of convergence*** of the series.

### Proof
Since the series 

$$\sum_{n=0}^\infty a_n(z_1 - z_0)^n$$

converges, the sequence $\\{ a_n(z_1 - z_0)^n \\}$ is bounded, that is, 

$$\vert a_n(z_1 - z_0)^n \vert \le M, \forall n \in \{ 0, 1, 2, \cdots \}$$

for some $M > 0$. 

Let $z$ be a point in the open disk $\vert z - z_0 \vert < R_1$, and let 

$$\rho = \frac{\vert z - z_0 \vert}{ \vert z_1 - z_0 \vert}.$$

Note that $\rho < 1$. Then we have 

$$\begin{align*}
\vert a_n(z-z_0)^n \vert &= \vert a_n(z_1 - z_0)^n \vert \left( \frac{\vert z - z_0 \vert}{\vert z_1 - z_0 \vert} \right)^n \\
& \le M \rho^n
\end{align*}$$

for each $n = 0, 1, 2, \cdots.$ Since $\rho < 1$, the series

$$\sum_{n=0}^\infty M \rho^n$$

converges. By the comparison test, we conclude that 

$$\sum_{n=0}^\infty \vert a_n(z-z_0)^n \vert$$

converges, which means that the given power series converges absolutely. $\blacksquare$

---
## Definition
Let 

$$S(z) = \sum_{n=0}^\infty a_n(z-z_0)^n$$

be a power series, and let 

$$S_k(z) = \sum_{n=0}^k a_n(z-z_0)^n$$

be the partial sums of the power series. Let $\rho_k(z) := S(z) - S_k(z)$ for each $k = 0, 1, 2, \cdots.$

The series $S(z)$ is said to be ***uniformly convergent*** in some region $E$ if 

$$\forall \varepsilon > 0, \exists N \in \mathbb{N} \text{ such that } \vert \rho_k(z) \vert < \varepsilon, \forall k \ge N \text{ whenever } z \in E.$$

위 정의에서는 구체적으로 region $E$의 정체를 밝히지 않았다. 실제로 $E$는 아래 정리와 같이 찾을 수 있음을 알 수 있다.

---
## Theorem 2
Let 

$$\sum_{n=0}^\infty a_n(z-z_0)^n$$

be a power series with the circle of convergence $\vert z - z_0 \vert = R$, and let $z_1$ be a point inside the circle of convergence. Then the series must be uniformly convergent in the closed disk $\vert z- z_0 \vert \le R_1$, where $R_1 = \vert z_1 - z_0 \vert$. 

### Proof
