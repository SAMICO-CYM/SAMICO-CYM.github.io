---
title: "Connected Graph"
date: 2026-04-21
categories: [Mathematics, Graph Theory]
tags: []
math: true
---

## Theorem 1
Let the relation $\sim_c$ be defined on $V(G)$ by 

$$u \sim_c v \iff \text{there is a } uv\text{-walk in } G.$$

Then $\sim_c$ is an equivalence relation on $V(G)$. 

### Proof
Let $u, v, w \in V(G)$.

Clearly, there is a $uu$-walk in $G$. **(reflexive)**

If there is a $uv$-walk in $G$, say $u = x_0, x_1, ..., x_k = v$, then there is a $vu$-walk in $G$, namely $v = x_k, x_{k-1}, ..., x_0 = u$. **(symmetric)**

If there is a $uv$-walk in $G$, say $u = x_0, x_1, ..., x_k = v$, and there is a $vw$-walk in $G$, say $v = y_0, y_1, ..., y_l = w$, then there is a $uw$-walk in $G$, namely $u = x_0, x_1, ..., x_k = v = y_0, y_1, ..., y_l = w$. **(transitive)**

Thus, $\sim_c$ is an equivalence relation on $V(G)$. $\blacksquare$

---

## Definition
**(i)** A graph $G$ is said to be ***connected*** if $u \sim_c v$ for all $u, v \in V(G)$.

**(ii)** Let $C$ be a equivalence class of $V(G)$ under $\sim_c$. The subgraph of $G$ induced by $C$ is called a ***component*** of $G$. 

---

## Theorem 2
**(i)** Each component of any graph is connected.

**(ii)** A graph is connected if and only if it has only one component.

### Proof
**(i)** Let $C$ be a component of $G$, and let $u, v \in V(C)$. Clearly $u \sim_c v$. 

**(ii)** 

$(\Longrightarrow)$

Suppose that a graph $G$ is connected. Since $u \sim_c v, \forall u, v \in V(G)$, there is only one equivalence class, that is $V(G)$. Therefore, $G$ has only one component.

$(\Longleftarrow)$

Suppose that a graph $G$ has only one component, say $C$. Then clearly $G = C$. By (i), $G$ is connected. $\blacksquare$

---

## Theorem 3
If a graph $G$ is disconnected, then its complement $\overline{G}$ is connected. 

### Proof
Suppose that $\overline{G}$ is disconnected. By Theorem 2 (ii), $\overline{G}$ has more than one components. Let $C_1, ..., C_n$ be the all components of $\overline{G}$. Then $u \not \sim_{\overline{G}} v, \forall u \in C_i, v \in C_j, i \ne j$, which is equivalent to $u \sim_{G} v, \forall u \in C_i, v \in C_j, i \ne j$. 

Let $x, y \in V(G)$. If $$