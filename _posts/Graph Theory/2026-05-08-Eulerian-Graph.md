--- 
title: Eulerian Graph
date: 2026-05-08
categories: [Mathematics, Graph Theory]
tags: []
math: true
---

## Definition
Let $G$ be a graph. ***An Eulerian tour*** of $G$ is a closed trail that contains every vertex and edge of $G$. We call $G$ ***Eulerian*** if $G$ has an Eulerian tour.

---
## Theorem 1
Let $G$ be a connected graph. Then $G$ is Eulerian $\iff$ Every vertex of $G$ has even degree.

### Proof
$(\Longrightarrow)$

If $G$ is Eulerian, then $G$ has an Eulerian tour $T$. Note that whenever $T$ passes each vertex $v$ of $G$, $T$ passes two edges attached to $v$. Since $T$ contains every edge of $G$ exactly once, every vertex of $G$ has even degree. 

$(\Longleftarrow)$

Suppose that every vertex of $G$ has even degree. Let $T = t_1 \cdots t_n$ be the longest trail in $G$. 

**Claim 1:** $T$ is closed.

$\big[(\because)$ If not, then $t_1$ occurs only an odd number of times in $T$. Since $t_1$ has odd degree in $T$ and $t_1$ has even degree in $G$, there exists $s \in V(G)$ such that $s \sim t_1$ and $s \notin T$. Then we can construct a trail $sT := st_1 \cdots t_n$, which is longer than $T$. $\bigotimes$ Thus, $T$ is closed. $\big]$

**Claim 2:** All vertices of $G$ are in $T$.

$\big[(\because)$ If not, then there is some vertex $s$ not in $T$. Since $G$ is connected, so is $T$. So we may assume that $s$ is adjacent to $t_i$ for some $i$. Then we can construct the trail $st_i \cdots t_n t_1 \cdots t_i$, which is longer than $T$. $\bigotimes$ Thus, all vertices of $G$ are in $T$. $\big]$ 

**Claim 3:** All edge of $G$ are in $T$.

$\big[(\because)$ If not, then there is some edge $e$ not in $T$. Since $T$ contains all vertices of $G$, $e := \\{ t_i, t_j \\}$ for some $t_i, t_j (i < j)$ in $T$. Then we can construct the trail $t_i \cdots t_j \stackrel{e}{\to} t_i \cdots t_1 t_n \cdots t_j$, which is longer than $T$. $\bigotimes$ Thus, all edges of $G$ are in $T$. $\big]$ 

By above claims, $T$ is a closed trail containing all vertices and edges of $G$, which means that $T$ is an Eulerian tour. Hence, $G$ is Eulerian. $\blacksquare$

---
## Theorem 2
Let $G$ be a connected graph. Then $G$ has a trail containing every edge $\iff$ exactly zero or two vertices of $G$ have odd degree.

### Proof
$(\Longrightarrow)$

$(\Longleftarrow)$
