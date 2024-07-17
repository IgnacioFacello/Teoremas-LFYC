[[notas clase 1]]
[[notas clase 2]]
[[notas clase 3]]
[[notas clase 4]]
[[notas clase 5]]
[[notas clase 6]]
# Clase 10 a 12
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

Para aproximar una función continua en un intervalo $[a,b]$ debemos minimizar
$$E(a_0,\dots,a_n)=\int_{a}^{b}[f(x)-P_n(x)]^2dx$$
Similarmente al caso anterior llegamos a un sistema de ecuaciones normales
$$\sum^{n}_{k=0}a_k\int^a_bx^{k+j}dx=\int^a_b{x^jf(x)dx}\quad\text{para}\quad j=0,1,\dots ,n$$ que si resolvemos podemos obtener los coeficientes que minimizan el error.
Problema: La matriz de coeficientes que generan estas ecuaciones es conocida como la mstriz de Hilbert y es mal condicionada, por esto es mejor buscar otra forma de representar el p