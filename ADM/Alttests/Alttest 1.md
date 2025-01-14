![[Pasted image 20250113110536.png]]

Gleiche Form zu $Z_{2}$ herz = 1, raute = 0

damit ein Ring und ein Körper

![[Pasted image 20250113111037.png]]

$$
p\equiv 9a_{1}+7a_{2}+9a_{3}+7a_{4}+\dots+7a_{12} \mod 10
$$
Im europäischen Artikelnummernsystem EAN werden Zahlen mit 13 Dezimalziffern der Form a1 a2 . . . a12 p verwendet. Dabei wird die letzte der 13 Ziffern, das ist die Prüfziffer p, im EAN-Code so bestimmt, dass a1 + 3a2 + a3 + 3a4 + · · · + a11 + 3a12 + p ≡ 0 mod 10 gilt.

Zeigen Sie, dass beim EAN-Code ein Fehler in einer einzelnen Ziffer stets erkannt
wird, während eine Vertauschung von zwei benachbarten Ziffern genau dann nicht
erkannt wird, wenn die beiden Ziffern gleich sind oder sich um 5 unterscheiden.

Sei eine beliebig Ziffer $a_{k}$ durch eine andere Ziffer vertauscht $a_{k}'$ so wird die Differenz zwischen den beiden entweder mit 1 oder mit 3 multipliziert. Im ersten Fall sind alle möglichen Ziffer $\pm1\dots 9$ womit mod 10 es ungleich 0 ist und ein Fehler erkannt wird. Im zweiten Fall wird die Differenz mit drei multipliziert. $\pm 3,6,9,2,5,8,1,4,7$ und somit wieder ungleich 0 und der Fehler wird erkannt.

Bei einer Vertauschung werden zwei Ziffern $a_{k}$ und $a_{k+1}$ vertauscht. Anstatt $a_{k}+3a_{k+1}$ steht nun $a_{k+1}+3a_{k}$ oder umgekehrt. In anderen Worten ändert sich der Wert des Ganzen um $\pm 2a_{k}\pm 2a_{k+1}$. Im Fall das beiden Ziffern gleich sind ist diese Veränderung trivialerweise 0. Im Fall dass sie sich um 5 unterscheiden ist. $+(2a_{k})-(2(a_{k}\pm5))$ $\iff +2a_{k}-2a_{k}\pm10 \mod 10$ . Wodurch sich die 10 durch das modulo 10 wieder aufhebt.

![[Pasted image 20250113135656.png]]

![[Pasted image 20250113140006.png]]

#Induktionsvoraussetzung
$$
\frac{1}{n+1}\cdot \sum_{i=1}^{n}\left( \frac{1}{n} +i^{2}\cdot((i-1)!)\right)=n!
$$
#Induktionsanfang
$$
\frac{1}{2}\cdot \left(\frac{1}{1}+1^{2}\cdot((1-1)!)\right)=1
$$
$$
\frac{1}{2} \cdot 2 = 1
$$

#Induktionsbehauptung
$$
\frac{1}{n+2} \cdot \sum_{i=1}^{n+1}\left( \frac{1}{n+1} +i^{2} \cdot ((i-1)!)\right)=(n+1)!
$$
#Induktionsschritt
$$
\frac{1}{n+2} \cdot \sum_{i=1}^{n+1}\left( \frac{1}{n+1} +i^{2} \cdot ((i-1)!)\right)=\frac{1}{n+1}\cdot \sum_{i=1}^{n}\left( \frac{1}{n} +i^{2}\cdot((i-1)!)\right)\cdot \frac{n+1}{n+2} + \frac{1}{n+2}\cdot( \frac{1}{n+2}+(n+1)^{2}\cdot((n)!))
$$
$$
n!\cdot\frac{(n+1)}{n+2} + \frac{1}{n+2}\cdot\left( \frac{1}{n+2}+(n+1)^{2}\cdot n! \right)
$$
$$
\frac{(n+1)!}{n+2}+\frac{1}{n+2}\cdot\left( \frac{1}{n+2}+n^{2}\cdot n!+2n\cdot n!+n! \right)
$$
$$
\dots \left(\frac{1+(n+1)^{2}(2n)(n!)}{n+2}\right)
$$
$$

$$
Erläutern Sie das Verfahren der vollständigen Induktion anhand eines Beweises
der folgenden Behauptung:

$$
\frac{1}{n+1}\cdot \sum_{i=1}^{n}\left( \frac{1}{n} +i^{2}\cdot((i-1)!)\right)=n!
$$

für alle $n ∈ \mathbb{N}^{+}$.

Anmerkung: Alle Schritte des Beweises müssen genau angegeben werden und die
Präsentation des Beweises muss der Beweislogik Rechnung tragen. Insbesondere
darf eine zu beweisende Behauptung nicht am Anfang des Beweises stehen, sondern
muss sich als dessen letzte Schlussfolgerung ergeben.