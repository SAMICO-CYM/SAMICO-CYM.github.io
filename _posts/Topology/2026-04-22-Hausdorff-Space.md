---
title: "Hausdorff Space"
date: 2026-04-22
categories: [Mathematics, Topology]
tags: []
math: true
---

## Definition
A topological space $X$ is called a ***Hausdorff space*** if for each pair $x_1, x_2 \in X$ of distinct points of $X$, there exist neighborhoods $U_1$ and $U_2$ of $x_1$ and $x_2$, respectively, such that $U_1 \cap U_2 = \emptyset$.

---

## Theorem 1
A topological space $X$ is a Hausdorff space if and only if every singleton set in $X$ is closed in $X$.

### Proof 
$(\Longrightarrow)$

Suppose that $X$ is a Hausdorff space. Let $x \in X$. 

**Claim**: $\\{x\\}' = \emptyset$. 

$\Big[$ $(\because)$ Assume that $\\{x \\}' \neq \emptyset$. Then there is some element $y \in \\{ x \\}'$. By definition, for any neighborhood $U$ of $y$, we have $U \cap (\\{ x \\} - \\{ y \\}) \neq \emptyset$. If $y = x$, then we have $U \cap \emptyset = \emptyset$. $\bigotimes$ Thus $y \neq x$. 

Since $X$ is a Hausdorff space, there exist neighborhoods $U_1$ and $U_2$ of $x$ and $y$, respectively, such that $U_1 \cap U_2 = \emptyset$. Then we have 

$$\begin{align*}
U_2 \cap (\{ x \} - \{ y \}) = U_2 \cap \{ x \} \subset U_2 \cap U_1 = \emptyset.
\end{align*}$$ 

But $U_2 \cap (\\{ x \\} - \\{ y \\}) \neq \emptyset$. $\bigotimes$ Thus $\\{ x \\}' = \emptyset$ $\Big]$