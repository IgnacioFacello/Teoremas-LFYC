# Clase 6 (Incompleto)
Método de la secante
Variación del método de Newton
Evita la evaluación de la derivada para cada iteración
Reemplazamos la derivada por una aproximación dada por el cociente incremental, dado por la pendiente de la recta secante que pasa por los puntos $(x_n,f(x_n))$ y $(x_n+h,f(x_n+h))$:
$$
f´(x_n)\approx {a_n}={ f(x_n+h) - f(x_n) \over h} 
$$
para algún h suficientemente pequeño. Tomamos $h=x_{n-1}-x_n$

Iteración de punto fijo
> #definicion 1 Punto fijo de una función
> Un punto fijo de una función $g$ es un numero $p$, en el dominio de $g$, tal que $g(p)=p$

Si tomamos $p$ raíz de $f$, podemos definir multiples funciones con punto fijo $p$  

> #teorema 1 Existencia y Unicidad de un punto fijo
> 1. (**EXISTENCIA**) 
> 2. (**UNICIDAD**)

El algoritmo se basa en la serie de aproximaciones $p_n=g(p_{n-1})$ 

> #teorema 2 Convergencia del método de punto fijo
> Suponiendo que se dan las condiciones de *existencia*  y *unicidad*, entonces para cualquier $p_0\in[a,b]$ la sucesión definida por $p_n=g(p_{n-1})$, para todo $n\geq 0$ converge al único punto fijo $p\in(a,b)$

> #corolario 1 Cota de error
> 	Dado que se cumplen las condiciones del teorema de convergencia, tenemos las siguientes cotas de error para el método $$\Delta p_n \leq k^n\max\left\{p_0-a,b-p_0\right\}$$ $$\Delta p_n\leq \frac{k^n}{1-k}|p_1-p_0|$$

