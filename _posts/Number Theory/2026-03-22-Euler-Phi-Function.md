--- 
title: Euler $\phi$ Function
date: 2026-03-
categories: [Mathematics, Number Theory]
tags: []
math: true
---

## Definition
The function $\phi: \mathbb{N} \to \mathbb{N}$ defined by

$$\phi(n) = \vert \{ m \in \{ 1, ..., n \} \mid \gcd (n, m) = 1 \} \vert$$

is called the ***Euler $\phi$-function***. 

단순히 말해서 자연수 $n$과 서로소인 자연수의 개수를 말한다. 

---

## Theorem
(i) $\phi(p) = p-1 \iff p$ is a prime number.

(ii) If $p$ is a prime number, and $k > 0$, then 

$$\phi(p^k) = p^k - p^{k-1} = p^k \left( 1 - \frac{1}{p} \right)$$

(iii) $\phi$ is multiplicative;

$$\phi(ab) = \phi(a)\phi(b) \quad \text{if } \gcd(a,b) = 1$$

