---
tags:
  - lfyc-c-IX
---
> Supongamos $f_i:D_{f_i}\subseteq{\omega^n\times\Sigma^{*m}}\to{O}$, $i=i,\dots,k$ son funciones $\Sigma\text{-recursivas}$ tales que $D_{f_i}\cap{D_{f_j}}=\emptyset$ para $i\neq{j}$. Entonces la función $f_1\cup\dots\cup{f_k}$ es $\Sigma\text{-recursiva}$.

- - -
Haremos el caso $k=2$, $n=m=1$ y $O=\omega$ . Sea $f_i:D_{f_i}\subseteq{\omega\times\Sigma^{\ast}}\to{\omega}$ para $i\in\{1,2\}$ tales que $D_{f_1}\cap{D_{f_2}}=\emptyset$ . Entonces la función $f_1\cup{f_2}$ es $\Sigma\text{-recursiva}$.
 - - -
Si $f_1,{f_2}$ son $\Sigma\text{-recursivas}$ entonces son $\Sigma\text{-computables}$ y sean $\mathcal{P}_1,\mathcal{P}_2$ los programas que computan a $f_1$ y ${f_2}$. Para $i=1,2$ definamos
$$
H_i=\lambda{tx_1\alpha_1}[\operatorname{Halt^{1,1}(t,x_1,\alpha_1,\mathcal{P}_{i})}]
$$
Notar que $D_{H_{i}}=\omega^{2}\times\Sigma^{\ast}$ y que $H_{i}$ es $\Sigma$-mixta. Ademas sabemops que la funcion \operatorname{Halt^{1,1}} es $(\Sigma\cup\Sigma_{p})$-p.r. por lo cual resulta facilmente que H_{i} es $(\Sigma\cup\Sigma_{p})$-p.r. y por el *lema de independencia del alfabeto* es $\Sigma$-p.r.. Entonces H_{i} es \Sigma-computable y tenemos un macro
$$
[IF\ H_i(V1,V2,W1)\ GOTO\ A1]
$$
El cual escribiremos de la siguiente manera para hacer su uso mas intuitivo
$$
[IF\ \operatorname{Halt^{1,1}(V1,V2,W1,\mathcal{P}_{i})}\ GOTO\ A1]
$$
 - - - 
Ya que cada $f_i$ es $\Sigma$-recursiva, por el *lema de las macros* tenemos las siguientes macros:
$$
\begin{aligned}
&[V2\gets{f_1(V1,W1)}] \\
&[V2\gets{f_2(V1,W1)}]
\end{aligned}
$$
 - - -
Sea $\mathcal{P}$ el siguiente programa
$$
\begin{aligned}
L1  & N20\gets N20+1
	&
\end{aligned}
$$