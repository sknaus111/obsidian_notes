Eine algebraische Struktur $(M,\land,\lor)$ heißt #Verband, wenn folgende Eigenschaften erfüllt sind:
- (i) $(M,\land)$ ist eine kommutative Halbgruppe
- (ii) $(M,\lor)$ ist eine kommutative Halbgruppe, und
- (iii) es gelten die #Verschmelzungsgesetze 
  $$
a = a \land (a \lor b)
$$ $$
a = a \lor (a \land b)
$$  für alle $a,b \in M$

## Beispiele
$(P(A),\cap,\lor)$ ist für jede Menge $A$ ein Verband

$M=\mathbb{N}$ mit $a \land b=min(a,b)$ und $a \lor b=max(a,b)$ ist ein Verband

$M=\mathbb{N}\setminus\{ 0 \}$ mit $a\land b=ggT(a,b)$ und $a \lor b=kgV(a,b)$ ist ein Verband

$B=\{ 0,1 \}$ mit den Operationen $\land,\lor$ ist ein Verband ebenso wie $B^{n}=\{ (x_{1},x_{2},\dots) \}$


## Infimum und Supremum
Es besteht ein enger Zusammenhang zwischen Vernänden und Halbordnungen, nämlich solchen, die zu je zwei Elementen $a,b$ ein #Infimum $inf(a,b)$ und ein #Supremum $sup(a,b)$ besitzen.

Ein Element $c$ einer Halbordnung heißt Infimum zweier Elemente $a,b$ wenn $c\leq a$ und $c\leq b$ ist und für jedes Element $d$ mit $d\leq a$ und $d\leq b$ auch $d\leq c$ gilt.

Enstprechend heißt ein Element $\overline{c}$ Supremum zweier Elemente $a,b \in M$, wenn $a\leq \overline{c}$ und $b\leq \overline{c}$ ist und für jedes Element $\overline{d}$ mit $a\leq \overline{d}$ und $b\leq \overline{d}$ auch $\overline{c}\leq \overline{d}$ gilt.

Sei $(M,\land, \lor)$ ein Verband. Dann wird auch
$$
a\leq b \iff a = a \land b
$$
auf $M$ eine Halbordnung definiert. In dieser Halbordnung gibt es zu je zwei Elementen ein Infimum, nämlich $inf(a,b) = a \land b$, und ein Supremum $sup(a,b)=a\lor b$.
Ist umgekehrt $\leq$ eine Halbordnung auf $M$ wird mit der Eigenschaft, dass es zu je zwei Elementen ein Infimum und ein Supremum gibt, so ist $M$ mit den Operationen $a \land b=inf(a,b)$ und $a \lor b=sup(a,b)$ ein Verband.

### Beweis
Wegen $a \land a = a$ gilt zunächst $a\leq a$. Ist weiters $a\leq b$ und $b\leq a$, so folgt $a=a\land b=b\land a=b$. Damit ist $\leq$ reflexiv und antisymmetrisch.
Es sei nun $a\leq b$ und $b\leq c$, also $a \land b=a$ und $b \land c = b$. Aus dem Assoziativgesetz folgt dann $a \land c = (a\land b)\land c=a\land(b\land c)=a\land b=a$. Also gilt auch $a\leq c$, womit die Transitivität von $\leq$ nachgewiesen ist.
Setzt man nun $c=a\land b$, so gilt sicherlich $c\leq a$, da $c\land a=(a\land b)\land a=a\land b=c$ ist. Ebenso gilt $c\leq b$. Ist nun $d\leq a$ und $d\leq b$, also $d\land a=d$ und $d\land b=d$, so folgt $d=d\land d=(d\land a)\land(d\land b)=d\land(a\land b)$, also $d\leq c=a\land b$. Daher ist $c=a\land b=inf(a,b)$. Aus den Verschmelzungsgesetzen erhält man unmittelbar $a \land b = a \iff a \lor b=b$, also $a\leq b \iff a \lor b = b$. Daraus ergibt sich mit analogen Überlegungen wie zuvor $sup(a,b)=a \lor b$. Die Relation $\leq$ erfüllt daher alle geforderten Eigenschaften. Ist nun umgekehrt $(H,\leq)$ eine solche Halbordnung, so überlegt man leicht, dass die Operationen $\land = inf$ und $\lor = sup$ alle Eigenschaften eines Verbandes haben. Beispielsweise muss $inf(a,sup(a,b))=a$ nachgeprüft werden. Dies ist aber aus der Definition von $inf$ und $sup$ direkt ersichtlich. Die Details werden dem Leser überlassen.

## Hassediagramme
Da jede Halbordnung durch ein #Hassediagramm dargestellt werden kann, ist es auch möglich, einen Verband durch das Hassediagramm der entsprechenden Halbordnungen zu repräsentieren.

$M=\{ 1,2,3,4,6,12 \}$ mit $a\land b=ggT(a,b)$ und $a\lor b=kgV(a,b)$ ist ein Verband.

