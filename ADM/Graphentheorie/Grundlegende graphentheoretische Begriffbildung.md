Ein Graph $G=(V,E)$ besteht aus einer endlichen Knotenmenge $V = V(G)$ und einer endlichen Kantenmenge $E=E(G)$. Dabei ist eine #Kante $e\in E(G)$ entweder #gerichtet auch geordnetes Paar $e=(v_{1},v_{2})$ oder #ungerichtet auch ungeordnetes Paar $e=\{ v_{1},v_{2} \}=v_{1}v_{2}$ von zwei Knoten $v_{1},v_{2} \in V(G)$. Im gerichteten Fall spricht man bei $v_{1}$ vom #Anfangsknoten und bei $v_{2}$ vom #Endknoten von $e$. Sind alle Kanten gerichtet so ist $G$ ein gerichteter Graph, sind sie jedoch alle ungerichtet so ist $G$ ein ungerichteter Graph.

Auch gibt es Kanten der Form $(v_{1},v_{1})$, $\{ v_{1},v_{1} \}=\{ v_{1} \}=v_{1}v_{1}$. So eine Kante wird auch als #Schlinge bezeichnet. Des weiteren können ungerichtete Kanten als Zusammenfassung von zwei gerichteten Kanten gesehen werden $e = \{ v_{1},v_{2} \}=\{ (v_{1},v_{2}),(v_{2},v_{1}) \}$

Sind zwei Knoten durch eine Kante verbunden so sind diese #adjazent. Die Anzahl der Knoten eines  Graphen wird mit $\alpha_{0}(G)=|V(G)|$ und die Anzahl der Kanten mit $\alpha_{1}(G)=|E(G)|$ bezeichnet. 

Auch gibt es Graphen mit #Mehrfachkanten. Solche Kanten können die gleichen Anfangs und Endknoten haben und so nicht mehr an ihren Paaren identifiziert werden. 

Ein Graph heißt #schlicht wenn dieser keine #Schlingen oder #Mehrfachkanten enthält.

## Schlichter Graph
In einem #schlichten #ungerichteten Graphen heißten die zu $v\in V(G)$ #adjazenten Knoten #Nachbarn von $v$
$$
\Gamma(v)=\{ w\in V(G)| vw \in E(G) \}
$$
Die Anzahl der Nachbarn ist der #Knotengrad
$$
d(v)=|\Gamma(v)|=|\{ w\in  V(G) | vw \in E(G) \}|
$$
In einem #gerichteten Graphen bilden die #Nachfolger und #Vorgänger von $v$ die Nachbarn von diesem ab
$$
\Gamma^{+}(v)=\{ w\in V(G) | (v,w) \ \in E(G) \}
$$
$$
\Gamma^{-}(v)=\{ w\in V(G) | (w,v) \in E(G) \}
$$
$$
\Gamma(v) = \Gamma^{+}(v) \cup \Gamma^{-}(v)
$$
Die Anzahl der #Nachfolger ist der #Weggrad von $v$ , also die Anzahl der Kanten die von $v$ wegführen
$$
d^{+}(v)=|\Gamma^{+}(v)|=|\{ w \ \in V(G)  | (v,w) \in E(G )\}|
$$
Die Anzahl der #Vorgänger ist der #Hingrad von $v$, also die Anzahl der Kanten die zu $v$ führen.
$$
d^{-}(v)=|\Gamma^{-}(v)|=|\{ w \in V(G) | (w,v) \in E(G) \}|
$$
Man beachte das bei dieser Definition von gerichteten Graphen Schlingen zugelassen werden.
### Handschlagschema
In einem schlichten ungerichteten Graphen gilt
$$
\sum_{v \in V(G)} d(v) = 2|E(G)|
$$
In einem gerichteten Graphen gilt
$$
\sum_{v \in V(G)}d^{+}(v)=\sum_{v\in V(G)}d^{-}(v)=|E(G)|
$$
Dies ist der Fall da bei einem gerichteten Graphen jede Kante genau einmal gezählt wird. Bei einem ungerichteten Graphen jedoch werden die Kanten zweimal gezählt da sie $A$ zu $B$ und $B$ zu $A$ verbinden.

