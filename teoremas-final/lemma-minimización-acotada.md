---
tags:
  - lfyc-c-VII
  - review
---
> Sean $n,m\ge0$. Sea $P:D_P\subseteq\omega\times\omega^n\times\Sigma^{*m}\to\omega$ un predicado $\Sigma$-pr. Entonces:
> (a) $M(P)$ es $\Sigma$-recursiva
> (b) Si hay una función $\Sigma$-pr $f:\omega^n\times\Sigma^{*m}\to\omega$ tal que $$M(P)(\vec x,\vec\alpha)=\min_t P(t,\vec x,\vec\alpha)\le f(\vec x,\vec\alpha)$$ para cada $(\vec x,\vec\alpha)\in D_{M(P)}$. Entonces $M(P)$ es $\Sigma$-pr.

---
> Suposiciones
> - P es un predicado $\Sigma$-pr

Sea $\bar P=P\cup (C_0^{n+1,m}|_{(\omega^{n+1}\times\Sigma^{*m})-D_P}):\omega^{n+1}\times\Sigma^{*m}\to\omega$ un predicado $\Sigma$-total, que ademas va a ser $\Sigma$-pr.
%% ya que P es $\Sigma$-pr %%
### Veamos primero que $M(P)=M(\overline P)$. 
Notar que para todo $(\vec x,\vec\alpha)\in\omega^{n}\times\Sigma^{*m}$
$$
\{t\in\omega:P(t,\vec x,\vec\alpha)=1\}=\{t\in\omega:\bar P(t,\vec x,\vec\alpha)=1\}
$$
Esto nos dice que $M(P)=M(\overline P)$, ya que:
- $D_{M(P)}=D_{M(\overline P)}$ 
	- Recordar que $D_{M(P)}=\{(\vec x,\vec\alpha)\in\omega^{n}\times\Sigma^{*m} :(\exists t\in\omega)\ P(t,\vec x,\vec\alpha)=1\}$
- y ademas  $M(P)(\vec x,\vec\alpha)=M(\overline P)(\vec x,\vec\alpha)$ para cada $(\vec x,\vec\alpha)\in D_{M(P)}$
	- $min\{t\in\omega:P(t,\vec x,\vec\alpha)=1\}=min\{t\in\omega:\bar P(t,\vec x,\vec\alpha)=1\}$
## (a)
Ahora vemos que $M(\overline P)$ es *recursiva*.
Sea k tal que $\bar P\in PR_k^{\Sigma}$.
Dado que
- $\bar P$ es $\Sigma$-total 
- y $PR_k^{\Sigma}\subseteq R_k^{\Sigma}$

Entonces tenemos que $M(\bar P)\in R_{k+1}^{\Sigma}$ y por lo tanto $M(P)$ es $\Sigma$-r.
## (b)
> (b) Si hay una función $\Sigma$-pr $f:\omega^n\times\Sigma^{*m}\to\omega$ tal que $$M(P)(\vec x,\vec\alpha)=\min_t P(t,\vec x,\vec\alpha)\le f(\vec x,\vec\alpha)$$ para cada $(\vec x,\vec\alpha)\in D_{M(P)}$. Entonces $M(P)$ es $\Sigma$-pr.

Ya que $M(P)=M(\bar P)$, basta con probar que $M(\bar P)$ es $\Sigma$-pr.
(1) $D_{M(\bar P)}$ es $\Sigma$-pr. 
$$
\begin{align}
\chi_{D_{M(\bar P)}}^{\omega^{n+1}\times\Sigma^{*m}}
&=\lambda\vec x\vec\alpha
	\left[
		(\exists t\in\omega)_{t\leq f(\vec x,\vec\alpha)} P(t,\vec x,\vec\alpha)
	\right] \\
&=\lambda y\vec x\vec\alpha
	\left[
		(\exists t\in\omega)_{t\leq y} P(t,\vec x,\vec\alpha)
	\right] \circ \left[
		f,p_1,\dots,p_{n+m}
	\right]
\end{align}
$$
es claramente $\Sigma$-pr por el [[guia6-lemma2|lemma 2]]. 
(2)
Sea el predicado $\Sigma$-total y $\Sigma$-pr
$$
\begin{align}
P_1
&=\lambda t \vec x\vec \alpha\left[
	\bar P(t, \vec x,\vec \alpha) \land
	(\forall j\in\omega)_{j\leq t}\ j=t\ \lor\ 
		\lnot\bar P(j, \vec x,\vec \alpha)
\right]\\
\end{align}
$$
> Es decir que, para $(\vec x,\vec \alpha)$, $t$ satisface $\bar P$ y no hay un $j$ menor que lo satisface. 
> Efectivamente $P_1$ nos dice si $t=M(\bar P)(\vec x,\vec \alpha)$ 
> Que sea $\Sigma$-pr necesariamente es trivial

Notar que para $(\vec x,\vec \alpha)\in \omega^n\times\Sigma^{*m}$ 
$$
\begin{align}
P_1(t,\vec x,\vec \alpha)
&= 1\iff (\vec x,\vec \alpha)\in D_{M(\bar P)} \land t=M(\bar P)(\vec x,\vec \alpha) \\
\end{align}
$$
Esto nos dice que:
$$
M(\bar P)=
$$