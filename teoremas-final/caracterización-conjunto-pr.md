---
tags:
  - "#lfyc-c-I"
---
> Un conjunto S es $\Sigma$-pr $\iff$ es el dominio de alguna función $\Sigma$-pr. (Solo caso composición)

---
## Todo $S$ $\Sigma$-pr es dominio de $\Sigma$-pr
> Predecesor de la característica. Solo va a estar definido para retorno 1.


($\implies$) Tomemos la función $F=Pred\circ\chi^{\omega\times\Sigma^*}_S$. Claramente $D_F=S$.
($\impliedby$)  Probaremos por inducción en k que $Dom(F)$ es $\Sigma$-pr para cada $F\in PR^{\Sigma}_k$
El caso $k=0$ es trivial. Supongamos ahora que el resultado vale para un $k$ fijo y que $F\in{PR}^{\Sigma}_{k+1}$ . Para esta proposición solo se pide el caso de la composición.

> Buscamos definir la característica de la composición en base a los dominios de las funciones.
> Clave 0: Por hipótesis todas las funciones y sus dominios van a ser $\Sigma$-pr. 
> Clave 1: Toda función $f$ $\Sigma$-pr no total es la restricción de otra $\bar f$ $\Sigma$-total 
> Clave 2: Definimos el conjunto S $\Sigma$-pr como la intersección de los dominios. Es decir que tenemos su característica.
> Usamos las claves para definir la función $\chi_{D_F}^{\omega^n\times\Sigma^{*m}}=\chi_{D_g}^{\omega^n\times\Sigma^{*m}}\circ[\bar g_1,\dots,\bar g_{n+m}]\land\chi_{S}^{\omega^n\times\Sigma^{*m}}$

(Para esta proposición solo se pide el caso de las composición)

Sea $F=g\circ[g_1,\dots,g_n,g_{n+1}\dots,g_{n+m}]$ con $g,g_1,\dots,g_{n+m}\in PR^{\Sigma}_k$.
Luego tenemos que, para $l,k,n,m\ge 0$
 $$
 \begin{align}
 g &:D_g\subseteq\omega^n\times\Sigma^{*m}\to O,\ O\in\{\omega,\Sigma^*\} \\
 g_i &:D_{g_i}\subseteq\omega^l\times\Sigma^{*k}\to\omega\ ,\ i=1,\dots,n \\
 g_i &:D_{g_i}\subseteq\omega^l\times\Sigma^{*k}\to\Sigma^*\ ,\ i=n+1,\dots,n+m \\
 \end{align}
 $$ 
Si $F=\emptyset$ entonces $D_F=\emptyset$ y claramente es $\Sigma$-pr.
Caso contrario...

Por [[guia5-lemma18|lema 18]] tenemos que hay funciones $\Sigma$-pr $\bar g_1,\dots,\bar g_{n+m}$ que son $\Sigma$-totales tales que:
$$g_i=\bar g_i|_{D_{g_i}}\ para\ i=1,\dots,n+m$$
Luego, por Hipótesis Inductiva tenemos que los conjuntos $D_g,\ D_{g_i}\ i=1,\dots, n+m$ son $\Sigma$-pr y por lo tanto
$$
S=\bigcap^{n+m}_{i=1} D_{g_i}
$$
Por lo tanto S también es lo es.
Finalmente notar que
$$
\chi_{D_F}^{\omega^n\times\Sigma^{*m}}=
\chi_{D_g}^{\omega^n\times\Sigma^{*m}}\circ
[\bar g_1,\dots,\bar g_{n+m}]\land
\chi_{S}^{\omega^n\times\Sigma^{*m}}
$$
