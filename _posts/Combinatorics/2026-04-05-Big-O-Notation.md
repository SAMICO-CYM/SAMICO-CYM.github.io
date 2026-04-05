--- 
title: Big O Notation
date: 2026-04-05
categories: [Mathematics, Combinatorics]
tags: []
math: true
---

## Definition 1
Let $f$ and $g$ be real functions. We say that $f$ is ***big-Oh*** of $g$, denoted by $f = O(g)$ if $\exists M > 0, c > 0$ such that $f(x) < cg(x), \forall x > M$.

---

## Example

**(i)** Consider $f(x) = x^3 + 20x^2 - 7$. Then 

$$\begin{align*}
f(x) = x^3 + 20x^2 - 7 &\le x^3 + 20x^2 \\
& \le 21x^3 
\end{align*}$$

for all $x \ge 1$, which means that $f = O(x^3)$. 

**(ii)** Let $H_n$ be the $n$th harmonic number, i.e., 

$$H_n = \sum_{k=1}^n \frac{1}{k} = \frac{1}{1} + \frac{1}{2} + \cdots + \frac{1}{n}.$$

Let 

$$\begin{align*}
G_1 &= \frac{1}{1} \\
G_2 &= \frac{1}{2} + \frac{1}{3} \\
G_3 &= \frac{1}{4} + \frac{1}{5} + \frac{1}{6} + \frac{1}{7} \\
&\vdots \\
\end{align*}$$

That is, for $n \ge 2$,

$$\frac{1}{2} \le G_n = \sum_{k=2^{n-1}}^{2^n-1} \frac{1}{k} < 2^{n-1} \cdot \frac{1}{2^{n-1}} = 1.$$

Since 

$$H_n = G_1 + G_2 + \cdots + G _ { \lfloor \log_2n \rfloor} + \underbrace{G _ { \lfloor \log_2n \rfloor}}_{\text{some of}},$$

we have 

$$\frac{1}{2} \lfloor \log_2{n} \rfloor \le H_n < \lceil \log_2n \rceil,$$

which means that $H_n = O(\log_2{n})$.

---

## Theorem
Let $f$ and $g$ be real functions. Then the following hold:

$$\lim{x \to \infty} \frac{f(x)}{g(x)} = c \implies f(x) = O(g(x))$$

---

## Definition 2
Let $f$ and $g$ be real functions. We say that $f$ is ***liitle-oh*** of $g$, denoted by $f = o(g)$, if 

$$\lim_{x \to \infty} \frac{f(x)}{g(x)} = 0.$$

---

## Definition 3
Let $f$ and $g$ be real functions. We say that $f$ is ***eventually smaller*** than $g$, denoted by $f \preceq g$, if $\exists M > 0$ such that $f(x) \le g(x), \forall x > M$.

## Remark
For any constants $c_1, c_2, c_3 > 1$, we have 

$$\log_{c_1} n \preceq n^{c_2} \preceq c_3^n.$$