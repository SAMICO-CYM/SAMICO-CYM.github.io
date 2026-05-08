--- 
title: Antiderivative
date: 2026-05-07
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Definition
Let $f(z)$ be a continuous function on a domain $D$. A function $F(z)$ is called an ***antiderivative*** of $f(z)$ if $F'(z) = f(z), \forall z \in D$.

---
## Remark
An antiderivative of a given function $f(z)$ is unique except for an additive constant.

$\big[(\because)$ Let $F(z)$ and $G(z)$ be two antiderivatives of $f(z)$. Since $F'(z) = f(z) = G'(z)$ on $D$, we have $(F - G)'(z) = F'(z) - G'(z) = 0$ on $D$, which means that the function $F - G$ is analytic on $D$. By [Theorem 1]({% post_url Complex Analysis/2026-04-09-Analytic-Function %}#theorem-1), we have $F(z) - G(z) = (F-G)(z) = C$ for some constant $C$.$\big]$

---
## Theorem 1
Suppose that a function $f(z)$ is continuous on a domain $D$. TFAE.

**(i)** $f(z)$ has an antiderivative $F(z)$ throughout $D$.

**(ii)** For any contour $C \subset D$, extending from any fixed point $z_1$ to any fixed point $z_2$, the value of integral along $C$ is ***independent of path*** taken. In particular, 

$$\int_{z_1}^{z_2} f(z) \, dz = F(z_2) - F(z_1),$$

where $F(z)$ is the antiderivative of $f(z)$.

**(iii)** For any closed contour $C \subset D$, $\displaystyle \int_C f(z) \, dz = 0$.

### Proof
**(i)** $\Longrightarrow$ **(ii)**

Suppose that $f(z)$ has an antiderivative $F(z)$ throughout $D$. Let $C$ be a contour in $D$ from $z_1$ to $z_2$ with the parametrization $z = z(t) (a \le t \le b)$. Suppose that $C$ is a single smooth curve. Then we have 

$$\frac{d}{dt}F[z(t)] = F'[z(t)] z'(t) = f[z(t)]z'(t)$$

for $a \le t \le b$. Then we have 

$$\begin{align*}
\int_C f(z) \, dz &= \int_a^b f[z(t)] z'(t) \, dt \\
&= \int_a^b \frac{d}{dt} F[z(t)] \, dt \\
&= F[z(b)] - F[z(a)] \\
&= F(z_2) - F(z_2)
\end{align*}$$

by [Theorem 3]({% post_url Complex Analysis/2026-04-28-Contours %}#theorem-3). The value $F(z_2) - F(z_1)$ of this countour integral is independent of the contour $C$. 

If $C$ consists of a finite number of smooth curves $C_1, \cdots, C_n$, each $C_k$ extending from a point $z_k$ to a point $z_{k+1}$, then we have 

$$\begin{align*}
\int_C f(z) \, dz &= \sum_{k=1}^n \int _ {C_k} f(z) \, dz \\
&= \sum_{k=1}^n \int _ {z_k} ^ {z_{k+1}} f(z) \, dz \\
&= \sum_{k=1}^n [F(z_{k+1}) - F(z_k)] \\
&= F(z_n) - F(z_1).
\end{align*}$$

Thus, the value $F(z_n) - F(z_1)$ of this countour integral is independent of the contour $C$. 

**(ii)** $\Longrightarrow$ **(iii)**