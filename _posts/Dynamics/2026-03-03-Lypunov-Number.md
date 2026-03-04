--- 
title: Lypunov Number
date: 2026-03-03 12:00:00 +0900
categories: [Mathematics, Dynamics]
tags: []
math: true
---

## Introduction
점 $p$를 맵 $f$의 sink, 혹은 source라고 하자. 이때 $p$ 주변의 점 $x$는 맵을 취할 때마다 근사적으로 $\vert f'(p) \vert$의 값만큼 $p$에 가까워지거나 멀어진다. Periodic-$k$ point의 경우에도 마찬가지로, $p_1$ 주변의 점 $x$는 맵을 $k$번 취했을 때 근사적으로 $\vert f'(p_1) \cdots f'(p_k) \vert$ 만큼 가까워지거나 멀어진다. 따라서 한 번 맵을 취했을 때 멀어지는 양은 $\vert f'(p_1) \cdots f'(p_k) \vert^{\frac{1}{k}}$ 로 정의하는 게 합리적이다.

이때 고정점이거나 주기점이 아니라 어떤 점 $x_1$과 그 orbit에 대해서 위 논의를 진행하면, 각 점에 대해서 그 주변의 점에 맵을 반복해서 취했을 때 가까워지고 멀어지는 정도를 정량화 할 수 있다. 이를 ***Lyapunov number***라고 부른다.

## Definition 1
**(i)** Let $f \in C(\mathbb{R})$. The ***Lyapunov number*** $L(x_1)$ of the orbit $\\{ x_1, x_2, ... \\}$ is defined as 

$$L(x_1) = \lim_{n \to \infty} \left(\vert f'(x_1)  \cdots f'(x_n)\vert \right)^{\frac{1}{n}},$$

if this limit exists. 

**(ii)** The ***Lyapunov exponent*** $h(x_1)$ is defined as 

$$h(x_1) = \lim_{n \to \infty} \frac{\log \vert f'(x_1) \vert + \cdots + \log \vert f'(x_n) \vert}{n},$$

if this limit exists. 

## Remark
- Lyapunov numbers and exponents are undefined for some orbits. In particular, an orbit containing a point $x_i$ with $f'(x_i) = 0$ causes the Lyapunov exponent to be undefined.
- It follows from the definition that the Lyapunov number of a fixed point $x_1$ for a one-dimensional map $f$ is $\vert f'(x_1) \vert$, or equivalently, the Lyapunov exponent of the orbit is $h = \log \vert f'(x_1) \vert$. If $x_1$ is a periodic point of period $k$, then it follows that the Lyapunov exponent is

$$h(x_1) = \frac{\log \vert f'(x_1) \vert + \cdots + \log \vert f'(x_k) \vert}{k}.$$

