--- 
title: The Derivative
date: 2026-02-21 15:00:00 +0900
categories: [Mathematics, Vector Calculus]
tags: []
math: true
---

## Directional Derivative
- Let $A \subset \mathbb{R}^m$ be open, and let $\mathbf{f} : A \to \mathbb{R}^n$. Given $\mathbf{u} \in \mathbb{R}^m$ with $\mathbf{u} \neq 0$, define 

$$\mathbf{f}'(\mathbf{a}; \mathbf{u}) = \lim_{t \to 0} \frac{ \mathbf{f}(\mathbf{a} + t\mathbf{u}) - \mathbf{f}(\mathbf{a})}{t},$$

provided the limit exists. We call this limit the ***directional derivative*** of $\mathbf{f}$ at $\mathbf{a}$ with respect to the vector $\mathbf{u}$. 

## Differentiable
- Let $E \subset \mathbb{R}^m$ be open, and let $\mathbf{f} : E \to \mathbb{R}^n$.We say that $\mathbf{f}$ is ***differentiable*** at $\mathbf{x}$ if $\exists \mathsf{T} \in \mathcal{L}(\mathbb{R}^m, \mathbb{R}^n)$ such that 

$$ \lim_{\mathbf{h} \to \mathbf{0}} \frac{ \| \mathbf{f}(\mathbf{x}+\mathbf{h}) - \mathbf{f}(\mathbf{x}) - \mathsf{T}(\mathbf{h}) \|}{\|\mathbf{h}\|} = \mathbf{0},$$

and we write $\mathbf{f}'(\mathbf{x}) = \mathsf{T}$. If $\mathbf{f}$ is differentiable at every $\mathbf{x} \in E$, then we say that $\mathbf{f}$ is differentiable in $E$. 

벡터 $\mathbf{h}$의 크기 $\| \mathbf{h}\|$가 충분히 작다면 $E$는 open이므로 $\mathbf{x} + \mathbf{h} \in E$라고 할 수 있고, 따라서 $\mathbf{f}(\mathbf{x} + \mathbf{h})$는 잘 정의된다. 

---

## Theorem 1
- Let $E \subset \mathbb{R}^n$ be open, and let $\mathbf{f} : E \to \mathbb{R}^m$. Suppose that $\mathbf{f}$ is differentiable at $\mathbf{x}$ with $\mathsf{T} = \mathsf{T}_1$ and with $\mathsf{T} = \mathsf{T}_2$. Then $\mathsf{T}_1 = \mathsf{T}_2$.

### Proof
Let $\mathsf{U} = \mathsf{T}_2 - \mathsf{T}_1$. Then 

$$\begin{gather*} & \| \mathsf{U}(\mathbf{h}) \| \le |\mathbf{f}(\mathbf{x} + \mathbf{h}) - \mathbf{f}(\mathbf{x}) - \mathsf{T}_1(\mathbf{h})| + |\mathbf{f}(\mathbf{x} + \mathbf{h}) - \mathbf{f}(\mathbf{x}) - \mathsf{T}_2(\mathbf{h})| \\ \implies & 0 \le \lim_{\mathbf{h} \to \mathbf{0}} \frac{\|\mathsf{U}(\mathbf{h})\|}{\|\mathbf{h}\|} \le \lim_{\mathbf{h} \to \mathbf{0}} \frac{|\mathbf{f}(\mathbf{x} + \mathbf{h}) - \mathbf{f}(\mathbf{x}) - \mathsf{T}_1(\mathbf{h}|)}{\|\mathbf{h}\|} \\ &+ \lim_{\mathbf{h} \to \mathbf{0}} \frac{|\mathbf{f}(\mathbf{x} + \mathbf{h}) - \mathbf{f}(\mathbf{x}) - \mathsf{T}_2(\mathbf{h})|}{\|\mathbf{h}\|} = 0 \\ \implies & \lim_{\mathbf{h} \to \mathbf{0}} \frac{\|\mathsf{U}(\mathbf{h})\|}{\|\mathbf{h}\|} = 0 \end{gather*}$$

Let $\mathbf{a} = t \mathbf{h}$ for fixed $\mathbf{h} \neq \mathbf{0}$. Then we have 

$$\begin{gather*} & \lim_{\mathbf{a} \to \mathbf{0}} \frac{\|\mathsf{U}(\mathbf{a})\|}{\|\mathbf{a}\|} = \lim_{t \to 0} \frac{\|\mathsf{U}(t\mathbf{h})\|}{\|t\mathbf{h}\|} \\ &= \lim_{t \to 0} \frac{\|\mathsf{U}(\mathbf{h})\|}{\|\mathbf{h}\|} = \frac{\|\mathsf{U}(\mathbf{h})\|}{\|\mathbf{h}\|} = 0 \\ \implies &\mathsf{U}(\mathbf{h}) = \mathbf{0}, \forall \mathbf{h} \in \mathbb{R}^n \\ \implies &\mathsf{T_1} = \mathsf{T}_2. \blacksquare \end{gather*}$$

---

## Theorem 2
- Let $E \subset \mathbb{R}^n$ be open, and let $\mathbf{f} : E \to \mathbb{R}^m$. Suppose that $\mathbf{f}$ is differentiable at $\mathbf{x}_0 \in E$, $\mathbf{g}$ maps an open set containing $\mathbf{f}(E)$ into $\mathbb{R}^k$, and $\mathbf{g}$ is differentiable at $\mathbf{f}(\mathbf{x}_0)$. Then the mapping $\mathbf{F} : E \to \mathbb{R}^k$ defined by 

$$ \mathbf{F}(\mathbf{x}) = \mathbf{g}(\mathbf{f}(\mathbf{x})) $$

is differentiable at $\mathbf{x}_0$, and 

$$ \mathbf{F}'(\mathbf{x}_0) = \mathbf{g}'(\mathbf{f}(\mathbf{x}_0))\mathbf{f}'(\mathbf{x}_0). $$

### Proof

---

