**Definition:** eine natürliche Zahl $p>1$ heißt #Primzahl, wenn die einzigen Teiler von $p$ die Zahlen $\pm1$ und $\pm p$ sind. Die Menge der Primzahlen wird mit $\mathbb{P}$ bezeichnet. 

**Satz** Teilt eine Primzahl $p$ eine Produkt ganzer Zahlen $a_{1},a_{2},\dots,a_{r}$ also $p|a_{1}a_{2}\dots a_{r}$ dann teilt sie wenigstens einen der Faktoren, also $p\mid a_{j}$ für ein $j \in \{1,2,\dots,r\}$

## Beweis
Zuerst beweisen wird den Satz für den Anfangsfall mir $r=2, a=a_{1},b=a_{2}$. Mit vollständiger Induktion wird dann der allgemeine Fall bewiesen.
$p|ab$ sei gegeben.
Fall 1: $p\mid a$ dann ist nichts weiteres zu beweisen.
Fall 2: $p \nmid a$ dann gilt dass $ggT(p,a)=1$. Dies ist der Fall, da $p$ nur $1$ und sich selbst als Teiler hat.  Da $p$ nicht $a$ teilt ist dieser ausgeschlossen und nur $1$ bleibt als ggT übrig.
Der Satz [[Teilbarkeit#Satz]] sagt aus, dass es zwei #Ganzen_Zahlen $e,f$ gibt für welche $1=ep+fa$ gilt. So kann $b$ in der Form $b=bep+fab$ , indem man die gerade eben gestellt Gleichung mit $b$ erweitert. $bep$ ist durch $p$ teilbar, da $p$ durch sich selbst teilbar ist. $fab$ ist durch $p$ teilbar, da dies bereits in der Annahme vorgegeben ist, dass $ab$ durch $p$ teilbar ist. So gilt $p\mid bep+fab=b$

## Fundamentalsatz der Zahlentheorie
Jede natürliche Zahl $a\geq 2$ lässt sich als Produkt von Primzahlen darstellen.
$$
a=p_{1}*p_{2}*\dots*p_{r} ~~~\text{mit}~p_{1},p_{2},\dots,p_{r}\in\mathbb{P}
$$
wobei die Darstellung bis auf die Reihenfolge eindeutig ist.

### Beweis
Zuerst zeigt man, dass $a$ als Produkt von Primzahlen darstellbar ist. 
Fall 1: $a$ ist eine Primzahl $a\in\mathbb{P}$, so ist nichts zu beweisen.
Fall 2: $a$ ist keine Primzahl $a \not \in \mathbb{P}$, so kann $a$ als $a = a_{1}*a_{2}$ mit $1<a_{1}<a$ und $1<a_{2}<a$ dargestellt werden. $a_{1}$ und $a_{2}$ sind die anderen Teiler von $a$ außer $a$ selbst und $1$. Diese ergeben sich aus der Tatsache, dass $a$ keine Primzahl ist.
Nun wendet man die vorherige Vorgehensweise auf $a_1$ und $a_{2}$ an. Die Teiler werden immer kleiner, bis $a$ als Produkt endlich vieler Primzahlen beschrieben werden kann.

Man nehme an $a$ hätte zwei Darstellungen aus Produkten von Primzahlen.
$$
a=p_{1}*p_{2}*\dots*p_{r}=q_{1}*q_{2}*\dots*q_{s} ~~~~~~~~~~p_{i},q_{j}\in\mathbb{P}
$$
Insbesondere gilt $p_{1}|q_{1}*q_{2}*\dots*q_{s}$. Demnach gilt
$$
p_{1}\mid q_{1} \text{ oder }p_{1}\mid q_{2} \text{ oder }\dots \text{ oder }p_{1}\mid q_{s}
$$
Man nehme an $p_{1}|q_{1}$. Daraus folgt dass $p_{1}=q_{1}$, da beides Primzahlen $\not=1$ sind und keine Teiler außer sich selbst haben. Also erhält man
$$
p_{2}*p_{3}*\dots*p_{r}=q_{2}*q_{3}*\dots*q_{s}
$$
Diesen Schritt kann wieder angewendet ($p_{2}|q_{2}$). Diese Verfahren ergibt, dass die Primzahlenfolge $p_{1},p_{2},\dots,p_{r}$ und $q_{1},q_{2},\dots,q_{s}$ bis auf die exakte Reihenfolge genau gleich sind.

Für eine natürliche Zahl $a$ und eine Primzahl $p$ schreibt man $v_{p}(a)=k$, falls $p^k\mid a$ und $p^{k+1}\nmid a$. Aus dem Fundamentalsatz erhält man durch Zusammenfassung der Primzahlen zu Potenzen die #Primfaktorzerlegung
$$
a = 2^{v_{2}(a)}*3^{v_{3}(a)}*5^{v_{5}(a)}*7^{v_{7}(a)}\dots=\prod_{p\in\mathbb{P}}p^{v_{p}(a)}
$$

 

Mit der Primzahlzerlegung sind auch Teilbarkeitseigenschaften ablesbar
$$
a\mid b \iff v_{p}(a)\leq v_{p}(b) \text{ für alle }p\in\mathbb{P}
$$
### Beispiel
$a=60 = 2^2*3^1*5^1$ Die Potenz $v_{2}(60)=2, v_{3}(60)=1$ und $v_{5}(60)=1$. Für alle anderen Primzahlen ist die Potenz 0 $v_{p}(60)=0$  

### Satz 
Es gibt unendlich viele Primzahlen.

### Beweis
Man nähme an, es gebe nur endlich viele Primzahlen $P={p_{1},\dots,p_{N}}$

So betrachte man die Zahl
$$
q=p_{1}*\dots*p_{N}+1
$$
Es gilt
$$
p_{1}\nmid q, p_{2} \nmid q , \dots , p_{N} \nmid q
$$
Da die Primzahlen $P$ nicht in der Primzahldarstellung von $q$ vorkommen können, kommt es zu einem Widerspruch mit der Tatsache, dass jede Zahl in Primfaktoren zerlegt werden kann.

### Satz 
Es seien $a = \prod_{p\in\mathbb{P}}p^{v_{p}(a)}$ und $b=\prod_{p \in \mathbb{P}}p^{v_{p}(b)}$ die Primfaktorzerlegungen von $a,b \in \mathbb{N}$. Dann gilt
$$
ggT(a,b)=\prod_{p\in\mathbb{P}}p^{min\{v_{p}(a),_{p}(b)\}} \text{ und }kgV(a,b) = \prod_{p\in\mathbb{P}}p^{max\{v_{p}(a),v_{p}(b)\}}
$$
Auch gilt
$ggT(a,b)*kgV(a,b)=ab$
