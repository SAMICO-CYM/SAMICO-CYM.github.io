--- 
title: First Isomorphism Theorem
date: 2026-05-13
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Theorem 1
Let $H \lhd G$. The map $\gamma: G \to G/H$ defined by $\gamma(g) = gH, \forall g \in G$ is an epimorphism with $\ker(\phi) = H$. We call $\gamma$ the ***canonical epimorphism***.

### Proof
Clearly, $\gamma$ is well-defined. 

Let $a, b \in G$. Then we have

$$\begin{align*}
\gamma(ab) &= (ab)H \\
&= (aH)(bH) \\
&= \gamma(a) \gamma(b),
\end{align*}$$

so that $\gamma$ is a homomorphism.

Let $gH \in G/H$. Then $g \in H$ and $\gamma(g) = gH$. Hence $\gamma$ is an epimorphism.

Let $g \in \ker(\phi)$. Then $gH = \phi(g) = H$, which means that $g \in H$. If $g \in H$, then $\gamma(g) = gH = H$, which means that $g \in \ker(\phi)$. Thus, $\ker(\phi) = H$. $\blacksquare$

---
## First Isomorphism Theorem
Let $\phi: G \to G'$ be a group homomorphism.

**(i)** The map $\mu: G/\ker(\phi) \to \mathrm{Im}(\phi)$ defined by 

$$\mu(g\ker(\phi)) = \phi(g)$$

for all $g\ker(\phi) \in G/\ker(\phi)$ is an isomorphism, and therefore $G/\ker(\phi) \cong \mathrm{Im}(\phi)$.

**(ii)** If $\gamma: G \to G/\ker(\phi)$ is the epimorphism in Theorem 1, then $\phi = \mu \circ \gamma$.

![](assets/img/Pasted%20image%2020260513165730.png)
