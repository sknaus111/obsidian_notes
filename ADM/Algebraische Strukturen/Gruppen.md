Eine algebraische Struktur $(A,\circ)$ heißt 
- (i) #Halbgruppe, wenn sie assoziativ ist, also (i) aus [[Binäre Operationen#Rechenregeln]] erfüllt.
- (ii) #Monoid, wenn sie assoziativ ist und ein neutrales Element besitzt, also (i) und (ii) aus [[Binäre Operationen#Rechenregeln]] erfüllt.
- (iii) #Gruppe, wenn sie assoziativ ist, ein neutrales Element und zu jedem Element ein Inverses besitzt, also (i), (ii) und (iii) aus [[Binäre Operationen#Rechenregeln]] erfüllt.
Erfüllt eine der Strukturen Gruppoid, Halbgruppe, Monoid bzw. Gruppe auch das Kommutativgesetz (iv), so heißt sie kommutatives Gruppoid, Halbgruppe, Monoid bzw. Gruppe.

Kommutative Gruppen werden auch als #abelsche_Gruppen bezeichnet.
## Beispiele

- a) $(A, \circ)$ mit $A=\mathbb{N}\setminus\{ 0 \}$ und $a \circ b=a^{b}$ ist ein Gruppoid.

- b) $(\mathbb{N}\setminus\{ 0 \},+)$ ist eine Halbgruppe. $(\mathbb{N},+)$ und $(\mathbb{N}, *)$ sind Monoide.

- c) Sei $\Sigma$ eine Menge, genannt Alphabet, und bezeichne $\Sigma ^{*}$ die Menge aller endlichen Wörter über $\Sigma$, das sind alle endlichen Folgen $x_{1}x_{2}\dots x_{k}$ mit $x_{j}\in \Sigma (1\leq j \leq k)$ ergänz um das leere Wort $\varepsilon$. Sind $w_{1}=x_{1}x_{2}\dots x_{k}$ und $w_{2}=y_{1}y_{2}\dots y_{l}$ zwei Wörter in $\Sigma ^{*}$, so definiert man$$
w_{1}\circ w_{2}=x_{1}x_{2}\dots x_{k}y_{1}y_{2}\dots y_{l} \in \Sigma*
$$ $(\Sigma*, \circ)$ ist damit ein Monoid mit neutralem Element $\epsilon$. Man bezeichnet $\Sigma*$ auch als #freies_Monoid über dem Alphabet $\Sigma$.

- d) $(\mathbb{Z}, +),(\mathbb{Q},+),(\mathbb{Q}\setminus \{ 0 \},*),(\mathbb{R},+),(\mathbb{R}\setminus \{ 0 \},*)$ sind abelsche Gruppen.

- e) Die Menge aller $n \times n$-Matrizen $\mathbb{R}^{n\times n}$ mit Koeffizienten aus $\mathbb{R}$ bildet mit der Matrizenaddition eine Gruppe. Außerdem bilden jene $n \times n$-Matrizen $A$ mit $\det(A)\not=0$ bezüglich der Matrizenmultiplikation eine Gruppe. Diese ist für $n\geq 2$ nicht kommutativ

- f) Sei $M$ eine beliebige Menge. Dann bildet $(P(M),\vartriangle)$, d.h. aller Teilmengen von $M$ mit der symmetrischen Mengendifferenz, eine Gruppe. Das neutrale Element ist $\emptyset$, und jedes Element ist zu sich selbst invers.

- g) Die Menge $S_{n}$ der Permutationen der Zahlen $\{ 1,2,\dots,n \}$ ist die Menge der bijektiven Abbildungen $\pi: \{ 1,2,\dots,n \}\rightarrow \{ 1,2,\dots,n \}$. Führt man zwei bijektive Abbildungen hintereinander aus, erhält man wieder eine bijektive Abbildung. $(S_{n},\circ)$ bildet die so genannte symmetrische Gruppe. Die identische Abbildung $id(j)=j$ ist das neutrale Element.

