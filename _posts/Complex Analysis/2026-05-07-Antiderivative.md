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

$\big[(\because)$ Let $F(z)$ and $G(z)$ be two antiderivatives of $f(z)$. Since $F'(z) = f(z) = G'(z)$ on $D$, we have $(F - G)'(z) = F'(z) - G'(z) = 0$ on $D$, which means that the function $F - G$ is analytic on $D$. By [Theorem 1]({% post_url Complex Analysis/2026-04-09-Analytic-Function %}#theorem-1), we have $F(z) - G(z) = (F-G)(z) = C$ for some constant $C$. 

$\big]$