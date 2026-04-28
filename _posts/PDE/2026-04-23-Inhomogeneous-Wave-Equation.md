---
title: Inhomogeneous Wave Equation
date: 2026-04-23
categories: [Mathematics, PDE]
tags: []
math: true
---

## Theorem 1
The solution of the initial value problem

$$ \begin{cases} 
u_{tt} - c^2 u_{xx} = f(x, t) \\
u(x, 0) = \phi(x), \quad u_t(x, 0) = \psi(x)
\end{cases} $$

for $-\infty < x < \infty, t >0$, where $f, \phi$ and $\psi$ are given functions, is given by

$$
u(x, t) = \frac{1}{2} [\phi(x-ct) + \phi(x+ct)] + \frac{1}{2c} \int_{x-ct}^{x+ct} \psi(s) \, ds + \frac{1}{2c} \iint_{\Delta} f,
$$ 

where $\Delta$ is the characteristic triangle, that is,

$$
\frac{1}{2c} \iint_{\Delta} f = \frac{1}{2c} \int_0^t \int_{x - c(t - s)}^{x + c(t - s)} f(y, s) \, dy ds
$$

### Proof
We already know that when $f \equiv 0$, $u(x, t) = \frac{1}{2} [\phi(x-ct) + \phi(x+ct)] + \frac{1}{2c} \int_{x-ct}^{x+ct} \psi(s) \, ds$ is a solution to the wave equation $u_{tt} - c^2 u_{xx} = 0$. Since the equation is linear, we only need to consider the case where $\phi(x) = 0$ and $\psi(x) = 0$, that is, 

$$u(x, t) = \frac{1}{2c} \iint_{\Delta} f = \frac{1}{2c} \int_0^t \int_{x - c(t - s)}^{x + c(t - s)} f(y, s) \, dy ds$$

is a solution of the given initial value problem.

$(\because)$ Substituting 

$$\begin{cases}
\xi = x + ct \\
\eta = x - ct,
\end{cases}$$

we have 

$$\begin{align*}
u_{tt} - c^2u_{xx} = -4c^2u_{\xi \eta} = f \left( \frac{\xi + \eta}{2}, \frac{\xi - \eta}{2c} \right).
\end{align*}$$

Integrating this with respect to $\eta$ and then with respect to $\xi$, we get 

$$u(\xi, \eta) = -\frac{1}{4c^2} \int^{\xi} \int^{\eta} f \, d\eta \, d \xi \quad \cdots ( \ast )$$

where the lower limits of integration here are arbitrary. (They correspond to constants of integration.) 

Fix $P_0 = (x_0, t_0)$ and let $\xi_0 = x_0 + ct_0$ and $\eta_0 = x_0 - ct_0$. We evaluate $(\ast)$ at $P_0$ and make a particular choice of the lower limits as follows: 

$$u(P_0) = -\frac{1}{4c^2} \int_{\eta_0}^{\xi_0} \int_{\xi}^{\eta_0} f \left( \frac{\xi + \eta}{2}, \frac{\xi - \eta}{2c} \right) \, d \eta \, d \xi.$$

We verify that the above choice of the lower limits leads to the given solution. Note that 

$$\begin{align*}
u(P_0) &= -\frac{1}{4c^2} \int_{\eta_0}^{\xi_0} \int_{\xi}^{\eta_0} f \left( \frac{\xi + \eta}{2}, \frac{\xi - \eta}{2c} \right) \, d \eta \, d \xi \\
&= \frac{1}{4c^2} \int_{\eta_0}^{\xi_0} \int_{\eta_0}^{\xi} f \left( \frac{\xi + \eta}{2}, \frac{\xi - \eta}{2c} \right) \, d \eta \, d \xi.
\end{align*}$$

Now, we make a change of variables back to $x$ and $t$. Since the Jacobian is 

$$\begin{align*}
J &= \left \vert \det \begin{pmatrix} 
\frac{\partial \xi}{\partial x} & \frac{\partial \xi}{\partial t} \\
\frac{\partial \eta}{\partial x} & \frac{\partial \eta}{\partial t} 
\end{pmatrix} \right \vert \\
&= \left \vert \det \begin{pmatrix} 
1 & c \\
1 & -c
\end{pmatrix} \right \vert \\
&= 2c,
\end{align*}$$

we obtain 

$$\begin{align*}
u(P_0) &= \frac{1}{4c^2} \int_{\eta_0}^{\xi_0} \int_{\eta_0}^{\xi} f \left( \frac{\xi + \eta}{2}, \frac{\xi - \eta}{2c} \right) \, d \eta \, d \xi \\
&= \frac{1}{4c^2} \iint_{\Delta} f(x, t) \cdot 2c \, dx \, dt \\
&= \frac{1}{2c} \iint_{\Delta} f,
\end{align*}$$

that is, 

$$u(x_0, t_0) = \frac{1}{2c} \int_0^{t_0} \int_{x_0 - c(t_0 - t)}^{x_0 + c(t_0 - t)} f(x, t) \, dx \, dt.$$

Thus, $u(x, t)$ is the solution of the given initial value problem. $\blacksquare$

---

증명에서는 생략했는데, 구체적으로 왜 $u(P_0)$에서 적분의 위끝과 아래끝을 저렇게 쓸 수 있는지 살펴보자. 우선 변수를 $(x, t)$에서 $(\xi, \eta)$로 변환했으므로, 주어진 영역 $\Delta$가 $(\xi, \eta)$ 좌표계에서는 어떻게 표현되는지 확인해봐야 한다. 

![alt text](assets/img/coor1.png)

![alt text](assets/img/coor2.png)

위 그림에서와 같이, $(\xi, \eta)$ 좌표계에서 삼각형의 아래 모서리는 $\eta = \xi$ 직선 위, 왼쪽 모서리는 $\eta = \eta_0$ 직선 위, 그리고 오른쪽 모서리는 $\xi = \xi_0$ 직선 위에 놓여 있다. 한편 각 꼭짓점의 좌표는 $(x, t)$ 좌표계에서 $(x_0 - c t, 0), (x_0 + c t_0, 0), (x_0, t_0)$ 이고, $\xi_0$와 $\eta_0$로 표현하면 왼쪽, 오른쪽 꼭짓점은 각각 $(\eta_0, 0), (\xi_0, 0)$이다. 이 점들의 좌표를 $(\xi, \eta)$ 좌표계로 옮겨서 표현해보면 각각 $(\eta_0, \eta_0), (\xi_0, \xi_0), (\xi_0, \eta_0)$이다. 

그러면 $(\xi, \eta)$ 좌표계에서 주어진 영역 $\Delta$의 범위를 손쉽게 표현할 수 있다. 그림에서 보이듯, 각각의 화살표는 어떤 $\xi$ 값을 고정한뒤 $\eta_0$에서부터 $\xi$까지 $\eta$에 대해 적분하는 행위를 나타낸다.

$$\int_{\eta_0}^{\xi} \cdots d \eta$$

그리고 $\xi$를 $\eta_0$에서부터 $\xi_0$까지 적분하면 주어진 삼각형 영역을 표현할 수 있는 것이다. 

$$\int_{\eta_0}^{\xi_0} \int_{\eta_0}^{\xi} \cdots d \eta \, d \xi$$