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

$$S = \\{a - xb \geq 0 \mid x \in \mathbb{Z}\\}$$

Since $b \geq 1$, we have

$$0 \leq a + |a| \leq a + |a|b = a - (-|a|)b.$$

Thus $S \neq \emptyset$. 

By Well-Ordering Principle, there is the least element $r \in S$. Then $\exists q \in \mathbb{Z}$ such that $r = a - qb$. Suppose that $r \geq b$. Then $0 \leq r - b = r - (q + 1)b \in S$, but $r - (q+1)b \leq r \bigotimes$. Thus $0 \leq r < b = |b|$. 

Let $b < 0$. Then $\exists q', r \in \mathbb{Z}$ such that $a = q'|b| + r (0 \leq r < |b|)$. Noting that $|b| = -b$, we may take $q = -q'$. Then we have $a = qb + r (0 \leq r < |b|)$.

Assume that $a$ has two representations of the form, say, $a = qb + r = q'b + r'$, where $0 \leq r, r' < |b|$. Then $r - r' = (q' - q)b \Longrightarrow |r - r'| = |q' - q||b|$.
Since $-|b| < r' \leq 0 \leq r < |b|$, $|r - r'| < |b|$. Then $|r - r'| = |q' - q||b| < |b| \Longrightarrow 0 \leq |q' - q| < 1 \Longrightarrow |q' - q| = 0 \Longleftrightarrow q = q' \Longrightarrow r = r'$. Thus the representation of $a$ is unique. $\blacksquare$ 