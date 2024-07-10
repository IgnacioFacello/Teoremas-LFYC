[[notas clase 1]]
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
