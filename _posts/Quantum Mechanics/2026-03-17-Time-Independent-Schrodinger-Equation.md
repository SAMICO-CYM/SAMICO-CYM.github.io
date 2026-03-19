---
title: Time-Independent Schrodinger Equation
date: 2026-03-17
categories: [Physics, Quantum Mechanics]
tags: []
math: true
---

## Time-Independent Schrodinger Equation
해밀토니안 연산자에 대응되는 고유값 방정식을 다음과 같이 작성할 수 있다.

$$\hat{\mathcal{H}} \Psi = \left( - \frac{\hbar^2}{2m} \frac{\partial^2}{\partial x^2} + V(x) \right) \Psi = E \Psi$$

한편 두 번째 식은 시간 의존 슈뢰딩거 방정식의 형태와 대응되므로 다음과도 같이 쓸 수 있다.

$$i \hbar \Psi_t = - \frac{\hbar^2}{2m} \Psi_{xx} + V \Psi$$

이때 파동함수 $\Psi(x, t)$가 각각의 변수로 분리된다고 가정하면, 즉 $\Psi(x,t) = \psi(x) \phi(t)$로 가정하면 다음과 같다.

$$\begin{align*} 
i \hbar \psi \phi_t &= \left( - \frac{\hbar}{2m} \psi_{xx} + V \psi \right) \phi = E \psi \phi \\
\implies i \hbar \frac{\phi_t}{\phi} &= - \frac{\hbar}{2m} \frac{\psi_{xx}}{\psi} + V = E \\
\end{align*}$$

따라서 다음의 두 식을 얻는다.

**(i)** $i \hbar \varphi_t = E \varphi$

**(ii)** $- \frac{\hbar}{2m} \psi_{xx} + V \psi = E \psi$

이때 두 번째 식을 시간 무관 슈뢰딩거 방정식이라고 부른다. 해밀토니안 연산자를 사용해 표현하면 다음과 같이 쓸 수 있다.

$$\hat{\mathcal{H}} \psi = E \psi$$

---

## Stationary States
위 (i)식을 풀면 다음의 일반해를 얻는다. 

$$\varphi(t) = Ce^{-i \frac{E}{\hbar} t} \quad (C \text{ is a constant.})$$

시간 무관 슈뢰딩거 방정식의 해를 $\psi(x)$라고 하면, 시간 의존 슈뢰딩거 방정식의 해는 다음과 같이 쓸 수 있다.

$$\Psi(x, t) = \psi(x) \varphi(t) = \psi(x) e^{-i \frac{E}{\hbar} t}$$

상수 $C$는 normalization condition에 의해 $1$로 결정된다. 이에 대해서 임의의 연산자 $\hat{Q}(\hat{x}, \hat{p})$의 기댓값을 계산하면 다음과 같다.

$$\begin{align*} \langle \hat{Q} \rangle &= \int_{-\infty}^{\infty} \Psi^*(x, t) \hat{Q} \Psi(x, t) dx \\ &= \int_{-\infty}^{\infty} \psi^*(x) e^{i \frac{E}{\hbar} t} \hat{Q} \psi(x) e^{-i \frac{E}{\hbar} t} dx \\ &= \int_{-\infty}^{\infty} \psi^*(x) \hat{Q} \psi(x) dx \end{align*}$$ 

따라서 기댓값 또한 time-independent하고, 이러한 상태를 stationary state라고 부른다. 