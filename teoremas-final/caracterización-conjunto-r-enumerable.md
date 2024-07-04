---
tags:
  - lfyc-c-VI
---
> Dado $S\subseteq\omega^n\times\Sigma^{*m}$, son equivalentes
> 	(1) $S$ es $\Sigma$-recursivamente enumerable
> 	(2) $S=I_F$ para alguna $F:D_F\subseteq\omega^k\times\Sigma^{\ast l}\to\omega^n\times\Sigma^{*m}$ tal que cada $F_{(i)}$ es $\Sigma$-r
> 	(3) $S=D_f$ para alguna función $\Sigma$-recursiva $f$

(Solo la prueba de $(2)\implies(3)$, $k=l=1$ y $n=m=2$)

---
($(2)\implies(3)$) Sean  $k=l=1$ y $n=m=2$. El caso general es completamente análogo.
> Partiendo de (2) $S=I_F$ para alguna $F:D_F\subseteq\omega\times\Sigma^{\ast}\to\omega^2\times\Sigma^{\ast 2}$ tal que cada $F_{(i)}$ es $\Sigma$-r
> Queremos llegar a (3) $S=D_f$ para alguna función $\Sigma$-recursiva $f$

Notar entonces que tenemos que $S\subseteq\omega^2\times\Sigma^{\ast 2}$ y $F:D_F\subseteq\omega\times\Sigma^{\ast}\to\omega^2\times\Sigma^{\ast 2}$ es tal que $I_F=S$ y $F_{(1)},F_{(2)},F_{(3)},F_{(4)}$ son $\Sigma$-recursivas. Para cada $i\in\{1,2,3,4\}$, sea $\mathcal{P}_i$ un programa el cual computa a $F_{(i)}$. Sea $\leq$ un orden sobre $\Sigma$. Definamos$$H_{i}=\lambda tx_1\alpha_1[\lnot\operatorname{Halt^{1,1}}(t,x_1,\alpha_1,\mathcal{P}_i)]$$
Notar que $D_{H_i}=\omega\times\omega\times\Sigma^{*}$ y que $H_i$ es $\Sigma$-mixta. Además, como ${Halt}^{1,1}$ es $(\Sigma\cup\Sigma_p)$-p.r., $H_i$ también lo es. Por la *proposición de independencia del alfabeto* tenemos que cada $H_i$ es $\Sigma$-p.r.
Entonces $H_i$ es $\Sigma$-computable y tenemos un macro $$[IF\ H_i(V2,V1,W1)\ GOTO\ A1]$$ que escribiremos cómo $$[IF\ \lnot\operatorname{Halt^{1,1}}(V2,V1,W1,,\mathcal{P}_i)\ GOTO\ A1]$$
 - - - 
Luego, definimos 
$$
\begin{align}
E_i &= \lambda{xtx_1\alpha_1}[x\neq E_{\#1}^{1,1}(t,x_1,\alpha_1,\mathcal{P}_i)] &i=1,2 \\
E_i &= \lambda{tx_1\alpha_1\alpha}[\alpha\neq E_{*1}^{1,1}(t,x_1,\alpha_1,\mathcal{P}_i)] &i=3,4
\end{align}
$$
tales que $$E_i=\lambda{xy}[x\neq y]\circ[p_1^{3,1},E_{\#1}^{1,1}\circ [p_2^{3,1},p_3^{3,1},p_4^{3,1},C_{\mathcal{P}_0}^{3,1}]]\quad i=1,2$$ y similar para $i=3,4$ claramente $\Sigma$-p.r. y por lo tanto $\Sigma$-computables y ademas tenemos macros
$$
\begin{align}
&[IF\ E_i(V2,V3,V1,W1)\ GOTO\ A1] &i=1,2 \\
&[IF\ E_i(V2,V1,W1,W2)\ GOTO\ A1] &i=3,4
\end{align}
$$
las cuales escribiremos de manera mas intuitiva como
$$
\begin{align}
&[IF\ V2\neq E_{\#1}^{1,1}(V3,V1,W1,\mathcal{P}_i)\ GOTO\ A1] &i=1,2 \\
&[IF\ W2\neq E_{*1}^{1,1}(V2,V1,W1,\mathcal{P}_i)\ GOTO\ A1] &i=3,4
\end{align}
$$
 - - -
SImilarmente, vamos a tomar las siguientes macros que existen por el *lema de las macros* para funciones $\Sigma$-p.r.
$$
\begin{align}
&[V2\gets(V1)_1]\\
&[V2\gets(V1)_2]\\
&[V2\gets\ast^{\leq}(V1)_3]
\end{align}
$$
 - - -
Sea $\mathcal{P}$ el siguiente programa
$$
\begin{align}
L1\ & N20\gets N20+1 \\
	& \left[ N10\gets(N20)_1 \right] \\
	& \left[N3\gets(N20)_2\right] \\
	& \left[P3\gets\ast^{\leq}(N20)_3 \right] \\
	& \left[IF\ \lnot{Halt}^{1,1}(N10,N3,P3,\mathcal{P}_{1})\ GOTO\ L1\right] \\
	& \left[IF\ \lnot{Halt}^{1,1}(N10,N3,P3,\mathcal{P}_{2})\ GOTO\ L1\right] \\
	& \left[IF\ \lnot{Halt}^{1,1}(N10,N3,P3,\mathcal{P}_{3})\ GOTO\ L1\right] \\
	& \left[IF\ \lnot{Halt}^{1,1}(N10,N3,P3,\mathcal{P}_{4})\ GOTO\ L1\right] \\
	& \left[IF\ N1\neq E_{\#1}^{1,1}(N10,N3,P3,\mathcal{P}_1)\ GOTO\ L1\right] \\
	& \left[IF\ N2\neq E_{\#1}^{1,1}(N10,N3,P3,\mathcal{P}_2)\ GOTO\ L1\right] \\
	& \left[IF\ P1\neq E_{*1}^{1,1}(N10,N3,P3,\mathcal{P}_3)\ GOTO\ L1\right] \\
	& \left[IF\ P2\neq E_{*1}^{1,1}(N10,N3,P3,\mathcal{P}_4)\ GOTO\ L1\right] \\
\end{align}
$$
que 