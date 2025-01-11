Wir betrachten zunächst eine Matrix $A\in K^{m\times n}$ und die Zuordnung
$$
x\in K^{n}\rightarrow f(x)=A\cdot x\in K^{m}
$$
Diese Abbildung $f:K^{n}\rightarrow K^{M}$ hat folgende zwei Eigenschaften

- (i) $f(x+y)=A\cdot(x+y)=A\cdot x+A\cdot y=f(x)+f(y)$
- (ii) $f(\lambda \cdot x)=A\cdot(\lambda \cdot x)=\lambda \cdot(A\cdot x)=\lambda \cdot f(x)$

Abbildungen, die diese Eigenschaften haben, werden als linear bezeichnet und treten in der einen oder anderen Form in vielen Bereichen der Mathematik auf

Eine Abbildung $f:V\rightarrow W$ zwischen zwei Vektorräumen $V$ und $W$ ist #linear, wenn sie die folgenden beiden Eigenschaften hat

- (i) $f(x+y)=f(x)+f(y)$
- (ii) $f(\lambda \cdot x)=\lambda \cdot f(x)$

Beispielsweise sind Drehungen und Spiegelungen, aber auch Projektionen linear. Eine einfache Eigenschaft linearer Abbildungen ist, dass Linearkombinationen auf Linearkombinationen abgebildet werden:
$$
f(\lambda_{1}\cdot x_{1}+\lambda_{2}\cdot x_{2}+\dots+\lambda_{k}\cdot x_{k})=\lambda_{1}\cdot f(x_{1})+\lambda_{2}\cdot f(x_{2})+\dots+\lambda_{k}\cdot f(x_{k})
$$
Dies führt zu folgender Beobachtung

## Fortsetzungssatz
Es sei $V$ ein $n$-dimensionaler Vektorraum und die Menge $B=\{ b_{1},b_{2},\dots,b_{n} \}$ eine Basis von $V$. Weiters sei $W$ ein Vektorraum, $f:V\rightarrow W$ linear, und $c_{j}=f(b_{j}), 1\leq j\leq n$, bezeichne die Bilder der Basisvektoren.
Ist $x=x_{1}\cdot b_{1}+x_{2}\cdot b_{2}+\dots+x_{n}\cdot b_{n}$, d.h. hat $x$ die Koordinaten $x_{1},x_{2},\dots,x_{n}\in K$, so gilt
$$
f(x)=x_{1}\cdot f(b_{1})+x_{2}\cdot f(b_{2})+\dots+x_{n}\cdot f(b_{n})=x_{1}\cdot c_{1}+x_{2}\cdot c_{2}+\dots+x_{n}\cdot c_{n}
$$
Umgekehrt vermittelt diese Formel bei beliebiger Wahl von $c_{j}\in W$ stets eine lineare Abbildung $f:V\rightarrow W$

Um eine lineare Abbildung $f:V\rightarrow W$ zu charakterisieren, ist es also ausreichend, die Bilder einer Basis zu kennen. Alles Weitere ergibt sich aus der Linearität. 
Dieses Prinzip ist bei linearen Abbildungen der Form $f(x)=A\cdot x$ noch deutlicher zu sehen. Hier geht man von der kanonischen Basis $E=\{ e_{1},e_{2},\dots,e_{n} \}$ aus und bildet $$f(e_{j})=A\cdot e_{j}=a_{j}$$

Das Bild des $j$-ten kanonischen Basisvektors ist also die $j$-te Spalte von $A$.