- h) Die #Symmetriegruppe eines gleichseitigen Dreiecks besteht aus allen Isometrien (das sind längen- und winkeltreue Abbildungen) der Ebene, die ein gleichseitiges Dreieck auf sich selbst abbilden. Da ein Dreieck durch seine Eckpunkte eindeutig gegeben ist, reicht es aus, die Auswirkung solcher Isometrie auf die Eckpunkte zu betrachten. Es entstehen gewisse Permutationen der Eckpunkte $\{ 1,2,3 \}$. Bei den Drehungen um $0°,120°$ und $240°$ werden die Eckpunkte zyklisch vertauscht, und bei den Spiegelungen an den drei Höhen werden jeweils zwei Eckpunkte miteinander vertauscht. Insgesamt erhält man also sechse verschiedene Symmetrien, die bezüglich Hintereinanderausführung eine Gruppe bilden. In diesem speziellen Fall eines gleichseitigen Dreiecks ist die Symmetriegruppe nicht anderes als die symmetrische Gruppe auf den drei Eckpunkten.

## Operationstafeln
Kleine algebraische Strukturen lassen sich mit Hilfe sogenannter #Operationstafeln definieren.

| $\circ$ | e   |
| ------- | --- |
| e       | e   |

| $\circ$ | e   | a   |
| ------- | --- | --- |
| e       | e   | a   |
| a       | a   | e   |

| $\circ$ | e   | a   | b   |
| ------- | --- | --- | --- |
| e       | e   | a   | b   |
| a       | a   | b   | e   |
| b       | b   | e   | a   |

| $\circ$ | e   | a   | b   | c   |
| ------- | --- | --- | --- | --- |
| e       | e   | a   | b   | c   |
| a       | a   | b   | c   | e   |
| b       | b   | c   | e   | a   |
| c       | c   | e   | a   | b   |

| $\circ$ | e   | a   | b   | c   | d   |
| ------- | --- | --- | --- | --- | --- |
| e       | e   | a   | b   | c   | d   |
| a       | a   | b   | c   | d   | e   |
| b       | b   | c   | d   | e   | a   |
| c       | c   | d   | e   | a   | b   |
| d       | d   | e   | a   | b   | c   |

| $\circ$ | e   | a   | b   | c   | d   | f   |
| ------- | --- | --- | --- | --- | --- | --- |
| e       | e   | a   | b   | c   | d   | f   |
| a       | a   | b   | c   | d   | f   | e   |
| b       | b   | c   | d   | f   | e   | a   |
| c       | c   | d   | f   | e   | a   | b   |
| d       | d   | f   | e   | a   | b   | c   |
| f       | f   | e   | a   | b   | c   | d   |

| $\circ$ | e   | a   | b   | c   | d   | f   |
| ------- | --- | --- | --- | --- | --- | --- |
| e       | e   | a   | b   | c   | d   | f   |
| a       | a   | e   | d   | f   | b   | c   |
| b       | b   | f   | e   | d   | c   | a   |
| c       | c   | d   | f   | e   | a   | b   |
| d       | d   | c   | a   | b   | f   | e   |
| f       | f   | b   | c   | a   | e   | d   |

## Untergruppen
Eine nichtleere Teilmenge $U \subseteq G$ einer Gruppe $(G, \circ)$ heißt #Untergruppe von $G$, wenn $(U,\circ)$ selbst eine Gruppe ist. Man schreibt dafür auch $(U,\circ) \leq (G,\circ)$ oder nur $U\leq G$.

Man beachte, dass es immer zwei so genannte #triviale_Untergruppen gibt: $\{ e \}\leq G$ und $G \leq G$.

### Beispiel
Für $m \in \mathbb{N}$ bilden die Mengen $m\mathbb{Z} = \{ 0,\pm m,\pm2m,\pm3\mathbf{m}\dots \}$ Untergruppen von $(\mathbb{Z}, +)$

Um zu überprüfen ob eine Teilmenge $U$ eine Untergruppe bildet, muss untersucht werden ob für je zwei Elemente $a,b \in U$ ihre Verknüpfung $a \circ b$ in der Teilmenge ist, sowie die inverse $a^{-1}$. Gilt dies so ist auch das neutrale Element in der Teilmenge. Beispielsweise sind die Restklassen Untergruppen der ganzen Zahlen.

### Definitionen für Untergruppen
Sei $(G, \circ)$ Gruppe, $U$ Untergruppe von $G$ und $a \in G$. Dann heißt

