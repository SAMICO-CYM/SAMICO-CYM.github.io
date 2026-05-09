--- 
title: Nested Interval Theorem
date: 2026-05-09
categories: [Mathematics, Real-Analysis]
tags: []
math: true
---

## Definition
A sequence of sets $\{ I_n \}_{n=1}^\infty$ is said to be **nested** if $I_n \supset I_{n+1}, \forall n \in \mathbb{N}$.

---
## Nested Interval Theorem
If $\{ [a_n, b_n] \}_{n=1}^\infty$ is a nested sequence of intervals, then

**(i)** $\displaystyle \bigcap_{n=1}^\infty [a_n, b_n] \neq \emptyset$.   

**(ii)** If $\displaystyle \lim_{n \to \infty} (b_n - a_n) = 0$, then $\displaystyle \bigcap_{n=1}^\infty [a_n, b_n]$ is a singleton.

### Proof
**(i)** Since $\{ a_n \}$ is increasing and bounded, and $\{ b_n \}$ is decreasing and bounded, $a_n \uparrow a$ and $b_n \downarrow b$ for some $a, b \in \mathbb{R}$. Since $a_n \le a \le b \le b_n, \forall n \in \mathbb{N}$, we have $$x \in [a, b] \iff x \in [a_n, b_n], \forall n \in \mathbb{N} \iff x \in \bigcap_{n=1}^\infty [a_n, b_n].$$ Thus $\displaystyle \bigcap_{n=1}^\infty [a_n, b_n] \neq \emptyset.$

**(ii)** Suppose that $\displaystyle \lim_{n \to \infty} (b_n - a_n) = 0$. Since $0 \le b - a \le b_n - a_n, \forall n \in \mathbb{N}$, we have $\displaystyle \lim_{n \to \infty} (b - a) = 0$, which implies that $a = b$, and $\displaystyle \bigcap_{n=1}^\infty [a_n, b_n]$ is a singleton. $\blacksquare$