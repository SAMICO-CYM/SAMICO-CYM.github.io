---
title: Chain and Antichain
date: 2026-03-23 00:00:01
categories: [Mathematics, Ordering]
tags: []
math: true
---

## Definition 1
Let $(X, \le)$ be a poset.

**(i)** Two elements $a$ and $b$ in $X$ are said to be ***comparable*** if $a \le b$ or $b \le a$. Otherwise, they are said to be ***incomparable***.

**(ii)** A subset $A \subset X$ is called a ***chain*** if every pair of element is comparable.

**(iii)** A subset $A \subset X$ is called an ***antichain*** if every pair of element is incomparable.

---

## Example

Boolean lattice $\mathcal{B}_3$을 고려하자. 

![Hasse Diagram](assets/img/booleanlattice.jpg)

딱봐도 $\\{(0, 1, 1), (1, 0, 1), (1, 1, 0) \\}$과 $\\{ (0,0,1), (0,1,0), (1,0,0) \\}$은 antichain이고, $\\{ (0,0,0), (0,0,1), (0,1,1), (1,1,1) \\}$은 chain이다. 

직관적으로도 알 수 있듯이 chain은 위아래로 뻗어있지만 antichain은 좌우로 퍼져있는 느낌이다. Hasse diagram을 그리면 순서 관계에 있어서 우세할수록 위쪽에 놓이고, 열세할수록 아래쪽에 놓이지만 순서 관계가 없는 원소끼리는 같은 높이에 놓이는 경향이 있기 때문이다. 그래서 chain중 가장 원소가 많은 chain의 크기를 height라고 부르고, antichain중 가장 원소가 많은 antichain의 크기를 width라고 부른다. 그러면 자연스럽게 드는 질문이, 어떤 finite poset이 주어졌을 때 가장 긴 chain의 길이와 가장 넓은 antichain의 너비는 얼마일까?

---

## Definition 2
Let $(X, \le)$ be a poset.

**(i)** The ***height*** $\, \omega(X)$ of $X$ is the size of it largest chain.

**(ii)** The ***width*** $\, \alpha(X)$ of $X$ is the size of it largest antichain.

---

## Theorem 1
Let $(X, \le)$ be a finite poset. Then $\alpha(X) \cdot \omega(X) \ge \vert X \vert$.

### Proof

---

## Theorem 2 
Any sequence $(x_1, x_2, ..., x_N)$ of $N = n^2+1$ real numbers has a monotone subsequence of length at least $n+1$.

### Proof
Define the relation $\preceq$ on the set $[N]$ defined by

$$i \preceq j \iff i \le j \text{ and } x_i \le x_j.$$

Then $([N], \preceq)$ is a poset. By Theorem 1, we have 

$$\alpha([N]) \cdot \omega([N]) \ge \vert [N] \vert = n^2 + 1,$$

which implies that $\alpha([N]) > n$ or $\omega([N]) > n$. 

Note that a chain in $([N], \preceq)$ is a monotonic increasing subsequence of $(x_1, x_2, ..., x_N)$ and an antichain in $([N], \preceq)$ is a monotonic decreasing subsequence of $(x_1, x_2, ..., x_N)$. Thus we must obtain a monotone subsequence of length at least $n+1$. $\blacksquare$