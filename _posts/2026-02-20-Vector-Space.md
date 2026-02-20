--- 
title: Vector Space
date: 2026-02-20 20:00:00 +0900
categories: [Mathematics, Linear Algebra]
tags: []
math: true
---

## Definition
- ***A vector space $V$ over a field $F$*** consists of a nonempty set on which two binary operations $+: V \times V \to V$ and $\cdot : F \times V \to V$ (called ***addition*** and ***scalar multiplication***, respectively) are defined such that the following conditions hold:

**(1)** $x + y = y + x, \forall x, y \in V$,  
**(2)** $(x+y)+z=x+(y+z), \forall x, y, z \in V$,  
**(3)** $\exists \,\mathbf{0} \in V$ such that $x+\mathbf{0}=x, \forall x \in V$,  
**(4)** $\forall x \in V, \exists \,y \in V$ such that $x+y=\mathbf{0}$ (We denote $y = -x$)
**(5)** $1 \cdot x = x, \forall x \in V$ where $1 \in F$,  
**(6)** $(ab)x = a(bx), \forall a, b \in F$ and $\forall x \in V$,  
**(7)** $a(x+ y) = ax + ay, \forall a \in F$ and $\forall x, y V$,  
**(8)** $(a + b)x = ax + bx, \forall a, b \in F$ and $\forall x \in V$,  
- We call an elemetnt $v$ in $V$ a ***vector*** and an element $a$ in $F$ a ***scalar***.

---

## Theorem 1
