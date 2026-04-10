---
title: Principle of Inclusion-Exclusion
date: 2026-04-06
categories: [Mathematics, Combinatorics]
tags: []
math: true
---

## Theorem
For $A_1, ..., A_n \subset X$, 

$$\left\vert \bigcup_{i=1}^n A_i \right\vert = \sum_{k=1}^n (-1)^{k-1} \sum_{I \in \binom{[n]}{k}} \left\vert \bigcap_{i \in I} A_i \right\vert.$$

### Proof
If suffices to show that for each $x \in \bigcup_{i=1}^n A_i$, $x$ is counted exactly once in the right hand side.

Suppose that $x$ is contained in $j$ sets of $A_i$'s. Then it is counted 

$$\begin{align*}
&+j \text{ times when } k = 1 \\
&- \binom{j}{2} \text{ times when } k = 2 \\
&+ \binom{j}{3} \text{ times when } k = 3 \\
\vdots \\
&+ (-1)^{j-1} \binom{j}{j} \text{ times when } k = j \\
&+ 0 \text{ times when } k > j
\end{align*}$$

In total, $x$ is counted 

$$j - \binom{j}{2} + \binom{j}{3} - \cdots + (-1)^{j-1} \binom{j}{j}$$

times. Note that 

$$0 = (1- 1)^j = \sum_{i=0}^j \binom{j}{i}(-1)^i = 1 - j + \binom{j}{2} - \cdots + (-1)^j \binom{j}{j}$$

Thus, 

$$j - \binom{j}{2} + \binom{j}{3} - \cdots + (-1)^{j-1} \binom{j}{j} = 1,$$

which means that $x$ is counted exactly once in the right hand side. $\blacksquare$

---

## Corollary
For $A_1, ..., A_n \subset X$, 

$$\left\vert \bigcap_{i=1}^n A_i^c \right\vert = \sum_{k=0}^n (-1)^k \sum_{I \in \binom{[n]}{k}} \left\vert \bigcap_{i \in I} A_i \right\vert.$$

### Proof

$$\begin{align*}
\left\vert \bigcap_{i=1}^n A_i^c \right\vert &= \left\vert \left( \bigcup_{i=1}^n A_i \right)^c \right\vert \\
&= \vert X \vert - \left\vert \bigcup_{i=1}^n A_i \right\vert \\
&= \vert X \vert - \sum_{k=1}^n (-1)^{k-1} \sum_{I \in \binom{[n]}{k}} \left\vert \bigcap_{i \in I} A_i \right\vert \\
&= \vert X \vert + \sum_{k=1}^n (-1)^{k} \sum_{I \in \binom{[n]}{k}} \left\vert \bigcap_{i \in I} A_i \right\vert \\
&= \sum_{k=0}^n (-1)^k \sum_{I \in \binom{[n]}{k}} \left\vert \bigcap_{i \in I} A_i \right\vert.
\end{align*}$$

because $\bigcap_{i \in \emptyset} A_i = X$. $\blacksquare$