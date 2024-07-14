[[notas clase 1]]
[[notas clase 2]]
[[notas clase 3]]
# Clase 4
Problema: Hallar la raíz de una función no lineal

Método de bisección
Basado en teorema de valor intermedio
Si $f(a)f(b)\lt0$ entonce $f$ tiene una raíz en $[a,b]$ 
Se calcula $c=\frac{a+b}{2}$ y $f(c)$ 
- Si $f(a)f(c)\lt0$ buscamos la raíz en $[a,c]$
- Si $f(c)f(b)\lt0$ buscamos la raíz en $[c,b]$ 
- Si $f(c)=0$ entonces $c$ es una raíz

Recomendaciones a la hora de implementar el algoritmo
Algoritmo de bisección
Observaciones

> #teorema 1 convergencia del método de la bisección
> Si $[a_0,b_0],[a_1,b_1],\dots,[a_n,b_n],\dots$ denotan los sucesivos intervalos en el método de bisección , entonces existen los limites $\lim\limits_{n\to\infty}a_n$ y $\lim\limits_{n\to\infty}b_n$, son iguales y representan una raíz de $f$. Si $c_n=\frac{a_n+b_n}2$ y $r=\lim\limits_{n\to\infty}c_n$ entonces $$\Delta{c_n}=\frac{b_0-a_0}{2^{n+1}}$$

# Clase 5
Método de Newton
Resolución de una serie de problemas simples que convergen en la solución real
Comenzando con una aproximación $x_0$ tenemos la serie
$$x_{n+1}=x_n-\frac{f(x_n)}{f'(x_n)}$$
Este método requiere una cierta cercanía a la raíz para asegurar la convergencia
Algoritmo

Análisis de errores

> #teorema 1 Convergencia del método de newton
> Si $f''$ es 

# Clase 6
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

