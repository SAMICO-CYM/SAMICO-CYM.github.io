--- 
title: Sensitive Dependence on Initial Conditions
date: 2026-02-19 15:00:00 +0900
categories: [Mathematics, Dynamics]
tags: []
math: true
---

## Definition
Let $f$ be a map on $\mathbb{R}$.
- A point $x_0$ has ***sensitive dependence on initial conditions*** if $\exists d > 0$ such that $\forall \varepsilon > 0$, $\exists x \in N_\varepsilon(x_0)$ such that $|f^k(x) - f^k(x_0)| \ge d$ for some nonnegative integer k. Sometimes we will call such a point $x_0$ a ***sensitive point***.

당연하게도, $x_0$에 가까운 점일수록 더 큰 $k$ 값이 필요할 것이다. 

---

## Itineraries
![](assets/img/Pasted%20image%2020260220174110.png)
다음과 같은 맵 $G(x) = g_4(x) = 4x(1-x)$를 고려하자. 이때 임의의 점 $x_0 \in [0, 1]$을 뽑고, 구간을 반으로 나누어서 $x_0 < \frac{1}{2}$이면 글자 $L$을, $x_0 > \frac{1}{2}$이면 글자 $R$을 부여한다. ($x_0 = \frac{1}{2}$인 경우 $L$과 $R$ 둘 다 부여될 수 있다.) $x_0$에 맵을 취한 $G(x_0)$에도 동일한 규칙을 적용해서 글자를 부여하고, 계속해서 맵을 취하고 글자를 부여한다. 이렇게 해서 얻어진 글자들의 수열을 orbit의 ***itinerary***라고 부른다. 
\
예컨대 $x_0 = \frac{1}{3}$인 경우 orbit은 $\\{ \frac{1}{3}, \frac{8}{9}, \frac{32}{81}, ... \\}$이고, 따라서 itinerary는 $LRL...$과 같이 얻어진다. 한편 $x_0 = \frac{1}{4}$인 경우 $\\{\frac{1}{4}, \frac{3}{4}, \frac{3}{4}, ... \\}$와 같이 $\frac{3}{4}$가 한없이 반복되는 orbit을 얻고, 이러한 경우 itinerary는 $LRR...$으로 주어진다. 이러한 경우 $L\overline{R}$으로 표기한다. 이러한 방법으로 표기했을 때 $\frac{1}{2}$과 같은 경우를 제외하면 $[0, 1]$ 안에 있는 각각의 실수마다 itinerary가 유일하게 결정된다. 
\
한편 처음 글자가 $L$이 부여되는 점들의 집합은 자명하게 $\left[0, \frac{1}{2} \right]$이고 마찬가지로 $R$을 처음 글자로 부여받는 점들의 집합은 $\left[\frac{1}{2}, 1\right]$이다. 각각의 집합을 $L, R$로 표기하자. 동일한 방식으로 계산하면 $LL = \left[ 0, \frac{1}{2} - \frac{\sqrt{2}}{4} \right]$, $LR = \left[ \frac{1}{2} - \frac{\sqrt{2}}{4}, \frac{1}{2} \right]$, $RR = \left[ \frac{1}{2}, \frac{1}{2} + \frac{\sqrt{2}}{4} \right]$, $RL = \left[ \frac{1}{2} + \frac{\sqrt{2}}{4}, 1 \right]$을 얻고, $LLR, RLR$과 같은 집합도 마찬가지로 얻어진다.
\
