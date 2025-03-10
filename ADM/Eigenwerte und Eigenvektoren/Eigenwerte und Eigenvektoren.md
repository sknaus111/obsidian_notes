## Definition von Eigenwerten und Eigenvektoren
Sei $f:V\rightarrow V$ eine lineare Abbildung. Ein Skalar $\lambda\in K$ heißt #Eigenwert von $f$, wenn es einen Vektor $x\in V\setminus\{ 0 \}$ mit $$
f(x)=\lambda \cdot x
$$
gibt. Die Vektoren $x\in V\setminus\{ 0 \}$ mit $f(x)=\lambda \cdot x$ heißen die zum Eigenwert $\lambda$ gehörigen #Eigenvektoren. 

Sei $A\in K^{n\times n}$ eine quadratische Matrix. Ein Skalar $\lambda\in K$ heißt Eigenwert von $A$, wenn es einen Vektor $x\in K^{n}\setminus\{ 0 \}$ mit $$
A\cdot x=\lambda \cdot x
$$ gibt. Die Vektoren $x\in K^{n}\setminus\{ 0 \}$ mit $A\cdot x=\lambda \cdot x$ heißen die zum Eigenwert $\lambda$ gehörigen Eigenvektoren. 

### Beispiele
Es geht um das Problem, die "Wichtigkeit" einer Internetseite zu bewerten. Ein Ansatz dafür ist, anzunehmen, dass die Wichtigkeit $x_{i}$ der $i$-ten Internetseite proportional zur Summe der Wichtigkeiten jener Seiten ist, die einen Link zur $i$-ten Seite haben. Man bekommt daher ein Gleichungssystem der Form $$
x_{i}=K\sum_{j=1}^{n}a_{ij}x_{j} ~~~~~~~~~~~~~(1\leq i\leq n)
$$
wobei $n$ die Anzahl der Internetseiten ist und $a_{ij}=1$ ist, wenn die Seite $j$ einen Link zur Seite $i$ hat; sonst ist $a_{ij}=0$. Das ist nichts anderes als ein Eigenwertproblem mit einer gigantisch großen Matrix $A=(a_{ij})$. 

## Eigenwerte bestimmen
Sei $A\in K^{n\times n}$ eine quadratische Matrix. Ein Skalar $\lambda\in K$ ist genau dann Eigenwert von $A$, wenn $$
\det(\lambda \cdot I_{n}-A)=0
$$
### Beweis
Die Existenz eines Vektors $x\not=0$ mit $A\cdot x=\lambda \cdot x$ ist gleichbedeutend mit der Existenz eines Vektors $x\neq 0$ mit $$
(\lambda \cdot I_{n}-A)\cdot x=0
$$
Das heißt, dass homogene lineare Gleichungssystem mit Koeffizienten Matrix $\lambda \cdot I_{n}-A$ eine nichttriviale Lösung hat. Dies ist aber genau dann der Fall, wenn $\lambda \cdot I_{n}-A$ singulär ist, also wenn $\det(\lambda \cdot I_{n}-A)=0$ gilt.

### Beispiel
Zur Bestimmung der Eigenwerte der Matrix $$
A=\left(\begin{matrix}
1 & 2 \\
3 & 2
\end{matrix}\right)
\in \mathbb{R}^{2\times_{2}}
$$
ermittelt man zunächst
$$
\lambda \cdot I_{2}-A=\left(\begin{matrix}
\lambda & 0 \\
0 & \lambda
\end{matrix}\right)
- \left(\begin{matrix}
1 & 2 \\
3 & 2
\end{matrix}\right)
=\left(\begin{matrix}
\lambda-1 & -2 \\
-3 & \lambda-2
\end{matrix}\right)
$$
und die Determinante
$$
\det(\lambda \cdot I_{2}-A)=\left|\begin{matrix}
\lambda-1 & -2 \\
-3 & \lambda-2
\end{matrix}\right|
=\lambda^{2}-3\lambda-4
$$
Dieses quadratische Polynom hat genau 2 Nullstellen
$$
\lambda_{1}=4,\lambda_{2}=-1
$$
Diese sind die 2 Eigenwerte von $A$.

Als nächstes bestimmen wir die Eigenvektoren zum Eigenwert $\lambda_{1}=4$. Dazu muss man das homogene lineare Gleichungssystem $$
(4\cdot I_{2}-A)\cdot x=\left(\begin{matrix}
3 & -2 \\
-3 & 2
\end{matrix}\right)\cdot x=0
$$
lösen. Man sieht sofort, dass alle Eigenvektoren skalare Vielfache des Vektors