## Teilgraph
Ein Graph $G' = (V',E')$ heißt #Teilgraph eines Graphen $G=(V,E)$, wenn $V' \subseteq V$ und $E' \subseteq E$ gelten
Ein Teilgraph $G'$ heißt induzierter Teilgraph wenn alle Kanten welche für Knoten in $G$ enthalten sind, auch für die Teilmenge an Knoten in $G'$ enthalten sind. Dieser kann vereinfacht mit $G'=V'$ angegeben werden da die Kanten von $G$ abgeleitet werden können.

## Kantenfolge
Eine Folge von Kanten $e_{1},e_{1},\dots,e_{k} \in E(G)$ eines ungerichteten Graphen $G$ heißt #Kantenfolge, wenn es Knoten $v,v_{1},v_{2},\dots,v_{k-1},w \in V(G)$ gibt welche man durchlaufen kann
$$
e_{1}=vv_{1},e_{2}=v_{1}v_{2},\dots,e_{k-1}=v_{k-2}v_{k-1},e_{k}=v_{k-1}w
$$
Man sagt auch das die Kantenfolge $e_{j}~(1\leq j\leq k)$ die Knoten $v$ und $w$ verbindet. Die Anzahl $k$ der Kanten ist die Länge der Kantenfolge. Eine Kantenfolge der Länge $0$ wird auch als leere Kantenfolge bezeichnet

Eine Folge von Kanten eines gerichteten Graphen heißt Kantenfolge, wenn für zwei aufeinander folgende Kanten der Endknoten von $e_{j}$ der Anfangsknoten on $e_{j+1}$ ist $1\leq j\leq k$.
$$
e_{1}=(v,v_{1}),e_{2}=(v_{1},v_{2}),\dots,e_{k-1}=(v_{k-2},v_{k-1}),e_{k}=(v_{k-1},w)
$$
Hier werden die Knoten $v$ und $w$ wieder durch die Kantenfolge verbunden. So ist $w$ #erreichbar von $v$, wenn es eine Kantenfolge von $v$ nach $w$ gibt.

Eine Kantenfolge heißt #Kantenzug wenn alle Kanten voneinander verschieden sind.

Eine Kantenfolge in einem ungerichteten Graphen heißt #Weg bzw. in einem gerichteten Graphen heißt #Bahn, wenn alle Knoten welche durchlaufen werden verschieden sind.

Eine Kantenfolge die einen Knoten $v$ mit sich selbst verbindet heißt #geschlossen. In einem ungerichteten Graphen heißt diese Kantenfolge auch #Kreis, wenn kein Knoten außer $v$ und keine Kante mehrfach vorkommt.
Eine geschlossene Kantenfolge in einem gerichteten Graphen heißt #Zyklus, wenn kein Knoten außer $v$ mehrfach vorkommt.

Werden zwei Knoten $v$ und $w$ mit einer Kantenfolge verbunden so gibt es auch einen Weg/Bahn um die beiden zu verbinden und nur Kanten aus der Kantenfolge zu nutzen.

Gibt es in einem ungerichteten Graph zwei Wege zwischen $v$ und $w$ so gibt es einen Kreis positiver Länge, welcher nur Kanten aus den beiden Wegen enthält.
Gibt es in einem gerichteten Graphen eine geschlossene Kantenfolge positiver Länge so gibt es auch einen Zyklus positiver Länge welcher nur Kanten aus der geschlossenen Kantenfolge enthält.

