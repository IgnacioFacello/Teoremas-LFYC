# Idea
Consiste en convertir la resolución de un problema complicado en una sucesión de problemas más sencillos.  Para ello utilizamos la sucesión $$x_{n+1}=x_n-\frac{f(x_n)}{f'(x_n)}$$
![[Pasted image 20220420115550.png]]
Un problema con este método es que si no tomamos un $x_0$ lo suficientemente cercano a la raíz, la sucesión no converge. Sin embargo, este método es mucho más rápido que el de [[Método de bisección|bisección]], teniendo convergencia cuadratica a la lineal del de bisección.

# Algoritmo
- $\text{fun}[0]$ es la función
- $\text{fun}[1]$ es la derivada de la función
- $x$ es $x_0$ la aproximación inicial
- err es la tolerancia para el error
- mit es el máximo de iteraciones
``` Python
def rnewton(fun,x,err,mit):
    x0 = x
    hx = []
    hf = []
    v, dv = fun(x0)
    for i in range(mit):
        hx.append(x0)
        hf.append(v)
        x0 = x0 - v / dv
        v, dv = fun(x0)
        if (abs(v) < err or abs((x0 - hx[i])/x0) < err):
            break
    return hx, hf
```
- $hx$ es una lista de las aproximaciones
- $hf$ es la evaluación de dichas aproximaciones

# Convergencia
## (incompleto)
Sea
- $f''$ continua en un entorno de una raíz $r$ de $f$ 
- $f'(r)\neq0$
Entonces existe $\delta>0$ tal que si el punto inicial satisface $x_0$

# Error
Sea 
$$e_{i+1}=\frac{e_nf'(x_n)+f(x_n)}{f'(x_n)}$$
y
$$f(x_n+h)=f(x_n)+f'(x_n)h+\frac12f''(\xi_n)h^2$$ es el desarrollo de Taylor de f centrado en $x_n$ para algún $\xi_n$ entre $x_n$ y $x_n+h$. 
Tomando $h = e_n = r - x_n$, se tiene que $x_n+h=r$ y luego 
$$e_{i+1}= -\frac12\frac{f''(\xi_n)}{f'(x_n)}e^2_n $$
con $\xi_n$ entre $x_n$ y $r$ 