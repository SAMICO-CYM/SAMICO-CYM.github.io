--- 
title: Connected Space
date: 2026-05-27
categories: [Mathematics, Topology]
tags: []
math: true
---

## Definition
Let $X$ be a topological space. A ***seperation*** of $X$ is a pair $(U, V)$ of disjoint nonemepty open subsets of $X$ whose union is $X$. The space $X$ is said to be ***connected*** if there does not exist a separation of $X$.

정의에서 $U, V$를 open이 아니라 closed로 바꿔도 상관없다. 어떤 경우든 $U$와 $V$는 open이면서 closed이기 때문이다. 

즉 $X$가 연결되지 않는다는 말은 열리면서 닫힌 비자명 부분집합으로 이루어진 $X$의 partition이 존재한다는 말이다. 위상 공간에서 열리면서 닫힌 집합으로는 당연하게 $\emptyset$과 집합 그 자신 $X$이 있다. 그런데 이 둘이 아닌 또 다른 집합들이 존재한다는 말은, $X$ 안에 마치 그 자신이 위상 공간처럼 행동하는 두 부분이 존재하는 것처럼 생각할 수 있다. 그러면 두 부분은 사실상 독립적인 공간들로 다뤄질 수 있고, 이는 연결되어 있지 않다는 직관으로 이어진다.

---
## Remark
**(i)** If $X \cong Y$ and $X$ is connected, then so is $Y$. That is, connectedness is a topological property, so it is preserved by a homeomorphism.

**(ii)** A space $X$ is connected $\iff$ the only subsets of $X$ that are both open and closed in $X$ are $\emptyset$ and $X$ itself.

---
## Lemma 1
If $Y$ is a subspace of $X$, a separation of $Y$ is a pair $(A, B)$ of disjoint nonempty subsets of $Y$ whose union is $Y$, neither of which contains a limit point of the other. The space $Y$ is connected if there exists no separation of $Y$. 

### Proof
Suppose that $(A, B)$ is a separation of $Y$. Then $A$ is a nonempty subset of $Y$ that is both open and closed in $Y$. Note that the closure of $A$ in $Y$ is $\overline{A} \cap Y$, where $\overline{A}$ is the closure of $A$ in $X$. Since $A$ is closed in $Y$, $A = \overline{A} \cap Y$. Since $A \cap B = \emptyset$, we have

$$\begin{align*}
\emptyset &= A \cap B \\
&= (\overline{A} \cap Y) \cap B \\
&= \overline{A} \cap (Y \cap B) \\
&= \overline{A} \cap B.
\end{align*}$$

It follows that $B$ does not contain a limit point of $A$. A similar argument shows that $A$ does not contain a limit point of $B$. 

Conversely, let $(A, B)$ be a pair of disjoint nonempty subsets of $Y$ whose union is $Y$, neither of which contains a limit point of the other. Since $\overline{A} \cap B = \emptyset = A \cap \overline{B}$,  we obtain that $Y - B = \overline{A}$ and $Y - A = \overline{B}$, which means that $A$ and $B$ are open in $Y$. Since $Y - A = B$ and $Y - B = A$, $A$ and $B$ are closed in $Y$. Thus, $(A, B)$ is a separation of $Y$. $\blacksquare$

---
## Lemma 2
If the sets $C$ and $D$ form a separation of $X$, and if $Y$ is a connected subspace of $X$, then $Y$ lies entirely within either $C$ or $D$.

### Proof
Since $C$ and $D$ are open in $X$, $Y \cap C$ and $Y \cap D$ are open in $Y$. Note that 

$$\begin{align*}
(Y \cap C) \cup (Y \cap D) &= Y \cap (C \cup D) \\
&= Y \cap X \\
&= Y,
\end{align*}$$

and

$$\begin{align*}
(Y \cap C) \cap (Y \cap D) &= Y \cap (C \cap D) \\
&= Y \cap \emptyset \\
&= \emptyset.
\end{align*}$$

If $Y \cap C$ and $Y \cap D$ are nonempty, then $(C, D)$ is a separation of $Y$. Thus, either $Y \cap C$ or $Y \cap D$ is empty, which means that $Y$ lies entirely within either $C$ or $D$. $\blacksquare$

---
## Theorem 1
The union of a collection of connected subspaces of $X$ that have a point in common is connected.

### Proof