#Linksnebenklasse von $U$ und $G$:
$$
a \circ U = \{ a \circ u | u \in U \}
$$
#Rechtsnebenklasse von $U$ und $G$:
$$
U \circ a = \{  u \circ a | u \in U \}
$$
Diese Nebenklassen bilden eine Zerlegung von $G$. Die Relation $a \thicksim b \iff a \circ U = b \circ U$ ist die entsprechende Äquivalenzrelation für die Linksnebenklassen. 
Der Index einer Untergruppe kann wie folgt definiert werden.
Sei $(G, \circ)$ eine endliche Gruppe und $U\leq G$. Die Anzahl der Links- bzw. Rechtsnebenklassen von $U$ und $G$ wird als #Index $|G:U|$ von $G$ nach $U$ bezeichnet, Die Anzahl $|G|$ der Elemente einer Gruppe wird als #Ordnung von $G$ bezeichnet.

### Satz von Lagrange 
Ist $(G,\circ)$ endliche Gruppe, so ist die Ordnung $|U|$ einer Untergruppe $U\leq G$ stets ein Teiler der Gruppenordnung $|G|$, und es gilt $|G:U|=|G|/|U|$.

#### Beweis des Satzes von Lagrange
Die Abbildung $U \rightarrow a \circ U, x \rightarrow a \circ u$ ist wegen der Gruppeneigenschaft eine bijektive Abbildung. Es gilt daher bei einer endlichen Gruppe immer $|a\circ U|=|U|$, d.h. die Linksnebenklassenzerlegung zerlegt die Gruppe $G$ in $m=|G:U|$ gleich große Teilmengen. Offensichtlich folgt dann $|G|=m|U|$. Für Rechtsnebenklassen ist die Überlegung ganz analog, insbesondere ist die Anzahl der Linksnebenklassen gleich der Anzahl der Rechtsnebenklassen.


### Potenzen
Sei $(G,\circ)$ Gruppe mit neutralem Element $e$. Für $a \in G$ werden die #Potenzen $a^{n}$ von $a$ mit $n \in \mathbb{Z}$ folgendermaßen definiert.

$a^{n} = \left\{ \begin{matrix} e & \text{ für }n=0 \\ a & \text{ für }n=1 \\ a^{n-1}\circ a & \text{ rekursiv für }n>1 \\ (a^{-1})^{-n} & \text{ für }n<0 \end{matrix} \right\}$

Wird das Operationssymbol $+$ verwendet, so schreibt man statt $a^{n}$ auch $n~a$, z.B. $3~a$ für $a+a+a$. Mit Hilfe der Beweismethode der vollständigen Induktion folgt für alle ganzen Zahlen $n,m$.

$$
a^{n+m}=a^{n}\circ a^{m} \text{ und } (a^{m})^{n} = a^{m~n}
$$
Aus der ersten Regel $a^{m+n}=a^{m}\circ a^{n}$ folgt, dass die Menge der Potenzen $<a> = \{  a^{n} | n \in \mathbb{Z} \}$ eine Untergruppe von $G$, die von $a$ erzeugt Untergruppe, bildet. Diese Untergruppe ist immer kommutativ, auch wenn $G$ nicht kommutativ ist.
Sind alle Potenzen $a^{n} (n\in \mathbb{Z})$ voneinander verschieden, so bildet diese Untergruppe eine Teilmenge von $G$, die als Kopie der ganzen Zahlen $\mathbb{Z}$ gesehen werden kann (falls man jede Potenz $a^{n}$ mit ihrem Exponenten $n$ identifiziert). Es muss aber nicht sein, dass alle Potenzen $a^{n}$ voneinander verschieden sind. Es sei also z.B. $a^{m}=a^{n}$ für ganze Zahlen $m<n$. Multipliziert man diese Beziehung mit $a^{-m}$, so erhält man $a^{n-m}=e$. Es gibt daher eine ganze Zahl $k>0$ mit $a^{k}=e$. Dies motiviert die folgende Definition.
Sei $(G,\circ)$ Gruppe und $a \in G$. Sind alle Potenzen $a^{n} (n\in \mathbb{Z})$ voneinander verschieden, so hat $a$ #unendliche_Ordnung $ord_{G}(a)=\infty$. Andernfalls bezeichnet man 
$$
ord_{G}(a)=min\{ k>0|a^{k}=e \}
$$
als #Ordnung von $a$. Das Element $a$ hat dann #endliche_Ordnungen.

