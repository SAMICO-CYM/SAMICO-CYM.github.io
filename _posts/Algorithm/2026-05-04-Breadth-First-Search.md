---
title: Breadth First Search
date: 2026-05-04
categories: [Mathematics, Algorithm]
tags: []
math: true
---

## Algorithm
***너비 우선 탐색 알고리즘(Breadth First Search; BFS)*** 은 주어진 그래프를 탐색하는 방법으로, BFS를 사용해서 그래프가 connected인지 판별하거나 두 버텍스 사이의 거리를 찾을 수 있다.

***Input:*** A graph $G$ and a vertex $v \in V(G)$

***Steps:*** 
**1.** Set $L_0 := \\{ v \\}, U = V(G) - L_0$, and $i = 0$.
**2.** Until $U = \emptyset$, do:
(a) Increase $i$. ($i := i+1$)
(b) Let $L_i$ be the set of vertices in $U$ adjacenty to some vertex in $L_{i-1}$.
(c) Set $U := U - L_i$.

***Output:*** A partition $P = \\{ L_0, L_1, \cdots, L_\ell \\}$ of the component of $G$ containing $v$ into parts $L_i$ whose members have distance $i$ from $v$. 

주어진 그래프가 유한 그래프라면, 이러한 알고리즘은 반드시 유한번 내에 멈출 수 밖에 없다.  

주어진 버텍스 $v$를 기준으로 각 layer $L_i$에 있는 버텍스들은 거리가 $i$만큼 떨어진 버텍스들이다. 따라서 거리를 구하고자 하는 점이 들어있는 layer를 찾은 뒤, 그 layer의 index가 거리가 된다. 만약 어떠한 layer에도 들어있지 않다면 그 점은 $v$와 다른 component에 있다는 뜻이고, 거리는 $\infty$가 된다.

마찬가지로, 위와 같은 방법을 통해 주어진 그래프가 connected인지도 쉽게 판별할 수 있다. Layer 안에 모든 버텍스들이 들어있다면 $G$는 단 하나의 component만 갖는다는 뜻이 되므로 connected이고, 어떤 layer 안에도 들어 있지 않는 버텍스가 존재한다면 또 다른 component가 존재한다는 뜻이므로 disconnected이다.

---
## Time
