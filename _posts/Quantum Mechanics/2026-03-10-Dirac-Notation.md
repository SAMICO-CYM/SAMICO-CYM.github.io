---
title: Dirac Notation
date: 2026-03-10
categories: [Physics, Quantum Mechanics]
tags: []
math: true
---

## Dirac Notation
양자역학에서는 벡터와 내적을 Dirac notation으로 표기한다. 예컨대 벡터 $x \in \mathbb{C}^n$은 다음과 같이 표기한다. 

$$\vert x \rangle = \begin{bmatrix} x_1 \\ \vdots \\ x_n \end{bmatrix}$$

한편 $\vert x \rangle$의 conjugate transpose는 다음과 같이 표기한다.

$$\langle x \vert = \vert x \rangle^{\dagger} = \begin{bmatrix} x^*_1 & \cdots & x^*_n \end{bmatrix}$$

이렇게 벡터를 표기한 방법을 braket notation이라고 부른다. 이러한 braket notation을 가지고 내적을 다음과 같이 표기할 수 있다.

$$\langle x \vert y \rangle = \sum_{i=1}^n x^*_iy_i$$

또한 선형 연산자 $A$에 대해서 다음의 관계가 성립한다.

$$\begin{align*}
& (i) \vert Ax \rangle = A \vert x \rangle \\
& (ii) \langle Ax \vert = \langle x \vert A^{\dagger} \\
& (iii) \langle x \vert Ay \rangle = \langle x \vert A \vert y \rangle = \langle A^{\dagger} x \vert y \rangle 
\end{align*}$$