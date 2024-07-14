# Definición
Un punto fijo es un
# Algoritmo
$Para encontrar un punto fijo de una función $g$ primero se toma una aproximación inicial $p_0$ y se calcula $p_n=g(p_{n-1})$ para $n\geq 1$, generando una serie de aproximaciones $\{p_n\}$. Si la función $g$ es continua y la sucesión converge, entonces lo hace en un punto fijo $p$ de $g$ pues $$p=\lim\limits_{n\to\infty}p_n=\lim\limits_{n\to\infty}g(p_{n-1})=g(\lim\limits_{n\to\infty} p_{n-1})=g(p)$$
### Teorema: Existencia y Unicidad
- Existencia
> Dada $g : \mathbb R\to \mathbb R$ tal que  $g\in C[a,b]$ y $g(x)\in [a,b],\forall\ x\in [a,b]$
> Entonces $\exists\ p\in [a,b]$ tq  $g(p) = p$   
- Unicidad
> Si además existe $g'(x)$  $\forall\ x\in (a,b)$ y una constante positiva $k \lt 1$ tal que $|g'(x)| \leq k$  en el mismo intervalo.
> Entonces el punto fijo $p$ es único

# Error