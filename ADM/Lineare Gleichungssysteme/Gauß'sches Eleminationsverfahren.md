Um allgemein ein Gleichungssystem lösen zu können wenden wir wieder verschiedene Elementare Zeilenumformungen an. Anders ausgedrückt multipliziert man mit einer invertierbaren Matrix $U\in K^{m\times m}$. Das lineare Gleichungssystem $A\cdot x=b$ wird durch $(UA)\cdot x=Ub$ ersetzt. Man kann weiters Spalten von $A$ vertauschen. Dies entspricht einfach einer Umnummerierung der Unbekannten $x_{1},x_{2},\dots,x_{n}$. Man erhält ein Verfahren zum Lösern allgemeiner linearer Gleichungssysteme, das #Gaußsche_Eleminationsverfahren . 

## Beispiel
Es soll das lineare Gleichungssystem
$$
x_{1}+2x_{2}-2x_{3}+3x_{4}=3
$$
$$
2x_{1}+5x_{2}+0+x_{4}=4
$$
$$
3x_{1}+8x_{2}+2x_{3}-x_{4}=5
$$
$$
x_{1}+4x_{2}+6x_{3}-7x_{4}=-1
$$
über einem Körper $K$ vollständig gelöst werden. Die Koeffizientenmatrix $A$ und die rechte Seite $b$ sind
$$
A=\left(\begin{matrix}
1  & 2 & -2  & 3 \\
2  & 5  & 0  & 1 \\
3  & 8  & 2  & -1 \\
1  & 4  & 6  & -7 
\end{matrix}\right)
$$
und
$$
b=\left(\begin{matrix}
3 \\
4 \\
5 \\
-1
\end{matrix}\right)
$$
Durch elementare Zeilenumformungen der erweiterten Matrix $(Ab)$ erhält man eine Matrix der Form
$$
\left(\begin{matrix}
1 & 2  & -2  & 3|  & 3 \\
2  & 5  & 0  & 1|  & 4 \\
3  & 8  & 2  & -1|  & 5 \\
1  & 4  & 6  & -7|  & -1
\end{matrix}\right) 
\rightarrow ~~(z_{2}=z_{2}-2z_{1},z_{3}=z_{3}-3z_{1},z_{4}=z_{4}-z_{1})~~$$$$\left(\begin{matrix}
1 & 2  & -2 &3 | &3 \\
0  & 1  & 4  & -5|   & -2 \\
0  & 2  & 8  & -10|   & -4 \\
0  & 2  & 8  & -10|   & -4
\end{matrix}\right)
\rightarrow (z_{3}=z_{3}-2z_{2},z_{4}=z_{4}-2z_{2}) \left(\begin{matrix}
1 &  2  & -2  & 3|  & 3 \\
0  & 1  & 4  & -5|  & -2 \\
0  & 0  & 0  & 0|  & 0 \\
0  & 0  & 0  & 0|  & 0
\end{matrix}\right)

$$
Das ursprüngliche lineare Gleichungssystem ist daher äquivalent zu
$$
x_{1}+2x_{2}-2x_{3}+3x_{4}=3
$$
$$
x_{2}+4x_{3}-5x_{4}=-2
$$
und wegen das Satzes von Kronecker-Capelli auch lösbar. Setzt man $x_{3}=t_{1}$ und $x_{4}=t_{2}$, so errechnet man
$$
x_{2}=-2-4x_{3}+5x_{4}
$$
$$
=-2-4t_{1}+5t_{2}
$$
$$
x_{1}=3-2x_{2}+2x_{3}-3x_{4}
$$
$$
7+10t_{1}-13t_{2}
$$
Alle Lösungen sind daher durch
$$
\left(\begin{matrix}
x_{1} \\
x_{2} \\
x_{3} \\
x_{4}
\end{matrix}\right)
=\left(\begin{matrix}
7 \\
-2 \\
0 \\
0
\end{matrix}\right)
+t_{1}\left(\begin{matrix}
10 \\
-4 \\
0 \\
0
\end{matrix}\right)
+t_{2}\left(\begin{matrix}
-13 \\
5 \\
0 \\ 
1
\end{matrix}\right)
$$
mit $t_{1},t_{2}\in K$ gegeben.

