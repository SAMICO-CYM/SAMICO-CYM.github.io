--- 
title: Laplace Equation in Rectangle and Cube
date: 2026-06-11
categories: [Mathematics, PDE]
tags: []
math: true
---

## Rectangle
Let $D = \\{ 0 < x < a, 0 < y < b \\}$ be the rectangle. We consider the problem $\Delta u = u_{xx} + u_{yy} = 0$ in $D$ with the boundary condition

![](assets/img/Pasted%20image%2020260611192305.png)

If we call the solution $u$ with data $(g, h, j, k)$, then $u = u_1 + u_2 + u_3 + u_4$ where $u_1$ has data $(g, 0, 0, 0),$ $u_2$ has data $(0, h, 0, 0),$ and so on. 

Let consider only $u = u_1.$ In this case, we have

![](assets/img/Pasted%20image%2020260611192542.png)

We separate variables $u(x, y) = X(x)Y(y).$ Then we get 

$$\begin{gather*}
0 = \Delta u =  u_{xx} + u_{yy} = X''Y + XY'' \\
\implies \frac{X''}{X} = -\frac{Y''}{Y} = - \lambda \\
\implies \begin{cases}
X'' + \lambda X = 0, & 0<x<a \\
Y'' - \lambda Y = 0, & 0 < y < b
\end{cases}
\end{gather*}$$

for a constant $\lambda.$

Furthermore, we get the boundary conditions $X(0) = 0 = X'(a)$ and $Y'(0) + Y(0) = 0$ from $u = 0, u_x = 0$ and $u_y + u = 0.$ 

Solving 

$$\begin{cases}
X'' + \lambda X = 0, & 0 < x < a \\
X(0) = 0 = X'(a),
\end{cases}$$

we obtain 

$$\beta^2_n = \lambda_n = \left( n+\frac{1}{2} \right)^2 \frac{\pi^2}{a^2}$$

for $n = 0, 1, 2, \cdots,$ so 

$$X_n = \sin \beta_n x = \sin \frac{\left( n + \frac{1}{2} \right)\pi x}{a}$$

for each $n.$ Note that we can only get the nontrivial solution in the case $\lambda = \lambda_n > 0.$

Next, solving $Y'' - \lambda Y = 0$ for $0 < y < b,$ we obtain

$$Y_n(y) = A \cosh \beta_n y + B \sinh \beta_n y$$

for each $n.$ From $Y'(0) + Y(0) = 0,$ we get $B \beta_n + A = 0.$ Putting $B = -1,$ we have $A = \beta_n,$ so 

$$Y_n(y) = \beta_n \cosh \beta_n y - \sinh \beta_n y.$$

Summing all eigenfunctions, we get 

$$u_1(x, y) = \sum_{n=0}^\infty A_nX_n(x)Y_n(y) = \sum_{n=0}^\infty A_n \sin \beta_n x (\beta_n \cosh \beta_n y - \sinh \beta_n y).$$

To satisfy the remaining boundary condition $u(x, b) = g(x),$ it requires that 

$$g(x) = u(x, b) = \sum_{n=0}^\infty A_n(\beta_n \cosh \beta_n b - \sinh \beta_n b) \sin \beta_n x$$

for $0 < x < a.$ This is simply a Fourier sine series, so 

$$\begin{gather*}
A_n(\beta_n \cosh \beta_n b - \sinh \beta_n b) = \frac{2}{a} \int_0^a g(x) \sin \beta_n x \, dx \\
\implies A_n = \frac{1}{\beta_n \cosh \beta_n b - \sinh \beta_n b} \cdot \frac{2}{a} \int_0^a g(x) \sin \beta_n x \, dx.
\end{gather*}$$

---
## Cube
Let $D = \\{ 0 < x < \pi, 0 < y < \pi, 0 < z < \pi \\}$ be the cube. We consider the Dirichlet problem in $D$

$$\begin{cases}
\Delta u = 0 & \text{in } D \\
u(\pi, y, z) = g(y, z) \\
u(0, y, z) = u(x, 0, z) = u(x, y, 0) = u(x, \pi, z) = u(x, y, \pi) = 0.
\end{cases}$$

We separate variables $u(x, y, z) = X(x)Y(y)Z(z).$ Then we get

$$\begin{gather*}
0 = \Delta u = u_{xx} + u_{yy} + u_{zz} = X''YZ + XY''Z + XYZ'' \\
\implies \frac{X''}{X} + \frac{Y''}{Y} + \frac{Z''}{Z} = 0.
\end{gather*}$$

Furthermore, we get the boundary conditions 

$$X(0) = Y(0) = Z(0) = Y(\pi) = Z(\pi) = 0.$$

Since each term

$$\frac{X''}{X}, \frac{Y''}{Y}, \frac{Z''}{Z}$$

must be a constant and satisfy the boundary conditions, we can find

$$Y_m(y) = \sin my \quad \text{and} \quad Z_n(z) = \sin n z$$

for each $m,n = 1, 2, \cdots,$ so that 

$$X'' = (m^2 + n^2)X, \quad X(0) = 0.$$

Therefore, we have 

$$X_{mn}(x) = A_{mn} \sinh(\sqrt{m^2 + n^2}x).$$

Summing up, we obtain

$$u(x, y, z) = \sum_{n=1}^\infty \sum_{m=1}^\infty A_{mn} \sinh(\sqrt{m^2 + n^2}x) \sin my \, \sin nz.$$

By the boundary condition $u(\pi, y, z) = g(y, z),$ it becomes

$$g(y, z) = u(\pi, y, z) = \sum_{n=1}^\infty \sum_{m=1}^\infty A_{mn} \sinh(\sqrt{m^2 + n^2}\pi) \sin my \, \sin nz.$$

This is a double Fourier sine series in the variables $y$ and $z.$

Note that the eigenfunctions $\\{ \sin my \sin nz \\}$ are mutually orthogonal on the square $\\{ 0 < y < \pi, 0 < z < \pi \\}.$ Their normalizing constants are 

$$\int_0^\pi \int_0^\pi (\sin my \sin nz)^2 dy dz = \frac{\pi^2}{2}.$$

Thus,

$$A_{mn} = \frac{4}{\pi^2 \sinh(\sqrt{m^2 + n^2} \pi)} \int_0^\pi \int_0^\pi g(y, z) (\sin my \sin nz)^2 dy dz.$$