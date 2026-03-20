---
Title: Embedding
date: 2026-03-20
categories: [Mathematics, Ordering]
tags: []
math: true
---

## Definition
Let $(X, \le)$ and $(X', \le')$ be [posets](<{% post_url Ordering/2026-03-15-Order %}>). We say that $(X, \le)$ can be ***embedded*** into $(X', \le')$ if there exists an injection $\phi: X \to X'$ such that for any $x, y \in X$,

$$x \le y \iff \phi(x) \le' \phi(y).$$ 

In this case, the function $\phi$ is called an ***embedding*** from $(X, \le)$ to $(X', \le')$.

쉽게 생각해서 두 poset 사이의 순서 관계를 보존하면서 원소들을 유일하게 매핑하는 함수를 임베딩이라고 한다. 

![Embedding](assets/img/Embedding.png)

예컨대 위 사진과 같이 Hasse diagram으로 정의된 두 poset이 있다고 하자. 이때 $1 \longleftrightarrow a$, $2 \longleftrightarrow b$와 같이 대응시키면 왼쪽 집합은 오른쪽 집합으로 임베디드 될 수 있고, 임베딩은 총 $5$개가 존재한다. 

---

## Theorem
For every poset $(X, \le)$, the map $\phi: X \to 2^X$ defined by

$$\phi(x) = L_x := \{ y \in X \mid y \le x \}, \forall x \in X$$

is an embedding of $(X, \le)$ into $(2^X, \subset)$.

### Proof
If $\phi(x) = \phi(y)$ for $x, y \in X$, then we have $L_x = L_y$. Since $x \in L_x$, $x \in L_y$ which means that $x \le y$. Similarly, we have $y \le x$. Since $\le$ is a partial order, $\le$ is antisymmetric, so that $x = y$. Thus $\phi$ is injective. 

If $x \le y$ for $x, y \in X$, then $x \in L_y$ so that $L_x \subset L_y$. Thus $\phi(x) \subset \phi(y)$. 

Conversely, suppose that $\phi(x) \subset \phi(y)$ for $x, y \in X$. Then $x \in L_y$, so that $x \le y$. Thus $\phi$ is an embedding. $\blacksquare$
