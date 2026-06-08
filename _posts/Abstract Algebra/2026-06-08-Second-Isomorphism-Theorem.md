--- 
title: Second Isomorphism Theorem
date: 2026-06-08
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Definition
Let $G$ be a group, and let $H, N \le G.$ Then the ***join*** of $H$ and $N$, denoted by $H \vee N,$ is defined by 

$$H \vee N := \bigcap_{HN \subset K \le G} K.$$

---
## Lemma
Let $G$ be a group, and let $H,N \le G.$ We denote $HN := \\{ hn \mid h \in H, n \in N \\}.$

**(i)** $H \vee N$ is the smallest subgroup of $G$ containing $HN.$

**(ii)** $H \vee N$ is the smallest subgroup of $G$ containing both $H$ and $N.$

**(iii)** If $N \lhd G,$ then $HN$ is the smallest subgroup of $G$ containing both $H$ and $N.$ That is, $H \vee N = HN = NH.$

**(iv)** If $N, H \lhd G,$ then $HN \lhd G.$
### Proof
**(i)** It is obtained by definition of the join and [Theorem 2](<{% post_url Abstract Algebra/2026-03-18-Subgroup %}#theorem-2>).

**(ii)** Let $K$ be a subgroup of $G$ containing both $H$ and $N.$ Then $HN \subset K.$ By definition of the join $H \vee N,$ we have $H \vee N \subset K.$ Thus, $H \vee N$ is the smallest subgroup of $G$ containing both $H$ and $N.$ 

**(iii)** **Claim 1:** $HN \le G.$ 

$\big[(\because)$ Let $x, y \in HN.$ (Since $H$ and $N$ are subgroups of $G$, clearly, $HN$ is not empty.) Then $x = h_1n_1$ and $y = h_2n_2$ for some $h_1, h_2 \in H$ and $n_1, n_2 \in N.$ Note that 

$$\begin{align*}
    xy^{-1} &= (h_1n_1)(h_2n_2)^{-1} \\
    &= h_1(n_1n_2^{-1})h_2^{-1} \\
    &\in h_1Nh_2^{-1}
\end{align*}$$ 

because $n_1n_2^{-1} \in N.$ 

Since $N$ is normal, $Nh_2^{-1} = h_2^{-1}N.$ Then 

$$\begin{align*}
    xy^{-1} &\in h_1Nh_2^{-1} \\
    &=(h_1h_2^{-1})N \\
    &\subset HN
\end{align*}$$

because $h_1h_2^{-1} \in H.$ Thus, $xy^{-1} \in HN,$ so $HN \le G.$ Note that clearly $H, N \subset HN.$ Similarly, we can show that $NH \le G.$$\big]$

**Claim 2:** $HN$ is the smallest subgroup containing both $H$ and $N.$ 

$\big[(\because)$ Take a subgroup $K \le G$ containing both $H$ and $N.$ Let $a \in HN.$ Then $a = hn$ for some $h \in H$ and $n \in N.$ Since $K$ contains $H$ and $N,$ $h \in K$ and $n \in K.$ Since $K$ is a group, $a = hn \in K$. Thus, $HN \subset K,$ which means that $HN$ is the smallest subgroup containing both $H$ and $N.$ Similarly, we can show that $NH$ is the smallest subgroup containing both $H$ and $N.$ Therefore, $HN = NH.$$\big]$

**Claim 3:** $H \vee N = HN = NH.$ 
 
$\big[(\because)$ Note that $H \vee N$ is the smallest subgroup of $G$ containing $HN.$ Since $H, N \subset HN,$ $H \vee N$ is a subgroup of $G$ containing both $H$ and $N$. By (i), $HN$ is the smallest subgroup of $G$ containing both $H$ and $N$, so we obtain $HN \subset H \vee N.$ 

On the other hand, since $HN \le G,$ we obtain $H \vee N \subset HN.$ Thus, $H \vee N = HN = NH.$$\big]$

**(iv)** Let $g \in G,$ and let $hn \in HN.$ Then we have 

$$\begin{align*}
g(hn)g^{-1} &= (ghg^{-1})(gng^{-1}) \\
& \in HN,
\end{align*}$$

so $g(HN)g^{-1} \subset HN,$ which means that $HN \lhd G.$ $\blacksquare$

---
## Remark
Let $G$ be a group, and let $H, N \le G.$ Then $HN$ need not to be a subspace of $G.$

$\big[(\because)$ Let $G = S_3$ and let $H = \langle \mu_1 \rangle = \\{ \rho_0, \mu_1 \\}$ and $N = \langle \mu_3 \rangle = \\{ \rho_0, \mu_3 \\}.$ Then $H, N \le G$ but $HN = \\{ \rho_0, \mu_1, \mu_3, \rho_2 \\} \not \le S_3. \big]$

---
## Second Isomorphism Theorem
Let $G$ be a group, and let $H \le G, N \lhd G.$ Then 

$$(HN)/N \cong H/(H \cap N)$$

### Proof
First, we note that $HN \le G,$ so $N \lhd HN,$ and that $H \cap N \lhd H.$

$\big[(\because)$ $N \lhd HN$ is clear. To verify another one, let $h \in H.$ Then for any $x \in H \cap N,$ $hxh^{-1} \in H,$ so $h(H \cap N)h^{-1} \subset H.$ Thus, $H \cap N \lhd H.\big]$

We define a map $\phi: HN \to H/(H \cap N)$ by $\phi(hn) = h(H \cap N), \forall hn \in HN.$ 

**Claim 1:** $\phi$ is well-defined.

$\big[(\because)$ Let $h_1n_1, h_2n_2 \in HN.$ Suppose that $h_1n_1 = h_2n_2.$ Then we have $h_1 = h_2n_2n_1^{-1}$ and $h_2^{-1}h_1 = n_2n_1^{-1} \in H \cap N.$ Then we obtain 

$$\begin{align*}
\phi(h_1n_1) &= h_1(H \cap N) \\
&= (h_2n_2n_1^{-1})(H \cap N) \\
&= (h_2(H \cap N))((n_2n_1^{-1})(H \cap N)) \\
&= h_2(H \cap N) (H \cap N) \\
&=h_2(H \cap N) \\
&= \phi(h_2n_2),
\end{align*}$$

so $\phi$ is well-defined.$\big]$

**Claim 2:** $\phi$ is an epimorphism with $\ker(\phi) = N.$

$\big[(\because)$ Let $h_1n_1, h_2n_2 \in HN.$ Since $HN \le G,$ $(h_1n_1)(h_2n_2) \in HN.$ Let $(h_1n_1)(h_2n_2) = h_3n_3.$

Then 

$$\begin{align*}
\phi((h_1n_1)(h_2n_2)) &= \phi(h_3n_3) \\
&= h_3(H \cap N)
\end{align*}$$