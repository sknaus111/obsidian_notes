## Aufgabe 1. 
Sei $n ≥ 2$, seien $0 < a_{i} < 1$ für $i = 1, ... , n$. Zeigen Sie dass mittels vollständiger
Induktion dass für alle $n ≥ 2$ gilt: $\prod_{i=1}^{n}(1-a_{i})>1-\sum_{i=1}^{n}a_{i}$. Kennzeichnen Sie dabei deutlich die
Struktur und alle Elemente Ihres Induktionsbeweises.


#Induktionsanfang
$$\prod_{i=1}^{2}(1-a_{i})>1-\sum_{i=1}^{n}a_{i}
$$$$(1-a_{1})(1-a_{2})>1-(a_{1}+a_{2})
$$$$1-a_{1}-a_{2}+a_{1}a_{2} > 1-a_{1}-a_{2}
$$$$a_{1}a_{2}>0
$$
#Induktionsschritt
#Induktionsvoraussetzung
$$
\prod_{i=1}^{n}(1-a_{i})>1-\sum_{i=1}^{n}a_{i}
$$
#Induktionsbehauptung
$$\prod ^{n+1}_{i=1}(1-a_{i})>1-\sum ^{n+1}_{i=1}a_{i}$$
$$
\prod ^{n+1}_{i=1}(1-a_{i})>1-\sum_{i=1}^{n}a_{i} - a_{n+1}
$$
$$
\prod_{i=1}^{n+1}(1-a_{i})=(1-a_{n+1})\cdot \prod ^{n}_{i=1}(1-a_{i})
$$
Einsetzen der Voraussetzung
$$
(1-a_{n+1})\cdot\prod ^{n}_{i=1}(1-a_{i})>(1-\sum ^{n}_{i=1}a_{i}) (1-a_{n+1})
$$
$$
 1-\sum_{i=1}^{n}a_{i}-a_{n+1}+\left( \sum_{i=1}^{n}a_{i}\cdot a_{n+1} \right) > 1-\sum ^{n}_{i=1}a_{i}-a_{n+1}
$$
$$
\prod^{n+1}_{i=1}(1-a_{i})=(1-a_{n+1})\cdot\prod ^{n}_{i=1}(1-a_{i})>1-\sum_{i=1}^{n}a_{i}-a_{n+1} + \left( \sum_{i=1}^{n}a_{i}\cdot a_{n+1} \right) > 1-\sum_{i=1}^{n}a_{i}-a_{n+1}
$$
$$
\prod^{n+1}_{i=1}(1-a_{i})>1-\sum ^{n+1}_{i=1}a_{i}
$$
## Aufgabe 2. 
Die Menge $A ⊆ Z$ sei induktiv wie folgt definiert: 1. $6 ∈ A$, 2. $−15 ∈ A$ und 3. falls
$x, y ∈ A$, dann ist auch $x + y ∈ A$. Zeigen Sie mittels struktureller Induktion dass für alle $x ∈ A:3 | x$

IA: $3|6$ und $3|-15$
IS:     
    IV: $3|x$ und $3|y$
    IB: $3|(x+y)$
    $$
(x+y)=x + y
$$
	Einsetzen der Voraussetzung
	$$
x=3*k, y=3*l~~~~k,l \in \mathbb{Z}
$$
$$
(x+y)=x+y=3*k+3*l=3(k+l)\implies3|(x+y)
$$
