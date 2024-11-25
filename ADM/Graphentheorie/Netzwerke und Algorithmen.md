Netzwerke sind gerichtete oder ungerichtete Graphen $G=(V,E)$, wo jeder Kante $e \in E$ ein #Wert $w(e) \in \mathbb{R}$ zugeordnet wird. Dieser Wert kann als Länge, Kosten, Kapazität, etc. gedeutet werden. Formal ist solche Bewertung eine Funktion $w: E \rightarrow \mathbb{R}$. In Netzwerken betrachte man auch die bewertete Adjazentmatrix $A_{w}(G)=(w(v_{i},v_{j}))_{1\leq ij \leq n}$. Hier ist zu definieren welche Bedeutung $w(v_{i},v_{j})=0$ hat.

## Gerüst eines Graphen
Ein spannender Baum $T$ eines schlichten ungerichteten zusammenhängenden Graphen $G$ ist eine Baum mit $V(T) = V(G)$ und $E(T)\subseteq E(G)$, d.h. er enthält dieselben Knoten wie $G$ und besteht aus Kanten von $G$
Ein Gerüst oder spannender Wald $W$ eines schlichten ungerichteten Graphen $G$ ist ein Wald mit $V(W) = V(G)$ und $E(W)  \subseteq E(G)$ und denselben Zusammenhangskomponenten wie $G$, d.h. schränkt man $W$ auf eine Zusammenhangskomponente $K$ von $G$ ein, so ist diese Einschränkung ein spannender Baum von $K$,
Ist $G$ ein bewerteter Graph, so bezeichnet man ein Gerüst $W$ als #minimales_Gerüst, wenn die Summe aller Kantengewichte des Gerüstes
$$
w(W) = \sum_{e\in E(W)} w(e)
$$
unter allen möglichen Gerüsten von $G$ kleinstmöglich ist.

Ein Beispiel für ein Gerüst $W$

```tikz
\begin{document} \begin{tikzpicture}

% Knoten 
\node (a) at (-10, 0) {$\circ$}; 
\node (b) at (-8, 0) {$\circ$}; 
\node (c) at (-7, -2) {$\circ$}; 
\node (d) at (-7, -4) {$\circ$}; 
\node (e) at (-4, 0) {$\circ$}; % Kanten 
\node (f) at (0, 0) {$\circ$};
\node (g) at (0, -4) {$\circ$};
\node (h) at (1, -2) {$\circ$};
\node (i) at (2, -4) {$\circ$};
\node (j) at (5, -1) {$\circ$};

\draw (a) -- (b);
\draw (a) -- (c);
\draw[thick] (a) -- (d);
\draw[thick] (b) -- (c);
\draw (b) -- (e);
\draw[thick] (c) -- (d);
\draw[thick] (c) -- (e);
\draw (d) -- (e);

\draw (f) -- (g);
\draw[thick] (f) -- (h);
\draw[thick] (g) -- (h);
\draw (g) -- (i);
\draw[thick] (h) -- (i);


\end{tikzpicture} 
\end{document}
```
Graphen haben meist viele versch. Gerüste. Der vollständige Graph $K_{n}$ aus $n$ Knoten und allen möglichen $\frac{n(n-1)}{2}$ Kanten $n^{n-2}$ verschiedene spannende Bäume. Um so ein minimales Gerüst nun zu finden baut man es einfach Schritt für Schritt auf. Man fängt mit der Kante mit dem kleinsten Gewicht an und fügt immer die Kante mit dem nächst größeren Wert hinzu. Entsteht durch das Hinzufügen einer Kante ein Kreis so entfernt man diese wieder und schaut sich die nächste Kante an. Diesen Prozess wiederholt man für alle weiteren Kanten.

### Kruskal-Algorithmus

