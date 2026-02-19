--- 
title: Real Number System
date: 2026-02-19 15:00:00 +0900
categories: [Mathematics, Real Ananlysis]
tags: []
math: true
---

## Real Number
The **real numbers** $\mathbb{R}$ is a set of objects satisfying Axioms 1 to 13 as listed in the following:  
- **(A1)** There is a binary operation, called addition and denoted $+$, such that $x, y \in \mathbb{R} \Longrightarrow x + y \in \mathbb{R}$,  
- **(A2)** $(x + y) + z = x + (y + z), \forall x, y, z \in \mathbb{R}$,  
- **(A3)** $x + y = y+x, \forall x, y \in \mathbb{R}$,  
- **(A4)** An additive identity exists. There exists a real number denoted $0$ which satisfies $x + 0 = 0+x = x, \forall x \in \mathbb{R}$,  
- **(A5)** Additive inverses exist. $\forall x \in \mathbb{R}, \exists y \in \mathbb{R}$ such that $x+y=0=y+x$ ($y$ is denoted $-x$ and we define $x-z$ as $x + (-z)$, $\forall x, z \in \mathbb{R}$),  
- **(A6)** There is a binary operation, called multiplication and denoted $\cdot$, such that $x, y \in \mathbb{R} \Longrightarrow x \cdot y (\text{or } xy) \in \mathbb{R}$,  
- **(A7)** $(xy)z = x(yz), \forall x, y, z \in \mathbb{R}$,  
- **(A8)** $xy = yx, \forall x, y \in \mathbb{R}$,  
- **(A9)** A multiplicative identity exists. There exists a real number, different from $0$, denoted $1$ which satisfies $x \cdot 1 = x = 1 \cdot x$,  
- **(A10)** Multiplicative inverses exist for nonzero real numbers. $\forall x \in \mathbb{R}$ with $x \neq 0$, $\exists y \in \mathbb{R}$ such that $xy = 1 = yx$, ($y$ is denoted $x^{-1}$ or $\frac{1}{x}$ and we define $\frac{x}{y} = x(y^{-1})$ if $y \neq 0$.)  
- **(A11)** $x(y+z) = xy + yz, (y+z)x = yx + zx, \forall x, y, z \in \mathbb{R}$,  
- **(A12)** There is a subset $P$ of $\mathbb{R}$ called the positive real numbers satisfying 

(i) $x, y \in P \Longrightarrow x+y, xy \in P$.  

(ii) If $x \in \mathbb{R}$, then exactly one of the following statements is true: $$x \in P \text{ or } x = 0 \text{ or } -x \in P$$
- **(A13)** A nonempty subset of real numbers which is bounded above has a least upper bound.

---
## Theorem 1
- The additive identity of (A4) and the additive inverse of (A5) are unique.
### Proof
Let $x \in \mathbb{R}$, and suppose that $0$ and $0'$ are two additive identities. Then $0 = 0 + 0' = 0'$ by axiom 4, so the additive identity is unique. Suppose that $y$ and $z$ are two additive inverses of $x$. Then 
$$\begin{align*} y & = y + 0 \text{(A4)} \\ &= y + (x + z) \text{(A5)} \\& = (y + x) + z \text{(A2)} \\ &= 0 + z \text{(A5)} \\ &= z. \text{(A4)} \end{align*}$$

Thus the additive inverse is unique. $\blacksquare$

---

## Theorem 2
Let $x, y, z \in \mathbb{R}$. Then the followings hold:
- **(1)** $x \cdot 0 = 0$,  
- **(2)** $-(-x) = x$,  
- **(3)** $-(x+y)=-x-y$  
- **(4)** $xy=0 \iff x=0 \vee y=0$,  
- **(5)** $xy=xz$ and $x \neq 0 \Longrightarrow y = z$,  
- **(6)** $-(xy) = x(-y) = (-x)y$,  
- **(7)** $(-1)x = -x$.
### Proof 
**(1)** 

$$\begin{align*} 0 \cdot x &= (0 + 0) \cdot x \text{(A4)} \\ &= 0 \cdot x + 0 \cdot x \text{(A11)} \\ \Longrightarrow 0 \cdot x &= 0 \text{(A4)}. \end{align*}$$

**(2)** Note that the additive inverse of $(-x)$ is $-(-x)$. Then

