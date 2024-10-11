Im [[Dezimalsystem]] oder im [[Binärsystem]] können Zahlen mittels ihrer Ziffern und der Exponenten ihrer Basis dargestellt werden. Durch diese einheitliche Darstellung, ist es auch möglich eine Zahl von einem Zahlensystem in ein anderes Zahlensystem umzuwandeln.


## Stellenwert 
Beispielsweise nimmt man die Zahl $1011 0111_{2}$. Diese soll mit Hilfe der Stellenwerte ins Dezimalsystem umgerechnet werden. 

Es wird folgende Formel  eingesetzt.$\sum_{i=0}^{n}a_{i}2^i$

| Binärdarstellung | ($1$     | $0$   | $1$      | $1$      | $0$   | $1$      | $1$      | $1$      | )$_{2}$      |
| ---------------- | -------- | ----- | -------- | -------- | ----- | -------- | -------- | -------- | ------------ |
| Stellenwerte     | $2^7$    | $2^6$ | $2^5$    | $2^4$    | $2^3$ | $2^2$    | $2^1$    | $2^0$    |              |
| Umrechnung       | $1*2^7+$ | $0+$  | $1*2^5+$ | $1*2^4+$ | $0+$  | $1*2^2+$ | $1*2^1+$ | $1*2^0+$ | $(183)_{10}$ |
## Hornerschema
Die zweite Variante eine Zahl von einem Zahlensystem in ein anderes umzuwandeln ist das sogenannte Hornerschema. Dieses ist oft effizienter und beruht auf folgende Aussage. 
$$
(\dots a_{3}a_{2}a_{1}a_{0} = \dots+a_{3}2^3+a_{2}2^2+a_{1}2^1+a_{0}2^0)
$$
$$
= (((\dots+a_{3})*2+a_{2})*2+a_{1})*2+a_{0}
$$
Beispielsweise kann dieses wie folgt angewendet werden.
$$
~~~~~~~~~(1 ~~~~~~~~~~~ 0 ~~~~~~~~~~~~ 1 ~~~~~~~~~~~~~ 1~~~~~~~~~~~ 0 ~~~~~~~~~~~~ 1 ~~~~~~~~~~~~ 1 ~~~~~~~~~~~ 1)_{2}
$$
$$
((((((1*2+0)*2+1)*2+1)*2+0)*2+1)*2+1)*2+1
$$$$
~~~~~~~~~~~~~~~(((((2*2+1)*2+1)*2+0)*2+1)*2+1)*2+1
$$
$$
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~((((5*2+1)*2+0)*2+1)*2+1)*2+1
$$
$$
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~(((11*2+0)*2+1)*2+1)*2+1
$$
$$
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~((22*2+1)*2+1)*2+1
$$
$$
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~(45*2+1)*2+1
$$
$$
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~91*2+1
$$
$$
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~183
$$

Ein anderes Beispiel, in welchem eine Zahl vom Dezimalsystem ins Binärsystem umgerechnet wird.

## Algorithmus von Dezimal auf Binär

Ein einfacher Algorithmus um von einer Dezimalzahl auf eine Binärzahl umzurechnen stellt dieser dar. Gesucht seien die einzelnen Ziffern der Binärzahl $a_{1},a_{2},a_{3},\dots$ und gegeben sei die Dezimalzahl $Z_{10}$. 
Man setzte $Z_{0} \gets Z$
$i \gets 0$

Solange $Z_{i} \not = 0$
	$a_{i} \gets Z_{i} mod 2$
	$Z_{i+1}\gets \frac{Z_{i}-a_{i}}{2}$
	$i \gets i+1$

Beispielsweise mit der Zahl $6_{10}$
$a_{0} = Z_{0} ~mod~ 2 = 0, Z_{i} = \frac{6-0}{2}=3$
$a_{1} = Z_{1}~mod~2=1,Z_{2}=\frac{3-1}{2}=1$
$a_{2}=Z_{2}~mod~2=1,Z_{3}=\frac{1-1}{2}=0$
Aus den Resten von unten nach oben die Binärzahl bilden. $6_{10} = 110_{2}$

Doch wie sieht das ganze mit [[Zahlen mit Nachkomma]] aus oder [[Zahlensysteme Allgemein]]?