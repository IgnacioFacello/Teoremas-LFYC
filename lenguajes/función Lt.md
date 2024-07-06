# Indice del máximo primo que forma a x
Guía 2 - P4
[[codificacion por infinitupla de un x#Coordenadas de (x)]]

$$\begin{align}
Lt &:\mathbb N\to\omega\\
Lt(x) &=\begin{cases}
max_i (x)_i\neq0 & si\ x\neq 1 \\
0 & si\ x= 1 
\end{cases}
\end{align}$$
Lt(x) retorna un $i$ tal que $pr(i)$ es el máximo primo que divide $x$