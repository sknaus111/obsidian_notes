Die #Determinante einer quadratischen Matrix $A=(a_{ij})\in K^{n\times n}$ ist durch
$$
\det A=\sum_{\pi\in S_{n}}sgn(\pi)a_{\pi(1)1}a_{\pi(2)2}\dots a_{\pi(n)n}
$$
gegeben. ($S_{n}$ bezeichnet die Menge aller Permutationen der Zahlen $1,2,\dots ,n$ und $sgn(\pi)$ das Vorzeichen einer Permutation $\pi$).

In er Darstellung als quadratisches Schema schreibt man anstelle von $\det A=\det(a_{ij})$ auch
$$
\det A=\left|\begin{matrix}
a_{11}  & a_{12} & \dots   & a_{1n} \\
a_{21}  & a_{22}  & \dots  & a_{2n} \\
\vdots   &  \vdots  &  \vdots  &  \vdots \\
a_{n_{1}}  & a_{n_{2}}  & \dots  & a_{nn} \\
\end{matrix}\right|
$$
## Beispiel 
Für $n=2$ gibt es zwei Permutationen, die identische Permutationen $id$ mit $id(1)=1$ und $id(2)=2$ und die Transposition $\pi_{12}$ mit $\pi_{12}(1)=2$ und $\pi_{12}(2)=1$. Weiters ist $sgn(id)=1$ und $sgn(\pi_{12})=-1$. Die Determinante hat daher die Form
$$
\left|\begin{matrix}
a_{11}   & a_{12} \\
a_{21} & a_{22}
\end{matrix}\right|
=a_{11}\cdot a_{22}-a_{12}\cdot a_{21}
$$
Für $n=e$ gibt es $3! =6$ Permutationen. Nach kurzer Rechnung erhält man die Form
$$
\left|\begin{matrix}
a_{11} & a_{12} & a_{13} \\
a_{21}  & a_{22}  & a_{23}  \\
a_{31}  & a_{32}  & a_{33}
\end{matrix}\right|
=a_{11}a_{22}a_{33}+a_{12}a_{23}a_{31}+a_{13}a_{21}a_{32}-a_{13}a_{22}a_{31}-a_{12}a_{21}a_{33}-a_{11}a_{23}a_{32}
$$
die so genannte #Regel_von_Sarrus

Man beachte aber, dass für eine Dreiecksmatrix
$$
A_{\vartriangle} = \left(\begin{matrix}
a_{11} & a_{12} & \dots a_{1n} \\
0  & a_{22}  & \dots  & a_{2n} \\
\vdots  & \vdots   & \vdots  & \vdots \\
0  & \dots  & 0  & a_{nn}
\end{matrix}\right)
$$
die Determinante leicht zu berechnen ist, da nur ein einziger Summand, nämlich jener, der zur identischen Permutation gehört ungleich 0 ist.
$$
\det_{\vartriangle}=a_{11},a_{22},\dots a_{nn}
$$
Die Determinante hat im Reellen eine interessante geometrische Interpretation. Das Volumen des von Spalten von $A\in \mathbb{R}^{n\times n}$ aufgespannten "Parallelepipeds" 
$$
P=\{ t_{1}a_{1}+\dots+t_{n}a_{n}|0\leq t_{1},\dots,t_{n}\leq1 \}
$$
ist der Betrag der Determinante von $A:Vol(P)=|\det A|$. Offensichtlich hat $P$ nur dann positives Volumen, wenn die Spalten von $A$ linear unabhängig sind, also wenn $A$ invertierbar ist.

Eine Matrix $A\in K^{n\times n}$ ist genau dann invertierbar, wenn $$
\det A \neq0
$$
Sind also die Spalten oder Zeilen von $A$ linear abhängig oder sind zwei Spalten oder Zeilen sogar gleich, so ist $\det A=0$.

## Eigenschaften von Determinanten
Die folgenden beiden Sätze geben weitere Eigenschaften der Determinante an. 

- (i) Für beliebige Matrizen $A,B\in K^{n\times n}$ gilt $$
\det(A\cdot B)=\det A\cdot \det B
$$
- (ii) Ist $A\in K^{n\times n}$ invertierbar, so berechnet sich die Determinante der inversen Matrix durch $$
\det(A^{-1})=(\det A)^{-1}
$$
- (iii) Für $A\in K^{n\times n}$ gilt $$
\det(A^{T})=\det A
$$
- (iv) Multipliziert man eine Spalte/Zeile einer Matrix $A$ mit einem Faktor $\lambda\in K$, so ist die Determinante der neuen Matrix $\det A'=\lambda \det A$.

