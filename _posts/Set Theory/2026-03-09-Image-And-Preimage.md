---
title: Image and Preimage
date: 2026-03-09 00:01:29
categories: [Mathematics, Set Theory]
tags: []
math: true
---

## Definition
Let $f : X \to Y$ be a function, and let $A \subseteq X$ and $B \subseteq Y$, respectively. Then

**(i)** The ***image*** of $A$ under $f$, which we denote $f(A)$, is the set 

$$f(A) = \{ f(x) \in Y \mid x \in A \}.$$

**(ii)** The ***inverse image*** or ***preimage*** of $B$ under $f$, which we denote $f^{-1}(B)$, is the set 

$$f^{-1}(B) = \{ x \in X \mid f(x) \in B \}.$$

## Theorem 1
Let $f : X \to Y$ be a function. Then

**(i)** $f(\emptyset) = \emptyset$.

**(ii)** $f(\{x\}) = \{ f(x) \}, \forall x \in X$.

**(iii)** $A \subseteq B \subseteq X \Longrightarrow f(A) \subseteq f(B)$.

**(iv)** $C \subseteq D \subseteq Y \Longrightarrow f^{-1}(C) \subseteq f^{-1}(D)$.

### Proof
$\blacksquare$

## Theorem 2
Let $f : X \to Y$ be a function. Then 

**(i)** $\displaystyle f \left(\bigcup_{\gamma \in \Gamma} A_{\gamma}\right) = \bigcup_{\gamma \in \Gamma} f(A_{\gamma})$.

**(ii)** $\displaystyle f \left(\bigcap_{\gamma \in \Gamma} A_{\gamma}\right) \subset \bigcap_{\gamma \in \Gamma} f(A_{\gamma})$.

**(iii)** $\displaystyle f^{-1} \left(\bigcup_{\gamma \in \Gamma} B_{\gamma} \right) = \bigcup_{\gamma \in \Gamma} f^{-1}(B_{\gamma})$.

**(iv)** $\displaystyle f^{-1} \left(\bigcap_{\gamma \in \Gamma} B_{\gamma} \right) = \bigcap_{\gamma \in \Gamma} f^{-1}(B_{\gamma})$.

### Proof
$\blacksquare$

## Remark
Let $f : X \to Y$ be a function. Then

**(i)** $f$ is injective $\iff \vert f^{-1}(y) \vert \le 1, \forall y \in Y$.

**(ii)** $f$ is surjective $\iff \vert f^{-1}(y) \vert \ge 1, \forall y \in Y$.

**(iii)** $f$ is bijective $\iff \vert f^{-1}(y) \vert = 1, \forall y \in Y$.