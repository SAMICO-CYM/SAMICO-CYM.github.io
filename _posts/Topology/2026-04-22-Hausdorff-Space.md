---
title: "Hausdorff Space"
date: 2026-04-22
categories: [Mathematics, Topology]
tags: []
math: true
---

## Definition
A topological space $X$ is called a ***Hausdorff space***, or ***$T_2$ space***, if for each pair $x_1, x_2 \in X$ of distinct points of $X$, there exist neighborhoods $U_1$ and $U_2$ of $x_1$ and $x_2$, respectively, such that $U_1 \cap U_2 = \emptyset$.

---

## Theorem 1
Every finite set in a Hausdorff space is closed. 

### Proof
Since any Hausdorff space is a $T_1$-space, every finite set in a Hausdorff space is closed. $\blacksquare$

---

## Remark
하우스도르프 공간이면 $T_1$ 공간임이 보장되지만, 그 역은 성립하지 않는다. 예를 들어 실수 공간 위에서 정의된 cofinite topology $\mathcal{T}_c$를 고려하자. $\mathcal{T}_c$에서 공집합이 아닌 이상 모든 열린 집합은 $\mathbb{R} - \\{ x_1, ..., x_n \\}$의 형태를 가지므로, 임의의 유한 집합 $\\{ x_1, ..., x_n \\}$은 닫힌 집합이다. 즉 $(\mathbb{R}, \mathcal{T}_c)$는 $T_1$ 공간이다.

그러나 하우스도르프 공간은 아닌데, 서로 다른 두 점 $x_1, x_2$를 실수 위에서 가지고 오면 두 점을 포함하는 열린 집합을 어떻게 가지고 와도 항상 두 집합은, 위에서 살펴본 바와 같이, 실수의 양 끝으로 뻗어나가는 구간을 포함하고 있을 수 밖에 없고, 따라서 항상 교집합을 가지기 때문이다.

---

## Theorem 2
Let $X$ be a Hausdorff space. Then every sequence in $X$ has either a unique limit or no limit.

### Proof
Let $\\{ x_n \\}$ be a sequence of points of $X$. If $\\{ x_n \\}$ does not converge to some point of $X$, then we are done. Suppose that $\\{ x_n \\}$ converges to two distinct points $x$ and $y$ of $X$. Since $X$ is Hausdorff, there are neighborhoods $U$ and $V$ of $x$ and $y$, respectively, such that $U \cap V = \emptyset$. Since $\\{ x_n \\}$ converges to both $x$ and $y$, there exist positive integers $N_1$ and $N_2$ such that $x_n \in U, \forall n \ge N_1$ and $x_n \in V, \forall n \ge N_2$. Take $N = \max \\{ N_1, N_2 \\}$. Then we have that $x_n \in U \cap V, \forall n \ge N$. $\bigotimes$ Thus, if $\\{ x_n \\}$ converges to some point of $X$, then it is unique. $\blacksquare$

---

## Theorem 3
**(i)** The product of two Hausdorff spaces is a Hausdorff space. 

**(ii)** A subspace of a Hausdorff space is a Hausdorff space.

### Proof
(i)

(ii)