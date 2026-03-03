--- 
title: Lypunov Number
date: 2026-03-03 12:00:00 +0900
categories: [Mathematics, Dynamics]
tags: []
math: true
---

## Definition 1
**(i)** Let $f \in C(\mathbb{R})$. The ***Lyapunov number*** $L(x_1)$ of the orbit $\\{ x_1, x_2, ... \\}$ is defined as 

$$L(x_1) = \lim_{n \to \infty} (\vert f'(x_1)  \cdots f'(x_n)\vert)^{\frac{1}{n}},$$

if this limit exists. 

**(ii)** The ***Lyapunov exponent*** $h(x_1)$ is defined as 

$$h(x_1) = \lim_{n \to \infty} \frac{\log \vert f'(x_1) \vert + \cdots + \log \vert f'(x_n) \vert}{n},$$

if this limit exists. 

## Remark
- Lyapunov numbers and exponents are undefined for some orbits. In particular, an orbit containing a point $x_i$ with $f'(x_i) = 0$ causes the Lyapunov exponent to be undefined.