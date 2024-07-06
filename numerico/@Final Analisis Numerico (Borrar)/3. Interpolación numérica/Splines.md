# Splines lineales
Dado un $i$ fijo, se pueden determinar los coeficientes $a_i,b_i$ para $i=0,1,\dots,n-1$ de la siguiente manera:
$$
\begin{aligned}
a_ix_i+b_i\quad =\quad {S_i=f(x_i)}\\
a_ix_{i+1}+b_i\quad =\quad {S_{i+1}=f(x_{i+1})}
\end{aligned}
	$$                                     ^^^^^MAL^^^^^
$$\begin{matrix}
a_i=\frac{f(x_{i+1})-f(x_{i})}{x_{i+1}-x_i}\ , &&
b_i=f(x_i)-a_ix_i
\end{matrix}$$

# Splines cúbicos
