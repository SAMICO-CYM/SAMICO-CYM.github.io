--- 
title: Cauchy-Goursat Theorem
date: 2026-05-08
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

[Cauchy Theorem]({% post_url Complex Analysis/2026-05-08-Cauchy-Theorem %}#cauchy's-theorem)은 $f(z)$가 analytic하고 $f'(z)$가 연속이어야 한다는 두 가지 조건이 필요했었다. 이때 $f'(z)$가 연속이라는 조건을 빼도 동일한 결론이 성립한다는 사실을 보인 정리가 Cauchy-Goursat Theorem이다. 

우선 simple closed contour $C$의 내부와 그 점들로 만든 영역을 $R$이라고 하자. 이때 구분구적법처럼 $R$을 각 축에 평행하게 잘게 자른다. 이때 $R$의 모양에 따라서 완벽한 사각형으로 잘릴 수도 있고, 경계면에 의해 잘려서 완벽하지 못한 사각형으로 잘릴 수도 있다. 이때 완벽한 사각형을 square, 완벽하지 못한 사각형을 partial sqaure이라고 하자. 각 square과 partial square들은 경계면 또한 포함하고 있음을 주의하자. 

그러면 영역 $R$은 당연하게도 square와 partial square들의 합집합으로 표현, 다시 말해 cover된다. 이때 다음의 Lemma가 성립한다.

---
## Lemma
Let $R$ be a closed region consisting of the points interior to a positively oriented simple closed contour $C$ together with the points on $C$ itself. Let $f(z)$ be an analytic function throughout $R$. For each $\varepsilon > 0$, the region $R$ can be covered with a finite number of squares and partial squares, indexed by $j = 1, 2,...,n$ such that in each one there is a fixed point $z_j$ for which the inequality

$$\left \vert \frac{f(z) - f(z_j)}{z - z_j} - f'(z_j) \right \vert < \varepsilon \quad \cdots \quad (\ast)$$

is satisfied by all points other than $z_j$ in that square or partial square.

### Proof
If every subregion contain a needed point $z_j$ such that the inequality $(\ast)$ holds for all other points $z$ in it, then we are done.

Suppose that there is some subregion $\sigma$ in which no point $z_j$ exists such that the inequality $(\ast)$ holds for all other points $z$ in it. 

If the subregion is a square, then we construct four smaller squares by drawing line segments joining the midpoints of its opposite sides. If the subregion is a partial square, then we treat the whole square in the same manner and then let the prtions that lie outside of $R$ be discarded. 

We claim that if this process is done to each of the original subreigoins that requires it, then we can find that after a finite number of steps, $R$ can be covered with a finite number of subregions such that the lemma is true. 

$\big[(\because)$ Suppose that after any finite number of steps, $R$ cannot be covered with a finite number of subregions such that the lemma is true. 

We let $\sigma_0$ denote that subregion $\sigma$ if it is a square; otherwise, if it is a partial square, we let $\sigma_0$ denote the entire square of which $\sigma$ is a part. 

After we subdivide $\sigma_0$, at least one of the four smaller squares, denoted by $\sigma_1$, must contain points of $R$ but no needed point $z_j$. We take $\sigma_1$ to be the one lowest and then furthest to the left. We then subdivide $\sigma_1$ and continue in this manner. Thus, we obtain the nested infinite sequence 

$$\sigma_0, \sigma_1, \cdots, \sigma_{k-1}, \sigma_k, \cdots$$

of squares. Note that each $\sigma_k$ does not contain the needed point $z_j$.

By the [nested interval theorem]({% post_url Real Analysis/2026-05-09-Nested-Interval-Theorem %}#nested-interval-theorem), there exists a point $z_0$ common to each $\sigma_k$. (By regarding each $\sigma_k$ as the product of two closed intervals in $\mathbb{R}$ and applying the theorem twice, we can find such point $z_0$.) Note that each of these squares contains points of $R$ other than possibly $z_0$. Note that any $\delta$-neighborhood $\vert z - z_0 \vert < \delta$ of $z_0$ contains such squares when their diagonals have lenghts less than $\delta$. Therefore, every $\delta$-neighborhood $\vert z - z_0 \vert < \delta$ of $z_0$ contains points of $R$ distinct from $z_0$, which means that $z_0$ is a limit point of $R$. Since $R$ is closed, $z_0 \in R$. 

Since $f(z)$ is analytic in $R$, it is analytic at $z_0$, which means that $f'(z_0)$ exists. Then for each $\varepsilon > 0$, there exists $\delta > 0$ such that

$$\vert z - z_0 \vert < \delta \implies \left \vert \frac{f(z) - f(z_0)}{z - z_0} - f'(z_0) \right \vert < \varepsilon.$$

Note that the neighborhood $\vert z − z_0 \vert < \delta$ of $z_0$ contains a square $\sigma_K$ when the integer $K$ is large enough that the length of a diagonal of that square is less than $\delta$. Thus, $z_0$ is the needed point $z_j$ in inequality $(\ast)$ for the subregion consisting of the square $\sigma_K$ or a part of $\sigma_K$. This contradicts that the nested sequence $\sigma_0, \sigma_1, \cdots, \sigma_k, \cdots$ does not contain the needed point $z_j.$ $\bigotimes$ Hence, the claim is true. $\big]$

Thus, we can always cover $R$ with a finite number of subregions such that the lemma is true. $\blacksquare$

---
## Cauchy-Goursat Theorem
If a function $f(z)$ is analytic at each point interior to and on the simple closed contour $C$, then 

$$\int_C f(z) \, dz = 0.$$

### Proof
