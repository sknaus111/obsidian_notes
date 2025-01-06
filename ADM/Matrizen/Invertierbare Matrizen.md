Sei $A\in K^{n\times n}$ eine quadratische Matrix. Sie heißt #invertierbar oder #regulär, wenn es eine Matrix $A^{-1}\in K^{n\times n}$ gibt mit
$$
A \cdot A^{-1}=A^{-1}\cdot A=I_{n}
$$
Die Matrix $A^{-1}$ heißt dann die zu $A$ inverse Matrix. Nicht invertierbare Matrizen werden auch als #singulär bezeichnet.

Es seien $A$ und $B$ zwei invertierbare Matrizen in $K^{n\times n}$. Dann sind $A \cdot B$ und $A^{T}$ ebenfalls invertierbar, und es gilt

- (i) $(A\cdot B)^{-1}=B^{-1}\cdot A^{-1}$
- (ii) $(A^{T})^{-1}=(A^{-1})^{T}$

Man betrachte die Multiplikation einer $m\times n$-Matrix $A$ mit einem $n$-dimensionalen Spaltenvektor: $A \cdot x$. Sind $a_{1},a_{2},\dots,a_{n}$ die Spalten von $A$ und $x_{1},x_{2},\dots,x_{n}$ die Koordinaten von $x$ so gilt
$$
A \cdot x=(a_{1} ~~ a_{2} ~~ \dots ~~ a_{n}) \cdot x=x_{1}\cdot a_{1}+x_{2}\cdot a_{2}+\dots+x_{n}\cdot a_{n}
$$
Das Produkt einer Matrix mit einem Vektor ist also nichts anderes als eine Linearkombination der Spalten von $A$, wobei die Koeffizienten die Koordinaten von $x$ sind. Daraus folgt etwa
$$
A \cdot e_{j}=a_{j}
$$
das Produkt einer Matrix $A$ mit dem $j$-ten kanonischen Basisvektor ist die $j$-te Spalte von $A$. Ist nun $B$ eine $n\times q$-Matrix mit Spalten $b_{1},b_{2},\dots,b_{q}$, dann ist die $j$-te Spalte des Matrizenprodukts $A\cdot B$ das Produkt von $A$ mit $b_{j}$
$$A\cdot B= (A\cdot b_{1} ~~A \cdot b_{2} ~~ \dots ~~ A\cdot b_{q})$$
Anders ausgedrückt, die Spalten von $A \cdot B$ sind Linearkombinationen der Spalten von $A$, wobei die Koeffizienten dieser Linearkombinationen in den entsprechenden Spalten von $B$ stehen. Offensichtlich kann man damit
$$
A \cdot I_{n}= A(e_{1} ~~ e_{2} ~~ \dots ~~ e_{n})=(a_{1} ~~ a_{2} ~~ \dots ~~ a_{n})=A
$$
direkt überprüfen.

Eine andere Interpretation der Multiplikation einer Matrix mit einem Spaltenvektor beruht auf dem Zusammenhang mit #linearen_Gleichungssystemen. Ein einfaches Beispiel ist etwa
$$
2x_{1}+3x_{2}=5
$$
$$
7x_{1}-5x_{2}=2
$$
Offensichtlich lässt sich dieses in der Form
$$
\left(\begin{matrix}
2 & 3 \\
7 & -5
\end{matrix}\right)
\cdot \left(\begin{matrix}
x_{1} \\
x_{2}
\end{matrix}\right)
=\left(\begin{matrix}
5 \\
2
\end{matrix}\right)
$$
schreiben.

Diese Interpretation kann genutzt werden, um invertierbare Matrizen zu charakterisieren.

Eine quadratische Matrix $A\in K^{n\times n}$ ist genau dann invertierbar, wenn ihre Spalten linear unabhängig sind, also eine Basis von $K^{n}$ bilden.

## Beweis der Invertierbarkeit
Wenn eine Matrix invertierbar ist, so ist die Matrizengleichung $A \cdot X = I_{n}$ lösbar. Das bedeutet aber, dass die kanonischen Basisvektoren $e_{1},e_{2},\dots,e_{n}$ als Linearkombination der Spalten von $A$ dargestellt werden können. Das gelingt aber genau dann, wenn die Spalten von $A$ linear unabhängig sind, also eine Basis von $K^{n}$ bilden. Entsprechendes gilt für die Zeilen.  Eine Matrix ist also genau dann invertierbar, wenn die lineare Hülle der Spalten von $A$ ganz $K^{n}$ ist.