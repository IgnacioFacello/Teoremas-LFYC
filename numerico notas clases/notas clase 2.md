# Clase 2

#algoritmo de Horner para la evaluación de polinomios. 
Consiste en reescribir el polinomio a modo de reducir el numero de operaciones.
$$
\begin{align}
b_{n-1} &= a_n\\
b_{n-2} &= a_{n-1}+z*b_{n-1}\\
		&\vdots \\
b_0 &= a_1+z*b_1 \\
p(z) &= a_0+z*b_0
\end{align}
$$

Eficiencia: Si el grado de p es n, se requieren 

| Metodo              | Sumas |  Productos   |
| ------------------- | :---: | :----------: |
| $n-1$ productos     | $n-1$ | $n(n+1) / 2$ |
| Productos sucesivos |  ''   |    $2n-1$    |
| Horner              |  ''   |    $n-1$     |
Fuentes de error y aritmética de la computadora
estimar la precisión del resultado de un cálculo numérico
hay distintas fuentes de error, no todas pueden ser mitigadas
1. Errores en los datos de entrada
	- mediciones erroneas
	- numero irracional con numero finito de digitos
2. Errores de redondeo
	- Numero finito de digitos
3. Errores de truncamiento
	- procesos no infinitos 
4. Errores humanos
	- formulación
	- calculo manual
	- de código

> #definicion 1 Error Absoluto y Relativo
> Cuando un numero real $r$ (valor exacto) es aproximado por otro numero $\bar{r}$, se define el **error** como  $r-\bar{r}$. Llamaremos, respectivamente, a
> **Error Absoluto**: $\Delta{r}=|r-\bar{r}|$
> **Error relativo**: $\delta{r}=\left|{r-\bar{r}\over{r}}\right|={\Delta{r}\over{r}}$
> También se llama **error (relativo) porcentual** a $100*\delta{r}$

El relativo suele ser mas util
No se conocen los valores reales del error (ya que necesitaríamos saber el valor real) pero podemos dar cotas

redondeo cambia según el ultimo dígito, tiene error $\Delta{r}\leq\frac12{10^{-n}}$
y truncado solo corta el numero,  tiene error $\Delta{r}\leq{10^{-n}}$

> #definicion 2 Digitos significativos
> El numero $\bar r$ aproxima a $r$ con $m$ digitos significativos si $$\delta{r}\leq5*10^{-m}$$
> Esto nos dice que el error relativo es del orden $10^{-m}$

Errores en las operaciones
Suma $\Delta{(x_1+x_2)}\leq\Delta{x_1}+\Delta{x_2}$ 
Resta $\Delta{(x_1-x_2)}\leq\Delta{x_1}+\Delta{x_2}$ 
Multiplicación $\Delta{(x_1*x_2)}\leq|x_1|\Delta{x_1}+|x_2|\Delta{x_2}$ 
División $\Delta{(x_1/x_2)}\leq\frac1{|x_1|}\Delta{x_1}+\frac{|x_1|}{|x_2|}\Delta{x_2}$ 