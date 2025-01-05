## Rang einer Matrix
Der #Spaltenrang $\text{rg}(A)$ einer Matrix $A\in K^{m\times n}$ ist die Dimension der linearen Hülle der Spalten von $A$. Der #Zeilenrang einer Matrix $A\in K^{m\times n}$ ist die Dimension der linearen Hülle der Zeilen von $A$, also der Spaltenrang von $A^{T}$.

Da Spaltenrang und Zeilenrang immer übereinstimmen spricht man auch vom #Rang_einer_Matrix. 

Für jede Matrix $A\in K^{m\times n}$ stimmt
$$
\text{rg}(A)=\text{rg}(A^{T})
$$
## Elementare Umformungen
Sei $A \in K^{m\times n}$ eine Matrix mit den Spalten $a_{1},\dots,a_{n}\in K^{m}$. Die drei Operationen

- (i) Multiplikation einer Spalte $a_{j} ~(1\leq j\leq n)$ mit einem Skalar $\lambda\in K\setminus\{ 0 \}$,
- (ii) Addieren eines Vielfachen einer Spalte $a_{i}~(1\leq i\leq n)$ zu einer Spalte $a_{j}~(i\not=j)$, d.h. Ersetzen der Spalte $a_{j}$ durch $\lambda \cdot a_{i}+a_{j}$ mit $\lambda\in K$ und $i\not=j$
- (iii) Vertauschen zweier Spalten $a_{i},a_{j}$

heißen #elementare_Spaltenumformungen der Matrix $A$.

Dies ist auch mit Zeilen möglich, den sogenannten #elementare_Zeilenumformungen. Diese funktionieren exakt gleich wie die Spaltenumformungen.

Sei $A'\in K^{m\times n}$ eine Matrix, die aus der Matrix $A\in K^{m\times n}$ durch eine Folge von elementaren Umformungen hervorgeht, dann gilt
$$
\text{rg}(A)=\text{rg}(A')
$$
### Beweis des gleichen Ranges
Durch Multiplikation einer Spalte mit einem Skalar bzw. durch das Vertauschen zweier Spalten bleibt die lineare Hülle der Spaltenvektoren unverändert. Aus dem Austaschlemma folgt, dass auch das Addieren eines Vielfachen einer Spalte nicht die lineare Hülle verändert. Der Spaltenrang bleibt also gleich.
Man interpretiere die Spalten von $A$ als Koordinaten von Vektoren bezüglich einer Basis $B$. Man betrachte eine Zeilenumformungen der Matrix $A$, es wird also z.B. der $j$-te Zeilenvektor $\tilde{a}_{j}$ durch $\lambda \cdot  \tilde{a}_{i}+\tilde{a}_{j}$ ersetzt. Die entstehende Matrix wird wieder mit $A'$ bezeichnet. Wir wenden nun die entsprechende inverse Umformung auf die Basis $B$ an, also z.B. würde der Vektor $b_{j}$ durch $-\lambda \cdot b_{i}+b_{j}$ ersetzt werden. Aus dem Austauschlemma folgt, dass die resultierende Menge $B'$ von Vektoren wieder eine Basis ist. Außerdem sind die Koordinaten der Vektoren $v_{1},\dots,v_{n}$ bezüglich $B'$ gerade die Spalten von $A'$. Die lineare Hülle der Spalten von $A$ bzw. von $A'$ entspricht daher der linearen Hülle der Vektoren $v_{1},\dots,v_{n}$. Der Spaltenrang bleibt daher bei Zeilenumformungen unverändert.

Es sei eine Matrix gegeben
$$
A=\left(\begin{matrix}
1 & 2 & -3 & 0 \\
2 & 5 & 1 & 8 \\
-1 & -2 & 4 & 1 \\
4 & 0 & 2 & 6
\end{matrix}\right)
$$
Die Spalten von $A$ bezeichnen wir mit $a_{1},a_{2},a_{3},a_{4}$. Wir erzeugen oberhalb bzw. rechts von der Diagonale Nullen. Dazu ersetzen wir zunächst die zweite Spalte $a_{2}$ durch $a_{2}-2a_{1}$ und die dritte durch $a_{3}+3a_{1}$
$$
A'=\left(\begin{matrix}
1 & 0 & 0 & 0 \\
2 & 1 & 7 & 8 \\
-1 & 0 & 1 & 1  \\
4 & -8 & 14 & 6
\end{matrix}\right)
$$
In dieser Matrix ersetzen wir die dritte Spalte durch $a'_{3}-7a_{2}'$ und die vierte durch $a_{4}'-8a_{2}'$
$$
A''=\left(\begin{matrix}
1 & 0 & 0 & 0 \\
2 & 1 & 0 & 0 \\
-1 & 0 & 1 & 1 \\
4 & -8 & 70 & 70
\end{matrix}\right)
$$
Schließlich ersetzen wir hier die vierte Spalte durch $a''_{4}-a_{3}''$ und erhalten eine Matrix der Form
$$
A'''=\left(\begin{matrix}
1 & 0 & 0 & 0 \\
2 & 1 & 0 & 0 \\
-1 & 0 & 1 & 0 \\
4 & -8 & 70 & 0
\end{matrix}\right)
$$
Offensichtlich hat diese Matrix $\text{rg}(A''')=3$, da die ersten drei Spalten linear unabhängig sind. Die ursprüngliche Matrix hat demnach ebenfalls $\text{rg}(A)=3$

Die Spalten von $A$ sind linear unabhängig und spannen einen dreidimensionalen Unterraum von $K^{4\times 1}$ auf.

