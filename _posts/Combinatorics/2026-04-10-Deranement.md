---
title: "Derangement"
date: 2026-04-10
categories: [Mathematics, Combinatorics]
tags: []
math: true
---

## Definition
A ***derangement*** of $[n]$ is a permutation $\sigma$ of $[n]$ such that $\sigma(x) \neq x$ for all $x \in [n]$.

---

## Theorem
The number of derangements of a set of size $n$ is given by

$$
D_n = n! \sum_{k=0}^n \frac{(-1)^k}{k!}.
$$

### Proof 

Let $A_i$ be a subset of permutations of $[n]$ such that $\sigma(i) = i$. Then the set $D_n$ of derangements of $[n]$ is 

$$D_n = S_n - \bigcup_{i=1}^n A_i.$$

By the Principle of Inclusion-Exclusion, we have 

$$\begin{align*}
|D_n| &= |S_n - \bigcup_{i=1}^n A_i| \\ 
&= \vert \bigcap_{i=1}^n A_i^c \vert \\
&= \sum_{k=0}^n (-1)^k \sum_{I \in \binom{[n]}{k}} |\bigcap_{i \in I} A_i| \\
&= \sum_{k=0}^n (-1)^k \binom{n}{k} (n-k)! \\
&= \sum_{k=0}^n (-1)^k \frac{n!}{k!(n-k)!} (n-k)! \\
&= n! \sum_{k=0}^n \frac{(-1)^k}{k!}.
\end{align*}$$

Note that for sufficiently large $n$, $D_n \approx \frac{n!}{e}$. $\blacksquare$ 