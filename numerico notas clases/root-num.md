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
Podemos expandir esta metodología hasta un polinomio de $n$ suponiendo que $n\lt{m-1}$ 