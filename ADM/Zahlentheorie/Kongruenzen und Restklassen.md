## Definition
Es sei eine positive ganze Zahl $m$, der so genannte #Modulo, ausgezeichnet. Zwei Zahlen $a,b \in \mathbb{Z}$ heißen kongruent modulo $m$, falls $m$ ein Teiler von $b-a$ ist. Man schreibt dafür auch $a \equiv b \text{ mod } m$. Unter einer #Restklasse $\overline{a}$ modulo $m$ versteht man die Menge
$$
\overline{a} = a+m*\mathbb{Z}=\{\dots,a-2m,a-m,a,a+m,a+2m\}
$$
$$
= \{b\in\mathbb{Z} \mid a \equiv b \text{ mod } m\}
$$
Die Menge aller Restklassen modulo $m$ wird mit $\mathbb{Z}_{m}$ bezeichnet.

Wenn $a \equiv b \text{ mod }m$ gilt, dann gilt auch $\overline{a}=\overline{b}$

In einer Restklasse werden jene Zahlen zusammengefasst, welche bei der Division durch $m$ den gleichen Rest $r$ haben. Beispielsweise für $m=2$, dann besteht $\overline{0}=2\mathbb{Z}$ aus den gerade Zahlen und $\overline{1}=2\mathbb{Z}$ aus den ungerade Zahlen

## Satz 
Für jede positive natürliche Zahl $m$, gibt es genau $m$ Restklassen
$$
\mathbb{Z}_{m} = \{\overline{0},\overline{1},\dots,\overline{m-1}\}
$$
### Beweis
Dividiert man eine ganze Zahl $n$ durch $m$, so gilt $n=mq+r$ mit $0\leq r<m$.
Also ist $n \equiv r \text{ mod }m$ und demnach $n \in \overline{r}$
Es seien zwei Kongruenzklassen $\overline{a},\overline{b}$ mit $0\leq a<b<m$. Angenommen $\overline{a}$ und $\overline{b}$ hätte eine Zahl $n$ gemeinsam. So würde gelten, dass $m \mid (n-a)$ und $m \mid (n-b)$. Daraus würde aber schließen, dass $m \mid (b-a)$ gilt. Da dies aber unmöglich ist gibt es genau $m$ Restklassen, welche durch $\overline{0},\overline{1},\dots,\overline{m-1}$ repräsentiert werden.

Auch ist es möglich mit Kongruenzen und Restklassen zu rechnen. Man nehme an
$$
a \equiv c \text{ mod }m ~~~~~\text{ und }~~~~~ b \equiv d \text{ mod }m
$$
Man hat also $c=a+q_{1}m$ und $d = b+q_{2}m$ für gewisse $q_{1},q_{2}$. Daraus folgt $c\pm d=a\pm b+(q_{1}\pm q_{2})m$ und $cd = ab + (q_{1}b+q_{2}a+q_{1}q_{2}m)m$ bzw.
$$
a\pm b=c\pm d ~~~~~\text{ und }~~~~~a*b=c*d \text{ mod }m
$$
## Beispiel
Für $m=9$ gilt $10 \equiv 1 \text{ mod }9$ und daher auch $10^j\equiv_{1} \text{ mod }9$ für alle $j\geq1$. Daher gilt auch für jede natürliche Zahl $n$ in ihrer Dezimalentwicklung.
$$
n = c_{0}+10c_{1}+\dots+10^kc_{k}\equiv c_{0}+c_{1}+\dots+c_{k} \text{ mod }9
$$Dies bedeutet die Summe der Ziffern von $n$ ist zu $n$ kongruent modulo 9. So ist $n$ durch 9 teilbar, wenn die Ziffernsumme von $n$ durch 9 teilbar ist.
Formuliert man die obige Überlegung für Kongruenzklassen um, so erhält man folgendes
$$
\overline{a}=\overline{c}, \overline{b}=\overline{d} \implies \overline{a\pm b} = \overline{c\pm d},\overline{a*b}=\overline{c*d}
$$
Dies rechtfertigt folgende Definition.
## Definition
Für Restklassen $\overline{a},\overline{b} \in \mathbb{Z}$ definiert man Summe und Produkt durch
$$
\overline{a}+\overline{b}=\overline{a+b}, ~~~~~\text{ und }~~~~~\overline{a}*\overline{b}=\overline{a*b}
$$
## Beispiel
Für $m = 3$ besteht $\mathbb{Z_{3}} = \{\overline{0},\overline{1},\overline{2}\}$ aus 3 Elementen. Die Rechenoperationen für diese sind wie folgt definiert mit Hilfe der Rechenregeln $\overline{a} + \overline{b} = \overline{a+b}$

| +              | $\overline{0}$ | $\overline{1}$ | $\overline{2}$ |
| -------------- | -------------- | -------------- | -------------- |
| $\overline{0}$ | $\overline{0}$ | $\overline{1}$ | $\overline{2}$ |
| $\overline{1}$ | $\overline{1}$ | $\overline{2}$ | $\overline{0}$ |
| $\overline{2}$ | $\overline{2}$ | $\overline{0}$ | $\overline{1}$ |

