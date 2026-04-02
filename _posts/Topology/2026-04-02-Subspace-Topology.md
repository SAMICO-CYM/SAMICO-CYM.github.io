---
title: "Subspace Topology"
date: 2026-04-02
categories: [Mathematics, Topology]
math: true
---

## Theorem 1
Let $(X, \mathcal{T})$ be a topological space and let $Y \subset X$. 

**(i)** The collection

$$\mathcal{T}_Y = \{ Y \cap U \mid U \in \mathcal{T} \}$$

is a topology on $Y$. We call $\mathcal{T}_Y$ the ***subspace topology*** on $Y$, and call $(Y, \mathcal{T}_Y)$ a ***subspace*** of $(X, \mathcal{T})$.

**(ii)** If $\mathcal{B}$ is a basis for $\mathcal{T}$, then

$$\mathcal{B}_Y = \{ Y \cap B \mid B \in \mathcal{B} \}$$

is a basis for $\mathcal{T}_Y$.

### Proof

---

## Example

---

## Definition
Let $(X, \mathcal{T})$ be a topological space, and let $(Y, \mathcal{T}_Y)$ be a subspace of $(X, \mathcal{T})$. We say that $U$ is ***open in $Y$*** if $U \in \mathcal{T}_Y$, that is, $U = Y \cap V$ for some $V \in \mathcal{T}$.

---

## Note
- $\mathcal{T}$ and $\mathcal{T}_Y$ are NOT comparable in general. That is, an open set $U \in \mathcal{T}$ is not necessarily open in $Y$, and an open set $V \in \mathcal{T}_Y$ is not necessarily open in $X$.

---

## Theorem 2
Let $(Y, \mathcal{T}_Y)$ be a subspace of $(X, \mathcal{T})$. If $U$ is open in $Y$ and $Y$ is open in $X$, then $U$ is open in $X$. 

### Proof

---

## Theorem 3
Let $(X, \mathcal{T}_X)$ and $(Y, \mathcal{T}_Y)$ be topological spaces, and let $A \subset X$ and $B \subset Y$. Let $(X \times Y, \mathcal{T} _ {X \times Y})$ be the product topological space, and let $(A, \mathcal{T}_A)$ and $(B, \mathcal{T}_B)$ be the subspace topologies on $A$ and $B$, respectively. Then the product topology on $A \times B$ is the same as the subspace topology on $A \times B$.

### Proof