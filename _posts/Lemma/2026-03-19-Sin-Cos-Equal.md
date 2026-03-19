---
title: "사인과 코사인 값이 모두 같을 조건"
date: 2026-03-19
categories: [Mathematics, Lemma]
tags: []
math: true
---

## Theorem
Let $\alpha, \beta \in \mathbb{R}$. If 

$$\sin \alpha = \sin \beta \quad \text{and} \quad \cos \alpha = \cos \beta$$

then 

$$\alpha - \beta = 2n\pi \quad \text{for some } n \in \mathbb{Z}$$

### Proof
Note that the identity

$$\begin{align*}
\sin \alpha - \sin \beta &= 2 \cos \left( \frac{\alpha + \beta}{2} \right) \sin \left( \frac{\alpha - \beta}{2} \right) \\
\cos \alpha - \cos \beta &= -2 \sin \left( \frac{\alpha + \beta}{2} \right) \sin \left( \frac{\alpha - \beta}{2} \right).
\end{align*}
$$

Since

$$\begin{align*}
\sin \alpha - \sin \beta &= 0 \\
\cos \alpha - \cos \beta &= 0,
\end{align*}$$

we have

$$\begin{align*}
2 \cos \left( \frac{\alpha + \beta}{2} \right) \sin \left( \frac{\alpha - \beta}{2} \right) &= 0 \\
-2 \sin \left( \frac{\alpha + \beta}{2} \right) \sin \left( \frac{\alpha - \beta}{2} \right) &= 0.
\end{align*}$$

If $\displaystyle \sin \left( \frac{\alpha - \beta}{2} \right) \neq 0,$ then we have 

$$\begin{align*}
\cos \left( \frac{\alpha + \beta}{2} \right) &= 0 \\
\sin \left( \frac{\alpha + \beta}{2} \right) &= 0
\end{align*}$$

so that 

$$\cos^2 \left( \frac{\alpha + \beta}{2} \right) + \sin^2 \left( \frac{\alpha + \beta}{2} \right) = 0 \bigotimes$$

Thus we must have 

$$\sin \left( \frac{\alpha - \beta}{2} \right) = 0$$

so that 

$$\frac{\alpha - \beta}{2} = n\pi \quad \text{for some } n \in \mathbb{Z}$$

and therefore 

$$\alpha - \beta = 2n\pi \quad \text{for some } n \in \mathbb{Z}. \quad \blacksquare$$
