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
\end{align*}$$ and similarly $t \ast' \phi(e) = t$. Hence $\phi(e)$ is the identity element of $(T, \ast')$.