--- 
title: Continuous Functions
date: 2026-04-29
categories: [Mathematics, Topology]
tags: []
math: true
---

## Definition
Let $(X, \mathcal{T}_X)$ and $(Y, \mathcal{T}_Y)$ be topological spaces. A function $f: X \to Y$ is said to be ***continuous*** if $f^{-1}(V) \in \mathcal{T}_X, \forall V \in \mathcal{T}_Y$. 

정의만 보면 왜 이 모양인가 싶겠지만, 사실 해석학에서 다루던 $\varepsilon - \delta$ 논법을 위상수학의 언어로 바꾼 것과 다름 없다. 

$$\begin{align*}
f: \mathbb{R} \to \mathbb{R} \text{ is continuous at } a &\iff \forall \varepsilon > 0, \exists \delta > 0 \text{ such that } \vert x - a \vert < \delta \implies \vert f(x) - f(a) \vert < \varepsilon \\
& \iff \forall \varepsilon > 0, \exists \delta > 0 \text{ such that } x \in (a - \delta, a + \delta) \implies f(x) \in (f(a) - \varepsilon, f(a) + \varepsilon) \\
& \iff \forall \varepsilon > 0, \exists \delta > 0 \text{ such that } x \in (a - \delta, a + \delta) \implies x \in f^{-1}((f(a) - \varepsilon, f(a) + \varepsilon)) \\
& \iff \forall \varepsilon > 0, \exists \delta > 0 \text{ such that } (a - \delta, a + \delta) \subset f^{-1}((f(a) - \varepsilon, f(a) + \varepsilon))
\end{align*}$$

즉 양수 $\varepsilon$을 하나 가지고 온다는 것은 $f(a)$의 네이버후드 $V$를 가지고 오는 것이고, 그에 대응되는 양수 $\delta$가 존재한다는 것은 $f^{-1}(V)$에 속하는 $a$의 네이버후드가 존재한다는 말이다. 그런데 이건 정확히 $f^{-1}(V)$가 open이 되는 조건이므로, 위에서 새롭게 정의한 연속과 $\varepsilon- \delta$논법의 정의가 사실상 같음을 알 수 있다. 

---

## Remark
**(i)** Let $\mathcal{B}$ be a basis generating $\mathcal{T}_Y$. If $f^{-1}(B) \in \mathcal{T}_X, \forall B \in \mathcal{B}$, then $f$ is continuous.  

$\big[ (\because)$ Let $V \in \mathcal{T}_Y$. Then $V = \bigcup _ {B \in \mathcal{A}} B$ for some $\mathcal{A} \subset \mathcal{B}$. Then

$$\begin{align*}
f^{-1}(V) &= f^{-1} \left( \bigcup_{B \in \mathcal{A}} B \right) \\
&= \bigcup_{B \in \mathcal{A}}f^{-1}(B) \in \mathcal{T}_X
\end{align*}$$

because each $f^{-1}(B) \in \mathcal{T}_X$. Thus, $f$ is continuous. $\blacksquare$ $\big]$

**(ii)** Let $\mathcal{S}$ be a subbasis generating $\mathcal{T}_Y$. If $f^{-1}(S) \in \mathcal{T}_X, \forall S \in \mathcal{S}$, then $f$ is continuous.

$\big[ (\because)$ Let $B \in \mathcal{B}$. Then $B = \bigcap_{i=1}^n S_i$ for some $S_1, ..., S_n \in \mathcal{S}$. Then

$$\begin{align*}
f^{-1}(B) &= f^{-1} \left( \bigcap_{i=1}^n S_i \right) \\
&= \bigcap_{i=1}^n f^{-1}(S_i) \in \mathcal{T}_X
\end{align*}$$

because each $f^{-1}(S_i) \in \mathcal{T}_X$. By (i), $f$ is continuous. $\blacksquare$ $\big]$

---

