---
title: Commutator
date: 2026-03-17
categories: [Physics, Quantum Mechanics]
tags: []
math: true
---

## Commutator
Let $\hat{A}$ and $\hat{B}$ be two linear operators. The ***commutator*** of $\hat{A}$ and $\hat{B}$ is defined by

$$[\hat{A}, \hat{B}] = \hat{A}\hat{B} - \hat{B}\hat{A}$$

## Remark
위치 연산자 $\hat{x}$와 운동량 연산자 $\hat{p}$의 교환자는 다음과 같이 계산된다.

$$\begin{align*} 
[\hat{x}, \hat{p}] &= \hat{x}\hat{p} - \hat{p}\hat{x} \\
&= x \left(-i \hbar \frac{\partial}{\partial x}\right) - \left(-i \hbar \frac{\partial}{\partial x}\right) x \\
&= -i \hbar \left( x \frac{\partial}{\partial x} - \frac{\partial}{\partial x} x \right) \\
&= -i \hbar \left( x \frac{\partial}{\partial x} - \left( 1 + x \frac{\partial}{\partial x} \right) \right) \\
&= -i \hbar \left( -1 \right) \\
&= i \hbar
\end{align*}$$

## Uncertainty Principle