| *              | $\overline{0}$ | $\overline{1}$ | $\overline{2}$ |
| -------------- | -------------- | -------------- | -------------- |
| $\overline{0}$ | $\overline{0}$ | $\overline{0}$ | $\overline{0}$ |
| $\overline{1}$ | $\overline{0}$ | $\overline{1}$ | $\overline{2}$ |
| $\overline{2}$ | $\overline{0}$ | $\overline{2}$ | $\overline{1}$ |
Für jede Restklasse $\overline{a}$ gibt es auch eine negative Restklasse $-\overline{a}=\overline{-a}$

Nun wollen wir untersuchen welche Restklassen eine **multiplikativ inverse Restklasse** besitzen. Also eine Restklasse $\overline{b}$ invers von der Restklasse $\overline{a}$, welche $\overline{a}*\overline{b} = 1$. Im vorherigen Beispiel besitzen die Restklassen $\overline{1}$ und $\overline{2}$  inverse Restklassen $\overline{1}^{-1}$ und $\overline{2}^{-1}$.

## Satz
Eine Restklasse $\overline{a} \in \mathbb{Z}$ besitzt genau dann eine multiplikativ inverse Restklasse, wenn $\text{ggT}(a,m) = 1$ ist.

## Beweis
Für eine Restklasse $\overline{a}$ und ihre inverse Restklasse $\overline{b}$ gilt $a*b=1+q*m$. Also gilt auch $1=a*b-q*m$. Jeder gemeinsame Teiler von $a$ und $m$ teilt daher auch $1$. Somit ist $\text{ggT}(a,m)=1$
Umgekehrt der $\text{ggT}(a,m)=1$ so gibt eine inverse Restklasse $\overline{b}$.

## Beispiel
Man sucht die inverse Restklasse von $\overline{15}$ modulo $17$. Da $\text{ggT}(15,17) = 1$ kann man mit Hilfe des Euklidischen Algorithmus die ganzen Zahlen $8$ und $-7$ finden.
$$
1=8*15-7*17
$$
Daraus ist abzulesen, dass die inverse Restklasse von $\overline{15}^{-1} = \overline{8}$ ist.

Division von Kongruenzen ist möglich wenn Divisor und Modul teilerfremd sind.
$$
a*c=b*c \text{ mod }m, \text{ ggT}(c,m)=1 \implies a \equiv b \text{ mod }m
$$Für ein Primzahlmodul m alle Restklassen $\overline{a}\not=0$ invertierbar sind.

Eine Anwendung für dieses mathematische Konzept gibt es als Prüfziffern wie bei den **ISBN** von Büchern. dieser ist wie folgt aufgebaut
$$
10a_{^1}+9a_{2}+8a_{3}+7a_{4}+6a_{5}+5a_{6}+4a_{7}+3a_{8}+2a_{9}+p \equiv 0 \text{ mod }11
$$
So gilt folgende Formel für die Prüfziffer $p \equiv a_{1}+2a_{2}+\dots+9a_{9} \text{ mod }11$ und $p \in \{0,1,2,\dots,10\}$

## Fehlererkennung
Jeder Fehler in einer Ziffer sowie alle Vertauschungen zweier Ziffern werden vom ISBN-Code erkannt.

## Eulersche $\varphi$-Funktion 
#Eulersche_Funktion $\varphi(m)$ gibt die Anzahl der invertierbaren Restklassen modulo $m$ an:
$$
\varphi(m)=|\{a\in\mathbb{Z}|1\leq a\leq m,\text{ggT}(a,m)=1\}|
$$
Beispielsweise ist die Eulersche $\varphi$-Funktion $\varphi(6)=2$. Die Eulersche $\varphi$-Funktion kann mit Hilfe einer einfachen Formel berechnet werden.

## Satz
Es sei $m=p_{1}^{e_{1}}\dots p_{r}^{e_{r}}$ die Primfaktorzerlegung von $m$ (wobei die $p_{j} \in \mathbb{P}$ paarweise verschieden sind und $e_{j}>0$) gilt
$$
\varphi(m)=m*1\left(1- \frac{1}{p_{1}}\right)*\dots*\left( 1- \frac{1}{p_{r}}\right)
$$
Für eine Primzahlpotenz $p^k$ ist diese Formel einsichtig, denn
$$
\varphi(p_{k})=p^k-p^{k-1}=p^{k-1}*(p-1)=p^k*\left( 1- \frac{1}{p} \right)
$$
Eine wichtiger Anwendungsfall für diese Funktion ist folgender Sachverhalt.
## Kleiner Satz von Fermat
Für teilerfremde ganze Zahlen $a,m$ gilt
$$
a^{\varphi(m)}\equiv1\text{ mod }m
$$
### Beweis
Ist $m=p$ eine Primzahl so vereinfacht sich das zu
$$
p \nmid a \implies a^{p-1}\equiv_{1} \text{ mod }p \text{ bzw. }p \mid(a^{p-1}-1)
$$Eine erste Zahlentheoretische Anwendung ist auch das [[RSA-Verfahren]]