## Allgemeines zu Vektoren
Eine ( #Spalte ) #Vektor $x$ im $n$-dimensionalen raum $\mathbb{R}^{3}$ hat $n$ Eintragungen von reellen Zahlen $x_{1},x_{2},\dots ,x_{n} \in \mathbb{R}$.
$$
x=\left( \begin{matrix}
x_{1} \\x_{2} \\ \vdots \\ x_{n}
\end{matrix}\right)
$$

Etwas allgemeiner betrachtet man für einen gegebenen Körper $K$ den $n$-dimensionalen Raum $K^{n}$ von Vektoren $x$ mit Eintragungen $\in K$. Der Körper $K$ heißt auch #Skalarkörper, und die Elemente aus $K$ heißen #Skalare.  Beispiele für $K$ sind
$$
\mathbb{R}^{2}=\left\{  x=\left(\begin{matrix}
x_{1} \\ x_{2}
\end{matrix} \right) | x_{1},x_{2}\in \mathbb{R}\right\}
$$
und
$$
\mathbb{R}^{3}=\left\{ x=\left(\begin{matrix}
x_{1} \\ x_{2} \\ x_{3}
\end{matrix}\right) | x_{1},x_{2},x_{3} \in \mathbb{R}\right\}
$$
Zwei Vektoren $x,y \in K^{n}$ werden koordinatenweise addiert.
$$
x+y=\left(\begin{matrix}
x_{1} \\ x_{2} \\ \vdots \\ x_{n}
\end{matrix}\right) + \left(\begin{matrix}
y_{1}\\y_{2}\\ \vdots \\ y_{n}
\end{matrix}\right) = \left(\begin{matrix}
x_{1}+y_{2} \\ x_{2}+y_{2} \\ \vdots \\ x_{n}+y_{n}
\end{matrix}\right)
$$
Geometrisch entspricht die Vektoraddition des aus der Physik bekannten #Parallelogrammregel für die Addition von Kräften. Weiters können Vektoren mit einem beliebigen Faktor $\lambda\in K$ multipliziert werden.

$$
\lambda \cdot x=\lambda \cdot \left(\begin{matrix}
x_{1}\\x_{2}\\ \vdots \\x_{n}
\end{matrix}\right) = \left(\begin{matrix}
\lambda x_{1}\\ \lambda x_{2} \\ \vdots \\ \lambda x_{n}
\end{matrix}\right)
$$Spezielle Vektoren sind der #Nullvektor $0$ und der additiv inverse Vektor $-x$
$$
0=\left(\begin{matrix}
0 \\ 0 \\ \vdots \\ 0
\end{matrix}\right)
$$
$$
-x = (-1) \cdot x = \left(\begin{matrix}
-x_{1} \\ -x_{2} \\ \vdots \\ -x_{n}
\end{matrix}\right)
$$
## Vektorräume

Sei $K$ ein Körper und $(V,+)$ eine abelsche Gruppe. Weiters werde jedem $\lambda \in K$ und $x \in V$ ein Produkt $\lambda \cdot x \in V$ zugeordnet. 
Die algebraische Struktur $(V,+,K)$ heißt #Vektorraum oder #linearer_Raum über $K$, wenn die folgenden Eigenschaften für alle $\lambda, \mu \in K$ und $x,y \in V$ erfüllt sind:

- (i) $\lambda \cdot (x+y)=\lambda \cdot x + \lambda \cdot y$
- (ii) $(\lambda +\mu) \cdot x=\lambda \cdot x+\mu \cdot x$
- (iii) $(\lambda \mu)\cdot x=\lambda \cdot(\mu \cdot x)$
- (iv) $1 \cdot x = x$


Insbesondere $K^{n}$ ein Vektorraum über $K$. 

### Erste Mediane
Sei $V=\mathbb{R}^{2}$ die Ebene und
$$
W=\left\{  x=\left(\begin{matrix}
x_{1} \\ x_{2}
\end{matrix}\right) \in \mathbb{R}^{2} | x_{1} = x_{2} \right\}
$$
die so genannte #erste_Mediane . Man erkennt, dass $W$ die Eigenschaften eines Vektorraums hat und man mit $W$ uneingeschränkt addieren und mit Skalaren multiplizieren kann. Sind $x$ und $y$ in $W$, also $x_{1}=x_{2}$ und $y_{1} = y_{2}$, dann gilt auch $x_{1}+y_{1}=x_{2}+y_{2}$ und $\lambda x_{1} = \lambda x_{2}$. Daher sind $x+y$ und $\lambda x$ in $W$ enthalten.

### Beispiel
Es sei nun $V=\mathbb{R}^{3}$ und $U=\{ x\in \mathbb{R}^{3} |x_{1}+x_{2}+x_{3}=0 \}$. Geometrisch ist $U$ eine Ebene durch den Ursprung. Auch in $U$ kann man uneingeschränkt addieren und mit Skalaren multiplizieren, ohne dass man $U$ verlässt. Sind $x$ und $y$ in $U$, so folgt aus $x_{1}+x_{2}+x_{3}=0$ und $y_{1}+x_{2}+y_{3}=0$ auch $(x_{1}+y_{2})+(x_{2}+y_{2})+(x_{3}+y_{3})=0$. Daher ist $x+y$ in $U$. Entsprechend ist $\lambda x_{1}+\lambda x_{2}+\lambda x_{3}=0$ und daher ist $\lambda \cdot x$ ebenfalls in $U$. Die Teilmenge $U$ bildet also einen Vektorraum.


### Teilräume
Sei $(V,+,K)$ ein Vektorraum und $U$ eine nichtleere Teilmenge von $V$. Bildet $(U,+,K)$ wieder einen Vektorraum, dann heißt $U$ #Unterraum oder #Teilraum von $V$.

Eine vereinfachte Schreibweise um zu zeigen dass $U$ ein Unterraum von $V$ ist, ist $U\leq V$. Dies kann überprüft werden ob $U$ noch einen Vektorraum bildet, wobei alle Vektoren nach Addition und Multiplikation noch in $U$ sind. Weiters gilt
$$
V\leq V ~~~~~ \text{ und } ~~~~~ \{ 0 \} \leq V
$$
Unterräume können durch lineare Gleichungen beschrieben werden. Diese werden auch mit #Verschobene_Unterräume, also Nebenklassen, die auch #Nebenräume genannt werden, bezeichnet.

### Nebenräume
Sei $U$ ein Unterraum eines Vektorraums $V$ und $x_{0}$ ein Vektor aus $V$. Die Menge
$$
N=x_{0}+U=\{ x_{0}+u|u\in U \}
$$
heißt #Nebenraum von $U$.

Unterräume und Nebenräume können aber nicht nur durch lineare Gleichungen beschrieben werden. Es sei nun $v \in \mathbb{R}^{3}$ ein Vektor. Dann bilden die skalaren Vielfachen von $v$
$$
[v]=\{ \lambda \cdot v|\lambda\in \mathbb{R} \}
$$
eine #Gerade, die vom Vektor $v$ aufgespannt wird. Wegen $\lambda_{1}\cdot v+\lambda_{2}\cdot v=(\lambda_{1}+\lambda_{2})\cdot v$ und $\lambda \cdot(\lambda_{1} \cdot v)=(\lambda \lambda_{1})\cdot v$ ist diese Gerade ein Unterraum von $V$. Die Menge $|v|$ ist übrigens der kleinste Unterraum von $V$, der den Vektor $v$ enthält, man bezeichnet ihn auch als den von $v$ #erzeugten_Unterraum. Verschiebt man diese Gerade um einen Vektor $x_{0}$, so erhält man eine allgemeine Gerade.
$$
y=x_{0}+[v]=\{ x=x_{0}+\lambda v|\lambda\in \mathbb{R} \}
$$
Sie geht durch die Spitze des Vektors $x_{0}$ und ist parallel zur ursprünglichen Geraden $[v]$. Der Vektor $x_{0}$ wird in diesem Zusammenhang auch #Ortsvektor genannt, und $v$ heißt #Richtungsvektor. Die Darstellung der Vektoren auf $g$ in der Form $x=x_{0}+\lambda \cdot v$ ist eine #Parameterdarstellung von $g$.

In ähnlicher Weise kann man auch eine Ebene in Parameterdarstellung angeben, dabei ist $x_{0}$ wieder ein Ortsvektor.
$$
\epsilon=\{ x=x_{0}+\lambda_{1}\cdot v_{1}+\lambda_{2}\cdot v_{2} | \lambda_{1},\lambda_{2} \in \mathbb{R} \}
$$
Die Vektoren $v_{1}$ und $v_{2}$ spannen einen Unterraum auf, und zwar eine Ebene, welche die Vektoren $v_{1}$ und $v_{2}$ enthält.
$$
[v_{1},v_{2}] = \{ \lambda_{1}v_{1}+\lambda_{2}v_{2} | \lambda_{1},\lambda_{2} \in \mathbb{R} \}
$$
Man beachte, dass $[v_{1},v_{2}]$ der kleinste Unterraum von $U$ ist, der $v_{1}$ und $v_{2}$ enthält.

Geometrische Objekte können in der analytischen Geometrie als Nebenräume betrachtet werden. Punkte werden als Nebenräume des Unterraums $\{ 0 \}$ interpretiert.

## Linearkombination
Es seien $v_{1},v_{2},\dots,v_{n}$ Elemente eines Vektorraums $V$ (über dem Körper $K$) und $\lambda_{1},\lambda_{2},\dots,\lambda_{n} \in K$. Dann heißt die Summe
$$
\lambda_{1} \cdot v_{1}+\lambda_{2}\cdot v_{2}+\dots+\lambda_{n}\cdot v_{n}=\sum_{i=1}^{n}\lambda_{i}\cdot v_{i}
$$
#Linearkombination der Vektoren $v_{1},v_{2},\dots,v_{n}$. Die Skalare $\lambda_{1},\lambda_{2},\dots ,\lambda_{n}\in K$ heißen #Koeffizienten der Linearkombination. Eine Linearkombination heißt #trivial, wenn alle Koeffizienten $\lambda_{i}=0$ sind. Andernfalls heißt sie #nichttrivial.

Die #lineare_Hülle $[M]$ einer nichtleeren Teilmenge $M$ von $V$ ist die Menge aller Vektoren, die durch die Linearkombination von Vektoren aus $M$ gebildet werden können. Weiters setzt man $[\emptyset]=\{ 0 \}$.

Beispielsweise ist $[v]=\{ \lambda \cdot v|\lambda\in K \}$ die lineare Hülle eines Vektors $v$ und $[v_{1},v_{2}]=\{ \lambda_{1}\cdot v_{1}+\lambda_{2}\cdot v_{2} | \lambda_{1},\lambda_{2} \in K \}$ die lineare Hülle von zwei Vektoren $v_{1},v_{2}$.

Sei $M$ eine Teilmenge eines Vektorraums $V$. Dann ist die lineare Hülle $[M]$ ein Unterraum von $V$, und zwar der kleinste Unterraum, der alle Vektoren von $M$ enthält.

### Beweis 
Ist $M=\emptyset$, so ist $[M]=0$ ein Unterraum von $V$. Andernfalls beobachtet man, dass die Summe von zwei Linearkombinationen, aber auch ein skalares Vielfaches einer Linearkombination wieder eine Linearkombination von Vektoren aus $M$ ist. Damit ist die lineare Hülle $[M]$ ein Unterraum. Weiters muss ein Unterraum, der alle Vektoren von $M$ enthält, auch alle Linearkombinationen von Vektoren aus $M$ enthalten. Demnach ist die lineare Hülle $[M]$ der kleinste Unterraum, der alle Vektoren aus $M$ enthält.