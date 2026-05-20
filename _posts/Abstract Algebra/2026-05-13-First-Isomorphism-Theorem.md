--- 
title: First Isomorphism Theorem
date: 2026-05-13
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Theorem 1
Let $H \lhd G$. The map $\gamma: G \to G/H$ defined by $\gamma(g) = gH, \forall g \in G$ is an epimorphism with $\ker(\phi) = H$. We call $\gamma$ the ***canonical epimorphism***.

### Proof
Clearly, $\gamma$ is well-defined. 

Let $a, b \in G$. Then we have

$$\begin{align*}
\gamma(ab) &= (ab)H \\
&= (aH)(bH) \\
&= \gamma(a) \gamma(b),
\end{align*}$$

so that $\gamma$ is a homomorphism.

Let $gH \in G/H$. Then $g \in H$ and $\gamma(g) = gH$. Hence $\gamma$ is an epimorphism.

Let $g \in \ker(\phi)$. Then $gH = \phi(g) = H$, which means that $g \in H$. If $g \in H$, then $\gamma(g) = gH = H$, which means that $g \in \ker(\phi)$. Thus, $\ker(\phi) = H$. $\blacksquare$

---
## First Isomorphism Theorem
Let $\phi: G \to G'$ be a group homomorphism.

**(i)** The map $\mu: G/\ker(\phi) \to \mathrm{Im}(\phi)$ defined by 

$$\mu(g\ker(\phi)) = \phi(g)$$

for all $g\ker(\phi) \in G/\ker(\phi)$ is an isomorphism, and therefore $G/\ker(\phi) \cong \mathrm{Im}(\phi)$.

**(ii)** If $\gamma: G \to G/\ker(\phi)$ is the epimorphism in Theorem 1, then $\phi = \mu \circ \gamma$.

![](assets/img/Pasted%20image%2020260513165730.png)

### Proof
(i) Let $x, y \in G$. If $x\ker(\phi) = y\ker(\phi)$, then we have $x^{-1}y \in \ker(\phi)$. Then 

$$\begin{align*} 
e' &= \phi(x^{-1}y) \\ 
&= \phi(x^{-1})\phi(y) \\
&= \phi(x)^{-1} \phi(y),
\end{align*}$$

so that $\mu(x\ker(\phi)) = \phi(x) = \phi(y) = \mu(y\ker(\phi))$. Thus, $\mu$ is well-defined.

Let $g\ker(\phi) \in \ker(\mu)$ where $g \in G$. Then $\phi(g) = \mu(g\ker(\phi)) = e'$, which means that $g \in \ker(\phi)$. Then $g\ker(\phi) = \ker(\phi)$. Thus, $\ker(\mu) = \\{\ker(\phi) \\}$, which means that $\mu$ is injective. 

Let $a \in \mathrm{Im}(\phi)$. Then $a = \phi(g)$ for some $g \in G$. Now, $\mu(g\ker(\phi)) = \phi(g) = a$. Thus, $\mu$ is surjective. 

Let $x\ker(\phi), y\ker(\phi) \in G/\ker(\phi)$. Then 

$$\begin{align*}
\mu(x\ker(\phi)y\ker(\phi)) &= \mu((xy)\ker(\phi)) \\
&= \phi(xy) \\
&= \phi(x)\phi(y) \\
&= \mu(x\ker(\phi))\mu(y\ker(\phi)).
\end{align*}$$

Hence, $\mu$ is an isomorphism.

(ii) Let $g \in G$. Then we have

$$\begin{align*}
(\mu \circ \gamma)(g) &= \mu(\gamma(g)) \\
&= \mu(g\ker(\phi)) \\
&= \phi(g).
\end{align*}$$

Thus, $\phi = \mu \circ \gamma$. $\blacksquare$

---

## Corollary
Let $\phi: G \to G'$ be a group epimorphism. Then $G/\ker(\phi) \cong G'$.

### Proof
Since $\phi$ is surjective, we have $\mathrm{Im}(\phi) = G'$. By Theorem 1 (i), $G/\ker(\phi) \cong \mathrm{Im}(\phi) = G'$. $\blacksquare$

---
## Theorem 3
Let $H$ and $K$ be groups. 

