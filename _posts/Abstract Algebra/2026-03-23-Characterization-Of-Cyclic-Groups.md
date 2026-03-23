---
title: Characterization Of Cyclic Groups
date: 2026-03-23 00:00:01
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Theorem
Let $G$ be a cyclic group.

**(i)** If $\vert G \vert = \infty$, then $G \cong (\mathbb{Z}, +)$.

**(ii)** If $\vert G \vert = n \in \mathbb{N}$, then $G \cong (\mathbb{Z}_n, +)$.

### Proof
Let $G = \langle a \rangle$, and let $e$ denote the identity of $G$.

**(i)** Suppose that $\vert G \vert = \infty$. Then $a^m \neq a^n, \forall m \neq n \in \mathbb{Z}$.

$\Big[ (\because)$ Suppose that $a^m = a^n$ for some integers $m > n$. Then $a^{m - n} = e$. We claim $G = \\{ e, a, a^2, \cdots, a^{m - n - 1} \\}$.
\\
$\Big[ (\because)$ Since $a \in G$, clearly $G \supset \\{ e, a, a^2, \cdots, a^{m - n - 1} \\}$. Let $x \in G$. Then $x = a^k$ for some $k \in \mathbb{Z}$. By division algorithm, $\exists \, q, r \in \mathbb{Z}$ such that $k = (m - n)q + r$ and $0 \le r < m - n$. Then we have 

$$\begin{align*}
x &= a^k \\
&= a^{(m-n)q + r} \\
&= (a^{m - n})^q a^r \\
&= a^r \in \{ e, a, a^2, \cdots, a^{m - n - 1} \}. \Big]
\end{align*}$$

Thus $G = \\{ e, a, a^2, \cdots, a^{m - n - 1} \\}$, so that $\vert G \vert = m - n < \infty$. $\bigotimes$ Hence $a^m \neq a^n, \forall m \neq n \in \mathbb{Z}$. $\Big]$

Define the function $\phi : G \to \mathbb{Z}$ by $\phi(a^m) = m, \forall a^m \in G$. Clearly $\phi$ is well-defined. 

If $\phi(a^m) = \phi(a^n)$, then $m = n$, so that $a^m = a^n$. Thus $\phi$ is injective. 

Let $m \in \mathbb{Z}$. Then $a^m \in G$, so that $\phi(a^m) = m$. Thus $\phi$ is surjective.

Let $a^m, a^n \in G$. Then 

$$
\begin{align*}
    \phi(a^m a^n) &= \phi(a^{m + n}) \\
    &= m + n \\
    &= \phi(a^m) + \phi(a^n).
\end{align*}
$$

Thus $\phi$ is a homomorphism, and so that $G \cong (\mathbb{Z}, +)$.

**(ii)** Suppose that $\vert G \vert = n \in \mathbb{N}$. Then $a^i \neq a^j, \forall 0 \le i < j \le n-1$.

$\Big[ (\because)$ If $a^i = a^j$ for some $0 \le i < j \le n-1$, then $a^{j-i} = e$, which means that $G = \\{ e, a, a^2, \cdots, a^{j - i - 1} \\}$. Thus $\vert G \vert = j - i \le n-1$. $\bigotimes$ Hence $a^i \neq a^j, \forall 0 \le i < j \le n-1$. $\Big]$

Since $G = \langle a \rangle$, we have $G = \\{ e, a, a^2, \cdots, a^{n-1} \\}$. Then $a^n = e$ because $a^n \in G$ so that $a^n = a^k$ for some $0 \le k < n-1$ and $a^{n-k} = e$ with $n-k \in \{ 1, 2, \cdots, n-1 \}$. $\bigotimes$

Define the function $\phi : G \to \mathbb{Z}_n$ by $\phi(a^m) = m \pmod n, \forall a^m \in G$. By division algorithm, $\phi$ is well-defined. Note that if $m \equiv r \pmod n$, then $a^m = a^r$.

If $\phi(a^m) = \phi(a^k)$, then $m \equiv k \pmod n$. so that $a^m = a^k$. Thus $\phi$ is injective. 

Let $m \in \mathbb{Z}_n$, that is, $m \equiv m \pmod n$. Then $a^m \in G$, so that $\phi(a^m) = m$. Thus $\phi$ is surjective.

Let $a^m, a^k \in G$, and let $m \equiv r_1 \pmod n$ and $k \equiv r_2 \pmod n$ with $0 \le r_1, r_2 \le n-1$. Then 

$$
\begin{align*}
    \phi(a^m a^k) &= \phi(a^{m + k}) \\
    &= m + k \pmod n \\
    &= r_1 + r_2 \pmod n \\
    &= r_1 + r_2 \\
    &= \phi(a^m) + \phi(a^k).
\end{align*}
$$

Thus $\phi$ is a homomorphism, and so that $G \cong (\mathbb{Z}_n, +)$. $\blacksquare$

---

## Remark
Let $G = \langle a \rangle$ with $\vert G \vert = n$. 

**(i)** $n$ is the smallest positive integer such that $a^n = e$.

**(ii)** $a^m = e$ for some $m \in \mathbb{Z} \setminus \\{ 0 \\} \iff n \vert m$.

---

## Example
Let $U_n = \\{ z \in \mathbb{C} \mid z^n = 1 \\}$. Then $(U_n, \cdot) \cong (\mathbb{Z}_n, +)$.