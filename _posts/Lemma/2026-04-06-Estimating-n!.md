---
title: Estimating $n!$
date: 2026-04-06
categories: [Mathematics, Combinatorics]
tags: []
math: true
---

## Theorem
For any $n \in \mathbb{N}$, we have

**(i)** $\displaystyle 2^{n-1} \le n! \le n^n$ (That is, $n! = O(n^n)$)

**(ii)** $\displaystyle \left( \frac{\sqrt{n}}{\sqrt{2}} \right)^n \le n! \le \left( \frac{n}{\sqrt{2}} \right)^n$ 

**(iii)** $\displaystyle (\sqrt{n})^n \le n! \le \left( \frac{n+1}{2} \right)^n$ 

**(iv)** $\displaystyle e\left( \frac{n}{e} \right)^n \le n! \le ne\left( \frac{n}{e} \right)^n$ 

### Proof

**(i)** Note that

$$\begin{align*}
n! &= n(n-1) \cdots 2 \cdot 1 \\
&\ge 2 \cdot 2 \cdots 2 \cdot 1 \\
&\ge 2^{n-1}
\end{align*}$$

and

$$
\begin{align*}
n! &= n(n-1) \cdots 2 \cdot 1 \\
&\le n \cdot n \cdots n \cdot n \\
&\le n^n
\end{align*}$$

Thus we have 

$$
\begin{align*}
2^{n-1} \le n! \le n^n.
\end{align*}
$$

**(iv)** 

We use the induction on $n$. If $n = 1$, then clearly the inequality holds. Assume that 

$$
\begin{align*}
(n-1)! \le (n-1)e \left( \frac{n-1}{e} \right)^{n-1}.
\end{align*}
$$

Then we have

$$\begin{align*}
n! = n (n-1)! \le n(n-1)e \left( \frac{n-1}{e} \right)^{n-1} &= ne^2 \left( \frac{n-1}{e} \right)^{n} \\
&= n \left( \frac{n}{e} \right)^n \left( \frac{n-1}{n} \right)^n e^2 \\
& \le n e \left( \frac{n}{e} \right)^n
\end{align*}$$

The last inequality holds since $\left( \frac{n-1}{n} \right)^n < \frac{1}{e}$ for all $n \ge 1$.

$(\because)$ 

$$\begin{align*}
1+x \le 1+ x + \frac{x^2}{2!} + \cdots = e^x & \implies 1+ \frac{x}{n} \le e^{\frac{x}{n}} \\
& \implies \left( 1+ \frac{x}{n} \right)^n \le e^x \\
& \implies \left( 1- \frac{1}{n} \right)^n \le e^{-1} = \frac{1}{e}.
\end{align*}$$

$\blacksquare$