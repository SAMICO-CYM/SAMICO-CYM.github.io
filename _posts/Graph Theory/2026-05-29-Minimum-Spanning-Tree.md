--- 
title: Minimum Spanning Tree
date: 2026-05-29
categories: [Mathematics, Graph Theory]
tags: []
math: true
---

## Definition
**(i)** A ***weighted graph*** $(G, w)$ consists of a graph $G$ and a function $w: E(G) \to \mathbb{Z}^+$ that assigns the weight $w(e) \in \mathbb{Z}^+$ to each edge $e \in E(G).$

**(ii)** For a subgraph $G' \le G,$ the ***weight*** of $G'$ is defined by

$$w(G') := \sum _{e \in E(G')} w(e).$$

그래프의 각 에지에 가중치를 부여한 개념이다. 예컨대 각 노드를 도시라고 하고 에지를 도시를 잇는 도로라고 할 때, 도로의 길이에 따라 가중치를 부여해서 어떤 도시에서 다른 도시로 이동할 때 가장 짧은 이동거리를 찾는 문제와 같은 곳에 사용할 수 있다.

---
## Kruskal's Algorithm
***Input:*** A connected weighted graph $(G, w).$

***Steps:***
Let $T$ be an null subgraph of $G$, that is, $E(T) = \emptyset$ and $V(T) = V(G).$

**(i)** Order the edges $\\{ e_1, e_2, \cdots, e_m \\}$ of $G$ by weight labeled to them: 

$$w(e_1) \le w(e_2) \le \cdots \le w(e_m)$$

**(ii)** Add the edge $e_1$ to $T.$ 

**(iii)** For $i = 1$ to $m$, add $e_i$ to $T$ unless it makes a cycle. 

***Output:*** The spanning tree $T \le G$ that minimizes $w(T).$

연결 그래프 $G$가 주어지면 spanning tree는 쉽게 찾을 수 있지만, 많은 상황에서는 그래프에 가중치가 부여된 상황에서 가중치를 최소화하는 spanning tree를 찾는 문제를 해결해야 한다. 이런 상황에서는 문제가 조금 더 복잡해지지만, 위에 서술되어 있는 바와 같이 그리디 알고리즘으로 일단은 해결할 수 있다. 