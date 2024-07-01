---
tags:
  - lfyc-c-IV
---
> Sea $\Sigma$ un alfabeto finito. Si $f:\omega\times S_1\times\dots\times S_n\times L_1\times\dots\times L_m\to\omega$ es $\Sigma$-pr, con $S_1,\dots,S_n\subseteq\omega$ y $L_1,\dots,L_m\subseteq\Sigma^*$ no vacíos, entonces la función $\lambda xy\vec x\vec\alpha\left[\sum_{t=x}^{t=y}f(t,\vec x,\vec\alpha)\right]$ es $\Sigma$-pr

Para mejorar la legibilidad vamos a tomar
$$
S_1\times\dots\times S_n\times L_1\times\dots\times L_m={S_{1..n}}\times{L_{1..m}}
$$

---
> Paso 1: Obtener algo de la forma $\lambda t\vec x\vec\alpha$ que haga recursion sobre el primer parámetro.
> Recordar que las definiciones se realizan bajo esta convención

Sea 
$$
G=\lambda tx\vec x\vec\alpha\left[\sum_{i=x}^{i=t}f(i,\vec x,\vec\alpha)\right]
$$

Luego tenemos que 
$$
\lambda xy\vec x\vec\alpha\left[\sum_{t=x}^{t=y}f(t,\vec x,\vec\alpha)\right] = 
G\circ\left[p_2^{n+2,m},p_1^{n+2,m},p_3^{n+2,m},\dots,p_{n+2+m}^{n+2,m}\right]
$$
por lo tanto basta con probar que $G$ es $\Sigma$-pr.
> Paso 2: Buscamos demostrar que $G=R(h,g)$

Primero, notemos que
$$
\begin{align}
G(0,x,\vec x,\vec\alpha) &= \begin{cases}
	0 & si\ x>0 \\
	f(0,\vec x,\vec\alpha) & si\ x=0
\end{cases} \\
G(t+1,x,\vec x,\vec\alpha) &= \begin{cases}
	0 & si\ x>t+1 \\
	G(t,x,\vec x,\vec\alpha)+f(t+1,\vec x,\vec\alpha) & si\ x\leq t+1
\end{cases}
\end{align}
$$
> Paso 2.3: Les damos la forma de las funciones con las que venimos trabajando en el paradigma recursivo

Es decir que podemos definir
$$
\begin{align}
	h : \omega\times{S_{1..n}}\times{L_{1..m}}&\to\omega\\
	(x,\vec x,\vec\alpha)&\to \begin{cases}
	    0 & si\ x>0 \\
	    f(0,\vec x,\vec\alpha) & si\ x=0
    \end{cases} \\ 
	g : \omega^{3}\times{S_{1..n}}\times{L_{1..m}}&\to\omega \\
	(A,t,x,\vec x,\vec\alpha)&\to \begin{cases}
	    0 & si\ x>t+1 \\
	    A+f(t+1,\vec x,\vec\alpha) & si\ x\leq t+1
    \end{cases} \\ 
\end{align}
$$


tales que $G=R(h,g)$. Solo queda probar que $h$ y $g$ son $\Sigma$-pr.
> Paso 2.6: Vamos a usar el lema de division por casos para mostrar que efectivamente son recursivas

Sean:
$$
\begin{align}
D_1&= \{(x,\vec x,\vec\alpha)\in\omega\times{S_{1..n}}\times{L_{1..m}}
: x\gt0\} \\
D_2&= \{(x,\vec x,\vec\alpha)\in\omega\times{S_{1..n}}\times{L_{1..m}}
: x=0\} \\
H_1&= \{(z,t,x,\vec x,\vec\alpha)\in\omega^3\times{S_{1..n}}\times{L_{1..m}}
: x\gt t+1\} \\
H_2&= \{(z,t,x,\vec x,\vec\alpha)\in\omega^3\times{S_{1..n}}\times{L_{1..m}}
: x\leq t+1\}
\end{align}
$$
Luego
$$
\begin{align}
	h &= 
		C_0^{n+1,m}|_{D_1} \cup 
		\lambda x\vec x\vec\alpha[f(0,\vec x,\vec\alpha)]|_{D_2} \\
	g &= 
		C_0^{n+3,m}|_{H_1} \cup 
		\lambda Atx\vec x\vec\alpha[A + f(t+1,\vec x,\vec\alpha)]|_{H_2} \\
\end{align}
$$
y por el [[division-casos-pr|lemma de división por casos]] si demostramos que $D_1,D_2,H_1,H_2$ son $\Sigma$-pr entonces $h$ y $g$ también lo serán. 
> Paso 3: Para poder validar el uso del lemma debemos garantizar que los conjuntos sean $\Sigma$-pr
> Esto lo logramos con una comparación simple y usando que f tenga dominio en el conjunto rectangular.
> Luego usamos su característica para garantizar que pertenezca al rectangular y la condición para garantizar que pertenezca al conjunto del caso.

Veamos el caso $H_1$ los demás salen de manera similar.
Dado que f es $\Sigma$-pr entonces $D_f=\omega\times S_1\times\dots\times S_n\times L_1\times\dots\times L_m$ es $\Sigma$-pr y podemos definir $R=\omega^3\times S_1\times\dots\times S_n\times L_1\times\dots\times L_m$ también lo es. 
Podemos usar este hecho para definir:
$$
\chi^{\omega^{n+3}\times\Sigma^{*m}}_{H_1} = \left[
	\chi^{\omega^{n+3}\times\Sigma^{*m}}_R \land 
	\lambda Atx\vec x\vec\alpha[ x\gt t+1 ]
\right]
$$
Lo cual nos garantiza que $H_1$ es $\Sigma$-pr