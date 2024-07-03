---
tags:
  - "#lfyc-c-I"
  - "#review"
  - flashcards
---
> **Proposición 1** Un conjunto S es $\Sigma$-pr $\iff$ es el dominio de alguna función $\Sigma$-pr. (Solo caso composición)
?

---
($\implies$) Tomemos la función $F=Pred\circ\chi^{\omega\times\Sigma^*}_S$. Claramente $D_F=S$.
> Predecesor de la característica. Solo va a estar definido para retorno 1.

($\impliedby$)  Probaremos por inducción en k que $Dom(F)$ es $\Sigma$-pr para cada $F\in PR^{\Sigma}_k$
El caso $k=0$ es trivial. Supongamos ahora que el resultado vale para un $k$ fijo y que $F\in{PR}^{\Sigma}_{k+1}$ . Para esta proposición solo se pide el caso de la composición.

> Buscamos definir la característica de la composición en base a los dominios de las funciones.
> Clave 0: Por hipótesis todas las funciones y sus dominios van a ser $\Sigma$-pr. 
> Clave 1: Toda función $f$ $\Sigma$-pr no total es la restricción de otra $\bar f$ $\Sigma$-total 
> Clave 2: Definimos el conjunto S $\Sigma$-pr como la intersección de los dominios. Es decir que tenemos su característica.
> Usamos las claves para definir la función $\chi_{D_F}^{\omega^n\times\Sigma^{*m}}=\chi_{D_g}^{\omega^n\times\Sigma^{*m}}\circ[\bar g_1,\dots,\bar g_{n+m}]\land\chi_{S}^{\omega^n\times\Sigma^{*m}}$

Sea $F=g\circ[g_1,\dots,g_{r}]$ con $g,g_1,\dots,g_{r}\in PR^{\Sigma}_k$. Si $F=\emptyset$ entonces es claro que $D_F=\emptyset$ es $\Sigma$-pr. Supongamos entonces que $F\neq\emptyset$. Tenemos entonces que $r=n+m$ y 
$$
\begin{aligned}
g:&
	D_{g}\subseteq\omega^{n}\times\Sigma^{*m}
	\to O\\
g_{i}:&
	D_{g_{i}}\subseteq\omega^{k}\times\Sigma^{*l}
	\to\omega,\ i=1,\dots,n\\
g_{i}:&
	D_{g_{i}}\subseteq\omega^{k}\times\Sigma^{*l}
	\to\Sigma^{*},\ i=n+1,\dots,n+m
\end{aligned}
 $$
con $O\in\{\omega,\Sigma^*\}$ y $k,l\in\omega$. 
> Notar que 
> $$D_F=\{(\vec x, \vec\alpha)\in D_{g_1}\cup\dots\cup D_{g_{n+m}}:[g_1,\dots,g_{n+m}](\vec x, \vec\alpha)\in D_g\}$$

---
Por Hipótesis Inductiva tenemos que los conjuntos $D_g,\ D_{g_i}$ para $i=1,\dots, n+m$ son $\Sigma$-pr y por lo tanto
$$
S=\bigcap^{n+m}_{i=1} D_{g_i}
$$
lo es.
> $$D_F=\{(\vec x, \vec\alpha)\in S:[g_1,\dots,g_{n+m}](\vec x, \vec\alpha)\in D_g\}$$

---
> Necesitamos que los dominios de las g sean totales

Luego, por el [[guia5-lemma18|lema de expansión]] hay funciones $\Sigma$-pr $\bar g_1,\dots,\bar g_{n+m}$ las cuales son $\Sigma$-totales y cumplen
$$
g_i=\bar g_i|_{D_{g_i}}\text{ para }i=1,\dots,n+m
$$

---
Finalmente notar que
$$
\chi_{D_{F}}^{\omega^{k}\times\Sigma^{*l}}= \left(
	\chi_{D_{g}}^{\omega^{n}\times\Sigma^{*m}}\circ [\bar{g}_{1},\dots,\bar{g}_{n+m}]
	\land\chi_{S}^{\omega^{k}\times\Sigma^{*l}}
\right)
$$
lo cual nos dice que $D_{F}$ es $\Sigma$-p.r.. 