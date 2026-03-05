--- 
title: Norm of Linear Transformation
date: 2026-03-05
categories: [Mathematics, Lienar Algebra]
tags: []
math: true
---

## Definition
Let $\mathsf{T} \in \mathcal{L}(\mathbb{R}^n, \mathbb{R}^m)$. The norm $\| \mathsf{T} \|$ of $\mathsf{T}$ is defined by 

$$\|\mathsf{T}\| = \sup_{\|x\| = 1} \|\mathsf{T}(\mathbf{x})\|.$$

## Remark
(i) The following three definitions are equivalent:

$$\begin{align*}
\|\mathsf{T}\| &= \sup_{\|x\| = 1} \|\mathsf{T}(\mathbf{x})\| \\
&= \sup_{\|x\| \le 1} \|\mathsf{T}(\mathbf{x})\| \\
&= \sup_{\|x\| \neq \mathbf{0}} \frac{\|\mathsf{T}(\mathbf{x})\|}{\|\mathbf{x}\|}
\end{align*}$$

(ii) By the third definition of the norm, we have the inequality

$$\|\mathsf{T}(\mathbf{x})\| \le \|\mathsf{T}\| \|\mathbf{x}\|, \forall \mathbf{x} \in \mathbb{R}^n.$$

## Theorem 1
(i) If $\mathsf{T} \in \mathcal{L}(\mathbb{R}^n, \mathbb{R}^m)$, then $\| \mathsf{T} \| < \infty$ and $\mathsf{T}$ is a uniformly continuous mapping of $\mathbb{R}^n$ into $\mathbb{R}^m$. 

(ii) If $\mathsf{T}, \mathsf{U} \in \mathcal{L}(\mathbb{R}^n, \mathbb{R}^m)$ and $c \in \mathbb{R}$, then 

$$\| \mathsf{T} + \mathsf{U} \| \le \| \mathsf{T} \| + \| \mathsf{U} \| \quad \text{and} \quad \| c \mathsf{T} \| = |c| \| \mathsf{T} \|.$$

(iii) If $\mathsf{T} \in \mathcal{L}(\mathbb{R}^n, \mathbb{R}^m)$ and $\mathsf{U} \in \mathcal{L}(\mathbb{R}^m, \mathbb{R}^k)$, then 

$$\| \mathsf{U} \mathsf{T} \| \le \| \mathsf{U} \| \|\mathsf{T}\|.$$

### Proof
$\blacksquare$
