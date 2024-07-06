Sucesiones de vectores que convergen a la solución bajo adecuadas hipótesis.
- Teorema 1 : Sea $b\in\mathbb R^n$ y $A=M-N\in\mathbb R^{n*n}$ donde $A$ y $M$ son matrices [[Determinante#Matrices singulares o degeneradas|no singulares]]. Si $||M^{-1}N||<1$ para alguna [[Vectores#Norma|norma]] matricial inducida entonces la sucesión generada por la ecuación$$\begin{matrix}x^{(k+1)}=(M^{-1}N)x^{(k)}+M^{-1}b&&para\ k\geq0\end{matrix}$$converge a la solución de $Ax=b$.

# Método de Jacobi
- Teorema 2 : Si $A$ es diagonalmente dominante, entonces la sucesión generada por el método de Jacobi converge a la solución de $Ax=b$, para cualquier vector inicial $x^{(0)}\in\mathbb R^n$.
	- $A\in\mathbb R^{n*n}$ es diagonalmente dominante si$$\begin{align}|a_{ii}|\lt\sum^{n}_{\begin{matrix}j=1\\j\neq i\end{matrix}}|a_{ij}|\end{align}$$
- Teorema 5 : Una condición necesaria y suficiente para que la sucesión generada por el método iterativo $x^{(k+1)}=(M^{-1}N)x^{(k)}+M^{-1}b$ converja a la única solución de $Ax=b$ para todo $x^{(0)}\in\mathbb R^n$ inicial es que $p(M^{-1}N)<1$

# Método de Gauss-Seidel
- Teorema 3 : Si $A$ es diagonalmente dominante, entonces la sucesión generada por el método de Gauss-Seidel converge en la solución de $Ax=b$, para cualquier vector inicial $x^{(0)}\in\mathbb R^n$.
- Teorema 4 :  Para cada matriz $A\in\mathbb R^{n*n}$, se cumple que $p(A)$ es igual a l $inf\{||A||\}$ sobre todas las normas matriciales inducidas
