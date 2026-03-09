--- 
title: Binary Operation
date: 2026-03-09
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Definition 1
**(i)** A ***binary operation*** $\ast$ on a set $S$ is a function $\ast : S \times S \to S$. For each $(a, b) \in S \times S$, we will denote $\ast(a, b)$ by $a \ast b$. We call the ordered pair $(S, \ast)$ a ***binary algebraic structure***.

**(ii)** Let $\ast$ be a binary operation on $S$, and let $H \subset S$. Then $H$ is said to be ***closed*** under $\ast$ if $a \ast b \in H \forall a, b \in H$. In this case, $\ast \vert_H$ is called the ***induced operation*** of $\ast$ on $H$.

## Definition 2
**(i)** A binary operation $\ast$ on a set $S$ is said to be ***associative*** if $(a \ast b) \ast c = a \ast (b \ast c) \forall a, b, c \in S$.

**(ii)** A binary operation $\ast$ on a set $S$ is said to be ***commutative*** if $a \ast b = b \ast a \forall a, b \in S$.

## Remark

$$
\begin{array}{c|cccc}
* & a & b & c & d \\
\hline
a & b &   &   &   \\
b & d & a &   &   \\
c & a & c & d &   \\
d & a & b & b & c
\end{array}
$$