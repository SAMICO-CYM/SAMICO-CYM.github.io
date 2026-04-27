---
title: "Lagrange's Theorem"
date: 2026-04-27
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Lemma
Let $G$ be a group and let $H \le G$. Let $a \in G$. Then $\vert aH \vert = \vert H \vert = \vert Ha \vert $.

즉 어떤 부분군 $H$와, $H$에 대해서 정의된 coset $aH, Ha$의 크기는 모두 같다. 이때 coset들은 동치관계가 주어짐으로 결정된 동치류들이었고, 이 동치류들은 부분군 $H$의 partition을 이룬다. 즉 동치류들은 서로 disjoint하게 $G$를 구성하므로, 집합의 크기를 고려했을 때 부분군 $H$의 크기는 $G$의 크기를 항상 나눈다. 

### Proof

Define $\phi: H \to aH$ by $\phi(h) = ah$ for all $h \in H$. Since $a$ and each $h$ are elements of $G$, $ah \in G$. Then $\phi$ is well-defined. 

If $\phi(h_1) = \phi(h_2)$, then $a h_1 = a h_2$, so $h_1 = h_2$. Thus $\phi$ is injective. 

Let $ah \in aH$. Then $\phi(h) = ah$, so $\phi$ is surjective. 

Thus $\vert aH \vert = \vert H \vert$.

Similarly, we can show that $\vert Ha \vert = \vert H \vert$. $\blacksquare$

---

## Theorem (Lagrange's Theorem)
Let $H$ be a subgroup of a finite group $G$. Then $\vert H \vert$ divides $\vert G \vert$. 

### Proof
Let $H_1, ..., H_n$ be all distinct left cosets of $H$ in $G$. Then $G = \bigsqcup_{i=1}^n H_i$, so we obtain 

$$\vert G \vert = \sum_{i=1}^n \vert H_i \vert = n \vert H \vert$$

by the previous lemma. Thus $\vert H \vert$ divides $\vert G \vert$. $\blacksquare$

$G$가 유한군이므로 coset은 반드시 유한 개만 존재한다. 

---

## Corollary
Let $G$ be a finite group.

(i) If $a \in G$, then $\vert \langle a \rangle \vert$ divides $\vert G \vert$.

(ii) If the order of $G$ is prime, then $G$ is cyclic.

### Proof
(i) Note that $\langle a \rangle \le G$. By Lagrange's theorem, $\vert \langle a \rangle \vert$ divides $\vert G \vert$. 

(ii) Suppose that $\vert G \vert$ is prime, and let $a \in G - \\{ e \\}$. By (i), $\vert \langle a \rangle \vert$ divides $\vert G \vert$. Since $a \neq e$, $\vert \langle a \rangle \vert > 1$. Thus, $\vert \langle a \rangle \vert = \vert G \vert$. Hence, $\langle a \rangle = G$, so $G$ is cyclic. $\blacksquare$

---

## Example
