## 389) 
Sei $\varphi: G → H$ ein Gruppenhomomorphismus und N ein Normalteiler von H. Man zeige,
dass dann $U =\varphi^{-1}(N)$ ein Normalteiler von G ist.

## 427) 
Man bestimme $\mathbb{Z}^{*}_{6}$ und $\mathbb{Z}^{*}_{3}$ und überprüfe, ob diese beiden Gruppen isomorph sind.

$ggT(1,6)=1$
$ggT(2,6)=2$
$ggT(3,6)=3$
$ggT(4,6)=2$
$ggT(5,6)=1$

$\mathbb{Z}^{*}_{6}=\{ 1,5 \}$

$ggT(1,3)=1$
$ggT(2,3)=1$

$\mathbb{Z}^{*}_{3}=\{ 1,2 \}$

| $\cdot$        | $\overline{1}$ | $\overline{5}$ |
| -------------- | -------------- | -------------- |
| $\overline{1}$ | $\overline{1}$ | $\overline{5}$ |
| $\overline{5}$ | $\overline{5}$ | $\overline{1}$ |
 
| $*$            | $\overline{1}$ | $\overline{2}$ |
| -------------- | -------------- | -------------- |
| $\overline{1}$ | $\overline{1}$ | $\overline{2}$ |
| $\overline{2}$ | $\overline{2}$ | $\overline{1}$ |
Überprüfen ob
$\varphi(a\cdot b) = \varphi(a) * \varphi (b)$
für Abbildung
$\varphi:\mathbb{Z}^{*}_{6}\rightarrow \mathbb{Z}^{*}_{3}$

$\varphi(\overline{1} \cdot \overline{5})=\varphi(\overline{1})*\varphi(\overline{5})$
$\varphi(\overline{5})=\overline{1}*\overline{2}$
$\overline{2}=\overline{2}$

$\varphi^{-1}(\overline{1})=\overline{1}, \varphi^{-1}(\overline{2})=\overline{5}$

Definieren Abbildung als
$\varphi:\mathbb{Z}^{*}_{3} \rightarrow \mathbb{Z}^{*}_{6}$

$\varphi(\overline{1}*\overline{2}) =\varphi(\overline{1})\cdot \varphi(\overline{2})$
$\varphi(\overline{2})= \overline{1} \cdot \overline{5}$
$\overline{5}=\overline{5}$
## 434) 
Sei $〈R, +, ·〉$ ein Ring, in dem $a^{2} = a$ für alle $a ∈ R$ gilt. Man zeige, dass dann $R$ kommutativ
ist. (Hinweis: Man betrachte $(a + a)^{2}$ und $(a + b)^{2}$.)

z.z. $\forall a,b \in R:ab=ba$

$$
(a+a)^{2}=(a+a)\cdot(a+a)= a\cdot(a+a)+a \cdot(a+a) =a^{2}+a^{2}+a^{2}+a^{2}
$$
$$
(a+a)^{2}=a^{2}+a^{2}+a^{2}+a^{2}
$$
ursprüngliche Voraussetzung $a^{2}=a$
$$
a+a=a+a+a+a
$$
$$
0=a+a
$$



$$
(a+b)^{2}=(a+b)\cdot(a+b)= a\cdot(a+b)+b\cdot(a+b) =a^{2}+ab+ba+b^{2}
$$
$$
(a+b)^{2}=a^{2}+ab+ba+b^{2}
$$
ursprüngliche Voraussetzung $a^{2}=a$
$$
a+b=a+ab+ba+b
$$
$$
-a +a +b -b = -a +a +ab +ba +b -b
$$
$$
0=ab+ba
$$
$$
ab+ab=ab+ba
$$
$$
-ab+ab+ab=-ab+ab+ba
$$
$$
ab=ba
$$
## 436) 
Man ermittle, ob beim Übergang von $R$ zu $R × R$ (Bsp. 431) die folgenden Eigenschaften
erhalten bleiben:

a) Kommutativität, b) Nullteilerfreiheit, c) Existenz eines Einselementes.

$$(a, b) + (c, d) = (a + c, b + d)$$
$$(a, b) · (c, d) = (a · c, b · d)$$
### Kommutativität
$$
(a,b)\cdot(c,d)=(a\cdot c,b \cdot d)=(c\cdot a,d \cdot b)=(c,d)\cdot(a,b)
$$
### Nullteilerfreiheit
Suchen Elemente $\not= (0,0)$ für die gilt $(a,b)\circ(c,d)=(0,0)$

$$
(a,b)\cdot(c,d)=(a\cdot c,b\cdot d)=(0,0) \implies a\cdot c = 0 \land b \cdot d=0 
$$
$$
\implies a \lor c = 0 \land b \lor d=0
$$
erfüllt für beispielsweise
$$
(a,0)\cdot(0,d)=(a\cdot 0, 0\cdot d)=(0,0)
$$
nicht nullteilerfrei
### Existenz eines Einselementes
$$
(a,b)\cdot(c,d)=(a,b)*1
$$
$$
(a,b)\cdot(c,d)=(a\cdot c,b\cdot d) =(a,b) \implies a \cdot c = a \land b \cdot d = b
$$
$$
\implies c = 1 \land d = 1
$$
$$
\text{ Neutrales Element }(1,1)
$$
##  Präsenzbeispiel
Für Ring $R$ beweise $\forall x,y \in R: (-x)y=-(xy),x(-y)=-(xy),(-x)(-y)=xy$

$$
x + (-x)=0
$$
$$
(x+(-x))y=0
$$
$$
xy+(-x)y=0
$$
$$
-(xy)+xy+(-x)y=-(xy)
$$
$$
(-x)y=-(xy)
$$



$$
y+(-y)=0
$$
$$
x(y+(-y))=0
$$
$$
xy+x(-y)=0
$$
$$
-(xy)+(xy)+x(-y)=-(xy)
$$
$$
x(-y)=-(xy)
$$


$$
(-x)(-y)=xy
$$
$$
\implies (-(x(-y)))
$$
$$
\implies(-(-(xy)))
$$
$$
\implies xy
$$
