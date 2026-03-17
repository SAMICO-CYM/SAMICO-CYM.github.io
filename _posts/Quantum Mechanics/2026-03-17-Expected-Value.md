---
title: Expected Value
date: 2026-03-17
categories: [Physics, Quantum Mechanics]
tags: []
math: true
---

## Expected Value
Let $\Psi$ be a normalized wave function. Then the expected value of a linear operator $A$ is given by

$$\langle A \rangle = \langle \Psi \vert A \vert \Psi \rangle = \int_{-\infty}^{\infty} \Psi^* A \Psi \, dx$$

## Remark
1차원에 대해서 위치 연산자 $\hat{x}$는 다음과 같이 정의된다.

$$\hat{x} \Psi = x \Psi$$

그리고 위치 연산자의 기댓값은 다음과 같다.

$$\langle x \rangle = \langle \Psi \vert x \vert \Psi \rangle = \int_{-\infty}^{\infty} \Psi^* x \Psi \, dx$$

이 결과를 가지고 운동량 연산자의 표현을 구해보자. 운동량 연산자의 기댓값은 다음과 같이 계산된다.

$$\langle p \rangle = m \langle v \rangle = m \frac{d \langle x \rangle}{dt}$$

$$\begin{align*} 
\frac{d \langle x \rangle}{dt} &= \frac{d}{dt} \int \Psi^\ast x \Psi \, dx \\
&= \int \frac{\partial}{\partial t} (\Psi^\ast x \Psi) \, dx \\
&= \int x(\Psi^\ast_t \Psi + \Psi^\ast \Psi_t) \, dx \\
&= \int x\left(\Psi \left(- \frac{i \hbar}{2m} \Psi_{xx} + \frac{i}{\hbar} V \Psi\right) + \Psi^\ast \left(\frac{i \hbar}{2m} \Psi_{xx} - \frac{i}{\hbar} V \Psi\right)\right) \, dx \\
&= \int x \frac{i \hbar}{2m}(\Psi^\ast \Psi_{xx} - \Psi \Psi^\ast_{xx}) \, dx \\
&= \frac{i \hbar}{2m} \int x \frac{\partial}{\partial x}(\Psi^\ast \Psi_x - \Psi \Psi^\ast_x) \, dx \\
&= \frac{i \hbar}{2m} \left[ \underbrace{x(\Psi^\ast \Psi_x - \Psi \Psi^\ast_x) \Bigg \vert_{-\infty}^{\infty}}_{\text{goes to zero}} - \int (\Psi^\ast \Psi_x - \Psi \Psi^\ast_x) \, dx \right] \\
&= -\frac{i \hbar}{2m} \int (\Psi^\ast \Psi_x - \Psi \Psi^\ast_x) \, dx \\
&= -\frac{i \hbar}{2m} \left[ \int \Psi^\ast \Psi_x \, dx - \left( \underbrace{\Psi^\ast \Psi \Bigg \vert_{-\infty}^{\infty}}_{\text{goes to zero}} - \int \Psi^\ast \Psi_x \, dx \right) \right] \\
&= -\frac{i \hbar}{m} \int \Psi^\ast \Psi_x \, dx
\end{align*}$$

$$\begin{align*} 
\implies \langle p \rangle &= m \frac{d \langle x \rangle}{dt} \\
&= - i \hbar \int \Psi^\ast \Psi_x \, dx \\
&= \int \Psi^\ast \left(-i \hbar \frac{\partial}{\partial x}\right) \Psi \, dx
\end{align*}$$

따라서 운동량 연산자는 다음과 같다.

$$\hat{p} = \begin{cases} 
-i \hbar \frac{\partial}{\partial x} & \text{ in one-dimension} \\
-i \hbar \nabla & \text{ in three-dimension} 
\end{cases}$$

이를 이용하면, 위치와 운동량에 의존하는 임의의 양 $Q(x, p)$의 기댓값을 구할 수 있다.

$$\langle Q(x, p) \rangle = \int_{-\infty}^{\infty} \Psi^\ast Q(x, -i \hbar \nabla) \Psi \, dx$$

예컨대 운동에너지의 기댓값은 다음과 같다.

$$\langle T \rangle = \int_{-\infty}^\infty \Psi^\ast \left( -\frac{\hbar^2}{2m} \frac{\partial^2}{\partial x^2} \right) \Psi \, dx$$

위 결과를 정리하면, 임의의 물리적 관측량은 그에 대응되는 연산자로 표현할 수 있음을 알 수 있다. 예컨대 해밀토니안은 다음과 같은 연산자로 표현할 수 있다.

$$\hat{\mathcal{H}} = \hat{T} + \hat{V} = \frac{\hat{p}^2}{2m} + V(x) = -\frac{\hbar^2}{2m} \frac{\partial^2}{\partial x^2} + V(x)$$