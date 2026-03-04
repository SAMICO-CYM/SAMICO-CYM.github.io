--- 
title: The Derivative
date: 2026-02-21 15:00:00 +0900
categories: [Mathematics, Vector Calculus]
tags: []
math: true
---

## Directional Derivative
Let $A \subset \mathbb{R}^m$ be open, and let $\mathbf{f} : A \to \mathbb{R}^n$. Given $\mathbf{u} \in \mathbb{R}^m$ with $\mathbf{u} \neq 0$, define 

$$\mathbf{f}'(\mathbf{a}; \mathbf{u}) = \lim_{t \to 0} \frac{ \mathbf{f}(\mathbf{a} + t\mathbf{u}) - \mathbf{f}(\mathbf{a})}{t},$$

provided the limit exists. We call this limit the ***directional derivative*** of $\mathbf{f}$ at $\mathbf{a}$ with respect to the vector $\mathbf{u}$. 

## Definition 1
Let $E \subset \mathbb{R}^n$ be open, and let $\mathbf{f} : E \to \mathbb{R}^m$. We say that $\mathbf{f}$ is ***differentiable*** at $\mathbf{x}$ if $\exists \mathsf{T} \in \mathcal{L}(\mathbb{R}^n, \mathbb{R}^m)$ such that 

$$ \lim_{\mathbf{h} \to \mathbf{0}} \frac{ \| \mathbf{f}(\mathbf{x}+\mathbf{h}) - \mathbf{f}(\mathbf{x}) - \mathsf{T}(\mathbf{h}) \|}{\|\mathbf{h}\|} = \mathbf{0},$$

and we write $\mathbf{f}'(\mathbf{x}) = \mathsf{T}$. If $\mathbf{f}$ is differentiable at every $\mathbf{x} \in E$, then we say that $\mathbf{f}$ is differentiable in $E$. 

벡터 $\mathbf{h}$의 크기 $\| \mathbf{h}\|$가 충분히 작다면 $E$는 open이므로 $\mathbf{x} + \mathbf{h} \in E$라고 할 수 있고, 따라서 $\mathbf{f}(\mathbf{x} + \mathbf{h})$는 잘 정의된다. 
\
표기법에 주의하자. $\mathbf{f}'(\mathbf{x})$는 $\mathbb{R}^m$에 속하는 어떤 벡터가 아니라 그 자체로 선형 변환이다.

---

## Theorem 1
Let $E \subset \mathbb{R}^n$ be open, and let $\mathbf{f} : E \to \mathbb{R}^m$. Suppose that $\mathbf{f}$ is differentiable at $\mathbf{x}$ with $\mathsf{T} = \mathsf{T}_1$ and with $\mathsf{T} = \mathsf{T}_2$. Then $\mathsf{T}_1 = \mathsf{T}_2$.

### Proof
Let $\mathsf{U} = \mathsf{T}_2 - \mathsf{T}_1$. Then 

$$\begin{gather*} & \| \mathsf{U}(\mathbf{h}) \| \le |\mathbf{f}(\mathbf{x} + \mathbf{h}) - \mathbf{f}(\mathbf{x}) - \mathsf{T}_1(\mathbf{h})| + |\mathbf{f}(\mathbf{x} + \mathbf{h}) - \mathbf{f}(\mathbf{x}) - \mathsf{T}_2(\mathbf{h})| \\ \implies & 0 \le \lim_{\mathbf{h} \to \mathbf{0}} \frac{\|\mathsf{U}(\mathbf{h})\|}{\|\mathbf{h}\|} \le \lim_{\mathbf{h} \to \mathbf{0}} \frac{|\mathbf{f}(\mathbf{x} + \mathbf{h}) - \mathbf{f}(\mathbf{x}) - \mathsf{T}_1(\mathbf{h}|)}{\|\mathbf{h}\|} \\ &+ \lim_{\mathbf{h} \to \mathbf{0}} \frac{|\mathbf{f}(\mathbf{x} + \mathbf{h}) - \mathbf{f}(\mathbf{x}) - \mathsf{T}_2(\mathbf{h})|}{\|\mathbf{h}\|} = 0 \\ \implies & \lim_{\mathbf{h} \to \mathbf{0}} \frac{\|\mathsf{U}(\mathbf{h})\|}{\|\mathbf{h}\|} = 0 \end{gather*}$$

Let $\mathbf{a} = t \mathbf{h}$ for fixed $\mathbf{h} \neq \mathbf{0}$. Then we have 

