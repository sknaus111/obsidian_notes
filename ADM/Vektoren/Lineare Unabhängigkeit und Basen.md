## Lineare Unabhängigkeit
Zwei Vektoren sind linear unabhängig wenn $v_{2}$ kein Vielfaches von $v_{1}$ ist.

Eine Menge $M$ von Vektoren heißt #linear_unabhängig, wenn kein Vektor aus $M$ als Linearkombination der anderen Vektoren aus $M$ dargestellt werden kann, also für alle $v \in M$ gilt. 
$$
v \not\in [M\setminus \{ v \}]
$$
Andererseits heißt eine Menge $M$ von Vektoren #linear_abhängig, wenn es möglich ist, einen Vektor aus $M$ als Linearkombination von anderen Vektoren aus $M$ darzustellen, wenn es also einen Vektor $v \in M$ gibt mit
$$
v \in [M\setminus \{ v \}]
$$
Auch gibt es Listen aus Vektoren. Bei diesen Listen ist der Unterschied zu den Mengen, dass Vektoren öfters vorkommen können. Kommt ein Vektor öfters vor ist die Liste nicht mehr linear unabhängig.

Die Menge der Vektoren
$$
e_{1}=\left(\begin{matrix}
1 \\ 0 \\ 0 \\ \vdots \\ 0
\end{matrix}
\right),
e_{2}=\left(\begin{matrix}
0 \\ 1 \\0 \\ \vdots  \\ 0
\end{matrix}\right),
\dots,
e_{n}=\left(\begin{matrix}
0\\0\\0\\\vdots\\1
\end{matrix}\right) \in K^{n}
$$
ist linear unabhängig. Sie bilden auch die #kanonische_Basis $E=\{ e_{1},e_{2},\dots,e_{n} \}$ von $K^{n}$

Eine Menge $M$ ist genau dann linear abhängig, wenn es eine nichttriviale Linearkombination gibt, die den Nullvektor darstellt.
$$
\exists(\lambda_{1},\lambda_{2},\dots,\lambda_{n})\not=(0,0,\dots,0) \text{ mit }\lambda_{1}\cdot v_{1}+\lambda_{2}\cdot v_{2}+\dots \lambda_{n} \cdot v_{n}=0
$$
Um die lineare Abhängigkeit zu überprüfen kann man also ein lineares Gleichungssystem aufstellen.

$$
\lambda_{1} \cdot \left(\begin{matrix}
1 \\ 3 \\ 4
\end{matrix}\right)
+ \lambda_{2} \cdot \left(\begin{matrix}
1 \\ 2 \\ 2
\end{matrix}\right)
+ \lambda_{3} \cdot \left(\begin{matrix}
-1 \\ 0 \\ 2
\end{matrix}\right)
= \left(\begin{matrix}
0 \\ 0 \\ 0
\end{matrix}\right)
$$
$$
1\lambda_{1}+1\lambda_{2}-1\lambda_{3}=0
$$
$$
3\lambda_{1}+2\lambda_{2}+0\lambda_{3}=0
$$
$$
4\lambda_{1}+2\lambda_{2}+2\lambda_{3}=0
$$
Die Lösung ist
$$
\lambda_{1}=2,\lambda_{2}=-3,\lambda_{3}=-1
$$
Folgende Vektoren sind linear unabhängig, da es keine nichttriviale Lösung gibt. 
$$
v_{1}=\left(\begin{matrix}
1\\-2\\3\\0
\end{matrix}\right),
v_{2}=\left(\begin{matrix}
0\\3\\-2\\1
\end{matrix}\right),
v_{3}=\left(\begin{matrix}
0\\0\\2\\-5
\end{matrix}\right)
$$
Fasst man diese zu einer Matrix zusammen bildet diese eine #Halbdiagonale
$$
\left(\begin{matrix}
1 & 0 & 0 \\
-2 & 3 & 0 \\
3 & -2 & 2 \\
0 & 1 & -5
\end{matrix}\right)
$$
Alle Eintragungen oberhalb und unterhalb der Diagonale sind 0. 

Nun wollen wir Linearkombinationen von linear unabhängigen Vektoren $v_{1},v_{2},\dots,v_{n}$ betrachten. Ist etwa der Vektor $x$ in der linearen Hülle dieser Vektoren enthalten, also
$$
x=\lambda_{1}\cdot v_{1}+\lambda_{2}\cdot v_{2}+\dots+\lambda_{n}\cdot v_{n}
$$
so sind die Koeffizienten $\lambda_{1},\lambda_{2},\dots,\lambda_{n}$ eindeutig bestimmt. Wäre es nämlich möglich, $x$ in der Form $$
x=\mu_{1}\cdot v_{1}+\mu \cdot v_{2}+\dots+ \mu_{n}\cdot v_{n}
$$
mit anderen Koeffizienten zu schreiben könnte man durch Differenzbildung
$$
x-x=(\lambda_{1}-\mu_{1})\cdot v_{1}+(\lambda_{2}-\mu_{2})\cdot v_{2} + \dots + (\lambda_{n}-\mu_{n}) \cdot v_{n}
$$
also eine nichttriviale Linearkombination die den Nullvektor darstellt. Dies ist aber wegen der linearen Unabhängigkeit ausgeschlossen.
## Basen
Eine Teilmenge $B$ eines Vektorraums $V$ heißt #Basis von $V$, wenn sie linear unabhängig ist und ihre lineare Hülle $[B]$ gleich $V$ ist.
Jeder Vektor $x$ aus $V$ lässt sich eindeutig als Linearkombination von Vektoren der Basis darstellen. Die Koeffizienten dieser Linearkombination heißen #Koordinaten von $x$ bezüglich der Basis $B$.

