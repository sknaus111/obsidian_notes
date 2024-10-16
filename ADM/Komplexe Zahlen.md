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



## Polarkoordinaten
Um komplexe Zahlen auf der #Zahlengerade darzustellen muss diese mit dem hinzufügen einer y-Achse zur #Gaußschen_Ebene erweitert werden. In dieser werden komplexe Zahlen als #Zeiger dargestellt. Dieser Zeiger startet vom Ursprung bis zu den Koordinaten der komplexen Zahl. Als x Koordinate dient der Realteil und als y Koordinate der Imaginärteil. Die Länge des Zeigers wird auch als Betrag bezeichnet.

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


## Rechnen mit komplexen Zahlen

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
zum Nachweis dieser betrachtet man einfach beide Seiten in Polarkoordinaten.

So wie bereits gewohnt gelten die sonstigen #Gesetze zum Rechnen mit Zahlen. Auch die komplexe #negative_Zahl $-z$ ist durch $-z = -a -ib$ gegeben. Genau wie der #Kehrwert $\frac{1}{z}$von $z$ $$\frac{1}{z}=\frac{a}{a^2+b^2}-i \frac{b}{a^2+b^2}$$ Noch einfacher lässt sich dieser mit der #konjugiert_komplexen_Zahl $\bar{z}$ schreiben. Diese ist folgend definiert.
$$
\bar{z}=a-ib
$$
So lässt sich der Kehrwert auch einfacher schreiben.
$$
\frac{1}{z}=\frac{\bar{z}}{z*\bar{z}}=\frac{\bar{z}}{|z|^2}
$$
So kommen folgende neuen Rechenregeln für konjugiert komplexen Zahlen vor.
$$
\overline{z_{1}+z_{2}}=\overline{z_{1}}+\overline{z_{2}}
$$
$$
\overline{z_{1}*z_{2}}=\overline{z_{1}}*\overline{z_{2}}
$$
$$
|z| = \sqrt{ z * \overline{z} }
$$
$$
\Re(z) = \frac{z + \overline{z}}{2}
$$
$$
\Im(z)=\frac{z-\overline{z}}{2i}
$$
Eine Erkenntnis aus diesen Regeln ist die Tatsache, dass $z * \overline{z}=|z|^2$ immer eine reelle Zahl $\geq 0$ ist. 

Bei der Division zwei komplexer Zahlen lässt sich der Bruch $\frac{z_{1}}{z_{2}}$ mit $\overline{z_{2}}$ erweitern. So wird der Nenner zu einer reellen Zahl.
$$
\frac{z_{1}}{z_{2}}=\frac{z_{1}*\overline{z_{2}}}{z_{2}*\overline{z_{2}}}=\frac{1}{z_{2}*\overline{z_{2}}}*(z_{1}*\overline{z_{2}})
$$
In Polarkoordinaten würde man die Division wie folgt anschreiben
$$
\frac{|z_{1}|}{|z_{2}|}=\frac{|z_{1}|}{|z_{2}|}
$$
und
$$
arg\left( \frac{z_{1}}{z_{2}} \right) = arg(z_{1})-arg(z_{2}) \text{ mod }2\pi
$$
### Beispiel
$$
\frac{2+3i}{1-2i}=\frac{(2+3i)(1+2i)}{(1-2i)(1+2i)}=\frac{1}{5}(-4+7i)=-\frac{4}{5}+\frac{7}{5}i
$$

## Wurzeln von komplexen Zahlen
Nun kommt man zur ursprünglichen Motivation für die Einführung komplexer Zahlen zurück. Das Lösen quadratischer und deren ähnlicher Gleichungen. Man nehme $w$ als komplexe Wurzel von $z$.
$$w = [\sqrt{ R },\left( \frac{\varphi}{2} \right)]$$
$$
w^2=z
$$
Dies gilt jedoch auch für die negative komplexe zahl $w'$
$$
w'^2 = z
$$
Allgemein sucht man die n-te Wurzel einer komplexen Zahl $\sqrt[^n]{ z },~~z\in\mathbb{C}$ bzw.  sucht man $w$ mit $w^n=z$. In Polarkoordinaten kann diese Relation wie folgt dargestellt werden.
$$
w_{j}=\left[ \sqrt[^n]{ R },\left( \frac{\varphi}{n} \right)+\frac{2\pi j}{n} \right],~~~j\in\{0,1,\dots,n-1\}
$$
Dies sind alle Lösungen, da es nicht mehr als n Lösungen der Gleichung $w^n=z$ geben kann.
### Beispiel
5-ten Wurzeln der Zahl $z=1+i=\left[ \sqrt{ 2 }, \frac{\pi}{4} \right] =\left[ \sqrt[^2]{ 2 }, \frac{\pi}{4} \right]$
$$
w_{0}=\left[ \sqrt[^{10}]{ 2 }, \frac{\pi}{20} \right]
$$
$$
w_{1}=\left[ \sqrt[^{10}]{ 2 }, \frac{\pi}{20} + \frac{2\pi}{5} \right]
$$
$$
w_{2}=\left[ \sqrt[^{10}]{ 2 }, \frac{\pi}{20} + \frac{4\pi}{5} \right]
$$
$$
w_{3}=\left[ \sqrt[^{10}]{ 2 }, \frac{\pi}{20} + \frac{6\pi}{5} \right]
$$
$$
w_{4}=\left[ \sqrt[^{10}]{ 2 }, \frac{\pi}{20} + \frac{8\pi}{5} \right]
$$


