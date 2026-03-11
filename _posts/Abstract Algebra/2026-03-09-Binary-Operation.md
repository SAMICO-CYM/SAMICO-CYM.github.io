--- 
title: Binary Operation
date: 2026-03-09 00:01:30
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Definition 1
**(i)** A ***binary operation*** $\ast$ on a set $S$ is a function $\ast : S \times S \to S$. For each $(a, b) \in S \times S$, we will denote $\ast(a, b)$ by $a \ast b$. We call the ordered pair $(S, \ast)$ a ***binary algebraic structure***.

**(ii)** Let $\ast$ be a binary operation on $S$, and let $H \subset S$. Then $H$ is said to be ***closed*** under $\ast$ if $a \ast b \in H \forall a, b \in H$. In this case, $\ast \vert_H$ is called the ***induced operation*** of $\ast$ on $H$.

---

## Definition 2
**(i)** A binary operation $\ast$ on a set $S$ is said to be ***associative*** if $(a \ast b) \ast c = a \ast (b \ast c) \forall a, b, c \in S$.

**(ii)** A binary operation $\ast$ on a set $S$ is said to be ***commutative*** if $a \ast b = b \ast a \forall a, b \in S$.

---

## Definition 3
Let $(S, \ast)$ be a binary algebraic structure.

**(i)** A element $e$ is called an **identity element** for $\ast$ if $e \ast a = a = a \ast e, \forall a \in S$.

**(ii)** Let $a \in S$. If there is an element $b \in S$ such that $a \ast b = e = b \ast a$, then $b$ is called an **inverse element** of $a$ for $\ast$.

---

## Theorem
A binary algebraic structure $(S, \ast)$ has at most one identity element.

### Proof
If $S$ does not have an identity element, then there is nothing to prove.

Suppose that $e_1$ and $e_2$ are identity elements for $\ast$. Then $e_1 = e_1 \ast e_2 = e_2$. $\blacksquare$

---

## Remark
Let $S = \\{ a, b, c \\}$, and let $\ast$ be a binary operation on $S$ as follows:

$$
\begin{array}{c|ccc}
* & a & b & c \\
\hline
a & b & c & b \\
b & a & c & b \\
c & c & b & a \\
\end{array}
$$

Then $\ast$ is not commutative.

We can easily see that a binary operation $\ast$ defined by a table is commutative $\iff$ the table is symmetric.