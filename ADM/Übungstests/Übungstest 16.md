## Frage 1 (8 Punkte)
Wie viele siebenrelementige Teilmengen von $\{1,2,3,4,5,6,7,8,9, 10\}$ enthalten genau vier ungerade Zahlen?
Der Lösungsweg muss verbal beschrieben und begründet werden, sodass Ihre Lösung nachvollziehbar ist.

$$
\binom{5}{4}\binom{5}{3}
$$
## Frage 2 (9 Punkte)
Erklären Sie das Verfahren der vollständigen Induktion anhand eines Beweises der folgenden Behauptung:

Für alle positiven natürlichen Zahlen $n$ gilt

$$
\sum_{k=1}^{n} \frac{1}{k^{2}(k+1)} <  1- \frac{1}{2n^{2}}
$$

Alle Schritte des Beweises müssen genau erklärt werden (verbal!) und die Präsentation muss der Logik des Beweises Rechnung tragen. Insbesondere darf eine zu beweisende Behauptung nicht am Anfang des Beweises stehen, sondern muss sich als dessen letzte Schlussfolgerung ergeben.

#Induktionsvoraussetzung
$$
\sum_{k=1}^{n} \frac{1}{k^{2}(k+1)} \leq  1- \frac{1}{2n^{2}}
$$
#Induktionsanfang
$$
\frac{1}{1(1+1)} \leq 1- \frac{1}{2*1}
$$
$$
\frac{1}{2} < 1= - \frac{1}{2}
$$
#Induktionsbehauptung
$$
\sum_{k=1}^{n+1} \frac{1}{k^{2}(k+1)} \leq  1- \frac{1}{2(n+1)^{2}}
$$
$$
\leq 1- \frac{1}{2n^{2}+4n+2}
$$
#Induktionsschritt
$$
\leq 1-\frac{1}{2n^{2}} + \frac{1}{(n+1)^{2}((n+1)+1)}
$$
$$
\leq 1- \left( \frac{1}{2n^{2}} - \frac{1}{(n^{2}+2n+1)(n+2)}\right)
$$
$$
\leq 1- \left(\frac{1}{2n^{2}} - \frac{1}{n^{3}+ 2n^{2}+2n^{2}+4n+n+2}\right)
$$
$$
\leq 1- \left(\frac{1}{2n^{2}}- \right)
$$
## Frage 3 (8 Punkte)
Bestimmen Sie alle ganzen Zahlen $x$, die folgende Kongruenz erfüllen:

$$362x = 4 \mod 398.$$
$$
ggT(362,398) = ?
$$
$$
398 = 362 * 1 + 36
$$
$$
362 = 36 * 10 + 2
$$
$$
36 = 2*18 +0
$$
$$
ggT=2
$$
$$
181x \equiv 2 \mod 199
$$
$$
2 = 362 - 36 * 10
$$
$$
2 = 362 - (398-362*1)*10
$$
$$
2 = 362*11 - 398 *10
$$
$$
181x *11\equiv 2 * 11 \mod 199 
$$
$$
x \equiv 22 \mod 199
$$
$$
x = 22 + p* 199 
$$
## Frage 4 (2 Punkte)
Was versteht man unter dem kartesischen Produkt zweier Mengen M und N?
Geben Sie zwei Elemente des kartesischen Produkts von M und N an, wenn
$M = \{1,2,3\}$ und $N = \{a, b, c, d, e\}$.

$$
M\times N = \{ \dots, (1,a) ,(1,b),\dots \}
$$
### Frage 5 (3 Punkte)
Bestimmen Sie die Polarkoordinatendarstellung aller komplexen Zahlen $z$ mit

$$
z^{4}=-16i
$$

$$
z_{0}=\left[ 2, \frac{−π}{8}​ \right],$$
$$z_{1}=\left[ 2, \frac{3π}{8} \right]$$$$z_{2}=\left[ 2, \frac{7\pi}{8} \right],
$$$$z_{3}=\left[ 2, \frac{11\pi}{8} \right]
$$
