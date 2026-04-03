---
title: Diffusion Equation
date: 2026-04-03
categories: [Mathematics, PDE]
tags: []
math: true
---

## Definition
The ***diffusion equation*** is a second order linear partial differential equation given by

$$
u_t = k \nu_{xx}$$

where $k > 0$ is a constant.

---

## Theorem 1 (Maximum Principle)
If $u(x, t)$ satisfies the diffusion equation in a rectangle(say, $0 \le x \le L, 0 \le t \le T$) in space-time, then the maximum value of $u(x, t)$ is assumed either initially ($t = 0$) or on the lateral sides ($x = 0$ or $x = L$).

예컨대 $u$를 물체의 위치 $x$와 시간 $t$에서의 온도 분포 함수라고 하자. 만약 별도의 열원이 없는 상태라면 기존의 온도 분포에서 시간이 흐름에 따라 평형 상태로 분포가 변해갈 것이다. 그러면 당연하게도 초기의 온도 분포($t = 0$)에서 $u$가 최소값을 가질 것이다. 

혹은 외부에서 물체에 열을 공급해주는 레저부어가 있다고 생각해보자. 이 열원이 내부에 있지 않는 한, 온도는 열원이 공급되는 물체의 경계($x= 0$ 또는 $x = L$)에서 최대값을 가져야 한다. 이러한 사실을 보장해 주는 정리가 maximum principle이다. 동일한 논리가 최소값에도 성립한다. 

### Proof
Let 

$$M = \max \{ u(x, t) \mid x = 0 \text{ or } x = L \text{ or } t = 0 \}$$

be the maximum value of $u$ on three sides. 

Let $\varepsilon > 0$, and let $v(x, t) = u(x, t) + \varepsilon x^2$. On the three sides, we have 

$$
\begin{align*}
&u(x, t) \le M \\
&\implies u(x, t) + \varepsilon x^2 \le M + \varepsilon x^2 \le M + \varepsilon L^2 \\
&\implies v(x, t) \le M + \varepsilon L^2,
\end{align*}
$$

which means that $M + \varepsilon L^2$ is the maximum value of $v$ on the three sides. Note that $v$ satisfies that 

$$\begin{align*}
v_t - kv_{xx} &= u_t - k(u_{xx} + 2 \varepsilon) \\
&= u_t - k u_{xx} - 2 \varepsilon k \\
&= (u_t - k u_{xx}) - 2 \varepsilon k \\
&= - 2 \varepsilon k < 0 \quad \cdots (\ast)
\end{align*}$$ 

Suppose that $v$ attains its maximum value at an interior point $(x_0, t_0)$ for $0 < x_0 < L$ and $0 < t_0 < T$. Then we have $v_t = 0$ and $v_{xx} \le 0$ at this point, so that

$$
0 > -2\varepsilon k = v_t - kv_{xx} = -kv_{xx} \ge 0. \bigotimes
$$

Suppose that, again, $v$ attains its maximum value at the top edge $(x_0, T)$ for $0 < x_0 < L$. Then we have $v_x \ge 0$ and $v_{xx} \le 0$ at this point. Note that

$$v_t(x_0, T) = \lim_{h \to 0^+} \frac{v(x_0, T) - v(x_0, T - h)}{h} > 0.$$

Then we have

$$
0 > -2\varepsilon k = v_t - kv_{xx} \ge 0. \bigotimes
$$

Since $v$ has a maximum value somewhere in the closed rectangle $R = \{ (x, t) \mid 0 \le x \le L, 0 \le t \le T \}$, $v$ must attain its maximum value on the bottom or sides. Thus $v(x, t) \le M + \varepsilon L^2$ throughout $R$. Since $\varepsilon$ is an arbitrary positive number, we have that for all $(x, t) \in R$,

$$\begin{align*}
v(x, t) \le M + \varepsilon L^2 \\
\implies u(x, t) \le M + \varepsilon (L^2 - x^2) \\
\implies u(x, t) \le M.
\end{align*}$$

Thus $u$ attains its maximum value on the bottom or sides. $\blacksquare$

---

## Corollary (Minimum Principle)
If $u(x, t)$ satisfies the diffusion equation in a rectangle(say, $0 \le x \le l, 0 \le t \le T$) in space-time, then the minimum value of $u(x, t)$ is assumed either initially ($t = 0$) or on the lateral sides ($x = 0$ or $x = l$).

### Proof
Apply Maximum principle to $-u(x, t)$. $\blacksquare$