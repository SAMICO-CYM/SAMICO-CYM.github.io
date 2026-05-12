--- 
title: Cauchy Integral Formula
date: 2026-05-12
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Cauchy Integral Formula
Let $f$ be an analytic function inside and on a positvely oriented simple closed contour $C$. If $z_0$ be any point interior to $C$, then 

$$f(z_0) = \frac{1}{2\pi i} \int_C \frac{f(z)}{z - z_0} \, dz.$$

### Proof
We let $C _ {\rho}$ denote a positively oriented circle $\vert z - z_0 \vert = \rho$, where $\rho$ is small enough that $C _ {\rho} \subset C$. Since the function $\displaystyle \frac{f(z)}{z - z_0}$ is analytic between and on the contours $C _ {\rho}$ and $C$, we have 

$$\int_C \frac{f(z)}{z - z_0} \, dz = \int _ {C _ {\rho}} \frac{f(z)}{z - z_0} \, dz$$

by [the principle of deformation of paths.](<{% post_url Complex Analysis/2026-05-08-Multiply-Connected-Domain %}#corollary-2>) Note that 

$$\begin{align*} 
\int _ {C _ {\rho}} \frac{f(z) - f(z_0)}{z - z_0} \, dz &= \int _ {C _ {\rho}} \frac{f(z)}{z - z_0} \, dz - f(z_0) \int _ {C _ {\rho}} \frac{dz}{z - z_0} \\
&= \int _ {C _ {\rho}} \frac{f(z)}{z - z_0} \, dz - 2\pi i f(z_0).
\end{align*}$$

Since $f$ is analytic, and therefore continuous, at $z_0$, we have that for given $\varepsilon > 0$, there exists $\delta > 0$ such that 

$$\vert z - z_0 \vert < \delta \implies \vert f(z) - f(z_0) \vert < \varepsilon.$$

We assume that $\rho < \delta$. Since $\vert z - z_0 \vert = \rho < \delta$ for all $z$ in $C _ {\rho}$, we have that 

$$\begin{align*}
\left \vert \frac{f(z) - f(z_0)}{z - z_0} \right \vert < \frac{\varepsilon}{\rho}
\end{align*}$$

for all $z$ in $C _ {\rho}$. By [$ML$-lemma](<{% post_url Complex Analysis/2026-05-01-ML-Lemma %}), we obtain 

$$\begin{align*}
\left \vert \int _ {C _ {\rho}} \frac{f(z) - f(z_0)}{z - z_0} \, dz \right \vert < \frac{\varepsilon}{\rho} \cdot 2\pi \rho = 2 \pi \varepsilon.
\end{align*}$$

Since we choose $\varepsilon$ arbitrarily, we conclude that 

$$\int _ {C _ {\rho}} \frac{f(z) - f(z_0)}{z - z_0} \, dz = 0.$$

Thus, 

$$\int _ {C _ {\rho}} \frac{f(z)}{z - z_0} \, dz = 2\pi i f(z_0). \quad \blacksquare$$

---
## Corollary 
Let $f$ be an analytic function inside and on a positvely oriented simple closed contour $C$. If $z_0$ be any point interior to $C$, then 

$$f^{(n)}(z_0) = \frac{n!}{2\pi i} \int_C \frac{f(z)}{(z - z_0)^{n+1}} \, dz$$

for each $n = 0, 1, 2, \cdots.$

### Proof
We use induction on $n$.

For any point $z$ interior to $C$, we have 

$$f(z) = \frac{1}{2\pi i} \int_C \frac{f(s)}{s-z} \, ds$$

by Cauchy integral formula. Let $d := \min \\{ \vert s - z \vert \mid s \in C \\}$. (Assume that $C$ is parametrized by $\gamma: [a, b] \to C$. Since $C$ is a simple closed contour, $\gamma$ is (piecewise) continuous and surjective. Then $C = \gamma([a, b])$ is compact. Note that the function $f: C \to \mathbb{R}$ defined by $f(s) = \vert s - z \vert$ is continuous. Thus, $f$ has the minimum, says $d$.) 

Assume that $0 < \vert \Delta z \vert < d$. Then we have 

$$\begin{align*}
\frac{f(z + \Delta z) - f(z)}{\Delta z} &= \frac{1}{2 \pi i} \int_C \left[ \frac{1}{s-(z + \Delta z)} - \frac{1}{s - z} \right] \frac{f(s)}{\Delta z} \, ds \\
&= \frac{1}{2\pi i}
\end{align*}$$