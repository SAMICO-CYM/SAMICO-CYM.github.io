--- 
title: Period 3 Implies Chaos
date: 2026-02-26 15:00:00 +0900
categories: [Mathematics, Dynamics]
tags: []
math: true
---

## Period-3 Point

Let $I$ be an interval and let $f: I \to I$ be a continuous function. A point $x \in I$ is called a **periodic point of period $p$** (or **period-$p$ point**) if $f^p(x) = x$ and $f^k(x) \neq x$ for all $1 \le k < p$.

If a dynamical system has a period-3 point, it exhibits very interesting properties, which lead to the famous statement: **"Period Three Implies Chaos."**

---

## Li-Yorke Theorem (1975)

The theorem by Tien-Yien Li and James A. Yorke states that if a continuous map on an interval has a period-3 point, then it has periodic points of every integer period, and the system is chaotic.

### Theorem Statement

Let $J$ be an interval and let $F: J \to J$ be a continuous function. Assume there is a point $a \in J$ for which the points $b = F(a)$, $c = F^2(a)$ and $d = F^3(a)$, satisfy

$$
d \le a < b < c \quad \text{or} \quad d \ge a > b > c.
$$

Then:
1. For every $k = 1, 2, \ldots$ there is a periodic point in $J$ having period $k$.
2. There is an uncountable set $S \subset J$ (containing no periodic points) which satisfies certain chaotic behaviors (e.g., sensitive dependence on initial conditions).

---

## Sarkovskii's Theorem (1964)

The result that a period-3 point implies periodic points of all other periods is actually a special case of a theorem proved earlier by the Ukrainian mathematician Oleksandr Sarkovskii.

### Sarkovskii's Ordering

Consider the following ordering $\triangleright$ of the natural numbers:

$$
\begin{align*}
& 3 \triangleright 5 \triangleright 7 \triangleright 9 \triangleright \cdots \\
\triangleright \, & 3 \cdot 2 \triangleright 5 \cdot 2 \triangleright 7 \cdot 2 \triangleright \cdots \\
\triangleright \, & 3 \cdot 2^2 \triangleright 5 \cdot 2^2 \triangleright 7 \cdot 2^2 \triangleright \cdots \\
\dots & \\
\triangleright \, & \cdots \triangleright 2^3 \triangleright 2^2 \triangleright 2 \triangleright 1
\end{align*}
$$

### Theorem Statement

Let $f: I \to I$ be a continuous function on an interval $I$. If $f$ has a periodic point of period $n$, and $n \triangleright m$ in Sarkovskii's ordering, then $f$ also has a periodic point of period $m$.

Since $3$ is the first and greatest element in Sarkovskii's ordering, if a continuous function $f$ has a period-3 point, it must have periodic points of **all** integer periods. $\blacksquare$