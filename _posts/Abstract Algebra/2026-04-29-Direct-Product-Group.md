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

**(iii)** $G$ is cyclic ***NOT*** if and only if each $G_i$ is cyclic.

$\big[$$(\because)$ Note that $\mathbb{Z}_2 \times \mathbb{Z}_2 \cong V$, $\mathbb{Z}_3 \times \mathbb{Z}_3 \not \cong \mathbb{Z}_9$ and $\mathbb{Z}_2 \times \mathbb{Z}_3 \cong \mathbb{Z}_6$. $\big]$

---

## Theorem 2
$\mathbb{Z}_m \times \mathbb{Z}_n$ is cyclic $\iff$ $\gcd(m, n) = 1$. In this case, $\mathbb{Z}_m \times \mathbb{Z}_n \cong \mathbb{Z} _ {mn}$.

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

Suppose that $\gcd(m, n) = 1$. Note that $(1, 1) \in \mathbb{Z}_m \times \mathbb{Z}_n$. We claim that $r(1, 1) \neq s(1,1), \forall 0 \le r < s < mn$. 

$\big[(\because)$ Suppose that $r(1, 1) = s(1, 1)$ for some $0 \le r < s < mn$. Then $(s-r)(1, 1) = (s-r, s-r) = (0, 0) \in \mathbb{Z}_m \times \mathbb{Z}_n$, which implies that $m$ and $n$ divide $s-r$. Since $\gcd(m ,n) = 1$, $mn$ divides $s-r$, which implies that $mn \le s-r$. But we have $s-r < mn$. $\bigotimes$ $\big]$

Note that $mn(1, 1) = (mn, mn) = (0, 0)$. Thus, $\vert (1, 1) \vert = mn$, which means that $\mathbb{Z}_m \times \mathbb{Z}_n = \langle (1, 1) \rangle. \blacksquare$

---

## Corollary
$\displaystyle \prod_{i=1}^n \mathbb{Z} _ {m_i}$ is cyclic $\iff \gcd(m_i, m_j) = 1$ for all $i \neq j$. In this case, $\displaystyle \prod_{i=1}^n \mathbb{Z} _ {m_i} \cong \mathbb{Z} _ {m_1 m_2 \cdots m_n}$.

### Proof
We use the induction on $n$. The case when $n=2$ was shown in Theorem 11.5

Suppose that there exists $t \ge 2$ such that 

$$\prod_{i=1}^t \mathbb{Z} _ {m_i} \cong \mathbb{Z} _ {m_1 \cdots m_t} \iff \gcd(m_i, m_j) = 1, \forall 1 \le i < j \le t.$$

Note that 

$$\prod_{i=1}^{t+1} \mathbb{Z} _ {m_i} \cong \left( \prod_{i=1}^t \mathbb{Z} _ {m_i} \right) \times \mathbb{Z} _ {m_{t+1}}.$$

By the induction hypothesis and Theorem 2, we have 

$$\prod_{i=1}^{t+1} \mathbb{Z} _ {m_i} \cong \mathbb{Z} _ {m_1 \cdots m_{t+1}} \iff \gcd(m_1 \cdots m_t, m_{t+1}) = 1 \iff \gcd(m_i, m_{t+1}) = 1, \forall 1 \le i \le t.$$

Hence, for all $n \ge 2$, we have

$$\displaystyle \prod_{i=1}^n \mathbb{Z} _ {m_i} \cong \mathbb{Z} _ {m_1 m_2 \cdots m_n} \iff \gcd(m_i, m_j) = 1, \forall i \neq j. \quad \blacksquare$$

---
## Example 1
**(i)** Let $n = p_1^{r_1} \cdots p_m^{r_m}$ be the prime factorization of $n$, where $p_1, \cdots, p_r$ are distinct primes. Then $\mathbb{Z}_n \cong \mathbb{Z} _ {p_1^{r_1}} \times \cdots \times \mathbb{Z} _ {p_m^{r_m}}$. 

**(ii)** $\mathbb{Z} _ {72} = \mathbb{Z}_8 \times \mathbb{Z}_9$.  

---

## Theorem 3
Let $(a_1, \cdots, a_n) \in \displaystyle \prod_{i=1}^n G_i$. If $\vert \langle a_i \rangle \vert = r_i$ in $G_i$, then $\vert \langle (a_1, \cdots, a_n) \rangle \vert = \mathrm{lcm}(r_1, \cdots, r_n)$ in $\displaystyle \prod_{i=1}^n G_i$.

### Proof
Let $\vert \langle (a_1, \cdots, a_n) \rangle \vert = m$. Then 

$$(a_1^m, \cdots, a_n^m) = (a_1, \cdots, a_n)^m = (e_1, \cdots, e_n),$$

so that each $r_i$ divides $m$. Hence $m$ is a common multiple of $r_1, ..., r_n$. 

Suppose that there exists a common multiple $t \in \mathbb{N}$ of $r_1, ..., r_n$. Then we have 

$$(a_1, \cdots, a_n)^t = (a_1^t, \cdots, a_n^t) = (e_1, \cdots, e_n).$$

Since $\vert \langle (a_1, \cdots, a_n) \rangle \vert = m$, we have $m \vert t$. Thus, $m = \mathrm{lcm}(r_1, \cdots, r_n)$. $\blacksquare$

---
## Example 2
**(i)** Let $(8, 4, 10) \in \mathbb{Z} _ {12} \times \mathbb{Z} _ {60} \times \mathbb{Z} _ {24}$. Then $\vert \langle 8 \rangle \vert = 3, \vert \langle 4 \rangle \vert = 15$ and $\vert \langle 10 \rangle \vert = 12$. By Theorem 3, $\vert \langle (8, 4, 10) \rangle \vert = \mathrm{lcm}(3, 15, 12) = 60$.

**(ii)** $\mathbb{Z} \times \mathbb{Z}_2 = \langle (1, 0), (0, 1) \rangle$ 

**(iii)** $\mathbb{Z} _ {m_1} \times \cdots \times \mathbb{Z} _ {m_n} = \langle (1, 0, \cdots, 0), (0, 1, 0, \cdots, 0), \cdots, (0, \cdots, 0, 1) \rangle$

**(iv)** $\mathbb{Z} _ 3 \times \mathbb{Z} _ 4 \times \mathbb{Z} _ {35} = \langle (1, 1, 1) \rangle$.  

(ii)와 (ii)의 경우,  finite가 아니거나 서로소라는 보장이 없으면 cyclic으로 나타낼 수 없지만 finitely generated set은 항상 된다는 사실을 보여준다. 반면 (iv)는 finite하면서 모두 서로소이므로 one-generated set, 즉 cyclic group이 된다.

---

## Theorem 4 (Fundamental Theorem of Finitely Generated Abelian Groups)
**(i)** Every finitely generated abelian group $G$ is isomorphic to a direct product of cyclic groups in the form 

$$\mathbb{Z}_{p_1^{r_1}} \times \cdots \times \mathbb{Z}_{p_k^{r_k}} \times \mathbb{Z} \times \cdots \times \mathbb{Z}$$

where $p_i$ are not necessarily distinct primes and $r_i \in \mathbb{N}$.

**(ii)** The direct product as in (i) is unique except for possible rearrangement of the factors.

Furthermore, the number of $\mathbb{Z}$ in the direct product of cyclic groups in (i) is called the ***Betti number*** of $G$.