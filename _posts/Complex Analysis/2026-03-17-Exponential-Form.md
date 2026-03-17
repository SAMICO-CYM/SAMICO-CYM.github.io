---
title: Exponential Form
date: 2026-03-17
categories: [Mathematics, Complex Analysis]
tags: []
math: true
---

## Remark
Let $z = (x, y) \in \mathbb{C}$ and let $\vert z \vert = r$. Assume $z \neq 0$. 
![alt text](assets/img/Gemini_Generated_Image_btbom8btbom8btbo.png)
Note that $\theta$ is the angle between the positive real axis and the directed line segment from the origin to $z$. Since 

$$x = r \cos \theta \quad \text{and} \quad y = r \sin \theta,$$

we have

$$
z = r(\cos \theta + i \sin \theta).
$$

Note that the ***Euler's formula*** is given by

$$
e^{i\theta} = \cos \theta + i \sin \theta.$$

Thus, we have

$$
z = r e^{i\theta}.
$$

## Definition 1
Let $z (\neq 0) \in \mathbb{C}$. Then $z$ can be written in ***exponential form*** as

$$z = r e^{i\theta}.$$

## Remark
**(i)** The circle 

$$C_R(z_0) = \{ z \in \mathbb{C} \mid \vert z - z_0 \vert = R \}$$

with radius $R$ centered at $z_0$ can be parametrized by 

$$z = z_0 + Re^{i\theta}, \quad \theta \in [0, 2\pi).$$

**(ii)** Note that $\cos \theta$ and $\sin \theta$ are periodic with period $2\pi$. Thus, there exists infinitely many $\theta$ such that $z = r e^{i\theta}$, says 

$$z = re^{i\theta} = r e^{i(\theta + 2n\pi)}, \quad \forall n \in \mathbb{Z}.$$ 

Each value of $\theta$ is called the ***argument*** of $z$, and the set of all such values is denoted by $\arg z$. The ***principal value*** of $\arg z$, denoted by $\text{Arg } z$, is the unique value $\Theta$ such that $-\pi < \Theta \le \pi$. Then we have

$$\arg z = \{\text{Arg } z + 2n\pi \mid n \in \mathbb{Z}\}$$

## Theorem 1
Let $z_1 = r_1 e^{i\theta_1}$ and $z_2 = r_2 e^{i\theta_2}$. Then

**(i)** $z_1 z_2 = r_1 r_2 e^{i(\theta_1 + \theta_2)}$

**(ii)** $\displaystyle \frac{z_1}{z_2} = \frac{r_1}{r_2} e^{i(\theta_1 - \theta_2)}$ if $z_2 \neq 0$

**(iii)** $z_1^n = r_1^n e^{in\theta_1}$ for any integer $n$

**(iv)** $\displaystyle \cos (2m \theta) = \sum_{k=0}^m (-1)^k \binom{2m}{2k} \cos^{2m-2k} \theta \sin^{2k} \theta$ and $\displaystyle \sin (2m \theta) = \sum_{k=0}^m (-1)^k \binom{2m}{2k+1} \cos^{2m-2k-1} \theta \sin^{2k+1} \theta$

### Proof
