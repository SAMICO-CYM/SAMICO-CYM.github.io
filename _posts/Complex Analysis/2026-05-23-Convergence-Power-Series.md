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
Since $R_1 < R$, there are points inside the circle of convergence and farther from $z_0$ than $z_1$ for which the series converges. By Theorem 1, there is a open disk containing $z_1$, lying in the circle of convergence. Thus, the series converges absolutely at $z_1$, i.e., 

$$\sum_{n=0}^\infty \vert a_n(z_1-z_0)^n \vert$$

converges. 

For each point $z$ inside the circle of convergence, we can write the remainders as

$$\begin{align*}
\rho_k(z) = \lim_{m \to \infty} \sum_{n=k}^m a_n(z-z_0)^n
\end{align*}$$

and

$$\sigma_k = \lim_{m \to \infty} \sum_{n=k}^m \vert a_n(z_1 - z_0)^n \vert$$

for each positive integer $k$, respectively. Since $\rho_k(z)$ is defined at each point inside the circle of convergence, the limit converges. Then we have 

$$\vert \rho_k(z) \vert = \lim_{m \to \infty} \left \vert \sum_{n=k}^m a_n(z-z_0)^n \right \vert.$$

Let $z$ be a point in the closed disk $\vert z - z_0 \vert \le R_1$, where $R_1 = \vert z_1 - z_0 \vert$, so $\vert z - z_0 \vert \le \vert z_1 - z_0 \vert$. Then we have

$$\begin{align*}
\left \vert \sum_{n=k}^m a_n(z-z_0)^n \right \vert & \le \sum_{n=k}^m \vert a_n \vert \vert z-z_0 \vert^n \\
& \le \sum_{n=k}^m \vert a_n \vert \vert z_1-z_0 \vert^n \\
&= \sum_{n=k}^m \vert a_n (z_1-z_0)^n \vert.
\end{align*}$$

By taking the limit that $m$ goes to infinity, we obtain 

$$\vert \rho_k(z) \vert \le \sigma_k \quad \text{when} \quad \vert z-z_0 \vert \le R_1.$$

Since the remainders are well-defined, each limit exists. 

Note that $\lim_{k \to \infty} \sigma_k = 0$ because the series $\displaystyle \sum_{n=0}^\infty \vert a_n(z_1-z_0)^n \vert$ converges. That is, for a given $\varepsilon > 0$, there exists a positive integer $N$ such that 

$$\sigma_k = \vert \sigma_k \vert < \varepsilon, \forall k \ge N.$$

Thus, we have that 

$$\vert \rho_k(z) \vert < \varepsilon, \forall k \ge N, \text{ whenever } \vert z - z_0 \vert \le R_1,$$

which means that the series $\displaystyle \sum_{n=0}^\infty a_n(z-z_0)^n$ converges uniformly in the closed disk $\vert z - z_0 \vert \le R_1$. $\blacksquare$

---
## Theorem 3
A power series 

$$S(z) := \sum_{n=0}^\infty a_n(z-z_0)^n$$

is a continuous function at each point inside its circle of convergence $\vert z - z_0 \vert = R$. 

### Proof
We let $S_k(z)$ denote the sum of the firsk $k$ terms of series, and write the remainder function 

$$\rho_k(z) = S(z) - S_k(z)$$

for $\vert z- z_0 \vert < R$. Since $S(z) = S_k(z) + \rho_k(z)$ for $\vert z- z_0 \vert < R$, we have 

$$\begin{align*}
\vert S(z) - S(z_1) \vert &= \vert [S_k(z) + \rho_k(z)] - [S_k(z_1) + \rho_k(z_1)] \vert \\
&= \vert [S_k(z) - S_k(z_1)] + [\rho_k(z) - \rho_k(z_1)] \vert \\
& \le \vert S_k(z) - S_k(z_1) \vert + \vert \rho_k(z) \vert + \vert \rho_k(z_1) \vert
\end{align*}$$

for each positive integer $k$ and $\vert z- z_0 \vert < R.$

Let $z$ be a point inside some closed disk $\vert z - z_0 \vert \le R_0$ where $\vert z_1 - z_0 \vert < R_0 < R$. By Theorem 2, $S(z)$ converges uniformly in that closed disk. That is, for a given $\varepsilon > 0$, there exists a positive integer $N$ such that 

$$\vert \rho_k(z) \vert < \frac{\varepsilon}{3}, \forall k \ge N, \text{ whenever } \vert z - z_0 \vert \le R_0.$$

In particular, the preceeding condition holds for each point $z$ in some neighborhood $\vert z- z_1 \vert < \delta_1$ of $z_1$ that is small enough to be contained in the closed disk $\vert z - z_0 \vert \le R_0$. 

