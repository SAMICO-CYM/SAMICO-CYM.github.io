--- 
title: Path Connected
date: 2026-06-04
categories: [Mathematics, Topology]
tags: []
math: true
---

## Definition
Let $X$ be a topological space.

**(i)** For given $x, y \in X,$ a ***path*** in $X$ from $x$ to $y$ is defined as a continuous map $f: [a, b] \to X$ such that $f(a) = x$ and $f(b) = y.$ 

**(ii)** $X$ is said to be ***path connected*** if every pair of points of $X$ can be joined by a path in $X$, that is, any two points in $X$, there is a path between them.

---
## Theorem
**(i)** Every path connected space is connected.

**(ii)** Let $f: X \to Y$ be a continuous map. If a subspace $A$ of $X$ is path connected, then so is $f(A).$
### Proof
**(i)** Let $X$ be a path connected space. Suppose that $X$ is not connected. Then $X$ has a separation $(A, B).$ Since $A, B \neq \emptyset$ and $A \cap B = \emptyset,$ we can choose distinct two points $x \in A$ and $y \in B.$ Since $x, y \in X$ and $X$ is path connected, there is a path $p: [a, b] \to X$ from $x$ to $y$, i.e., $p$ is continuous and satisfies that $p(a) = x$ and $p(b) = y.$

[Since $p$ is continuous, $p([a, b])$ is also connected.](<{% post_url Topology/2026-05-27-Connected-Space %}#theorem-3>) Since $p([a, b]) \subset X$ and $X$ is not connected, [either $p([a, b]) \subset A$ or $p([a, b]) \subset B.$](<{% post_url Topology/2026-05-27-Connected-Space %}#lemma-2>) But it contradicts to the fact that $p(a) = x \in A$ and $p(b) = y \in B.$ Thus, $X$ is connected.

**(ii)** Let $x, y \in f(A).$ Then $f(a) = x$ and $f(b) = y$ for some $a, b \in A.$ Since $A$ is path connected, there is a path $p:[\alpha, \beta] \to A$ from $a$ to $b$. That is, $p$ is continuous and satisfies that $p(\alpha) = a$ and $p(\beta) = b.$ 

[Since $f$ is continuous, the restriction $g: A \to f(A)$ is also continuous.](<{% post_url Topology/2026-04-29-Continuous-Functions %}#theorem-3>) Furthermore, [the composition $g \circ p : [\alpha, \beta] \to f(A)$ is also continuous.](<{% post_url Topology/2026-04-29-Continuous-Functions %}#theorem-3>) Then $g \circ p$ is a path in $f(A)$ from $x$ to $y$ because 

$$(g \circ p)(\alpha) = g(p(\alpha)) = g(a) = f(a) = x$$

and 

$$(g \circ p)(\beta) = g(p(\beta)) = g(b) = f(b) = y.$$

Thus, $f(A)$ is path connected. $\blacksquare$