# Teoremas 
- Teorema 1 : Dados $x_0,x_1,\dots ,x_n$, $(n+1)$ números reales distintos con valores asociados $y_0,y_1,\dots ,y_n$ entonces existe un único polinomio $p_n$ de grado $\leq n$ tal que $p_n(x_i)=y_i$ para todo $i=0,1,\dots ,n$

# Forma de Newton 
$$P_n(x)=\sum^{n}_{i=0}c_i\prod^{i-1}_{j=0}{x-x_j}$$
## Diferencias divididas
Remplazamos los coeficientes $c_i$ por
$$c_k=f[x_0,x_1,\dots ,x_k]$$
donde 
$$f[x_i] = f(x_i)$$
y

$$f[x_i,\dots ,x_k]=\frac{f[x_{i+1},\dots ,x_k]-f[x_i,\dots ,x_{k+1}]}{x_k-x_n}$$
(Teorema 1)

#### Propiedades de las diferencias divididas
- Teorema 2 : Reorganizar los $x$ no cambia el resultado de $f[x_0,\dots ,x_n]$
- Teorema 3 : Sea $t$ un numero real distinto a cualquiera de los $x$ que el polinomio $p$ interpola, entonces $$f(t)-p(t)=f[x_0,\dots,x_n,t]\prod^{n}_{i=0}(t-x_i)$$
- Teorema 4 : Si $f$ es una función n veces continuamente diferenciable en $[a,b]$, entonces existe un punto $\xi\in (a,b)$ tal que$$f[$x_0,x_1,\dots ,x_n$]=\frac1{n!}f^{n}(\xi)$$
# Forma de Lagrange
Sea $l_i$ los polinomios básicos de Lagrange
$$l_i(x)=\prod^{n}_{j=0,j\neq i}{\frac{x-x_j}{x_i-x_j}}$$
para $i=0,1,\dots ,n$. Luego la forma de Lagrange para el polinomio interpolate es:
$$P_n(x)=\sum^{n}_{i=0}y_il_i(x)$$

# Error del polinomio interpolante
Teorema 2 : Sea $f$una función en $C^{n+1}[a,b]$ y $p$ un polinomio de grado$\leq n$ que interpola a $f$ en $(n+1)$ puntos distintos $x_0,x_1,\dots ,x_n$ en $[a,b]$. Entonces para cada $x\in [a,b]$ existe un $\xi=\xi_x\in(a,b)$ tal que $E(x)$ (error de la interpolación en x) es
$$f(x)-p(x)=\frac{f^{n+1}(\xi)}{(n+1)!}\prod^{n}_{i=0}(x-x_i)$$