Since the partial sum $S_k(z)$ is a polynomial, it is continuous at $z_1$ for each positive integer $k$. In particular, taking $k = N$, there exists $\delta_2 > 0$ such that if $\vert z - z_1 \vert < \delta_2$, then

$$\vert S_N(z) - S_N(z_1) \vert < \frac{\varepsilon}{3}.$$

Let $\delta := \min \\{ \delta_1, \delta_2 \\}.$ Thus, we obtain 

$$\begin{align*}
\vert S(z) - S(z_1) \vert &\le \vert S_N(z) - S_N(z_1) \vert + \vert \rho_N(z) \vert + \vert \rho_N(z_1) \vert \\
&< \frac{\varepsilon}{3} + \frac{\varepsilon}{3} + \frac{\varepsilon}{3} \\
&= \varepsilon
\end{align*}$$

for $\vert z - z_1 \vert < \delta$. Hence, $S(z)$ is continuous at each point $z$ inside $\vert z- z_0 \vert < R$. $\blacksquare$

---
## Theorem 4
Let $C$ denote any contour interior to the circle of convergence of the power series 

$$S(z) := \sum_{n=0}^\infty a_n(z-z_0)^n,$$

and let $g$ be a continuous function on $C$. Then 

$$\int_C g(z) S(z) \, dz = \sum_{n=0}^\infty a_n \int_C g(z) (z-z_0)^n \, dz.$$

### Proof
Let 

$$\rho_k(z) = \sum_{n=k}^\infty a_n(z-z_0)^n$$

for each positive integer $k$. By Theorem 3, both $g$ and $S$ are continuous on $C$. Then the integeral over $C$ of 

$$g(z) S(z) = \sum_{n=0}^{k-1} a_n \, g(z) (z-z_0)^n + g(z) \rho_k(z)$$

exists for each $k$. Since both the partial sum of $S(z)$ and the remainder are continuous, we obtain 

$$\int_C g(z) S(z) \, dz = \sum_{n=0}^{k-1} a_n \int_C g(z) (z-z_0)^n \, dz + \int_C g(z) \rho_k(z) \, dz.$$

Let $\displaystyle M := \max _ {z \in C} \vert g(z) \vert$, and let $L := \text{length}(C)$. Since the series converges uniformly on $C$, for a given $\varepsilon > 0$, there exists a positive integer $N$ such that 

$$\vert \rho_k(z) \vert < \frac{\varepsilon}{ML}, \forall k \ge N.$$

By $ML$-Lemma, we have 

$$\left \vert \int_C g(z) \rho_k(z) \, dz \right \vert \le M \frac{\varepsilon}{ML} L = \varepsilon, \forall k \ge N,$$

which implies that 

$$\lim_{k \to \infty} \int_C g(z) \rho_k(z) \, dz = 0.$$

It follows that 

$$\begin{align*}
\int_C g(z) S(z) \, dz &= \lim_{k \to \infty} \int_C g(z) S(z) \, dz \\
&= \lim_{k \to \infty} \left[ \sum_{n=0}^{k-1} a_n \int_C g(z) (z-z_0)^n \, dz + \int_C g(z) \rho_k(z) \, dz \right] \\
&= \sum_{n=0}^\infty a_n \int_C g(z) (z-z_0)^n \, dz. \quad \blacksquare
\end{align*}$$

---
## Corollary
The power series 

$$S(z) := \sum_{n=0}^\infty a_n(z-z_0)^n$$

is analytic at each point $z$ interior to the circle of convergence of that series. 

### Proof
Let $C$ be a closed contour lying in the open disk bounded by the circle of convergence of the series, and let $g(z) = 1$ for each point $z$ in that domain. Since $(z-z_0)^n$ is a polynomial, it is entire for each $n = 0, 1, 2, \cdots.$ Then we have 

$$\int_C g(z) (z-z_0)^n \, dz = \int_C (z-z_0)^n \, dz = 0$$

by [Theorem 1.](<{% post_url Complex Analysis/2026-05-08-Multiply-Connected-Domain %}#theorem-1>) 

By Theorem 4, we have 

$$\int_C S(z) \, dz = 0.$$

By [Morera's Theorem](<{% post_url Complex Analysis/2026-05-16-Morera-Theorem %}#morera's-theorem>), we conclude that $S$ is analytic throughout the circle of convergence of the series. $\blacksquare$

---
## Theorem 5
Let

$$S(z) := \sum_{n=0}^\infty a_n(z-z_0)^n$$

be a power series. Then 

$$S'(z) = \sum_{n=1}^\infty na_n(z-z_0)^{n-1}$$

at each point $z$ inside the circle of convergence of the series. 

### Proof