## Theorem
Let $(X, \mathcal{T}_X)$ and $(Y, \mathcal{T}_Y)$ be topological spaces, and let $f:X \to Y$ be a function. TFAE.

**(i)** $f$ is continuous.

**(ii)** $f(\overline{A}) \subset \overline{f(A)}, \forall A \subset X$.

**(iii)** $f^{-1}(B)$ is closed in $X$ for all closed set $B$ of $Y$.

**(iv)** For each $x \in X$ and a neighborhood $V$ of $f(x)$, there exists a neighborhood $U$ of $x$ such that $f(U) \subset V$. In this case, we say that $f$ is ***continuous at*** $x \in X$.

### Proof
**(i)** $\Longrightarrow$ **(ii)**

Suppose that $f$ is continuous. Let $y \in f(\overline{A})$. Then $y = f(x)$ for some $x \in \overline{A}$. Let $V$ be a neighborhood of $y$. Since $f(x) = y \in V$, we have $x \in f^{-1}(V)$. Since $V$ is open in $Y$,  $f^{-1}(V) \in \mathcal{T}_X$, which means that $f^{-1}(V)$ is a neighborhood of $x$. Then $f^{-1}(V) \cap A \neq \emptyset$, which implies that $\exists a \in f^{-1}(V) \cap A$. Then $a \in f^{-1}(V)$ and $a \in A$, so that $f(a) \in V$ and $f(a) \in f(A)$. Thus, $f(a) \in V \cap f(A)$, which means that $V \cap f(A) \neq \emptyset$. Hence, $y \in \overline{f(A)}$, so that $f(\overline{A}) \subset \overline{f(A)}$. 

**(ii)** $\Longrightarrow$ **(iii)**

Suppose that $f(\overline{A}) \subset \overline{f(A)}, \forall A \subset X$. Let $B$ be a closed set of $Y$. Then we have 

$$\begin{gather*}
f\left( \overline{f^{-1}(B)} \right) \subset \overline{f\left( f^{-1}(B) \right)} = \overline{B} = B \\
\implies \overline{f^{-1}(B)} \subset f^{-1}(B).
\end{gather*}$$

Since clearly $f^{-1}(B) \subset \overline{f^{-1}(B)}$, we have $f^{-1}(B) = \overline{f^{-1}(B)}$, which means that $f^{-1}(B)$ is closed in $X$. 

**(iii)** $\Longrightarrow$ **(i)**

Suppose that $f^{-1}(B)$ is closed in $X$ for all closed set $B$ of $Y$. Let $V \in \mathcal{T}_Y$. Since $Y - V$ is closed in $Y$, we have $f^{-1}(Y-V)$ is closed in $X$. Then 

$$\begin{align*}
f^{-1}(Y- V) &= f^{-1}(Y) - f^{-1}(V) \\
&= X - f^{-1}(V),
\end{align*}$$

so that $f^{-1}(V)$ is open in $X$. Thus, $f$ is continuous.

**(i)** $\Longrightarrow$ **(iv)**

Suppose that $f$ is continuous. Let $x \in X$ and let $V$ be a neighborhood of $f(x)$. Since $f(x) \in V$, we have $x \in f^{-1}(V)$. Since $f^{-1}(V)$ is open, $f^{-1}(V)$ is a neighborhood of $x$. Then $f(f^{-1}(V)) = V \subset V$. 

**(iv)** $\Longrightarrow$ **(i)**

Suppose that for each $x \in X$ and a neighborhood $V$ of $f(x)$, there exists a neighborhood $U$ of $x$ such that $f(U) \subset V$. Let $V \in \mathcal{T}_Y$. Let $x \in f^{-1}(V)$. Then $f(x) \in V$. Then there exists a neighborhood $U$ of $x$ such that $f(U) \subset V$, which implies that $U \subset f^{-1}(V)$. Thus, $f^{-1}(V) \in \mathcal{T}_X$, so that $f$ is continuous. $\blacksquare$