$$
3x_{1} -2x_{2} = 0
$$
$$
-3 x_{1} + 2x_{2} = 0
$$
$$
3x_{1}=2x_{2}
$$
$$
x_{1}=\left(\begin{matrix}
2 \\
3
\end{matrix}\right)
$$
sind. Die Menge aller Eigenvektoren zum Eigenwert $\lambda_{1}=4$ bildet daher einen eindimensionalen Unterraum von $\mathbb{R}^{2}$.

Entsprechend kann man auch zum Eigenwert $\lambda_{2}=-1$ alle Eigenvektoren bestimmen. Es sind dies alle skalaren Vielfachen des Vektors
$$
\left(-1 \cdot I_{2} - A\right) \cdot x = \left(\begin{matrix}
-2 & -2 \\
-3 & -3
\end{matrix}\right) \cdot x = 0
$$
$$
-2 x_{1} -2x_{2} = 0
$$
$$
-3 x_{1}-3x_{2} =0
$$
$$
x_{1}=-x_{2}
$$
$$
x_{2}=\left(\begin{matrix}
1 \\
-1
\end{matrix}\right)
$$
Man beachte, dass die beiden Eigenvektoren $x_{1},x_{2}$ lineare unabhängig sind. Bildet man damit die reguläre Matrix $T=(x_{1},x_{2})\in \mathbb{R}^{2\times2}$, so kann man die Beziehung $A\cdot x_{1}=4\cdot x_{1}$, $A\cdot x_{2}=-1\cdot x_{2}$ in Matrixform auch folgendermaßen darstellen.
$$
\left(\begin{matrix}
1 & 2 \\
3 & 2
\end{matrix}\right)
\cdot \left(\begin{matrix}
2 & 1 \\
3 & -1
\end{matrix}\right)
=\left(\begin{matrix}
2 & 1 \\
3 & -1
\end{matrix}\right)
\cdot \left(\begin{matrix}
4 & 0 \\
0 & -1
\end{matrix}\right)
$$
bzw. 
$$
A\cdot T=T\cdot \left(\begin{matrix}
\lambda_{1} & 0 \\
0 & \lambda_{2}
\end{matrix}\right)
$$
oder $$
A=T\cdot \left(\begin{matrix}
\lambda_{1} & 0 \\
0 & \lambda_{2}
\end{matrix}\right) \cdot T^{-1}
$$
In diesem Beispiel fallen zwei Punkte auf. Zunächst tritt ein Polynom auf, das so genannte charakteristische Polynom.

## Charakteristische Polynom
Das #charakteristische_Polynom einer quadratischen Matrix $A\in K^{n\times n}$ ist die Determinante $$
\chi_{A}(\lambda)=\det (\lambda \cdot I_{n}-A)
$$
Man beachte, dass das charakteristische Polynom Grad $n$ und Führungskoeffizient 1 hat. Eigenwerte sind jetzt nichts anderes als Nullstellen von $\chi_{A}(\lambda)$. Da ein Polynom vom Grad $n$ höchstens $n$ verschiedene Nullstellen haben kann, hat eine $n\times n$-Matrix $A$ höchstens $n$ verschiedene Eigenwerte.

Die zweite Beobachtung ist, dass man unter gewissen Voraussetzungen mit Hilfe von Eigenwerten und Eigenvektoren eine Matrix diagonalisieren kann. 

### Diagonalisierung
Sind die Vektoren $x_{1},x_{2},\dots,x_{n}\in K^{n}$ lineare unabhängig und Eigenvektoren einer Matrix $A\in K^{n\times n}$ zu den Eigenwerten $\lambda_{1},\lambda_{2},\dots,\lambda_{n}\in K$, so gilt mit $T=(x_{1}~x_{2} ~\dots~x_{n})$
$$
A=T\cdot diag(\lambda_{1},\lambda_{2},\dots,\lambda_{n})\cdot T^{-1}
$$
Man bezeichnet die Matrix $A$ in diesem Fall als #diagonalisierbar.

Mit diagonalisierbaren Matrizen kann i.Allg. einfacher gerechnet werden. Beispielsweise gilt für die Potenzen dieser Matrizen
$$
A^{k}=T\cdot diag(\lambda_{1}^{k},\lambda_{2}^{k},\dots,\lambda_{n}^{k})\cdot T^{-1}
$$
