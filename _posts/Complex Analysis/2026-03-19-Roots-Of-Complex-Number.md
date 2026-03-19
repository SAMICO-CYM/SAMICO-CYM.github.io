---
title: Roots of Complex Number
date: 2026-03-19
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Definition
Let $z_0 \in \mathbb{C}$ and let $n \in \mathbb{N}$. The set 

$$z_0^{\frac{1}{n}} = \{ z \in \mathbb{C} \mid z^n = z_0 \}$$

is called the ***set of $n$-th roots*** of $z_0$.

## Remark
복소수에서 정의된 방정식 $z^n = z_0$의 근이 어떤 형태를 갖는지 살펴보자. $z_0$와 $z$ 모두 $0$이 아니라고 하면 $z_0 = r_0 e^{i \theta_0}$와 $z = r e^{i \theta}$과 같이 exponential form으로 쓸 수 있다. 그러면 다음과 같이 방정식을 작성할 수 있다.

$$r^n e^{i n \theta} = r_0 e^{i \theta_0}$$

두 복소수 값이 같을 조건은 $r^n = r_0$와 $n\theta = \theta_0 + 2k\pi$ ($k$는 정수)으로 주어진다. 따라서 $r = \sqrt[n]{r_0}$, $\theta = \frac{\theta_0 + 2k\pi}{n}$ ($k$는 정수)를 얻는다. 이때 사실상 $k = 0, 1, ..., n-1$까지만 다뤄도 모든 distinct form들을 얻고, 각 $k$에 대해서 근을 $c_k$로 두자. 

$$c_k = \sqrt[n]{r_0} \exp \left( i \frac{\theta_0 + 2k\pi}{n} \right), \quad k = 0, 1, ..., n-1$$

따라서 방정식의 근의 집합 $z_0^{\frac{1}{n}}$은 다음과 같이 표현된다.

$$z_0^{\frac{1}{n}} = \{ c_k \mid k = 0, 1, ..., n-1 \} = \left\{ \sqrt[n]{r_0} \exp \left( i \frac{\theta_0 + 2k\pi}{n} \right) \middle| k = 0, 1, ..., n-1 \right\}$$

