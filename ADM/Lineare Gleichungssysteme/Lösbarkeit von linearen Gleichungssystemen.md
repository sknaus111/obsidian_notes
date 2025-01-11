## Lineare Gleichungssysteme
Seien $m,n,\geq 1$ ganze Zahlen und $K$ ein Körper. Weiters seien Elemente $a_{ij}\in K~~(1\leq i\leq m,1\leq j\leq n)$ und $b_{i}\in K~~(1\leq i\leq m)$ gegeben. Dann heißt ein System der Form
$$
\begin{matrix}
a_{11}x_{1} & + & \dots  & + & a_{1n}x_{n} & = & b_{1} \\
a_{21}x_{1} & + & \dots & + & a_{2n}x_{n} & = & b_{2} \\
\vdots & \vdots & & \vdots & \vdots & \vdots & \vdots \\
a_{m_{1}}x_{1} & + & \dots & + & a_{mn}x_{n} & = & b_{m}
\end{matrix}
$$
#linearen_Gleichungssystem in den Unbekannten $x_{1},x_{2},\dots,x_{n} \in K$. Sind alle $b_{1}=b_{2}=\dots=b_{m}=0$, so heißt das lineare Gleichungssystem #homogen, sonst #inhomogen

Es besteht nun die Aufgabe, ein lineares Gleichungssystem vollständig zu lösen, d.h. alle $n$-Tupel $(x_{1},x_{2},\dots,x_{n}) \in K^{n}$ anzugeben, die das obige Gleichungssystem erfüllen. Fasst man die Koeffizienten $a_{ij}$ zu einer Matrix $A=(a_{ij})\in K^{m\times n}$ zusammen und entsprechend auch dir rechte Seiter $b_{1},b_{2},\dots,b_{n}$ zu einem Spaltenvektor $b\in K^{m}$ sowie die Unbekannten $x_{1},x_{2},\dots x_{n}$ zu einem Spaltenvektor $x\in K^{n}$, so lässt sich ein lineares Gleichungssystem folgendermaßen darstellen
$$
A\cdot x=b
$$
Das bedeutet aber, dass es genau dann eine Lösung $x$ gibt, wenn $b$ Linearkombinationen der Spalten von $A$ ist. Daraus ergibt sich das folgende Lösungskriterium.

### Satz von Kronecker-Capelli
Sei $A\in K^{m\times n}$ und $b\in K^{m}$. Dann ist das lineare Gleichungssystem $Ax=b$ genau dann lösbar, wenn
$$
rg(A)=rg(A\cdot b)
$$
Die Matrix $(A\cdot b)$ bezeichnet man auch als erweiterte Systemmatrix des linearen Gleichungssystem $A\cdot x=b$.

### Lösungsmenge
Um alle Lösungen eines linearen Gleichungssystems beschreiben zu können, verwenden wir die Interpretation der Matrizemultiplikation als lineare Abbildung: $f(x)=A\cdot x$. Wir setzen voraus, dass das lineare Gleichungssystem $f(x)=A\cdot x=b$ eine Lösung $x_{0}$ hat. Ist nun $x$ irgend eine andere Lösung, so folgt aus $f(x_{0})=f(x)=b$ auch
$$
f(x-x_{0})=A\cdot(x-x_{0})=0
$$
Daher liegt $x-x_{0}$ im Kern von $f$, und alle Lösungen $L$ des linearen Gleichungssystem können durch
$$
L=x_{0}+ker(f)
$$
also durch einen Nebenraum des Kerns von $f$ beschrieben werden. Aus der Rangformel folgt $dim(ker(f))=n-rg(f)=n-rg(A)$. Daher kann man die Lösungsmenge $L$ auch folgendermaßen angeben:

Sei $A\in K^{m\times n}$ und $b\in K^{m}$. Ist das lineare Gleichungssystem $Ax=b$ lösbar, so gibt es $s=n-rg(A)$ linear unabhängige Vektoren $x_{1},\dots x_{n}\in ker(f)\subseteq K^{n}$, d.h. Lösungen des homogenen linearen Gleichungssystem $A\cdot x=0$, so dass alle Lösungen von $A\cdot x=b$ durch die Menge
$$
\{ x_{0}+t_{1}x_{1}+\dots+t_{s}x_{s}|t_{1},\dots,t_{s}\in K \}
$$
gegeben sind, wobei $x_{0}$ eine beliebige, aber fest gewählte Lösung von $A\cdot x=b$ ist.

