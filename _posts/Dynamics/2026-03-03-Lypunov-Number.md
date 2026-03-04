--- 
title: Lypunov Number
date: 2026-03-03 12:00:00 +0900
categories: [Mathematics, Dynamics]
tags: []
math: true
---

## Definition 1
**(i)** Let $f \in C(\mathbb{R})$. The ***Lyapunov number*** $L(x_1)$ of the orbit $\\{ x_1, x_2, ... \\}$ is defined as 

$$L(x_1) = \lim_{n \to \infty} \left(\vert f'(x_1)  \cdots f'(x_n)\vert \right)^{\frac{1}{n}},$$

if this limit exists. 

**(ii)** The ***Lyapunov exponent*** $h(x_1)$ is defined as 

$$h(x_1) = \lim_{n \to \infty} \frac{\log \vert f'(x_1) \vert + \cdots + \log \vert f'(x_n) \vert}{n},$$

if this limit exists. 

Source, 혹은 sink point $p$ 주변의 점 $x$에서 맵 $f$를 취할 때마다 얼마나 멀어지고 가까워지는지는 $\vert f'(p) \vert$의 값에 의해 결정된다. 즉 $x$에 반복해서 맵을 취할 때마다 $\vert f'(p) \vert$만큼 $p$에 가까워지거나 멀어진다. 

## Remark
- Lyapunov numbers and exponents are undefined for some orbits. In particular, an orbit containing a point $x_i$ with $f'(x_i) = 0$ causes the Lyapunov exponent to be undefined.