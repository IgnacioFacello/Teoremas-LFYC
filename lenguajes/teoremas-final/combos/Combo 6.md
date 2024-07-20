---
tags:
  - flashcards
---
11. [[e-computable-implica-e-enumerable|Lema 11]] Si $S\subseteq\omega^n\times\Sigma^{*m}$ es $\Sigma$-efectivamente computable entonces $S$ es $\Sigma$-efectivamente enumerable
12. [[caracterización-conjunto-r-enumerable|Lema 12]] Dado $S\subseteq\omega^n\times\Sigma^{*m}$, son equivalentes
	 	(1) $S$ es $\Sigma$-recursivamente enumerable
	 	(2) $S=I_F$ para alguna $F:D_F\subseteq\omega^k\times\Sigma^{\ast l}\to\omega^n\times\Sigma^{*m}$ tal que cada $F_{(i)}$ es $\Sigma$-r
	 	(3) $S=D_f$ para alguna función $\Sigma$-recursiva $f$
 	(Solo la prueba de $(2)\implies(3)$, $k=l=1$ y $n=m=2$)
?
11. Suponemos no vacío, generamos todo el espacio y devolvemos usamos la característica para determinar si devolvemos lo generado o $e_0$ si lo generado no pertenece
12. $F_{(i)}$ $\Sigma$-r implica que hay programas $\mathcal{P}_i$. Definimos macros $[IF\ \lnot\operatorname{Halt^{1,1}}(V2,V1,W1,,\mathcal{P}_i)\ GOTO\ A1]$ y $[IF\ V2\neq E_{\#1}^{1,1}(V3,V1,W1,\mathcal{P}_i)\ GOTO\ A1]$. Finalmente damos un programa que toma un elemento $(x_1,x_2,\alpha_1,\alpha_2)$ que itera luego en $\omega$, generando elementos $(y_1,\beta_1)$ y un numero de pasos $t$ hasta que todas las $F_{(i)}$ terminan y retornan $(x_1,x_2,\alpha_1,\alpha_2)$. Este programa computa $p_1^{2,2}|_S$ que es $\Sigma$-computable y por lo tanto $\Sigma$-recursiva con dominio $S$.
<!--SR:!2024-07-21,1,190-->