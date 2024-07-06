# Second coming of Taylor
**Hipótesis:**
$f\in C^{(n)}[a,b]$ y existe $f^{(n+1)}(a,b)$ entonces para todo par $x,c\in [a,b]$ se tiene que 
$$\begin{align}
f(x) & =\lim_{n\to\infty}\left(\sum_{n=0}^{n}\frac{f^{(n)}(a)}{n!}(x-a)^n + R_{n,a}(x)\right)\\
& = \lim_{n\to\infty}\left(\ T_{n,a}(x) + R_{n,a}(x)\ \right)
\end{align}$$
Donde:
![[Series de Potencias#Series de Taylor#Polinomio de Taylor|Second coming of Taylor]]
![[Series de Potencias#Series de Taylor#Resto de Taylor#Fórmula de Lagrange para el resto|Second coming of Taylor]]

# Órdenes de Convergencia
### Notación O grande y o chica
Esta notación se usa para comparar la velocidad de convergencia de sucesiones y funciones

![[Ordenes de convergencia#Notación mathcal O grande]]

![[Ordenes de convergencia#Notación mathcal o chica]]

### Tasa de convergencia
La tasa de convergencia es una medida de la velocidad a la que crece una función o sucesión. Una *tasa lineal* es más lenta que una *superlineal*, que a su vez es más lenta que una *tasa cuadrática *. 

![[Ordenes de convergencia#Órdenes de convergencia#Tasa lineal]]
Es decir que multiplicar por una constante supera a la velocidad de convergencia de $\{x_i\}$ en $n+1$

![[Ordenes de convergencia#Órdenes de convergencia#Tasa superlineal]]
Es decir que la velocidad de la sucesión de $\{x_i\}$ en cada paso es superada al multiplicar por un valor que no es constante.

![[Ordenes de convergencia#Órdenes de convergencia#Tasa cuadrática]]


# Algoritmo de Horner
Para evaluar polinomios de manera eficiente utilizamos el método de Horner y el algoritmo derivado de dicho método.

![[Algoritmo de Horner#Idea]]

![[Algoritmo de Horner#Algoritmo]]

# Cálculo del error
Todo resultado obtenido en un entorno numérico tiene una cierta taza de error inevitable, ya sea por problemas en la representación de los valores o simplemente el hecho de realizar operaciones sobre ellos. Sin embargo, podemos aproximar el error y usar técnicas para mitigarlo.

![[Cálculo de error#Cálculo]]

## Errores de representacion![[Cálculo de error#Redondeo y truncado]]
## Errores por operaciones

![[Cálculo de error#Suma]]

![[Cálculo de error#Resta]]

![[Cálculo de error#Producto]]

## [[Cálculo de error#Cancelación de dígitos significativos|Dígitos significativos]]
El número $\bar a$ se aproxima al número real $a$ con $r$ dígitos significativos si
$$\frac{\Delta a}{|a|}\leq 5*10^{-r}=\frac12*10^{1-r}$$
Conforme aumenta el error, se reducen los dígitos significativos

# Estándar de punto flotante
![[Estandar de punto flotante#Definición]]

![[Estandar de punto flotante#Errores de redondeo]]

![[Estandar de punto flotante#Operaciones aritméticas#Suma]]