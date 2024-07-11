[[notas clase 1]]
[[notas clase 2]]
[[notas clase 3]]
# Clase 4
Problema: Hallar la raiz de una función no lineal

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