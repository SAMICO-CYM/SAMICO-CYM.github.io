---
title: Fourier Series
date: 2026-05-07
categories: [Mathematics, Fourier Series]
tags: []
math: true
---

## Definition 1
Let $X = \\{x_1, x_2, \ldots\\}$ be a countable orthonormal set in an inner product space $V$ and let $x \in V$. The infinite series 

$$ \sum_{n=1}^\infty \langle x, x_n \rangle x_n $$ 

is called the ***Fourier series*** of $x$ (relative to $X$). The coefficient $\langle x, x_n \rangle$ is called the $n$th ***Fourier coefficient*** of $x$ (relative to $X$).

---

## Remark
Note that 

$$\left\\{ 1, \cos \frac{n\pi}{p} x, \sin \frac{n \pi}{p} x \, \bigg \vert \, n \in \mathbb{N} \right\\}$$

is an orthonormal basis of $\mathcal{R}[-L, L]$. Then the Fourier series of a function $f$ in $\mathcal{R}[-L, L]$ relative to the trigonometric set is 

$$\begin{align*}
\sum_{n=0}^\infty \langle f, \phi_n \rangle \phi_n(x) = \frac{a_0}{2} + \sum_{n=1}^{\infty} \left( a_n \cos \frac{n \pi}{L} x + b_n \sin \frac{n \pi}{L} x \right)
\end{align*}$$ 

where 

$$\begin{align*}
a_n &= \frac{1}{L} \int_{-L}^L f(x) \cos \frac{n \pi}{L} x \, dx \\ 
b_n &= \frac{1}{L} \int_{-L}^L f(x) \sin \frac{n \pi}{L} x \, dx.
\end{align*}$$ 

---

## Definition 2

**(i)** Let $f$ be an even real-valued function on $(-L, L)$. Then the ***Fourier cosine series*** of $f$ is defined by 

$$\frac{a_0}{2} + \sum_{n=1}^{\infty} a_n \cos \frac{n \pi}{L} x$$

where 

$$\begin{align*}
    a_n &= \frac{2}{L} \int_{0}^L f(x) \cos \frac{n \pi}{L} x \, dx.
\end{align*}$$

**(ii)** Let $f$ be an odd real-valued function on $(-L, L)$. Then the ***Fourier sine series*** of $f$ is defined by 

$$\sum_{n=1}^{\infty} b_n \sin \frac{n \pi}{L} x $$

where 

$$\begin{align*}
    b_n &= \frac{2}{L} \int_{0}^L f(x) \sin \frac{n \pi}{L} x \, dx.
\end{align*}$$