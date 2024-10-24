Eine binäre Relation $R$ auf einer Menge $A$ heißt #Äquivalenzrelation , wenn folgende drei Eigenschaften erfüllt sind.
- #Reflexivität $\forall a \in A: aRa$
- #Symmetrie $\forall a,b \in A: aRb \implies bRa$
- #Transitivität $\forall a,b,c \in A:(aRb \land bRc)\implies aRc$

## Beispiele für Äquivalenzrelationen

### Identische Relation
$A$ sei eine beliebige Menge und $R$ die Relation $=$. Daher steht jede Element $a\in A$ nur mit sich selbst in Relation

### Allrelation
$A$ sei eine beliebige Menge und $R$ die Relation $R=A\times A=A^2$. Daher steht jedes Element $a\in A$ mit jedem anderem Element $b\in A$ in Relation.

### Restrelation
$A=\mathbb{Z}$ sei die Menge der ganzen Zahlen und $R$ die Relation $aRb \iff a\equiv b \bmod m$. Jedes Element $a\in A$ steht mit den Elementen in gleicher Restklasse in Relation

### Funktionsrelation
Sei $A$ eine Menge und $f: A\longrightarrow B$ eine beliebige Funktion. Setzt man $aRb \iff f(a) = f(b)$ so ist $R$ eine Äquivalenzrelation.


## Beispiele für Darstellungen

### kartesische Darstellung
In kartesischer Darstellung kann man die Reflexivität und die Symmetrie daran ablesen, dass es die #erste_Mediane gibt, und dass sich die Elemente entlang der ersten Mediane spiegeln. 


### Graph basierte Darstellung
Die Reflexivität in einem Graphen $G(x)$ ist daran erkennbar, dass alle #Knoten mit #Schlingen schließlich auf sich selbst zeigen. Die Symmetrie lässt sich an den gepaarten #Kanten erkennen. Die Transitivität lässt sich anhand der #Knoten ablesen.

## Äquivalenzklassen
Ein System von nichtleeren Teilmengen $A_{j}~~(j\in I)$ einer Menge $A$ heißt #Partition oder #Zerlegung von $A$, wenn die $A_{i}~~(i\in I)$ paarweise disjunkt sind d.h.
$$
A_{i}\cap A_{j}~~~~~\text{für}~i\not=j
$$
und $A$ die Vereinigung
$$
A=\bigcup_{i\in I}A_{i}
$$
ist. 
Sei $R$ eine Äquivalenzrelation auf $A$. Für $a\in A$ heißt die Menge
$$
K(A)=\{b\in A|bRa\}
$$
die von $a$ erzeugt #Äquivalenzklasse. Aufgrund der #Reflexivität gilt auch immer $a\in K(a)$.

Sei $R$ eine #Äquivalenzrelation auf $A$. Dann bilden die #Äquivalenzklassen der Elemente von $A$ eine Partition von $A$.
Sei umgekehrt $A_{i}~~(i\in I)$ eine Partition von $A$ und bezeichne $\check{K}(a)~~(a\in A)$ jene Teilmenge $A_{j}$ der Partition mit $a\in A_{j}$. Definiert man $aRb$ genau für jene $a,b \in A$, für die $\check{K}(a)=\check{K}(b)$ gilt, so ist $R$ eine #Äquivalenzrelation mit $K(a)=\check{K}(a)$ für alle $a\in A$.

### Beweis
Es sei $R$ eine #Äquivalenzrelation auf der Menge $A$. Es sei $\mathcal{K} = \{K(a)|a\in A\}$ das System der #Äquivalenzklassen .
Offensichtlich gilt $K(a)\subseteq A$ und $a\in K(a)$. So ist auch kein $K(a)$ für $a\in A$ leer. Es folgt $\bigcup_{a\in A}K(a)=A$. Nun muss noch gezeigt werden, dass versch. #Äquivalenzklassen kein Element gemeinsam haben, also #disjunkt sind $K(a)\not=K(b)$. Wäre $c\in K(a)\cap K(b)$, würde $cRa$ und $cRb$ folgen, dies würde aber wegen der Symmetrie und Transitivität zu $aRb$ führen. Daraus folgt aber $K(a)=K(b)$, was ausgeschlossen wurde.
Nun gilt zu überprüfen ob $R$ reflexiv, symmetrisch und transitiv ist. $\check{K}(a)=\check{K}(a)$ folgt $aRa$ und $\check{K}(a)=\check{K}(b)\implies\check{K}(b)=\check{K}(a)$ und $\check{K}(a)=\check{K}(b)\land \check{K}(b)=\check{K}(c)\implies\check{K}(a)=\check{K}(c)$
