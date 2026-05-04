--- 
title: Direct Product Group
date: 2026-04-29
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Theorem 1
Let $G_1, ..., G_n$ be groups. Then $\displaystyle \prod_{i=1}^n G_i$ is a group under the binary operation defined by 

$$(a_1, \cdots, a_n) (b_1, \cdots, b_n) = (a_1b_1, \cdots, a_nb_n)$$

for all $(a_1, \cdots, a_n), (b_1, \cdots, b_n) \in \displaystyle \prod_{i=1}^n G_i$, and we call it the ***direct product*** of the groups $G_i$. 

### Proof
Let $a = (a_1, \cdots, a_n), b = (b_1, \cdots, b_n), c = (c_1, \cdots, c_n) \in \displaystyle \prod_{i=1}^n G_i$. Then 

$$\begin{align*}
ab &= (a_1, \cdots, a_n)(b_1, \cdots, b_n) \\
&= (a_1b_1, \cdots, a_nb_n) \\
& \in \prod_{i=1}^n G_i.
\end{align*}$$

Next, we have 

$$\begin{align*}
(ab)c &= ((a_1, \cdots, a_n)(b_1, \cdots, b_n))(c_1, \cdots, c_n) \\
&= (a_1b_1, \cdots, a_nb_n)(c_1, \cdots, c_n) \\
&= ((a_1b_1)c_1, \cdots, (a_nb_n)c_n) \\
&= (a_1(b_1c_1), \cdots, a_n(b_nc_n)) \\
&= (a_1, \cdots, a_n)((b_1, \cdots, b_n)(c_1, \cdots, c_n)) \\
&= a(bc).
\end{align*}$$

Next, let $e := (e_1, \cdots, e_n)$. Then $e \in \displaystyle \prod_{i=1}^n G_i$ and we have 

$$\begin{align*}
ea &= (e_1, \cdots, e_n)(a_1, \cdots, b_n) \\
&= (e_1a_1, \cdots, e_na_n) \\
&= (a_1, \cdots, a_n) \\
&= (a_1e_1, \cdots, a_ne_n) \\
&= (a_1, \cdots, a_n)(e_1, \cdots, e_n) \\
&= ae.
\end{align*}$$

Hence $e$ is the identity element of $\displaystyle \prod_{i=1}^n G_i$. 

Let $a^{-1} := (a^{-1}_1, \cdots, a^{-1}_n)$. Then we have 

$$\begin{align*}
a^{-1}a &= (a^{-1}_1, \cdots, a^{-1}_n)(a_1, \cdots, a_n) \\
&= (a^{-1}_1a_1, \cdots, a^{-1}_na_n) \\
&= (e_1, \cdots, e_n) \\
&= e \\
&= (e_1, \cdots, e_n) \\
&= (a_1a^{-1}_1, \cdots, a_na^{-1}_n) \\
&= (a_1, \cdots, a_n)(a^{-1}_1, \cdots, a^{-1}_n) \\
&= aa^{-1}.
\end{align*}$$

Thus, $\displaystyle \prod_{i=1}^n G_i$ is a group. $\blacksquare$

---

## Remark
Let $G := \displaystyle \prod_{i=1}^n G_i$.

**(i)** $G$ is abelian $\iff$ each $G_i$ is ablelian. In this case, we denote $\displaystyle \bigoplus_{i=1}^n G_i$, and we call $G$ the ***direct sum*** of the groups $G_i$.

**(ii)** $G$ is finite $\iff$ each $G_i$ is finite. 

**(iii)** $G$ is cyclic $\not\iff$ each $G_i$ is cyclic.

$\big[$$(\because)$ Note that $\mathbb{Z}_2 \times \mathbb{Z}_2 \cong V$ and $\mathbb{Z}_2 \times \mathbb{Z}_3 \cong \mathbb{Z}_6$. $\big]$

---

## Theorem 2
$\mathbb{Z}_m \times \mathbb{Z}_n$ is cyclic $\iff \gcd(m, n) = 1$. In this case, $\mathbb{Z}_m \times \mathbb{Z}_n \cong \mathbb{Z}_{mn}$.

### Proof

$(\Longrightarrow)$
Suppose that $\alpha = \gcd(m, n) \neq 1$. Then $m = \alpha k_1$ and $n = \alpha k_2$ for some $k_1, k_2 \in \mathbb{N}$ with $\gcd(k_1, k_2) = 1$. Since $\mathbb{Z}_m \times \mathbb{Z}_n$ is cyclic, it has a generator $(a, b)$. Then $r(a, b) \neq (0, 0), \forall r \in \\{ 1, ..., mn-1\\}$ because $\mathbb{Z}_m \times \mathbb{Z}_n$ has order $mn$. 

However, we have 

$$\begin{align*}
\frac{mn}{\alpha}(a, b) &= \left( \frac{n}{\alpha}ma, \frac{m}{\alpha} nb \right) \\
&= (k_2ma, k_1nb) \\
&= (0, 0)
\end{align*}$$ 

which is a contradiction. Therefore $\alpha = 1$.

$(\Longleftarrow)$
Suppose that $\gcd(m, n) = 1$. We claim that $r(1, 1) \neq s(1,1), \forall 0 \le r < s < mn$. 

---

## Corollary
$\displaystyle \prod_{i=1}^n \mathbb{Z}_{m_i}$ is cyclic $\iff \gcd(m_i, m_j) = 1$ for all $i \neq j$. In this case, $\displaystyle \prod_{i=1}^n \mathbb{Z}_{m_i} \cong \mathbb{Z}_{m_1 m_2 \cdots m_n}$.

### Proof

---

## Theorem 3
Let $(a_1, \cdots, a_n) \in \displaystyle \prod_{i=1}^n G_i$. If $\vert \langle a_i \rangle \vert = r_i$ in $G_i$, then $\vert \langle (a_1, \cdots, a_n) \rangle \vert = \mathrm{lcm}(r_1, \cdots, r_n)$ in $\displaystyle \prod_{i=1}^n G_i$.

### Proof

---

## Theorem 4 (Fundamental Theorem of Finitely Generated Abelian Groups)
**(i)** Every finitely generated abelian group $G$ is isomorphic to a direct product of cyclic groups in the form 

$$\mathbb{Z}_{p_1^{r_1}} \times \cdots \times \mathbb{Z}_{p_k^{r_k}} \times \mathbb{Z} \times \cdots \times \mathbb{Z}$$

where $p_i$ are not necessarily distinct primes and $r_i \in \mathbb{N}$.

**(ii)** The direct product as in (i) is unique except for possible rearrangement of the factors.

Furthermore, the number of $\mathbb{Z}$ in the direct product of cyclic groups in (i) is called the ***Betti number*** of $G$.