---
title: Archimedean Property
date: 2026-05-14
categories: [Mathematics, Real Analysis]
tags: []
math: true
---

## Archimedean Property
**(i)** If $a$ and $b$ are positive real numbers, there exists a positive integer $n$ such that $a < nb$.

**(ii)** If $\varepsilon$ is a positive real number, there exists a positive integer $N$ such that $\frac{1}{N} < \varepsilon$.

### Proof
**(i)** Suppose that there does not exist a positive integer $n$ such that $a < nb$. Then $\forall n \in \mathbb{N}, a \geq nb$. Then $n \leq \frac{a}{b}, \forall n \in \mathbb{N}$, which means that $\mathbb{N}$ is bounded above, clearly a contradiction. $\bigotimes$ Thus, there exists a positive integer $n$ such that $a < nb$. 

**(ii)** In (i), take $a = 1$ and $b = \varepsilon$. Then $\exists N \in \mathbb{N}$ such that $1 < N \varepsilon \iff \frac{1}{N} < \varepsilon.$ $\blacksquare$