Unter einer $m\times n$ Matrix $A=(a_{ij})$ mit Koeffizienten aus einem Körper $K$ versteht man ein rechteckiges Schema
$$
A=\left(\begin{matrix}
a_{11} & a_{12} & \dots & a_{1n} \\
a_{21} & a_{22} & \dots & a_{2n} \\
\vdots & \vdots & & \vdots \\
a_{m1} & a_{m2} & \dots & a_{mn}
\end{matrix}\right)
$$
aus $m$ Zeilen und $n$ Spalten mit Eintragungen $a_{ij} \in K$. Die Menge aller $m\times n$- Matrizen mit Eintragungen aus $K$ wird mit $K^{m\times n}$ bezeichnet. Eine Matrix $A\in K^{m\times n}$ mit gleicher Spaltenanzahl und Zeilenanzahl heißt #quadratisch. 

#Spaltenvektoren können auch als $K^{m\times 1}$ Matrizen gesehen werden und #Zeilenvektoren als $K^{1\times n}$ Matrizen.

Ist $A\in K^{m\times n}$ eine $m\times n$-Matrix, so bezeichnen wir mit $A^{T}$ die zu $A$ #transponierte_Matrix. Sie ist eine $n\times m$-Matrix und geht aus $A$ dadurch hervor, dass Zeilen und Spalten vertauscht werden. d.h. die erste Spalte von $A$ ist die erste Zeile von $A^{T}$, usw. Eine quadratische Matrix $A=(a_{ij})\in K^{n\times n}$ heißt #symmetrisch, wenn
$$
A^{T}=A
$$
ist, d.h. wenn $a_{ij}=a_{ji}$ für alle $i,j\leq n$

Auch lässt sich mit Matrizen elementweise addieren. $A+B=(a_{ij}+b_{ij})$
$$
\left(\begin{matrix}
1 & 2  \\
5 & 7 \\
0 & 2
\end{matrix}\right)
+ \left(\begin{matrix}
-2 & 1 \\
3 & 0 \\
1 & -2
\end{matrix}\right)
=\left(\begin{matrix}
-1 & 3 \\
8 & 7 \\
1 & 0
\end{matrix}\right)
$$
Ebenso kann man das Vielfache $\lambda \cdot A=(\lambda a_{ij})$
$$
3\cdot \left(\begin{matrix}
1 & 2 \\
5 & 7 \\
0 & 2
\end{matrix}\right)
=\left(\begin{matrix}
3 & 6 \\
15 & 21 \\
0 & 6
\end{matrix}\right)
$$
Die algebraische Struktur $(K^{m\times n},+,K)$ bildet einen Vektorraum der Dimension $m\cdot n$

Sind $A=(a_{ij})\in K^{m\times n}$ und $B=(b_{jk})\in K^{n\times q}$ zwei Matrizen, wobei die Anzahl der Spalten der ersten gleich der Anzahl der Zeilen der zweiten ist, so wird durch 
$$
c_{ik}=a_{i1}b_{1k}+a_{i 2}b_{2k}+\dots+a_{in}b_{nk}=\sum_{j=1}^{n}a_{ij}b_{jk}
$$
eine Matrix  in $K^{m\times q}$, die als #Produkt $A\cdot B=(c_{ik})$ der Matrizen $A$ und $B$ bezeichnet wird.