$$\begin{gather*} & \lim_{\mathbf{a} \to \mathbf{0}} \frac{\|\mathsf{U}(\mathbf{a})\|}{\|\mathbf{a}\|} = \lim_{t \to 0} \frac{\|\mathsf{U}(t\mathbf{h})\|}{\|t\mathbf{h}\|} \\ &= \lim_{t \to 0} \frac{\|\mathsf{U}(\mathbf{h})\|}{\|\mathbf{h}\|} = \frac{\|\mathsf{U}(\mathbf{h})\|}{\|\mathbf{h}\|} = 0 \\ \implies &\mathsf{U}(\mathbf{h}) = \mathbf{0}, \forall \mathbf{h} \in \mathbb{R}^n \\ \implies &\mathsf{T_1} = \mathsf{T}_2. \blacksquare \end{gather*}$$

---

## Remark
- Let $E \subset \mathbb{R}^n$ be open, and let $\mathbf{f} : E \to \mathbb{R}^m$. If $\mathbf{f}$ is differentiable in $E$, then $\mathbf{f}$ is continuous in $E$. 
- If $\mathsf{T} \in \mathcal{L}(\mathbb{R}^n, \mathbb{R}^m)$ and if $\mathbf{x} \in \mathbb{R}^n$, then $\mathsf{T}'(\mathbf{x}) = \mathsf{T}$.  

---
## Theorem 2
Let $E \subset \mathbb{R}^n$ be open, and let $\mathbf{f} : E \to \mathbb{R}^m$. Suppose that $\mathbf{f}$ is differentiable at $\mathbf{x}_0 \in E$, $\mathbf{g}$ maps an open set containing $\mathbf{f}(E)$ into $\mathbb{R}^k$, and $\mathbf{g}$ is differentiable at $\mathbf{f}(\mathbf{x}_0)$. Then the mapping $\mathbf{F} : E \to \mathbb{R}^k$ defined by 

$$ \mathbf{F}(\mathbf{x}) = \mathbf{g}(\mathbf{f}(\mathbf{x})) $$

is differentiable at $\mathbf{x}_0$, and 

$$ \mathbf{F}'(\mathbf{x}_0) = \mathbf{g}'(\mathbf{f}(\mathbf{x}_0))\mathbf{f}'(\mathbf{x}_0). $$

### Proof
$\blacksquare$

---

## Definition 2
Let $E \subset \mathbb{R}^n$ be open, and let $\mathbf{f} : E \to \mathbb{R}^m$. Denote the components of $\mathbf{f}$ by $\mathbf{f} = (f_1, ..., f_m)$. Let $\\{\mathbf{e}_1, \dots, \mathbf{e}_n\\}$ and $\\{\mathbf{u}_1, \dots, \mathbf{u}_m\\}$ be the standard ordered bases of $\mathbb{R}^n$ and $\mathbb{R}^m$, respectively. 
For $\mathbf{x} \in E$, $1 \le i \le m$, $1 \le j \le n$, we define 

$$(D_j f_i)(\mathbf{x}) = \lim_{t \to 0} \frac{f_i(\mathbf{x} + t\mathbf{e}_j) - f_i(\mathbf{x})}{t},$$

provided the limit exists. The notation 

$$\frac{\partial f_i}{\partial x_j}$$

is often used in place of $D_j f_i$, and $D_j f_i$ is called a ***partial derivative***.

## Theorem 3
Let $E \subset \mathbb{R}^n$ be open, and let $\mathbf{f} : E \to \mathbb{R}^m$. Suppose that $\mathbf{f}$ is differentiable at a point $\mathbf{x} \in E$. Then the partial derivatives $(D_j f_i)(\mathbf{x})$ exist, and 

$$\mathbf{f}'(\mathbf{x})\mathbf{e}_j = \sum_{i=1}^m (D_j f_i)(\mathbf{x})\mathbf{u}_i \quad (1 \le j \le n),$$

where $\\{\mathbf{e}_1, \dots, \mathbf{e}_n\\}$ and $\\{\mathbf{u}_1, \dots, \mathbf{u}_m\\}$ are the standard ordered bases of $\mathbb{R}^n$ and $\mathbb{R}^m$, respectively. 

### Proof 
$\blacksquare$

## Remark
다음과 같이 행렬 $J$를 정의하자.

$$J = \begin{bmatrix}
(D_1f_1)(\mathbf{x}) & \cdots & (D_nf_1)(\mathbf{x}) \\
\vdots & \ddots & \vdots \\
(D_1f_m)(\mathbf{x}) & \cdots & (D_nf_m)(\mathbf{x})
\end{bmatrix}$$

위 정리에 의해 $\mathbf{f}'(\mathbf{x})$는 위 행렬 $J$로 정의되는 선형 변환, 즉 $\mathbf{f}'(\mathbf{x})\mathbf{a} = J \mathbf{a}$임을 알 수 있다. 따라서 $\mathbf{f}'(\mathbf{x})$의 행렬 표현은 $\left[ \mathbf{f}'(\mathbf{x}) \right] = J$이고, 이를 $\mathbf{f}$의 ***Jacobian***이라고 부른다. 