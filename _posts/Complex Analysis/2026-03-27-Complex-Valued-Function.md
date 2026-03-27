---
title: Complex Valued Function
date: 2026-03-27
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Definition

**(i)** Let $S \subset \mathbb{C}$. A function $f: S \to \mathbb{C}$ is called a ***complex valued function*** on $S$. 

**(ii)** The function that assigns more than one value to a point $z$ in the domain of the function is called a ***multi-valued function***. We usually construct a single-valued function from a multi-valued function by assigning just one of the possible values at each point is taken.

---

## Remark
Let $f$ be a complex valued function on $S$. Then $f$ can be written as $f(z) = u(x, y) + i v(x, y)$ for all $z = x + iy \in S$, where $u$ and $v$ are real valued functions on $S$. 

---

## Example

**(i)** Consider $f(z) = \frac{1}{z}, \forall z \in \mathbb{C} \setminus \{ 0 \}$. Note that 

$$\begin{align*}
f(z) &= \frac{1}{z} \\
&= \frac{\var{z}}{\vert z \vert^2} \\
&= \frac{x - iy}{x^2 + y^2} \\
&= \left( \frac{x}{x^2 + y^2} \right) + i \left( \frac{-y}{x^2 + y^2} \right).
\end{align*}$$

Hence $f = u + iv$ where 

$$u(x, y) = \frac{x}{x^2 + y^2} \quad \text{and} \quad v(x, y) = \frac{-y}{x^2 + y^2}.$$

**(ii)** Consider $f(z) = z^2, \forall z \in \mathbb{C}$. Note that 

$$\begin{align*}
f(z) &= z^2 \\
&= (x + iy)^2 \\
&= x^2 - y^2 + 2xyi \\
&= \left( x^2 - y^2 \right) + i \left( 2xy \right).
\end{align*}$$

Hence $f = u + iv$ where 

$$u(x, y) = x^2 - y^2 \quad \text{and} \quad v(x, y) = 2xy.$$

**(iii)** Consider $f(z) = z^{\frac{1}{2}}, \forall z \in \mathbb{C} \setminus \{ 0 \}$. Since $z^{\frac{1}{2}}$ has the two possible values

$$z^{\frac{1}{2}} = \pm \sqrt{r} \exp \left( i \frac{\Theta}{2} \right)$$

where $r = \vert z \vert$ and $\Theta \in (-\pi, \pi]$ is the principal value of the argument of $z$. But, if we choose only the positive value of $\pm \sqrt{r}$ and write

$$f(z) = \sqrt{r} \exp \left( i \frac{\Theta}{2} \right)$$

then $f$ is a single-valued function on $\mathbb{C} \setminus \{ 0 \}$. By assigning $f(0) = 0$, the function $f$ is well-defined on $\mathbb{C}$.