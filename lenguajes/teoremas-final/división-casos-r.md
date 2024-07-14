---
tags:
  - lfyc-c-IX
---
> **Lema 19** Supongamos $f_i:D_{f_i}\subseteq{\omega^n\times\Sigma^{*m}}\to{O}$, $i=i,\dots,k$ son funciones $\Sigma\text{-recursivas}$ tales que $D_{f_i}\cap{D_{f_j}}=\emptyset$ para $i\neq{j}$. Entonces la función $f_1\cup\dots\cup{f_k}$ es $\Sigma\text{-recursiva}$.
?

- - - 
> Usamos *Neuman v. Godel* para obtener los programas de las $f_i$
> $H_i$ se define en base a Halt  que es $\Sigma\cup\Sigma_p$-recursiva y por la *independencia del alfabeto* es $\Sigma$-recursiva
> Luego por el *lema de las macros*  tenemos macros para $H_i$ 
> Usamos los $H_i$ y los macros de las $f_i$, iterando en cantidad de pasos hasta que alguno de los dos programas terminen, en cuyo caso devolvemos el resultado apropiado

Haremos el caso $k=2$, $n=m=1$ y $O=\omega$ . Sean $f_i:D_{f_i}\subseteq{\omega\times\Sigma^{\ast}}\to{\omega}$ para $i\in\{1,2\}$ funciones $\Sigma\text{-recursivas}$ tales que $D_{f_1}\cap{D_{f_2}}=\emptyset$ . Entonces la función $f_1\cup{f_2}$ es $\Sigma\text{-recursiva}$.

Si $f_1,{f_2}$ son $\Sigma\text{-recursivas}$ entonces son $\Sigma\text{-computables}$ y sean $\mathcal{P}_1,\mathcal{P}_2$ los programas que computan a $f_1$ y ${f_2}$. Para $i=1,2$ definamos
$$
H_i=\lambda{tx_1\alpha_1}[\operatorname{Halt^{1,1}(t,x_1,\alpha_1,\mathcal{P}_{i})}]
$$
Notar que $D_{H_{i}}=\omega^{2}\times\Sigma^{\ast}$ y que $H_{i}$ es $\Sigma$-mixta. Además sabemos que la función $\operatorname{Halt^{1,1}}$ es $(\Sigma\cup\Sigma_{p})$-p.r. por lo cual resulta fácilmente que $H_{i}$ es $(\Sigma\cup\Sigma_{p})$-p.r. y por la *proposición de independencia del alfabeto* es $\Sigma$-p.r.. Entonces $H_{i}$ es $\Sigma$-computable y tenemos un macro
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
L1\ & N20\gets N20+1 \\
	& [IF\ \operatorname{Halt^{1,1}(N20,N1,P1,\mathcal{P}_{1})}\ GOTO\ L2] \\
	& [IF\ \operatorname{Halt^{1,1}(N20,N1,P1,\mathcal{P}_{2})}\ GOTO\ l3] \\
	& GOTO\ L1 \\
L2\ & [N1\gets{f_1(N1,P1)}] \\
	& GOTO\ L4\\
L3\ & [N1\gets{f_2(N1,P1)}] \\
L4\ & SKIP 
\end{aligned}
$$
Notar que $\mathcal{P}$ computa a la función $f_1\cup{f_2}$ por el*teorema Godel vence a Neumann*  es $\Sigma$-recursiva.

---
> Iteramos $t\in\omega$ hasta que alguno de los programas termine en t pasos y devolvemos el resultado. Si ninguno de los dos termina entonces la entrada se encuentra fuera de $D_{f_1}\cup{D_{f_2}}$  y el programa no termina nunca.
 > Claves:
 > 1. ${Halt}^{1,1}$ es $(\Sigma\cup\Sigma_{p})$-p.r.
 > 2. Tenemos programa y macros para cada función 
 