Hat $a \in G$ unendliche Ordnung, so ist auch die von $a$ erzeugt Untergruppe $<a> = \{ a^{n}|n\in \mathbb{Z} \}$ unendlich. Bei endlicher Ordnung, $ord_{G}(a)$ ist $<a>$ die von $a$ erzeugt Untergruppe, da die Potenzen $a^{n}$ wegen $a^{n+ord_{G}(a)}=a^{n}$ zyklisch bzw. periodisch mit Periode $ord_{G}(a)$ wieder auftreten.
$$
<a> = \{ a^{n}|0\leq n<ord_{G}(a) \}
$$
Man beachte, dass in allen Fällen folgendes gilt.
$$
|<a>|=ord_{G}(a)
$$
Insbesondere ist daher $ord_{G}(a)$ ein Teiler der Gruppenordnung $|G|$. Daraus leitet sich der kleine Fermat'sche Satz der Gruppentheorie ab.

### Kleiner Fermat'scher Satz
Für jedes Element $a\in G$ einer endlichen Gruppe $(G,\circ)$ gilt $a^{|G|}=e$

#### Beweis des kleinen Fermat'schen Satz
Es bezeichne $U= <a>, k= ord_{G}(a) = |<a>|$ und $m=|G:U|$. Dann gilt $km=|G|$. Aus $a^{k}=e$ erhält man nun direkt $a^{|G|}=(a^{k})^{m}=e^{m}=e$

### Zyklische Gruppen
Gruppen bzw. Untergruppen der Form $<a>$ bezeichnet man als #zyklische_Gruppe, wenn es ein $a \in G$ mit $G=<a>$ gibt, d.h.  wenn $G$ von $a$ erzeugt wird.
### Normalteiler
Eine Untergruppe $N$ einer Gruppe $G$ heißt #Normalteiler, wenn die Linksnebenklassen und Rechtsnebenklassen übereinstimmen. man schreibt dafür kurz $N \trianglelefteq G$

Offensichtlich ist jede Untergruppe einer kommutativen Gruppe $G$ ein Normalteiler. Weiters ist jede Untergruppe $N$ mit Index $|G:N|=2$ Normalteiler, da es in diesem Fall nur zwei Linksnebenklassen bzw. Rechtsnebenklassen gibt. Die eine ist $e \circ N = N \circ e = N$ und die andere $G\setminus N$. Die wesentliche Eigenschaft von Normalteilern ist, dass man mit ihnen in derselben Weise wie mit Restklassen $\overline{a}=a+m\mathbb{Z}$ rechnen kann. Es seien $a\circ N=N\circ a$ und $b\circ N=N\circ b$ zwei Nebenklassen von $N$ und $a_{2} \in a \circ N$ und $b_{2} \in b \circ N$. Dann liegt das Produkt $a_{2}\circ b_{2}\in (a\circ N) \circ (b \circ N)$. Wegen der Normalteilereigenschaft gilt aber
$$
(a \circ N) \circ (b \circ N)=(N \circ a)\circ(b \circ N)
$$
$$
=(N\circ (a \circ b)) \circ N
$$
$$
=(a \circ b)\circ(N \circ N)
$$
$$
=(a \circ b)\circ N
$$
d.h. das Produkt $a_{2} \circ b_{2}$ liegt wieder in einer Nebenklasse, nämlich $(a\circ b)\circ N$, und diese ist nicht von der Wahl von $a_{2}$ und $b_{2}$ anhängig. Mit Hilfe dieser Eigenschaft von Normalteilern kann auch auf die Menge der Nebenklassen eine Gruppenoperation definiert werden.

Sei $N$ Normalteiler einer Gruppe $G$ und bezeichne $G / N$ die Menge der Nebenklassen von $G$ nach $N$. Dann wird durch die Operation
$$
(a \circ N) \circ (b \circ N)=(a \circ b) \circ N
$$
eine Gruppenoperation auf $G / N$ definiert. Die Gruppe $(G / N,\circ)$ heißt #Faktorgruppe von $G$ nach $N$.

$e\circ N=N$ ist das neutrale Element und $a^{-1}\circ N$ ist die inverse Nebenklasse von $a \circ N$