Selbstverständlich hätte man mit einer weiteren Zeilenumformung auch zu einer Matrix folgender Form umformen können
$$
\left(\begin{matrix}
1 & 2   & -2   & 3|   & 3 \\
0  & 1  & 4  & -5|  & -2 \\
0  & 0  & 0  & 0|  & 0 \\
0  & 0  & 0 & 0|  & 0
\end{matrix}\right)
\rightarrow ~~ (z_{1}=z_{1}-2z_{2}) ~~\left(\begin{matrix}
1 & 0 & -10  & 13|   & 7 \\
0  & 1  & 4  & -5|  & -2 \\
0  & 0  & 0  & 0|  & 0 \\
0  & 0  & 0  & 0|  & 0
\end{matrix}\right)
$$
## Konkreter Ablauf
Wir formulieren nun das Gauß'sche Eleminationsverfahren. Es sei also $A\cdot x=b~~(A\in K^{m\times n},b\in K^{m})$ ein lineares Gleichungssystem, wobei wir voraussetzen, dass $A$ nicht die Nullmatrix ist. Man bildet die erweiterte Systemmatrix $(Ab)$ und führt folgende Zeilenumformungen durch

- (i) Durch etwaiges Zeilenvertauschen in $(Ab)$ bzw. Spaltenvertauschen in $A$ erreicht man, dass $a_{11}\not=0$ ist. Danach ersetzt man die $j$-te Zeile $(\tilde{a}_{j}~b_{j})$ von $(A~b)$ (für $2\leq j\leq m$) durch $(\tilde{a}_{j}~b_{j})-a_{11}^{-1}a_{j 1}(\tilde{a}_{1} ~ b_{1})$ und erhält eine Matrix der Form$$
\left(\begin{matrix}
a_{11} & a_{12} & \dots & a_{1n} | & b_{1} \\
0   & a_{22} & \dots & a_{2n}| & b_{2} \\
\vdots & \vdots & & \vdots| &\vdots \\
0 & a_{m2} & \dots & a_{nm}| & b_{m}
\end{matrix}\right)
$$
d.h. in der ersten Spalte ist nur das erste Element $a_{11}$ ungleich $0$.

- (ii) Daraufhin betrachtet man die Untermatrix$$
\left(\begin{matrix}
a_{22} & \dots & a_{2n}| & b_{2} \\
a_{32} & \dots & a_{3n} | & b_{3} \\
\vdots & & \vdots | &\vdots \\
a_{m2} & \dots & a_{mn}| &b_{m}
\end{matrix}\right)=(A'~b')
$$
und wendet darauf dasselbe Verfahren an wie in (i) auf $(A~b)$. Man beachte, dass diese Matrix einem linearen Gleichungssystem entspricht, in dem die Unbekannte $x_{1}$ nicht mehr vorkommt. Sie wurde eliminiert. Dies erklärt auch den Namen Eleminationsverfahren. Insgesamt erhält man dabei eine Matrix der Gestalt
$$
\left(\begin{matrix}
a_{11} & a_{12} & a_{13} & \dots & a_{1n}|    & b_{1} \\
0  & a_{22}  & a_{23}  & \dots  & a_{2n} |  & b_{2} \\
\vdots  & \vdots  & \vdots  &    & \vdots|  & \vdots \\
0  & 0  & a_{m3}   & \dots  & a_{mn}|  & b_{m} 
\end{matrix}\right)
$$
mit $a_{11}\not=0$ und $a_{12}\not=0$

- (iii) Das soeben beschriebene Verfahren wird so lange wie möglich iterativ fortgesetzt. Man gewinnt schließlich eine Matrix der Form $$
\left(\begin{matrix}
a_{11}  & a_{12}  & \dots  & a_{1r}  & a_{1,r+1}   & \dots  & a_{1n}|  & b_{1} \\
0  & a_{22}  & \dots  & a_{2r}  & a_{2,r+1}  & \dots  & a_{2n} |  & b_{2} \\
\vdots  & \vdots  & \vdots  & \vdots  & \vdots  &   & \vdots |   & \vdots \\
0  & \dots  & 0  & a_{rr}   & a_{r,r+1}  & \dots  & a_{rn} |   & b_{r} \\
0  & \dots  & 0  & 0  & 0  & \dots  & 0|  & b_{r+1} \\
\vdots  &   & \vdots  & \vdots  & \vdots  &   & \vdots|  & \vdots \\
0  & \dots  & 0  & 0  & 0  & ..  & 0|  & b_{m} 
\end{matrix}\right)
=(A^{*}~b^{*})
$$
mit $a_{11}\not=0,\dots a_{rr}\not=0$. Dabei ist $r$ der rang der Matrix $A$. Diese Transformation wurde durch sukzessive elementare Zeilenumformungen der ursprünglichen erweiterten $(A~b)$ Matrix gewonnen. Es gibt daher eine reguläre Matrix $U\in K^{m\times m}$(und eine Spaltentransformationsmatrix $T\in K^{n\times n}$) , so dass
$$
A^{*}=UAT
$$
und
$$
b^{*}=UB
$$
Weiters können wir alle vollständigen Nullzeilen von $(A^{*}~b^{*})$ weglassen, ohne die Lösung zu verändern, d.h. wir streichen alle Zeilen mit Index $j ~(r<j\leq m)$ und $b_{j}=0$

