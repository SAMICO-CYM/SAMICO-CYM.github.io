---
title: Dynamical System
date: 2026-02-19 15:00:00 +0900
categories:
  - Mathematics
  - Dynamics
tags: []
math: true
---
## Dynamical System
1. ***A dynamical system*** consists of a set of possible states, together with a rule that determines the present state in terms of past states.

---
## Fixed Point
1. A function $f: X \to X$ whose domain and range are the same is called a ***map***. 
2. Let $x$ be a point and let $f$ be a map. ***The orbit of $x$ under $f$*** is the set of points $\\{x, f(x), f^2(x), ... \\}$. The starting point $x$ for the orbit is called the ***initial value*** of the orbit. 
3. A point $p$ is a ***fixed point*** of the map $f$ if $f(p)=p$.

---

## Sink and Source
Let $f$ be a map on $\mathbb{R}$ and let $p$ be a fixed point of the map $f$. 
1. The point $p$ is called a ***sink*** or an ***attracting fixed point*** if $\exists \varepsilon > 0$ such that $$\lim_{k \to \infty} f^k(x) = p, \forall x \in N_\varepsilon(p).$$ 
2. The point $p$ is called a ***source*** or a ***repelling fixed point*** if $\exists \varepsilon > 0$ such that for each $x \in N_{\varepsilon}(p)$ except for $p$, $\exists N \in \mathbb{N}$ such that $f^N(x) \notin N_\varepsilon(p).$ 

---

## Theorem
Lef $f \in C^\infty$ be a map on $\mathbb{R}$, and let $p$ be a fixed point of $f$. Then
1. If 
$|f'(p)| < 1$, 
then $p$ is a sink. 
2. If 
$|f'(p)| > 1$, 
then $p$ is a source.

### Proof
Suppose that $|f'(p)| < 1$. Let $a \in (|f'(p)|, 1)$. Since 

$$\begin{align*} 
& \lim_{x \to p} \frac{|f(x) - f(p)|}{|x-p|} = |f'(p)|,
\end{align*}$$

$\exists \varepsilon > 0$ such that $\forall x \in N_\varepsilon(p)$,

$$\begin{gather*} 
& \frac{|f(x) - f(p)|}{|x - p|} - |f'(p)| < a - |f'(p)| \\ 
\implies &\frac{|f(x) - f(p)|}{|x - p|} < a \\ 
\implies &|f(x) - p| = |f(x) - f(p)| < a |x-p| < \varepsilon \\ 
\implies &f(x) \in N_\varepsilon(p), 
\end{gather*}$$

so that $f^k(x) \in N_\varepsilon(p), \forall k \in \mathbb{N}.$
\
Furthermore, we have 

$$\begin{gather*} |f^k(x) - p| \le a^k|x-p|, \forall k \in \mathbb{N}, \forall x \in N_\varepsilon(p). \end{gather*}$$

$(\because)$ We have shown the case $k=1$. Suppose that 
$|f^k(x) - p| \le a^k|x-p|, \forall x \in N_\varepsilon(p)$ 
holds for some $k > 2$. Since $f^k(x) \in N_\varepsilon(p),$ $\forall x \in N_\varepsilon(p)$, we have 

$$\begin{gather*} |f(f^k(x)) - p| = |f^{k+1}(x) - p| \le a |f^k(x) - p| \\ \le a \cdot a^k|x-p| = a^{k+1}|x-p|, \forall x \in N_\varepsilon(p). \end{gather*}$$

Thus the induction step is finished.

Then it follows that $\forall x \in N_\varepsilon(p),$

$$\begin{gather*} & 0 \le \lim_{k \to \infty} |f^k(x) - p| \le \lim_{k \to \infty} a^k|x-p| = 0 \\ \implies & \lim_{k \to \infty} |f^k(x) - p| = 0 \\ \implies & \lim_{k \to \infty} f^k(x) = p, \end{gather*}$$

which means that $p$ is a sink. 
\
The part 2 is similar to 1. $\blacksquare$

도함수 $f'$는 입력값이 그 근방에서 얼마나 변화하는지에 대한 정량적 척도라고 이해할 수 있으므로, 그 값이 $1$보다 작을 때 반복해서 $f$를 취하면 자연스레 값이 $p$에 수렴하리라고 이해할 수 있다. $1$보다 클 때도 마찬가지로 생각할 수 있다. 
반대로 말하면 $f'(p) = 1$일 때는 함부로 판정할 수 없음을 알 수 있다. 

---
## Periodic Point
- Let $f$ be a map on $\mathbb{R}$. We call $p$ a ***periodic point of period $k$*** of $f$ if $f^k(p) = p$, and if $k$ is the smallest such positive integer. The orbit with initial point $p$ (which consists of $k$ points) is called a ***periodic orbit of period $k$***. We will often use the abbreviated terms ***period-$k$ point*** and ***period-$k$ orbit***.

예컨대 $f(p_1) = p_2, f(p_2) = p_1$을 만족하는 점 $p_1, p_2$가 존재한다고 해보자. 이때 $g = f^2$라는 맵에 대해서 $g(p_1) = f^2(p_1) = p_1$이고, $g(p_2) = f^2(p_2) = p_2$를 만족하므로 이러한 점들은 $g$의 고정점이라고 할 수 있다. 

---

## Periodic Sink and Source
Let $f$ be a map on $\mathbb{R}$ and assume that $p$ is a period-$k$ point of $f$. 
- The period-$k$ orbit of $p$ is a ***periodic sink*** if $p$ is a sink for the map $f^k$. 
- The orbit of $p$ is a ***periodic source*** if $p$ is a source for the map $f^k$.