--- 
title: Positive Integer
date: 2026-02-21 15:00:00 +0900
categories: [Mathematics, Real Analysis]
tags: []
math: true
---

## Successor Set
- A set $X \subseteq \mathbb{R}$ is said to be a ***successor set*** if the followings are satisfied:
**(i)** $1 \in X$,  
**(ii)** $n \in X \implies n+1 \in X$.

실수 집합 $\mathbb{R}$이 successor set이기 때문에 successor set은 적어도 하나 존재한다.

## Lemma 1
- If $\mathcal{A}$ is any nonempty collection of successor sets, then $\cap \mathcal{A}$ is a successor set.

### Proof
Since $1$ is in every succerssor set, $1 \in \cap \mathcal{A}$. Let $n \in \cap \mathcal{A}$. Then $n \in A, \forall A \in \mathcal{A}$. Then $n + 1$ is also in any $A$ in $\mathcal{A}$ by definition. Thus $\cap \mathcal{A}$ is a successor set. $\blacksquare$

---

## Positive Integer
- The set $\mathbb{N}$ of ***positive integers*** is the intersection of the family of all successor sets.

자명하게 $\mathbb{N}$은 successor set들 중 가장 작은 집합이다.

---

## Theorem 1
- $n \in \mathbb{N} \implies n ≥ 1$.

### Proof
We will use mathematical induction. Let $S(n)$ be the statement which is $n \geq 1$. Note that $S(1)$ is clearly true. If $S(k)$ is true, then $k \geq 1$. [Note that $k-1 \in P$ or $k = 1$.]({% post_url 2026-02-19-Real-Number-System %}) If $k = 1$, then $k \in P$ by theorem 4.2. If $k - 1 \in P$, $(k - 1) + 1 = k \in P$. Thus $k \in P$, and 

$$k = k + 1 - 1 \in P \\ \Longrightarrow k + 1 > 1 \Longrightarrow k + 1 \geq 1.$$

Thus $S(n)$ is true for all positive integer $n$. $\blacksquare$

---

## Theorem 2
- $m,n \in \mathbb{N} \implies m + n \in \mathbb{P}$.

### Proof 
Let $S(n)$ be the statement which is $m+n \in \mathbb{N}$. Since $m \in \mathbb{N}$, clearly $m+1 \in \mathbb{N}$, so $S(1)$ is true. If $S(n)$ is true, that is, $m+n \in \mathbb{N}$, then $m+n+1 \in \mathbb{N}$, so $S(n+1)$ is true. Then by mathematical induction, $S(n)$ is true for all positive integers. $\blacksquare$

---

## Lemma 2
- $n \in \mathbb{N} \implies n − 1 = 0 \vee n − 1 \in \mathbb{N}$.

### Proof
Let $G = \{ n \in \mathbb{N} \, | \, n - 1 = 0 \vee n - 1 \in \mathbb{N} \}$. We will show that $G = \mathbb{N}$. Clearly $G \subset \mathbb{N}$. Note that $1 \in G$. If $n \in G$, then $(n+1) - 1 = n \neq 0$ and $n \in \mathbb{N}$. Thus $n+1 \in G$, so $G$ is a successor set. Since $\mathbb{N}$ is the smallest successor set, $\mathbb{N} \subset G$, so $G = \mathbb{N}$. $\blacksquare$

---

## Lemma 3
- $m, n \in P \wedge m < n \implies n ‒ m \in \mathbb{N}$.

### Proof
Let $S(m)$ be the statement which is $n - m \in \mathbb{N}$. By the assumption, $1 < n$. Then by Lemma 2, either $n-1 = 0$ or $n-1 \in \mathbb{N}$. Since $1 < n$, $n-1$ cannot equal to $0$, so $n-1 \in \mathbb{N}$, which means that $S(1)$ is true.   
Suppose that $S(m)$ is true, i.e., $n - m \in \mathbb{N}$ for the positive integers $n, m$ such that $n > m$. If $m+1 < n$, then $n - 1 \in \mathbb{N}$ because $n -1$ cannot equal to $0$, so $n - 1 \in \mathbb{N}$ by Lemma 2. Since $m < n - 1$ and $S(m)$ is true, $n-1 - m = n - (m + 1) \in \mathbb{N}$. Thus $S(m+1)$ is also true. By mathematical induction, $S(m)$ is true for all positive integers. $\blacksquare$

---

## Lemma 4
- Let $n \in \mathbb{N}$. No positive integer $m$ satisfies the inequality $n < m < n + 1$.

### Proof
Suppose that $\exists m \in \mathbb{N}$ such that $n < m < n+1$. Then $m - n \in \mathbb{N}$ by Lemma 3. But $m < n + 1$, so $m - n < 1$ which is a contradiction by Theorem 1. Thus there is no positive integer $m$ such that $n < m < n+1$. $\blacksquare$