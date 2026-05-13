--- 
title: Periodic Function
date: 2026-05-13
categories: [Mathematics, Fourier Series]
tags: []
math: true
---

## Definition 1
A function $f: \mathbb{R} \to \mathbb{R}$ is said to be ***periodic*** if there exists $p > 0$ such that $f(x+p) = f(x), \forall x \in \mathbb{R}$, and a number $p$ is called a ***period*** of $f$.

---
## Lemma
If a periodic function $f:\mathbb{R} \to \mathbb{R}$ has a period $p$, then $f$ has a period $mp$ for each $m \in \mathbb{N}$.

### Proof
For all $x \in \mathbb{R}$, we have

$$\begin{align*}
f(x+mp) &= f([x+(m-1)p] + p) \\
&= f(x + (m-1)p) \\
&= \cdots \\
&= f(x).
\end{align*}$$

Thus, $f$ has a period $mp$. $\blacksquare$

---
## Theorem
Let $f_1, \cdots, f_n: \mathbb{R} \to \mathbb{R}$ be periodic functions with a period $p_1, \cdots, p_n$, respectively. Then their linear combination $f := c_1f_1 + \cdots + c_nf_n$ is a periodic function with a period $p := \mathrm{lcm}(p_1, \cdots, p_n)$. 

### Proof
For all $x \in \mathbb{R}$, we have 

$$\begin{align*}
f(x+ p) &= (c_1f_1 + \cdots + c_nf_n)(x+p) \\
&= \sum_{i=1}^n c_if_i(x+p) \\
&=\sum_{i=1}^n c_if_i(x+m_ip_i) \quad \text{for some integer } m_i \\
&= \sum_{i=1}^n c_if_i(x) \quad \text{by Lemma} \\
&= f(x).
\end{align*}$$

Thus, $f$ is a periodic function with a period $p$. $\blacksquare$

---
## Definition 2
Let $f: (-p, p) \to \mathbb{R}$ be a function. The periodic extension $f _ {\text{per}}$ of $f$ is a function $f _ {\text{per}} : \mathbb{R} \to \mathbb{R}$ defined by 

$$f _ {\text{per}}(x) = f(x - 2pm)$$

for $-p + 2pm < x < p + 2pm$ for all integers $m$. The values at the endpoints can be specified arbitrary. 