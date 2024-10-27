Die Grundalge der Halbordnung ist eine Hierarchie auf einer Menge $A$. 

Eine binäre Relation $R$ auf einer Menge $A$ heißt #Halbordnung oder **partielle Ordnung**, wenn folgende drei Eigenschaften erfüllt sind

- #Reflexivität $\forall a\in A:aRa$
- #Antisymmetrie $\forall a,b \in A: (aRb \land bRa)\implies a=b$
- #Transitivität $\forall a,b,c \in A: (aRb \land bRc) \implies aRc$

Halbordnungen haben die Eigenschaft der #Antisymmetrie.

Eine Halbordnung $R$ auf einer Menge $A$ heißt #Totalordnung, wenn für je zwei Elemente $a,b \in A$ entweder $aRb$ oder $bRa$ gilt d.h. je zwei Elemente sind vergleichbar.

## Totalordnung
$A = \mathbb{R}$ mit $aRb \iff a\leq b$ bildet eine Totalordnung (die natürliche Ordnung der reellen Zahlen)

## allgemeine Halbordnungen
$A = \mathbb{N}$ mit $mRn \iff m|n$ ist eine Halbordnung. Ein Beispiel für eine Ordnung welche die Regeln der Halbordnung verletzen würde, wäre wenn $A=\mathbb{Z}$ ist. Die negativen Gegenstücke haben zwar in der Relation die gleichen Eigenschaften, sind aber verschiedene Zahlen.

$A=P(M)$ mit $BRC \iff B \subseteq C$ bildet eine Halbordnung aber für $|M|>1$ keine Totalordnung.

## Graph basierte Darstellung
Da aufgrund der definierenden Eigenschaften einige Kanten redundant sind führt man folgende Schritte durch um aus einem Graphen $G(R)$ der Halbordnung $R$, ein #Hassediagramm der Relation $R$ zu bekommen

- Weglassen der Schlingen
- Weglassen aller Kanten die sich mit der #Transitivität wiederherstellen lassen. Nur unmittelbare Nachbarn mit Kanten verknüpfen.
- Weglassen der Orientierungen aufgrund der #Antisymmetrie 


Ein Hassediagramm mit $A =P(M)=\{\emptyset,\{1\},\{2\},\{3\},\{1,2\},\{1,3\},\{2,3\},\{1,2,3\} \}$ der Potenzmenge von $M=\{1,2,3\}$ mit der Inklusion($\subseteq$) als Relation.

```tikz
\begin{document}
\begin{tikzpicture}


\node at (0,0.2) {$\{1,2,3\}$};
% Draw lines
\draw[-] (0,0) -- (-2,-2) node[below] {$\{1,2\}$};
\draw[-] (0,0) -- (0,-2) node[below] {$\{1,3\}$};
\draw[-] (0,0) -- (2,-2) node [below] {$\{2,3\}$};

\draw[-] (-2,-2.5) -- (-2,-4.5);
\draw[-] (-1.9,-2.5) -- (-0.1,-4.5);

\draw[-] (-0.1,-2.5) -- (-1.9,-4.5);
\draw[-] (0.1,-2.5) -- (1.9,-4.5);

\draw[-] (1.9,-2.5) -- (0.1,-4.5);
\draw[-] (2,-2.5) -- (2,-4.5);

\draw[-] (0,-7) -- (-2,-5) node[above] {$\{1\}$};
\draw[-] (0,-7) -- (0,-5) node[above] {$\{2\}$};
\draw[-] (0,-7) -- (2,-5) node[above] {$\{3\}$};

\node at (0,-7.2) {$\emptyset$};

\end{tikzpicture}
\end{document}
```

## Ketten
Eine #Kette $K$ einer Halbordnung $(H,R)$ ist eine Teilmenge von $H$, die mit der Relation $R$ eine Totalordnung bildet. Eine Kette heißt **maximal**, wenn diese nicht mit einem Element von $H$ erweiterbar ist, so dass $R$ wieder eine Totalordnung bildet. Ein Beispiel für so eine Kette wäre $K=\{\emptyset,\{1\},\{1,2\},\{1,2,3\}\}$ von $P(\{1,2,3\},\subseteq)$. Das #Hausdorffsche_Maximalitätsprinzip besagt, dass jede Halbordnung eine maximale Kette besitzt. Für endliche Ketten ist dies offensichtlich bei unendlichen aber nicht direkt offensichtlich.

Ein Element $m$ einer Teilmenge $S$ einer Halbordnung $H$ heißt #Minimum, wenn für alle Elemente $s\in S$ die Relation $mRs$ gilt. Beispielsweise ist 0 ist das Minimum der natürlichen Zahlen als Teilmenge in der Halbordnung der ganzen Zahlen. 

Eine Totalordnung heißt #Wohlordnung, wenn jede nicht leere Teilmenge $S$ von $H$ ein Minimum besitzt. Die natürlichen Zahlen bilden beispielsweise eine Wohlordnung.
Es sei nun $A(x)$ ein Prädikat für $x\in H$. Das Prinzip der #transfiniten_Induktion für Wohlordnungen lautet
$$
\forall x \in H: ((\forall yRx, y\not=x:A(y))\implies A(x))\implies \forall x \in H:A(x)
$$
Ist also $A(y)$ wahr für alle $yRx$ $y\not=x$ kann man daraus ableiten dass auch $A(x)$ wahr ist. Gäbe es ein $x\in H$ für welches $A(x)$ falsch ist so betrachte man die Menge $S=\{x\in H:\lnot A(x)\}$. Da $H$ wohlgeordnet ist, gibt es ein Minimum $m$ in $S$. Insbesondere muss für alle $y\in H$ mit $yRm$ $y\not=m$ die Aussage $A(y)$ wahr sein(sonst wäre $m$ nicht Minimum in $S$). Wegen der Voraussetzung müsste dann $A(m)$ wahr sein, was $m\in S$ widerspricht. So ist bewiesen, dass $A(x)$ für alle $x\in H$ wahr ist.
Ähnlich ist dieses Prinzip zur [[vollständige Induktion]], da diese ein Spezialfall der transfiniten Induktion ist. 
