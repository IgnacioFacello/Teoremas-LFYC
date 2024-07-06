La idea consiste en factorizar la matriz como un producto de dos matrices mas simples: $A=LU$, donde $L$ es una matriz triangular inferior con elementos diagonales iguales a 1 y $U$ triangular superior.
Luego debemos resolver dos sistemas mas simples:$$\begin{matrix}
Ux=y\\
Ly=b
\end{matrix}$$
# Método
Comenzamos por la primera fila de $U$. Que es igual a la primera fila de $A$
$$\begin{aligned}u_{1i}=a_{1i}&&\text{para} && i = 1,\dots,n\end{aligned}$$
Luego la primera columna de $L$.
$$\begin{aligned}l_{j1}=\frac{a_{j1}}{u_{11}}&&\text{para} && j = 2,\dots,n\end{aligned}$$
Además, la diagonal de $L$ esta compuesta por 1s.
$$\begin{aligned}l_{ji}=1&&si\ \ j=i\end{aligned}$$
Luego calculamos el resto de los coeficientes.
$$\begin{aligned}u_{kj}=a_{kj}-\sum^{k-1}_{m=1}l_{km}u_{mj}&&para\ \ j=k,\dots,n\end{aligned}$$

$$\begin{aligned}l_{ik}=\frac1{u_{kk}}(a_{ik}-\sum^{k-1}_{m=1}l_{im}u_{mk})&&para\ \ i=k+1,\dots,n\end{aligned}$$

