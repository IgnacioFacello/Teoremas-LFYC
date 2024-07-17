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
11. Suponemos no vacío, generamos todo el espacio y devolvemos usamos la caracteristica para determinar si devolvemos lo generado o $e_0$ si lo generado no pertenece
12. Definimos programas para las coordenadas de F y la macro que define si dichos programas NO terminan. Luego usamos $E_{\#}$ y $E_{*}$ para definir macros del predicado "El elemento es diferente a la salida del programa". Luego tenemos un programa toma un elemento $(x_1,x_2,\alpha_1,alpha_2)$ que itera luego en $\omega$, generando un elementos $(y_1,\beta_1)$ y un numero de pasos $t$
<!--SR:!2024-07-16,1,230-->