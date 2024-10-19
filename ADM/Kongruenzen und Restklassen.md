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
## Beweis
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
