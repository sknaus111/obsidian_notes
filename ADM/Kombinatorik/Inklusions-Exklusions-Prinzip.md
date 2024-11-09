Es gilt die Beziehung
$$
|A \cup B |=|A|+|B|-|A\cap B|
$$
zur Beschreibung der Anzahl von Elementen zwischen zwei Mengen. Bei drei Mengen ist dies schon komplizierter.
$$
|A\cup B\cup C|=|A|+|B|+|C|-|A\cap B|-|A\cap C|-|B\cap C|+ |A\cap B\cap C|
$$
Im Allgemeinen sieht dieses Prinzip wie folgt aus.
## Siebformel
Es seien $A_{1}\dots A_{n}$ endliche Mengen
$$
\left|\bigcup_{i=1}^{n}A_{i}\right|=|A_{1}\cup A_{2}\cup\dots \cup A_{n}|
$$
$$
=\sum_{i=1}^{n}|A_{i}|\sum_{1\leq i< j\leq n}|A_{i}\cap A_{j}|+\sum_{1\leq i<j<k\leq n}|A_{i}\cap A_{j}\cap A_{k}|
$$
$$
\pm\dots+(-1)^{n-1}|A_{1}\cap A_{2}\cap\dots \cap A_{n}|
$$
$$
\sum_{\emptyset \not=I\subseteq\{1,2,\dots,n\}}(-1)^{|I|-1}\left|\bigcap_{i\in I} A_{i}\right|
$$
### Beweis 
Der Induktionsanfang ist bereits bekannt. Man nehme an die Siebformel ist für ein $n\geq2$ richtig.
Es folgt
$$
\left|\bigcup_{i=1}^{n+1}A_{i}\right|=\left|\bigcup_{i=1}^{n}A_{i}\cup A_{n+1}\right|
$$
$$
=\left|\bigcup_{i=1}^{n}A_{i}\right| + |A_{n+1}|-\left|\bigcup_{i=1}^{n}A_{i}\cap A_{n+1}\right|
$$
$$
=\sum_{\emptyset \not=I\subseteq \{ 1,2,\dots,n \}}(-1)^{|I|-1}\left|\bigcap_{i\in I}A_{i}\right|+|A_{n+1}|-\sum_{\emptyset\not= \subseteq \{ 1,2,\dots,n \}}(-1)^{|I|-1}\left|\bigcap_{i\in I}A_{i}\cap A_{n+1}\right|
$$
$$
=\sum_{\emptyset\not=J\subseteq \{ 1,2,\dots,n+1 \}}(-1)^{|J|-1}\left|\bigcap_{j\in J}A_{j}\right|
$$
Setzt man nun voraus das alle Mengen in einem Universum $E$ sind gilt für das Komplement $A_{1}\cup A_{2}\cup\dots \cup A_{n}$
$$
\left|\bigcap_{i=1}^{n}A_{i}^{'}\right|=\left|\left( \bigcup_{i=1}^{n}A_{i} \right)^{'}\right|=|E|-\left|\bigcup_{i=1}^{n}A_{i}\right|
$$
$$
=|E|-\sum_{\emptyset\not=I\subseteq \{ 1,2,\dots,n \}}(-1)^{|I|-1}\left|\bigcap_{i\in I}A_{i}\right|
$$
$$
=\sum_{I\subseteq \{ 1,2,\dots,n \}}(-1)^{|I|}\left|\bigcap_{i\in I}A_{i}\right|
$$

wobei der leere Durchschnitt als $\{ x\in E|\forall i\in \emptyset:x\in A_{i} \}=E$ gedeutet wird. Für $n=2$
$$
|A^{'}\cap B^{'}|=|E|-|A|-|B|+|A\cap B|
$$