1.  Man nummeriere die Kanten $E = \{ e_{1},e_{2},\dots,e_{n} \}$ nach steigendem Gewicht: $$
w(e_{1}) \leq w(e_{2}) \leq \dots \leq w(e_{m})
$$
2.  Setze $E' := 0$ und $j := 1$
3.  Ist der Graph $(V,E' \cup \{ e_{j} \})$ kreisfrei, so setze $E':=E' \cup \{ e_{j} \}$
4. Ist $|E'| = |V|-1$ oder $j=m$, so wird der Algorithmus beendet und $W=(V,E')$ ist ein minimales Gerüst von $G$. Andernfalls setze $j:=j+1$ und gehe zu Schritt 3

Jedes Gerüst von $G$ hat genau $|V|-k$ Kanten, wobei $k$ die Anzahl der Zusammenhangskomponenten bezeichnet. Ist $k$ bekannt, so kann im Schritt 4. abgebrochen werden, wenn $E'$ bereits $|V| -k$ Kanten enthält.


## Distanz zwischen Knoten
Sei $G=(V,E)$ ein Netzwerk mit Bewertung $w: E \rightarrow \mathbb{R}^{+}_{0}$. Die Länge einer Kantenfolge $e_{1},e_{2},\dots,e_{k}$ ist durch die Summe der Gewichte
$$
w(\{ e_{1},e_{2},\dots,e_{k} \})= \sum_{j=1}^{k}w(e_{j})
$$
gegeben. Die Distanz $d(v,w)$ zwischen zwei Knoten $v,w \in V$ ist die kleinstmögliche Länge einer Kantenfolge von $v$ nach $w$. Gibt es keine Kantenfolge von $v$ nach $w$, so setzt man $d(v,w)=\infty$

Mit Hilfe des #Dijkstra-Algorithmus wird für einen Knoten $v_{0} \in V$ eines Netzwerks mit nichtnegativer Bewertung die Distanz $d(v_{0},v)$ für alle Knoten bestimmt

### Dijkstra-Algorithmus

1. Man setzte $l(v_{0}) = 0, l(v)=\infty$ für alle $v \in V \setminus\{ v_{0} \},U=\{ v_{0} \}$ und $u=v_{0}$
2. Für alle $v \in V\setminus U$ mit $(u,v) \in E$, die $l(v)>l(u)+w(u,v)$ erfüllen, setze man $p(v):=u$ und $$
l(v):=l(u)+w(u,v)
$$
3. Man bestimme $m=min_{v\in V\setminus U} ~l(v)$. Falls $m = \infty$, dann terminiere, andernfalls wähle einen Knoten $z \in V \setminus U$ mit $l(z)=m$ und setze $U:= U \cup \{ z \}$ und $u:=z$.
4. Ist $U=V$, so wird der Algorithmus beendet. Andernfalls gehe zu Schritt 2.

Die Menge $U \subseteq V$ umfasst in jedem Zeitpunkt des Algorithmus jene Knoten $v\in V$, für die der kürzeste Weg von $v_{0}$ schon bekannt ist, wobei $l(v)=d(v_{0},v)$ ist. Für $v\in V \setminus U$ ist hingegen $l(v)$ die minimale Länge einer Kantenfolge, die mit Ausnahme von $v$ nur Knoten aus $U$ enthält, und kann sich im Verlauf des Algorithmus noch ändern. $p(v)$ ist jeweils der Vorgängerknoten von $v$ auf einer minimalen Kantenfolge von $v_{0}$ nach $v$. Aus diesen Bedingungen ist klar, dass der in Schritt 3. ausgewählt Knoten $z$ in $U$ aufgenommen werden kann.
Endet der Algorithmus nicht mit $U=V$, sondern mit der Abbruchbedingung $l(v)=\infty$ für alle $v\in V\setminus U$, so ist $G$ nicht zusammenhängend, und $U$ umfasst genau jene Knoten, die von $v_{0}$ aus erreichbar sind.
Um nicht die Distanz für alle Knoten ausrechnen zu müssen bricht man den Algorithmus ab sobald im Schritt 4. $u=v_{ziel}$ ist.

Beispiel zum Dijkstra-Algorithmus im Buch auf Seite 77-78.
