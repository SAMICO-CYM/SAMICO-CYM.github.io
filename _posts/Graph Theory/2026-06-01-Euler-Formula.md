--- 
title: Euler's Formula
date: 2026-06-01
categories: [Mathematics, Graph Theory]
tags: []
math: true
---

## Definition
Given a planer graph, a ***face*** is a region of the plane graph you get by cutting all edges of the graph. For the edges touching a face and its boundary edges, we say that ***they are in the face***.

## Euler's Formula
For any connected plane graph $G$ with $\vert V(G) \vert = n, \vert E(G) \vert = m$ and $f$ faces in the plane, 

$$n - m + f = 2.$$

### Proof
We use induction on $m$. Note that $m \ge n-1$ because $G$ is connected.

If $m = n-1,$ then $G$ is a tree, and there is only one face, so $f=1$. Then 

$$n-m+f = n-(n-1) +1 = 2$$

holds.

Suppose that $m \ge n.$ Then $G$ must have a cycle, so there is some edge $e$ whose removal does not disconnect $G$. 

Let $G' := G \setminus e.$ As $e$ was in a cycle in $G$, it was on the boundary of two faces which were joined in $G'.$ 

Since $n-m+f = 2$ holds for $G'$ and we get this from $G$ by removing one edge and one face, it also holds for $G.$ $\blacksquare$