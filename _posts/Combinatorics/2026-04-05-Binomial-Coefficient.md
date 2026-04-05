--- 
title: Binomial Coefficient
date: 2026-04-05
categories: [Mathematics, Combinatorics]
tags: []
math: true
---

## Definition
The ***binomial coefficient*** is defined by

$$\binom{n}{k} = \frac{n!}{k!(n-k)!}.$$

---

## Theorem
**(i)** $\displaystyle \binom{n}{k} = \binom{n}{n-k}$

**(ii)** $\displaystyle \binom{n}{k} = \binom{n-1}{n-1} + \binom{n-1}{k}$

**(iii)** $\displaystyle \binom{n}{k} \binom{k}{m} = \binom{n}{m} \binom{n-m}{k-m}$ where $m \le k \le n$

**(iv)** $\displaystyle (1+x)^n = \sum_{k=0}^n \binom{n}{k} x^k$

**(v)** $\displaystyle \binom{2n}{n} = \sum_{k=0}^n \binom{n}{k}^2$

### Proof
**(v)** Dividing the set $[2n]$ into $A = \\{1, ..., n \\}$ and $B = \\{ n+1, ..., 2n \\}$, an $n$-element subset of $[2n]$ consists of $i$-elements of $A$ and $(n-i)$-elements of $B$, for some $0 \le i \le n$. Then we can choose an $n$-element subset of $[2n]$ in 

$$\binom{2n}{n} = \sum_{i=0}^n \binom{n}{i} \binom{n}{n-i} = \sum_{i=0}^n \binom{n}{i}^2. \blacksquare$$

