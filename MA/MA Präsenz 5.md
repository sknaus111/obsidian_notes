## Aufgabe 1. 
Der Betrag einer reellen Zahl $x ∈ \mathbb{R}$ ist definiert als
$$|x| = \Bigg \{\begin{array}{c}~~~ x~~~ \text{ falls } x\geq0 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~\\-x ~~~\text{ falls } x<0 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~\end{array}$$
Zeigen Sie mittels einer Fallunterscheidung dass für alle $x, y ∈ \mathbb{R}, y \not= 0$ gilt:
$$
\left| \frac{x}{y}  \right| = \frac{|x|}{|y|}
$$

$(A \lor B) \implies C \iff A\implies C \land B\implies C$

$(A \lor B \lor C \lor D) \implies E \iff A \implies E \land B \implies E \land C \implies E \land D \implies E$
	$A (x \geq 0, y>0): |\frac{x}{y}| = \frac{x}{y} = \frac{|x|}{|y|}$
	$B(x,y < 0): |\frac{x}{y}| = \frac{x}{y} = \frac{|x|}{|y|}$
	$C(x\geq 0, y<0) \frac{|x|}{|y|}=\frac{x}{-y}=|\frac{x}{y} |=-\frac{x}{y}$
	$D(x<0,y) \frac{|x|}{|y|}=\frac{-x}{y} = | \frac{x}{y}| = -\frac{x}{y}$
## Aufgabe 2. 
Beweisen Sie die folgende Aussage durch Kontraposition: Für alle $m, n ∈ \mathbb{Z}$ gilt: falls
$m · n$ ungerade ist, dann sind sowohl $m$ als auch $n$ ungerade.

$A \implies B \iff \lnot B \implies \lnot A$
$m*n=2*i+1 \implies (k*2+1)*(l*2+1)$
$2*k =m\implies m*n=2*k*n \lor 2*l=n \implies m*n=2*l*m$

Falls $m,n$ gerade ist $m*n$ gerade
$m=2*k$
$2*k*n$ gerade
## Aufgabe 3. 
Ein magisches Quadrat ist ein Quadrat mit $n × n$ Feldern die jeweils eine natürliche
Zahl enthalten so dass jede Zeile, jede Spalte und die beiden Diagonalen die selbe Summe ergeben. Für $n = 3$ handelt es sich also um eine Konfiguration der Form

| $a_{1,1}$ | $a_{1,2}$ | $a_{1,3}$ |
| --------- | --------- | --------- |
| $a_{2,1}$ | $a_{2,2}$ | $a_{2,3}$ |
| $a_{3,1}$ | $a_{3,2}$ | $a_{3,3}$ |
 
so dass ein $m$ existiert mit
$$a_{i,1} + a_{i,2} + a_{i,3} = m \text{ für } i = 1, 2, 3$$
$$a_{1,j} + a_{2,j} + a_{3,j} = m \text{ für } j = 1, 2, 3$$
$$a_{1,1} + a_{2,2} + a_{3,3} = m$$
$$a_{1,3} + a_{2,2} + a_{3,1} = m$$
Ein Beispiel für ein magisches Quadrat mit $n = 3$ und $m = 15$ ist:

| 8   | 1   | 6   |
| --- | --- | --- |
| 3   | 5   | 7   |
| 4   | 9   | 2   |
Zeigen Sie dass das folgende Quadrat nicht zu einem magischen Quadrat ergänzt werden kann.

| 8   |     | 2   |
| --- | --- | --- |
| 3   | 6   |     |
|     | 4   |     |

Welche Beweistechnik verwenden Sie dazu?

indirekten Beweis

$8 + a_{1,2} + 2 = m$
$3 + 6 + a_{2,3} = m$
$a_{1,2} + 6 + 4 = m$
$a_{3,1} + 8 + 3 = m$
$a_{3,1}+4+a_{3,3}=m$
$2 + a_{2,3}+a_{3,3}=m$
$8+4+a_{3,3}=m$
$2+6+a_{3,1}=m$

$8+3+a_{3,1}=2+6+a_{3,1}$
$11=8$ Widerspruch