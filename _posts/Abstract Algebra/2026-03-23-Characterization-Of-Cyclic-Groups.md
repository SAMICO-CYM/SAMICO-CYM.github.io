---
title: Characterization Of Cyclic Groups
date: 2026-03-23 00:00:01
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Theorem
Let $G$ be a cyclic group.

**(i)** If $\vert G \vert = \infty$, then $G \cong (\mathbb{Z}, +)$.

**(ii)** If $\vert G \vert = n \in \mathbb{N}$, then $G \cong (\mathbb{Z}_n, +)$.

### Proof
Let $G = \langle a \rangle$, and let $e$ denote the identity of $G$.

**(i)** Suppose that $\vert G \vert = \infty$. Then $a^m \neq a^n \forall m \neq n \in \mathbb{Z}$.

$(\because)$ Suppose that $a^m = a^n$ for some integers $m > n$. Then $a^{m - n} = e$. Then we claim $G = \\{ e, a, a^2, \cdots, a^{m - n - 1} \\}$.
\
($(\because)$ Since $a \in G$, clearly $G \supset \\{ e, a, a^2, \cdots, a^{m - n - 1} \\}$. Let $x \in G$. Then $x = a^k$ for some $k \in \mathbb{Z}$. By division algorithm, $\exists \, q, r \in \mathbb{Z}$ such that $k = (m - n)q + r$ and $0 \le r < m - n$. Then we have 

$$\begin{align*}
x &= a^k \\
&= a^{(m-n)q + r} \\
&= (a^{m - n})^q a^r \\
&= a^r \in \{ e, a, a^2, \cdots, a^{m - n - 1} \}.
\end{align*}$$

Thus $G = \{ e, a, a^2, \cdots, a^{m - n - 1} \}$, so that $\vert G \vert = m - n < \infty$. $\bigotimes$ )


**(ii)** Suppose that $\vert G \vert = n \in \mathbb{N}$. Then $a^n = e$ and $a^n \neq a^m$ for all $n \neq m$ in $\mathbb{Z}$.