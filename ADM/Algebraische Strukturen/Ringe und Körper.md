Aufgrund von Konvention, werden im folgenden Kapitel für binäre Operationen $+$ und $\cdot$ verwendet. Die neutralen Elemente sind somit $0$ und $1$. Das additive inverse ist $-a$ und das multiplikative inverse ist $a^{-1}$.

Eine algebraische Struktur $(R,+,\cdot)$ mit zwei binären Operationen heißt #Ring, wenn die folgenden drei Eigenschaften erfüllt sind. 

- (i) $(R,+)$ ist eine kommutative Gruppe (mit neutralem Element $0$)
- (ii) $(R, \cdot)$ ist eine Halbgruppe, und
- (iii) es gelten die #Distributivgesetze $$
a \cdot (b+c)=a\cdot b+a\cdot c
$$$$
(a+b)\cdot c=a\cdot c+b\cdot c \text{ für alle }a,b,c\in R
$$
Besitzt $R$ bezüglich $\cdot$ ein neutrales Element, so nennt man $R$ Ring mit #Einselement, und ist $R$ bezüglich $\cdot$ kommutativ, so nennt man $R$ #kommutativen_Ring. 

## Beispiel
$(\mathbb{Z},+,\cdot)$ und $(\mathbb{Z},+,\cdot)$ $m\geq 1$ sind kommutative Ringe mit Einselement. (Die Rechenoperationen $+$ und $\cdot$ in $\mathbb{Z}_{m}$ wurden bereits definiert: $\overline{a}+\overline{b}=\overline{a+b}$ und $\overline{a}\cdot\overline{b}=\overline{a\cdot b}$)

Die Menge aller $n \times n$-Matrizen $A=(a_{ij})_{1\leq i,j\leq n}$ mit Eintragungen $a_{ij}$ aus einem Ring $R$ bildet mit der Matrizenaddition und Matrizenmultiplikation wieder einen Ring

## Polynome
#Polynome in der Unbestimmten $x$ über einen Ring $R$ sind formale Summen der Form $p(x)=a_{0}+a_{1}x+a_{2}x^{2}+\dots+a_{k}x^{k}$ mit #Koeffizienten $a_{0},a_{1},\dots,a_{k} \in R$. Die Menge aller dieser Polynome wird mit $R[x]$ bezeichnet. Aus notationstechnischen Gründen schreibt man Polynome oft auch als (formal) unendliche Summen $p(x)=\sum_{k=0}^{\infty}a_{k}x^{k}$, wobei immer vorausgesetzt wird, dass ab einem Index $k_{0}$ alle Koeffizienten verschwinden: $a_{k_{0}+1}=a_{k_{0}+2}=\dots=0$, also tatsächlich nur endlich viele Summanden auftreten. Ist $p(x)$ ungleich dem Nullpolynom, so nennt man das maximale $k$ mit $a_{k}\not=0$ den #Grad von $p(x)$, in Zeichen $grad(p(x))$. Man beachte auch, dass $x$ kein Element aus $R$ ist, sondern wirklich als "Unbestimmte" zu sehen ist. Im Speziellen sind zwei Polynome nur dann gleich, wenn alle Koeffizienten gleich sind.
Sind nun $p(x)=\sum_{k=0}^{\infty}a_{k}x^{k},q(x)=\sum_{k=0}^{\infty}b_{k}x^{k}$ zwei Polynome über $R$, so definiert man Summe $p(x)+q(x)$ und Produkt $p(x) \cdot q(x)$ durch
$$
p(x)+q(x)=\sum_{k=0}^{\infty}(a_{k}+b_{k})x^{k} \text{ und }p(x)\cdot q(x)=\sum_{k=0}^{\infty}\left(\sum_{j=0}^{k} a_{j}\cdot b_{k-j}\right)x^{k}
$$
Die algebraische Struktur $(R[x],+,\cdot)$ ist, wie man leicht nachrechnen kann, wieder ein Ring, der #Polynomring über $R$.

Es fällt auf, dass die Definition von $p(x)+q(x)$ und $p(x)\cdot q(x)$ auch für (formale) unendliche Summen verwendet werden kann. Man betrachtet daher die Menge $R[[x]]$ der formalen #Potenzreihe $\sum_{k=0}^{\infty}a_{k}x^{k}$ mit Koeffizienten $a_{k}\in R$, sie bildet mit $+$ und $\cdot$ den Ring der formalen Potenzreihen über $R$.