Man beachte, dass die Vektoren $x_{1},x\dots,x_{s}$, die ja eine Basis des Kerns von $f$, also Lösungen des homogenen linearen Gleichungssystems $A\cdot x=0$ sind, nicht von der rechten Seite $b$ abhängen. Diese müssen jedenfalls bestimmt werden. Zu jeder rechten Seite $b$ reicht es dann, noch eine Lösung $x_{0}$ des inhomogenen linearen Gleichungssystems $A\cdot x=b$ zu finden. Die Gesamtlösung $L$ wird dann aus $x_{0}$ und Linearkombinationen von $x_{1},\dots,x_{s}$ zusammengesetzt. Aus der Interpretation eines linearen Gleichungssystems $A\cdot x=b$ in der Form $f(x)=b$ ergibt sich auch der nächste Satz. 

Sei $A\in K^{m\times n},f(x)=A\cdot x$ und $b\in K^{m}$.
Ist $f$ surjektiv, d.h. $rg(f)=rg(A)=m$, so ist das lineare Gleichungssystem $A\cdot x=b$ für alle rechten Seiten $b\in K^{m}$ lösbar.
Ist $f$ injektiv, d.h. $rg(f)=rg(A)=n$, so ist $ker(f)=\{ 0 \}$, und das lineare Gleichungssystem $A\cdot x=b$ hat höchstens eine Lösung.

Ein wichtiger Spezialfall ist jener, wo die Matrix $A\in K^{n\times n}$ quadratisch ist. Ist $A$ zusätzlich regulär, also invertierbar, so ist das lineare Gleichungssystem $A\cdot x=b$ für jede rechte Seite $b\in K^{n}$ eindeutig lösbar, und die Lösung ist gegeben durch
$$
x=A^{-1}\cdot b
$$
Insbesondere ist für $b=0$ die Lösung $x=A^{-1}\cdot 0=0$. Übrigens hat ein homogenes System $A\cdot x=0$ immer den Nullvektor als Lösung. Nur wenn $A$ invertierbar ist, ist der Nullvektor die einzige Lösung. Anders ausgedrückt bedeutet das, dass ein System $A\cdot x=0$ mit quadratischer Matrix $A$ genau dann eine Lösung hat, wenn $A$ singulär, also nicht invertierbar ist.

### Lösen linearer Gleichungsysteme
Das Lösen eines linearen Gleichungssystems ist besonders einfach, wenn die Matrix $A$ von spezieller Gestalt ist