#### Beispiel
Sei $G=(\mathbb{Z},+)$ und $N=(m\mathbb{Z},+)$. Dann besteht $\mathbb{Z}\setminus m\mathbb{Z}=\mathbb{Z}_{m}$ aus $m$ Nebenklassen $\overline{0}=0+m\mathbb{Z}=m\mathbb{Z},\overline{1}=1+m\mathbb{Z},\dots,\overline{m-1}=m-1+m\mathbb{Z}$ den schon bekannten Restklassen modulo $m$. das Rechnen in der Faktorgruppe $\mathbb{Z}_{m}=\mathbb{Z}\setminus m\mathbb{Z}$ ist nichts anderes als das Addieren von Restklassen btw. das Addieren modulo $m$ 
Übrigens ist $(\mathbb{Z}_{m},+)$ eine endliche zyklische Gruppe, sie wird etwa von $\overline{1}=1+m\mathbb{Z}$ erzeugt.

## Homomorphismus
Eine Abbildung $\varphi: G \rightarrow H$ zwischen zwei Gruppen $(G,\circ)$ und $(H,*)$ heißt #Homomorphismus (oder #Gruppenhomomorphismus), wenn für alle $a,b \in G$ gilt.
$$
\varphi(a\circ b)=\varphi (a) * \varphi (b)
$$
Ist $\varphi$ bijektiv, so heißt $\varphi$ #Isomorphismus. Die inverse Abbildung $\varphi^{-1}:H \rightarrow G$ ist dann auch ein Isomorphismus. Existiert zwischen zwei Gruppen $G,H$ ein Isomorphismus, so heißten $G$ und $H$ #isomorph , und man schreibt dafür $G\cong H$.

### Beispiel
Sei $G$ Gruppe und $a \in G$. Dann ist die Abbildung $\varphi: \mathbb{Z} \rightarrow ⟨a⟩, n\rightarrow a^{n}$ ein Gruppenhomomorphismus. Sind alle Potenzen $a^{n}$ voneinander verschieden, so ist $\varphi$ bijektiv, also ein Isomorphismus, d.h. in diesem Fall gilt $⟨a⟩ \cong \mathbb{Z}$

### Weitere Definitionen des Homomorphismus
Ist $\varphi:G \rightarrow H$ ein Gruppenhomomorphismus, so wird das neutrale Element $e_{G}$ von $G$ auf das neutrale Element $e_{H}$ von $H$ abgebildet, d.h. $\varphi(e_{G})=e_{H}$. Weiters gilt $\varphi(a^{-1})=\varphi(a)^{-1}$ für alle $a\in G$

Aus $e_{G}\circ e_{G}=e_{G}$ folgt $\varphi(e_{G})*\varphi(e_{G})=\varphi(e_{G})$ und nach Multiplikation mit $\varphi(e_{G})^{-1}$ schließlich $\varphi(e_{G})=e_{H}$. Weiters folgt aus $a \circ a^{-1}=a^{-1}\circ a=e_{G}$, dass $\varphi(a)*\varphi(a^{-1})=\varphi(a^{-1})*\varphi(a)=e_{H}$ und damit $\varphi(a^{-1})=\varphi(a)^{-1}$.

Sei $\varphi: G \rightarrow H$ ein Gruppenhomomorphismus. Das Urbild $\varphi^{-1}(\{ e_{H} \})$ des neutralen Elementes $e_{H}$ wird als #Kern von $\varphi$ bezeichnet.
$$
ker(\varphi)=\{ a\in G|\varphi(a)=e_{H} \}
$$
Weiters nennt man das folgende, das #Bild von $G$ unter $\varphi$
$$
\varphi(G)=\{ b\in H|\exists a\in G:\varphi(a)=b \}
$$
Sei $\varphi:G\rightarrow H$ ein Gruppenhomomorphismus. Dann ist $ker(\varphi)$ ein Normalteiler von $G$ und $\varphi(G)$ eine Untergruppe von $H$.