## Nullteiler
Man beachte, dass in jedem Ring $R$ die Rechenregel $a \cdot 0=0\cdot a=0$ gilt; ist also in einem Produkt ein Faktor $0$, so ist auch das Produkt $0$. Aus $0+0=0$ folgt nämlich $a\cdot0=a(0+0)=a\cdot0+a\cdot 0$ und nach Addition mit $-(a \cdot 0)$ die Beziehung $a \cdot 0= 0$. In ähnlicher Weise zeigt man $0 \cdot a=0$, aber auch $-(a\cdot b)=(-a) \cdot b=a\cdot(-b)$.
In einem Ring kann das Produkt zweier von $0$ verschiedener Elemente dennoch $0$ sein. Z.B. gilt in $\mathbb{Z}_{6}$ die Beziehung $\overline{2}\cdot\overline{3}=\overline{6}=0$. Man nennt i.Allg. ein Element $a\not=0$ eines Ringes $R$ #Nullteiler, wenn es ein $b\not=0$ aus $R$ gibt, so dass $a \cdot b=0$ oder $b \cdot a=0$ ist. Ringe ohne Nullteiler werden gesondert betrachtet.

## Integritätsring
Ein kommutativer Ring mit Einselement ohne Nullteiler heißt #Integritätsring.
### Beispiel
Der Ring $(\mathbb{Z},+,\cdot)$ ist ein Integritätsring, $\mathbb{Z}_{m,+,\cdot} (m\geq1)$ ist nur ein Integritätsring, wenn $m$ eine Primzahl ist. Weiters sind die Polynomringe $R[x]$ und der Ring der formalen Potenzreihen $R[[x]]$ über einem Integritätsring $R$ wieder Integritätsringe.

Ein wesentlicher Vorteil, in einem Integritätsring zu arbeiten, ist es, dass die #Kürzungsregel gilt. Ist $a\not=0$ und $a \cdot b=a \cdot c$, so folgt $a \cdot(b-c)=0$ und damit auch $b-c=0$ bzw. $b=c$, also 
$$
a \cdot b = a \cdot c \land a\not= 0 \implies b=c
$$
In einem beliebigen Ring $R$ kann man stets durch Elemente $a \in R$ kürzen, die ein multiplikatives Inverses $a^{-1}$ besitzen. Solche Elemente heißen auch #Einheiten. Es ist direkt nachzurechnen, dass die Menge aller Einheiten $R^{*}$ von $R$ eine (multiplikative) Gruppe bildet, die so genannte #Einheitsgruppe von $R$. Beispielsweise ist $\mathbb{Z}^{*}=\{ -1,1 \}$

$\mathbb{Z}^{*}_{m}$ besteht genau aus jenen Restklassen $\overline{a}$, welche' die Eigenschaft $ggT(a,m)=1$ erfüllen. Außerdem gilt $|\mathbb{Z}^{*}_{m}|=\varphi(m)$, wobei $\varphi(m)$ die Euler'sche $\varphi$-Funktion bezeichnet. Man beachte insbesondere, dass für eine Primzahl $p\in \mathbb{P}$ die Beziehung $\varphi(p)=p-1$ gilt, d.h. alle Elemente aus $\mathbb{Z}_{p}$ außer $\overline{0}$ sind Einheiten. Diese Beobachtung führt uns zu einer weiteren zentralen algebraischen Struktur.
## Körper
Ein kommutativer Ring $(K,+,\cdot)$ mit Einselement $1\not=0$, in dem jedes Elemente $a\not=0$ eine Einheit ist, also ein multiplikatives Inverses besitzt, heißt ein Körper

Eine algebraische Struktur $(K,+,\cdot)$ ist also genau dann ein Körper, wenn $(K,+)$ und $(K\setminus\{ 0 \},\cdot)$ kommutative Gruppen sind und die Distributivgesetze gelten.