Die Wurzeln von 1 sind auch als #Einheitswurzeln bekannt. Die komplexe Zahl
$$
\Im = \left[ 1,\frac{2\pi}{n} \right] = \cos\left( \frac{2\pi}{n} \right) + i \sin\left( \frac{2\pi}{n} \right)
$$
wird #primitive_n-te_Einheitswurzel genannt. Für sie gilt
$$
\zeta^n_{n} = 1
$$
alle anderen $n$-ten Einheitswurzeln sind Potenzen von $\zeta_{n}$
$$
\zeta^j_{n}=\left[1, \frac{2\pi j}{n} \right], ~~~j\in\{0,1,\dots,n-1\} 
$$
Beispielsweise sind $\{1,-1\}$ die zweiten Einheitswurzeln, $\left\{ 1, \frac{1}{2}+i\frac{\sqrt{ 3 }}{2} , -\frac{1}{2}-i\frac{\sqrt{ 3 }}{2}\right\}$ die dritten Einheitswurzeln und $1,-1,i,-i$ die vierten Einheitswurzeln.

Man betrachte eine allgemeine #quadratische_Gleichung
$$
z^2+pz+q=0
$$
mit den komplexen Koeffizienten $p,q \in \mathbb{C}$. Wie in den reellen Zahlen hat diese Gleichung zwei Lösungen.
$$
z_{1,2} = -\frac{p}{2}\pm \sqrt{ \frac{p^2}{4}-q }
$$
Nur dann, wenn die Diskriminante $D = p^2-4q = 0$ ist, fallen beide Lösungen auf den gleichen Wert. Auf jeden Fall zerfällt die Gleichung in zwei Linearfaktoren entstehend aus den Lösungen.
$$
z^2+pz+q=(z-z_{1})(z-z_{2})
$$
Vergleicht man die Koeffizienten der Potenzen erhält man den #Vietaschen_Wurzelsatz
$$
p=-(z_{1}+z_{2}) \text{ und } q=z_{1}z_{2}
$$
Also sind quadratische Gleichungen immer explizit lösbar.

### Beispiel
$z^2+2z+2=0$ hat folgende Lösungen 
$$
z_{1,2} = - 1 \pm \sqrt{ 1-2 } = -1\pm \sqrt{ -1 }=-1\pm i
$$
es gilt
$$
z^2+2z+2=(z+1-i)(z+1+i)
$$

Auch allgemeine algebraische Gleichungen können betrachtet werden, auch wenn es bei diesen meist keine expliziten Lösungen gibt.

#Fundamentalsatz_der_Algebra Es sein $a_{0},a_{1},\dots,a_{n}$ komplexe Zahlen $a_{n}\not=0$
$$
p(z)=a_{n}z^n+a_{n-1}z^{n-1}+\dots+a_{1}z+a_{0}
$$
In Linearfaktorschreibweise
$$
a_{n}z^n+\dots+a_{0}=a_{n}(z-z_{1})(z-z_{2})\dots(z-z_{n}) 
$$
Also hat das Polynom $p(z)$ die Nullstellen $z_{1}$ bis $z_{n}$, für welche der Wert der Gleichung gleich 0 ist $p(z)=0$

Für Polynome dritten und vierten Grades gibt es noch Lösungsformeln für dessen Nullstellen. Bei einem $n\geq5$ gibt es keine allgemeinen algebraischen Lösungsformeln mehr. Daher kann man die Nullstellen nur approximieren.