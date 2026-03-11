--- 
title: Isomorphism
date: 2026-03-09
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

$(\because)$ $\vert \mathbb{Q} \vert = \aleph_0 \lneq 2^{\aleph_0} = \vert \mathbb{R} \vert$.