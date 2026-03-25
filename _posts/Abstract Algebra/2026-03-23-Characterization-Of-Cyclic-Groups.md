---
title: Characterization Of Cyclic Groups
date: 2026-03-23 00:00:01
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Theorem 1
Let $G$ be a cyclic group.

**(i)** If $\vert G \vert = \infty$, then $G \cong (\mathbb{Z}, +)$.

**(ii)** If $\vert G \vert = n \in \mathbb{N}$, then $G \cong (\mathbb{Z}_n, +)$.

### Proof
Let $G = \langle a \rangle$, and let $e$ denote the identity of $G$.

**(i)** Suppose that $\vert G \vert = \infty$. Then $a^m \neq a^n, \forall m \neq n \in \mathbb{Z}$.

$\Big[ (\because)$ Suppose that $a^m = a^n$ for some integers $m > n$. Then $a^{m - n} = e$. We claim $G = \\{ e, a, a^2, \cdots, a^{m - n - 1} \\}$.
\\
$\Big[ (\because)$ Since $a \in G$, clearly $G \supset \\{ e, a, a^2, \cdots, a^{m - n - 1} \\}$. Let $x \in G$. Then $x = a^k$ for some $k \in \mathbb{Z}$. By division algorithm, $\exists \, q, r \in \mathbb{Z}$ such that $k = (m - n)q + r$ and $0 \le r < m - n$. Then we have 

$$\begin{align*}
x &= a^k \\
&= a^{(m-n)q + r} \\
&= (a^{m - n})^q a^r \\
&= a^r \in \{ e, a, a^2, \cdots, a^{m - n - 1} \}. \Big]
\end{align*}$$

Thus $G = \\{ e, a, a^2, \cdots, a^{m - n - 1} \\}$, so that $\vert G \vert = m - n < \infty$. $\bigotimes$ Hence $a^m \neq a^n, \forall m \neq n \in \mathbb{Z}$. $\Big]$

Define the function $\phi : G \to \mathbb{Z}$ by $\phi(a^m) = m, \forall a^m \in G$. Clearly $\phi$ is well-defined. 

If $\phi(a^m) = \phi(a^n)$, then $m = n$, so that $a^m = a^n$. Thus $\phi$ is injective. 

Let $m \in \mathbb{Z}$. Then $a^m \in G$, so that $\phi(a^m) = m$. Thus $\phi$ is surjective.

Let $a^m, a^n \in G$. Then 

$$
\begin{align*}
    \phi(a^m a^n) &= \phi(a^{m + n}) \\
    &= m + n \\
    &= \phi(a^m) + \phi(a^n).
\end{align*}
$$

Thus $\phi$ is a homomorphism, and so that $G \cong (\mathbb{Z}, +)$.

**(ii)** Suppose that $\vert G \vert = n \in \mathbb{N}$. Then $a^i \neq a^j, \forall 0 \le i < j \le n-1$.

$\Big[ (\because)$ If $a^i = a^j$ for some $0 \le i < j \le n-1$, then $a^{j-i} = e$, which means that $G = \\{ e, a, a^2, \cdots, a^{j - i - 1} \\}$. Thus $\vert G \vert = j - i \le n-1$. $\bigotimes$ Hence $a^i \neq a^j, \forall 0 \le i < j \le n-1$. $\Big]$

Since $G = \langle a \rangle$, we have $G = \\{ e, a, a^2, \cdots, a^{n-1} \\}$. Then $a^n = e$ because $a^n \in G$ so that $a^n = a^k$ for some $0 \le k < n-1$ and $a^{n-k} = e$ with $n-k \in \{ 1, 2, \cdots, n-1 \}$. $\bigotimes$

Define the function $\phi : G \to \mathbb{Z}_n$ by $\phi(a^m) = m \pmod n, \forall a^m \in G$. By division algorithm, $\phi$ is well-defined. Note that if $m \equiv r \pmod n$, then $a^m = a^r$.

If $\phi(a^m) = \phi(a^k)$, then $m \equiv k \pmod n$. so that $a^m = a^k$. Thus $\phi$ is injective. 

Let $m \in \mathbb{Z}_n$, that is, $m \equiv m \pmod n$. Then $a^m \in G$, so that $\phi(a^m) = m$. Thus $\phi$ is surjective.

Let $a^m, a^k \in G$, and let $m \equiv r_1 \pmod n$ and $k \equiv r_2 \pmod n$ with $0 \le r_1, r_2 \le n-1$. Then 

$$
\begin{align*}
    \phi(a^m a^k) &= \phi(a^{m + k}) \\
    &= m + k \pmod n \\
    &= r_1 + r_2 \pmod n \\
    &= r_1 + r_2 \\
    &= \phi(a^m) + \phi(a^k).
\end{align*}
$$

Thus $\phi$ is a homomorphism, and so that $G \cong (\mathbb{Z}_n, +)$. $\blacksquare$

---

## Remark
Let $G = \langle a \rangle$ with $\vert G \vert = n$. 

**(i)** $n$ is the smallest positive integer such that $a^n = e$.

