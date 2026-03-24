---
title: Infinite Square Well
date: 2026-03-24
categories: [Physics, Quantum Mechanics]
tags: []
math: true
---

## Infinite Square Well
퍼텐셜

$$V(x) = \begin{cases} 
0 & 0 \le x \le a \\ 
\infty & \text{ otherwise} \end{cases}$$

이 주어진 영역에서 입자가 운동한다고 하자. 

![alt text](assets/img/squarewell.png)

이때 입자의 에너지와 파동함수를 구해보자. 

영역 $0 \le x \le a$에서 입자의 시간 무관 슈뢰딩거 방정식은 다음과 같이 주어진다.

$$-\frac{\hbar^2}{2m} \psi_{xx} = E \psi$$

이는 평범한 2nd order linear ODE이고 해는 다음과 같이 주어진다.

$$\psi(x) = A \sin(kx) + B \cos(kx) \quad \text{where } k = \sqrt{\frac{2mE}{\hbar^2}}$$

한편 $x=0$, $x = a$에서 입자를 발견할 확률은 $0$이고, 이는 곧 $\psi(0) = 0 = \psi(a)$라는 경계조건을 의미한다. 이를 위 해에 대입하면 $B = 0$이고, $A \sin(ka) = 0$를 얻고, 따라서 

$$k_n = \frac{n \pi}{a}, \quad n = 1, 2, 3, \dots$$

과 같이 $k$는 자연수 $n$에 의존하는, '양자화된' 값을 가지게 된다. 사실 수학적으로는 $n$이 자연수 뿐만 아니라 모든 정수 값을 가질 수 있지만, $n = 0$일 때는 trivial solution을, $n$이 음수일 때는 양수와 동일한 모양의 해를 얻으므로 사실상 자연수값만 고려해도 무방하다. 

따라서 각 $n$에 대해서 파동함수 $\psi_n$은 

$$\psi_n(x) = A\sin \left( \frac{n \pi x}{a} \right), \quad n = 1, 2, 3, \dots$$

로 주어진다. 상수 $A$를 normalization condition을 이용해서 구해보자.

$$ \begin{align*}
1 &= \int_{-\infty}^{\infty} \vert \psi_n(x) \vert^2 \, dx \\
&= \int_0^a \vert \psi_n(x) \vert^2 \, dx \\ 
&= \int_0^a \vert A \vert^2 \sin^2 \left( \frac{n \pi x}{a} \right) \, dx \\
&= \vert A \vert^2 \frac{a}{2}
\end{align*}$$

따라서 $A = \sqrt{\frac{2}{a}}$이고, 무한 퍼텐셜 우물에서 거동하는 입자의 파동함수는 다음과 같다.

$$\psi_n(x) = \sqrt{\frac{2}{a}} \sin \left( \frac{n \pi x}{a} \right), \quad n = 1, 2, 3, \dots$$

또한 각 $\psi_n$에 대한 에너지 $E_n$은

$$E_n = \frac{\hbar^2 k_n^2}{2m} = \frac{n^2 \pi^2 \hbar^2}{2ma^2}, \quad n = 1, 2, 3, \dots$$

으로 주어진다. 즉 $n$이 커질수록 에너지도 더 큰 값을 가지되, 자연수에 의존하는 이산적인 값, 즉 양자화된 값만을 가진다는 사실을 얻는다. 

![alt text](assets/img/graphwavefunction.png)