### Beispiel mit Wörtern
Sei gesucht die Anzahl aller Wörter der Länge 4 aus den Buchstaben $\{ a,b,c,d,e \}$, welche mindestens ein $a,b$ oder $c$ enthalten. Die Menge $W$ soll alle Wörter der Länge 4 aus $a,b,c,d$ und $e$ enthalten. $W_{a}$ soll alle Wörter der Länge 4 ohne $a$, $W_{b}$ ohne $b$ usw.
Die Länge der Wörter in W welche mindestens ein $a,b$ oder $c$ enthalten ist nun $W_{a}^{'}\cap W_{b}^{'}\cap W_{c}^{'}$. 
$$
|W_{a}^{'}\cap W_{b}^{'}\cap W_{c}^{'}|=|W|-|W_{a}|-|W_{b}|-|W_{c}|+|W_{a}\cap W_{b}|+|W_{a}\cap W_{c}|+|W_{b}\cap W_{c}|-|W_{a}\cap W_{b}\cap W_{c}|
$$
Aus der Produktregel folgt unmittelbar $W=5^{4}$ und in analoger weise $|W_{a}|=|W_{b}|=|W_{c}|=4^4$, $|W_{a} \cap W_{b}|=|W_{a}\cap W_{c}|=|W_{b}\cap W_{c}|=3^4$ und $|W_{a}\cap W_{b}\cap_{Wc}|=2^4$
Daher gibt wie folgt versch. gesuchte Wörter
$$
5^4-3*4^4+3*3^4-2^4=84
$$

### Beispiel mit gleicher Stelle
Wie viele Permutationen von $n$ Elementen gibt es, so dass kein Element an seiner ursprünglichen Position steht. Auch spricht man von einer fixpunktfreien Permutation.
Bezeichne $P$ die Menge aller Permutationen von $n$ Elementen $\{ 1,2,\dots,n \}$ und $P_{j}~(1\leq j \leq n)$ die Menge der Permutationen aus P, wo das Element $j$ wieder an dieselbe Stelle kommt. Folglich ist $|P|=n!$ und $|P_{j}|=(n-1)!$.

Die fixprunkfreie Menge ist jene wo kein Element an dessen ursprünglicher Position steht also
$$
P_{1}^{'}\cap P_{2}^{'}\cap\dots \cap P_{n}^{'}
$$
Mit dem Inklusions-Exklusions-Prinzip können wir nun die Anzahl bestimmen.
Ist $I\subseteq \{ 1,2,\dots,n \}$ so beschreibt $\bigcap_{i\in I}P_{i}$ die Permutationen, wo die Elemente aus $I$ sicher festgehalten werden. Die anderen $n-|I|$ Elemente können aber beliebig umgeordnet werden. Daher gilt
$$
\left|\bigcap_{i\in I}P_{i}\right|=(n-|I|)!
$$
Daraus folgt
$$
|P_{1}^{'}\cap P_{2}^{_{'}}\cap\dots \cap P_{n}^{'}|=\sum_{I\subset \{ 1,2,\dots,n \}} (-1)^{|I|} \left|\bigcap_{i\in I}P_{i}\right|
$$
$$
=\sum_{k=0}^{n}(-1)^{k}\binom{n}{k}(n-k)!
$$
$$
=n!\sum_{k=0}^{n}\frac{(-1)^{k}}{k!}
$$
Schließlich ist zu betrachten, dass $\sum_{k=0}^{n} \frac{(-1)^{k}}{k!}$ die Partialsummer der unendlichen Reihe
$$
\sum_{k=0}^{\infty} \frac{(-1)^{k}}{k!}=e^{-1}=\frac{1}{e}=0.367879\dots
$$
Daher gilt
$$
|P_{1}^{'}\cap P_{2}^{'}\cap\dots \cap P_{n}^{'}|\approx \frac{n!}{e}\approx0.37*n!
$$
Somit sind ca. $37\%$ aller Permutationen fixpunktfrei, hat also jedes Element einen andere Stelle als zuvor.
### Beispiel mit Primfaktorzerlegung
Bereits vorher wurde [[Kongruenzen und Restklassen#Eulersche $ varphi$-Funktion]] besprochen
$$
\varphi(m)=|\{ a\in\mathbb{Z}|1\leq a\leq m,ggT(a,m) =1\}|
$$
Mit $m=p_{1}^{e_{1}}\dots p_{r}^{e_{r}}$ ist die Primfaktorzerlegung von $m$ beschrieben worden. Dann gilt
$$
\varphi(m)=m* \left(1- \frac{1}{p_{1}}\right)*\dots*\left(1- \frac{1}{p_{r}}\right)
$$
$$
=m-\sum_{j=1}^{r} \frac{m}{p_{j}}+\sum_{1\leq j_{1}< j_{2}\leq r} \frac{m}{p_{j_{1}}*p_{j_{2}}}\pm\dots+(-1)^r \frac{m}{p_{1}p_{2}\dots p_{r}}
$$
Diese Formel kann nun wieder bewiesen werden. Sei $E = \{ 1,2,\dots,m \}$ und für $1\leq j \leq r$ bezeichne $A_{j}$ die Menge jener Zahlen in $E$ die durch $p_{j}$ teilbar sind. Offensichtlich gilt $|A_{j}|=m/p_{j}$. Ist weiters $I \subseteq \{ 1,2,\dots,r \}$ so besteht $\bigcap_{j\in J}A_{j}$ genau aus jenen Zahlen in $E$, die durch alle $p_{j}, j\in I$ und damit auch durch das Produkt $\prod_{j \in I}p_{j}$ teilbar sind. Es gilt
$$
\left|\bigcap_{j\in I}A_{j}\right|=\frac{m}{\prod_{j\in I}p_{j}}
$$
Wendet man nun das Inklusions-Exklusions-Prinzip auf $\varphi(m)=|\bigcap_{j=1}^{r}A_{j}'|$ an erhält die Darstellung
$$
\varphi(m)=m-\sum_{j=1}^{r} \frac{m}{p_{j}}+\sum_{1\leq j_{1}< j_{2}\leq r} \frac{m}{p_{j_{1}}*p_{j_{2}}}\pm\dots+(-1)^r \frac{m}{p_{1}p_{2}\dots p_{r}}
$$
