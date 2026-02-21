--- 
title: Jordan Canonical Form
date: 2026-02-21 15:00:00 +0900
categories: [Mathematics, Matrix Algebra]
tags: []
math: true
---

## Jordan Block
- A matrix of the type of 

$$J = \begin{bmatrix}  
\lambda & 1 & & \mathbf{0} \\   
& \ddots & \ddots & \\  
&  & \ddots & 1 \\  
\mathbf{0} & & & \lambda  
\end{bmatrix}$$

is called a ***Jordan block*** belonging to $\lambda$.

## Jordan Canonical Form
- Every square matrix $A$ is similar to the ***Jordan canonical form*** $J$ of $A$: 

$$J = \begin{bmatrix} J_1 & & & \mathbf{0} \\ & J_2 & & \\ & & \ddots & \\ \mathbf{0} & & & J_s  
\end{bmatrix}$$

where $s$ is the number of linearly independent eigenvectors of $A$ and each $J_i$ is a Jordan block.
\
대각화 가능한 행렬은 여러 가지 좋은 성질을 가지는데, 그 중 하나는 행렬의 거듭제곱을 간편하게 계산할 수 있다는 것이다. 행렬의 곱셈 연산이 꽤나 많은 연산량을 수반한다는 점에서 거듭제곱이 간편하다는 건 아주 좋은 성질이다. 그러나 모든 정사각행렬이 대각화 가능하지는 않다. 이런 상황에서 거듭제곱을 보다 더 적은 연산으로 수행할 수 있는 방법은 없을까? 모든 정사각행렬이 대각행렬과 닮을 수는 없지만, Jordan canonical form이라고 불리는 특수한 형태의 행렬과는 항상 닮아있다는 점이 보장되어 있다. JCF의 꼴을 살펴본다면 당연하게도 대각행렬은 JCF의 특수한 경우라고도 이해할 수 있다.

---

## Remark
- A diagonal matrix is a special case of a JCF.  
- Any two JCFs of $A$ cannot be similar except for the case of permuting the Jordan blocks.  
- A matrix $A$ and its JCF $J$ have the same eigenvalues with the same multiplicities and the same number of linearly independent eigenvectors.  
- $\operatorname{rank}(A-\lambda I)^k = \operatorname{rank}(J-\lambda I)^k, \forall k \in \mathbb{N}$ for any eigenvalue $\lambda$. Hence Hence $J$ is completely determined by the sequence $\{\operatorname{rank}(A-\lambda I)^k\}_{k=0}^\infty$ for each $\lambda$.  
- If $J_\lambda$ is the size $n$ Jordan block with eigenvalue $\lambda$, then 

$$\{\operatorname{rank}(J_\lambda-\lambda I)^k\}_{k=0}^\infty = \{n, n-1, n-2, \ldots, 1, 0, 0, \ldots\}.$$

- The number of Jordan blocks belonging to $\lambda$ is equal to the number of linearly independent eigenvectors of $A$ belonging to $\lambda$. (i.e. $\# J_\lambda = \dim E(\lambda)$.)

각 Jordan block들의 순서를 고려하지 않는다면 어떤 정사각행렬 A의 JCF는 유일하게 결정된다. 그렇다면 어떤 행렬의 JCF를 어떻게 찾아낼 수 있을까? 그 답은 Jordan block의 형태에 있다. Jordan block $$J_i = \begin{bmatrix}  
\lambda & 1 & & \mathbf{0} \\   
& \ddots & \ddots & \\  
&  & \ddots & 1 \\  
\mathbf{0} & & & \lambda  
\end{bmatrix}$$을 고려할 때, 그 제곱, 세제곱은 다음과 같다. $$J_i^2 = \begin{bmatrix}  
\lambda & 1 & & \mathbf{0} \\   
& \ddots & \ddots & \\  
&  & \ddots & 1 \\  
\mathbf{0} & & & \lambda  
\end{bmatrix}$$

---

## High Power of Matrices
Let $A \in M_{n \times n}(\mathbb{C})$ and let $J$ be the JCF of $A$. Let denote 

$$Q^{-1}AQ = J = \begin{bmatrix} J_1 & & \mathbf{0} \\ & \ddots & \\ \mathbf{0} & & J_\ell \end{bmatrix}.$$

Then $A^k = QJ^kQ^{-1}$ where 

$$J^k = \begin{bmatrix} J^k_1 & & \mathbf{0} \\ & \ddots & \\ \mathbf{0} & & J^k_\ell \end{bmatrix}.$$

Suppose that $J_i = \lambda I + N \in M_{m \times m}(\mathbb{C})$ for some $1 \le i \le \ell$, where 

$$N = \begin{bmatrix} 0 & 1 & & \mathbf{0} \\ & \ddots & \ddots & \\ & & \ddots & 1 \\ \mathbf{0} & & & 0 \end{bmatrix}.$$

Since $IN = NI$ and $N^m = O$, we have 

$$\begin{align*} J_i^k &= \sum_{j=0}^k \binom{k}{j} N^j (\lambda I)^{k-j} = \sum_{j=0}^{m-1} \binom{k}{j} N^j (\lambda I)^{k-j} \\ &= \lambda^k I + \binom{k}{1} \lambda^{k-1} N + \binom{k}{2} \lambda^{k-2} N^2 + \cdots \\ & = \begin{bmatrix} \lambda^k & \binom{k}{1} \lambda^{k-1} & \binom{k}{2} \lambda^{k-2} & \cdots & \binom{k}{m-1} \lambda^{k-m+1} \\ & \ddots & \ddots & \ddots & \vdots \\ & & \ddots & \ddots & \binom{k}{2} \lambda^{k-2} \\ & & & \ddots & \binom{k}{1} \lambda^{k-1} \\ \mathbf{0} & & & & \lambda^k \end{bmatrix}. \end{align*}$$