- (v) Addiert man zu einer Spalte/Zeile einer Matrix das Vielfache einer anderen Spalte/Zeile, so verändert sich der Wert der Determinante nicht.
- (vi) Vertauscht man in einer Matrix $A$ zwei Spalten/Zeilen, so ist die Determinante der neuen Matrix $\det A'=-\det A$

Mit elementaren Spalten- und Zeilenumformungen kann jede Matrix in eine obere Dreiecksmatrix umgeformt werden. 

### Beispiel
Die Determinante der Matrix
$$
A=\left(\begin{matrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{matrix}\right)
$$
berechnet sich nach geeigneten elementaren Zeilenumformungen zu
$$
\left|\begin{matrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 &9 \\
\end{matrix}\right|
=\left|\begin{matrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & -6 & -12
\end{matrix}\right|
=\left|\begin{matrix}
1 & 2 & 3 \\
0 & -3  & -6 \\
0  & 0  & 0
\end{matrix}\right| = 0
$$


## Kofaktor
Sei $A\in K^{n\times n}$. Unter dem #Kofaktor $A_{ij} ~~(1\leq i,j\leq n)$ versteht man die Determinante jener Matrix, die dadurch hervorgeht, dass man die $j$-te Spalte durch den Vektor $e_{i}$ der kanonischen Basis ersetzt. 

Addiert man entsprechende Vielfache von $e_{i}$ zu den Spalten $a_{1},\dots a_{j-1},a_{j+1},\dots,a_{n}$ von $A$, so kann man erreichen, dass in der $i$-ten Zeile dieser Spalten nur mehr 0 steht. Es gilt daher auch
$$
A_{ij}=\left|\begin{matrix}
a_{11} & \dots  &  a_{1,j-1}   & 0  & a_{1,j+1}   & \dots  & a_{1n} \\
\vdots  &   & \vdots  & \vdots  & \vdots  &   & \vdots \\
a_{i-1,1}  & \dots  & a_{i-1,j-1}  & 0  & a_{i-1,j+1}  & \dots  & a_{i-1,n} \\
0  & \dots  & 0  & 1  & 0  & \dots  & 0 \\
a_{i+1,1}  & \dots  & a_{i+1,j-1}  & 0  & a_{i+1,j+1}  & \dots  & a_{i+1,n} \\
\vdots  &   & \vdots  & \vdots  & \vdots  &   & \vdots \\
a_{n 1} & \dots  & a_{n,j-1}  & 0  & a_{n,j+1}  & \dots  & a_{nn}
\end{matrix}\right|
$$
In dieser Determinante sind sozusagen die Informationen, welche die $i$-te Zeile und die $j$-te Spalte enthalten, "gelöscht" worden. Tatsächlich besteht ein enger Zusammenhang zwischen $A_{ij}$ und jener Matrix, wo die $i$-te Zeile und die $j$-te Spalte tatsächlich gestrichen werden.

Sei $D_{ij} ~~(1\leq i,j\leq n)$ die Determinante jener Matrix aus $K^{(n-1)\times(n-1)}$, die aus $A\in K^{n\times n}$ dadurch hervorgeht, dass die $i$-te Zeile und die $j$-te Spalte gestrichen werden. Dann gilt $$
A_{ij}=(-1)^{i+j}D_{ij}
$$
## Laplace'scher Entwicklungssatz
Sei $A=(a_{ij})\in K^{n\times n}$

- (i) #Entwicklung_nach_der_i-ten_Zeile: Für jedes $i~~(1\leq i\leq n)$ gilt $$
\det A=\sum_{j=1}^{n}a_{ij}A_{ij}=\sum_{j=1}^{n}(-1)^{i+j}a_{ij}D_{ij}
$$
- (ii) #Entwicklung_nach_der_j-ten_Spalte: Für jedes $j~~(1\leq j\leq n)$ gilt $$
\det A=\sum_{i=1}^{n}a_{ij}A_{ij}=\sum_{i=1}^{n}(-1)^{i+j}a_{ij}D_{ij}
$$
Mit Hilfe dieses Satzes kann das Berechnen der Determinante einer $n\times n$-Matrix auf das Berechnen von $n$ Determinanten von $(n-1)\times(n-1)$-Matrizen zurückgeführt werden. Dabei kann die Determinante nach jeder beliebigen Zeile oder Spalte entwickelt werden.

### Beispiele
Entwickelt man die Determinante
$$
\left|\begin{matrix}
1 & 2  & 3 \\
4  & 5  & 6 \\
7  & 8  & 9 
\end{matrix}\right|
$$
nach der $1$. Zeile, so ergibt sich
$$
\left|\begin{matrix}
1 & 2 & 3 \\
4  & 5  & 6 \\
7  & 8  & 9   
\end{matrix}\right|
= 1\cdot \left|\begin{matrix}
5 & 6 \\
8 & 9
\end{matrix}\right|
- 2\cdot \left|\begin{matrix}
4 & 6 \\
7 & 9
\end{matrix}\right|
+3\cdot \left|\begin{matrix}
4 & 5 \\
7 & 8
\end{matrix}\right|
$$
$$
=(5\cdot9-6\cdot 8)-2\cdot(4\cdot9-6\cdot 7)+3\cdot(4 \cdot 8-5\cdot 7)=0
$$
Sei $A\in K^{n\times n}$ und berechne $\hat{A}=(A_{ij})\in K^{n\times n}$ die Matrix der Kofaktoren von $A$. Dann gilt $$
A\cdot \hat{A}^{T}=(\det A)I_{n}
$$
### Kofaktor Eigenschaft
Insbesondere gilt für reguläre Matrizen $A\in K^{n\times n}$
$$
A^{-1}=\frac{1}{\det A}\hat{A}^{T}=\left( \frac{A_{ij}}{\det A} \right)_{1\leq i,j\leq n}
$$
#### Beispiel
Die inverse Matrix einer regulären $2\times2-$Matrix hat die folgende Form
$$
\left(\begin{matrix}
a_{11} & a_{12} \\
a_{21}   & a_{22} 
\end{matrix}\right)^{-1}
=\frac{1}{a_{11}a_{22}-a_{12}a_{21}}
\left(\begin{matrix}
a_{22} & -a_{12} \\
-a_{21} & a_{11}
\end{matrix}\right)
$$

Sei $A\in K^{n\times n}$ eine reguläre Matrix und $b\in K^{n}$. Dann kann das lineare Gleichungssystem $A\cdot x=b$ immer eindeutig gelöst werden. Die einzige Lösung ist durch $$
x=A^{-1}\cdot b
$$
gegeben. Da $A^{-1}$ durch Determinanten explizit berechnet werden kann, ist damit die Lösung $x=A^{-1}\cdot b$ auch explizit anzugeben. Dieses Verfahren kann aber noch abgekürzt werden

## Cramer'sche Regel
Sei $A\in K^{n\times n}$ eine reguläre Matrix und $b\in K^{n}$. Bezeichnet man mit $A_{j} ~~(1\leq j\leq n)$ jene Matrix, die aus $A$ dadurch hervorgeht, dass man die $j$-te Spalte durch $b$ ersetzt, so ist die einzige Lösung des linearen Gleichungssystems $Ax=b$ durch
$$
x=\frac{1}{\det A}\left(\begin{matrix}
\det A_{1} \\
\det A_{2} \\
\vdots \\
\det A_{n}
\end{matrix}\right)
$$
gegeben.

Man kann also durch $x_{j}= \frac{\det A_{j}}{\det A}$ jede Koordinate der Lösung einzeln berechnen. 

### Beispiel
Die eindeutige Lösung $(x_{1},x_{2})$ eines regulären linearen Gleichungssystems 
$$
a_{11}x_{1} + a_{12}x_{2}=b_{1}
$$
$$
a_{21}x_{1}+a_{22}x_{2}=b_{2}
$$
ist gegeben durch
$$
x_{1} = \frac{\left|\begin{matrix}
b_{1} & a_{12} \\
b_{2} & a_{22}
\end{matrix}\right|}{\left|\begin{matrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{matrix}\right|}
=\frac{b_{1}a_{22}-b_{2}a_{12}}{a_{11}a_{22}-a_{12}a_{21}}
$$
und 
$$
x_{2}= \frac{\left|\begin{matrix}
a_{11} & b_{1} \\
a_{21} & b_{2}
\end{matrix}\right|}{\left|\begin{matrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{matrix}\right|}
=\frac{-b_{1}a_{21}+b_{2}a_{11}}{a_{11}a_{22}-a_{12}a_{21}}
$$

