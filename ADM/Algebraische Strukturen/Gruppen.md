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
