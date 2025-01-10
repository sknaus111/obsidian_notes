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
### Elementarmatrizen
Elementrare Spaltenumformungen von $A$ können auch durch das Multiplizieren der Matrix $A$ mit geeigneten Transformationsmatrizen realisiert werden. Eine so genannte #Elementarmatrix ist eine Matrix, die aus der Einheitsmatrix $I_{n}$ nach Anwendung einer elementaren Spalten- bzw. Zeilenumformung hervorgeht. So sind etwa
$$
T'=\left(\begin{matrix}
1 & 0  & 0 \\
0  & 1  & \lambda \\
0  & 0  & 1
\end{matrix}\right)
$$
und $$
T''=\left(\begin{matrix}
0 & 1 & 0 \\
1  & 0  & 0 \\
0  & 0  & 1
\end{matrix}\right)
$$
Elemantarmatrizen. Bei $T'$ wurde das $\lambda$-fache der $2$. Spalte von $I_{3}$ zu $3$. Spalte addiert und bei $T''$ wurden die ersten beiden Zeilen von $I_{3}$ vertauscht. Multipliziert man nun beispielsweise eine beliebige 3-spaltige Matrix $A$ von rechts mit der Elementarmatrix $T'$, so entsteht eine Matrix $A'$, die aus $A$ durch dieselben Spaltenumformungen entsteht wie $T'$ aus $I_{3}$

$$
A\cdot T'=(a_{1} ~~ a_{2} ~~ a_{3}) \cdot \left(\begin{matrix}
1 & 0 & 0 \\
0 & 1  & \lambda \\
0  & 0  & 1
\end{matrix}\right)
=\left(a_{1} ~~ a_{2} ~~ \lambda a_{2}+a_{3}\right)
$$
Man beachte insbesondere, dass Elementarmatrizen invertierbar sind. Beispielsweise ist 
$$
(T')^{-1}=\left(\begin{matrix}
1 & 0 & 0 \\
0 & 1 & \lambda \\
0  & 0  & 1
\end{matrix}\right)^{-1}
=\left(\begin{matrix}
1 & 0 & 0 \\
0 & 1 & -\lambda \\
0 & 0  & 1
\end{matrix}\right)$$
Das Umformen einer Matrix $A$ in eine Matrix $A'$ mittels elementarer Spaltenumformungen entspricht also der Multiplikation mit einer invertierbaren Matrix $T$.
$$
A'=A\cdot T
$$
wobei $T$ Produkt geeigneter Elementarmatrizen ist. Entsprechendes gilt natürlich auch für Zeilenumformungen, die einer Multiplikation mit einer invertierbaren Matrix $\tilde{T}$ von links entsprechen: $A''=\tilde{T}\cdot A$

### Berechnung inverser Matrizen
Diese Eigenschaft kann auch zur Berechnung der inversen Matrix $A^{-1}$ verwendet werden. Ist $A$ invertierbar, dann sind nach dem Satz, dass eine quadratische Matrix $A\in K^{n\times n}$ genau dann invertierbar ist, wenn ihre Spalten oder Zeilen linear unabhängig sind, ihre Spalten linear unabhängig. Es ist daher allein durch Spaltenumformungen möglich, $A$ in die Einheitsmatrix $A'=I_{n}$ umzuformen, also $A \cdot T=I_{n}$. Die Matrix $T$ ist daher gleich der inversen Matrix $A^{-1}$. Aus der obigen Überlegung folgt, dass $T$ auch als jene Matrix gesehen werden kann, die aus der Einheitsmatrix dadurch hervorgeht, dass man darauf dieselben Spaltenumformungen wie auf $A$ ausführt. Dies kann folgendermaßen explizit durchgeführt werden. 

Es soll die inverse Matrix $A^{-1}$ von
$$
A=\left(\begin{matrix}
1 & 2 & 0 \\
0 & 2 & 1 \\
3 & 5 & 0
\end{matrix}\right)
$$
bestimmt werden. Durch elementare Spaltenumformungen erhält man
$$
\left(\begin{matrix}
1 & 2 & 0 \\
0 & 2 & 1 \\
3 & 5 & 0 \\
-- & -- & -- \\
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{matrix}
\right) \rightarrow ~(x_{2}-2x_{1})~ \left(\begin{matrix}
1 & 0 & 0 \\
0 & 2 & 1 \\
3 & -1 & 0 \\
-- & -- & -- \\
1 & -2 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{matrix}\right) \rightarrow ~ (x_{2} \iff x_{3}) ~
\left(\begin{matrix}
1 & 0 & 0 \\
0 & 1 & 2 \\
3 & 0 & -1 \\
-- & -- & -- \\
1 & 0 & -2 \\
0 & 0 & 1 \\
0 & 1 & 0
\end{matrix}\right)
$$

$$
\rightarrow ~ ( x_{3}-2x_{2})  ~ \left(\begin{matrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
3 & 0 & -1 \\
-- & -- & -- \\
1 & 0 & -2 \\
0 & 0 & 1 \\
0 & 1 & -2
\end{matrix}\right)
\rightarrow ~ (x_{3}\cdot-1) ~ \left(\begin{matrix}
1 & 0 & 0 \\
0 & 1 & 0  \\
3 & 0 & 1 \\
-- & -- & -- \\
1 & 0 & 2 \\
0 & 0 & -1 \\
0 & 1 & 2
\end{matrix}\right)
\rightarrow ~ (x_{1}-3x_{3} )~\left(\begin{matrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
-- & -- & -- \\
-5 & 0 & 2 \\
3 & 0 & -1 \\
-6 & 1 & 2
\end{matrix}\right)
$$
Die inverse Matrix $A^{-1}$ ist also 
$$
A^{-1}=\left(\begin{matrix}
-5 & 0 & 2 \\
3 & 0 & -1 \\
-6 & 1 & 2
\end{matrix}\right)
$$
In ganz analoger Weise kann man mit der Matrix
$$
\left(\begin{matrix}
1 & 2 & 0| 1 & 0 & 0 \\
0 & 2 & 1| 0 & 1 & 0 \\
3 & 5 & 0| 0 & 0 & 1
\end{matrix}\right)
$$
beginnen und mit Hilfe von Zeilenumformungen die linke Hälfte in die Einheitsmatrix überführen. Dann steht auf der rechten Seite wieder die inverse Matrix $A^{-1}$.

