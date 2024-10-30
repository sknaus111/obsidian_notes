## Aufgabe 1.
Für $n,k,k \in \mathbb{Z}$ definieren wir das Prädikat
$$
n\equiv k \text{ (mod m)} :\Leftrightarrow  \exists q\in\mathbb{Z}n=q*m+k
$$

Geben Sie für jede der im folgenden Beweis mit $a$ bis $e$ markierten Stellen an, was an der
jeweiligen Stelle die Voraussetzungen sind und was die Behauptung ist.

Satz. Falls $k ≡ l \text{ (mod } m)$ und $n | m$ dann $k ≡ l \text{ (mod } n)$.

Beweis. Sei $k ≡ l \text{ (mod } m)$ und $n | m.$ $a$ Dann existiert ein $q$ mit $k = q · m + l$ und ein
$r$ mit $n · r = m$. $b$ Es reicht zu zeigen, dass ein $s$ existiert mit $k = s · n + l$. $c$ Es gilt
$k = q · m + l = q · n · r + l$. $d$ Sei $s = q · r$ , dann reicht es zu zeigen dass $k = q · r · n + l$.
$e$ Das ist bekannt.

$\forall k,m,l,n(k\equiv l \text{ (mod m)} \land m (n \implies k\equiv l \text{ (mod m)}))$
- $a)~ \implies \exists q (k=q*m+l) \land \exists r(n*r=m)$ 
- $b)~ \exists s(k=s*n+l)$
- $c) ~ \implies k=q*m+l=q*n*r+l$
- $d) ~ s=q*r ~~~~~~~~~~k=q*r*n+l$
## Aufgabe 2. 
Wir betrachten den folgenden Beweis.

Satz. Falls $n_{1}$ und $n_{2}$ gerade sind, dann ist auch $n_{1} + n_{2}$ gerade.

Beweis (realistisch). Sei $n_{1} = 2k_{1}$ und $n_{2} = 2k_{2}$, dann ist $n_{1} + n_{2} = 2k_{1} + 2k_{2} = 2(k_{1} + k_{2})$,
also ist auch $n_{1} + n_{2}$ gerade.
Geben Sie von diesem Beweis a) eine detaillierte und b) eine formale Darstellung an

- $a)$ Sei $n_{1}$ und $n_{2}$ gerade, Es gibt also ein $k_{1}$ und ein $k_{2}$ so dass $2k_{1}=n_{1}$ und $2k_{2}=n_{2}$. Dann ist $n_{1}+n_{2}=2(k_{1}+k_{2})$. Jetzt reicht es zu zeigen, dass ein $x$ existiert 
$z_{x}=n_{1}+n_{2}$ Sei $x=k_{1}+k_{2}$ dann reicht es zu zeigen, dann $2(k_{1}+k_{2})=n_{1}+n_{2}$
 - $b$) $n_{1},n_{2}$ gerade                                    $n_{1}+n_{2}$ gerade  
	 $\exists k_{1}: 2k_{1}=n_{1} \land \exists k_{2}:2k_{2}=n_{2}$           $\exists k: 2k=n_{1}+n_{2}$
	 Sei $k_{1}$ s.d $2k_{1}=n_{1}$                              Sei $k=k_{1}+k_{2}$
	 Sei $k_{2}$ s.d. $2k_{2}=n_{2}$                                Es reicht zu zeigen
	 $\exists$ Voraussetzung                                  $n_{1}+n_{2}=2(k_{1}+k_{2})$
	 $n_{1}+n_{2}=2k_{1}+2k_{2}=2(k_{1}+k_{2})$       schon bekannt
