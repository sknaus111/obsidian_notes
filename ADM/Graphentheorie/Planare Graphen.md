Ein Graph $G$ heißt #planar oder #eben, wenn $G$ kreuzungsfrei in der Ebene $\mathbb{R}^{2}$ dargestellt werden kann, d.h. die Kurven, die die Kanten repräsentieren, haben außer in jenen Punkten, die die Knoten repräsentieren, keine weiteren Schnittpunkte

Auf gut Deutsch überschneiden sich keine Kanten

Der Graph aus 4 Knoten, wobei jeder Knoten jeden anderen durch eine Kante verbindet, ist planar.

```tikz
\begin{document} \begin{tikzpicture}

% Knoten 
\node (a) at (0, 2) {}; 
\node (b) at (0, 0) {}; 
\node (c) at (-2, -2) {}; 
\node (d) at (2, -2) {}; 

\draw (a) -- (b);
\draw (a) -- (c);
\draw (a) -- (d);
\draw (b) -- (c);
\draw (b) -- (d);
\draw (c) -- (d);


\end{tikzpicture} 
\end{document}
```

Die kreuzungsfreie Darstellung eines Graphen $G$ zerlegt die Ebene in eine endliche Anzahl von Gebieten. Diese Anzahl ist unabhängig davon, wie man $G$ in der Ebene kreuzungsfrei repräsentiert. Man bezeichnet diese Anzahl durch $\alpha_{2}(G)$.

## Euler'sche Polyederformel
Für einen zusammenhängenden planaren Graphen $G$ gilt
$$
\alpha_{0}(G)- \alpha_{1}(G)+\alpha_{2}(G) = 2
$$
### Beweis der Euler'schen Polyederformel
Jeder planare Graph kann aus einem Baum erzeugt werden, welchem weiter Kanten hinzugefügt werden. Offensichtlich ist die Formel für einen Baum richtig da gilt $\alpha_{0}(T)=\alpha_{1}(T)+1$ und $\alpha_{2}(T)=1$. Da durch jedes hinzufügen einer Kante $\alpha_{1}$ und $\alpha_{2}$ um 1 erhöht werden ist die Formel wahr.

Durch Projektion eines konvexen Polyeders $P$ (Durschnitt von endlich vielen Halbräumen im $\mathbb{R}^{3}$) auf eine im Inneren des Polyeders liegende Kugel erhält man auf der Kugeloberfläche eine kreuzungsfreie Darstellung eines Graphen $G$, der dieselbe Anzahl von Knoten, Kanten und Gebieten hat wie das Polyeder Eckpunkte, Kanten und Flächen. Projiziert man nun die Kugeloberfläche mittels stereographischer Projektion auf die Ebene (wobei als Nordpol weder ein Knotenpunkt noch ein Punkt einer Kante des Graphen auf der Kugeloberfläche verwendet werden darf) so wird die kreuzungsfreie Darstellung von $G$ in der Ebene projiziert. Natürlich bleibt auch bei dieser Projektion die Anzahl der Knoten, Kanten und Gebiete gleich. Daher gilt auch
$$
\alpha_{0}(P)-\alpha_{1}(P)+\alpha_{2}(P)=2
$$
wobei $\alpha_{0}(P)$ die Anzahl der Eckpunkte, $\alpha_{1}(P)$ die Anzahl der Kanten und $\alpha_{2}(P)$ die Anzahl der Flächen des Polyeders $P$ bezeichnet.

Aus der eben geführten Überlegung ergibt sich auch die folgende Eigenschaft.

Ein Graph läßt sich genau dann kreuzungsfrei in der Ebene darstellen, wenn er kreuzungsfrei auf einer Kugeloberfläche darstellbar ist.

Graphen können nur planar sein wenn sie wenige Kanten haben also mindestens $\alpha_{1}(G) <3\alpha_{0}(G) -6$ erfüllen.

## Satz von Kuratowski
Ein Graph $G$ ist genau dann nicht planar, wenn er einen Teilgraphen enthält, der aus $K_{5}$ oder $K_{3,3}$
durch eventuelle Unterleitung (von Kanten) entsteht. (Dabei ist eine Unterteilung ein Graph, der aus $G$ dadurch hervorgeht, dass in einer oder in mehreren Kanten von $G$ zusätzliche Knoten eingefügt werden.)

## Färbungseigenschaften
Ein wichtiges Gebiet in der Graphentheorie sind Färbungseigenschaften. Dabei geht es die Knoten/Kanten so zu färben, dass gewisse Eigenschaften erfüllt sind. Beispielsweise kann eine Eigenschaft fordern, dass benachbarte Knoten verschiedene Farben haben. Die #chromatische_Zahl $\chi(G)$ eines Graphen beschreibt die minimale Anzahl an Farben, die diese Eigenschaft erfüllen können.

Für planare Graphen gilt $\chi(G)\leq 4$.