#### Beweis 
$e_{G}$ ist sicher in $ker(\varphi)$ enthalten, also ist der Kern nie leer. Sind nun $a,b \in ker(\varphi)$, so gilt $\varphi(a\circ b)=\varphi(a)*\varphi(b)=e_{H}*e_{H}=e_{H}$ und $\varphi(a^{-1})=\varphi(a)^{-1}=e_{H}$. Daher ist $ker(\varphi)$ eine Untergruppe von $G$.
Sei nun $a\in ker(\varphi)$ und $c \in G$. Dann ist wegen $\varphi(e^{-1}\circ a \circ c)=\varphi(c)^{-1}*\varphi (a)*\varphi(c)=\varphi(c^{-1})*\varphi(c)=e_{H}$ auch $e^{-1}\circ a \circ c\in ker(\varphi)$. Also gilt $c^{-1} \circ ker(\varphi) \circ c \subseteq ker(\varphi)$ oder $ker(\varphi)\circ c \subseteq c \circ ker(\varphi)$. Vertauscht man nun die Rollen von $c$ und $c^{-1}$, so erhält man auch $c \circ ker(\varphi) \subseteq ker(\varphi) \circ c$ und schließlich $c \circ ker(\varphi)=ker(\varphi)\circ c$. Also ist $ker(\varphi)$ Normalteiler von $G$.

### Homomorphiesatz
Sei $\varphi: G \rightarrow H$ ein Gruppenhomomorphismus. Dann ist die Faktorgruppe $G\setminus ker(\varphi)$ zum Bild $\varphi(G)$ isomorph
$$
G/ ker(\varphi) \cong \varphi(G)
$$
Die Nebenklasse $a \circ ker(\varphi) \in G/ker(\varphi)$ entspricht dem Element $\varphi(a)\in \varphi(G)$. 

#### Beweis des Homomorphiesatzes
Man muss sich zunächst überlegen, dass die Abbildung $\psi:G/ker(\varphi) \rightarrow \varphi(G)$ mit $a \circ ker(\varphi)\rightarrow \varphi(a)$ wohldefiniert ist. Ist nämlich $a \circ ker(\varphi)=b\circ ker(\varphi)$, d.h. gibt es $c,d \in ker(\varphi)$ mit $a \circ c= b\circ d$, so folgt $\varphi(a)=\varphi(a)*e_{H}=\varphi(a\circ c)=\varphi(b\circ d)=\varphi(b)*e_{H}=\varphi(b)$.
Die Abbildung $\psi$ ist surjektiv, da jedes Element $\varphi(a) \in \varphi(G)$ als Bild von $a \circ ker(\varphi)$ auftritt. Die Abbildung $\psi$ ist auch injektiv. Ist nämlich $\varphi(a)=\varphi(b)$, so folgt $\varphi(a\circ b^{-1})=e_{H}$ also $a\circ b^{-1}\in ker(\varphi)$. Das wiederum impliziert $a \in b \circ ker(\varphi)$ und $a \circ ker(\varphi)\subseteq b \circ ker(\varphi)$. Vertauscht man nun die Rollen von $a$ und $b$, so erhält man auch die umgekehrte Inklusion und schließlich die Gleichheit: $a \circ ker(\varphi)=b\circ ker(\varphi)$.
Die Homomorphieeigenschaft $\psi((a\circ ker(\varphi))\circ(b\circ ker(\varphi)))=\Psi(a\circ ker(\varphi))*\Psi(b\circ ker(\varphi))$ ist nichts anderes als $\varphi(a \circ b)=\varphi(a) *\varphi (b)$.

#### Beispiel
Sei $G=\mathbb{Z}$ die Gruppe der ganzen Zahlen mit der Addition und $H=\{ 1,\zeta_{m},\zeta^{2}_{m},\dots,\zeta^{m-1}_{m} \}$ die endliche multiplikative zyklische Gruppe der $m$-ten Einheitswurzeln $(\zeta_{m}=e^{2\pi i/m})$. Dann ist $\varphi: G \rightarrow H,n \rightarrow \zeta_{m}^{n}$ ein surjektiver Homomorphismus mit $ker(\varphi)=m\mathbb{Z}$, da $\varphi(n)=\zeta_{m}^{n}=e^{2\pi in/m}=1$ genau dann gilt, wenn $n/m$ eine ganze Zahl, also ein ganzzahliges Vielfaches von $m$ ist. Nach dem Homomorphiesatz gilt daher $\mathbb{Z}_{m}=\mathbb{Z}/m\mathbb{Z}\cong H=⟨\zeta_{m}⟩$. Die Restklasse $\overline{a}$ entspricht der $a$-ten Potenz $\zeta_{m}^{a}$.