#### Basisgestalt
Sei $A\in K^{m\times n} ~~(n\geq m)$ eine Matrix der Gestalt
$$
A=\left(\begin{matrix}
1 & 0 & \dots & 0 & a_{1,m+1} & \dots & a_{1,n} \\
0 & 0 & \dots & 0 & a_{2,m+1} & \dots & a_{2,n} \\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots \\
0 & \dots & 0 & 1 & a_{m,m+1} & \dots & a_{m,n}
\end{matrix}\right) = (I_{m}A')
$$
mit $A'\in K^{m\times(n-m)}$, so sind alle Lösungen $x=(x_{1},\dots,x_{n})^{T}\in K^{n}$ des Gleichungssystems $Ax=b$ gegeben durch
$$
x=\left(\begin{matrix}
b \\
0
\end{matrix}\right)
+ \left(\begin{matrix}
-A' \\
I_{n-m}
\end{matrix}\right)
\left(\begin{matrix}
t_{1} \\
\vdots \\
t_{n-m}
\end{matrix}\right)
$$
bzw.
$$
\left(\begin{matrix}
x_{1} \\
\vdots \\
x_{m} \\
x_{m+1} \\
\vdots \\
x_{n}
\end{matrix}\right)
= \left(\begin{matrix}
b \\
0
\end{matrix}\right)
+ t_{1} \left(\begin{matrix}
-a_{m+1} \\
e_{1}
\end{matrix}\right)
+t_{2} \left(\begin{matrix}
-a_{m+2} \\
e_{2}
\end{matrix}\right)
+\dots+
t_{n-m}\left(\begin{matrix}
-a_{n} \\
e_{n-m}
\end{matrix}\right)
$$
mit $t_{1},t_{2},\dots,t_{n-m}\in K$. Dabei bezeichnen $a_{m+1},\dots,a_{n}$ die Spalten von $A'$, $0$ den Nullvektor in $K^{n-m}$ und $e_{1},\dots,e_{n-m}$ die Vektoren der kanonischen Basis von $K^{n-m}$.

##### Beweis
Die obige Formel ist offensichtlich, wenn man das Gleichungssystem in der Koordinatenschreibweise betrachtet und $t_{1}=x_{m+1},\dots t_{n-m}=x_{n}$ setzt. Die übrigen Koordinaten $x_{1},\dots ,x_{m}$ ergeben sich dann direkt: $x_{i}=b_{i}-x_{m+1}a_{i,m+1} - \dots-x_{n}a_{i,n}=b_{i}-t_{1}a_{i,m+1}-\dots-t_{n-m}a_{i,n} ~~(\text{für} 1\leq i\leq m)$

#### Dreiecksgestalt
Das gerade angegebene Verfahren funktioniert auch, wenn die Matrix $A\in K^{m\times n}(n\geq m)$ eine so genannte Dreiecksgestalt mit nichtverschwindender Diagonale hat:
$$
A=\left(\begin{matrix}
a_{1,1} & a_{1,2}  & \dots  & a_{1,m}  & a_{1,m+1}  & \dots& a_{1,n} \\
0  & a_{2,2}  & \dots  & a_{2,m}  & a_{2,m+1}&\dots & a_{2,n}  \\
\vdots  & \vdots  & \vdots   & \vdots  & \vdots  & \vdots  & \vdots \\
0  & \dots  & 0  & a_{m,m}  & a_{m,m+1}  & \dots  & a_{m,n}
\end{matrix}\right)
$$
mit $a_{1,1}\not=0,\dots a_{m,m}\not=0$. Wie vorhin setzen wir $x_{m+1}=t_{1},\dots x_{n}=t_{n-m}$. Dann ermittelt man
$$
x_{m} = a_{m,m}^{-1} (b_{m}-t_{1}a_{m,m+1}-\dots-t_{n-m}a_{m,n})
$$
$$
= b'_{m-1}+t_{1}a'_{1,m-1}+\dots+t_{n-m}a'_{n-m,m-1}
$$
und danach rekursiv $x_{m-2},x_{m-3},\dots x_{1}$. Die Lösungen haben daher wieder die Form $\left(\begin{matrix}x_{1}  \\ \vdots \\ x_{m} \\ x_{m+1} \\ \vdots \\ x_{n}\end{matrix}\right)$ . Wir illustrieren dieses Verfahren an einem kleinen Beispiel

Wir betrachten das Gleichungssystem
$$
\left(\begin{matrix}
2   & 3  & -1 \\
0  & 1  & 2
\end{matrix}\right)
\cdot \left(\begin{matrix}
x_{1} \\
x_{2} \\
x_{3}
\end{matrix}\right)
=\left(\begin{matrix}
4 \\
3
\end{matrix}\right)
$$
bzw.
$$
2x_{1}+3x_{2}-x_{3}=4
$$
$$
x_{2}+2x_{3}=3
$$
Setzt man $x_{3}=t$, so folgt aus der 2. Gleichung $x_{2}=3-2x_{3}=3-2t$ und schließlich aus der 1. Gleichung $2x_{1}=4-3x_{2}+x_{3}=4-3(3-2t)+t$ bzw. $x_{1}=-\frac{5}{2}+\frac{7}{2}t$ . Insgesamt also 
$$
\left(\begin{matrix}
x_{1} \\
x_{2} \\
x_{3}
\end{matrix}\right)
=\left(\begin{matrix}
-\frac{5}{2} \\
3 \\
0
\end{matrix}\right)
+t \left(\begin{matrix}
\frac{7}{2} \\
-2 \\
1
\end{matrix}\right)
$$