Sei $G$ ein Graph mit Knotenmenge $V(G)=\{ v_{1},v_{2},\dots,v_{n} \}$. Die #Adjazentmatrix $A(G)=(a_{ij})$ ist eine quadratische $n \times n$-Matrix mit
$$
a_{ij}=\Bigg \{ \begin{array}{c}~~~ 1~~~ \text{ für }(v_{i},v_{j}) \in E(G) \text{ bzw. } v_{i}v_{j} \in E(G), \\0 ~~~\text{ sonst.} ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~\end{array}
$$

Die Adjazentmatrix eines ungerichteten Graphen ist immer symmetrisch also $a_{ij}=a_{ji}$.
Schlingen sind erkennbar durch $a_{ii}=1$ in der Diagonalen. Schlichte ungerichtete Graphen sind also symmetrisch mit einer Diagonale von $a_{ii}=0$. Auch kann man Graphen mit Mehrfachkanten eine Adjazentmatrix zuordnen wo $a_{ij}$ die Anzahl der Kanten bezeichnet.

So eine Matrix könnte beispielsweise so aussehen
$$
A(G)=\left( \begin{array}{ccc} 1 & 1 & 0 \\ 1 & 0 & 1 \\ 0 & 1 & 0 \\ \end{array}\right)
$$
Mit Hilfe so einer Matrix lässt sich der Knotengrad ablesen. Ist der Graph schlicht und ungerichtet gilt
$$
d(v_{i})=\sum ^{n}_{j=1}a_{ij}=\sum ^{n}_{j=1}a_{ji}
$$
Ist der Graph gerichtet gilt 
$$
d^{+}(v_{i})=\sum ^{n}_{j=1}a_{ij} \text{ und }d^{-}(v_{i})=\sum ^{n}_{j=1}a_{ji}
$$
Weiters kann mit Hilfe der Potenzen der Adjazentmatrix die Erreichbarkeit beschrieben werden. Ist $a_{ij}^{[k]}$ die Anzahl der Kantenfolgen der Länge $k$ von $v_{i}$ nach $v_{j}$ so ist
$$
A(G)^{k}=(a_{ij}^{[k]})
$$
das $i-j$-te Element der $k$-ten Potenz positiv und es gibt eine Kantenfolge. Doch kann die Länge eines Weges/Bahn nicht länger als $|E|$ bzw. $|V|-1$ sein.
$$
C=(c_{ij})=\sum_{k=0}^{m}A(G)^{k} ~~~~~ \text{ mit }~~~~~m=min\{ |E(G)|,|V(G)|-1 \}
$$
so ist $v_{j}$ von $v_{i}$ erreichbar, wenn $c_{ij} > 0$ ist

## Zusammenhängende Graphen
Ein ungerichteter Graph heißt #zusammenhängend, wenn es zwischen je zwei $v,w \in V(G)$ eine Kantenfolge von $v$ nach $w$ gibt. Die maximalen zusammenhängenden #Teilgraphen heißen #Komponenten von $G$

Ein gerichteter Graph heißt stark zusammenhängend, wenn für je zwei $v,w \in V(G)$ eine gerichtete Kantenfolge von $v$ nach $w$ existiert. 
Ein gerichteter Graph heißt schwach zusammenhängend, wenn für je zwei $v,w \in V(G)$ eine Kantenfolge ohne Berücksichtigung der Richtung der Kante existiert.
Die maximalen starken/schwachen Teilkomponenten eines gerichteten Graphen heißen starke/schwache #Zusammenhangskomponenten oder Komponenten des starken/schwachen Zusammenhangs.

Mit Hilfe der Adjazentmatrix lässt sich die Anzahl der Kantenfolgen der Länge $k$ zwischen zwei Knoten berechnen.

### Satz von Menger
Sei $G$ ein ungerichteter Graph und $v,w$ zwei verschiedene Knoten. Dann ist die maximale Anzahl von kantendisjunkten Wegen, die $v$ und $w$ verbinden gleich der minimalen Anzahl von Kanten, die man aus $G$ entfernen muss, um $v$ und $w$ in $G$ zu trennen