**(i)** $(H \times K) / (H \times \\{ e_K \\}) \cong K$.

**(ii)** $(H \times K) / (\\{ e_H \\} \times K) \cong H$.

### Proof
**(i)** Define a function $\phi: H \times K \to K$ by $\phi(h, k) = k, \forall (h, k) \in H \times K$. Clearly, $\phi$ is an epimorphism with kernel $H \times \\{ e_K \\}$. By the first isomorphism theorem, $(H \times K)/(H \times \\{ e_K \\}) \cong K$. 

**(ii)** Similar to (i). $\blacksquare$

---
## Remark
대수학을 잠깐 벗어나서 집합론으로 돌아가 일반적으로 생각해보자. 집합 $X$가 주어지면 각각의 원소는 exactly 구분된다. 정말로 각 원소가 같으면 같고 다르면 다르다는 말이다. 그런데 "같음"을 정의하는 방식을 항상 이렇게 강하게 줄 필요는 없다. 두 도형이 같다는 말을 정확히 길이와 각도가 같은 합동 조건으로 줄 수도 있지만, 닮음 조건으로 줄 수도 있듯이 말이다. 마찬가지로 수학에서 두 대상이 "같다"라는 말을 할 때 주로 사용하는 방법이 동치 조건을 이용한 방법인데, 동치 조건 $\sim$에 대하여 $x \sim y$라면 두 대상 $x, y$는 "사실상 같다"고 말할 수 있다. 그러면 이렇게 "사실상 같은" 대상들 끼리 모아서 집합 $[x]$을 구성하면 그 자체를 우리가 정의한 동치 관계 $\sim$의 관점에서 하나의 원소로 취급할 수 있고, 이들을 모아놓은 집합을 $X / \sim$이라고 쓰고 quotient set이라고 부른다. 

이 컨셉을 그대로 가져와서 함수 $f: X \to Y$에 적용해보자. 위에서와 비슷하게, $f$가 injective가 아니라면 $f(x) = f(y)$라고 해서 $x=y$라고 말할 수 없다. 그러면 거꾸로 $f$를 bijection으로 만들기 위해서는 함수값이 같은 원소는 "사실상 같다"고 정의해주면 된다. 즉 $X$ 위에서의 동치 관계 $\sim$를 $x \sim y \iff f(x) = f(y)$로 정의하자는 말이다. 그리고 $f$로부터 유도되는 함수 $f': X / \sim \to \mathrm{Im}(f)$를 $f'([x]) = f(x)$로 정의하면 $f'$이 bijection이라는 사실은 쉽게 확인할 수 있다. 즉 quotient set $X / \sim$과 $\mathrm{Im}(f)$의 원소들은 하나씩 일대일대응이되고, 이 말은 구조적으로 두 집합이 "사실상 같다"는 말이다. 

한편, 위에서 $X$의 원소들이 "사실상 같음"을 정의할 때 기준이 됐었던 대상은 함수 $f$였다. 그러면 $f$가 다르게 주어지면 "사실상 같음"의 기준도 달라질 것이다. 함수 $f$로 같음의 기준을 정의하는 과정이 완벽하게 discrete하게 구분이 됐던 $X$의 원소들을 적당히 "뭉뚱그려서" 구분을 하는 과정과 같다는 사실을 이해한다면, 함수 $f$를 주는 행위는 집합 $X$를 적당히 잘 자르는 행위와 같음을 받아들일 수 있을 것이다. 극단적인 예시를 들어보면, $f$를 identity function으로 주는 행위는 이전과 동일하게 각 원소들을 exactly하게 구분하는 행위와 동일하고, $f$를 constant function으로 주는 행위는 아예 모든 원소를 다 동일하게 보는, 아주 rough한 기준을 주는 행위와 동일하다. 

이제 다시 대수학으로 돌아와서 group에 대해서 위의 논의를 적용해보자. 위에서와 마찬가지로 $G$라는 군을 적당히 자르기 위해 group homomorphism $\phi: G \to G'$을 가지고 왔다. 이때 $H := \ker(\phi)$는 $G$의 정규부분군이고, 따라서 $G/H$은 factor group이다. 군 $G / H$를 위의 관점으로 보면 $G$라는 집합을 $H$라는 부분군으로 정의되는 동치 관계로 잘 잘랐다고 볼 수 있는데, 이때 "사실상 같음"은 어떤 기준으로 정의된 걸까?

