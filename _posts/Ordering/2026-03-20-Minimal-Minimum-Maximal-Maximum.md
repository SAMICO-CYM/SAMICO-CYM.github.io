---
Title: Minimal, Minimum, Maximal, Maximum
date: 2026-03-20
categories: [Mathematics, Ordering]
tags: []
math: true
---

## Definition
Let $(X, \le)$ be a [poset](<{% post_url Ordering/2026-03-15-Order %}>). Then an element $x \in X$ is called

**(i)** ***minimal*** if $\forall y \in X, y \le x \implies y = x$.

**(ii)** ***minimum*** if $\forall y \in X, x \le y$.

**(iii)** ***maximal*** if $\forall y \in X, x \le y \implies x = y$.

**(iv)** ***maximum*** if $\forall y \in X, y \le x$.

Minimum과 maximum은 진정한 의미로 모든 원소보다 작거나 큰 원소라고 이해할 수 있다. 거꾸로 말하면 일단 minimum, maximum 조건을 체크하기 이전에 뭐가 됐든 모든 원소와 순서 관계가 주어져 있어야 한다는 점이다. 어떤 원소와는 관계가 없으면 minimum이든 maximum이든 논의 자체가 불가능하다. 

반면 minimal, maximal은 굳이 모든 원소와 관계가 있을 필요는 없다. 자신과 관계가 있는 원소들에 한해서 최소, 최대를 만족하면 된다.

---

## Remark
**(i)** If $x$ is a minimum of $(X, \le)$, then $x$ is a minimal of $(X, \le)$.

$(\because)$ Let $y \in X$ with $y \le x$. Since $x$ is a minimum, $x \le y$. By antisymmetry, $x = y$. Thus $x$ is a minimal.

**(ii)** If $x$ is a maximum of $(X, \le)$, then $x$ is a maximal of $(X, \le)$.

$(\because)$ Similarly...

**(iii)** Not even a finite poset need have a minimum or maximum element. 

$(\because)$

![alt text](assets/img/minimal.png)

위 그림에서 $a, b$는 minimal이지만 $a$와 $b$ 서로는 관계가 없으므로 minimum이 아니다. 따라서 이 poset에서 minimum element는 존재하지 않는다.

---

## Theorem
Every finite poset has at least one minimal and at least one maximal element.

### Proof
Let $(X, \le)$ be a finite poset. For each $x \in X$, let 

$$L_x = \{ y \in X \mid y \le x \}.$$

Note that 

**(i)** $\vert L_x \vert \ge 1, \forall x \in X$ since $x \le x$, so that $x \in L_x$.

**(ii)** if $x \le y$, then $\vert L_x \vert \le \vert L_y \vert$ since $L_x \subset L_y$.

Then we can choose an element $x_0 \in X$ such that $\vert L_{x_0} \vert$ is minimum among $\vert L_x \vert, \forall x \in X$. 

Suppose that $\vert L_{x_0} \vert > 1$. Then there exists $y \in L_{x_0}$ such that $y \neq x_0$. Since $y \lneqq x_0$, we have $\vert L_y \vert < \vert L_{x_0} \vert$. $\bigotimes$ Thus $\vert L_{x_0} \vert = 1$, so that $x_0$ is minimal.

Similarly, we can show that there exists a maximal element. $\blacksquare$