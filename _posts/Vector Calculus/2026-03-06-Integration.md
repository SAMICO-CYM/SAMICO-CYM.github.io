--- 
title: Integration
date: 2026-03-06
categories: [Mathematics, Vector Calculus]
tags: []
math: true
---

## Definition 1
Let 

$$Q = [a_1, b_1] \times \cdots [a_n, b_n] \subset \mathbb{R}^n$$

be a rectanlge ($n$-cell) in $\mathbb{R}^n$.

**(i)** Each of the intervals $[a_i, b_i]$ is called a ***component interval*** of $Q$.

**(ii)** The number $\displaystyle \max_{1 \le i \le n} \{ b_i - a_i \}$ is called the ***width*** of $Q$.

**(iii)** The number 

$$v(Q) = \prod_{i=1}^n (b_i - a_i) = (b_1 - a_1) \cdots (b_n - a_n)$$

is called the ***volume*** of $Q$.

**(iv)** A ***partition*** of $Q$ is an $n$-tuple $(P_1, ..., P_n)$ such that each $P_j$ is a partition of $[a_j, b_j]$. 

**(v)** If each $I_j$ is one of the subintervals determined by $P_j$ of the interval $[a_j, b_j]$, then the rectangle

$$R = I_1 \times \cdots \times I_n$$

is called a ***subrectangle*** determined by $P$, of the rectangle $Q$. The number $\displaystyle \max_{1 \le i \le n} \{ \vert I_i \vert \}$ is called the ***mesh*** of P.

## Definition 2
Let $Q$ be a rectangle ($n$-cell) in $\mathbb{R}^n$, and let $f : Q \to \mathbb{R}$ be a bounded function. Let $P = (P_1, \ldots, P_n)$ be a partition of $Q$. 

**(i)** For each subrectangle $R$ determined by $P$, let 

$$\begin{align*} 
m_R(f) &= \inf_{\mathbf{x} \in R} \{f(\mathbf{x})\} \\ 
M_R(f) &= \sup_{\mathbf{x} \in R} \{f(\mathbf{x})\}.
\end{align*}$$

We define the ***lower sum*** and the ***upper sum***, respectively, of $f$, determined by $P$, by the equations 

$$ \begin{align*}
L(f,P) &= \sum_R m_R(f) \cdot v(R) \\
U(f,P) &= \sum_R M_R(f) \cdot v(R),
\end{align*}$$

where the summations extend over all subrectangles $R$ determined by $P$. 

**(ii)** If $P''$ is a partition of $Q$ obtained from $P$ by adjoining additional points to some or all of the partitions $P_1, \ldots, P_n$, then $P''$ is called a ***refinement*** of $P$. Given two partitions $P$ and $P' = (P'_1, \ldots, P'_n)$ of $Q$, the partition 

$$P'' = (P_1 \cup P'_1, \ldots, P_n \cup P'_n)$$

is a refinement of both $P$ and $P'$; it is called their ***common refinement***.

## Lemma 1
Let $P$ be a partition of the rectangle $Q$ in $\mathbb{R}^n$, and let $f : Q \to \mathbb{R}$ be a bounded function. If $P''$ is a refinement of $P$, then 

$$L(f,P) \le L(f,P'') \quad \text{and} \quad U(f,P'') \le U(f,P).$$

### Proof
$\blacksquare$

## Lemma 2
Let $Q$ be a rectangle in $\mathbb{R}^n$, and let $f : Q \to \mathbb{R}$ be a bounded function. If $P$ and $P'$ are any two partitions of $Q$, then 

$$L(f,P) \le U(f,P').$$

### Proof
$\blacksquare$

## Definition 3
Let $Q$ be a rectangle in $\mathbb{R}^n$, and let $f : Q \to \mathbb{R}$ be a bounded function. Define 

$$\underline{\int_Q} f = \sup_P \{L(f,P)\} \quad \text{and} \quad \overline{\int_Q} f = \inf_P \{U(f,P)\},$$

where
These numbers are called the lower integral and upper integral, respectively, of $f$ over $Q$. They exist because the numbers $L(f,P)$ are bounded above by $U(f,P')$ where $P'$ is any fixed partition of $Q$; and the numbers $U(f,P)$ are bounded below by $L(f,P')$. If the upper and lower integrals of $f$ over $Q$ are equal, we say $f$ is integrable over $Q$, and we define the integral of $f$ over $Q$ to equal the common value of the upper and lower integrals. We denote the integral of $f$ over $Q$ by either of the symbols $$\int_Q f \quad \text{or} \quad \int_{\mathbf{x} \in Q} f(\mathbf{x}).$$