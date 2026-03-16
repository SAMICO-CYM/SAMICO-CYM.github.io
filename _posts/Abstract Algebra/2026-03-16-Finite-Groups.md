---
title: Finite Groups
date: 2026-03-16 00:01:25
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Group Table
Finite group, 즉 유한군이란 군의 원소의 개수가 유한한 경우를 말한다. 이러한 경우 테이블을 작성해서 모든 원소들과 그 연산의 결과를 나열할 수 있기 때문에 군의 구조를 한눈에 볼 수 있고, 이렇게 작성한 테이블을 ***group table*** 혹은 ***Cayley table***이라고 한다.

## Remark

(i) 군의 정의에 의해 모든 군은 항등원이라는 원소를 반드시 포함하므로 $\vert G \vert \ge 1$이다. 

(ii) 어떤 테이블이 group table이 되기 위해서는 같은 행과 열에 같은 원소가 두 번 이상 나타나지 않아야 한다. 만약 다음과 같은 테이블이 있다고 하자.

$$
\begin{array}{c|cc}
* &  & b & \cdots & c & \cdots \\
\hline
\vdots & \vdots & \vdots &  & \vdots & \\
a & \cdots & x & \cdots & x & \cdots \\
\vdots &  & \vdots &  & \vdots & \\
\end{array}
$$



원소의 개수를 하나씩 늘려가며 케이스별로 살펴보자.

## $\vert G \vert = 1$
자명하게 원소의 개수가 1개 뿐인 군은 $G = \\{ e \\}$뿐이다. 즉 이 경우

$$\begin{array}{c|c}
* & e \\
\hline
e & e \\
\end{array}$$

라는 테이블을 얻게 되고, 이러한 군은 $(\\{ 0 \\}, +)$와 동형이다.

## $\vert G \vert = 2$
원소의 개수가 2개인 군을 $G = \\{e, a \\}$로 나타내자. 그러면

$$\begin{array}{c|cc}
* & e & a \\
\hline
e & e & a \\
a & a & e \\
\end{array}$$

위와 같은 테이블을 얻게 되는데, $a \ast a = a$이면 $a$는 항등원이 되어야 하므로 모순이다. 따라서 $a \ast a = e$여야 한다. 즉