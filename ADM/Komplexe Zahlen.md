Um praktisch alle Zahlen abzudecken muss der Zahlenbegriff ein weiteres mal erweitert werden. Man betrachte die Gleichung
$$
x^2=-1
$$
Selbst in den reellen Zahl hat diese Gleichung keine Lösung, da das Quadrat einer reellen Zahl nicht negativ sein kann. Um Gleichung dieser Art zu lösen wird die #imaginäre_Zahl $i$ eingeführt, für welche gilt
$$
i^2=-1
$$
Die Menge $\mathbb{C}$ der #komplexen_Zahlen besteht aus den formalen Summen der Form
$$
z = a+ib \text{ mit }a,b \in \mathbb{R}
$$
Dabei heißt $a=\Re(z)$ auch #Realteil und $b=\Im(z)$ #Imaginärteil von $z$.

Beispielsweise ist $z=3+2i$ eine komplexe Zahl mit einem Realteil von $3$ und einem Imaginärteil von $2$.

Um komplexe Zahlen auf der Zahlengerade darzustellen muss diese mit dem hinzufügen einer y-Achse zur #Gaußschen_Ebene erweitert werden. In dieser werden komplexe Zahlen als #Zeiger dargestellt. Dieser Zeiger startet vom Ursprung bis zu den Koordinaten der komplexen Zahl. Als x Koordinate dient der Realteil und als y Koordinate der Imaginärteil. Die Länge des Zeigers wird auch als Betrag bezeichnet.

$$
r = |z| =\sqrt{ a^2+b^2 }
$$

```tikz
\begin{document}
\begin{tikzpicture}
\draw[->,thin] (-1,0) -- (10,0); 
\draw[->,thin] (0,-1) -- (0,5); 
\draw[->,thick] (0,0) -- (1,0) node [anchor=north] {1}; 
\draw[->,thick] (0,0) -- (0,1) node [anchor = east] {i}; 

\draw[-,thin] (8,4) -- (8,0) node [anchor = north] {$a=Re(z)$} ; 
\draw[-,thin] (8,4) -- (0,4) node [anchor = east] {$b=Im(z)$}; 

\draw[->,thick] (0,0) -- (8,4) node [anchor=north west] {$z=a+ib$} ;
\node at (5,3) {$r$};

\draw[->,thick] (3,0) arc [start angle=0, end angle=30, radius=2.6]; 
\node at (3.2,0.7) {$\varphi$};

\end{tikzpicture}
\end{document}
```

Komplexe Zahlen können auch als Polarkoordinaten $r$ und $\varphi$ dargestellt werden. $r$ ist wie zuvor bereits erwähnt der Betrag des Zeigers.  Das #Argument $\varphi = arg(z)$ bezeichnet den Winkel des Zeigers zur Achse der reellen Zahlen. Mithilfe der Winkelfunktionen ist es möglich zwischen den zwei Darstellungssystemen umzurechnen.

$$
a =r \cos \varphi, b=r\sin \varphi
$$
und 
$$
r^2 = a^2 + b^2, \tan \varphi = \frac{b}{a}
$$
Erwähnenswert ist, dass das Argument $\varphi$ modulo $2\pi$ bestimmt ist. Also auf das Intervall $(0,\pi)$ eingeschränkt ist für $b>0$ und $(\pi,2\pi)$ für $b<0$.

Um komplexe Zahlen zu addieren werden ihre einzelnen Realteile und Imaginärteile addiert.
$$
z_{1} = a_{1}+b_{1}i \text{ und }z_{2}=a_{2}+b_{2}i
$$
$$
z = z_{1} + z_{2} = (a_{1}+a_{2})+(b_{1}+b_{2})i
$$
Graphisch entspricht dies der #Parallelogrammregel

```tikz
\begin{document}
\begin{tikzpicture}
\draw[->,thin] (-1,0) -- (10,0); 
\draw[->,thin] (0,-1) -- (0,5); 

\draw[->,thick] (0,0) -- (5,3) ;
\node at (3.5,2.4) {$z_{1}$};

\draw[->,thick] (0,0) -- (6,-2) ;
\node at (3.5,-1.5) {$z_{2}$};

\draw[->,thick] (0,0) -- (11,1) ;
\node at (11.5,1.3) {$z=z_{1}+z_{2}$};

\draw[dashed,thick] (5,3) -- (11,1) ;
\draw[dashed,thick] (6,-2) -- (11,1) ;

\end{tikzpicture}
\end{document}
```
Ebenso ist es möglich komplexe Zahlen zu multiplizieren. Hierbei setzt man die Gültigkeit des #Distributivgesetz voraus und die Tatsache, dass $i^2=-1$
$$
z_{1}*z_{2}=(a_{1}+ib_{1})(a_{2}+ib_{2})=a_{1}a_{2}+ib_{1}a_{2}+ia_{1}b_{2}+i^2b_{1}b_{2}
$$
$$
 = (a_{1}a_{2}-b_{1}b_{2})+i(a_{1}b_{2}+a_{2}b_{1})
$$
Da $(a_{1}^2+b_{1}^2)(a_{2}^2+b_{2}^2)$ dem Ausdruck $(a_{1}a_{2}-b_{1}b_{2})^2+(a_{1}b_{2}+a_{2}b_{1})^2$ entspricht, kann abgeleitet werden das der Betrag des Produktes gleich ist wie das Produkt der einzelnen Beträge.
$$
|z_{1}*z_{2}| = |z_{1}| * |z_{2}|
$$
Das neue Argument setzt sich aus einer Addition der vorherigen Argumente $mod ~2\pi$ zusammen.
$$
arg(z_{1}*z_{2}) = arg(z_{1})+arg(z_{2}) ~~~mod~2\pi
$$
Dies kann aus den #Summensätzen der Winkelfunktionen abgeleitet werden.
Graphisch entspricht die Multiplikation einer #Drehstreckung des Zeigers $z_{1}$ um den Betrag von $z_{2}$ und dem Winkel von $z_{2}$
In den Polarkoordinaten ist die Multiplikation vereinfacht
$$
z_{1}*z_{2}=[r_{1},\varphi_{1}]*[r_{2},\varphi_{2}] = [r_{1}r_{2},\varphi_{1}+\varphi_{2}]
$$
In diesem Zusammenhang sei auch die #Moivresche_Formel erwähnt.
$$
(\cos\varphi+i\sin\varphi)^n=\cos(n*\varphi)+i\sin(n*\varphi)
$$