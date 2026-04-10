---
title: "The Number Of Functions"
date: 2026-04-10
categories: [Mathematics, Combinatorics]
tags: []
math: true
---

## Remark
If two sets $X$ and $Y$ are equipotent, i.e., there exists a bijection between $X$ and $Y$, then the cardinality of $X$ and $Y$ are the same. 

## Theorem 1
Let $X$ and $Y$ be finite sets. The number of functions from $X$ to $Y$ is given by $\vert Y \vert^{\vert X \vert}$.

### Proof

---

## Theorem 2
Let $X$ and $Y$ be finite sets. The number of injective functions from $X$ to $Y$ is given by $\frac{\vert Y \vert !}{(\vert Y \vert - \vert X \vert)!}$ if $\vert X \vert \leq \vert Y \vert$, and $0$ if $\vert X \vert > \vert Y \vert$.

### Proof
By Pigeonhole Principle, if $\vert X \vert > \vert Y \vert$, then there is no injective function from $X$ to $Y$. 

Suppose that $\vert X \vert \leq \vert Y \vert$. Then we have

$$\binom{\vert Y \vert}{\vert X \vert} \cdot \vert X \vert ! = \frac{\vert Y \vert !}{(\vert Y \vert - \vert X \vert)!}. \blacksquare$$

---

## Theorem 3
Let $X$ and $Y$ be finite sets. The number of surjective functions from $X$ to $Y$ is given by $\sum_{k=0}^{\vert Y \vert} (-1)^k \binom{\vert Y \vert}{k} (\vert Y \vert - k)^{\vert X \vert}$ if $\vert X \vert \geq \vert Y \vert$, and $0$ if $\vert X \vert < \vert Y \vert$. 

### Proof
If $\vert X \vert < \vert Y \vert$, then there is no surjective function from $X$ to $Y$. 

Suppose that $\vert X \vert \geq \vert Y \vert$. Let $A_i = Y - \\{ y_i \\}$ for each $i = 1, ..., \vert Y \vert$. By the Principle of Inclusion-Exclusion, we have 

$$\begin{align*}
\vert Y^X - \bigcup_{i=1}^{\vert Y \vert} A_i \vert &= \vert \bigcap_{i=1}^{\vert Y \vert} A_i^c \vert \\
&= \sum_{k=0}^{\vert Y \vert} (-1)^k \sum_{I \in \binom{[\vert Y \vert]}{k}} \vert \bigcap_{i \in I} A_i \vert \\
&= \sum_{k=0}^{\vert Y \vert} (-1)^k \sum_{I \in \binom{[\vert Y \vert]}{k}} (\vert Y \vert - k)^{\vert X \vert} \\
&= \sum_{k=0}^{\vert Y \vert} (-1)^k \binom{\vert Y \vert}{k} (\vert Y \vert - k)^{\vert X \vert}. \blacksquare
\end{align*}$$

---

## Theorem 4
Let $X$ and $Y$ be finite sets. The number of bijective functions from $X$ to $Y$ is given by $\vert X \vert !$ if $\vert X \vert = \vert Y \vert$, and $0$ if $\vert X \vert \neq \vert Y \vert$.

### Proof
If $\vert X \vert \neq \vert Y \vert$, then there is no bijective function from $X$ to $Y$. 

Suppose that $\vert X \vert = \vert Y \vert$. Then the number of bijections from $X$ to $Y$ is the same as the number of permutations of $X$, which is $\vert X \vert !$. $\blacksquare$ 