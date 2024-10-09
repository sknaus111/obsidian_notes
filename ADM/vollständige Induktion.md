
P(n) sei eine Eigenschaft, welche für eine natürliche Zahl gelten kann.

#P #Eigenschaft #Natürliche_Zahlen 

Es gilt zu untersuchen ob P(n) für jede natürliche Zahl gilt. 

$$
\forall n \in \mathbb{N} :P(n)
$$

Laut der Vorgehensweise des Induktion muss zuerst untersucht werden ob die Eigenschaft P auf die natürliche Zahl 0 zutrifft. Ebenfalls muss überprüft werden ob sich mit der Annahme, dass die Eigenschaft auf eine natürliche Zahl n zutrifft, diese Eigenschaft sich auf den Nachfolger n' übertragen lässt. #Induktion #Induktionsanfang #Induktionsschritt
$$
P(0) 
$$
$$
P(n') = P(n+1)
$$
Die vollständige logische Schreibweise der vollständigen Induktion sieht nun wie folgt aus.

$$
P(0) \land (\forall n \in \mathbb{N} : P(n) \implies P(n+1)) \implies \forall n \in : P(n)
$$
## Beispiele
#Beispiele
### Beispiel 1.1

P(n) sei folgende Aussage

$$
\displaystyle\sum_{k=0}^nk=\frac{n(n+1)}{2}
$$
P(0) in die Gleichung eingesetzt ergibt.
$$
\displaystyle\sum_{k=0}^0k = 0
$$
Da die Summe auf der linken Seite der Gleichung 0 ergibt ist die Gleichung wahr. Da $P(n)$ #Induktionsvoraussetzung wahr ist kann überprüft werden $P(n+1)$ #Induktionsbehauptung ebenfalls wahr ist.

Die Summe von $n+1$ entspricht der Summe aus $n$ mit $n+1$ addiert.
$$
\displaystyle\sum_{k=0}^{n+1}k=\displaystyle\sum_{k=0}^nk+(n+1)
$$
Da die Induktionsvoraussetzung voraussetzt, dass $P(n)$ wahr ist kann die Summe mit dem rechten Teil der Behauptung ausgetauscht werden.
$$
= \frac{n(n+1)}{2}+(n+1)
$$
Jetzt kann aus dem Term $(n+1)$ herausgehoben werden.
$$
=(\frac{n}{2}+1)(n+1)
$$
Multipliziert man nun mit 2 und dividiert durch zwei entsteht folgender Term.
$$
= \frac{2\left( \frac{n}{2}+1\right)(n+1)}{2}
$$
Die 2 lässt sich in die erste Klammer hineinmultiplizieren und löst die halbe unter dem n in der Klammer auf.
$$
= \frac{(n+2)(n+1)}{2}
$$
Vergleicht man das Ergebnis mit der Induktionsbehauptung sieht man, dass dieses übereinstimmt.
$$
\frac{(n+1)((n+1)+1)}{2} = \frac{(n+2)(n+1)}{2}
$$
### Beispiel 1.2
In diesem Beispiel soll demonstriert werden, dass der Induktionsanfang verschiebbar ist. Somit gilt die Eigenschaft für

$$
\forall n \geq n_{0}
$$

$P(n)$ sei folgende Aussage
$$
2^n > n+2
$$
$P(0)$,$P(1)$ und $P(2)$ in die Gleichung eingesetzt ergibt.
$$
2^0 > n+2
$$
$$
2^1>n+2
$$
$$
2^2>n+2
$$
Da keiner dieser Aussagen wahr ist wird der Induktionsanfang auf $P(3)$ verschoben.
$$
2^3>n+2
$$
Da anzunehmen ist, dass die Eigenschaft für alle n größer als 3 gilt wird nun die Induktionsbehauptung überprüft.
$$
2^{n+1} > (n+1) +2
$$
Da eine Erhöhung im Exponenten um 1 einer weiteren Multiplikation von 2 entspricht kann die Gleichung für $P(n)$ dazu umgeformt werden $P(n+1)$ zu entsprechen.
$$
2^{n+1} = 2*n^2 > 2(n+2)
$$
Ebenfalls kann $2(n+2)$ umgeformt werden.
$$
2*n^2>2n+4
$$
Diese Gleichung kann erneut umgeformt werden.
$$
2n+4 = n+3+n+1
$$
$$
2*n^2>n+3+n+1
$$
Da $n+1$ größer als 0 ist kann immer angenommen werden das $n+1$, 1 oder größer ist.
$$
n+1 > 0
$$
So kann die Gleichung so umgeformt werden, dass sie zumindest $n+4$ entspricht.
$$
n + 3 + (n+1) \geq n+4
$$
Da 2^(n+1) größer  oder gleich groß ist wie n+4  
$$
2^{n+1} \geq  n+4
$$
kann man wieder in die ursprüngliche Gleichung der Induktionsbehauptung einsetzen. 
$$
2^{n+1}>(n+1)+2
$$
Da folgende Aussage offensichtlich wahr ist
$$
n+4>(n+1)+2
$$ergibt sich folgende Aussage als wahr.
$$
2^{n+1} \geq n+4>(n+1)+2
$$


Da die vollständige Induktion doch nicht in jedem Sachverhalt anwendbar ist, gibt es die [[Verlaufsinduktion]]