Umgekehrt kann einer linearen Abbildung eine Matrix zugeordnet werden, indem man die Bilder der kanonischen Basis bestimmt und zu einer Matrix zusammenfasst. Ist also $f:K^{n}\rightarrow K^{m}$ eine lineare Abbildung und 
$$
A=\left(f(e_{1}~~f(e_{2}~~\dots~~f(e_{n}))\right)
$$
so gilt für alle $x\in K^{n}$
$$
f(x)=A\cdot x
$$
Wir hatten früher schon beobachtet, dass das Produkt einer Matrix $A$ mit einem Vektor $x$ nichts anderes ist als die Linearkombination der Spalten von $A$, wobei die Koeffizienten die Koordinaten von $x$ sind. Dies entspricht hier genau der Beobachtung vom Fortsetzungssatz.

### Beispiele
#### a
Sei $f:\mathbb{R}^{2}\rightarrow \mathbb{R}^{2}$ die Drehung um den Winkel $\varphi$ gegen den Uhrzeigersinn. Dann ist
$$
A=\left(\begin{matrix}
f(e_{1}) & f(e_{2})
\end{matrix}\right)
=
\left(\begin{matrix}
\cos \varphi & -\sin \varphi \\
\sin \varphi  & \cos \varphi
\end{matrix}\right)
$$
die dazu gehörige Matrix, d.h. $A\cdot x$ ist der um den Winkel $\varphi$ gedrehte Vektor $x$

#### b 
Die Matrix $S=\left(\begin{matrix}1 & 0  \\0 & -1\end{matrix}\right)$ entspricht der Spiegelung an der $x_{1}$-Achse
#### c
Die Matrix $P=\left(\begin{matrix}1/2 & 1 / 2 \\1 / 2 & 1 / 2 \end{matrix}\right)$ projiziert auf die erste Mediane
## Hintereinanderausführung linearer Abbildungen
Offensichtlich ist die #Hintereinanderausführung $h=g \circ f$ zweier linearer Abbildungen $f$ und $g$ wieder eine lineare Abbildung. Ist insbesonder $f(x)=A\cdot x$ und $g(x)=B\cdot y$, so ist
$$
h(x)=g(f(x))=g(A\cdot x)=B\cdot (A\cdot x)=(B\cdot A)\cdot x=C\cdot x
$$
jene lineare Abbildung, die durch das Produkt $C=B\cdot A$ der beiden Matrizen $B$ und $A$ gebildet wird. Das Matrizenprodukt entspricht daher der Hintereinanderausführung von linearen Abbildungen.

### Koordinatenwechsel
Der #Koordinatenwechsel zwischen zwei verschiedenen Basen $B=\{ b_{1},b_{2},\dots,b_{n} \}$ und $C=\{ c_{1},c_{2},\dots,c_{n} \}$ eines $n$-dimensionalen Vektorraums $V$, also die Frage, wie man die Koordinaten $\Phi_{B}(x)$ in die Koordinaten $\Phi_{C}(x)$ umrechnet, kann ebenfalls mit Hilfe einer Matrizenmultiplikation gelöst werden. Formal geschieht der Koordinatenwechsel einfach durch die 
lineare Abbildung $\Phi_{C} \circ \Phi_{B}^{-1}:K^{n}\rightarrow K^{n}$. Dies kann aber durch eine Matrix

$$
T_{B,C} = \left(\begin{matrix}
\Phi_{C}(b_{1}) & \Phi_{C}(b_{2}) & \dots & \Phi_{C}(b_{n})
\end{matrix}\right)
$$
mit den Spalten $(\Phi_{c}\circ\Phi_{B}^{-1})(e_{j})=\Phi_{C}(b_{j})$ realisiert werden. Es gilt daher
$$
T_{B,C} \cdot \Phi_{B}(x)=\Phi_{C}(x)
$$
Abschließend definieren wir zwei wichtige Kenngrößen von linearen Abbildungen

## Kern und Bild
Es sei $f:V\rightarrow W$ eine lineare Abbildung. Die Mengen
$$
ker(f)=\{ x\in V|f(x)=0 \}
$$
und
$$
f(V)=\{ f(x)|x\in V \}
$$
heißen #Kern und #Bild von $f$. Die Dimension des Kerns und des Bilds sind der #Defekt und der #Rang von $f$
$$
def(f)=dim(ker(f))
$$
und
$$
rg(f)=dim(f(V))
$$
Es ist leicht zu sehen, dass $ker(f)$ und $f(V)$ Teilräume von $V$ bzw. $W$ sind. Defekt und Rang sind daher immer wohldefiniert. Außerdem entspricht der Rang einer linearen Abbildung der Form $f(x)=A\cdot x$ genau dem Rang der Matrix $A$, da die Spalten von $A$ die Bilder der kanonischen Basisvektoren sind und daher alle möglichen Bildvektoren aufspannen:
$$
rg(A)=rg(f)
$$
Rang und Defekt einer linearen Abbildung erfüllen eine einfache Beziehung
### Rangformel
Es sei $V$ ein eindlichdimensionaler Vektorraum und $f:V\rightarrow W$ eine lineare Abbildung. Dann gilt
$$
rg(f)+def(f)=dimV
$$
Eine lineare Abbildung $f:\mathbb{R}^{2}\rightarrow \mathbb{R}^{2}$ sei durch Angabe der zugehörigen Matrix
$$
A=\left(\begin{matrix}
1 & 2  \\
2 & 4
\end{matrix}\right)
$$
gegeben. Der Raum $ker(f)$ bestimmt sich durch die Gleichung $f(x)=A\cdot x=0$ und $f(\mathbb{R}^{2})$ ist die lineare Hülle der Spalten von $A$. Nach kurzer Rechnung erhält man
$$
ker(f)=\left[\left(\begin{matrix}
2 \\
-1
\end{matrix}\right)\right]
$$
und
$$
f(R^{2})=\left[\left(\begin{matrix}
1 \\
2
\end{matrix}\right)\right]
$$
Beide Räume haben Dimension 1, also $def(f)=rg(f)=1$. Offensichtlich ist die Rangformel erfüllt: $1+1=2$
