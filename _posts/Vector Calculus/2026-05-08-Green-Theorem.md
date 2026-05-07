--- 
title: Green's Theorem
date: 2026-05-08
categories: [Mathematics, Vector Calculus]
tags: []
math: true
---

## Theorem 1
Let $C$ be a piecewise smooth, simple closed curve enclosing a region $R$ in the plane. Let $\mathbf{F}(x, y) = ( P(x, y), Q(x, y) )$ be a vector field with $C^1$ class functions $P, Q$ in an open region containing $R$. Then the counterclockwise circulation of $\mathbf{F}$ around $C$ equals the double integral of $(\nabla \times \mathbf{F}) \cdot \mathbf{k}$ over $R$: 

$$\oint_C \mathbf{F} \cdot d \mathbf{r} = \iint_R \left( Q_x - P_y \right) \,dA$$

---
## Theorem 2
Let $C$ be a piecewise smooth, simple closed curve enclosing a region $R$ in the plane. Let $\mathbf{F}(x, y) = ( P(x, y), Q(x, y) )$ be a vector field with $C^1$ class functions $P, Q$ in an open region containing $R$. Then the outward flux of $\mathbf{F}$ across $C$ equals the double integral of $\nabla \cdot \mathbf{F}$ over $R$ enclosed by $C$: 

$$\oint_C \mathbf{F} \cdot \mathbf{n} \, ds = \iint_R \left( P_x + Q_y \right) \, dA$$

Green's Theorem은 위와 같이 두 개의 형태가 있으며, 각각 circulation-curl, flux-divergence로 대응된다. 두 정리는 벡터장 $\mathbf{F}$를 변형해주면 각각 성립하므로 서로 동치이다. 

직관적으로는 다음과 같이 이해할 수 있다. 평면 영역 $R$이 있을 때, $R$ 전체에 대해서 어떤 유체와 같은 대상이 얼마나 회전하고 있는지를 파악하고자 한다. 원칙적으로는 $R$의 모든 $dA$에 대해서 curl을 적분해야 한다. 그러나 $R$을 $x, y$축으로 잘게 쪼개고 각 piece에 대해서 curl을 생각하면 인접한 piece들이 맞닿아 있는 부분은 크기는 같고 방향은 반대인 회전 성분을 가지므로 서로 상쇄됨을 직관적으로 알 수 있다. 이런 식으로 계산하다보면 결국 영역 전체의 curl은 $R$의 테두리만 고려하면 됨을 알 수 있고, 이는 circulation이다. Flux 형태도 마찬가지로 생각할 수 있다.

### Proof of Theorem 1
The curve $C$ can be expressed by two different curves: 

$$C_1: y = f_1(x), a \leq x \leq b, \quad -C_2: y = f_2(x), a \le x \le b.$$

Then we have 

$$\begin{align*}
\iint_R P_y \, dy \, dx &= \int_a^b \int_{f_1(x)}^{f_2(x)} P_y \, dy \, dx \\
&= \int_a^b [P(x, f_2(x)) - P(x, f_1(x))] \, dx  \\ 
&= \int_a^b P(x, f_2(x)) \, dx - \int_a^b P(x, f_1(x)) \, dx \\
&= \int_{-C_2} P \, dx - \int_{C_1} P \, dx \\
&= -\int_{C_2}  P \, dx - \int_{C_1} P \, dx \\
&= - \oint_C P \, dx.
\end{align*}$$

Similarly, we can integrate $Q_x$ on the region $R$. We can divide $C$ by two distinct curves $C'_1$ and $C'_2$: 

$$-C'_1: x = g_1(y), c \le y \le d, \quad C'_2: x = g_2(y), c \leq y \leq d$$

Then we obtain 

$$\begin{align*}\iint_R Q_x \, dx \, dy &= \int_c^d \int_{g_1(y)}^{g_2(y)} Q_x \, dx \, dy \\
&= \int_c^d [Q(g_2(y), y) - Q(g_1(y), y)] \, dy  \\ 
&= \int_c^d Q(g_2(y), y) \, dy - \int_c^d Q(g_1(y), y) \, dx \\
&= \int_{C'_2} Q \, dy - \int_{-C'_1} Q \, dy \\
&= \int_{C'_2} Q \, dy + \int_{C'_1} Q \, dy \\
&= \oint_C Q \, dy.
\end{align*}$$

Summing these two equations gives 

$$\oint_C Q \, dy - P \, dx = \iint_R \left( Q_x - P_y \right) \, dA. \quad \blacksquare$$