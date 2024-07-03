---
tags:
  - lfyc-c-II
---
> **Lema 3** Supongamos $f_i:D_{f_i}\subseteq\omega^n\times\Sigma^{}*m\to\Sigma^*, i=1,\dots,k$ son funciones $\Sigma$-pr tales que $D_j\cap D_i=\emptyset$ para todo $i\neq j$. Entonces $\bigcup^k_{i=1} f_i$ es $\Sigma$-pr.
?

---
> Por inducción. Demostramos el caso con dos funciones y el resto de la demostración sale trivialmente
> Clave 1: Lemma 18 - Toda función no total es la restricción de alguna función total.
> Clave 2: Lemma 19 - El dominio de una función $\Sigma$-pr también es $\Sigma$-pr
> Paso 1 : $\lambda x\alpha \left[ \alpha^x\right]\circ\left[\chi^{\omega^n\times\Sigma^{*m}}_{D_{f}}, \bar f\right]$ devuelve palabra vacía fuera del dominio de $f$
> Paso 2 : Concatenamos el resultado de las $k$ funciones
> Paso 3 : Para el caso k+1 simplemente hacemos la union entre la union de las k anteriores y la k+1

Probamos por inducción.

---
Si $k=2$, por el [[guia5-lema18|lema de expansión]] tenemos que existen funciones $\Sigma$-pr $\bar f_1,\bar f_2:\omega^n\times\Sigma^{*m}\to\Sigma^*$ que son $\Sigma$-totales tales que:
$$
f_i=\bar f_i|_{D_{f_i}}\qquad i=1,2
$$
Por la [[guia5-lema19|caracterización básica de conjuntos pr]], tenemos que $D_{f_1},D_{f_2}$ sus dominios son $\Sigma$-pr y por lo tanto $D_{f_1}\cup D_{f_2}$ también lo será.
Definimos la union de las funciones como:
$$
\left.
f_1\cup f_2=\left( 
\lambda \alpha\beta \left[ \alpha\beta \right] \circ 
\left[
	\lambda x\alpha \left[ \alpha^x \right]\circ
	\left[
		\chi^{\omega^n\times\Sigma^{*m}}_{D_{f_1}}, \bar f_1
	\right]
	,
	\lambda x\alpha \left[ \alpha^x \right]\circ
	\left[
		\chi^{\omega^n\times\Sigma^{*m}}_{D_{f_2}}, \bar f_2
	\right]
\right]
\right)
\right|_{D_{f_1}\cup D_{f_2}}$$
que es $\Sigma$-pr.

---
Ahora supongamos que la hipótesis se cumple para el paso $k$ y veamos si se cumple para $k+1$ funciones.
Por hipótesis inductiva tenemos que $\bigcup^k_{i=1} f_i$ es $\Sigma$-pr, ademas tenemos la función $f_{k+1}$ $\Sigma$-pr.
Usando el mismo procedimiento anterior obtenemos que la función
$$
\bigcup^k_{i=1} f_i\cup f_{k+1}=\bigcup^{k+1}_{i=1} f_i
$$
es $\Sigma$-pr
$$\tag*{$\blacksquare$}$$