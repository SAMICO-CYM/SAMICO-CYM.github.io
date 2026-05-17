--- 
title: Normal Subgroup
date: 2026-05-06
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Definition
Let $H$ be a subgroup of a group $G$. Then $H$ is called a ***normal subgroup*** of $G$ if $aH = Ha$ for all $a \in G$. If $H$ is normal in $G$, then we denoted by $H \lhd G$. 

---

## Remark
**(i)** Let $\phi: G \to G'$ be a group homomorphism. Then $\ker(\phi) \lhd G$.

**(ii)** Every subgroup of an abelian group is normal.

$(\because)$ Let $G$ be an abelian group and $H \le G$. Let $a \in G$. Then $ah = ha, \forall h \in H$, which means that $aH = Ha$. Thus $H \lhd G$.

**(iii)** Every group has trivial normal subgroups $\\{ e\\}$ and $G$.

$(\because)$ Let $a \in G$. Then $ae = ea = a$, so $a\{e\} = \{a\} = \{e\}a$. Thus $\\{e\\} \lhd G$. 

Let $a \in G$. Then for each $g \in G$, $a = a(a^{-1}g) \in aG$ and $a = (ga^{-1})a \in Ga$. Thus $aG = Ga$, which means that $G \lhd G$. 

---

## Theorem 1
Let $H \le G$. TFAE.

**(i)** $H \lhd G$

**(ii)** $gHg^{-1} \subset H, \forall g \in G$

**(iii)** $gHg^{-1} = H, \forall g \in G$

결국 normal group에 한해서, 집합 양 옆에 곱해져있는 원소들을 마치 원소를 연산하듯이 처리해도 된다는 결론을 얻는다.

### Proof
**(i)** $\Longrightarrow$ **(ii)**

Suppose that $H \lhd G$. Let $g \in G$ and $h \in H$. Since $gH = Hg$, we have $gh = ag$ for some $a \in H$. Then we have $ghg^{-1} = a \in H$, so that $gHg^{-1} \subset H$.

**(ii)** $\Longrightarrow$ **(iii)**

Suppose that $gHg^{-1} \subset H, \forall g \in G$. Let $h \in H$. Since $g^{-1} \in G$, we have $g^{-1}Hg \subset H$. Then we have $g^{-1}hg = a$ for some $a \in H$. Thus, we have $h = gag^{-1} \in gHg^{-1}$, so that $H \subset gHg^{-1}$. Hence, $gHg^{-1} = H, \forall g \in G$.

**(iii)** $\Longrightarrow$ **(i)**

Suppose that $gHg^{-1} = H, \forall g \in G$. Let $g \in G$, and let $h \in H$. Then $ghg^{-1} = a$ for some $a \in H$, so that $gh = ag \in Hg$. Thus $gH \subset Hg$.

Let $h \in H$. Since $g^{-1}Hg = H$, we have $g^{-1}hg = b$ for some $b \in H$, so that $hg = gb \in gH$. Thus $Hg \subset gH$. Hence, $gH = Hg$, which means that $H \lhd G$. $\blacksquare$

---
## Theorem 2
An intersection of normal subgroups of a group $G$ is again a normal subgroup of $G$.

### Proof
Let $\{ H_i \lhd G \mid i \in I\}$ be a collection of normal subgroups of $G$, where $I$ is an index set. By [Theorem 2](<{% post_url Abstract Algebra/2026-03-18-Subgroup %}#theorem-2>), $\bigcap_{i \in I}  H_i \le G$. By Theorem 1, we have that $gH_ig^{-1} \subset H_i, \forall g \in G$, for each $i \in I$. 

Denote 

$$H := \bigcap_{i \in I}H_i.$$

We will show that $gHg^{-1} \subset H, \forall g \in G,$ which is equivalent to $H \lhd G$. 

Fix $g \in G$, and let $x \in gHg^{-1}$. Then $x = gyg^{-1}$ for some $y \in H$. Since $y \in H_i, \forall i \in I$, $gyg^{-1} \in gH_ig^{-1} \subset H_i, \forall i \in I$ by Theorem 1, which means that $gyg^{-1} \in H$. Thus, we have $x = gyg^{-1} \in H$, and therefore $gHg^{-1} \subset H$. By Theorem 1, $H \lhd G$. $\blacksquare$

---
## Remark
A union of normal subgroups of a group need NOT be a normal subgroup.

$(\because)$ Consider the Klein-$4$ group $V = \\{e, a, b, c \\}$. Since $V$ is abelian, $\\{ e, a \\}$ and $\\{ e, b \\}$ are normal subgroups of $V$. But $\\{ e, a\\} \cup \\{ e, b \\} = \\{ e, a, b \\}$ is not closed under the operation of $V$ because $ab = c$. Thus, $\\{ e, a\\} \cup \\{ e, b \\} = \\{ e, a, b \\}$ is not a subgroup of $G$, so is not a normal subgroup of $G$.
