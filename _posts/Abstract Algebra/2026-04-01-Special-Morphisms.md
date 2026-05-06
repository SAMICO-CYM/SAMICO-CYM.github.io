---
title: Special Morphisms
date: 2026-04-01
categories: [Mathematics, Abstract Algebra]
math: true
---

## Definition
Let $G$ and $G'$ be groups. 

**(i)** A map $\phi: G \to G'$ is a ***homomorphism*** if 

$$\phi(ab) = \phi(a)\phi(b), \forall a, b \in G.$$

Let $\phi : G \to G'$ be a homomorphism.

**(ii)** If $\phi$ is injective, then $\phi$ is called a ***monomorphism***.

**(iii)** If $\phi$ is surjective, then $\phi$ is called an ***epimorphism***.

**(iv)** If $\phi$ is bijective, then $\phi$ is called an ***isomorphism***.

**(v)** If $\phi$ is an isomorphism and $G = G'$, then $\phi$ is called an ***automorphism***.

---

## Theorem
Let $\phi: G \to G'$ be a group homomorphism. Then

**(i)** $\phi(e_G) = e_{G'}$.

**(ii)** For each $a \in G$, $\phi(a^{-1}) = (\phi(a))^{-1}$

**(iii)** $H \le G \implies \phi(H) \le G'$

**(iv)** $K \le G' \implies \phi^{-1}(K) \le G$

### Proof
$\blacksquare$

---

## Example
Let $G, G'$ be groups.

**(i)** The map $\phi:G \to G'$ defined by 

$$\phi(g) = e_{G'}, \forall g \in G$$

is a homomorphism. We call such a map $\phi$ the ***trivial homomorphism***.

**(ii)** The identity map $id_G:G \to G$ defined by 

$$id_G(g) = g, \forall g \in G$$

is an automorphism. 

**(iii)** (Evaluation Homomorphism) Let $F = \mathbb{R}^{\mathbb{R}}$. Then clearly $\langle F, + \rangle$ is a group. For each $c \in \mathbb{R}$, define $\phi_c: F \to \mathbb{R}$ by 

$$\phi_c(f) = f(c), \forall f \in F$$

Then $\phi_c$ is a homomorphism. 

$(\because)$ Let $f, g \in F$. Then 

$$\begin{align*}
\phi_c(f+g) &= (f+g)(c) \\
&= f(c) + g(c) \\
&= \phi_c(f) + \phi_c(g),
\end{align*}$$

so $\phi_c$ is a homomorphism. 

Let $\alpha \in \mathbb{R}$. Define the function $f_{\alpha}: \mathbb{R} to \mathbb{R}$ by

$$f_{\alpha}(x) = \alpha, \forall x \in \mathbb{R}.$$ 

Then $f_{\alpha} \in F$ and $\phi_c(f_{\alpha}) = f_{\alpha}(c) = \alpha$. Thus $\phi_c$ is surjective, so that it is an epimorphism. 

**(iv)** (Linear Transformation) Let $A \in \mathbb{R}^{m \times n}$. Define $\phi: \mathbb{R}^n \to \mathbb{R}^m$ by 

$$\phi(x) = Ax, \forall x \in \mathbb{R}^n.$$

Then $\phi$ is a homomorphism. 

**(v)** Let $n \ge 2$. Define $\phi: \mathbb{Z} \to \mathbb{Z}_n$ by 

$$\phi(a) = a \pmod{n}, \forall a \in \mathbb{Z}.$$

Then $\phi$ is an epimorphism. 

$(\because)$ Let $a, b \in \mathbb{Z}$. Then $a \equiv r_1 \pmod{n}$ and $b \equiv r_2 \pmod{n}$ for some $r_1, r_2 \in \\{ 0, 1, ..., n-1 \\}$. Note that $a+b \equiv r_1 + r_2 \pmod{n}$. Then

$$\begin{align*}
\phi(a+b) &\equiv r_1 + r_2 \pmod{n} \\
&= \phi(a) + \phi(b),
\end{align*}$$

so $\phi$ is a homomorphism. 

Let $r \in \\{ 0, 1, ..., n-2 \\}$. Then clearly $\phi(r) = r$, so $\phi$ is surjective, hence it is an epimorphism. 

**(vi)** Define $\phi: \mathbb{C} \setminus \\{ 0 \\} \to \mathbb{R}^+$ by 

$$\phi(z) = \vert z \vert, \forall z \in \mathbb{C} \setminus \\{ 0 \\}.$$

Clearly, $\phi$ is a homomorphism. Note that $\mathrm{Ker}(\phi)$ is a unit circle in the complex plane.

**(vii)** Defined $\phi: S_n \to \mathbb{Z}_2$ by 

$$\phi(\sigma) = \begin{cases} 
0 & \text{if } \sigma \text{ is even} \\
1 & \text{if } \sigma \text{ is odd}
\end{cases}$$

for all $\sigma \in S_n$. Then clearly $\phi$ is an epimorphism.

**(viii)** Let $G = \displaystyle \prod_{i=1}^n G_i$ be a direct product of groups. For each $k \in \\{ 1, ..., n \\}$, define $\iota_k : G_k \to G$ by 

$$\iota_k(g_k) = (e_1, \cdots, e_{k-1}, g_k, e_{k+1}, \cdots, e_n), \forall g_k \in G_k.$$

Then $\iota_k$ is a monomorphism, but not epimorphism in general. The map $\iota_k$ is called the ***natural injection***.

Furthermore, For each $k \in \\{ 1, ..., n \\}$, define $\pi_k : G \to G_k$ by 

$$\pi_k(g_1, \cdots, g_n) = g_k, \forall (g_1, \cdots, g_n) \in G.$$

Then $\pi_k$ is an epimorphism, but not monomorphism in general. The map $\pi_k$ is called the ***canonical epimorphism***, or the ***projection map***.