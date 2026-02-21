--- 
title: ## Generalized Eigenvector
date: 2026-02-21 15:00:00 +0900
categories: [Mathematics, Matrix Algebra]
tags: []
math: true
---

## Generalized Eigenvector
- Let $A \in M_{n \times n}(\mathbb{C})$. A vector $x \neq 0 \in \mathbb{C}^n$ is called a ***generalized eigenvector*** of $A$ of order $k$ belonging to an eigenvalue $\lambda$ of $A$ if 

$$ (A-\lambda I)^k x = \mathbf{0} \quad \text{but} \quad (A-\lambda I)^{k-1} x \neq \mathbf{0}. $$

## Remark
If $x_k$ is a generalized eigenvector of $A$ of order $k$ belonging to $\lambda$, then 

$$ \begin{align*} x_{k-1} = (A&-\lambda I)x_k, \\ x_{k-2} = (A&-\lambda I)x_{k-1} \\ &\vdots \\ x_1 = (A&-\lambda I)^{k-1}x_k. \end{align*} $$

Following this process, we can determine the invertible matrix $Q$ such that $J = Q^{-1}AQ$.

## Chain of Generalized Eigenvectors
- In the above remark, we call the set $\\{x_1,\ldots,x_k\\}$ a ***chain of generalized eigenvectors*** of $A$ belonging to $\lambda$.

---

## Theorem
Let $\\{x_1,\ldots,x_k\\}$ and $\\{u_1,\ldots,u_\ell \\}$ be chains of generalized eigenvectors of $A$ belonging to $\lambda$ and $\mu$, respectively. 
- If $\lambda \neq \mu$, then $\\{x_1,\ldots,x_k,u_1,\ldots,u_\ell \\}$ is linearly independent.  
- If $\lambda = \mu$ and $\\{x_1,u_1 \\}$ is linearly independent, then $\\{x_1,\ldots,x_k,u_1,\ldots,u_\ell \\}$ is linearly independent.