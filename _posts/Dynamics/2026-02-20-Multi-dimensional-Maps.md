--- 
title: Multidimensional Maps
date: 2026-02-20 15:00:00 +0900
categories: [Mathematics, Dynamics]
tags: []
math: true
---

## Definition 1
Let $f$ be a map on $\mathbb{R}^m$, and let $p \in \mathbb{R}^m$ be a [fixed point]({% post_url 2026-02-19-Dynamical-System %}#fixed-point) of $f$. 
- We call $p$ a ***sink*** or ***attracting fixed point*** if $\exists \varepsilon > 0$ such that $\lim_{k\to\infty} f^k(v) = p, \forall v \in N_\varepsilon(p).$
- We call $p$ a ***source*** or ***repeller*** if $\exists \varepsilon > 0$ such that for each $v \in N_\varepsilon(p)$ except for $p$, $\exists N \in \mathbb{N}$ such that $f^N(v) \notin N_\varepsilon(p)$.

---

## Theorem 1
Let $\mathsf{T}_A$ be a linear map on $\mathbb{R}^m$, and let $\lambda_1, ..., \lambda_m$ be the eigenvalues of $A$. Then
- The origin 
$\mathbf{0}$
is a sink if $|\lambda_i| < 1, \forall i \in \\{ 1, ..., m \\}$.
- The origin 
$\mathbf{0}$
is a source if $|\lambda_i| > 1, \forall i \in \\{ 1, ..., m \\}$.

### Proof
Suppose that $|\lambda_i| < 1, \forall i \in \\{ 1, ..., m \\}$. Let $J$ be the [JCF]({% post_url 2026-02-21-Jordan-Canonical-Form %}#jordan-canonical-form) of $A$, and let denote 

$$Q^{-1}AQ = J = \begin{bmatrix} J_1 & & \mathbf{0} \\ & \ddots & \\ \mathbf{0} & & J_\ell \end{bmatrix}$$

where $\ell$ is the number of linearly independent eigenvectors of $A$ and each $J_i$ is a Jordan block.
\
Note that

$$J^k = \begin{bmatrix} J^k_1 & & \mathbf{0} \\ & \ddots & \\ \mathbf{0} & & J^k_\ell \end{bmatrix}.$$

Suppose that $J_i = \lambda I + N \in M_{n \times n}(\mathbb{C})$ for some $1 \le i \le \ell$, where 

$$N = \begin{bmatrix} 0 & 1 & & \mathbf{0} \\ & \ddots & \ddots & \\ & & \ddots & 1 \\ \mathbf{0} & & & 0 \end{bmatrix}.$$

Since $IN = NI$ and $N^n = O$, we have 

$$\begin{align*} J_i^k &= \sum_{j=0}^k \binom{k}{j} N^j (\lambda I)^{k-j} = \sum_{j=0}^{n-1} \binom{k}{j} N^j (\lambda I)^{k-j}. \end{align*}$$

Consider the series $$\sum_{k=0}^\infty \binom{k}{j} \lambda^{k-j}.$$
Since 

$$\begin{align*} \lim_{k \to \infty} \left| \frac{\binom{k+1}{j} \lambda^{k+1-j}}{\binom{k}{j} \lambda^{k-j}} \right| &= \lim_{k \to \infty} \frac{\frac{(k+1)!}{(k+1-j)!j!}}{\frac{k!}{(k-j)!j!}} \left| \lambda \right| \\ &= \lim_{k \to \infty} \frac{k+1}{k-j+1} |\lambda| \\ & = |\lambda| < 1, \end{align*}$$

by the ratio test, the series $\sum_{k=0}^\infty \binom{k}{j} \lambda^{k-j}$ converges, which implies 

$$\lim_{k \to \infty} \binom{k}{j} \lambda^{k-j} = 0.$$

Then 

$$\begin{align*} \lim_{k \to \infty} J_i^k &= \lim_{k \to \infty} \sum_{j=0}^{n-1} \binom{k}{j} N^j (\lambda I)^{k-j} \\ & = \sum_{j=0}^{n-1} N^j \lim_{k \to \infty} \binom{k}{j} (\lambda I)^{k-j} \\ &= \sum_{j=0}^{n-1} N^j \mathbf{O} = \mathbf{O}, \end{align*}$$

 and therefore 
 
 $$\lim_{k \to \infty} J^k = \mathbf{O}.$$

Take any $\varepsilon > 0$. For any $v \in N_\varepsilon(\mathbf{0})$, we have 

$$\begin{align*} \lim_{k \to \infty} A^kv &= \lim_{k \to \infty} Q J^k Q^{-1} v \\ &= Q \left( \lim_{k \to \infty} J^k \right)Q^{-1}v \\ &= \mathbf{0}. \end{align*}$$

Hence the origin $\mathbf{0}$ is a sink. The second part can be proved by the similar way. $\blacksquare$


---

## Definition 2
Let $\mathsf{T}_A$ be a linear map on $\mathbb{R}^m$, and let $\lambda_1, ..., \lambda_m$ be the eigenvalues of $A$. 
- We say 
$A$
is ***hyperbolic*** if $|\lambda_i| \neq 1, \forall i \in \\{ 1, ..., m \\}$. 
- If 
$A$
is hyperbolic and $|\lambda_i| > 1$ or $|\lambda_i| < 1$ for some $i \in \\{ 1, ..., m \\}$, then the origin $\mathbf{0}$ is called a ***saddle***.

---