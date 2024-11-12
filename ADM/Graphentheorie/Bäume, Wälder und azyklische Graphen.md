## Bäume und Wälder
Ein schlichter ungerichteter Graph $W$, der keine Kreise positiver Länge enthält, heißt #Wald. Ein Wald $T$, der auch zusammenhängend ist, heißt #Baum

Daraus ergibt sich, dass ein die #Zusammenhangskomponenten eines Waldes Bäume sind. In einem Baum $T$ gibt es genau einen Weg zwischen zwei Knoten $v$ und $w$. Dieser wird auch als #Abstand $d_{T}(v,w)$ zwischen den Knoten bezeichnet.

### Anzahl der Knoten und Kanten von Bäumen und Wäldern
Für einen Baum gilt
$$
\alpha_{0}(T)=\alpha_{1}(T)+1
$$
entsprechend gilt für einen Wald mit $k$ Komponenten 
$$
\alpha_{0}(W)=\alpha_{1}(W)+k
$$
#### Beweis der Anzahl von Knoten und Kanten
Da Wäldern aus $k$ vielen Bäumen bestehen folgt der Beweis für Wälder aus dem Beweis für Bäume.
Offensichtlich stimmt die Aussage für $n=\alpha_{0}(T)=1$.
Man nehme an die Aussage stimmt für alle Bäume mit $n$ Knoten. Ist $T$ ein Baum mit $\alpha_{0}=n+1$ Knoten so hat $T$ garantiert einen Knoten $v$ mit einem Knotengrad von $1$, einen so genannten Endknoten der an den ursprünglichen Baum mit $n$ Knoten drangehängt wird. Entfernt man diesen wieder erhält man $T'$ für welches gilt $\alpha_{0}(T')=\alpha_{0}(T)-1=n$ und $\alpha_{1}(T')=\alpha_{1}(T)-1$. Aus der Voraussetzung folgt $\alpha_{0}(T')=\alpha_{1}(T')+1$ und damit $\alpha_{0}(T)=\alpha_{0}(T')+1=\alpha_{1}(T')+2=\alpha_{1}(T)+1$

### Wurzel
Zeichnet man in einem Baum einen Knoten $w \in V(T)$ als sogenannte #Wurzel lässt sich das Bild eins Baumes verdeutlichen. Zeichnet man die Nachbarn von $w$ über $w$, und deren Nachbarn wieder über den einzelnen Knoten entsteht ein Baum wie man aus der Logik kennt. In einem Baum unterscheidet man zwischen externen Knoten mit Knotengrad $1$ und internen Knoten mit Knotengrad $>1$. Die Wurzel wird als externen Knoten gezählt, wenn sie einen Knotengrad von $0$ hat also der einzige Knoten im Graph ist, sonst als internen Knoten.
In der Informatik findet man auch oft sogenannte Binärbäume, wo mit Ausnahme der Wurzel welche einen Knotengrad von $2$ oder $0$ hat, jeder Knoten zu zwei weiteren Knoten verbindet oder keinem. So hat jeder Knoten außer der Wurzel einen Knotengrad von entweder $1$ oder $3$.

## Azyklische Graphen
Ein gerichteter Graph heißt #azyklisch wenn er keine Zyklen positiver Länge hat.

Jeder azyklische Graph besitzt einen Knoten $v\in V(G)$ mit Weggrad $d^{+}(v)=0$ und einen Knoten $w\in V(G)$ mit Hingrad $d^{-}(w)=0$

In einem azyklischen Graphen hat jede Kantenfolge eine beschränkte Länge. Würde man eine Kantenfolge unbeschränkt verlängern würde man einen Knoten irgendwann ein zweites mal erreichen womit es kein Zyklus wäre. Der Endknoten dieser Kantenfolge ist hat dann Weggrad $d^{+}(v)=0$ und der Anfangsknoten dieser Kantenfolge hat den Hingrad $d^{-}(w)=0$.

### Markierungsalgorithmus
Um zu überprüfen ob eine Graph azyklisch ist kann man einen Knoten mit Hingrad oder Weggrad $0$ entfernen um daraus einen neuen azyklischen Graphen zu gewinnen. Können so alle Knoten entfernt werden war der ursprüngliche Graph azyklisch. Dies kann auch als #Markierungsalgorithmus formuliert werden.

1.
- (a) Bestimme alle Knoten $v$ mit Weggrad $d^{+}(v)=0$ und markiere diese mit $\oplus$
- (b) Wurde in 1.(a) kein solcher Knoten gefunden, so ist $G$ nicht azyklisch $\rightarrow$ **ENDE**
2.
 - (a) Sind bereits alle Knoten von $G$ mit $\oplus$ markiert, so ist $G$ azyklisch $\rightarrow$ **ENDE**
 - (b) Suche unmarkierte Knoten, von denen nur Kanten zu schon markierten führen und markiere diese mit $\oplus$
 3.
 - (a) Wurde in 2.(b) mindestens ein Knoten markiert, so wiederhole 2.
 - (b) Wurde in 2.(b) kein Knoten markiert, so ist $G$ nicht azyklisch $\rightarrow$ **ENDE**