**(ii)** $a^m = e$ for some $m \in \mathbb{Z} \setminus \\{ 0 \\} \iff n \vert m$.

---

## Example
Let $U_n = \\{ z \in \mathbb{C} \mid z^n = 1 \\}$. Then $(U_n, \cdot) \cong (\mathbb{Z}_n, +)$.

---

## Theorem 2
Let $G$ be a cyclic group with $\vert G \vert = n$, and let $a$ be a generator of $G$. Then 

$$\vert \langle a^s \rangle \vert = \frac{n}{\gcd(n, s)}, \quad \forall s \in \mathbb{Z}$$

### Proof

Since $\langle a^s \rangle \le G$, $\vert \langle a^s \rangle \vert < \infty$. Let $m = \vert \langle a^s \rangle \vert$. Then $m$ is the smallest positive integer such that $a^{sm} = (a^s)^m = e$. Since $\vert \langle a \rangle \vert = \vert G \vert = n$, $n \vert sm$. 

We claim $m = \frac{n}{\gcd(n, s)}$.

$(\because)$ Let $d = \gcd(n, s)$. Then 

$$\begin{align*}
d &= n \alpha + s \beta \\
\implies 1 &= \left( \frac{n}{d} \right) \alpha + \left( \frac{s}{d} \right) \beta
\end{align*}$$

for some $\alpha, \beta \in \mathbb{Z}$. Note that 

$$\frac{\frac{ms}{d}}{\frac{n}{d}} = \frac{ms}{n} \in \mathbb{Z},$$

so that $\frac{n}{d} \vert \frac{ms}{d}$, and so $\frac{n}{d} \vert m$ because $\gcd(\frac{n}{d}, \frac{s}{d}) = 1$. 

Since $(a^s)^{\frac{n}{d}} = (a^{n})^{\frac{s}{d}} = e$, we have $m \vert \frac{n}{d}$. Thus $m = \frac{n}{d}$.  $\blacksquare$

---

## Corollary
Let $G = \langle a \rangle$ with $\vert G \vert = n$. 

**(i)** $\vert \langle a^s \rangle \vert = \vert \langle a^t \rangle \vert \iff \gcd(n, s) = \gcd(n, t)$.

**(ii)** The other generators of $G$ are the elements of the form $a^r$, where $\gcd(n, r) = 1$.

### Proof
**(i)** By Theorem 2, 

$$\begin{gather*} 
\frac{n}{\gcd(n, s)} = \vert \langle a^s \rangle \vert = \vert \langle a^t \rangle \vert = \frac{n}{\gcd(n, t)} \\
\iff \gcd(n, s) = \gcd(n, t).
\end{gather*}$$

**(ii)** Let $G = \langle a^r \rangle$. By Theorem 2, we have

$$n = \vert G \vert = \vert \langle a^r \rangle \vert = \frac{n}{\gcd(n, r)}.$$

Thus $\gcd(n, r) = 1$. $\blacksquare$

순환군 $G$의 생성원을 $a$라고 하면, $G$의 어떤 부분군 $H$도 순환군이므로 적당한 정수 $k$에 대하여 $a^k$를 생성원으로 가질 것이다. 

순환군은 생성원의 반복 연산으로 얻어진 집합이다. 그러니까 어떤 원소 $x$에 $a$를 연산하는 것은 $x$의 '다음 단계'원소를 얻는 행위로 이해할 수 있다. 이때 군의 order가 $n$이면 $\langle a \rangle = \\{ e, a, a^2, ..., a^{n-1} \\}$로 나타낼 수 있다. 그러니까 모든 원소를 생성해 내기 위해 항등원에서 거쳐야 할 단계가 총 $n$단계 있다는 뜻이다. 

그런데 부분 순환군 $H$가 $a^k$를 생성원으로 가지면, $H$ 안에서는 다음 단계로 가기 위해서는 $a^k$, 즉 $a$를 $k$번 연산해야 한다. 만약 $k$가 $n$의 약수라면, 즉 $k$를 적당히 $m$번의 정수번 만큼 더해서 $n$을 만들어낼 수 있다면, $H$ 안에서 모든 원소를 생성해 내기 위해 항등원에서 거쳐야 할 단계는 총 $m$단계인 것이다. 그리고 $m$은 정확히 $H$의 order이다. 

$k$가 $n$의 약수는 아니지만 적당히 공유하는 약수가 있다고 하자. 일반적으로 얘기하면, 기존에는 총 $n$ 단계를 거쳐서 순환군의 모든 원소를 만들어냈어야 했다면, 부분군에서는 단위가 $a$에서 $a^k$로 $k$배가 늘어났기 때문에, 즉 $1$에서 $k$로 단위가 늘어났기 때문에 모든 원소를 $k$번씩 연산해서 만들어낸다. 이때 공약수만큼은 모든 원소를 만들어내기 위해 $a^k$를 반복적으로 취한다는 관점에서 아무런 영향을 미치지 못하므로, '진짜' 기여도를 보기 위해서는 $gcd(n, k)$로 나눠줘야 하는 것이다.