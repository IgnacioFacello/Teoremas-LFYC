---
tags:
  - "#lfyc-c-I"
  - lfyc-c-IIX
---
> **Teorema 19** Si h es $\Sigma$*-[[paradigma-godel|recursiva]]* entonces es $\Sigma$*-[[paradigma-neumann|computable]]*
?

---
Probaremos por inducción en k que

($*$) Si $h\in\mathrm{R}_{k}^{\Sigma}$, entonces $h$ es $\Sigma$-computable.

El caso $k=0$ es fácil. Sea $k=0$ y $h\in R_{k}^{\Sigma}$, notar que
$$
\begin{aligned}
Succ&=\Psi_{N1\gets N1+1}^{1,0,\#} \\
Pred&=\Psi_{N1\gets N1\dot{-}1}^{1,0,\#} \\
C_{0}^{0,0}&=\Psi_{N1\gets0}^{0,0,\#} \\
C_{\varepsilon}^{0,0}&=\Psi_{P1\gets\varepsilon}^{0,0,*} \\
d_{a}&=\Psi_{P1\gets P1.a}^{0,1,*}\text{ para todo }a\in\Sigma \\
p_{j}^{n,m}&=\Psi_{N1\gets N\overline{j}}^{n,m,\#}\text{ si }j\in\left\{ 1,\dots,n\right\} \\
p_{j}^{n,m}&=\Psi_{P1\gets P\overline{j-n}}^{n,m,*}\text{ si }j\in\left\{ n+1,\dots,n+m\right\}
\end{aligned}
$$

---
Supongamos ($*$) vale para $k$, veremos que vale para $k+1$. 
Sea $h\in R_{k+1}^{\Sigma}-R_{k}^{\Sigma}$. Hay varios casos, pero solo vamos a probarlo para $h=M(P)$, con $P:\omega\times\omega^{n}\times\Sigma^{\ast m}\to\omega$ un predicado en ${R}_{k}^{\Sigma}$. 
Por Hipótesis Inductiva $P$ es $\Sigma$-computable y tenemos el macro
$$[IF\ P(V1,\dots, V\overline{n+1},W\bar1,\dots, W\overline{m})\ GOTO\ A1]$$
el cual podemos utilizar para definir el siguiente programa
$$
\begin{align}
L2\ & [IF\ P(N\overline{n+1},\dots, N\overline{n},P\bar1,\dots, P\overline{m})\ GOTO\ L1] \\
&N\overline{n+1}\gets N\overline{n+1} + 1 \\
&GOTO\ L2 \\
L1\ & N1\gets N\overline{n+1}
\end{align}
$$
el cual es fácil ver que computa $M(P)$.