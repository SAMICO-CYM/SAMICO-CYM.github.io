---
Title: Boolean Lattice
Date: 2026-03-20
Categories:
  - Mathematics
  - Ordering
Tags: []
Math: true
---

## Definition
Let $n \in \mathbb{N}$. The $n$-th ***boolean lattice*** $\mathcal{B}_n$ is the [poset](<{% post_url Ordering/2026-03-09-Order %}>) $(B_n, \prec)$, where $B_n = \{ 0, 1 \}^n$ and $\prec$ is defined by 

$$a \prec b \iff a_i \le b_i, \forall i \in [n]$$

where $[n] = \\{ 1, ..., n \\}$.

각 원소가 $0$과 $1$로만 이루어진 순서쌍들과 componentwise하게 정의된 order를 가지는 집합을 boolean lattice라고 한다. $n=3$에 대하여 [Hasse diagram](<{% post_url Ordering/2026-03-20-Hasse-Diagram %}>)을 그리면 다음과 같다.

![Hasse Diagram](assets/img/booleanlattice.jpg)