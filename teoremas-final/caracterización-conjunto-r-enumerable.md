---
tags:
  - lfyc-c-VI
---
z> Dado $S\subseteq\omega^n\times\Sigma^{*m}$, son equivalentes
> (1) $S$ es $\Sigma$-recursivamente enumerable
> (2) $S=I_F$ para alguna $F:D_F\subseteq\omega^k\times\Sigma^{\ast l}\to\omega^n\times\Sigma^{*m}$ tal que cada $F_{(i)}$ es $\Sigma$-r
> (3) $S=D_f$ para alguna función $\Sigma$-recursiva $f$

(Solo la prueba de $(2)\implies(3)$, $k=l=1$ y $n=m=2$)

---
($(2)\implies(3)$) caso  $k=l=1$ y $n=m=2$. El caso general es completamente análogo.
> Partiendo de (2) $S=I_F$ para alguna $F:D_F\subseteq\omega\times\Sigma^{\ast}\to\omega^2\times\Sigma^{\ast 2}$ tal que cada $F_{(i)}$ es $\Sigma$-r
> Queremos llegar a (3) $S=D_f$ para alguna función $\Sigma$-recursiva $f$

Note entonces que tenemos que $S\subseteq\omega^2\times\Sigma^{\ast 2}$ y $F:D_F\subseteq\omega\times\Sigma^{\ast}\to\omega^2\times\Sigma^{\ast 2}$ es tal que $I_F=S$ y $F_{(1)},F_{(2)},F_{(3)},F_{(4)}$ son $\Sigma$-recursivas. Para cada $i\in\{1,2,3,4\}$, sea $\mathcal{P}_i$ un programa el cual computa a $F_{(i)}$. Sea $\leq$ un orden sobre $\Sigma$. Definamos
$$
H_{i}=\lambda tx_1\alpha_1[\lnot\operatorname{Halt^{1,1}}(t,x_1,\alpha_1,\mathcal{P}_i)]
$$
