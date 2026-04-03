---
title: Limit of Complex Functions
date: 2026-04-03
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Definition

Let $f: D \to \mathbb{C}$ be a complex function defined on a domain $D \subset \mathbb{C}$. We say that $\lim_{z \to z_0} f(z) = \omega_0$ if

$$\forall \varepsilon > 0, \exists \delta > 0 \text{ such that } 0 < |z - z_0| < \delta \implies |f(z) - \omega_0| < \varepsilon.$$

---

## Theorem 1
**(i)** When a limit of a function $f(z)$ exists at a point $z_0$, it is unique. 

**(ii)** Suppose that $f(z) = u(x, y) + iv(x, y) (z = x + iy)$ and $z_0 = x_0 + iy_0, \omega_0 = u_0 + iv_0$. Then

$$\begin{gather*}
\lim_{(x, y) \to (x_0, y_0)} u(x, y) = u_0 \quad \text{and} \quad \lim_{(x, y) \to (x_0, y_0)} v(x, y) = v_0 \\
\iff \\
\lim_{z \to z_0} f(z) = \omega_0.
\end{gather*}
$$

### Proof
(ii) 

$(\Longrightarrow)$

Let $\varepsilon > 0$. Since $u(x, y) \to u_0$ and $v(x, y) \to v_0$ as $(x, y) \to (x_0, y_0)$, there exist $\delta_1 > 0$ and $\delta_2 > 0$ such that

$$\begin{gather*}
0 < \sqrt{(x - x_0)^2 + (y - y_0)^2} < \delta_1 \implies \vert u(x, y) - u_0\vert < \frac{\varepsilon}{2} \\
0 < \sqrt{(x - x_0)^2 + (y - y_0)^2} < \delta_2 \implies \vert v(x, y) - v_0\vert < \frac{\varepsilon}{2}.
\end{gather*}$$

Take $\delta = \min \\{ \delta_1, \delta_2 \\}$. Note that

$$\vert z - z_0 \vert = \sqrt{(x - x_0)^2 + (y - y_0)^2}.$$

For $z \in N_{\delta}(z_0) \setminus \{ z_0 \}$, we have

$$\begin{align*}
\vert f(z) - \omega_0 \vert &= \vert u(x, y) - u_0 + i(v(x, y) - v_0) \vert \\
&\le \vert u(x, y) - u_0 \vert + \vert v(x, y) - v_0 \vert \\
&\le \frac{\varepsilon}{2} + \frac{\varepsilon}{2} = \varepsilon,
\end{align*}$$

so that $\lim_{z \to z_0} f(z) = \omega_0$.

($\Longleftarrow$)

Let $\varepsilon > 0$. Since $\lim_{z \to z_0} f(z) = \omega_0$, there exists $\delta > 0$ such that

$$0 < \vert z - z_0 \vert < \delta \implies \vert f(z) - \omega_0 \vert < \varepsilon.$$

For $(x, y)$ such that $0 < \sqrt{(x - x_0)^2 + (y - y_0)^2} < \delta$, we have

$$\vert u(x, y) - u_0 \vert \le \vert f(z) - \omega_0 \vert < \varepsilon.$$

Thus, $\lim_{(x, y) \to (x_0, y_0)} u(x, y) = u_0$. Similarly, we can show that $\lim_{(x, y) \to (x_0, y_0)} v(x, y) = v_0$. $\blacksquare$