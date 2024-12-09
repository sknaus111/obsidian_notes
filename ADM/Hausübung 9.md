## 400) 
Von der Abbildung $f : (\mathbb{Z}_{3})^{2} → (\mathbb{Z}_{3})^{4}$ sei bekannt, dass $f$ ein Gruppenhomomorphismus
bezüglich der Addition ist (die jeweils komponentenweise definiert sein soll), sowie dass $f (1, 0) = (0, 1, 2, 1), f (0, 1) = (1, 0, 0, 2)$. Man ermittle daraus $f (w)$ für alle $w ∈ (\mathbb{Z}_{3})^{2}$.

Bekannt ist bereits
$f(1,0)=(0,1,2,1)$
$f(0,1)=(1,0,0,2)$

Homomorphismus
$\varphi(a\circ b)=\varphi(a) * \varphi(b)$

$f(1,1)=f(1,0)+f(0,1)=(0,1,2,1)+(1,0,0,2)=(1,1,2,0)$
$f(1,2)=f(1,1)+f(0,1)=(1,1,2,0)+(1,0,0,2)=(2,1,2,2)$
$f(2,1)=f(1,1)+f(1,0)=(1,1,2,0)+(0,1,2,1)=(1,1,1,1)$
$f(0,2)=f(0,1)+f(0,1)=(1,0,0,2)+(1,0,0,2)=(2,0,0,1)$
$f(2,0)=f(1,0)+f(1,0)=(0,1,2,1)+(0,1,2,1)=(0,2,1,2)$
$f(2,2)=f(1,1)+f(1,1)=(1,1,2,0)+(1,1,2,0)=(2,2,1,0)$
$f(0,0)=f(2,2)+f(1,1)=(2,2,1,0)+(1,1,2,0)=(0,0,0,0)$

## 424) 
Sei $〈R, +, ·〉$ ein Ring mit Einselement und $E(R)$ die Menge derjenigen Elemente in $R$,
die bezüglich der Multiplikation ein inverses Element besitzen. Zeigen Sie, dass $E(R)$ mit der
Multiplikation eine Gruppe bildet (die Einheitengruppe von $R$).

### assoziativ
vom Ring erhalten gebliebene Eigenschaft
$a\cdot b=b\cdot a\implies a^{-1}\cdot b^{-1}=b^{-1}\cdot a^{-1}$
### abgeschlossen
z.z. $a,b \in R \implies ab \in R$
z.z $(ab)^{-1}$

$(ab)(ab)^{-1}=1$
$a(b(ab)^{-1})=1$
$a^{-1}a(b(ab)^{-1})=a^{-1}1$
$1(b(ab)^{-1})=a^{-1}$
$b(ab)^{-1}=a^{-1}$
$b^{-1}b(ab)^{-1}=b^{-1}a^{-1}$
$(ab)^{-1}=b^{-1}a^{-1}$

Da es $(ab)^{-1}$ gibt, ist die Gruppe abgeschlossen
### neutrales Element
Einselement vom Ring, da dieses mit sich selbst inverse ist. 
$e^{-1}=e$
### inverses Element
von Definition gegeben

## 453) 
Sei $M$ die Menge aller positiven Teiler von $60$. Bestimmen Sie alle Komplemente in $(M, ggT, kgV)$.
Ist diese Struktur eine Boolesche Algebra?

Alle Elemente Teiler von $60$
$1,2,3,4,5,6,10,12,15,20,30,60$

Komplemente sind nun Paare wo gilt $kgV(a,a')=\text{Einselement}$, $ggT(a,a')=\text{Nullelement}$
$kgV(a,a')=60, ggT(a,a')=1$

muss gelten $x*y=60$

für 1
$1*60=60$
$kgV(1,60)=60,ggT(1,60)=1$

für 2
$2*30=60$
$kgV(2,30)=60,ggT(2,30=2)$
kein Komplement für zwei

für 3
$3*20=60$
$kgV(3,20)=60,ggT(3,20)=1$

für 4
$4*15=60$
$kgV(4,15)=60,ggT(4,15)=1$

für 5
$5*12=60$
$kgV(5,12)=60, ggT(5,12)=1$

für 6
$6*10=60$
$kgV(6,10)=60,ggT(6,10)=2$
kein Komplement


$(1,60),(3,20),(4,15),(5,12)$

keine Boolsche Algebra, da nicht jedes Element ein Komplement hat

## 460) 
Bildet $\mathbb{R}^{2}$ mit den angegebenen Operationen einen Vektorraum über $\mathbb{R}$?
$$(x_{1}, x_{2}) + (y_{1}, y_{2}) = (x_{1} + y_{1}, 0)$$
,$$ λ(x_{1}, x_{2}) = (λx_{1}, x_{2})$$
Vektorräume sind eine Gruppe und haben daher ein neutrales Element
$(x_{1},x_{2})+(e_{1},e_{2})=(x_{1},0)$
es gibt kein neutrales Element, daher keine Gruppe, daher kein Vektorraum
