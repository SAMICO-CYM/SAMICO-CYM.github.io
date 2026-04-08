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
u_t = k u_{xx}$$

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
u(x, t) \le M &\implies u(x, t) + \varepsilon x^2 \le M + \varepsilon x^2 \le M + \varepsilon L^2 \\
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

Since $v$ has a maximum value somewhere in the closed rectangle $R = \\{ (x, t) \mid 0 \le x \le L, 0 \le t \le T \\}$, $v$ must attain its maximum value on the bottom or sides. Thus $v(x, t) \le M + \varepsilon L^2$ throughout $R$. Since $\varepsilon$ is an arbitrary positive number, we have that for all $(x, t) \in R$,

$$\begin{align*}
&v(x, t) \le M + \varepsilon L^2 \\
\implies &u(x, t) \le M + \varepsilon (L^2 - x^2) \\
\implies &u(x, t) \le M.
\end{align*}$$

Thus $u$ attains its maximum value on the bottom or sides. $\blacksquare$

---

## Corollary (Minimum Principle)
If $u(x, t)$ satisfies the diffusion equation in a rectangle(say, $0 \le x \le l, 0 \le t \le T$) in space-time, then the minimum value of $u(x, t)$ is assumed either initially ($t = 0$) or on the lateral sides ($x = 0$ or $x = l$).

### Proof
Apply Maximum principle to $-u(x, t)$. $\blacksquare$

---

## Theorem 2
There is at most one solution to the problem

$$\begin{cases}

u_t - k u_{xx} = f(x, t) & 0 < x < L, t > 0 \\
u(x, 0) = \phi(x) \\
u(0, t) = g(t), \quad u(L, t) = h(t)
\end{cases}$$

where $f, \phi, g, h$ are given functions.

### Proof 1 (Maximum Principle)
Let $u_1, u_2$ be two solutions, and let $w \equiv u_1 - u_2$. Then $w$ satisfies

$$\begin{cases}

w_t - k w_{xx} = 0 \\
w(x, 0) = 0 \\
w(0, t) = 0, \quad w(L, t) = 0
\end{cases}$$

By Maximum principle, $w(x, t) \le 0$ for all $0 \le x \le L$ and $t \ge 0$. Similarly, by Minimum principle, $w(x, t) \ge 0$ for all $0 \le x \le L$ and $t \ge 0$. Thus $w(x, t) = 0$ for all $0 \le x \le L$ and $t \ge 0$ and therefore, $u_1(x, t) = u_2(x, t)$ for all $0 \le x \le L$ and $t \ge 0$. $\blacksquare$

### Proof 2 (Energy)
Let $u_1, u_2$ be two solutions, and let $w \equiv u_1 - u_2$. Then $w$ satisfies

$$\begin{cases}

w_t - k w_{xx} = 0 \\
w(x, 0) = 0 \\
w(0, t) = 0, \quad w(L, t) = 0
\end{cases}$$

Multiplying the equation for $w$ by $w$ itself, we have 

$$\begin{align*}
0 &= 0 \cdot w \\
&= (w_t - kw_{xx})w \\
&= w_t w - k w_{xx} w \\
&= \left( \frac{1}{2} w^2 \right)_t - (k w_x w)_x + k (w_x)^2.
\end{align*}$$

Integrating over $0 < x < L$, we get

$$\begin{align*}
0 &= \int_0^L \left( \frac{1}{2} w^2 \right)_t dx - \int_0^L (k w_x w)_x dx + \int_0^L k (w_x)^2 dx \\
&= \frac{d}{dt} \int_0^L \frac{1}{2} w^2 dx - \left[ k w_x w \right]_0^L + \int_0^L k (w_x)^2 dx.
\end{align*}$$

Then 

$$\begin{align*}
\frac{d}{dt} \int_0^L \frac{1}{2} w^2 dx &= - \int_0^L k (w_x)^2 dx \le 0,
\end{align*}$$

which means that the energy $\int_0^L \frac{1}{2} w^2 dx$ is non-increasing in $t$. Thus

$$0 \le \int_0^L \frac{1}{2} w^2 dx \le \int_0^L \frac{1}{2} w(x, 0)^2 dx = 0,$$

which implies that $w(x, t) = 0$ for all $0 \le x \le L$ and $t \ge 0$. Therefore, $u_1(x, t) = u_2(x, t)$ for all $0 \le x \le L$ and $t \ge 0$. $\blacksquare$ 

---

## Theorem 3
The problem 

$$\begin{cases}

u_t = k u_{xx} & 0 < x < L, t > 0 \\
u(x, 0) = \phi(x) \\
u(0, t) = 0 = u(L, t)
\end{cases}$$

satiesfies the stability.

### Proof 1 ($L^2$ sense)
Let $u_1, u_2$ be two solutions, and let $u_1(x, 0) = \phi_1(x)$ and $u_2(x, 0) = \phi_2(x)$. Let $w \equiv u_1 - u_2$. By the energy method of the previous theorem, we have

$$
\int_0^L \frac{1}{2} w(x, t)^2 dx \le \int_0^L \frac{1}{2} w(x, 0)^2 dx.
$$

Then we get

$$\int_0^L (u_1 - u_2)^2 dx \le \int_0^L (\phi_1 - \phi_2)^2 dx.$$

Note that RHS is independent of $t$, so that it is just a constant. This means that if we start nearby at $t=0$, then we stay nearby for all $t > 0$. Thus the solution is stable. $\blacksquare$

### Proof 2 (Uniform sense)
Let $u_1, u_2$ be two solutions, and let $u_1(x, 0) = \phi_1(x)$ and $u_2(x, 0) = \phi_2(x)$. Let $w \equiv u_1 - u_2$. Then $w = 0$ on the lateral sides of the rectangle, and $w$ satisfies

$$\begin{cases}

w_t - k w_{xx} = 0 \\
w(x, 0) = \phi_1(x) - \phi_2(x) \\
w(0, t) = 0 = w(L, t)
\end{cases}$$

By Maximum principle, we have

$$u_1 - u_2 \le \max \vert \phi_1 - \phi_2 \vert$$

and by Minimum principle, we have

$$u_1 - u_2 \ge - \max \vert \phi_1 - \phi_2 \vert$$

Thus we get

$$\vert u_1 - u_2 \vert \le \max \vert \phi_1 - \phi_2 \vert.$$ 

Note that RHS is independent of $t$, so that it is just a constant. This means that if we start nearby at $t=0$, then we stay nearby for all $t > 0$. Thus the solution is stable. $\blacksquare$