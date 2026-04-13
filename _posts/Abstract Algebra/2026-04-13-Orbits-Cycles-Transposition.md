---
title: Orbits, Cycles, and Transpositions
date: 2026-04-13
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Remark
Let $\sigma$ be a permutation of a set $A$.
Define a relation $\sim$ on $A$ by

$$ a \sim b \quad \iff \quad b = \sigma^n(a) \quad \text{for some} \quad n \in \mathbb{Z}. $$

Then $\sim$ is an equivalence relation on $A$.

($\because$) Let $a, b, c \in A$.

**(i)** Note that $a = \sigma^0(a)$; so $a \sim a$. Thus, $\sim$ is reflexive.

**(ii)** If $a \sim b$, then $b = \sigma^n(a)$ for some $n \in \mathbb{Z}$. Since $\sigma$ is bijective, $a = \sigma^{-n}(b)$; so $b \sim a$. Thus, $\sim$ is symmetric.

**(iii)** Suppose that $a \sim b$ and $b \sim c$. Then $b = \sigma^m(a)$ and $c = \sigma^n(b)$ for some $m, n \in \mathbb{Z}$. Hence $c = \sigma^n(\sigma^m(a)) = \sigma^{n+m}(a)$, which means that $a \sim c$. Thus, $\sim$ is transitive.

Therefore, $\sim$ is an equivalence relation on $A$.

---

## Definition 
Let $\sigma$ be a permutation of a set $A$. 

**(i)** The ***orbits*** of $\sigma$ are the equivalence classes in $A$ determined by the equivalence relation $\sim$ in the previous remark.

**(ii)** $\sigma$ is called a ***cycle*** if it has at most one orbit containing more than one element.

**(iii)** The ***length*** of a cycle is the number of elements in its largest orbit.

**(iv)** A cycle of length 2 is a ***transposition***.

--- 

## Example

예컨대 $\sigma \in S_8$이 다음과 같이 주어져 있다.

$$\sigma = \begin{pmatrix} 1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 \\ 3 & 8 & 6 & 7 & 4 & 1 & 5 & 2 \end{pmatrix}$$

그러면 다음의 관계가 성립한다. 

Then

$$
\begin{align*}
1 &\xrightarrow{\sigma} \boxed{3} \xrightarrow{\sigma} \boxed{6} \xrightarrow{\sigma} \boxed{1} \xrightarrow{\sigma} 3 \\
&\xrightarrow{\sigma} 6 \xrightarrow{\sigma} \cdots, \\
2 &\xrightarrow{\sigma} \boxed{8} \xrightarrow{\sigma} \boxed{2} \xrightarrow{\sigma} 8 \xrightarrow{\sigma} 2 \\
&\xrightarrow{\sigma} 8 \xrightarrow{\sigma} \cdots \\
\text{and} \quad 4 &\xrightarrow{\sigma} \boxed{7} \xrightarrow{\sigma} \boxed{5} \xrightarrow{\sigma} \boxed{4} \\
&\xrightarrow{\sigma} 7 \xrightarrow{\sigma} 5 \xrightarrow{\sigma} \cdots.
\end{align*}
$$

Hence the orbits of $\sigma$ are $\\{1, 3, 6\\}, \\{2, 8\\}, \\{4, 5, 7\\}$.