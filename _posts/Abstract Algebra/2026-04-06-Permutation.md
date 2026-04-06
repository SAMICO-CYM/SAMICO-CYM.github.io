---
title: Permutation
date: 2026-04-06
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Definition 1
A ***permutation*** of a set $A$ is a bijection $\sigma: A \to A$. We write the permutation $\sigma$ as 

$$
\sigma = \begin{pmatrix} a_1 & a_2 & \cdots & a_n \\ \sigma(a_1) & \sigma(a_2) & \cdots & \sigma(a_n) \end{pmatrix}.
$$

We denote the set of permutations of $A$ by $S_A$.

---

## Remark

(i) If $\sigma$ and $\tau$ are permutations of $A$, then so are $\sigma \tau$ and $\tau \sigma$.

(ii) If $A = \\{ 1 \\}$, then $S_A = \\{ id_A \\}$ and it is isomorphic to $\mathbb{Z}_1$. If $A = \\{ 1, 2 \\}$, then $S_A = \\{ id_A, \\sigma \\}$, where 

$$
\\sigma = \begin{pmatrix} 1 & 2 \\ 2 & 1 \end{pmatrix}.
$$

Then $S_A$ is isomorphic to $\mathbb{Z}_2$.

(iii) If $\vert A \vert \ge 3$, then $S_A$ is always non-abelian.

($\because$) For $n \ge 3$, let $A = \\{ 1, 2, ..., n \\}$. Let 

$$\sigma = \begin{pmatrix} 1 & 2 & \cdots & n-1 & n \\ 2 & 3 & \cdots & n & 1 \end{pmatrix} \quad \text{and} \quad \tau = \begin{pmatrix} 1 & 2 & 3 & \cdots & n \\ 2 & 1 & 3 & \cdots & n \end{pmatrix}.$$

Then $(\sigma \tau)(1) = 3 \neq 1 = (\tau \sigma)(1)$. Thus $S_A$ is non-abelian.


---

## Theorem 1
Let $A$ be a nonempty set. Then $S_A$ is a group under permutation multiplication.

### Proof
By Remark (i), $S_A$ is closed under permutation multiplication. 

Since the composition of functions is associative, $S_A$ is associative. 

The identity function $id_A$ on $A$ is the identity element of $S_A$.

For each $\sigma \in S_A$, $\exists \sigma^{-1} \in S_A$ such that $\sigma \sigma^{-1} = \sigma^{-1} \sigma = id_A$ because $\sigma$ is a bijection.

Thus $S_A$ is a group under permutation multiplication. $\blacksquare$

---

## Definition 2
Let $A = \\{ 1, 2, ..., n \\}$. Then the group of permutations of $A$ is called the ***symmetric group*** on $n$ letters and is denoted by $S_n$.

---

## Remark

$\vert S_n \vert = n!$.

---

## Example

Let $A = \\{ 1, 2, 3 \\}$. Then $S_3 = \\{ \rho_0, \rho_1, \rho_2, \mu_1, \mu_2, \mu_3 \\}$, where 

$$ \begin{align*}
\rho_0 = \begin{pmatrix} 1 & 2 & 3 \\ 1 & 2 & 3 \end{pmatrix}, \quad 
\rho_1 = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 3 & 1 \end{pmatrix}, \quad 
\rho_2 = \begin{pmatrix} 1 & 2 & 3 \\ 3 & 1 & 2 \end{pmatrix}, \\
\mu_1 = \begin{pmatrix} 1 & 2 & 3 \\ 1 & 3 & 2 \end{pmatrix}, \quad 
\mu_2 = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 3 \end{pmatrix}, \quad 
\mu_3 = \begin{pmatrix} 1 & 2 & 3 \\ 3 & 2 & 1 \end{pmatrix}.
\end{align*}
$$

---