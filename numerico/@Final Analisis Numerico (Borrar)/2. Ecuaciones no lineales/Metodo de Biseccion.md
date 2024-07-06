# Iteración
Consiste en utilizar las conclusiones del [[Limite#Teorema del valor intermedio|teorema del valor intermedio]] para encontrar una raíz de $f$ a partir de un intervalo $[a,b]$ en el que se cumplan las hipótesis del teorema.
Sea:
- $f\in C[a,b]$
- $f(a)*f(b)<0$ ($f(a)$ y $f(b)$ tienen signo distinto)

El método consiste en una dividir el intervalo a la mitad y aplicar la segunda hipótesis de nuevo para encontrar en que mitad se encuentra la raíz. Para eso usamos la sucesión
$$c_{n+1}=\frac{b_n-a_n}2$$
con $$a_{n+1}=\left\{\begin{array}{ll}
c_n & \text{si}\ f(c_n)*f(a_n) < 0\\
a_n & \text{si}\ f(c_n)*f(a_n) > 0
\end{array}\right.$$
$$b_{n+1}=\left\{\begin{array}{ll}
c_n & \text{si}\ f(c_n)*f(b_n) < 0\\
b_n & \text{si}\ f(c_n)*f(b_n) > 0
\end{array}\right.$$
Si $f(a)*f(b)=0$ entonces $a$, o $b$ es una raíz y el algoritmo termina.

==Si se cumplen las hipótesis se asegura la convergencia==

# Error
Sea $[a_i,b_i]\ i = 0, 1, \dots, n$ el intervalo generado por el método de bisección para la iteración $i$, entonces existen los límites: $\lim_{i\to\infty}a_i$ y $\lim_{i\to\infty}b_i$ que son iguales y representan una raíz $r$ de $f$. Si $c_n=\frac12(a_i+b_i)$ y $r=\lim_{i\to\infty}c_i$, entonces 
$$\bbox[10px,border:0.5px solid red]{|r-c_n|\leq\frac1{2^{n+1}}(b_0-a_0)}$$

# Teoremas
- Teorema 1 : Si $[a_0,b_0],\dots,[a_n,b_n],\dots$ denotan los sucesivos intervalos en el método de bisección, entonces existen los limites : $\lim_{n\to\infty}a_n$ y $\lim_{n\to\infty}b_n$, son iguales y representan una raíz de $f$. Si $c_n=\frac{a_n+b_n}{2}$ y $r = \lim_{n\to\infty}c_n$ entonces $$\Delta c_n=|r-c_n|=\frac{b_0+a_0}{2^{n+1}}$$