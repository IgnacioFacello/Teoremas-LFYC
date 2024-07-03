---
tags:
  - lfyc-c-III
  - "#review"
  - flashcards
---
> **Teorema 6** Sean $S\subseteq\omega^n\times\Sigma^{*m}$. Son equivalentes:
> (a) $S$ es $\Sigma$-efectivamente computable
>	(Es decir) Hay un procedimiento que computa a $\chi^{\omega^n\times\Sigma^{*m}}_S$
>  (b) $S$ y $\omega^n\times\Sigma^{*m}-S$ $\Sigma$-efectivamente enumerables
?

(Solo caso $(b)\implies (a)$)
 - - -  
$S$ $\Sigma$-e.computable $\implies$$S$ y $\bar S$ $\Sigma$-e.enumerable
> Suponemos que podemos generar $S$ y $S^{-1}$
> Dado un $(\vec x,\vec\alpha)$ de consulta vamos a realizar un ciclo finito, ya que eventualmente se cumple la condición
> En cada paso generamos valores de ambos conjuntos, y si alguno de los valores generados es el valor de consulta devolvemos 0 o 1 según cual de los generados coincida

Si $S=\emptyset$ o $S = \omega^n\times\Sigma^{*m}$ entonces es trivial, por lo tanto suponemos $S\subset\omega^n\times\Sigma^{*m}$ **no vacío**.
Sea
- $\mathbb P_1$ un procedimiento efectivo que enumera a $S$ y
- $\mathbb P_2$ un procedimiento efectivo que enumera a $\omega^n\times\Sigma^{*m}-S$ }. 

Es fácil ver que el siguiente procedimiento computa al predicado $\chi^{\omega^n\times\Sigma^{*m}}_S$.
$$
\begin{align}
&Etapa 1:\\
	&\qquad\text{Asignar a la variable T el valor 0}
	\\
&Etapa 2:\\
	&\qquad\text{Realizar } \mathbb P_1 \text{ con el valor de T como entrada, obteniendo como salida la upla } (\vec y,\vec\beta).
	\\
&Etapa 3:\\
	&\qquad\text{Realizar } \mathbb P_2 \text{ con el valor de T como entrada, obteniendo como salida la upla } (\vec z,\vec\gamma).
	\\
&Etapa 4:\\
	&\qquad\text{Si } (\vec y,\vec\beta)=(\vec x,\vec\alpha) \text{ detenerse y devolver 0.} \\
	&\qquad\text{Si } (\vec z,\vec\gamma)=(\vec x,\vec\alpha) \text{ detenerse y devolver 1.} \\ 
	&\qquad \text{Caso contrario, aumentar T en 1 e ir a la etapa 2}
	\\
\end{align}
$$

$$\tag*{$\blacksquare$}$$
 