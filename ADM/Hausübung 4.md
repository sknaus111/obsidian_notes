
$M=\{(1,2),(1.1,2),(1.11,2)\}$

$a-c=b-d \implies a-b=c-d$
## 113) 
Sei $M = \mathbb{R} \times \mathbb{R}$ und $R$ eine Relation auf $M$ gegeben durch
$$(a, b)R(c, d) :⇔ a − c = b − d$$
Zeigen Sie, dass $R$ eine Äquivalenzrelation ist, und bestimmen Sie die durch $R$ induzierte Partition
von $M$.

- Reflexivität
	$(a,b)R(a,b)$
	$a-a=b-b$
	$0=0$
- Symmetrie
	$(a,b)R(c,d)$

	$a-c=b-d \implies  a+d=b+c \implies d-b=c-a \implies c-a=d-b\implies(c,d)R(a,b)$
- Transitivität
	$(a,b),(c,d),(e,f) \in M$
	$(a,b)R(c,d) ~~(c,d)R(e,f)$
	$a-c=b-d \implies a-b=c-d$
	$c-e=d-f \implies c-d=e-f$
	$a-b=e-f \implies a-e=b-f \implies (a,b)R(e,f)$

alle Paare aus Zahlenpaare mit gleicher Differenz
$K=\{ (a,b) \in \mathbb{R}^2|a-b=c-d|(c,d)\in\mathbb{R}^2\}$

## 128) 
Für $k, n \in \{1, 3, 4, . . . , 10\}$ sei $kRn$, falls $k$ ein Teiler von $n$ ist und $k$ und $\frac{n}{k}$ teilerfremd sind. Man untersuche, ob die Relation $R$ eine Halbordnung ist, und ermittle gegebenfalls das Hassediagramm.

- Reflexivität
	$kRk$
	$k|k$
	$ggT(k,\frac{k}{k}) =ggT(k,1)=1$
- Antisymmetrie
	$kRn = nRk \implies k=n$
	$kRn \implies k|n\implies n=k*p$
	$nRk \implies n|k \implies k=n*q$
	$\implies n=n*q*p \land k=k*p*q \implies q*p=1$
	$kRn \implies n=k*1 \implies n=k$
	$nRk \implies k=n*1 \implies k=n$
- Transitivität
	$kRn ~~~ nRl$
	$n=k*p$
	$l=n*q \implies l=k*p*q \implies l=k*r \implies k|l$
	$ggT(k \frac{n}{k})=1 \land ggT(n \frac{l}{n})=1  \implies      ggT(k\frac{l}{k})$
	$ggT(k,\frac{k*p}{k}) \implies ggT(k,p)=1$
	$ggT(k*p, \frac{n*q}{k*p}) \implies ggT(k*p, \frac{k*p*q}{k*p}) \implies ggT(k*p,q) = 1 \implies ggT(k,q)=1$

	$ggT(k, \frac{k*p*q}{k}) \implies ggT(k,p*q)$	
	$ggT(k,p)=1 \land ggT(k,q)=1 \implies ggT(k,p*q)=1$




```tikz
\begin{document}
\begin{tikzpicture}[scale=2, transform shape] 

\node (1) at (0,0) {1}; 
\node (3) at (-1.5,2) {3}; 
\node (4) at (-0.5,4) {4}; 
\node (5) at (1.5,2) {5}; 
\node (6) at (-2.5,4) {6}; 
\node (7) at (1.5,4) {7}; 
\node (8) at (0.5,4) {8}; 
\node (9) at (-1.5,4) {9}; 
\node (10) at (2.5,4) {10};

\draw (1) -- (3); 
\draw (1) -- (4); 
\draw (1) -- (5); 
\draw (3) -- (6); 
\draw (1) -- (8); 
\draw (5) -- (10); 
\draw (1) -- (9); 
\draw (1) -- (7);
\end{tikzpicture}
\end{document}
```
## 131) 
Welche der Eigenschaften Reflexivität, Symmetrie, Antisymmetrie und Transitivität
haben folgende Relationen $R$ auf $\mathbb{Z}$:

$mRn \iff m^2 = n^2$

- Reflixivität
	$mRm \iff m^2=m^2$

- Symmetrie
	$mRn \iff m^2=n^2 \implies nRm \iff n^2=m^2$
	$m^2=n^2 \iff n^2=m^2 \implies mRn \iff nRm$

- Transitivität
	$mRn \iff m^2=n^2 \land nRo \iff n^2=o^2$
	$m^2=n^2=o^2 \implies m^2=o^2 \implies mRo$
- Antisymmetrie
	$m,-m\in\mathbb{Z}$
	$mR-m ~\iff m^2=-m^2 \land -m^2=m^2$
	$-m\not=m$ Widerspruch zur Definition der Antisymmetrie
## 139)  
Untersuchen Sie, ob es sich bei den folgenden Relationen $R ⊆ A × B$ um Funktionen,
injektive Funktionen, surjektive Funktionen bzw. bijektive Funktionen handelt. ($\mathbb{R}^+$ bezeichnet
die Menge aller positiven reellen Zahlen.)

$R = \{(log_{2}x, x)|x ∈ \mathbb{R}^+\}, A = B = \mathbb{R}$

$\log_{2}x \rightarrow x \in\mathbb{R}^+$

- injektiv (Wertemenge max 1mal)
	Angenommen stimmt nicht
	$f(\log_{2}x_{1})=f(\log_{2}x_{2})=x~~~~~~~~ x_{1}\not=x_{2}$
	$x_{1}=x_{2}$ Widerspruch

	Da Gegenannahme nicht stimmt ist die Funktion injektiv


- surjektiv (Wertemenge min 1mal)
	$f(\log_{2}x)$ mit $x\leq1$ nicht definiert für $R^+$

	Nicht surjektiv
- bijektiv (beides)
	Da es nicht surjektiv ist, ist die Funktion auch nicht bijektiv