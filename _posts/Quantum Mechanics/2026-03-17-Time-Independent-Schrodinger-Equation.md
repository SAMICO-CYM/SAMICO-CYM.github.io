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

---

## Remark 1
시간 무관 슈뢰딩거 방정식의 고유값 $E$와 고유함수 $\psi$에 대해서 해밀토니안 연산자의 기댓값을 구해보자.

$$\begin{align*}
\langle \hat{\mathcal{H}} \rangle &= \int_{-\infty}^{\infty} \psi^*(x) \hat{\mathcal{H}} \psi(x) dx \\
&= \int_{-\infty}^{\infty} \psi^*(x) E \psi(x) dx \\
&= E \int_{-\infty}^{\infty} \psi^*(x) \psi(x) dx \\
&= E
\end{align*}$$

제곱의 기댓값 또한 구할 수 있다.

$$\begin{align*}
\langle \hat{\mathcal{H}}^2 \rangle &= \int_{-\infty}^{\infty} \psi^*(x) \hat{\mathcal{H}}^2 \psi(x) dx \\
&= \int_{-\infty}^{\infty} \psi^*(x) E^2 \psi(x) dx \\
&= E^2 \int_{-\infty}^{\infty} \psi^*(x) \psi(x) dx \\
&= E^2
\end{align*}$$

따라서 해밀토니안 연산자의 표준편차는 다음과 같다.

$$\sigma_{\mathcal{H}} = \sqrt{\langle \hat{\mathcal{H}}^2 \rangle - \langle \hat{\mathcal{H}} \rangle^2} = \sqrt{E^2 - E^2} = 0$$

이는 정상상태에서 측정한 에너지의 uncertainity가 0임을 의미한다. 즉, 정상상태에서는 에너지가 정확하게 $E$로 결정된다.

---

## Remark 2
시간 무관 슈뢰딩거 방정식에서 각 고유값 $E_n$에 대응되는 고유함수를 $\psi_n$이라고 하자. 이때 시간 무관 슈뢰딩거 방정식은 선형 미분 방정식이기 때문에 그 해집합은 벡터 공간이 되므로, 방정식의 일반해는 선형종속인 해들의 선형 결합으로 나타내어진다. 즉, 임의의 해 $\Psi(x, t)$는 다음과 같이 쓸 수 있다. 

$$\Psi(x, t) = \sum_{n=1}^\infty c_n \psi_n(x) e^{-i \frac{E_n}{\hbar} t}$$

이러한 표현으로 해밀토니안의 기대값을 구해보자.

우선 각 고유함수들의 집합 $\\{ \psi _n \\}_{n=1}^\infty$는 orthonormal set임을 보이자. 우선

$$\begin{align*}
\langle \psi_m \vert \hat{\mathcal{H}} \psi_n \rangle &= \langle \psi_m \vert E_n \psi_n \rangle \\
&= E_n \langle \psi_m \vert \psi_n \rangle
\end{align*}$$

이 성립하고, 반대로 해밀토니안 연산자를 반대쪽에 취해주면

$$\begin{align*}
\langle \psi_m \vert \hat{\mathcal{H}} \psi_n \rangle &= \langle \hat{\mathcal{H}} \psi_m \vert \psi_n \rangle \\
&= E_m \langle \psi_m \vert \psi_n \rangle
\end{align*}$$

이 성립한다. 이 두 식의 값이 같기 때문에 

$$(E_n - E_m) \langle \psi_m \vert \psi_n \rangle = 0$$

이 성립한다. 따라서 $E_n \neq E_m$이면 $\langle \psi_m \vert \psi_n \rangle = 0$이므로, 각 고유함수들은 서로 orthogonal하다. 또한 파동함수는 규격화되어야 하기 때문에 $n = m$인 경우 $\langle \psi_n \vert \psi_n \rangle = 1$이 성립한다. 즉, 각 고유함수들의 집합 $\{ \psi _n \}_{n=1}^\infty$는 orthonormal set이다. 

따라서 

$$\begin{align*}
\langle \hat{\mathcal{H}} \rangle &= \int_{-\infty}^{\infty} \Psi^*(x, t) \hat{\mathcal{H}} \Psi(x, t) dx \\
&= \int_{-\infty}^{\infty} \left( \sum_{n=1}^\infty c_n^* \psi_n^*(x) e^{i \frac{E_n}{\hbar} t} \right) \hat{\mathcal{H}} \left( \sum_{m=1}^\infty c_m \psi_m(x) e^{-i \frac{E_m}{\hbar} t} \right) dx \\
&= \int_{-\infty}^{\infty} \sum_{n=1}^\infty \sum_{m=1}^\infty c_n^* c_m \psi_n^*(x) \psi_m(x) e^{i \frac{E_n - E_m}{\hbar} t} \hat{\mathcal{H}} dx \\
&= \int_{-\infty}^{\infty} \sum_{n=1}^\infty \sum_{m=1}^\infty c_n^* c_m \psi_n^*(x) \psi_m(x) e^{i \frac{E_n - E_m}{\hbar} t} E_m dx \\
&= \sum_{n=1}^\infty \sum_{m=1}^\infty c_n^* c_m E_m e^{i \frac{E_n - E_m}{\hbar} t} \int_{-\infty}^{\infty} \psi_n^*(x) \psi_m(x) dx \\
&= \sum_{n=1}^\infty \vert c_n \vert^2 E_n
\end{align*}$$

$$\langle \hat{\mathcal{H}} \rangle = \sum_{n=1}^\infty \vert c_n \vert^2 E_n$$

그리고 상수 $\vert c_n \vert^2$은 각 에너지 고유값 $E_n$을 측정할 확률을 나타낸다. 