```tikz
\begin{document} \begin{tikzpicture}

% Knoten 
\node (a) at (0, 0) {1}; 
\node (b) at (2, 2) {2}; 
\node (c) at (-2, 2) {3}; 
\node (d) at (4, 4) {4}; 
\node (e) at (0, 4) {6}; 
\node (f) at (2, 6) {12}; 

\draw (a) -- (b);
\draw (a) -- (c);
\draw (b) -- (d);
\draw (b) -- (e);
\draw (c) -- (e);
\draw (d) -- (f);
\draw (e) -- (f);


\end{tikzpicture} 
\end{document}
```

## Distributiver Verband
Ein Verband $(M,\land,\lor)$ heißt #distributiver_Verband, wenn die #Distributivgesetze für alle $a,b,c \in M$ gelten.
$$
a \land(b \lor c)=(a \land c) \lor (b \land c)
$$
$$
a \lor (b\land c)=(a\lor b)\land(a\lor c)
$$
### Beispiel
Folgender Verband ist nicht Distributiv. Es gilt $a \land (b \lor c)=a \land 1=a$, aber $(a \land b) \lor (a\land c)=0 \lor 0=0$

```tikz
\begin{document} \begin{tikzpicture}

% Knoten 
\node (a) at (0, 0) {0}; 
\node (b) at (-2, 2) {a}; 
\node (c) at (0, 2) {b}; 
\node (d) at (2, 2) {c}; 
\node (e) at (0, 4) {1}; 

\draw (a) -- (b);
\draw (a) -- (c);
\draw (a) -- (d);
\draw (b) -- (e);
\draw (c) -- (e);
\draw (d) -- (e);


\end{tikzpicture} 
\end{document}
```
Gewisse Verbände haben außer den Distributivgesetzen noch weitere Eigenschaften. Beispielsweise hat der Verband $(P(A),\cap,\cup)$ die ganze Menge $A$ als gemeinsame obere Schranke und die leere Menge $\emptyset$ als gemeinsame untere Schranke. Diese Elemente sind dann natürlich neutrale Elemente für $\cap$ und $\cup$. Weiers gibt es zu jeder Menge $B \in P(A)$ das Komplement $B'=A\setminus B$ mit den Eigenschaften $inf(B,B')=B\cap B'=\emptyset$ und $sup(B,B')=B \cup B' = A$. Der Verband $(P(A),\cap, \cup)$ bildet eine so genannte #Boolesche_Algebra

## Boole'sche Algebra
Ein distributiver Verband $(M,\land,\lor)$ heißt #Boolesche_Algebra, wenn er die folgenden beiden zusätzlichen Eigenschaften besitzt.

- (i) Es gibt ein neutrales Element $1 \in M$ bezüglich $\land$, und es gibt ein neutrales Element $0 \in M$ bezüglich $\lor$
- (ii) Zu jedem $a\in M$ gibt es ein Komplement $a'\in M$ mit $$
  a\lor a'=1 ~~~~~\text{ und }~~~~~a\land a'=0$$
Eine Boole'sche Algebra $(M,\land,\lor)$ hat die folgenden Eigenschaften

- (i) Für alle $a\in M$ gilt $a \lor 1=1$ und $a \land 0=0$
- (ii) Gelten für ein $b\in M$ die Beziehungen $a \lor b=1$ und $a \land b=0$, so ist $a'=b$
- (iii) Für alle $a\in M$ gilt $(a')'=a$
- (iv) Für alle $a,b\in M$ gelten die DeMorgan'schen Regeln $$
(a\land b)'=a'\lor b'
$$ $$
(a \lor b)'=a'\land b'
$$
### Beweis
Es folgt aus den Verschmelzunsgesetzen: $a \lor1=(a\land1)\lor1=1$ und $a\land0=(a \lor 0) \land 0=0$
Es sei nun $b\in M$ mit $a \lor b=1$ und $a \land b=0$. Weiters bezeichne $\leq$ die zu $M$ gehörige Halbordnung. Aus $$
a'=a'\land1=a'\land(a\lor b)=(a'\land a)\lor(a'\land b)=0\lor(a'\land b)=a'\land b
$$
folgt $a'\leq b$. Analog ergibt sich $b=b\land a'$, also $b\leq a'$. Insgesamt folgt $a'=b$. Diese Eigenschaft impliziert aber auch $(a')'=a$
Schließlich rechnet man mit Hilfe des Distributivgesetzes nach, dass $(a'\lor b')\lor(a\land b)=1$ und $(a'\lor b')\land(a\land b)=0$ gilt. Daraus folgt $(a\land b)'=a'\lor b'$. In analoger Weise zeigt man $(a\lor b)'=a'\land b'$

### Beispiel
$(B^{n},\land,\lor)$ ist für jedes $n$ in den natürlichen Zahlen eine Boole'sche Algebra. Interessanterweise sind dies (bis auf Isomorphie) alle endlichen Boole'schen Algebren, wie der folgende Satz, den wir ohne Beweis angeben, besagt.

Jede endliche Boole'sche Algebra ist zu $(B^{n},\land,\lor)$ für ein $n\in \mathbb{N}$ isomorph, d.h. es gibt nur endliche Boole'sche Algebren der Ordnung $2^{n}~~~(n\in \mathbb{N})$