우선 $H$의 coset들을 살펴보면, 그 형태는 각각 $gH$로 주어진다. 즉 $H$의 원소들을 $g$만큼 움직인 집합인데, 다르게 말하면 $H$의 원소로부터 $g$만큼 떨어져 있는 원소들을 모아놓은 집합이다. 이때 $H$는 $\phi$의 kernel이고, kernel의 원소들은 $\phi$에 의해서 매핑됐을 때 사실상 아무런 영향이 없는 원소들이라고 볼 수 있으므로 $gH$에서 원소를 하나 들고와서 $\phi$에 의해 매핑시키면 그냥 $g$를 매핑했을 때와 같은 결과를 준다. 그러면 $G$를 $H$로 자른다는 말은, 어차피 $g$에 $H$의 원소 $h$를 곱해서$\phi$로 보내나, $g$를 그냥 $\phi$로 보내나 같은 값을 주기 때문에 $G$의 원소에 $h$를 곱해서 보낸 값이 같은 $G$의 원소들은 같다고 보겠다는 말과 같다. 이게 $G$를 $H$를 기준으로 잘랐다, factorization했다는 말의 직관이다. 그러면 $G / H$와 $\mathrm{Im}(\phi)$가 isomorphic함은 자명한 사실이다. 

--- 
## Example
(i) 다음과 같이 정의된 group homomorphism $\phi: \mathbb{Z}_4 \times \mathbb{Z}_2 \to \mathbb{Z}_4 \times \mathbb{Z}_2$을 고려하자. 

$$\phi(a, b) = (a, 0), \forall (a, b) \in \mathbb{Z}_4 \times \mathbb{Z}_2.$$

우선 $\ker(\phi) = \\{ 0 \\} \times \mathbb{Z}_2$이고, $\phi(\mathbb{Z}_4 \times \mathbb{Z}_2) = \mathbb{Z}_4 \times \\{ 0 \\}$임을 쉽게 확인할 수 있다. 따라서 First Isomorphism Theorem에 의해서 

$$
\begin{align*}
\mathbb{Z}_4 \times \mathbb{Z}_2 / (\{ 0 \} \times \mathbb{Z}_2) & \cong \mathbb{Z}_4 \times \{ 0 \} \\
& \cong \mathbb{Z}_4
\end{align*}
$$

이 성립한다. 위의 factor group이 $\mathbb{Z}_4$와 isomorphic함을 정리를 통해서도 확인할 수 있지만, 다루고 있는 집합들이 모두 finite abelian group이므로 직접 분류해서 보여줄 수도 있다. 

우선 $\mathbb{Z}_4 \times \mathbb{Z}_2$은 order $8$인 group이고 $\ker(\phi) = \\{ 0 \\} \times \mathbb{Z}_2$은 order $2$인 subgroup이므로 factor group의 order는 $\frac{8}{2} = 4$이다. 이때 order $4$인 group은 $\mathbb{Z}_4$와 Klein-4 group $V$뿐임을 알고 있으므로, factor group은 둘 중 하나와 isomorphic하다. 

둘 중 어느 것과 isomorphic한지 결정하기 위해서 factor group의 원소의 order를 계산해보자. $(1, 0) + \ker(\phi)$를 반복해서 더하면 $(1, 0) + \ker(\phi), (2, 0) + \ker(\phi), (3, 0) + \ker(\phi), (0, 0) + \ker(\phi)$이 나오고 각 coset들은 자명하게 모두 다르다. 따라서 $(1, 0) + \ker(\phi)$는 order가 $4$인 원소이므로, factor group은 $\mathbb{Z}_4$와 isomorphic하다. 

위와 같이 집합 간의 isomorphic함을 보이기 위해서 first isomorphism theorem을 이용할 수도 있지만, 이 방법은 구체적으로 homomorphism을 잡아야 한다는 단점이 있다. 따라서 위와 같이 finite abelian group을 분류해 냄으로써 isomorphic함을 보이는 게 때때로는 더 효율적일 수도 있음을 명심하자.

(ii) 