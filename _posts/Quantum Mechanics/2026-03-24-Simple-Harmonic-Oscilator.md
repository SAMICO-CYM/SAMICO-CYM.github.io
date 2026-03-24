---
title: Simple Harmonic Oscillator
date: 2026-03-24
categories: [Physics, Quantum Mechanics]
tags: []
math: true
---

## Remark
1차원 조화 진동자를 고려하자. 이때 각 물리량은 다음과 같이 주어진다.

$$\begin{align*}
F &= -kx \\
x(t) &= A \sin \omega t + B \cos \omega t \quad \text{where } \omega = \sqrt{\frac{k}{m}} \\
p(t) &= m \dot{x}(t) = m \omega (A \cos \omega t - B \sin \omega t) \\
T &= \frac{p^2}{2m} \\
V &= \frac{1}{2}kx^2 = \frac{1}{2}m \omega^2 x^2 \\
E &= T + V = \frac{1}{2} m \omega^2 (A^2 + B^2)
\end{align*}$$

따라서 1차원 조화 진동자의 시간 무관 슈뢰딩거 방정식은 다음과 같이 주어진다.

$$\begin{align*}
\left( -\frac{\hbar^2}{2m} \frac{d^2}{dx^2} + \frac{1}{2} m \omega^2 x^2 \right) \psi(x) = E \psi(x)
\end{align*}$$

---

## Ladder Operators

방정식을 풀기에 앞서, 사다리 연산자 $\hat{a_+}, \hat{a_-}$를 다음과 같이 정의하자.

$$\begin{align*}
\hat{a_+} &= \frac{1}{\sqrt{2 m\hbar \omega}} \left( m \omega \hat{x} - i \hat{p} \right) \\
\hat{a_-} &= \frac{1}{\sqrt{2 m\hbar \omega}} \left( m \omega \hat{x} + i \hat{p} \right)
\end{align*}$$

그러면 다음이 성립한다.

**(i)** $[\hat{a_+}, \hat{a_-}] = 1$

**(ii)** $\hat{H} = \hbar \omega \left( \hat{a_+} \hat{a_-} + \frac{1}{2} \right) = \hbar \omega \left( \hat{a_-} \hat{a_+} - \frac{1}{2} \right)$