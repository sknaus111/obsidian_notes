## Rechenregeln für konvergente Folgen
Seien $(a_{n})_{n\geq 0}$ und $(b_{n})_{n\geq0}$ konvergente Folgen mit $\lim_{ n \to \infty }a_{n} = a$ und $\lim_{ n \to \infty }b_{n}=b$ Dann gilt.

- (i) $\lim_{ n \to \infty }(a_{n}\pm b_{n})=a\pm b$
- (ii) $\lim_{ n \to \infty }(\lambda a_{n})=\lambda a$ für $\lambda\in \mathbb{R}$
- (iii) $\lim_{ n \to \infty }(a_{n}b_{n})=ab$
- (iv) $\lim_{ n \to \infty }\frac{a_{n}}{b_{n}}= \frac{a}{b}$ falls $b_{n}\not=0$, für alle $n\in \mathbb{N}$, und $b\not=0$

### Beweis
Es gelte also $a_{n}\rightarrow a$ und $b_{n}\rightarrow b$. Für gegebenes $\varepsilon>0$ gibt es daher $N_{1}$ und $N_{2}$, so dass $|a_{n}-a|<\frac{\varepsilon}{2}$ für $n>N_{2}$ gilt. Daraus folgt, dass $|a_{n}\pm b_{n}-(a\pm b)|\leq |a_{n}-a|+|b_{n}-b|<\varepsilon$ für alle $n>max(N_{1},N_{2})$.

Die Menge $F$ aller konvergenten Folgen ist ein Unterraum des Vektorraums aller Funktionen $f:\mathbb{N}\rightarrow \mathbb{R}$. 

## Uneigentliche konvergente Folgen
Betrachte man die Folgen $a_{n}=n$ und $b_{n}=n+c_{n},c_{n}\geq 0$. Beide Folgen sind uneigentlich konvergent gegen $+\infty$. Über die Differenz $a_{n}-b_{n}=c_{n}$ kann jedoch a priori keine Aussage gemacht werden. Ihr Verhalten hängt von der Folge $c_{n}$ ab. Ähnlich verhält es sich bei Quotienten zweier uneigentlich konvergenten Folgen oder bei Quotienten zweier Nullfolgen: Es gibt beispielsweise
$$
\frac{n}{n^{2}}\rightarrow 0, \frac{n^{2}}{n}\rightarrow \infty, \frac{2n}{n}\rightarrow2
$$
Diese Beispiele zeigen, dass man Ausdrücken wie $\infty-\infty,\frac{\infty}{\infty} oder \frac{0}{0}$ keinen sinnvollen Wert zuweisen kann. Solche Ausdrücke heißen auch #unbestimmte_Formen. Auch $1^{\infty},\infty^{0}$ und $0^{0}$ zählen zu den unbestimmten Formen. 

## Rechenregeln für uneigentlich konvergente Folgen
Sei $(a_{n})_{n\geq 0}$ eine uneigentliche konvergente Folge und $\lambda\in \mathbb{R}$. Es gelte $\lim_{ n \to \infty }a_{n}=\infty$ und $\lim_{ n \to \infty }b_{n}=b$. Dann gilt

- (i) $\lim_{ n \to \infty }(a_{n}+b_{n})=\infty$, falls $b\in \mathbb{R}$ oder $b=\infty$
- (ii) $$\lim_{ n \to \infty }(\lambda a_{n})=\begin{matrix}

\end{matrix}$$
- (iii) $\lim_{ n \to \infty }(a_{n}b_{n})=\infty$. falls $b>0$
- (iv) $\lim_{ n \to \infty } \frac{b_{n}}{a_{n}}=0$, falls $b\in \mathbb{R}$