- (iv) Man unterscheide nun drei Fälle

1. Ist $r<m$ und gibt es ein Element $b_{j}\not=0,r<j\leq m$, so ist $rg(A^{*}~b^{*})>rg(A^{*})$ und somit das ursprüngliche lineare Gleichungssystem $Ax=b$ unlösbar.


2. Ist nach dem Streichen der Nullzeilen $r=n$, so gib es eine eindeutige Lösung. Die Unbekannte $x_{n}$ kann direkt bestimmt werden, darauf $x_{n-1}$ usw.

3. Ist nach dem Streichen der Nullzeilen $r<n$, so gibt es unendlich viele Lösungen. In diesem Fall ist $rg(A^{*}~b^{*})=rg(A^{*})$, und das ursprüngliche lineare Gleichungssystem $A\cdot x=b$ ist lösbar. Es hat dieselben Lösungen wie $A^{*}\cdot x=b^{*}$. Wir enthalten eine mehrdeutige Lösung mit $s=n-r$ Parametern $t_{1},\dots t_{s}$

## Weitere Beispiele
### a
Wir betrachten das lineare Gleichungssystem mit seiner erweiterten Systemmatrix:
$$
\begin{matrix}
x_{1} & & & + & x_{3} & = & 1 \\
2x_{1} & + & x_{2} & - & 2x_{3} & = & 0 \\
3x_{1} & + & x_{2} & - & x_{3} & = & -1
\end{matrix}
\rightarrow \left(\begin{matrix}
1 & 0 & 1 | & 1 \\
2 & 1 & -2 | & 0 \\
3 & 1 & -1 | & -1
\end{matrix}\right)
$$
Nach kurzer Umformung erhalten wir die Matrix
$$
\rightarrow ~~(z_{2}=z_{2}-2z_{1},z_{3}=z_{3}-3z_{1})~~ \left(\begin{matrix}
1 & 0  & 1|  & 1 \\
0  & 1  & -4 | & -2 \\
0  & 1  & -4|  & -4
\end{matrix}\right)$$$$
\rightarrow ~~(z_{3}=z_{3}-z_{2})~~
\left(\begin{matrix}
1 & 0 & 1 |  & 1 \\
0  & 1  & -4|  & -2 \\
0  & 0  & 0 |  & -2
\end{matrix}\right)
$$
Die letzte Zeile zeigt einen Widerspruch, somit kann es offensichtlich keine Lösung geben.

### b
Wir betrachten nun das leicht veränderte lineare Gleichungssystem:
$$
\begin{matrix}
x_{1} & & & + & x_{3} & = & 1 \\
2x_{1} & + & x_{2} & - & 2x_{3} & = & 0 \\
3x_{1} & + & x_{2} & & & = & 1 \\
\end{matrix}
\rightarrow \left(\begin{matrix}
1 & 0 & 1|  & 1 \\
2  & 1  & -2 |  & 0 \\
3  & 1  & 0 |  & 1
\end{matrix}\right)
$$
Hier erhalten wir die Matrix
$$
\rightarrow ~~(z_{2}=z_{2}-2z_{1},z_{3}=z_{3}-3z_{1})~~ \left(\begin{matrix}
1 & 0 & 1| & 1 \\
0 & 1  & -4 |  & -2 \\
0  & 1  & -3|  & -2
\end{matrix}\right)
$$
$$
\rightarrow ~~ (z_{3}=z_{3}-z_{2}) ~~ \left(\begin{matrix}
1 & 0 & 1| & 1 \\
0 & 1  & -4|  & -2 \\
0  & 0  & 1 |  &  0
\end{matrix}\right)
$$
Es gibt eine eindeutige Lösung. Aus der letzten Zeile folgt $x_{3}=0$. Damit erhalten wir aus der zweiten Zeile $x_{2}-4x_{3}=-2$ die Lösung $x_{2}=-2$ und schließlich aus der ersten Zeile $x_{1}+x_{3}=1$ dir erste Lösungskoordinate $x_{1}=1$.
