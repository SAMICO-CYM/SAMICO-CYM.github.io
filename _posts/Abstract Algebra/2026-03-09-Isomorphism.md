--- 
title: Isomorphism
date: 2026-03-09 00:00:01
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Definition
Let $(S, \ast)$ and $(T, \ast')$ be binary algebraic structures.

**(i)** A ***homomorphism*** of $S$ with $T$ is a function $\phi : S \to T$ such that 

$$\phi(x \ast y) = \phi(x) \ast' \phi(y) \forall x, y \in S.$$

**(ii)** If a homomorphsim $\phi : S \to T$ is bijective, then $\phi$ is called an ***isomorphism*** of $S$ with $T$.

**(iii)** If an isomorphism $\phi : S \to T$ of $S$ with $T$ exists, then $S$ and $T$ are said to be ***isomorphic*** binary structures and we denote by $S \cong T$ (or $S \simeq T$).

---

## Theorem
Let $\phi : (S, \ast) \to (T, \ast')$ be an isomorphism of $(S, \ast)$ with $(T, \ast')$. If $e$ is the identity element of $(S, \ast)$, then $\phi(e)$ is the identity element of $(T, \ast')$.

### Proof
Let $t \in T$. Then $\exists s \in S$ such that $\phi(s) = t$ because $\phi$ is surjective. Thus we have

$$\begin{align*}
\phi(e) \ast' t & = \\
&= \phi(e) \ast' \phi(s) = \\
&= \phi(e \ast s) \\
&= \phi(s) \\
&= t,
\end{align*}$$ 

and similarly $t \ast' \phi(e) = t$. Hence $\phi(e)$ is the identity element of $(T, \ast')$. $\blacksquare$

증명 과정을 보면 알겠지만 사실 one-to-one 조건은 필요하지 않다. 즉 $\phi$가 homomorphism이면서 onto이기만 하면 충분하다.

---

## Example
**(i)** $(\mathbb{R}, +) \cong (\mathbb{R}^+, \cdot)$.

$(\because)$ Define $\phi : (\mathbb{R}, +) \to (\mathbb{R}^+, \cdot)$ by

$$\phi(r) = 2^r, \forall r \in \mathbb{R}$$

Then $\phi$ is clearly bijective. Let $a, b \in \mathbb{R}$. Since

$$ \begin{align*}
\phi(a + b) &= 2^{a + b} \\
&= 2^a \cdot 2^b \\
&= \phi(a) \cdot \phi(b),
\end{align*}$$

$\phi$ is an isomorphism.

**(ii)** $(\mathbb{Z}, +) \cong (2\mathbb{Z}, +)$.

($\because$) Define $\phi : \mathbb{Z} \to 2\mathbb{Z}$ by

$$\phi(a) = 2a, \forall a \in \mathbb{Z}.$$

Then $\phi$ is clearly bijective. Let $a, b \in \mathbb{Z}$. Since

$$ \begin{align*}
\phi(a + b) &= 2(a + b) \\
&= 2a + 2b \\
&= \phi(a) + \phi(b),
\end{align*}$$

$\phi$ is an isomorphism.

**(iii)** $(\mathbb{Q}, +) \not\cong (\mathbb{R}, +)$. 

$(\because)$ Since $\vert \mathbb{Q} \vert = \aleph_0 \lneq 2^{\aleph_0} = \vert \mathbb{R} \vert$, there does not exist a bijection between $\mathbb{Q}$ and $\mathbb{R}$. 

**(iv)** $(\mathbb{Q}, +) \not\cong (\mathbb{Z}, +)$.

($\because$) Suppose that there is an isomorphism $\phi$ of $(\mathbb{Q}, +)$ with $(\mathbb{Z}, +)$. Note that $\phi(q) = 1$ for some $q \in \mathbb{Q}$. Then

$$\begin{align*}
\phi(q) &= \phi \left( \frac{q}{2} + \frac{q}{2} \right) \\
&= \phi \left( \frac{q}{2} \right) + \phi \left( \frac{q}{2} \right) \\
&= 2 \phi \left( \frac{q}{2} \right) \\
&= 1.
\end{align*}$$ 

Note that $\phi \left( \frac{q}{2} \right) \in \mathbb{Z}$ but there is no $x \in \mathbb{Z}$ such that $2x = 1$. $\bigotimes$ Thus $\phi$ is not an isomorphism.

**(v)** $(\mathbb{C}, \cdot) \not\cong (\mathbb{R}, \cdot)$.

($\because$) Suppose that there is an isomorphism $\phi$ of $(\mathbb{C}, \cdot)$ with $(\mathbb{R}, \cdot)$. Note that $\phi(z^2) = -1$ for some $z \in \mathbb{C}$. Then

$$\begin{align*}
\phi(z^2) &= \phi(z \cdot z) \\
&= \phi(z) \cdot \phi(z) \\
&= (\phi(z))^2 \\
&= -1.
\end{align*}$$ 

Note that $(\phi(z))^2 = -1$ has no solution in $\mathbb{R}$. $\bigotimes$ Thus $\phi$ is not an isomorphism.

**(vi)** $(\mathbb{R}^{2 \times 2}, \cdot) \not\cong (\mathbb{R}, \cdot)$.

($\because$) Suppose that there is an isomorphism $\phi$ of $(\mathbb{R}^{2 \times 2}, \cdot)$ with $(\mathbb{R}, \cdot)$. Let $A, B \in \mathbb{R}^{2 \times 2}$. Then

$$\begin{align*}
\phi(A \cdot B) &= \phi(A) \cdot \phi(B) \\
&= \phi(B) \cdot \phi(A) \\
&= \phi(B \cdot A),
\end{align*}$$

which means that $A \cdot B = B \cdot A$ for all $A, B \in \mathbb{R}^{2 \times 2}$. $\bigotimes$ Thus $\phi$ is not an isomorphism. 