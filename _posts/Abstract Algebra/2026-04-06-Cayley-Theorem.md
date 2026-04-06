---
title: Cayley's Theorem
date: 2026-04-06
categories: [Mathematics, Abstract Algebra]
math: true
---

## Lemma
Let $\phi:G \to G'$ be a monomorphism of groups. Then $\operatorname{Im}(\phi) \le G'$ and $\operatorname{Im}(\phi) \cong G$.

### Proof 

Since $\phi$ is a homomorphism, clearly $\operatorname{Im}(\phi) = \phi(G) \le G'$.

Define a function $f: G \to \phi(G)$ by $f(g) = \phi(g)$ for all $g \in G$. Since $\phi$ is a monomorphism, $f$ is injective. Clearly $f$ is surjective, so that $f$ is an isomorphism. Thus, $\operatorname{Im}(\phi) \cong G$. $\blacksquare$

## Cayley's Theorem
Every group is isomorphic to a subgroup of $S_A$ for some set $A$.

### Proof