# Idea
Dado un polinomio
$$P(x)=a_0+a_1x^1+a_2x^2+\dots+a_{n-1}x^{n-1}+a_nx^n$$
el método de Horner consiste en reescribirlo y evaluarlo en la forma equivalente:
$$P(x)=a_0+x(a_1+x(a_2+x(\dots(a_{n-1}+a_nx))))$$

# Algoritmo
``` Python
def horner(coefs : list, x : float):
	y = coefs[0]
	for i in range(len(coefs),0):
		y = y*x + coefs[i]	
	return y
```