$$
A_{1}\cdot A_{2}=\left(\begin{matrix}
1 & 5 & 2 \\
3 & 2 & 1 \\
0 & 1 & 2
\end{matrix}\right)
\cdot
\left(\begin{matrix}
1 & 2 \\
5 & 7 \\
0 & 2
\end{matrix}\right)
$$
$$
=\left(\begin{matrix}
1\cdot 1+ 5 \cdot 5 + 2\cdot0 & 1 \cdot 2+ 5 \cdot 7 + 2 \cdot 2 \\
3 \cdot 1+ 2 \cdot 5 + 1 \cdot 0 & 3 \cdot 2 + 2 \cdot 7 + 1 \cdot 2 \\
0 \cdot 1 + 1 \cdot 5 + 2 \cdot 0 & 0 \cdot 2 + 1 \cdot 7 + 2 \cdot 2
\end{matrix}\right)
=\left(\begin{matrix}
26 & 41 \\
13 & 22 \\
5 & 11
\end{matrix}\right)
$$
Man beachte, dass die Elemente $c_{ik}$ durch ein so genanntes #Skalarprodukt der $i$-ten Zeile von $A$ und der $k$-ten Spalte von $B$ gebildet wird. Ein Skalarprodukt von einem Zeilenvektor $x$ und einem Spaltenvektor $y$ ist dabei durch
$$
x\cdot y=(x_{1} ~~ x_{2} ~~ \dots ~~x_{n}) \cdot \left(\begin{matrix}
y_{1} \\
y_{2} \\
\vdots  \\
y_{n}
\end{matrix}\right)
=x_{1}y_{1}+x_{2}y_{2}+\dots+x_{n}y_{n}
$$
gegeben. Die Matrizenmultiplikation folgt, wie wir gleich sehen werden zahlreichen Rechenregeln. Allerdings sind zwei gewohnte Eigenschaften nicht erfüllt. Das Kommutativgesetz gilt nicht
$$
A \cdot B \not= B \cdot A
$$
und das Produkt zweier von der Nullmatrix verschiedener Matrizen kann die Nullmatrix ergeben.
$$
\left(\begin{matrix}
0 & 1 \\
0 & 0
\end{matrix}\right)
\cdot \left(\begin{matrix}
0 & 1  \\
0 & 0
\end{matrix}\right)
=\left(\begin{matrix}
0 & 0 \\
0 & 0
\end{matrix}\right)
$$
Sei $n\geq1$ eine ganze Zahl. Unter der $n$-dimensionalen #Einheitsmatrix $I_{n}\in K^{n\times n}$ versteht man die Matrix.
$$
I_{n}=\left(\begin{matrix}
1 & 0 & \dots & 0 \\
0 & 1 & \dots & 0 \\
\vdots & \vdots & & \vdots \\
0 & 0 & \dots & 1
\end{matrix}\right)
$$
d.h. die Spalten von $I_{n}$ sind die Vektoren $e_{1},e_{2},\dots,e_{n}$ der #kanonische_Basis 

Die Einheitsmatrix hat auch die Eigenschaft, dass nur in der #Diagonale Elemente stehen, die von Null verschieden sind. Allgemein betrachtet man so genannte #Diagonalmatrizen.
$$
diag(\lambda_{1},\lambda_{2},\dots,\lambda_{n})=\left(\begin{matrix}
\lambda_{1} & 0 & \dots & 0 \\
0 & \lambda_{2} & \dots & 0 \\
\vdots & \vdots & & \vdots \\
0 & 0 & \dots & \lambda_{n}
\end{matrix}\right)
$$
Entsprechend spricht man von #oberen_Dreiecksmatrizen bzw. #unteren_Dreiecksmatrizen, wenn alle Elemente unterhalb bzw. oberhalb der Diagonale 0 sind.

$A,B,C$ bezeichne Matrizen, $I$ die Einheitsmatrix und $\lambda$ einen Skalar. Dann gelten die folgenden Rechenregeln.

- (i) $A\cdot I=I \cdot A=A$
- (ii) $(A \cdot B)\cdot C=A \cdot(B\cdot C)$
- (iii) $(A+B)\cdot C=A\cdot C+B\cdot C$
- (iv) $A \cdot (B+C)=A\cdot B+A\cdot C$
- (v) $(\lambda \cdot A)\cdot B=A\cdot(\lambda \cdot B)=\lambda \cdot(A\cdot B)$
- (vi) $(A+B)^{T}=A^{T}+B^{T}$
- (vii) $(A \cdot B)^{T}=B^{T}\cdot A^{T}$
- (viii) $(\lambda \cdot A)^{T}=\lambda \cdot A^{T}$

