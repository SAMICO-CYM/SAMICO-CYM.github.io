--- 
title: The Statistical Interpretation of Wave Functions
date: 2026-03-13
categories: [Mathematics, Quantum Mechanics]
tags: []
math: true
---

## The Statistical Interpretation
막스 보른의 확률적 해석은 파동함수를 해석하는 방법 중 하나로, 어떤 입자의 파동함수의 제곱 $\vert \Psi(x, t) \vert^2$을 확률밀도함수로 보고 이를 제곱한 값을 입자를 발견할 확률로 해석한다. 

$$\int_a^b \vert \Psi(x, t) \vert^2 \, dx = \text{Probability of finding the particle between } a \text{ and } b, \text{ at time } t$$

따라서 파동함수는 확률의 여러 성질을 만족해야 하는데, 대표적으로 규격화와 적분가능성이다. 전체 구간에 대해서 적분했을 경우 값은 $1$이 되어야 하며, 각 구간과 시점에서 적분값이 발산하면 안되고 항상 적분가능해야 한다.

---

## Normalization
슈뢰딩거 방정식은 선형 편미분방정식이므로 그 해인 파동함수 $\Psi$의 상수배 $c \Psi$ 또한 해가 된다. 때문에

$$\int_{-\infty}^\infty \vert \Psi(x, t) \vert^2 \, dx = C$$

와 같이 전체 구간에 대해 적분값이 $1$이 아니더라도 양변을 $C$로 나눠 줌으로써 규격화, 즉 normalization시킬 수 있다.

$$\int_{-\infty}^\infty \left\vert \frac{1}{\sqrt{C}}\Psi(x, t) \right\vert^2 \, dx = 1$$

---

## Theorem
Let $\Psi(x, t)$ be a wave function of a particle. If $\Psi(x, t)$ is normalized at $t = 0$, then it stays normalized for any $t > 0$.

### Proof
Since $\Psi(x, t)$ is normalized at $t = 0$, we have 

$$\int_{-\infty}^\infty \vert \Psi(x, 0) \vert^2 \, dx = \text{const.}$$


$\blacksquare$