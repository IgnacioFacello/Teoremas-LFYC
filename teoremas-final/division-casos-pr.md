---
tags:
  - lfyc-c-II
---
> Supongamos $f_i:D_{f_i}\subseteq\omega^n\times\Sigma^{}*m\to\Sigma^*, i=1,\dots,k$ son funciones $\Sigma$-pr tales que $D_j\cap D_i=\emptyset$ para todo $i\neq j$. Entonces $\bigcup^k_{i=1} f_i$ es $\Sigma$-pr.

---

Probamos por inducción.
### (Caso k=2)
Por el lema 18 tenemos que existen funciones $\Sigma$-pr $\bar f_1,\bar f_2:\omega^n\times\Sigma^{*m}\to\Sigma^*$ que son $\Sigma$-totales tales que:
$$
f_i=\bar f_i|_{D_{f_i}}\qquad i=1,2
$$
Por el lema 19 (Caracterización básica de conjuntos pr), tenemos que $D_{f_1},D_{f_2}$ sus dominios son $\Sigma$-pr y por lo tanto su union también lo será.
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
### (Caso k + 1 > 2)
Por hipótesis inductiva tenemos que $\bigcup^k_{i=1} f_i$ es $\Sigma$-pr, ademas tenemos la función $f_{k+1}$ $\Sigma$-pr.
Usando el mismo procedimiento anterior obtenemos que la función
$$
\bigcup^k_{i=1} f_i\cup f_{k+1}=\bigcup^{k+1}_{i=1} f_i
$$
es $\Sigma$-pr
$$\tag*{$\blacksquare$}$$