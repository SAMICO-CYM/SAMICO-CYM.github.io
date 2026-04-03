---
title: Wave Equation
date: 2026-03-26
categories: [Mathematics, PDE]
tags: []
math: true
---

## Definition
The ***wave equation*** is a second order linear partial differential equation given by

$$
u_{tt} = c^2 u_{xx}
$$

where $c$ is a constant.

---

## Theorem 1
The general solution of the wave equation $u_{tt} = c^2 u_{xx}$ is given by

$$
u(x, t) = f(x + ct) + g(x - ct)
$$

where $f$ and $g$ are arbitrary twice differentiable functions.

### Proof 1
Note that 

$$\partial_{tt} - c^2 \partial_{xx} = (\partial_t - c \partial_x)(\partial_t + c \partial_x)$$

Let $v = u_t + c u_x$. Then the wave equation can be written as

$$
v_t - cv_x = 0,
$$

[which solution is given by $v(x, t) = h(x + ct)$ for some arbitrary function $h$.](<{% post_url PDE/2026-03-10-1st-Order-Linear-PDE-Constant-Coefficients %}#theorem-1>)

Thus, we have

$$
v = u_t + cu_x = h(x + ct)
$$

We can easily verify that $u(x, t) = f(x + ct)$ where $f$ is a function such that $f'(s) = \frac{h(s)}{2c}$. 

$\Big[$ $(\because)$ Since $u_x = f'(x+ct)$ and $u_t = c f'(x+ct)$, we have

$$\begin{align*}
u_t + c u_x &= c f'(x+ct) + c f'(x+ct) \\
&= 2c f'(x+ct) \\
&= h(x+ct) \Big]
\end{align*}$$

Since the homogeneous equation $u_t + cu_x = 0$ has the solution $u(x, t) = g(x - ct)$ and the wave equation is linear, we have the general solution

$$u(x, t) = f(x + ct) + g(x - ct). \blacksquare$$

### Proof 2
We can derive the general solution by the method of change of variables. Let 

$$\begin{align*}
\xi &= x + ct \\
\eta &= x - ct
\end{align*}$$

Then we have

$$\begin{align*}
u_x &= u_\xi + u_\eta \\
u_t &= c(u_\xi - u_\eta)
\end{align*}$$

so that

$$\begin{align*}
u_{xx} &= u_{\xi \xi} + 2 u_{\xi \eta} + u_{\eta \eta} \\
u_{tt} &= c^2 (u_{\xi \xi} - 2 u_{\xi \eta} + u_{\eta \eta}).
\end{align*}$$

Thus the wave equation can be written as

$$\begin{gather*}
u_{tt} - c^2 u_{xx} = -4c^2 u_{\xi \eta} = 0 \\
\implies u_{\xi \eta} = 0.
\end{gather*}$$

The solution to the above equation is $u(x, y) = u(\xi, \eta) = f(\xi) + g(\eta) = f(x+ct) + g(x-ct)$ for some arbitrary twice differentiable functions $f$ and $g$. $\blacksquare$

증명 1의 첫 줄에서 확인한 것처럼, 파동 방정식의 연산자는 두 개의 연산자 $\mathcal{L}_1 = \partial_t - c \partial_x$와 $\mathcal{L}_2 = \partial_t + c \partial_x$의 합성으로 분해할 수 있다.

$$\partial_{tt} - c^2 \partial_{xx} = (\partial_t - c \partial_x)(\partial_t + c \partial_x)$$

이때 각 미분연산자의 characteristic line이 $x + ct = A$, $x - ct = B$로 주어지므로, 변수를 이와 같이 치환하여 두는 방법이 효과가 있다. 

---

## Theorem 2
The initial value problem for the wave equation

$$\begin{cases}
u_{tt} = c^2 u_{xx} \\
u(x, 0) = \phi(x) \\
u_t(x, 0) = \psi(x)
\end{cases}$$

for $-\infty < x < \infty, t > 0$, where $\phi$ and $\psi$ are given functions, has the solution

$$
u(x, t) = \frac{1}{2} [\phi(x + ct) + \phi(x - ct)] + \frac{1}{2c} \int_{x - ct}^{x + ct} \psi(s) ds$$

### Proof
By Theorem 1, the general solution to the wave equation is given by

$$
u(x, t) = f(x + ct) + g(x - ct)$$

Then

$$u_t = cf'(x + ct) - cg'(x - ct)$$

Taking $t = 0$, we have

$$\begin{align*}
&\begin{cases}
f(x) + g(x) = \phi(x) \\
cf'(x) - cg'(x) = \psi(x)
\end{cases}
\\
\implies &\begin{cases}
f'(x) + g'(x) = \phi'(x) \\
f'(x) - g'(x) = \frac{\psi(x)}{c}
\end{cases}
\\
\implies &\begin{cases}
f'(x) = \frac{1}{2} \left( \phi'(x) + \frac{\psi(x)}{c} \right) \\
g'(x) = \frac{1}{2} \left( \phi'(x) - \frac{\psi(x)}{c} \right)
\end{cases}
\\
\implies &\begin{cases}
f(x) = \frac{1}{2} \phi(x) + \frac{1}{2c} \int^x \psi(s) ds  + C_1 \\
g(x) = \frac{1}{2} \phi(x) - \frac{1}{2c} \int^x \psi(s) ds  + C_2
\end{cases}
\end{align*}$$

