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

## Ladder Operators 1

방정식을 풀기에 앞서, ***사다리 연산자*** $\hat{a_+}, \hat{a_-}$를 다음과 같이 정의하자.

$$\begin{align*}
\hat{a_+} &= \frac{1}{\sqrt{2 m\hbar \omega}} \left( m \omega \hat{x} - i \hat{p} \right) \\
\hat{a_-} &= \frac{1}{\sqrt{2 m\hbar \omega}} \left( m \omega \hat{x} + i \hat{p} \right)
\end{align*}$$

이때 $\hat{a_+}$를 ***raising operator***, $\hat{a_-}$를 ***lowering operator***라고 부른다. 그러면 다음이 성립한다.

**(i)** $[\hat{a_+}, \hat{a_-}] = 1$

**(ii)** $\hat{a_+} \hat{a_-} = \frac{1}{\hbar \omega} \left( \hat{H} - \frac{1}{2} \hbar \omega \right) = \frac{1}{\hbar \omega} \hat{\mathcal{H}} - \frac{1}{2}$

**(iii)** $\hat{a_-} \hat{a_+} = \frac{1}{\hbar \omega} \left( \hat{H} + \frac{1}{2} \hbar \omega \right) = \frac{1}{\hbar \omega} \hat{\mathcal{H}} + \frac{1}{2}$

**(iv)** $\hat{H} = \hbar \omega \left( \hat{a_+} \hat{a_-} + \frac{1}{2} \right) = \hbar \omega \left( \hat{a_-} \hat{a_+} - \frac{1}{2} \right)$

즉 해밀토니안 연산자는 사다리 연산자를 이용해서 표현할 수 있다.

---

## Theorem
If $\psi$ is the solution of the time-independent Schrödinger equation for the 1D harmonic oscillator, then $\hat{a_+}\psi$ and $\hat{a_-}\psi$ are also solutions with the eigenvalue $E + \hbar \omega$ and $E - \hbar \omega$, respectively.

### Proof
Suppose that $\hat{\mathcal{H}}\psi = E \psi$. Then we have

$$\begin{align*}
\hat{\mathcal{H}}(\hat{a_+}\psi) &= \hbar \omega \left( \hat{a_+} \hat{a_-} + \frac{1}{2} \right) (\hat{a_+}\psi) \\
&= \hbar \omega \hat{a_+} \left( \hat{a_-} \hat{a_+} + \frac{1}{2} \right) \psi \\
&= \hbar \omega \hat{a_+} \left( \hat{a_+} \hat{a_-} + 1 + \frac{1}{2} \right) \\
&= \hat{\mathcal{H}} (\hat{a_+} \psi) + \hbar \omega (\hat{a_+} \psi) \\
&= (E + \hbar \omega) (\hat{a_+} \psi)
\end{align*}$$

Thus $\hat{\mathcal{H}}(\hat{a_+}\psi) = (E + \hbar \omega) (\hat{a_+} \psi)$. Similarly, we have 

$$\hat{\mathcal{H}}(\hat{a_-}\psi) = (E - \hbar \omega) (\hat{a_-} \psi). \blacksquare$$

이말인즉슨, 조화진동자의 파동함수 $\psi$에 사다리 연산자를 적용시키면 기존의 에너지 $E$에서 $\hbar \omega$만큼 더하거나 줄어드는 결과를 얻는다. 즉 $\hat{a_+}$는 에너지를 $\hbar \omega$ 단위 만큼 증가시키는, 반대로 $\hat{a_-}$는 $\hbar \omega$ 단위 만큼 감소시키는 연산자라고 이해할 수 있다. 그리고 우리는 $\hbar \omega$는 광자 하나의 에너지에 대응된다는 것을 알고 있다. 

---

## Simple Harmonic Oscillator

이제 본격적으로 조화진동자의 파동함수과 에너지를 구해보자. 

우선 파동함수에 lowering operator를 반복적으로 취할수록 점점 낮은 에너지값을 얻게 된다. 그런데 자명하게 에너지가 무한히 낮아질수는 없으므로 입자가 가질 수 있는 에너지의 최소값, 즉 바닥 상태가 존재할 것이고, 그때 대응되는 파동함수를 $\psi_0$라고 하면 다음과 같이 정의한다.

$$\hat{a_-} \psi_0 = 0$$

이 식을 정리하면 다음과 같다.

$$\begin{align*}
\hat{a_-} \psi_0 &= \frac{1}{\sqrt{2 m\hbar \omega}} \left( m \omega \hat{x} + i \hat{p} \right) \psi_0 \\
&= \frac{1}{\sqrt{2 m\hbar \omega}} \left( m \omega x + \hbar \frac{d}{dx} \right) \psi_0 \\
\implies \frac{d \psi_0}{dx} &= - \frac{m \omega}{\hbar} x \psi_0 \\
\implies \psi_0(x) &= \left( \frac{m \omega}{\pi \hbar} \right)^{1/4} \exp \left( -\frac{m \omega}{2 \hbar} x^2 \right)
\end{align*}$$

한편

$$\begin{align*}
\hat{\mathcal{H}} \psi_0 &= \hbar \omega \left( \hat{a_+} \hat{a_-} + \frac{1}{2} \right) \psi_0 \\
&= \hbar \omega \left( \frac{1}{2} \right) \psi_0 \\
&= \frac{1}{2} \hbar \omega
\end{align*}$$

이므로 바닥 상태의 에너지는 $E_0 = \frac{1}{2} \hbar \omega$이다. 한편 사다리 연산자는 에너지를 $\hbar \omega$만큼 올리고 내리는 연산자였으므로 각 자연수 $n = 1, 2, ...$에 대해서 파동함수의 에너지 $E_n$은 

$$E_n = \hbar \omega \left( n + \frac{1}{2} \right)$$

으로 주어진다. 

---

## Ladder Operators 2
위의 결과를 참고하면 다음의 식이 성립한다.

**(i)** $\hat{a_+}\hat{a_-} \psi_n = n \psi_n$ 

**(ii)** $\hat{a_-}\hat{a_+} \psi_n = (n+1) \psi_n$ 

**(iii)** $\hat{a_+} \psi_n = \sqrt{n+1} \psi_{n+1}$ 

**(iv)** $\hat{a_-} \psi_n = \sqrt{n} \psi_{n-1}$ 

**(v)** $\psi_n(x) = \frac{1}{\sqrt{n!}} (a_+)^n \psi_0(x)$ 

### Proof
(i) 

$$\begin{align*}
\hat{a_+}\hat{a_-} \psi_n &= \left( \frac{1}{\hbar \omega} \hat{\mathcal{H}} - \frac{1}{2}\right) \psi_n \\
&= \left( n + \frac{1}{2} \right) \psi_n - \frac{1}{2} \psi_n \\
&= n \psi_n
\end{align*}$$

(ii)

$$\begin{align*}
\hat{a_-}\hat{a_+} \psi_n &= \left( \frac{1}{\hbar \omega} \hat{\mathcal{H}} + \frac{1}{2}\right) \psi_n \\
&= \left( n + \frac{1}{2} \right) \psi_n + \frac{1}{2} \psi_n \\
&= (n+1) \psi_n
\end{align*}$$
