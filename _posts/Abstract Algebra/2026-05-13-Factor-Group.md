--- 
title: Factor Group
date: 2026-05-13
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Theorem 1
Let $H \le G$. We denote $G / H = \\{ aH \mid a \in G \\}$. Then the operation on $G / H$ defined by 

$$(aH)(bH) = (ab)H, \forall a , b \in G$$

is well-defined $\iff$ $H \lhd G$.

### Proof
$(\Longrightarrow)$

Suppose that the operation is well-defined. We will show that $aH = Ha, \forall a \in G$.

Let $a \in G$. If $x \in aH$, then we have $xH = aH$, so that 

$$\begin{align*}
(xa^{-1})H &= (xH)(a^{-1}H) \\
&= (aH)(a^{-1}H) \\
&= (aa^{-1})H \\
&= eH \\
&= H.
\end{align*}$$

Thus, $xa^{-1} \in H$, which means that $x \in Ha$. Hence, $aH \subset Ha$.

Conversely, if $x \in Ha$, then we have $x = ha$ for some $h \in H$. Since $a^{-1} = x^{-1}h \in x^{-1}H$, we have $a^{-1}H = x^{-1}H$, and therefore 

$$\begin{align*}
(a^{-1}x)H &= (a^{-1}H)(xH) \\
&= (x^{-1}H)(xH) \\
&= (x^{-1}xH) \\
&= H.
\end{align*}$$

Thus, $a^{-1}x \in H$, which means that $x \in aH$. Hence, $Ha \subset aH$, so that $aH = aH.

$(\Longleftarrow)$

Suppose that $aH = Ha, \forall a \in G$. We assume that $a_1H = a_2H$ and $b_1H = b_2H$. We will show that $(a_1b_1)H = (a_1H)(b_1H) = (a_2H)(b_2H) = (a_2b_2)H$.

Let $x \in (a_1b_1)H$. Then $x = a_1b_1h$ for some $h \in H$. Since $b_1h \in b_1H$ and $b_1H = b_2H$, $b_1h \in b_2H$, which means that $b_1h = b_2h_1$ for some $h_1 \in H$. Then $x = a_1b_2h_1$.

Since $b_2h_1 \in b_2H$ and $b_2H = Hb_2$, $b_2h_1 \in Hb_2$, which means that $b_2h_1 = h_2b_2$ for some $h_2 \in H$. Then $x = a_1h_2b_2$.

Since $a_1h_2 \in a_1H$ and $a_1H = a_2H$, $a_1h_2 \in a_2H$, which means that $a_1h_2 = a_2h_3$ for some $h_3 \in H$. Then $x = a_2h_3b_2$.

Since $h_3b_2 \in Hb_2$ and $Hb_2 = b_2H$, $h_3b_2 \in b_2H$, which means that $h_3b_2 = b_2h_4$ for some $h_4 \in H$. Then $x = a_2b_2h_4$. Thus, $x \in (a_2b_2)H$, and therefore $(a_1b_1)H \subset (a_2b_2)H$.

Similarly, we also have $(a_2b_2)H \subset (a_1b_1)H$. Hence, $(a_1b_1)H = (a_2b_2)H$. $\blacksquare$

---
## Corollary
Let $H \lhd G$. Then $G / H$ is a group under the binary operaton defined above theorem. 

### Proof
By Theorem 1, the operation is well-defined.

Let $a, b, c \in G$. Then we have 

$$\begin{align*}
[(aH)(bH)](cH) &= [(ab)H](cH) \\
&= [(ab)c]H \\
&= [a(bc)]H \\
&= (aH)[(bc)H] \\
&= (aH)[(bH)(cH)].
\end{align*}$$

Thus, the operation is associative.

Note that 

$$\begin{align*}
(aH)(eH) &= (ae)H \\
&=aH \\
&=(ae)H \\
&= (aH)(eH).
\end{align*}$$

Thus, $eH (=H)$ is the identity element in $G/H$.

Note that 

$$\begin{align*}
(aH)(a^{-1}H) &= (aa^{-1})H \\
&= eH \\
&= (a^{-1}a)H\\
&= (a^{-1}H)(aH).
\end{align*}$$

Thus, each element $aH$ in $G/H$ has the inverse and $(aH)^{-1} = a^{-1}H$. Hence, $G/H$ is a group. $\blacksquare$

---
## Definition
Let $H \lhd G$. The group $G/H$ is called the ***factor group*** (or ***quotient group***) of $G$ by $H$. 

---
## Remark
**(i)** If $G$ is abelian and $H \lhd G$, then $G / H$ is abelian.

**(ii)** $G /H$ being abelian does not imply that $G$ is abelian.

$\big[(\because)$ Note that $A_n \le S_n$ and $\vert A_n \vert = \frac{n!}{2}$. Then we have $(S_n:A_n) = \frac{\vert S_n \vert}{\vert A_n \vert} = 2$ by [Remark 2 (ii).](<{% post_url Abstract Algebra/2026-04-27-Coset %}#remark-2>), and therefore $A_n \lhd S_n$ by [Theorem 3.](<{% post_url Abstract Algebra/2026-04-27-Coset %}#theorem-3>) For all $n \ge 3$, $S_n/A_n \cong \mathbb{Z}_2$ is abelian, but $S_n$ is not abelian.$\big]$

**(iii)** For $n \in \mathbb{N}$, we have $n\mathbb{Z} \lhd \mathbb{Z}$ because $\mathbb{Z}$ is abelian. Then $\mathbb{Z}/n\mathbb{Z}$ is the factor group of $\mathbb{Z}$ by $n\mathbb{Z}$. In particular, $\mathbb{Z}/n\mathbb{Z} \cong \mathbb{Z}_n$.

**(iv)** Note that $\ker(\phi) \lhd G$ for a group homomorphism $\phi : G \to G'$ by [Theorem 1.](<{% post_url Abstract Algebra/2026-05-06-Kernel %}#theorem-1>) Then $G/\ker(\phi)$ is a factor group of $G$ by $\ker(\phi)$. 

**(v)** $G / \\{ e \\} \cong G$ and $G / G \cong \\{ e \\}$.