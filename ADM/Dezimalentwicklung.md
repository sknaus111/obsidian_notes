Eine #Dezimalentwicklung zerteilt eine Zahl in ihre einzelnen Ziffern multipliziert mit einem Exponenten der Basis. Bei #Dezimalzahlen sind dies Exponenten der Zahl 10. So kann die Zahl $327$ auch folgend dargestellt werden.
$$
(327)_{10}=3*10^2+2*10^1+7*10^0
$$
Allgemein werden Zahlen in der Dezimalentwicklung wie folgt dargestellt.
$$
n = c_{k}*10^k+c_{k-1}*10^{k-1}+\dots+c_{1}*10^1+c_{0}*10^0=(c_{k}c_{k-1}\dots c_{1}c_{0})_{10}
$$
Bei negativen Zahlen kann einfach ein Minuszeichen davor gesetzt werden.

Um rationale darzustellen können auch negative Potenzen von 10 verwendet werden. Die Ziffern $c_{-1}, c_{-2}, \dots c_{-m}$ werden auch als Nachkommastellen bezeichnet.

Um nicht rationale Zahlen in einer Dezimalentwicklung darzustellen bedarf es einer #unendlichen_Dezimalentwicklung. Die Schreibweise dieser sieht wie folgt aus.
$$
x = c_{k}*10^k+c_{k-1}*10^{k-1}+\dots+c_{1}*10^1+c_{0}*10^0+\sum_{m=1}^{\infty}c_{-m}*10^{-m}
$$
Zu jeder unendlichen Dezimalentwicklung gehört auch eine #Intervallschachtelung von Intervallen der Form $I_{m} = [x'_{m},x''_{m}]$. In dieser wir die unendliche Dezimalentwicklung nach $m$ Schritten abgebrochen. 

Beispielsweise kann $\sqrt{ 2 }$ als Exempel hervorgezogen werden. 

$$
I_{0} = [1,2],~~ I_{1}=[1.4,1.5],~~I_{2}=[1.41,1.42]
$$
Die Schachtelung entsteht daher, dass die Intervalle ineinander geschachtelt sind. So ist das Intervall $I_{1}$ auch im Intervall $I_{0}$ enthalten oder das Intervall $I_{2}$ im Intervall $I_{1}$ enthalten. Doch Intervallschachtelung funktioniert nicht nur bei irrationalen Zahlen wie $\sqrt{ 2 }$. Auch für die rationalen Fälle wie $\frac{1}{3}$, welche nicht mittels endlicher Dezimalentwicklung dargestellt werden können, ist die Intervallschachtelung von Nutzen.
$$
\frac{1}{3} = 0.333\dots
$$
Sogenannte unendliche Dezimalentwicklungen sind als periodische Dezimalentwicklungen bekannt. Hier wiederholen sich eine oder mehrere Ziffern im Nachkommateil bis ins Unendliche. Unterschieden wird zwischen Perioden, welche zuvor einen nicht periodischen Nachkommaanteil haben, die Vorperioden auch schließlich periodisch genannt, und jenen die dies nicht haben.


## Behauptung
Die Dezimalentwicklung jeder rationalen Zahlen ist periodisch. Sie ist eindeutig, wenn man den Sonderfall der Periode 999... ausschließt.
## Beweis
Fall 1) $x$ hat eine endliche Dezimalentwicklung. Ist dies der Fall so ist $x$ offensichtlich rational.
Fall 2) $x$ hat x jedoch eine (schließlich) periodisch Dezimalentwicklung $$x = (c_{k}c_{k-1}\dots c_{1}c_{0}.c_{-1}\dots c_{-m}p_{1}\dots p_{r}p_{1}\dots p_{r}p_{1}\dots$$
mit Periode
$$
p_{1}\dots p_{r}
$$
so hat $10^rx-x = (10^r-1)x$ eine endliche Dezimalentwicklung. Es fällt zum Fall 1 zurück und $(10^r-1)x$  ist rational. Daraus folgt, dass auch $x$ rational ist.

Wendet man dieses Beispiel im Spezialfall $x = 0.999\dots$ an
$$
x=\frac{10x-x}{9}=\frac{9.999\dots-0.999\dots}{9}=1
$$
So kann jede Zahl mit einer (schließlichen) Periode von $999\dots$ als endliche Dezimalentwicklung dargestellt werden.

Die nächste Beobachtung ist die Tatsache, dass 
$$
x=0.c_{-1}c_{-2}c_{-3}\dots \not = 0.999\dots ~~~~~~~x< 1
$$
So folgt
$$
x\leq 1-10^{-k}<1
$$
x ist also kleiner oder gleich groß als 1 weniger der kleinsten Abweichung.

so sind auch zwei Zahlen $x,y$ mit verschiedener Periode verschieden sind. Ist nun umgekehrt $x=\frac{m}{n}$ eine rationale Zahl, erhält man die Dezimalentwicklung durch den einfachen Divisionsalgorithmus. Di e Reste $r_{i}$ der Division sind immer kleiner als $n$. 
Fall 1) ist der Rest $r_{i} = 0$ so ist die Dezimalentwicklung endlich.
Fall 2) ist dies nicht der Fall muss sich nach $n$ Schritten der Rest wiederholen.
Daher gibt es nun ein $i$ und ein $l>0$ mit $r_{i+l} = r_{i} \geq1$. Der daraus folgende Rest $r_{i+1}$ ist ab dem Zeitpunkt wo nur noch Null übertragen wird, nur von $r_{i}$ und $n$ abhängig. Daher gilt für $i\geq i_{0}$
$$
r_{i+l+1}=r_{i+1}
$$
Die Reste sind periodisch. Daraus folgt, dass die dazugehörige Dezimalentwicklung periodisch ist.