Eine wichtige Eigenschaft von Vektorräumen ist, dass jede Basis gleich viele Elemente hat. Dies wird mit Hilfe der folgenden Eigenschaft nachgewiesen.

### Austaschlemma
Es sei $M=\{ v_{1},v_{2},\dots,v_{n} \}$ eine Menge von Vektoren und $a=\mu_{1} \cdot v_{1}+\dots+\mu_{n}\cdot v_{n}$ eine Linearkombination dieser Vektoren. Weiter sei $M'=(M\setminus \{ v_{j} \}) \cup \{ a \}=\{ v_{1},\dots,v_{j-1},a,v_{j+1},\dots,v_{n} \}$ für ein $j$ mit $\mu_{j}\not=0$. Dann ist $M$ genau dann linear unabhängig, wenn $M'$ linear unabhängig ist, und es gilt immer $[M']=[M]$.

#### Beweis des Austaschlemma
Wir betrachten eine Linearkombination des Vektoren aus $M'$
$$
\lambda_{1}\cdot v_{1}+\dots+\lambda_{j-1}\cdot v_{j-1}+\lambda_{j}\cdot a+\lambda_{j+1}\cdot v_{j+1}+\dots+\lambda_{n}\cdot v_{n}
$$
$$
=\lambda_{1}\cdot v_{1}+\dots+\lambda_{j-1}\cdot v_{j-1}+\lambda_{j}\cdot(\mu_{1}\cdot v_{1}+\dots+\mu_{n}\cdot v_{n})+\lambda_{j+1}\cdot v_{j+1}+\dots+\lambda_{n}\cdot v_{n}
$$
$$
=(\lambda_{1}+\lambda_{j}\mu_{1})\cdot v_{1}+\dots+(\lambda_{j-1}+\lambda_{i}\mu_{j-1})\cdot v_{j-1}+\lambda_{j}\mu_{j}\cdot v_{j}
$$
$$
+(\lambda_{j+1}+\lambda_{j}\mu_{j+1})\cdot v_{j+1}+\dots+(\lambda_{n}+\lambda_{j}\mu_{n})\cdot v_{n}
$$
Setzt man nun voraus, dass $M$ linear unabhängig ist, und nimmt man an, dass diese Linearkombination der Vektoren aus $M'$ den Nullvektor darstellt, so folgt zunächst, dass $\lambda_{j}=0$ ist, also
$$
\lambda_{1}\cdot v_{1}+\dots+\lambda_{j-1}\cdot v_{j-1}+\lambda_{j+1}\cdot v_{j+1}+\dots+\lambda_{n}\cdot v_{n}=0
$$
Daraus folgt aber auch $\lambda_{1}=\dots=\lambda_{j-1}=\lambda j+1=\dots=\lambda_{n}=0$ und schließlich, dass $M'$ linear unabhängig ist.
Man beachte nun, dass $v_{j}$ als Linearkombination
$$
v_{j}=-\frac{\mu_{1}}{\mu_{j}}\cdot v_{1}-\dots-\frac{\mu_{j-1}}{\mu_{j}}\cdot v_{j-1}+\frac{1}{\mu_{j}}\cdot a - \frac{\mu_{j+1}}{\mu_{j}} \cdot v_{j+1} - \dots - \frac{\mu_{n}}{\mu_{j}}\cdot v_{n}
$$
der Vektoren aus $M'$ dargestellt werden kann, wobei der Koeffizient $1/\mu_{j} \not= 0$ ist. Aus denselben Überlegungen wie vorhin folgt nun, dass $M$ linear unabhängig sein muss, wenn man voraussetzt, dass $M'$ linear unabhängig ist. Weiters folgt aus der obigen Darstellung dass in jedem Fall $[M']\subseteq[M]$ ist, da jede Linearkombination von Vektoren aus $M'$ als Linearkombination von Vektoren aus $M$ dargestellt werden kann. Auch gilt die umgekehrte Inklusion, also insgesamt $[M']=[M]$

Wir nehmen nun an, dass $B=\{ b_{1},b_{2},\dots,b_{n} \}$ eine Basis eines Vektorraums $V$ ist, und $C=\{ c_{1},c_{2} \}$ sei eine linear unabhängige Menge. Wir wollen jetzt versuchen, nicht nur einen Vektor aus $B$ auszutauschen, sondern zwei. Wir gehen schrittweise vor. Wegen $c_{1}\not=0$ sind in der Darstellung $c_{1}$ als Linearkombination der Vektoren aus $B$ nicht alle Koeffizienten 0. Wir nehmen o.B.d.A. an, der Koeffizient von $b_{1}$ wäre ungleich 0. Dann folgt aus dem Austauschlemma, dass $B'=\{ c_{1},b_{2},\dots,b_{n} \}$ wieder eine Basis von $V$ ist. Im zweiten Schritt wollen wir $c_{2}$, gegen einen Vektor aus $B'$ austauschen. Dazu betrachten wir jene Linearkombination von Vektoren aus $B'$, die $c_{2}$ darstellt. Angenommen, alle Koeffizienten der Vektoren $b_{2},\dots,b_{n}$ wären 0, dann wäre $c_{2}$ ein Vielfaches von $c_{1}$. Dies ist jedoch ausgeschlossen, da wir vorausgesetzt haben, dass die Vektoren $c_{1},c_{2}$ linear unabhängig sind. Wir können daher annehmen, dass der Koeffizient von $b_{2}$ von 0 verschieden ist, und es folgt aus dem Austaschlemma, dass $B''=\{ c_{1},c_{2},b_{3},\dots,b_{n} \} =(B\setminus \{ b_{1},b_{2} \}) \cup C$ eine Basis ist.
Dieselbe Überlegung funktioniert für jede lineare unabhängige Menge $C$. es gibt in $B$ eine Teilmenge $D$ mit $|D|=|C|$, so dass $(B\setminus D)\cup C$ wieder eine Basis ist. Insbesondere kann $C$ nicht unendlich sein, und es muss $|C|\leq |B|$ gelten. Wendet man diese Überlegung für eine Basis $C$ an und vertauscht man in einem zweiten Schritt die Rollen von $B$ und $C$, so folgt auch $|B|\leq |C|$ und $|B|=|C|$. Daher haben zwei Basen desselben Vektorraums immer gleich viele Elemente haben.
### Dimension
Besitzt ein Vektorraum $V$ eine endliche Basis $B$, so ist die #Dimension $\text{dim}$ $V$ gleich der Anzahl $|B|$ der Vektoren von $B$. Besitzt $V$ keine endliche Basis, so heißt er #unendlichdimensional.
Die Menge der Vektoren der #kanonische_Basis spannen alle Vektoren aus $K^{n}$ auf. Die Koordinaten $x_{1},x_{2},\dots,x_{n}$ eines Vektors $x\in K^{n}$ sind gleichzeitig die Koordinaten bezüglich $E$. Insbesondere gilt dim $K^{n}=n$

Die #Polynome $p(x)=a_{0}+a_{1}x+\dots+a_{n}x^{n}$ mit reellen Koeffizienten $a_{j}\in \mathbb{R}$ bilden einen Vektorraum über $\mathbb{R}$. Offensichtlich ist die Menge $B=\{ 1,x,x^{2},x^{3},\dots \}$ der Monome eines Basis der Polynome. Damit ist $(\mathbb{R}[x],+,\mathbb{R})$ ein #unendlichdimensionaler Vektorraum.

Im Folgenden wollen wir uns auf endlichdimensionale Vektorräume beschränken. Es sei nun $V$ ein allgemeiner Vektorraum der Dimension $n$ und $B=\{ b_{1},b_{2},\dots,b_{n} \}$ eine Basis von $V$. Jeder Vektor $x\in V$ lässt sich eindeutig als Linearkombination der Basisvektoren darstellen. 
$$
x=\lambda_{1}\cdot b_{1}+\lambda_{2}\cdot b_{2}+\dots+\lambda_{n}\cdot b_{n}
$$
Man nennt die Abbildung $\Phi_{B}:V \rightarrow K^{n}$, die einem Vektor $x\in V$ die Koordinaten

$$
\Phi_{B}(x)=\left(\begin{matrix}
\lambda_{1}\\ \lambda_{2} \\ \vdots \\ \lambda_{n}
\end{matrix}\right)
$$

zuordnet, die #Koordinatenabbildung bezüglich der Basis $B$. 
Wegen der Eindeutigkeit der Darstellung als Linearkombination einer Basis ist die Koordinatenabbildung $\Phi_{B}$ bijektiv und erfüllt die Eigenschaften
$$
\Phi_{B}(x+y)=\Phi_{B}(x)+\Phi_{B}(y) \text{ und }\Phi_{B}(\lambda \cdot x)=\lambda \cdot \Phi_{B}(x)
$$
für alle $x,y\in V$ und $\lambda\in K$. Man kann daher auf der Ebene der Koordinaten alle Rechnungen in $V$ auch im Vektorraum $K^{n}$ durchführen. $V$ und $K^{n}$ haben daher dieselbe Struktur, man nennt sie auch #isomorph . Der Vektorraum $K^{n}$ ist daher in diesem Sinn der "einzige" Vektorraum der Dimension $n$ Dies rechtfertigt auch die eingangs gewählte Beschränkung auf den $K^{n}$. Abschließend bemerken wir noch, dass die Dimension von Teilräumen $U\leq V$ nie größer sein kann als die von $V$. 
$$
U\leq V \implies \text{ dim } U\leq \text{ dim }V 
$$
Für den trivialen Nullraum gilt $\text{dim}\{ 0 =0\}$