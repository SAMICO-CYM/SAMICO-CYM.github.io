--- 
title: Simple Group
date: 2026-06-01
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Definition 1
A group $G$ is ***simple*** if 

**(i)** $G \neq \\{ e \\},$

**(ii)** $G$ has no proper nontrivial normal subgroups.

정의를 한마디로 요약하면 $\\{ e \\} \lneq H \lneq G$를 만족하는 normal subgroup $H \lhd G$가 존재하지 않으면 $G$를 simple group이라고 부른다. 조금 다르게 정의해서, $G$의 subgroup $H$가 오직 $\\{ e\\}$이거나 $G$이면 simple이라고 하기도 하나, 이 경우 $G = \\{ e \\}$인 경우를 포함한다는 데 있어서 위 정의와 차이점이 있다. 

정수론에서 소수가 $1$과 자기 자신만을 약수로 가지는 수로 정의하는 맥락에 있어서, 군의 관점에서 소수의 역할을 하는 개념이라고 볼 수 있겠다. 실제로 다음의 사실이 성립한다.

---
## Theorem 1
A group $G$ is a simple abelian group $\iff$ $G \cong \mathbb{Z}_p$ for some prime $p.$

### Proof
$(\Longrightarrow)$

Suppose that $G$ is a simple abelian group. Let $a \in G \setminus \\{ e \\}.$ Then $\langle a \rangle \lhd G.$ Since $G$ is simple and $a \neq e,$ $\langle a \rangle = G,$ which means that $G$ is cyclic.

Note that $\mathbb{Z}$ has infinitely many subgroups, and since $\mathbb{Z}$ is abelian, all subgroups are normal. Thus, $G \not \cong \mathbb{Z},$ which implies that $G \cong \mathbb{Z}_p$ for some prime $p.$ 

$(\Longleftarrow)$

Suppose that $G \cong \mathbb{Z}_p$ for some prime $p.$ Clearly, $G$ is abelian.

By Lagrangle's theorem, the only subgroups, actually normal, of $\mathbb{Z}_p$ are $\\{ 0 \\}$ and $\mathbb{Z}_p.$ Thus, $\mathbb{Z}_p$ is normal, so is $G.$ $\blacksquare$

---
## Theorem 2
$A_n$ is simple $\iff$ $n=3$ or $n \ge 5.$

### Proof
$(\Longrightarrow)$

$(\Longleftarrow)$

First, we consider $n=3.$ Note that $\vert A_3 \vert = 3$, so $A_3 \cong \mathbb{Z}_3.$ By Theorem 1, $A_3$ is simple.

---
## Remark
$A_2$ is the trivial group, and $A_4$ is not simple.

$\big[(\because)$ Clearly, $A_2 = \\{ e \\}.$ Note that $N = \\{ (1), (1, 2)(3, 4), (1, 3)(2, 4), (1, 4)(2, 3) \\} \lhd A_4.$ Hence, $A_4$ is not simple.$\big]$

---
## Definition 2
A ***maximal normal subgroup*** of a group $G$ is a normal subgroup $M$ of $G$ such that 

**(i)** $M \neq G,$

**(ii)** If there exists a normal subgroup $N$ of $G$ such that $M \le N$, then $N = M$ or $N = G.$

앞서 설명했듯이, simple group은 더 이상 그 안에 trivial하지 않은 더 작은 normal subgroup을 발견할 수 없는, normal에 있어서 소수의 역할을 하는 group이다. 그러면 역으로 생각해서 non-simple group은 그 안에 nontrivial한 normal subgroup을 가지고 있다는 뜻이고, 자연스럽게 그 중에 가장 maximal한 놈은 무엇인지 생각해 볼 수 있다. 

따라서 maximal normal subgroup $M$이 주어졌다면, $M$과 $G$ 사이에는 더 이상 normal subgroup을 찾아볼 수 없다는 말이 된다.  

---
## Theorem 3
Let $G$ be a group, and let $M \lhd G.$ Then $M$ is a maximal normal subgroup of $G$ $\iff$ $G/M$ is simple.

### Proof
$(\Longrightarrow)$

Suppose that $M$ is a maximal normal subgroup of $G.$ Consider the canonical epimorphism $\gamma: G \to G/M$ defined by $\gamma(g) = gM, \forall g \in G.$ 

Let $N \lhd G/M.$ Since $\gamma$ is an epimorphism, $\gamma^{-1}(N) \lhd G.$ 

Since $M$ is the identity of the factor group $G/M$, $M \in N$. 

Note that $\gamma(m) = M, \forall m \in M,$ which means that $\gamma(M) = \\{ M \\}.$ It follows that $M \subset \\{ \gamma^{-1}(M) \\}.$ 

증명, center, commutator exercise찾아서 정리.

$(\Longleftarrow)$

