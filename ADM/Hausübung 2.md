
## 29) 
Zeigen Sie, dass $\sqrt{ 30 }$ irrational ist.

Man nehme an für $\sqrt{ 30 }$ gäbe es zwei Zahlen $a,b \in \mathbb{Z}$ für welche $\sqrt{ 30 } =\frac{a}{b} \in\mathbb{Q}, b>0, ggT(a,b)=1$ 
$30=\frac{a^2}{b^2} \implies 30*b^2=a^2$
$a=30*k$
$30*b^2=(30*k)^2$
$30*b^2=900*k^2$
$b^2=30*k^2$
Würde bedeuten, dass a und b durch 30 teilbar sind. Somit ist der Annahme widersprochen, dass $a$ und $b$ teilerfremd sind und es kommt zu einem Widerspruch.

## 35) 
Man bestimme rechnerisch (ohne Taschenrechner) und graphisch Summe und Produkt der
komplexen Zahlen $z_{1} = 5 + 2i \text{ und } z_{2} = \left[ 3, \frac{\pi}{2}  \right]$

$z_{2} = \Re+i*\Im$
$\Re = \cos\left( \frac{\pi}{2} \right)3=0*3=0$
$\Im=\sin\left( \frac{\pi}{2} \right)*3=1*3=3$
$z_{2}=0+3i=3i$

$z_{3}=z_{1}+z_{2}=5+0+3i+2i=5+5i$

$z_{4}=z_{1}*z_{2}=(0*5-3*2)+(5*3+2*0)i=-6+15i$

Zum graphischen Darstellen kann bei der Summe ein Parallelogramm gezeichnet werden.
Zum Multiplizieren würde man die komplexe Zahl $z_{1}$ um 3 erweitern. Dann diese von Ursprung aus um einen viertel Kreisdrehung gegen den Uhrzeigersinn verschieben.
## 48) 
Welche Teilmenge der komplexen Zahlenebene beschreibt die angegebene Ungleichung?

$$|\frac{z+4}{z-4}|<3$$
Anders kann der Bruch von dem Betrag komplexer Zahlen wie folgt geschrieben werden.
$$
\frac{\sqrt{ (a^2+4)+b^2 }}{\sqrt{ (a^2-4) +b^2}} <3
$$
Dass kann mit dem Nenner multipliziert werden
$$
\sqrt{ (a+4)^2+b^2 } <3\sqrt{ (a-4)^2 +b^2}
$$
$$
(a+4)^2+b^2  <9 ((a-4)^2 +b^2)
$$
$$
(a+4)^2+b^2  -9 ((a-4)^2 +b^2)<0
$$
$$
a^2+8a+16+b^2-9(a^2-8a+16+b^2)<0
$$
$$
a^2+8a+16+b^2-9a^2+72a-144-9b^2<0
$$
$$
-8a^2-8b^2+80a-128<0
$$

## 58) 
Man bestimme zwei ganze Zahlen $x, y$, welche die Gleichung $451x + 176y = 11$ erfüllen

$451x+176=11$
$41x+16=1$

Man wende den Euklidischen Algorithmus an.
$$
41 = 16*2+9
$$
$$16=9*1+7$$
$$
9=7*1+2
$$
$$
7=2*3+1
$$
$$
2=1*2+0
$$
In andere Richtung
$$
1=7-2*3
$$
$$
=7-(9-7*1)*3
$$
$$
=4*7-3*9
$$
$$
4*(16-9*1)-3*9
$$
$$
4*16-7*9
$$
$$
4*16-7*(41-16*2)
$$
$$
18*16-7*41
$$
$$x=-7, y=18$$
$$
-7*451+18*176=11
$$
