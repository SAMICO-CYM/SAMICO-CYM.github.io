--- 
title: The Logistic Maps
date: 2026-02-19 16:00:00 +0900
categories: [Mathematics, Dynamics]
tags: []
math: true
---

## Logistic Map
- For $a \ge 0$, we call $g_a(x) = ax(1-x)$ the ***logistic map***. 

---

### Properties
- If $1 < a \le 4$, then $p = \frac{a-1}{a}$ is a fixed point of the logistic map $g_a: [0, 1] \to [0, 1]$.
- If $1 < a < 3$, then $p = \frac{a-1}{a}$ is a sink, and if $a \ge 3$, then it is a source.

---

## Bifurcation Diagram
![image](assets/img/Pasted%20image%2020260220163028.png)
위와 같은 그림을 로지스틱 맵의 ***bifucation diagram***이라고 부른다. 이 다이어그램은 컴퓨터에서 다음과 같은 과정을 반복함으로 그릴 수 있다.
1. Choose a value of $a$, starting with $a=1$.
2. Choose $x$ at random in $[0, 1]$.
3. Calculate the orbit of $x$ under $g_a(x)$.
4. Ignore the first $100$ iterates and plot the orbit beginning with iterate $101$. Then increment $a$ and begin the procedure again.

그림에서도 알 수 있듯, $1 \le a \le 3$까지 맵은 주기가 1인 고정점을 가지고 이후부터는 주기가 2가 되고, 좀 더 가서는 주기가 4가 되는 식으로 형성된다. 이와 같이 $a$가 증가할수록 period-$2^n$ orbit이 형성됨을 알 수 있다. 그러나 조금 더 가면 점이 무수히 많이 찍히며 ***chaotic***한 모습을 형성함을 확인할 수 있다. 

---

## When $a=4$
로지스틱 맵에서 $a=4$일 때, 즉 $g_4(x) = 4x(1-x) = G(x)$라고 하자. 이때 다음이 성립한다.
- $G^k$ has $2^k$ fixed points.
- $G$ has fewer than $2^k$ points of period-$k$ ($k > 1$).