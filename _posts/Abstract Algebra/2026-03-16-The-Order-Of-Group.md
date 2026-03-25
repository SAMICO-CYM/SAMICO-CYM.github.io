---
title: The Order of Group
date: 2026-03-09 00:00:07
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Definition
Let $G$ be a group. 

**(i)** The ***order*** of $G$ is the number of elements in $G$, denoted by $\vert G\ vert$.

**(ii)** The order of an element $a \in G$ is the order of $\langle a \rangle$.

---

## Remark
Let $G$ be a finite group, and let $a \in G$. Then

$$\vert a \vert = \vert \langle a \rangle \vert = \min \{ m \in \mathbb{N} \mid a^m = e \}$$

$(\because)$ Let $n = \min \{ m \in \mathbb{N} \mid a^m = e \}$, that is, $a^n = e$ and $a^k \neq e, \forall 1 \le k < n$. We claim that $\langle a \rangle = \\{ e, a, a^2, \cdots, a^{n-1} \\}$.

$(\because)$ Suppose that $a^i = a^j$ for some $0 \le i < j \le n-1$. Then $a^{j-i} = e$, but it contradicts for the minimality of $n$. $\bigotimes$ Thus $a^i \neq a^j, \forall 0 \le i < j \le n-1$. 

Clearly $\langle a \rangle \supset \\{ e, a, a^2, \cdots, a^{n-1} \\}$. Let $x \in \langle a \rangle$. Then $x = a^\ell$ for some $\ell \in \mathbb{Z}$. By division algorithm, $\exists q, r \in \mathbb{Z}$ such that $\ell = nq + r$ and $0 \le r \le n-1$. Then we have 

$$x = a^{\ell} = (a^{n})^q a^r = a^r \in \\{ e, a, a^2, \cdots, a^{n-1} \\}.$$

Thus $\langle a \rangle = \\{ e, a, a^2, \cdots, a^{n-1} \\}$, so that $\vert a \vert = \vert \langle a \rangle \vert = n = \min \\{ m \in \mathbb{N} \mid a^m = e \\}$. $\blacksquare$