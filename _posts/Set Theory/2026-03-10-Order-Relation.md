--- 
title: Order Relation
date: 2026-03-09 00:01:27
categories: [Mathematics, Set Theory]
tags: []
math: true
---

## Definition 1
A relation $R$ on a set $A$ is called an ***order relation*** if it has the following properties:

**(i)** $\forall x, y \in A (x \neq y), xRy \vee yRx$.

**(ii)** $\nexists \, x (xRx).$

**(iii)** $xRy \wedge yRz \implies xRz$

## Example
The "less than" symbol $<$ on $\mathbb{R}$ is an ordered relation. Clearly, the relation $<$ satisfies the above conditions:

**(i)** $\forall x, y \in \mathbb{R} (x \neq y), x < y \vee y < x$

**(ii)** $\nexists \, x (x < x).$

**(iii)** $x < y \wedge y < z \implies x < z$

## Definition 2
Suppose that $A$ and $B$ are two sets with order relaitons $<_A$ and $<_B$, respectively. We say that $A$ and $B$ have the same ***order type*** if there exists a bijection $f: A \to B$ such that

$$a_1 <_A a_2 \implies f(a_1) <_B f(a_2).$$

## Definition 3
Suppose that $A$ and $B$ are two sets with order relations $<_A$ and $<_B$, respectively. Define an order relation $<$ on $A \times B$ by defining

$$a_1 \times b_1 < a_2 \times b_2$$

if $a_1 <_A a_2$, or if $a_1 = a_2$ and $b_1 <_B b_2$. It is called the ***dictionary order relation*** on $A \times B$. 