### Beispiel 
Die Strukturen $(\mathbb{Q},+,\cdot)$, $(\mathbb{R},+,\cdot)$ und $(\mathbb{C},+,\cdot)$, aber auch $(\mathbb{Z}_{p},+,\cdot) (p\in \mathbb{P})$ sind Körper. Ist $m \in \mathbb{Z}$ keine Primzahl, so ist $(\mathbb{Z}_{m},+,\cdot)$ kein Körper. Stellt man nämlich $m$ durch $m=k*l$ mit $1<k<m$ und $1<l<m$ dar, so haben die Restklassen $\overline{k}$ und $\overline{l}$ kein multiplikatives Inverses. 

Wie man bereits aus der Definition sieht, besteht ein enger Zusammenhang zwischen Integritätsringen und Körpern, allerdings sind, wie das Beispiel der ganzen Zahlen $\mathbb{Z}$ zeigt, die Begriffe sicherlich verschieden. Allgemein gilt der folgende Satz.

Jeder Körper ist ein Integritätsring, und jeder endliche Integritätsring ist ein Körper.

### Beweis
Jeder Körper ist definitionsgemäß ein kommutativer Ring mit Einselement. Angenommen, es gäbe $a,b \in K \setminus\{  0\}$ mit $a \cdot b = 0$, so folgt nach Multiplikation mit $a^{-1}$ die widersprüchliche Beziehung $b=a^{-1} \cdot 0 =0$. Daher gibt es in einem Körper keine Nullteiler, er ist also auch ein Integritätsring. Sei nun umgekehrt $R = \{ r_{0},r_{1},\dots,r_{n-1} \}$ ein endlicher Integritätsring und $a\in R\setminus\{  0\}$. Wegen der Kürzungsregel sind die Elemente $a \cdot r_{0},a \cdot r_{1},\dots,a\cdot r_{n-1}$ alle paarweise verschieden. Es muss daher $\{  a \cdot r_{0},a\cdot r_{1},\dots,a\cdot r_{n-1} \} = R$ gelten. Insbesondere muss es ein $j$ mit $a \cdot r_{j}=1$ geben. Es sind demnach alle Elemente $a\not=0$ invertierbar, also ist $R$ ein Körper.

### Beispiel
Wir betrachten die Polynome vom Grad $\leq1$ über dem Körper $\mathbb{Z}_{2}$, also die Menge $F=\{ \overline{0},\overline{1},x,\overline{1}+x \}$ und definieren folgende Operationen:

| $+$              | $\overline{0}$   | $\overline{1}$   | $x$              | $\overline{1}+x$ |
| ---------------- | ---------------- | ---------------- | ---------------- | ---------------- |
| $\overline{0}$   | $\overline{0}$   | $\overline{1}$   | $x$              | $\overline{1}+x$ |
| $\overline{1}$   | $\overline{1}$   | $\overline{0}$   | $\overline{1}+x$ | $x$              |
| $x$              | $x$              | $\overline{1}+x$ | $\overline{0}$   | $\overline{1}$   |
| $\overline{1}+x$ | $\overline{1}+x$ | $x$              | $\overline{1}$   | $\overline{0}$   |


| $\cdot$          | $\overline{0}$ | $\overline{1}$   | $x$              | $\overline{1}+x$ |
| ---------------- | -------------- | ---------------- | ---------------- | ---------------- |
| $\overline{0}$   | $\overline{0}$ | $\overline{0}$   | $\overline{0}$   | $\overline{0}$   |
| $\overline{1}$   | $\overline{0}$ | $\overline{1}$   | $x$              | $\overline{1+}x$ |
| $x$              | $\overline{0}$ | $x$              | $\overline{1}+x$ | $\overline{1}$   |
| $\overline{1}+x$ | $\overline{0}$ | $\overline{1}+x$ | $\overline{1}$   | $x$              |
Wie man nachrechnet, ist $(F,+,\cdot)$ ein Körper mit 4 Elementen.

### Konstruieren von Körpern
Allgemein lässt sich zeigen, dass es nur für Primzahlpotenzen $p^{m}(m\geq1)$ endliche Körper mit $p^{m}$ Elementen gibt. Es gibt also keinen Körper mit 6 Elementen, aber einen mit 8 und einem mit 9. Wir deuten nun abschließend an, wie man endliche Körper dieser Art, die in der Kodierungstheorie und der Kryptografie von großer Bedeutung sind, konstruieren kann. Ausgangspunkt ist die Division mit Rest von Polynomen über einem Körper.

