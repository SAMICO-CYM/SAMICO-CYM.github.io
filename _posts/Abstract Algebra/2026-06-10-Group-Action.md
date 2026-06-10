--- 
title: Group Action
date: 2026-06-10
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Definition
Let $G$ be a group, and let $X$ be a nonempty set. Then a ***group action*** of $G$ on $X$ is a map $\ast: G \times X \to X,$ denoted by $\ast(g, x) = g \ast x = gx,$ such that 

**(i)** $ex = x, \forall x \in X,$

**(ii)** $(g_1g_2)x = g_1(g_2x), \forall g_1, g_2 \in G, x \in X.$

If there exists a group action of $G$ on $X$, then $X$ is called a ***$G$-set.***

---
## Example
**(i)** Let $X$ be any nonemptyset, and let $H \le S_X.$ Then $X$ is a $H$-set.

$\big[(\because)$ Define $\ast: H \times X \to X$ by $\ast(\sigma, x) = \sigma(x), \forall (\sigma, x) \in H \times X$. Then $\ast$ is well-defined. 

**(a)** $\ast(e_H, x) = e_H(x) = x, \forall x \in X.$ 

**(b)** 

$$\begin{align*}
\ast(\sigma_1 \sigma_2, x) &= \sigma_1 \sigma_2(x) \\
&= \sigma_1(\sigma_2(x)) \\
&= \ast(\sigma_1, \sigma_2(x)) \\
&= \ast(\sigma_1, \phi(\sigma_2, x))
\end{align*}$$

for all $\sigma_1, \sigma_2 \in H,x \in X.$ Thus, $(\sigma_1 \sigma_2)(x) = \sigma_1(\sigma_2(x)).$

Hence, $\ast$ is a group action of $H$ on $X.\big]$

**(ii)** Let $G$ be a group. Then $G$ is a $G$-set.

$\big[(\because)$ Define $\ast: G \times G \to G$ by $\ast(g_1, g_2) = g_1g_2, \forall (g_1, g_2) \in G \times G.$ Then $\ast$ is well-defined. 

**(a)** $\ast(e, g) = eg = g, \forall g \in G.$

**(b)** 

$$\begin{align*}
\ast(g_1g_2, g) &= (g_1g_2)g \\
&= g_1(g_2g) \\
&= \ast(g_1, g_2g) \\
&= \ast(g_1, \ast(g_2, g))
\end{align*}$$

for all $g_1, g_2, g \in G.$ 

Hence, $\ast$ is a group action of $G$ on $G.\big]$

**(iii)** Let $H \le G.$ Then $G$ is an $H$-set.

$\big[(\because)$ Define $\ast: H \times G \to G$ by $\ast(h, g) = hgh^{-1}, \forall (h, g) \in H \times G.$ Then $\ast$ is well-defined. 

**(a)** $\ast(e, g) = ege^{-1} = g, \forall g \in G.$

**(b)** 

$$\begin{align*}
\ast(h_1h_2, g) &= (h_1h_2)g(h_1h_2)^{-1} \\
&= (h_1h_2)g(h_2^{-1}h_1^{-1}) \\
&= h_1(h_2gh_2^{-1})h_1^{-1} \\
&= \ast(h_1, h_2gh_2^{-1}) \\
&= \ast(h_1, \ast(h_2, g)).
\end{align*}$$

for all $h_1, h_2 \in H, g \in G.$ 

Hence, $\ast$ is a group action of $H$ on $G.\big]$

---
## Theorem 1
Let $X$ be a $G$-set. 

**(i)** For each $g \in G$, the map $\sigma_g: X \to X$ defined by $\sigma_g(x) = gx, \forall x \in X$ is a permutation on $X$.

**(ii)** The map $\phi: G \to S_X$ defined by $\phi(g) = \sigma_g, \forall g \in G$ is a group homomorphism with $\phi(g)(x) = \sigma_g(x) = gx$.

### Proof
**(i)** Clearly, $\sigma_g$ is well-defined. Suppose that $\sigma_g(x_1) = \sigma_g(x_2).$ Then $gx_1 = gx_2,$ so 

$$\begin{align*}
x_1 &= ex_1 \\
&= (g^{-1}g)x_1 \\
&= g^{-1}(gx_1) \\
&= g^{-1}(gx_2) \\
&= (g^{-1}g)x_2 \\
&= ex_2 \\
&= x_2.
\end{align*}$$

Thus, $\sigma_g$ is one-to-one.

Let $x \in X.$ Then we have $\sigma_g(g^{-1}x) = g(g^{-1})x = ex = x,$ and $g^{-1}x \in X.$ Thus, $\sigma_g$ is onto, so $\sigma_g$ is a permutation on $X.$

**(ii)** Clearly, $\phi$ is well-defined. Let $g_1, g_2 \in G,$ and let $x \in X.$ Then we have 

$$\begin{align*}
(\phi(g_1g_2))(x) &= \sigma_{g_1g_2}(x) \\
&= (g_1g_2)x \\
&= g_1(g_2x) \\
&= \sigma_{g_1}(\sigma_{g_2}(x)) \\
&= (\phi(g_1))(\phi(g_2)(x)) \\
&= (\phi(g_1)\phi(g_2))(x),
\end{align*}$$

so $\phi(g_1g_2) = \phi(g_1)\phi(g_2).$ Hence, $\phi$ is a homomorphism. $\blacksquare$