Since $\phi(x) = f(x) + g(x) = \phi(x) + C_1 + C_2$, we have $C_1 + C_2 = 0$.

Thus the particular solution is

$$
\begin{align*}
u(x, t) &= f(x + ct) + g(x - ct) \\
&= \frac{1}{2} [\phi(x + ct) + \phi(x - ct)] + \frac{1}{2c} \int_{x - ct}^{x + ct} \psi(s) ds. \blacksquare
\end{align*}
$$

---

## Remark
$xt$ 평면 위 점 $(x_0, 0)$에서의 초기 조건 $\phi(x_0)$와 $\psi(x_0)$는 시간이 흐름에 따라, 즉 $t > 0$에서 오직 $x_0 - ct < x < x_0 + ct$ 영역에만 영향을 미칠 수 있다. 그림으로 그리면 다음과 같은 삼각형 모양의 영역이 그려질 것이고, 이를 ***domain of influence***라고 부른다.

![alt text](assets/img/domaininfluence.png)

한편 정리 2에서 유도한 1차원 파동방정식의 초기값 문제의 해의 꼴을 보면, $u(x, t)$는 오직 $x \pm ct$에서의 $\phi$값과 구간 $[x-ct, x+ ct]$에서의 $\psi$값에만 의존함을 알 수 있다. 이때 만약 $\phi$와 $\psi$가 구간 $\vert x \vert > R$에서 사라진다면, 구간 $[x-ct, x+ct]$에서 초기 조건 $\phi(x)$와 $\psi(x)$의 값에 의해서만 $u(x,t)$가 결정되므로, $\vert x \vert > R + ct$인 영역에서는 $u(x,t) = 0$임을 알 수 있다. 다르게 말하면 구간 $\vert x \vert \le R$에서의 domain of influence는 $\\{ (x, t) \mid \vert x \vert < R + ct \\}$이다. 

이 논리를 거꾸로 생각해보자. 즉, $xt$ 평면 위 점 $(x_0, t_0)$에서의 해 $u(x_0, t_0)$가 결정되기 위해서는 어떤 초기 조건이 필요할까? 앞서 보았던 것처럼 $u(x_0, t_0)$는 $x_0 \pm ct_0$에서의 $\phi$값과 구간 $[x_0-ct_0, x_0+ ct_0]$에서의 $\psi$값에 의해서만 결정된다. 따라서 $u(x_0, t_0)$를 결정하기 위해서는 $[x_0-ct_0, x_0+ ct_0]$에서의 정보가 필요하고, 그림을 그려보면 다음과 같은 삼각형 모양의 영역이 그려질 것이다. 이를 ***domain of dependence***라고 부른다.

![alt text](assets/img/domaindependence.png)
---

## Conservation of Energy
상수 값의 선밀도 $\rho$와 장력 $T$를 가지는 무한한 길이의 줄을 생각하자. 이때 초기값과 함께 파동 방정식이 다음과 같이 주어졌다고 가정하자. 

$$ \begin{cases}
\rho u_{tt} = T u_{xx}, \quad -\infty < x < \infty, t > 0 \\
u(x, 0) = \phi(x), \quad u_t(x, 0) = \psi(x) \\
\phi(x) = 0 = \psi(x) \quad \text{for } |x| > R
\end{cases}$$

그러면 영역 $\\{ (x, t) \mid \vert x \vert > R + ct \\}$에서 $u(x, t) = 0$이다.

한편 ***운동 에너지***와 ***퍼텐셜 에너지***를 각각 다음과 같이 정의하자.

$$\begin{align*}
K(t) &= \frac{1}{2} \int_{-\infty}^\infty \rho u_t^2 dx \\
V(t) &= \frac{1}{2} \int_{-\infty}^\infty T u_x^2 dx
\end{align*}$$

이때 다음을 얻는다.

$$\begin{align*}
\frac{dK}{dt} &= \int_{-\infty}^\infty \rho u_t u_{tt} dx \\
&= \int_{-\infty}^\infty \rho u_t (c^2 u_{xx}) dx \\
&= \rho c^2 \int_{-\infty}^\infty u_t u_{xx} dx \\
&= \rho c^2 \left[ u_t u_x \right]_{-\infty}^\infty - \rho c^2 \int_{-\infty}^\infty u_t u_{xx} dx \\
&= - \frac{d}{dt} \left( \frac{1}{2} \int_{-\infty}^\infty T u_x^2 dx \right) \\
&= - \frac{dV}{dt}
\end{align*}$$

***전체 에너지***를 $E = K + V$로 정의하면 

$$\begin{align*}
\frac{dE}{dt} &= \frac{dK}{dt} + \frac{dV}{dt} = 0
\end{align*}$$

을 얻고, 따라서 전체 에너지 

$$
E = K + V = \frac{1}{2} \int_{-\infty}^\infty (\rho u_t^2 + T u_x^2) dx
$$

는 시간에 대해 상수값을 가짐을 알 수 있다. 즉, 에너지는 보존된다. 