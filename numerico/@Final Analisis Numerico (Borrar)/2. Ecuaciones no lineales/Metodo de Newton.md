# Iteración
$$x_{n+1}=x_n-\frac{f(x_n)}{f'(x_n)}$$
# Convergencia
Sea
- Error inicial menor a un $\delta$, es decir $|r-x_0|\leq\delta$ 
- $f''$ continua en un entorno de una raíz $r$ de $f$ 
- $f'(r)\neq0$ (No debe ser un punto critico)
Entonces existe $\delta>0$ tal que si el punto inicial satisface $x_0$

# Error
==Arréglate con el [[Cálculo de error#Cálculo de error#Cálculo|relativo]] capo==

Sea 
$$e_{i+1}=\frac{e_nf'(x_n)+f(x_n)}{f'(x_n)}$$
y
$$f(x_n+h)=f(x_n)+f'(x_n)h+\frac12f''(\xi_n)h^2$$es el desarrollo de Taylor de f centrado en $x_n$ para algún $\xi_n$ entre $x_n$ y $x_n+h$. 
Tomando $h = e_n = r - x_n$, se tiene que $x_n+h=r$ y luego 
$$e_{i+1}= -\frac12\frac{f''(\xi_n)}{f'(x_n)}e^2_n $$
con $\xi_n$ entre $x_n$ y $r$ 

# Método de la secante
Reemplazamos la derivada en el método de newton por$$a_n=\frac{f(x_n)-f(x_{n-1})}{x_n-x_{n-1}}$$ luego
$$x_{n+1}=x_n-f(x_n)\left[ \frac{f(x_n)-f(x_{n-1})}{x_n-x_{n-1}} \right]$$
El resto del método es igual.

Nos ahorramos calcular la derivada ( Mas simple ) a cambio de que sea un poco mas lento que el método Newton ( pero mas lento).

# Teoremas
- Teorema 1 :  Si $f''$ es continua en un entorno de una raíz r de $f$ y si $f'(r)\neq 0$ entonces existe $\delta>0$ tal que si el punto inicial satisface $|r-x_0|\leq\delta$ luego todos los puntos de la sucesión $\{x_n\}$ generados por el algoritmo del método de Newton satisfacen que $|r-x_n|\leq\delta$ para todo $n$, la sucesión $\{x_n\}$ converge a r y la [[Ordenes de convergencia|convergencia]] es cuadrática.

- Teorema 2 : Si $f''$ es continua en $\mathbb R$, $f$ es creciente y convexa ( U ) en $\mathbb R$ y tiene una raíz, entonces esa raíz es única y la iteración de newton convergerá a esa raíz independientemente del punto inicial $x_0$
