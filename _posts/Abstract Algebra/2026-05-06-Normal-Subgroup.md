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

$(\because)$ Let $a \in G$. Then $ae = ea = a$, so $a\{e\} = \{a\} = \{e\}a$. Thus $\\{e\} \lhd G$. 

Let $a \in G$. Then for each $g \in G$, $a = a(a^{-1}g) \in aG$ and $a = (ga^{-1})a \in Ga$. Thus $aG = Ga$, which means that $G \lhd G$. 

---

## Theorem 1
Let $H \le G$. TFAE.

**(i)** $H \lhd G$

**(ii)** $gHg^{-1} \subset H, \forall g \in G$

**(iii)** $gHg^{-1} = H, \forall g \in G$

### Proof
**(i)** $\Longrightarrow$ **(ii)**

Suppose that $H \lhd G$. Let $g \in G$ and $h \in H$. Since $gH = Hg$, we have $gh = ag$ for some $a \in H$. Then we have $ghg^{-1} = a \in H$, so that $gHg^{-1} \subset H$.

**(ii)** $\Longrightarrow$ **(iii)**

Suppose that $gHg^{-1} \subset H, \forall g \in G$. Let $h \in H$. Since $g^{-1} \in G$, we have $g^{-1}Hg \subset H$. Then we have $g^{-1}hg = a$ for some $a \in H$. Thus, we have $h = gag^{-1} \in gHg^{-1}$, so that $H \subset gHg^{-1}$. Hence, $gHg^{-1} = H, \forall g \in G$.

**(iii)** $\Longrightarrow$ **(i)**

Suppose that $gHg^{-1} = H, \forall g \in G$. Let $g \in G$, and let $h \in H$. Then $ghg^{-1} = a$ for some $a \in H$, so that $gh = ag \in Hg$. Thus $gH \subset Hg$.

Let $h \in H$. Since $g^{-1}Hg = H$, we have $g^{-1}hg = b$ for some $b \in H$, so that $hg = gb \in gH$. Thus $Hg \subset gH$. Hence, $gH = Hg$, which means that $H \lhd G$. $\blacksquare$