---
title: "Hausdorff Space"
date: 2026-04-22
categories: [Mathematics, Topology]
tags: []
math: true
---

## Definition
Let $X$ be a topological space.

(i) We say that $X$ satisfies ***$T_1$ axiom***, or $X$ is a ***$T_1$ space***, if every finite set in $X$ is closed in $X$.

(ii) $X$ is called a ***Hausdorff space***, or ***$T_2$ space***, if for each pair $x_1, x_2 \in X$ of distinct points of $X$, there exist neighborhoods $U_1$ and $U_2$ of $x_1$ and $x_2$, respectively, such that $U_1 \cap U_2 = \emptyset$.

---

## Theorem 1
Every singleton set in a Hausdorff space is closed. 

### Proof 
Let $X$ be a Hausdorff space, and let $x \in X$. 

**Claim**: $\\{x\\}' = \emptyset$. 

$\Big[$ $(\because)$ Assume that $\\{x \\}' \neq \emptyset$. Then there is some element $y \in \\{ x \\}'$. By definition, for any neighborhood $U$ of $y$, we have $U \cap (\\{ x \\} - \\{ y \\}) \neq \emptyset$. If $y = x$, then we have $U \cap \emptyset = \emptyset$. $\bigotimes$ Thus $y \neq x$. 

Since $X$ is a Hausdorff space, there exist neighborhoods $U_1$ and $U_2$ of $x$ and $y$, respectively, such that $U_1 \cap U_2 = \emptyset$. Then we have 

$$\begin{align*}
U_2 \cap (\{ x \} - \{ y \}) = U_2 \cap \{ x \} \subset U_2 \cap U_1 = \emptyset.
\end{align*}$$ 

But $U_2 \cap (\\{ x \\} - \\{ y \\}) \neq \emptyset$. $\bigotimes$ Thus $\\{ x \\}' = \emptyset$ $\Big]$

Hence, $\\{ x \\}$ is closed in $X$. $\blacksquare$

---

## Corollary 
Every finite set in a Hausdorff space is closed. 

### Proof
Let $\\{ x_1, ..., x_n \\}$ be a finite set in a Hausdorff space $X$. Since $\\{ x_1, ..., x_n \\} = \\bigcup_{i=1}^n \\{ x_i \\}$ and $\\{ x_i \\}$ is closed in $X$ for each $i$ by Theorem 1, it follows that $\\{ x_1, ..., x_n \\}$ is closed in $X$ by the definition of a topology. $\blacksquare$

---

## Remark

위 정리에 의해 하우스도르프 공간이면 $T_1$ 공간임이 보장되지만, 그 역은 성립하지 않는다. 예를 들어 실수 공간 위에서 정의된 cofinite topology $\mathcal{T}_c$를 고려하자. $\mathcal{T}_c$에서 공집합이 아닌 이상 모든 열린 집합은 $\mathbb{R} - \\{ x_1, ..., x_n \\}$의 형태를 가지므로, 임의의 유한 집합 $\\{ x_1, ..., x_n \\}$은 닫힌 집합이다. 즉 $(\mathbb{R}, \mathcal{T}_c)$는 $T_1$ 공간이다.

그러나 하우스도르프 공간은 아닌데, 서로 다른 두 점 $x_1, x_2$를 실수 위에서 가지고 오면 두 점을 포함하는 열린 집합을 어떻게 가지고 와도 항상 두 집합은, 위에서 살펴본 바와 같이, 실수의 양 끝으로 뻗어나가는 구간을 포함하고 있을 수 밖에 없고, 따라서 항상 교집합을 가지기 때문이다.

---

## Theorem 2
Let $X$ be a space satisfying the $T_1$ axiom, and let $A \subset X$. Then $x \in A'$ $\iff$ every neighborhood of $x$ contains infinitely many points of $A$.

### Proof
$(\Longrightarrow)$
Let $x \in A'$. Then for any neighborhood $U$ of $x$, we have $A \cap (U - \\{x\\}) \neq \emptyset$. Suppose that there is some neighborhood $U$ of $x$ such that $U \cap A$ is finite. Then $U \cap (A - \\{ x \\})$ is also finite, and we denote $U \cap (A - \\{ x \\}) = \\{ x_1, ..., x_n \\}$. 

Since $X$ is a $T_1$ space, $\\{ x_1, ..., x_n \\}$ is closed in $X$, so that $X - \\{ x_1, ..., x_n \\}$ is open in $X$. Then $U \cap (X - \\{ x_1, ..., x_n \\}) = U - \\{ x_1, ..., x_n \\}$ is also open in $X$. Since $x \notin U \cap (A - \\{ x \\}) = \\{ x_1, ..., x_n \\}$, we have that $x \in U - \\{ x_1, ..., x_n \\}$, which means that $U - \\{ x_1, ..., x_n \\}$ is a neighborhood of $x$.

Then 

$$(U - \\{ x_1, ..., x_n \\}) \cap (A - \\{ x \\}) \neq \emptyset$$

by assumption. But $U \cap (A - \\{ x \\}) = \\{ x_1, ..., x_n \\}$, so that

$$(U - \\{ x_1, ..., x_n \\}) \cap (A - \\{ x \\}) = \\emptyset. \bigotimes$$

Thus, every neighborhood of $x$ contains infinitely many points of $A$. 

$(\Longleftarrow)$
Let $U$ be a neighborhood of $x$. Then $U$ contains infinitely many points of $A$. Then $A \cap (U - \\{ x \\})$ also contains infinitely many points of $A$, which means that it is not empty. Thus $x \in A'$. $\blacksquare$

---

## Theorem 3
If $X$ is a Hausdorff space, then a sequence of points of $X$ converges to at most one point of $X$.

### Proof
Let $\\{ x_n \\}$ be a sequence of points of $X$. If $\\{ x_n \\}$ does not converge to some point of $X$, then we are done. Suppose that $\\{ x_n \\}$ converges to two distinct points $x$ and $y$ of $X$. Since $X$ is Hausdorff, there are neighborhoods $U$ and $V$ of $x$ and $y$, respectively, such that $U \cap V = \emptyset$. Since $\\{ x_n \\}$ converges to both $x$ and $y$, there exist positive integers $N_1$ and $N_2$ such that $x_n \in U, \forall n \ge N_1$ and $x_n \in V, \forall n \ge N_2$. Take $N = \max \\{ N_1, N_2 \\}$. Then we have that $x_n \in U \cap V, \forall n \ge N$. $\bigotimes$ Thus, if $\\{ x_n \\}$ converges to some point of $X$, then it is unique. $\blacksquare$

---

## Theorem 4
**(i)** The product of two Hausdorff spaces is a Hausdorff space. 

**(ii)** A subspace of a Hausdorff space is a Hausdorff space.

### Proof
(i)

(ii)