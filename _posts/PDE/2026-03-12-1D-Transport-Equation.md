---
title: One-Dimensional Transport Equation
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

## Remark
1차원 선을 따라서 어떤 물질, 예컨대 물과 같은 유체가 흐르고 있다고 해보자. 이때 수직선상 위치 $x$와 시간 $t$에서의 물질의 밀도를 $u(x, t)$로 나타내면 $t$일 때 구간 $[0, x]$에 담겨있는 물질의 양 $M$은 

$$M = \int_0^x u(x', t) \, dx'$$

로 주어진다. 이때 물질이 $x$축을 따라서 속도 $c$로 일정하게 움직이고 있다고 하면 $h$만큼의 시간이 흘렀을 때 같은 양의 물질이 구간 $[ch, x + ch]$에 담겨있어야 한다.

$$M = \int_0^x u(x', t) \, dx' = \int_{ch}^{x + ch} u(x', t + h) \, dx'$$

위 식은 임의의 $x \ge 0, h \ge 0$에 대해서 성립한다. 이제 양변을 $x$로 미분하면 다음을 얻는다.

$$u(x, t) = u(x + ch, t + h)$$

다시 양변을 $h$로 미분하고 $h = 0$을 대입하면 다음을 얻는다.

$$0 = cu(x, t) + u_t(x, t)$$

이로써 1차원 수송 방정식을 얻었다.

1차원 수송 방정식의 해는 $u(x, t) = f(x - ct)$로 주어지는데, 이는 함수 $y = f(x)$를 $x$축을 따라 $ct$만큼 평행이동한 꼴이다. $c$는 속도이기 때문에 $ct$ 시간이 $t$만큼 흘렀을 때 이동한 거리를 나타낸다. 직관적으로 이해하기 위해 $u(x, t)$를 물질의 모양, 즉 어떤 파동의 형태라고 두자. 그러면 $t = 0$일 때 파동의 모양이 $u(x, 0) = f(x)$이고, 시간이 지날수록 이 모양이 그대로 형태를 유지하면서 $x$축을 따라 일정하게 이동하는 현상을 모델링한 방정식이 1차원 수송 방정식이라고 이해할 수 있다. 

또 다른 관점으로, 방정식을 $u_t = -cu_x (c > 0)$로 두고 이해해보자. 어떤 관찰자가 1차원 위의 고정된 위치에서 파동이 움직이는 현상을 관찰하고 있고, 파동은 $x$축을 따라 양의 방향으로 이동하고 있다고 하자. 아직 파동이 관찰자의 위치까지 도달하기 전에는 관찰자의 위치에서 파동의 기울기, 즉 $u_x$는 음수이지만 분명히 시간에 따라서 관찰자의 위치로 가까이 다가오고 있으므로 시간에 따른 파동의 변화율, 즉 $u_t$는 양수다. 반대로 파동이 관찰자의 위치를 지나쳐서 멀어지고 있다면 관찰자의 위치에서의 파동의 기울기, 즉 $u_x$는 양수이지만 시간에 따른 파동의 변화율, 즉 $u_t$는 음수다. 이러한 센스에서 방정식 $u_t = -cu_x$에서 마이너스 부호가 붙었다고 이해할 수 있다.