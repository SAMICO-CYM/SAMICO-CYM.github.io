---
title: Convergence of a Sequence
date: 2026-04-22
categories: [Mathematics, Topology]
tags: []
math: true
---

## Definition
Let $X$ be a topological space. We say that a sequence $\\{ x_n \\}_{n \in \mathbb{N}}$ in $X$ ***converges*** to a point $x \in X$ if for each neighborhood $U$ of $x$, there is a positive integer $N$ such that $x_n \in U$ for all $n \ge N$. 

실수나 거리 공간에서는 어떤 수열이 수렴한다면 항상 극한값은 유일했지만, 일반적인 위상 공간으로 넘어오면 수렴한다고 해서 그 값이 유일하다고 보장할 수 없다. 예컨대 다음의 예시를 보자.

$X = \\{ a, b, c \\}$로 주고, $\mathcal{T} = \\{ \\emptyset, \\{ b \\}, \\{ a, b \\}, \\{ b, c \\}, X \\}$라고 하자. 이 때 모든 자연수에 대해서 $x_n = b$으로 정의되는 수열 $\\{ x_n \\}$을 가지고 오면, $a$와 $c$는 모두 위 정의를 만족함을 알 수 있다. 따라서 $a$와 $c$ 모두 수열 $\\{ x_n \\}$의 극한값이 될 수 있다. 

이는 일반적인 위상 공간에서 singleton set $\\{ x \\}$가 닫혀 있다는 보장을 항상 할 수 없기 때문에 생기는 현상인데, 거꾸로 실수공간 $\mathbb{R}$에서는 singleton set이 닫혀 있기 때문에 극한값이 유일함을 알 수 있다. 그렇기에 하우스도르프 공간이 굉장히 좋은 공간이라는 사실은 말할 것도 없다.