$$\begin{align*} x &= x + 0 \text{(A4)} \\ &= x + ((-x) + (-(-x))) \text{(A5)} \\ &= (x + (-x)) + (-(-x)) \text{(A2)} \\ &= 0 + (-(-x)) \text{(A5)} \\ &= -(-x). \text{(A4)} \end{align*}$$

Thus $x = -(-x)$.  
**(3)** Then 

$$\begin{align*} -(x + y) &= -(x+y) + 0 + 0 \text{(A4)} \\ &= -(x+y) + (x -x) + (y - y) \text{(A5)} \\ &= -(x+y) + (x+y) + (-x -y) \text{(A2, A3)} \\ &= 0 + (-x -y) \text{(A5)} \\ &= -x -y. \text{(A4)} \end{align*}$$

Thus $-(x+y) = -x -y$.   
**(4)** $(\Longleftarrow)$ Clear.  
$(\Longrightarrow)$ Suppose that $y \neq 0$. Then 

$$\begin{align*}x &= x\cdot 1 \text{(A9)} \\ &= x \cdot(y \cdot \frac{1}{y}) \text{(A10)} \\ &= (xy) \cdot \frac{1}{y} \text{(A7)} \\ &= 0.\end{align*}$$

Similarly, if $x \neq 0$, then $xy = 0$.   
**(5)** 

$$\begin{align*}y &= y \cdot 1 \text{(A9)} \\ &= y \cdot(x \cdot \frac{1}{x}) \text{(A10)} \\ &= (xy) \cdot \frac{1}{x} \text{(A7, A8)} \\ &= z \cdot (x \cdot \frac{1}{x}) \text{(A7, A8)} \\& = z \cdot 1 = z. \text{(A10, A9)}\end{align*}$$

**(6)** 

$$\begin{align*}0 &= xy - (xy) \text{(A5)} \\ &= xy - (xy) + 0 \text{(A4)} \\ &= xy - (xy) + x(-y) - x(-y) \text{(A5)} \\ &= x(y - y) - (xy) - x(-y) \text{(A3, A11)} \\ &= x \cdot 0 -(xy) - x(-y) \\ &= -(xy) - x(-y) \text{(A4, A5, (1))}\end{align*}$$

Then 

$$-(xy) = -(-x(-y)) = x(-y) \text{(A5, (2))}$$

Similarly, we can show that $-(xy) = (-x)y$.   
**(7)** 

$$(-1)x = -(1 \cdot x) = -x. \text{(A9), (6)} \blacksquare$$



---

## Inequalities
Let $x, y \in \mathbb{R}$.
- **(1)** $x$ is **negative** if $-x$ is positive,  
- **(2)** $x > y$ means $x − y$ is positive,  
- **(3)** $x ≥ y$ means $x > y$ or $x = y$,  
- **(4)** $x < y$ means $y > x$,  
- **(5)** $x ≤ y$ means $y ≥ x$.

---

## Theorem 3
Let $x, y, z \in \mathbb{R}$.  
- **(1)** $1 > 0$,  
- **(2)** $x > y \wedge y > z \Longrightarrow x > z$,  
- **(3)** $x > y \Longrightarrow x + z > y + z$,  
- **(4)** $x > y \wedge z > 0 \Longrightarrow xz > yz,$  
- **(5)** $x > y \wedge z < 0 \Longrightarrow xz < yz$
### Proof 
**(1)** By A12, $1 \in P$ or $1 = 0$ or $-1 \in P$. By A9, $1 \neq 0$. If $-1 \in P$, then $(-1) \cdot (-1) = -(-1) = 1 \in P$ by A12 and Thm 3.4. $\bigotimes$ Thus $1 = 1 - 0 \in P \iff 1 > 0$. 

**(2)** Note that $x > y \iff x - y \in P$ and $y > z \iff y - z \in P$ by Definition 4.1. Then $(x - y) + (y - z) = x - z \in P \iff x > z$ by Definition 4.1, A2, and A4. 

**(3)** Note that $x > y \iff x - y \in P$. Then $x - y = x - y + 0 = x - y + (z - z) = x + z - (y + z) \in P \iff x + z > y + z$ by A2, A3, A4, A5, and Definition 4.1. $\blacksquare$