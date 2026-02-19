---
title: Dynamical System
date: 2026-02-19 15:00:00 +0900
categories:
  - Mathematics
  - Dynamics
tags: []
math: true
---
## Definition 1
1. ***A dynamical system*** consists of a set of possible states, together with a rule that determines the present state in terms of past states.

---
## Definition 2
1. A function $f: X \to X$ whose domain and range are the same is called a ***map***. 
2. Let $x$ be a point and let $f$ be a map. ***The orbit of $x$ under $f$*** is the set of points $\{x, f(x), f^2(x), ... \}$. The starting point $x$ for the orbit is called the ***initial value*** of the orbit. 
3. A point $p$ is a ***fixed point*** of the map $f$ if $f(p)=p$.

---

## Definition 3
Let $f$ be a map on $\mathbb{R}$ and let $p$ be a fixed point of the map $f$. 
1. The point $p$ is called a ***sink*** or an ***attracting fixed point*** if $\exists \varepsilon > 0$ such that $$\lim_{k \to \infty} f^k(x) = p, \forall x \in N_\varepsilon(p).$$ 
2. The point $p$ is called a ***source*** or a ***repelling fixed point*** if $\exists \varepsilon > 0$ such that for each $x \in N_{\varepsilon}(p)$ except for $p$, $\exists N \in \mathbb{N}$ such that $f^N(x) \notin N_\varepsilon(p).$ 

---

## Theorem
Lef $f \in C^\infty$ be a map on $\mathbb{R}$, and let $p$ be a fixed point of $f$. Then
- If $$|f'(p)| < 1$$, then $p$ is a sink. 
- If $|f'(p)| > 1$, then $p$ is a source.
### Proof
1. Suppose that $|f'(p)| < 1$. Let $a \in (|f'(p)|, 1)$. Since 
\
$$\lim_{x \to p} \frac{|f(x) - f(p)|}{|x-p|} = |f'(p)|,$$ \
$\exists \varepsilon > 0$ such that $\forall x \in N_\varepsilon(p)$, we have 
\
$$\begin{gather*} & \frac{|f(x) - f(p)|}{|x - p|} - |f'(p)| < a - |f'(p)| \\ \Longrightarrow &\frac{|f(x) - f(p)|}{|x - p|} < a \\ \Longrightarrow &|f(x) - p| = |f(x) - f(p)| < a |x-p| < \varepsilon \\ \Longrightarrow &f(x) \in N_\varepsilon(p), \end{gather*}$$
\
so that $f^k(x) \in N_\varepsilon(p), \forall k \in \mathbb{N}.$ 
\
Furthermore, we have 
\
$$|f^k(x) - p| \le a^k|x-p|, \forall k \in \mathbb{N}.$$ \
$(\because)$ 

### Theorem
Let $$f \in C^\infty$$ be a map on $$\mathbb{R}$$, and let $$p$$ be a fixed point of $$f$$. Then
- (i) If \$$|f'(p)| < 1$$, then \$$p$$ is a sink.
- (ii) If \$$|f'(p)| > 1$$, then \$$p$$ is a source.

### Proof
- (i) Suppose that \$$|f'(p)| < 1$$. Let \$$a \in (|f'(p)|, 1)$$. Since 

$$
\lim_{x \to p} \frac{|f(x) - f(p)|}{|x - p|} = |f'(p)|,
$$

\$$\exists \varepsilon > 0$$ such that $$\forall x \in N_\varepsilon(p)$$, we have

$$
\begin{align}
\frac{|f(x) - f(p)|}{|x - p|} - |f'(p)| &< a - |f'(p)| \\
\implies \frac{|f(x) - f(p)|}{|x - p|} &< a \\
\implies |f(x) - p| = |f(x) - f(p)| &< a|x - p| < \varepsilon \\
\implies f(x) &\in N_\varepsilon(p)
\end{align}
$$

so that $$f^k(x) \in N_\varepsilon(p), \forall k \in \mathbb{N}$$. Furthermore, we have $$|f^k(x) - p| \le a^k|x - p|, \forall k \in \mathbb{N}$$.