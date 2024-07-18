[[notas clase 1]]
[[notas clase 2]]
[[notas clase 3]]
[[notas clase 4]]
[[notas clase 5]]
[[notas clase 6]]
# Clase 10 a 12
## Clase 10
Queremos aproximar funciones, ya sea porque desconocemos la función real o para simplificar su computo

Aproximación *discreta* por **cuadrados mínimos**
Función desconocida, tenemos un set de datos experimentales que indican que la función es lineal.
A diferencia de el tema anterior no es necesario ni razonable pedir que la función pase por todos los puntos ya que los datos van a tener errores  
Es mejor pensar en un *modelo lineal* y encontrar la recta que mejor se ajuste a los datos.
Dado un set de $m$ datos experimentales. El método de cuadrados mínimos consiste en determinar coeficientes $a_0,a_1$ que minimizan $$E(a_0,a_1)=\sum_{i=0}^{m}\left[y_i-(a_1x^i+a_0)\right]^2$$
Condicion necesaria para minimizar es que las derivadas sean 0
Las reordenamos y obtenemos un sistema de ecuaciones que al ser resuelto nos da los coeficientes que buscabamos
Podemos expandir esta metodología hasta un polinomio de $n$ suponiendo que $n\lt{m-1}$. Luego tenemos que encontrar coeficientes $a_0,a_1,\dots,a_n$ que minimizan $$E(a_0,a_1)=\sum_{i=0}^{m}\left[y_i-P_n[a_0,\dots,a_n](x_i)\right]^2$$
Es decir que resuelven el sistema de ecuaciones
$$\sum^{n}_{k=0}a_k\sum^{m}_{i=1}x^{j+k}_i=\sum^{m}_{i=1}{y_ix^j_i}$$

Este método solo es util para aproximar funciones **polinomiales**.

## Clase 11
Para aproximar una función continua en un intervalo $[a,b]$ debemos minimizar
$$E(a_0,\dots,a_n)=\int_{a}^{b}[f(x)-P_n(x)]^2dx$$
Similarmente al caso anterior llegamos a un sistema de ecuaciones normales
$$\sum^{n}_{k=0}a_k\int^a_bx^{k+j}dx=\int^a_b{x^jf(x)dx}\quad\text{para}\quad j=0,1,\dots ,n$$ que si resolvemos podemos obtener los coeficientes que minimizan el error.
Problema: La matriz de coeficientes que generan estas ecuaciones es conocida como la matriz de Hilbert y es mal condicionada, por esto es mejor buscar otra forma de representar el polinomio. En cierta forma cambiamos la base sobre la que trabajamos.

> #definicion Funciones linealmente independientes
> El conjunto $\{\phi_0,\dots,\phi_n\}$ es *linealmente* **independiente** en el intervalo $[a,b]$, si siempre que $$c_0\phi_0(x)+\dots+c_n\phi_n=0\quad\text{para cualquier }x\in[a,b]$$ se tiene que $c_0=\dots=c_n=0$. Caso contrario se dice que el conjunto de funciones es linealmente **dependiente**

> #teorema Un conjunto de polinomios todos de grado distinto son linealmente independientes

> #teorema Dado un conjunto de polinomios linealmente independientes podemos usarlos para describir cualquiere polinomio de grado menor o igual al mayor de ellos

## Clase 12
> #definicion Función de peso

Estas funciones se van a usar para definir la medida del error y permiten asignar mas o menos importancia a distintas partes del intervalo
Ahora reformulamos el problema. Dado un conjunto de funciones linealmente independientes en $[a,b]$ una funcion de peso $\omega$ y una funcion $f$ continua en el intervalo. Se desean determinar los coeficientes de $$P(x)=\sum^n_{k=0}{a_k\phi_k(x)}$$ que minimizan $$E(a_0,\dots,a_n)=\sum^{m}_{j=0}\omega(x)[y_i-P_n(x_i)]^2$$
