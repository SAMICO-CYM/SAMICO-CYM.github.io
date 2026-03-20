---
Title: Linear Extension
date: 2026-03-20
categories: [Mathematics, Ordering]
tags: []
math: true
---

## Definition
Let $(X, \le)$ be a poset. A ***linear extension*** of $(X, \le)$ is a total order $\prec$ on $X$ such that for any $x, y \in X$,

$$x \le y \implies x \prec y.$$

---

## Example
집합 $\\{ a, b, c \\}$에 순서 관계 $a \le b, a \le c$를 주면 자연스럽게 poset이 된다. 그러나 $b$와 $c$ 사이의 관계는 주어지지 않았기 때문에 여기서 $\le$는 total order는 아니다. 여기에 $b \le c$, 혹은 $c \le b$를 추가해서 정의한 순서 집합은 totally ordered set이 되고, 따라서 원래 순서 집합을 그대로 보존하면서 모든 원소에 순서 관계를 준 linear extension이 된다. 주의할 점은 순서를 $b \le c$ 혹은 $c \le b$ 중 아무거나 부여해도 linear extension이 되기 때문에, linear extension은 유일하지 않다.

---

## Lemma
A restriction of a poset is also a poset.

---

## Theorem
Every finite poset has a linear extension.

### Proof
Let $(X, \le)$ be a finite poset. We prove this by induction on $n = \vert X \vert$.

When $n = 1$, there is only one partial ordering on $X$, and clearly it is a linear extension.

Assume that the theorem holds for all poset of size up to $n-1$ and let $\vert X \vert = n$. Since $X$ is finite, [it has a minimal element](<{% post_url Ordering/2026-03-20-Minimal-Minimum-Maximal-Maximum %}#theorem>) $x_0 \in X$. Let $X' = X \setminus \\{ x_0 \\}$. By the lemma and the induction hypothesis, the poset $(X', \le \cap (X' \times X'))$ has a linear extension $\prec'$. 

Define the order $\prec$ on $X$ by $x \prec y$ if $x \prec' y$ for any $x, y \in X'$, or $x = x_0$ and $y \in X'$. Then $\prec$ is a total order on $X$ (Why?), so that $\prec$ is a linear extension of $(X, \le)$. Thus the proof is complete. $\blacksquare$ 