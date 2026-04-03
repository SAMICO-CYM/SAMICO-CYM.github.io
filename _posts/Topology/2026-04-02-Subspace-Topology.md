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
**(i)** Since $\emptyset = Y \cap \emptyset \in \mathcal{T}_Y$ and $Y = Y \cap X \in \mathcal{T}_Y$, the first condition is satisfied.

Let $\\{ U _ {\alpha} \\} \subset \mathcal{T}_Y$. Since each $U _ {\alpha} \in \mathcal{T}_Y$, we have $U _ {\alpha} = Y \cap V _ {\alpha}$ for some $V _ {\alpha} \in \mathcal{T}$, for each $\alpha$. Then

$$\bigcup U _ {\alpha} = \bigcup (Y \cap V _ {\alpha}) = Y \cap \bigcup V _ {\alpha}.$$

Since $\bigcup V _ {\alpha} \in \mathcal{T}$, we have $\bigcup U _ {\alpha} \in \mathcal{T}_Y$. 

Let $U_1, ..., U_n \in \mathcal{T}_Y$. Then $U_i = Y \cap V_i$ for some $V_i \in \mathcal{T}$, for each $i = 1, ..., n$. Then

$$\bigcap_{i=1}^n U_i = \bigcap_{i=1}^n (Y \cap V_i) = Y \cap \bigcap_{i=1}^n V_i.$$

Since $\bigcap_{i=1}^n V_i \in \mathcal{T}$, we have $\bigcap_{i=1}^n U_i \in \mathcal{T}_Y$. Thus $\mathcal{T}_Y$ is a topology on $Y$. 

**(ii)** Let $U \in \mathcal{T}_Y$. Then $U = Y \cap V$ for some $V \in \mathcal{T}$. Since $\mathcal{B}$ is a basis for $\mathcal{T}$ and $V$ is an open set in $X$, for each $x \in U = Y \cap V$ (so that $x \in V$), $\exists B \in \mathcal{B}$ such that $x \in B \subset V$. Since $x \in Y$, we have $x \in Y \cap B \subset Y \cap V = U$. Since $Y \cap B \in \mathcal{B}_Y$, $\mathcal{B}_Y$ is a basis generating $\mathcal{T}_Y$. $\blacksquare$

---

## Example
**(i)** Let $\mathcal{T}$ be the standard topology on $\mathbb{R}$, and let $Y = [0, 3] \subset \mathbb{R}$. Then $[0, 1) = Y \cap (-1, 1)$ so is open in $Y$. But $(-1, 1)$ is NOT open in $Y$. 

$(\because)$ If $(-1, 1)$ is open in $Y$, then $(-1, 1) = Y \cap (a, b)$ for some $(a, b) \in \mathcal{T}$. Note that $-0.5 \in (-1, 1)$ but $-0.5 \notin [0, 3] = Y$. $\bigotimes$ Thus $(-1, 1)$ is not open in $Y$.

**(ii)** Let $\mathcal{T}$ be the standard topology on $\mathbb{R}^2$, and let $Y = S^1$. Then each arc without the boundary points is open in $Y$.

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
Since $U$ is open in $Y$, $U = Y \cap V$ for some $V \in \mathcal{T}$. Since $Y$ is open in $X$ and $\mathcal{T}$ is a topology, $U = Y \cap V$ is open in $X$. $\blacksquare$

---

## Theorem 3
Let $(X, \mathcal{T}_X)$ and $(Y, \mathcal{T}_Y)$ be topological spaces, and let $A \subset X$ and $B \subset Y$. Let $(X \times Y, \mathcal{T} _ {X \times Y})$ be the product topological space, and let $(A, \mathcal{T}_A)$ and $(B, \mathcal{T}_B)$ be the subspace topologies on $A$ and $B$, respectively. Then the product topology on $A \times B$ is the same as the subspace topology on $A \times B$.

### Proof
Let $\mathcal{T}$ be the product topology on $A \times B$, and let $\mathcal{T}'$ be the subspace topology on $A \times B$. 