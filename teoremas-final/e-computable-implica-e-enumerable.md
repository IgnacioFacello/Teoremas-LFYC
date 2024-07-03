---
tags:
  - lfyc-c-VI
  - review
  - flashcards
---
> ** Si $S\subseteq\omega^n\times\Sigma^{*m}$ es $\Sigma$-efectivamente computable entonces $S$ es $\Sigma$-efectivamente enumerable
?

---
> Suponemos que $S\neq\emptyset$ y que $e_0\in S$
> Generamos  $\omega^n\times\Sigma^{*m}$ y devolvemos el valor generado si pertenece a S, caso contrario devolvemos $e_0$

Suponemos que $S\neq\emptyset$ ya que el caso vacío es trivial y además que $e_0\in S$.
Sea $\mathbb P$ el procedimiento que enumera a $\omega^n\times\Sigma^{*m}$ y $\mathbb P_S$ el procedimiento que efectivamente computa $\chi_S^{\omega^n\times\Sigma^{*m}}$. 
Entonces el siguiente procedimiento enumera $S$. Se toma $x\in\omega$ de entrada
$$
\begin{align}
&Etapa 1:\\
	&\qquad\text{Realizar } \mathbb P \text{ con el valor de x de entrada, obteniendo como salida la upla } (\vec y,\vec\beta).
	\\
&Etapa 2:\\
	&\qquad\text{Realizar } \mathbb P_S \text{ con } (\vec y,\vec\beta) \text{ como entrada. Si retorna 1 detenerse y retornar }(\vec y,\vec\beta) \text{. Caso contrario ir a 3}.
	\\
&Etapa 3:\\
	&\qquad\text{Detenerse y retornar } e_0 
	\\
\end{align}
$$