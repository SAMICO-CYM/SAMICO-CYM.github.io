--- 
title: 
date: 2026-03-
categories: [Mathematics, ]
tags: []
math: true
---

## Definition
**(i)** An open set $S$ is ***connected*** if each pair of points $z_1$ and $z_2$ in it can be joint by a polygonal line, consisting of a finite number of line segments, joined end to end, that lies entirely in $S$. 

**(ii)** A nonempty open set that is connected is a ***domain***.

**(iii)** If $D$ is a domain, then the ***region*** is the set $D \cup \partial D$.

**(iv)** A ***simply connected domain*** $D$ is a domain such that every simple closed contour within it encloses only points of $D$. 

**(v)** A ***multiply connected domain*** is a domain that is not simply connected.

---
## Theorem 1
If a function $f(z)$ is analytic throughout a simply connected domain $D$, then 

$$\int_C f(z) \, dz = 0$$

for every closed contour $C$ lying in $D$.

### Proof


---
## Corollary 1
**(i)** A function $f$ that is analytic throughout a simply connected domain $D$ must have an antiderivative everywhere in $D$. 

**(ii)** Entire functions always have antiderivatives.

---
## Theorem 2
Suppose that

**(i)** $C$ is simple closed contour with the counterclockwise direction.

**(ii)** $C_k (k = 1, 2, \cdots, n)$ are disjoint, simple closed contours interior to $C$, with the counter clockwise directions.

**(iii)** A function $f(z)$ is analytic on all of these contours and throughout the multiply connected domain consisting of the points inside $C$ and exterior to each $C_k$.

Then 

$$\int_C f(z) \, dz + \sum_{k=1}^n \int_{C_k} f(z) \, dz = 0.$$

### Proof


---
## Corollary 2