Seien $a(x)$ und $b(x)$ zwei Polynome mit Koeffizienten aus einem Körper $K$, und sei $b(x)\not=0$. Dann gibt es Polynome $q(x),r(x) \in K[x]$ mit
$$
a(x)=b(x)q(x)+r(x)
$$
wobei $r(x)$ entweder das Nullpolynom ist oder $grad(r(x)) < grad(b(x))$

Damit kann man wie in den ganzen Zahlen mit Hilfe einer Divisionskette den größten gemeinsamen Teiler zweier Polynome bestimmen. Dabei heißt ein Polynom $d(x) \in K[x]$ größter gemeinsamer Teiler der Polynome $a(x),b(x)\in K[x]$, wenn $d(x)$ ein gemeinsamer Teiler von $a(x)$ und $b(x)$ ist und jeder gemeinsame Teiler $t(x)\in K[x]$ von $a(x)$ und $b(x)$ ein Teiler von $d(x)$ ist. Schließlich gelingt es mit demselben Verfahren wie bei den ganzen Zahlen, zwei Polynome $e(x)$ und $f(x)$ mit $a(x)e+b(x)f=d(x)$ zu finden.
Es sei nun $q(x)\in K[x]$ ein festes Polynom ungleich Nullpolynom. Die polynomiellen Vielfachen $q(x)K[x]$ dieses Polynoms bilden einen additiven Normalteiler von $K[x]$. Auf der additiven Faktorgruppe $K[x]/ q(x)K[x]$ kann in natürlicher Weise eine Multiplikation definiert werden, nämlich $\overline{a(x)} \cdot \overline{b(x)}=\overline{a(x)\cdot b(x)}$, und $K[x]/q(x)K[x]$ wird dadurch wieder zu einem Ring. Das Rechnen in diesem Faktorring ist - grob gesprochen - das Rechnen in $K[x]$ modulo dem Polynom $q(x)$. 

Sei $K$ ein Körper, ferner sei $q(x)\in K[x]$ ein Polynom mit Koeffizienten aus $K$ und $grad(q(x))\geq1$. Dann ist der Faktorring $(K[x]/q(x)K[x],+,\cdot)$ genau dann ein Körper, wenn das Polynom $q(x)$ #irreduzibel über $K$ ist, d.h. wenn $q(x)$ nicht als Produkt zweier Polynome $a(x),b(x)\in K[x]$ mit kleinerem Grad als $q(x)$ dargestellt werden kann.

Ist $q(x)$ ein irreduzibles Polynom vom Grad $k\geq 1$ über $\mathbb{Z}_{p}$, so ist $F=\mathbb{Z}_{p}[x]/q(x)\mathbb{Z}_{p}[x]$ ein endlicher Körper. Jede Restklasse in $F$ kann wegen $a(x)=b(x)q(x)+r(x)$ eindeutig durch ein Polynom vom Grad $< k$ repräsentiert werden. Daher hat $F$ genau $p^{k}$ Elemente. Beispielsweise führt das über $\mathbb{Z}_{2}$ irreduzible Polynom $p(x)=x^{2}+x+1$ auf den vorhin angegebenen Körper $F$ mit 4 Elementen.

Das soeben beschriebene Verfahren wird auch benützt, einen Körper $K$ um Nullstellen von Polynomen zu erweitern.

#### Beispiel
Das Polynom $q(x)=x^{2}+1$ ist irreduzibel über $\mathbb{R}$. Daher ist der Faktorring $F=\mathbb{R}[x]/(x^{2}+1)\mathbb{R}[x]$ ein Körper. Die Nebenklasse $I=x+(x^{2}+1)\mathbb{R}[x]$ hat die Eigenschaft $I \cdot I=x^{2}+(x^{2}+1)\mathbb{R}[x]=-1+(x^{2}+1)\mathbb{R}[x]$. Es ist leicht einzusehen, dass $F$ nichts anderes als die komplexen Zahlen $\mathbb{C}$ repräsentiert. Die imaginäre Einheit $i$, die Nullstelle von $q(x)=x^{2}+1$, muss nur mit $I=x+(x^{2}+1)\mathbb{R}[x]$ identifiziert werden.