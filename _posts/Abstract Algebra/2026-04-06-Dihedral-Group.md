---
title: Dihedral Group
date: 2026-04-06
categories: [Mathematics, Abstract Algebra]
tags: []
math: true
---

## Definition 1
Let $n \ge 3$ be a positive integer. Then the ***$n$-th dihedral group***, denoted by $D_n$, is defined as the group of symmetries of a regular $n$-gon.

---

## Example
**(i)** 예컨대 $D_3$을 고려해보자. 정의대로 생각하면 $D_3$는 정삼각형의 대칭성을 가지는 군인데, 예컨대 다음과 같이 각 꼭짓점에 번호를 붙인 정삼각형을 생각해보자. 

![alt text](assets/img/triangle.jpg)

삼각형의 무게중심을 축으로 반시계방향으로 회전시킨다고 할 때, 기존의 삼각형과 완전히 겹쳐지도록 하는 변환의 경우의 수는 총 3가지가 있다. 아예 회전시키지 않거나, $\frac{2\pi}{3}$만큼 회전시키거나, $\frac{4\pi}{3}$만큼 회전시키는 경우이다. 

반면 기존의 삼각형과 완전히 겹쳐지도록 하는 변환이 꼭 회전만 있는 건 아니다. 이등분선을 기준으로 뒤집어도 여전히 삼각형과 겹쳐지는데, 꼭짓점 1을 지나는 이등분선을 기준으로 뒤집는 경우, 꼭짓점 2를 지나는 이등분선을 기준으로 뒤집는 경우, 꼭짓점 3을 지나는 이등분선을 기준으로 뒤집는 경우가 있다. 따라서 정삼각형의 대칭성을 가지도록 바꿔주는 변환의 개수는 총 $6$개이고, 즉 $D_3$는 원소의 개수가 $6$개다. 

한편 꼭짓점에 매겨진 번호를 생각해보면 변환이란 각 번호를 다른 번호들로 바꿔주는 변환이다. 즉 일종의 순열로 생각할 수 있고, 각 순열을 나열해보면 다음과 같다.

$$ \begin{align*}
\rho_0 = \begin{pmatrix} 1 & 2 & 3 \\ 1 & 2 & 3 \end{pmatrix}, \quad 
\rho_1 = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 3 & 1 \end{pmatrix}, \quad 
\rho_2 = \begin{pmatrix} 1 & 2 & 3 \\ 3 & 1 & 2 \end{pmatrix}, \\
\mu_1 = \begin{pmatrix} 1 & 2 & 3 \\ 1 & 3 & 2 \end{pmatrix}, \quad 
\mu_2 = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 3 \end{pmatrix}, \quad 
\mu_3 = \begin{pmatrix} 1 & 2 & 3 \\ 3 & 2 & 1 \end{pmatrix}.
\end{align*}
$$

$\rho$는 회전, $\mu$는 반전이다. 즉 $D_3 = \\{ \rho_0, \rho_1, \rho_2, \mu_1, \mu_2, \mu_3 \\}$이고 이는 정확히 대칭군 $S_3$이다. 

(ii) 이번엔 $D_4$를 고려해보자. 정삼각형의 경우와 동일하게 정사각형도 회전과 반전을 통해 갖게 되는 대칭성이 존재한다. 꼭짓점에 번호를 붙여놓고 생각해보면, 회전은 총 $4$개 존재할 것이고 반전은 각 대각선을 축으로 뒤집는 경우 2개, 그리고 변의 중점을 지나는 직선을 축으로 뒤집는 경우 2개가 존재한다. 따라서 $D_4$는 원소의 개수가 $8$개이고 각 순열을 나열해보면 다음과 같다. 

$$ \begin{align*}
\rho_0 = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 1 & 2 & 3 & 4 \end{pmatrix}, \quad 
\rho_1 = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 2 & 3 & 4 & 1 \end{pmatrix}, \quad 
\rho_2 = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 3 & 4 & 1 & 2 \end{pmatrix}, \quad 
\rho_3 = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 4 & 1 & 2 & 3 \end{pmatrix}, \\
\mu_1 = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 2 & 1 & 4 & 3 \end{pmatrix}, \quad 
\mu_2 = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 4 & 3 & 2 & 1 \end{pmatrix}, \quad 
\delta_1 = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 3 & 2 & 1 & 4 \end{pmatrix}, \quad 
\delta_2 = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 1 & 4 & 3 & 2 \end{pmatrix}.
\end{align*}
$$

이때 $D_4 = \\{ \rho_0, \rho_1, \rho_2, \rho_3, \mu_1, \mu_2, \delta_1, \delta_2 \\}$는 자명하게 대칭군 $S_4$의 부분군이다. 한편 $D_4$의 table을 작성해보면 다음과 같다. 

$$\begin{array}{c|c|c|c|c|c|c|c|c}
       & \rho_0 & \rho_1 & \rho_2 & \rho_3 & \mu_1  & \mu_2  & \delta_1  & \delta_2  \\ \hline
\rho_0 & \rho_0 & \rho_1 & \rho_2 & \rho_3 & \mu_1  & \mu_2  & \delta_1  & \delta_2  \\ \hline
\rho_1 & \rho_1 & \rho_2 & \rho_3 & \rho_0 & \delta_2  & \mu_1  & \mu_3  & \delta_1  \\ \hline
\rho_2 & \rho_2 & \rho_3 & \rho_0 & \rho_1 & \mu_2  & \delta_2  & \delta_1  & \mu_1  \\ \hline
\rho_3 & \rho_3 & \rho_0 & \rho_1 & \rho_2 & \delta_1  & \mu_2  & \mu_1  & \delta_2  \\ \hline
\mu_1  & \mu_1  & \delta_1  & \mu_2  & \delta_2  & \rho_0 & \rho_1 & \rho_2 & \rho_3 \\ \hline
\mu_2  & \mu_2  & \mu_1  & \delta_2  & \delta_1  & \rho_3 & \rho_0 & \rho_1 & \rho_2 \\ \hline
\delta_1  & \delta_1  & \mu_3  & \delta_1  & \mu_1  & \rho_2 & \rho_3 & \rho_0 & \rho_1 \\ \hline
\delta_2  & \delta_2  & \delta_1  & \mu_1  & \mu_2  & \rho_1 & \rho_2 & \rho_3 & \rho_0
\end{array}$$

Subgroup diagram은 다음과 같다.

![alt text](assets/img/diagram.png)
