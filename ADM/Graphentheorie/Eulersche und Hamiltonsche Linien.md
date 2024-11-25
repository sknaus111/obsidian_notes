## Eulersche Linie
Eine Kantenfolge in einem (gerichteten oder ungerichteten) Graphen $G$ heißt #Eulersche_Linie, wenn sie jeden Knoten und jede Kante enthält, und zwar jede Kante genau einmal. Ein Graph wird als #Eulerscher_Graph bezeichnet, wenn er eine Euler'sche Linie besitzt.

Bei einer geschlossenen Euler'schen Linie stimmen Anfangs- und Endknoten überein, bei einer offenen Euler'schen Linie sind sie verschieden.

Einfacher ausgedrückt beschreibt die Euler'sche Linie ob ein Graph in einem Zug ohne einen Stift abzusetzen gezeichnet werden kann. Ob ein Graph so eine Linie besitzt kann anhand der Knotengrade überprüft werden.

Ein ungerichteter Graph $G$ besitzt genau dann eine geschlossene Euler'sche Linie, wenn $G$ zusammenhängend ist und alle Knotengrade $d(v) ~ (v\in V(G))$ gerade sind.
Ein ungerichteter Graph $G$ besitzt genau dann eine offene Euler'sche Linie, wenn $G$ zusammenhängend ist und mit der Ausnahme von zwei Knoten $w_{1},w_{2} \in V(G)$ mit ungeraden Knotengrade alle übrigen Knotengrade $d(v) (v\in V(G) \setminus \{ w_{1},w_{2} \})$ gerade sind.

```tikz
\begin{document} \begin{tikzpicture}

% Knoten 
\node (a) at (-3, 0) {}; 
\node (b) at (-1, -1) {}; 
\node (c) at (-1, 1) {}; 
\node (d) at (1, 1) {}; 
\node (e) at (1, -1) {}; % Kanten 
\node (f) at (3, 0) {};

\draw (a) -- (b);
\draw (a) -- (c);
\draw (b) -- (c);
\draw (b) -- (d);
\draw (b) -- (e);
\draw (c) -- (d);
\draw (c) -- (e);
\draw (d) -- (e);
\draw (d) -- (f);
\draw (e) -- (f);

\end{tikzpicture} 
\end{document}
```


Ein gerichteter Graph $G$ besitzt genau dann eine geschlossene Euler'sche Linie, wenn $G$ schwach zusammenhängend ist und für alle Knoten $v \in V(G)$ Hin- und Weggrad gleich sind: $d^{+}(v)=d^{-}(v)$
Ein gerichteter Graph $G$ besitzt genau dann eine offene Euler'sche Linie, wenn $G$ schwach zusammenhängend ist und mit der Ausnahme von zwei Knoten $w_{1},w_{2} \in V(G)$, für die $d^{+}(w_{1})=d^{-}(w_{1})+1$ und $d^{+}(w_{2}) = d^{-}(w_{2})-1$ gilt, bei allen übrigen Knoten von $v \in V(G) \setminus \{ w_{1},w_{2} \}$ Hin- und Weggrad gleich sind: $d^{+}(v)=d^{-}(v)$

### Beweis der Euler'schen Linien

Man untersuche einen gerichteten schwach zusammenhängenden Graphen, der die Bedingung $d^{+}(v)=d^{-}(v)$ für alle Knoten erfüllt.

Dies kann mittels vollständiger Induktion bewiesen werden. Sei $m = \alpha_{1}(G)$ die Anzahl der Kanten. Bei $m=0$ besteht der Graph nur aus einem Knoten und somit ist eine Euler'sche Linie in diesem Fall einfach eine leere Kantenfolge, was offensichtlich erfüllt ist. Bei allen $m\geq1$ kann nimmt man an es gilt für alle Graphen mit Anzahl von Kanten weniger als $m$. Da $G$ schwach zusammenhängend ist gilt $d^{+}(v_{1})=d^{-}(v_{1}) > 0$ da $m\geq1$ ist. Also kann man von diesem Anfangsknoten einen Knoten $v_{2}$ finden mit $(v_{1},v_{2}) \in E(G)$. Aufgrund der Bedingung $d^{+}(v_{2})=d^{-}(v_{2})$ existiert auch ein Knoten $v_{3}$ für welchen gilt $(v_{2},v_{3}) \in E(G)$. Solange $v_{j}~~(3\leq j \leq |V(G)|)$ ist kann man diesen Prozess wiederholen bis man bei $v_{1}$ landet. Somit gibt es eine geschlossene Kantenfolge $K$ in der kein Kante mehrfach vorkommt.

Ist $K = E(G)$, so hat man bereits die Euler'sche Linie gefunden. Ist dies nicht de Fall betrachte man $G'=G\setminus K$. Dieser Graph ist zwar vielleicht nicht mehr schwach zusammenhängend doch gilt die Bedingung $d^{+}_{G'}(v)=d^{-}_{G'}(v)$ für alle $(v \in V(G'))$. Aus der Induktionsvoraussetzung folgt nun jedoch, dass jede Komponente von $G'$ aus zusammenhängenden Knoten eine Euler'sche Linie besitzt. Da $G' \cup K =G$ schwach zusammenhängend ist, muss jede Euler'sche Linie einer Komponente von $G'$ einen Knoten mit $K$ gemeinsam haben. Also ist es möglich alle Euler'schen Linien von $G'$ in die ursprüngliche Euler'sche Linie hinzuzufügen, indem man diese im gemeinsamen Knoten einfügt. Wo in der ursprünglichen Kantenfolge eine Kante von $v_{1}$ zu $v_{2}$ und dann zu $v_{3}$ führt kann eine Kantenfolge mit gemeinsamen Knoten $v_{2}$ eingefügt werden, wobei diese bei $v_{2}$ startet und endet und von dort wieder wie in der ursprünglichen Folge zu $v_{3}$ führt.

## Hamilton'sche Linie
Eine Kantenfolge in einem (gerichteten oder ungerichteten) Graphen $G$ heißt #Hamiltonsche_Linie, wenn sie jeden Knoten (mit der möglichen Ausnahme, dass Anfangs- und Endpunkt übereinstimmen) genau einmal enthält. Ein Graph wird als #Hamiltonscher_Graph bezeichnet, wenn er eine Hamilton'sche Linie besitzt. Bei einer geschlossenen Hamilton'schen Linie stimmen Anfangs- und Endkonten überein, bei einer offenen Hamilton'schen Linie sind sie verschieden

Im Gegensatz zu der Euler'schen Linie gibt es bist heute noch kein allgemeines Kriterium für die Existenz von Hamilton'schen Linien, Es gibt aber viele Sätze, die hinreichende Bedingungen für die Existenz einer Hamilton'schen Linie angeben. Als Beispiel dafür der folgende Satz ohne Beweis angegeben.

Sei $G$ ein schlichter ungerichteter Graph mit $n$ Knoten, so dass für alle Knotenpaare $x,y\in V(G)$, die in $G$ nicht durch eine Kante verbunden sind, d.h. $(x,y) \not \in E(G)$
$$
d(x)+d(y)\geq n
$$
gilt. Dann gibt es in $G$ eine geschlossene Hamilton'sche Linie