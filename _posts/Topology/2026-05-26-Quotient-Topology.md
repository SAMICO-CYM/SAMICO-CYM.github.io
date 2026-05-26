--- 
title: Quotient Topology
date: 2026-05-26
categories: [Mathematics, Topology]
tags: []
math: true
---

## Definition 1
Let $X$ and $Y$ be topological spaces, and let $p: X \to Y$ be a surjective map. The map $p$ is said to be a ***quotient map*** if 

$$U \text{ is open in } Y \iff p^{-1}(U) \text{ is open in } X.$$

[연속함수](<{% post_url Topology/2026-04-29-Continuous-Functions %}#definition>)가 $(\Longrightarrow)$ 방향에 대해서만 정의되는 반면, quotient map은 양방향 모두 성립하면서 surjective인 함수로 정의된다. 

---
## Remark
**(i)** Every quotient map is continuous.

**(ii)** An equivalent condition is to require that 

$$C \text{ is closed in } Y \iff p^{-1}(C) \text{ is closed in } X.$$

**(iii)** Every surjective, continuous, open (or closed) map is a quotient map. However, the converse does not hold. In particular, there is a quotient map that is not an open map.

$\big[(\because)$ We consider $\pi_1: \mathbb{R} \times \mathbb{R} \to \mathbb{R}$ and $A = \\{ (x, y) \in \mathbb{R} \times \mathbb{R} \mid x \ge 0 \text{ or } y = 0 \\}.$ Then $q := \pi_1 \vert_A : A \to \mathbb{R}$ is a quotient map, but not open. 

To see this, consider 

$$B := A \cap \\{ (x, y) \in \mathbb{R} \times \mathbb{R} \mid x^2 + (y- 2)^2 \le 1 \\}.$$

Then $q(B) = [0, 1)$, which is not open in $\mathbb{R}$.$\big]$

---
## Theorem
Let $X$ be a topological space and let $A$ be a set. Let $p: X \to A$ be a surjective map. Then the collection 

$$\mathscr{T}_p = \{  U \subset A \mid p^{-1}(U) \text{ is open in } X \}$$

forms a topology on $A$. We call this ***the quotient topology on $A$ induced by $p$.***

정의에서는 $A$에 어떠한 topology도 주지 않았었고, 당연히 $p$도 quotient map이라는 말을 하지 않았다. 그런데 $\mathscr{T}_p$와 같이 컬렉션을 주면 이는 $A$에서의 topology가 되고, 그제서야 비로소 $p$도 quotient map이 된다. 사실 정의를 보면 $p$가 반드시 quotient map이 되도록 topology를 만든 것에 불과하다.

### Proof
Since $p^{-1}(\emptyset) = \emptyset$ and it is open in $X$, $\emptyset \in \mathscr{T}_p.$ Since $p^{-1}(A) = X$ and it is open in $X$, $X \in \mathscr{T}_p.$

Let $\\{ U_\alpha \\}$ be a collection of elements of $\mathscr{T}_p.$ Then 

$$\begin{align*}
p^{-1}\left( \bigcup U_\alpha \right) &= \bigcup p^{-1}(U_\alpha)
\end{align*}$$

is open in $X$ because each $p^{-1}(U_\alpha)$ is open in $X$. 

Let $\\{ U_i \\}_{i=1}^n$ be a finite collection of elements of $\mathscr{T}_p$. Then 

$$\begin{align*}
p^{-1}\left( \bigcap_{i=1}^n U_i \right) &= \bigcap_{i=1}^n p^{-1}(U_i)
\end{align*}$$

is open in $X$ because each $p^{-1}(U_\alpha)$ is open in $X$. 

Hence $\mathscr{T}_p$ forms a topology on $A$. $\blacksquare$

---
## Definition 2
Let $X$ be a topological space, and let $\sim$ be an equivalence relation of $X$. Let $p: X \to X / \sim$ be the canonical projection, that is, $p(x) = [x], \forall x \in X$, where $[x]$ is the equivalence class of $x$. Then the topological space $(X/\sim, \mathscr{T}_p)$ is called a ***quotient space*** of $X$. 

---
## Example
이쯤 왔으면 도대체 quotient map이니, quotient topology, space라는 걸 왜 다루는지 의문을 가지는 게 당연하다. 결론부터 말하자면 quotient space는 기존에 있었던 topology를 "cut-and-paste"하는, 즉 "자르고 이어붙인" 위상공간에 해당한다.

위상수학이라는 학문은 대중적으로 "커피잔과 도넛이 같다"라는 재미난 사실을 다루는 분야로 알려져 있는 듯하다. 어떻게 커피잔과 도넛이 같은고 하니, 커피잔을 적당히 잘 "주물러서" 컵 손잡이 부분을 늘리고 잔 내부를 채워서 도넛으로 만들 수 있다는 것이다. 

![](assets/img/mugdonut.jpg)

비슷한 방법으로 직사각형 모양의 종이를 잘 "주물러서" 토러스 모양으로 만들 수 있다. 아래 사진에서 각 $a$ 선분을 이어붙여서 원통 모양으로 만들고, 원통의 양 끝을 이어붙이면 토러스가 된다. 

![](assets/img/rectorus.png)

직관적으로 이해는 될텐데, 수식으로 써보라고 하면 막막하다. 이때 강력한 도구가 되는게 바로 quotient space다.

**(i)** 간단한 예부터 시작해보자. $X = D^2 = \\{ (x, y) \in \mathbb{R}^2 \mid x^2 + y^2 \le 1 \\}$과 같이 closed disk를 하나 들고오고, $X$ 위에서의 동치 관계 $\sim$을 다음과 같이 정의하자. 

$$\begin{align*}
&(x_1, y_1) \sim (x_2, y_2), \text{ if } (x_1, y_1) = (x_2, y_2) \text{ or } (x_1, y_1), (x_2, y_2) \in \partial X
\end{align*}$$

그러니까 경계에 있는 점들은 모두 관계가 있다고 보고, 그 외 다른 점들은 자기 자신과 관계가 있도록 두는 것이다. 이렇게 정의하면 경계점들은 마치 어떤 한 점으로 수축되는 듯한 효과를 주게 된다. 그러면 $X$를 quotient map $p$로 매핑한 이미지를 생각해보면, 자연스럽게(?) $X$는 sphere $S^2 = \\{ (x, y, z) \in \mathbb{R}^2 \mid x^2 + y^2 + z^2 = 1 \\}$로 옮겨진다는 사실을 알 수 있다. 정확하게는 quotient space $X/\sim$은 $S^2$와 homeomorphic하다. 

![](assets/img/rectorus1.png)

**(ii)** 두 번째로 직사각형과 토러스를 다뤄보자. $X = [0, 1] \times [0, 1]$로 가져오고, $X$ 위에서의 동치 관계 $\sim$을 다음과 같이 정의하자. 

$$\begin{align*}
&(x_1, y_1) \sim (x_2, y_2), \text{ if } x_1 - y_1 \in \mathbb{Z} \text{ and } y_1 - y_2 \in \mathbb{Z}
\end{align*}$$

러프하게 말해서 $x, y \in [0, 1]$에 대해서 $(x, 0) \sim (x, 1)$이고, $(0, y) \sim (1, y)$으로 두고, 그 외 다른 점들은 자기 자신과 관계가 있다고 두는 것이다. 그러면 직관적으로(?) 위아래 선분이 평행하게 딱 들어맞고, 좌우의 선분 또한 딱 들어맞게 바뀌는 효과가 되고, $X$는 $p$에 의해 토러스로 매핑된다. 정확하게는 $X/\sim$은 토러스와 homeomorphic하다. 

![](assets/img/rectorus2.png)