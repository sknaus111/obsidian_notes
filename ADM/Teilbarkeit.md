Definition: Es seien $a,b$ ganze Zahlen. Man sagt $b$ **teilt** $a$, in Zeichen $b|a$, wenn es eine ganze Zahl $c$ mit $a=b*c$ gibt, also wenn $\frac{a}{b}$ wieder eine ganze Zahl ist.


## Größter gemeinsamer Teiler
Definition: Für $a,b \in \mathbb{Z}$ heißt $d = ggT(a,b)$ ein **größter gemeinsamer Teiler**, wenn folgend zwei Eigenschaften erfüllt sind.
- (i) $d|a$ und $d|b$
- (ii) Ist $t$ gemeinsamer Teiler von $a$ und $b$, d.h. $t|a$ und $t|b$,dann gilt auch $t|d$
Man beachte, dass der größte gemeinsame Teiler $d$ mit dem Abstand zur null gemessen werden. So muss man negativen Zahlen mit deren Absolutbetrag vergleichen.

Zwei Zahlen sind #teilerfremd, wenn $ggT(a,b) = 1$

Ähnlich wird das kleinste gemeinsame Vielfache definiert.

Um den $ggT$ mit Hilfe des Euklidischen Algorithmus effizient zu bestimmen braucht man dafür die **Division mit Rest**. 
Seien $a,b \in \mathbb{Z}, b>0$ dann gibt es ganze Zahlen $q,r \in \mathbb{Z}$. $q$ ist der #Quotient und $r$ der #Rest der Division
$$
a=b*q+r ~~~~~~~~~\text{und} ~~~~~~~~~0\leq r<b
$$
Beweis: Man setzt $q=\frac{a}{b}$ und $r=a-bq = (\frac{a}{b}-q)b$. Da $0\leq \frac{a}{b}-q<1$ gilt, gilt $0\leq r<b$ 

### Euklidischer Algorithmus
Führt man für zwei ganze Zahlen die Divisionskette durch
$$
a=bq_{0}+r_{0}, ~~~~~0<r_{0}<b
$$
$$
b=r_{0}q_{1}+r_{1}~~~~~0<r_{1}<r_{0}
$$
$$
r_{0}=r_{1}q_{2}+r_{2} ~~~~~0<r_{2}<r_{1}
$$
$$
\vdots
$$
$$
r_{k-2}=r_{k-1}q_{k}+r_{k} ~~~~~0<r_{k}<r_{k-1}
$$
$$
r_{k-1}=r_{k}q_{k+1}+0
$$
so wird diese Aufgrund von $b>r_{0}>r_{1}>r_{2}>\dots>0$ einmal abbrechen. Der letzte Rest $r_{k} \not =0$ ist dann der größte gemeinsame Teiler $ggT(a,b)$

### Beweis
Es folgt aus $r_{k}|r_{k-1}$ auch $r_{k}|r_{k-2}$ und $r_{k}|r_{j}$ für $0\leq j<k$. Schließlich hat dies $r_{k}|a$ und $r_{k}|b$ zur Folge.
Gilt $t|a$ und $t|b$ so folgt $t|(a-q_{0}b)=r_{0}$ daraufhin $t|r_{1}$ und induktiv $t|r_{k}$
Daher ist $r_{k}=ggT(a,b)$

Die Anzahl der Divisonsschritte ist aus $r_{k-2}\geq r_{k-1}+r_{k}\geq2*r_{k}$ gefolgt
$$
r_{k}\leq \frac{1}{2} *r_{k-2}
$$
Das Verfahren bricht nach wenigen Schritten ab
### Beispiel
Gesucht ist $ggT(59,11)$
$$
59 = 11*5+4
$$
$$
11=4*2+3
$$
$$
4=3*1+1
$$
$$
3=1*3+0
$$
Der letzte Rest $> 0$ war 1. Daraus folgt das $ggT(59,11) = 1$

Umgekehrt kann man mit dem $ggT(59,11)=1$ und den letzten beiden Resten $3$ und $4$ wieder auf die ursprünglichen $a$ und $b$ schließen.
$$
1 = 4 - 3*1
$$
$$
=4-(11-4*2)*1
$$
$$
=3*4-1*11
$$
$$
=3*(59-5*11)-1*11
$$
$$
= 3*59-16*11
$$
**Satz**: ist d der größte gemeinsame Teiler der von Null verschiedenen ganzen Zahlen $a,b$ , so gibt es ganze Zahlen $e,f$ mit
$$
ea+fb=d
$$
die mit Hilfe der Divisionskette des Euklidischen Algorithmus von $a$ und $b$ effektiv berechnet werden können.