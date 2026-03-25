---
title: Division Algorithm
date: 2026-03-25 00:00:01
categories: [Mathematics, Number Theory]
tags: []
math: true
---

## Theorem
Let $a, b \in \mathbb{Z}$ with $b \neq 0$. Then $\exists ! \, q, r \in \mathbb{Z}$ such that $a = bq + r$ and $0 \le r < \vert b \vert$.

### Proof
Let $b > 0$, and let 

$$S = \{a - xb \geq 0 \mid x \in \mathbb{Z}\}$$

Since $b \geq 1$, we have

$$0 \leq a + \vert a \vert \leq a + \vert a \vert b = a - (- \vert a \vert)b.$$

Thus $- \vert a \vert \in S$, so that $S \neq \emptyset$. 

By Well-Ordering Principle, there is the least element $r \in S$. Then $\exists q \in \mathbb{Z}$ such that $r = a - qb$. Suppose that $r \geq b$. Then 

$$
0 \leq r - b = r - (q + 1)b \in S,
$$

but $r - (q+1)b \leq r \bigotimes$. Thus $0 \leq r < b = \vert b \vert$. 

Let $b < 0$. Then $\exists q', r \in \mathbb{Z}$ such that $a = q'\vert b \vert + r (0 \leq r < \vert b \vert)$. Noting that $\vert b \vert = -b$, we may take $q = -q'$. Then we have $a = qb + r (0 \leq r < \vert b \vert)$.

Assume that $a$ has two representations of the form, say, $a = qb + r = q'b + r'$, where $0 \leq r, r' < \vert b \vert$. Then 

$$
\begin{align*}
    r - r' &= (q' - q)b \\
    \Longrightarrow \vert r - r' \vert &= \vert q' - q \vert \vert b \vert.
\end{align*}
$$

Since $- \vert b \vert < r' \leq 0 \leq r < \vert b \vert$, we have $\vert r - r' \vert < \vert b \vert$. Then 

$$
\begin{align*}
    \vert &r - r' \vert = \vert q' - q \vert \vert b \vert < \vert b \vert \\
    \Longrightarrow &0 \leq \vert q' - q \vert < 1 \\
    \Longrightarrow &\vert q' - q \vert = 0 \\
    \Longleftrightarrow &q = q' \\
    \Longleftrightarrow &r = r'.
\end{align*}
$$

Thus the representation of $a$ is unique. $\blacksquare$ 