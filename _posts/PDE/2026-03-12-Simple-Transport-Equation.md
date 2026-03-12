---
title: Simple Transport Equation
date: 2026-03-12
categories: [Mathematics, PDE]
tags: []
math: true
---

## Theorem
The general solution of the ***one-dimensional transport equation***

$$u_t + cu_x = 0$$

where $c$ is a constant, is given by

$$u(x, t) = f(x - ct)$$

where $f$ is an arbitrary function.

### Proof
Since the given PDE $u_t + cu_x = 0$ is first-order linear PDE with constant coefficients, the general solution is given by

$$u(x, t) = f(x - ct)$$

where $f$ is an arbitrary function. $\blacksquare$

## Derivation
1차원 선을 따라서 어떤 물질, 예컨대 물과 같은 유체가 흐르고 있다고 해보자. 이때 수직선상 위치 $x$와 시간 $t$에서의 물질의 밀도를 $u(x, t)$로 나타내면 $t$일 때 구간 $[0, x]$에 담겨있는 물질의 양 $M$은 

$$M = \int_0^x u(x', t) \, dx'$$

로 주어진다. 이때 물질이 $x$축을 따라서 속도 $c$로 일정하게 움직이고 있다고 하면 $h$만큼의 시간이 흘렀을 때 같은 양의 물질이 구간 $[ch, x + ch]$에 담겨있어야 한다.

$$M = \int_0^x u(x', t) \, dx' = \int_{ch}^{x + ch} u(x', t + h) \, dx'$$

위 식은 임의의 $x \ge 0, h \ge 0$에 대해서 성립한다. 이제 양변을 $x$로 미분하면 다음을 얻는다.

$$u(x, t) = u(x + ch, t + h)$$

다시 양변을 $h$로 미분하고 $h = 0$을 대입하면 다음을 얻는다.

$$0 = cu(x, t) + u_t(x, t)$$

이로써 1차원 수송 방정식을 얻었다.