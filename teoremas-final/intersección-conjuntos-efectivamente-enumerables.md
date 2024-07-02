---
tags:
  - lfyc-c-V
  - "#review"
---
> Sean $S_1,S_2\subseteq\omega^n\times\Sigma^{*m}$ conjuntos $\Sigma$-efectivamente enumerables. Entonces $S_1\cap S_2$ es $\Sigma$-efectivamente enumerable 

---
> Suponemos que existe al menos un elemento $e_0$ en la intersección
> Generamos un elemento $(x_1,x_2)\in\omega^2$ y usamos sus coordenadas para generar valores de ambos conjuntos $(e_1,e_2)$
> Si ambos elementos son iguales (es decir que pertenece a ambos conjuntos) devolvemos alguno de los dos
> caso contrario devolvemos $e_0$ 

El caso $S_1\cap S_2=\emptyset$ es trivial.
Supongamos $S_1\cap S_2\neq\emptyset$ y sea $e_0\in S_1\cap S_2$.
Sea $\mathbb P$ un procedimiento efectivo el cual enumera a $\omega\times\omega$ y $\mathbb P_1,\mathbb P_2$ los procedimientos que enumeran a $S_1$ y $S_2$ respectivamente
El siguiente procedimiento claramente enumera $S_1\cap S_2$:
$$
\begin{align}
&Etapa 1:\\
	&\qquad\text{Realizar }\mathbb P\text{ con x como dato de entrada, obteniendo un par } (x_1,x_2)\in\omega\times\omega
	\\
&Etapa 2:\\
	&\qquad\text{Realizar } \mathbb P_1 \text{ con el valor }x_1 \text{ como entrada, obteniendo como salida un elemento }e_1\in S_1.
	\\
&Etapa 3:\\
	&\qquad\text{Realizar } \mathbb P_2 \text{ con el valor }x_2 \text{ como entrada, obteniendo como salida un elemento }e_2\in S_2. \\
&Etapa 4:\\
	&\qquad\text{Si } e_1=e_2 \text{ entonces detenerse y devolver}e_1 \\
	&\qquad \text{Caso contrario, devolver }e_0
	\\
\end{align}
$$

> Hasta la etapa 3 se enumera $S_1\times S_2$ 
> En la etapa 4 filtramos los elementos $(e,e)\in S_1\times S_2$, es decir $e\in S_1\cap S_2$.
> Para $(e_1,e_2)\in S_1\times S_2$ con $e_1\neq e_2$ devolvemos $e_0\in S_1\cap S_2$ que sabemos que existe.
