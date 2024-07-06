# Idea
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
Si $f(a)*f(b)=0$ entonces $a$, o $b$ es una raiz y el algoritmo termina.

# Algoritmo
- fun es una Función 
- I es una lista $[a,b]$
- err es la tolerancia para el Error
- mit es el Máximo Número de Iteraciones Permitido
 
``` Python
def rbisec(fun,I,err,mit):
    a = I[0]
    fa = fun(a)
    b = I[1]
    fb = fun(b)
    e = b - a
    hx = []
    hf = []
    if (fa*fb >= 0): 
        return (hx,hf)
    for i in range(mit):
        e = e/2
        c = e + a
        w = fun(c)
        hx.append(c)
        hf.append(w)
        if ( abs(w) < err ): 
            return (hx,hf)
        if ( (fun(b))*(fun(c)) < 0 ):
            a = c
            fa = w
        if ( (fun(c))*(fun(a)) < 0 ):            
            b = c
            fb = w
    return hx, hf
```
- hx es la lista de todas las aproximaciones de la raíz
- hf es la evaluación de dichas aproximaciones

# Error
Sea $[a_i,b_i]\ i = 0, 1, \dots, n$ el intervalo generado por el método de bisección para la iteración $i$, entonces existen los límites: $\lim_{i\to\infty}a_i$ y $\lim_{i\to\infty}b_i$ que son iguales y representan una raíz $r$ de $f$. Si $c_n=\frac12(a_i+b_i)$ y $r=\lim_{i\to\infty}c_i$, entonces 
$$\bbox[10px,border:0.5px solid red]{|r-c_n|\leq\frac1{2^{n+1}}(b_0-a_0)}$$