### Beispiel
Man nehme die Folge $a_{n}=\frac{n^{2}+n-1}{3n^{2}-11}$. Bei dieser Folge sind Zähler und Nenner uneigentlich konvergente Folgen, so dass die Rechenregeln auf konvergente Folgen nicht direkt anwendbar sind. Das Herausheben der höchsten Potenzen und Kürzen macht diese aber anwendbar.
$$
\lim_{ n \to \infty } a_{n}=\lim_{ n \to \infty }  \frac{1+\frac{1}{n}-\frac{1}{n^{2}}}{3-\frac{11}{n^{2}}}= \frac{1+0+0}{3-0}=\frac{1}{3}
$$
Für die geometrische Folge $a_{n}=q^{n}$ gilt
$$
\lim_{ n \to \infty } q^{n}= \left(\begin{matrix}
0 & \text{ falls }|q|<1  \\
1 & \text{ falls }q=1 \\
\infty & \text{ falls }q>1 
\end{matrix}\right)
$$
Um das zu zeigen, sei zunächst $q=1+p>1$. Dann gilt
$$
q^{n}=(1+p)^{n}=1+np+\binom{n}{2}p^{2}+\dots+\binom{n}{n}p^{n}\geq 1+np \rightarrow \infty
$$
Für $0<q<1$ gilt $\frac{1}{q}>1$ und daher $\frac{1}{q^{n}}\rightarrow \infty$. Daraus folgt aber $q^{n}\rightarrow 0$, denn setzt man ein $a_{n}=\frac{1}{q^{n}}$ und $b_{n}=1$, so folgt $q^{n}= \frac{b_{n}}{a_{n}} \rightarrow 0$. Der Fall $-1 < q < 0$ funktioniert analog, und die Fälle $q=0$ und $q=1$ sind trivial. Für $q\leq -1$ ist $(q^{n})_{n\geq0}$ divergent. Ähnlich lässt sich auch für $q\in \mathbb{C}$ argumentieren. Geometrische Folgen im Komplexen konvergieren also für $q$ innerhalb des Einheitskreises sowie für $q=1$ und divergieren für alle anderen Werte von $q$.

### Uneigentlich konvergente Folgen und Potenzbildung
Sei $a_{n}=1+ \frac{1}{n}$ und $b_{n}=n$. Es ist offensichtlich $\lim_{ n \to \infty }a_{n}=1$ und $\lim_{ n \to \infty }b_{n}=\infty$ Der Schluss $\lim_{ n \to \infty }a_{n}=1^{\infty}=1$ ist aber falsch! Denn mit Hilfe des binomischen Lehrsatzes bekommen wir
$$
a_{n}^{b_{n}}=\left(1+ \frac{1}{n}\right)^{n}= \sum_{k=0}^{n}\binom{n}{k} \left(\frac{1}{n}\right)^{k}\geq 1+ \binom{n}{1} \frac{1}{n}=2
$$
$a_{n}^{b_{n}}$ kann somit nicht gegen 1 konvergieren. Um die Folge weiter zu untersuchen benötigt es ein weiteres Resultat.

### Bernoulli'sche Ungleichung
Sei $n\in \mathbb{N}$ mit $n\geq 2$ und $x\geq -1$ mit $x\not=0$. Dann gilt
$$
(1+x)^{n}>1+nx
$$
### Beweis
Für $x=-1$ ist die Ungleichung trivial. Sei also $x>-1$. Wir führen den Beweis mit vollständiger Induktion. Für $n=2$ haben wir $(1+x)^{2}=1+2x+x^{2}>1+2x$, da $x^{2}>0$. Es gelte also $(1+x)^{n}>1+nx$. Multiplikation mit $1+x$ liefert.
$$
(1+x)^{n+1}>(1+nx)(1+x)=1+(n+1)x+nx^{2}>1+(n+1)x
$$
wie behauptet.

Mit Hilfe der Bernoulli'schen Ungleichung lässt sich zeigen, dass $\left( 1+ \frac{1}{n} \right)^{n}$ eine monoton wachsende Folge ist. Es gilt
$$
\frac{\left( 1+ \frac{1}{n+1} \right)^{n+1}}{\left( 1 + \frac{1}{n} \right)^{n}} = \left(1 + \frac{1}{n}\right) \left(\frac{1+ \frac{1}{n+1}}{1 + \frac{1}{n}}\right)^{n+1} = \left(1 + \frac{1}{n}\right)\left(1 - \frac{1}{(n+1)^{2}}\right)^{n+1}
$$$$
> \left(1 + \frac{1}{n}\right)\left(1 - \frac{1}{n+1}\right) = \frac{n+1}{n}\cdot \frac{n}{n+1}=1
$$
Daraus folgt, dass $\left( 1+\frac{1}{n} \right)^{n}$ streng monoton wächst. Weiters erhalten wir mit Hilfe des binomischen Lehrsatzes
$$
\left(1+ \frac{1}{n}\right)^{n} = 1 + \binom{n}{1} \frac{1}{n}+ \binom{n}{2} \frac{1}{n^{2}}+\binom{n}{3} \frac{1}{n^{3}}+\dots+\binom{n}{n} \frac{1}{n^{n}}
$$
$$
<1+1+\frac{1}{2}+\frac{1}{2^{2}}+\dots+\frac{1}{2^{n-1}}<3
$$
Die Folge ist daher nicht nur monoton wachsend, sondern überdies noch nach oben beschränkt und daher konvergent. Den Grenzwert $e=2.7182818$ nennt man die #Eulersche_Zahl.

