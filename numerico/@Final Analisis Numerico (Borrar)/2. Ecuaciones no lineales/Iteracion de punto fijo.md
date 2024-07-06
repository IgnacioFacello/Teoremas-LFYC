# Iteración
Si el punto fijo existe y es único en $[a,b]$ entonces la sucesión con $x_0\in[a,b]$
$$x_{n+1}=f(x_n) \qquad \qquad n \geq 0$$
converge a dicho punto fijo

# Error
==Arréglate con el relativo capo==

Si las derivadas de la función de iteración de punto fijo se anulan en el punto fijo p hasta el orden (r-1) entonces el método tiene orden de convergencia (al menos) r.

- Corolario 2 : Si $f$ es una función que tiene raíz simple p entonces el método de newton es un método de punto fijo y tiene orden de convergencia ( al menos ) 2

- Corolario 3 :  SI $p$ es una raíz de multiplicidad $r \geq 2$ de $f$, entonces el método de newton tiene orden 1.

- Corolario 4 : Si p es una raíz de multiplicidad $r \geq 2$ de $f$, entonces la siguiente modificación del método recupera la convergencia
$$x_{n+1}=x_n-r\frac{f(x_n)}{f'(x_n)}$$

### Teoremas: Existencia y Unicidad
- Existencia
> Dada $g : \mathbb R\to \mathbb R$ tal que  $g\in C[a,b]$ y $g(x)\in [a,b],\forall\ x\in [a,b]$
> Entonces $\exists\ p\in [a,b]$ tq  $g(p) = p$   
- Unicidad
> Si además existe $g'(x)$  $\forall\ x\in (a,b)$ y una constante positiva $k \lt 1$ tal que $|g'(x)| \leq k$  en el mismo intervalo.
> Entonces el punto fijo $p$ es único

# Teoremas:
- Teorema 2 : Sea $g\in C[a,b]$