## Symmetrische Gruppen
Wir betrachten wieder die symmetrische Gruppe $S_{n}$ aller $n!$ Permutationen der Zahlen $\{ 1,2,\dots,n \}$, also alle bijektiven Funktionen $\pi :\{ 1,2,\dots,n \}\rightarrow \{ 1,2,\dots,n \}$. Es gibt daher verschiedene Darstellungen von Permutationen. Üblich ist vor allem die #zweistellige_Darstellung. Hier wird $\pi\in S_{n}$ durch eine zweizeilige Matrix dargstellt.
$$
\pi = \left(\begin{matrix}
1 & 2 & 3 & \dots & n-1 & n \\ \\
\pi(1) & \pi(2) & \pi(3) & \dots & \pi(n-1) & \pi(n)
\end{matrix}\right)
$$
Beispielsweise.
$$
\pi = \left(\begin{matrix}
1 & 2 & 3 & 4 & 5 \\ \\
3 & 5 & 4 & 1 & 2
\end{matrix}\right)
$$
In dieser Darstellung kann man die Gruppenoperationen leicht realisieren. Die inverse Permutation $\pi^{-1}$ erhält man etwa dadurch, dass man die beiden Zeilen(in der zweizeiligen Darstellung von $\pi$) vertauscht und dann spaltenweise ordnet
$$
\pi^{-1}=\left(\begin{matrix}
3 & 5 & 4 & 1 & 2 \\
1 & 2 & 3 & 4 & 5
\end{matrix}\right)
=\left(\begin{matrix}
1 & 2 & 3 & 4 & 5 \\
4 & 5 & 1 & 3 & 2
\end{matrix}\right)
$$
Ist $\sigma = \left(\begin{matrix}1&2&3&4&5\\4&2&5&1&3\end{matrix}\right)$ eine weitere Permutation, so bestimmt sich
$$
\sigma \circ \pi = \left(\begin{matrix}
1&2&4&4&5 \\
4&2&5&1&3
\end{matrix}\right)
\circ \left(\begin{matrix}
1 & 2 & 3 & 4 & 5 \\
3 & 5 & 4 & 1 & 2
\end{matrix}\right)
= \left(\begin{matrix}
1 & 2 & 3 & 4 & 5 \\
5 & 3 & 1 & 4 & 2
\end{matrix}\right)
$$
durch Hintereinanderausführe: z.B. ist $\pi(1)=3$ und $\sigma(3)=5$, also $\sigma \circ\pi=5$. Man kann eine Permutation $\pi \in S_{n}$ aber auch als gerichteten Graphen darstellen. Die Zahlen $\{ 1,2,\dots,n \}$ werden als Punkte(Knoten) dargestellt, und ist $j=\pi(i)$, so verläuft eine gerichtete Kante von $i$ nach $j$. Man beachte, dass von jedem Punkt genau eine Kante wegführt und zu jedem Punkt genau eine Kante hinführt. Der Graph muss daher in #Zyklen zerfallen. Im obigen Beispiel sind dies die Zyklen $1,\pi(1)=3,\pi(3)=4,\pi(4)=3,\pi(3)=1$ und $2,\pi(2)=5,\pi(5)=2$. Die Graphen von Permutationen haben daher eine sehr einfache Struktur. Sie bilden eine Menge von Zyklen, wobei natürlich auch Schlingen auftreten können, und zwar genau dann, wenn ein $j \in \{ 1,2,\dots,n \}$ auf sich selbst abgebildet wird d.h. $\pi(j)=j$. Solche Punkte heißen auch #Fixpunkte.
### Zyklendarstellung
Dies führt uns direkt zur #Zyklendarstellung einer Permutation. Da jede Permutation $\pi \in S_{n}$ in eine Menge von Zyklen zerfällt, genügt es, einfach diese anzugeben. Ist etwa $1,\pi(1),\pi(\pi(1)),\pi(\pi(\pi(1)))=\pi^{3}(1),\dots,\pi^{k-1}(1),\pi^{k}(1)=1$ der erste Zyklus, so stellt man diesen durch folgende Darstellung an.
$$
(1\pi(1)\pi^{2}(1)\dots \pi^{k-1}(1))
$$
Im obigen Beispiel es also die Zyklen $(1,3,4)$ und $(2,5)$. Schreibt man nun alle Zyklen von $\pi$ hintereinander an, so erhält man die Zyklendarstellung von $\pi$.
$$
\pi=(1,3,4)(2,5)
$$
Schreibt man die Zyklen in einer anderen Reihenfolge an, bzw. vertauscht man innerhalb eines Zyklus die Elemente zyklisch, so erhält man auch eine Zyklendarstellung dieser Permutation also z.B.
$$
\pi=(5,2)(3,4,1)
$$
die Menge der Zyklen wird dadurch ja nicht verändert. Man beachte auch, dass mit $\pi=(5,2)\circ(3,4,1)$ auch als Produkt der zyklischen Permutationen $(5,2)$ und $(3,4,1)$ dargestellt wird. Man bezeichnet eine Permutation als zyklisch, wenn sie nur aus einem Zyklus besteht. Daher kann jede Permutation als Produkt von zyklischen Permutationen dargestellt werden.
Wir definieren nun das #Signum (bzw. Vorzeichen) von $\pi \in S_{n}$ durch
$$
sgn(\pi):= \prod_{1\leq i< j\leq n} \frac{\pi(j)-\pi(i)}{j-i}
$$
Da $\pi$ bijektiv ist, treten bis auf die Reihenfolge und bis auf das Vorzeichen im Zähler dieselben Faktoren auf wie im Nenner. Daher ist $sgn(\pi)$ entweder 1 oder -1. Man nennt eine Permutation auch gerade, wenn das Signum 1 ist und ungerade, wenn das Signum -1 ist. Es gibt übrigens immer gerade und ungerade Permutationen (falls $n\geq2$ ist). Beispielsweise ist $sgn(id)=1$ und $sgn((1,2))=-1$. Man kann das Signum übrigens auch mit Hilfe der Fehlstände von $\pi$ berechnen. Ein Fehlstand von $\pi$ ist ein Paar ($i,j$) mit $i<j$ und $\pi(i)>\pi(j)$. Aus der Definition von $sgn$ ergibt sich direkt, dass bei einer geraden Anzahl von Fehlständen das Signum +1 ist, also $\pi$ gerade ist, und bei einer ungerade Anzahl den Wert -1 hat.
Die wichtigste Eigenschaft des Signums ist, dass für zwei Permutationen $\pi,\sigma \in S_{n}$ die folgende Beziehung gilt.
$$
sgn(\pi \circ\sigma)=\prod_{1\leq i<j\leq n}\frac{ (\pi \circ \sigma)(j)-(\pi \circ\sigma)(i)}{j-i}
$$
$$
=\prod_{1\leq i<j\leq n}\frac{ \pi(\sigma(j))-\pi(\sigma(i))}{\sigma (j)-\sigma(i)} ~~\cdot~~\prod_{1\leq i<j\leq n} \frac{\sigma(j)-\sigma(i)}{j-i}
$$
$$
sgn(\pi) \cdot sgn(\sigma)
$$
Die Abbildung $sgn$ ist daher ein Gruppenhomomorphismus zwischen der symmetrischen Gruppe $(S_{n},\circ)$ und er zwei-elementigen Gruppe $(\{ 1,-1 \},\cdot)$. Für $n\geq2$ ist dieser Homomorphismus auch surjektiv. Der Kern von $sgn$
$$
ker(sgn)=\{ \pi \in S_{n}|sgn(\pi)=1 \} =: A_{n}
$$
wird auch als #alternierende_Gruppe $A_{n}$ bezeichnet und umfasst alle gerade Permutationen. Aus dem Homomorphiesatz folgt, dass die Nebenklassenzerlegung von $A_{n}$ (für $n\geq2$) aus zwei Nebenklassen besteht, nämlich aus $A_{n}$, den geraden Permutationen, und $S_{n}\setminus A_{n}$, den ungeraden Permutationen. $A_{n}$ ist daher eine Untergruppe vom Index $|S_{n}:A_{n}|=2, A_{n}$ und $S_{n}\setminus A_{n}$ bestehen jeweils aus $n!/2$ Elementen. Es gibt daher genauso viele gerade wie ungerade Permutationen