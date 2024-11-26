Sei $A$ eine nichtleere Menge. Eine #binäre_Operation $\circ$ auf $A$ ist eine Abbildung $A \times A \rightarrow A$, d.h. je zwei Elementen $a,b \in A$ wird eine Element $a \circ b$ zugeordnet. Das Paar $(A,\circ)$ heißt dann binäre algebraische Struktur oder #Gruppoid

Die Addition bildet auf den Zahlenmengen eine algebraische Struktur
$$
(\mathbb{N},+), (\mathbb{Z},+), (\mathbb{R},+), (\mathbb{C}, +)
$$
Sowie die Multiplikation
$$
(\mathbb{N}, *), (\mathbb{Z},*),(\mathbb{R},*),(\mathbb{C},*)
$$
Oft betrachtet man bei einer binären Relation nur die Elemente $a,b$, die in einer Teilmenge $B \subseteq A$ sind. Hier ist wichtig dass $a \circ b$ wieder in $B$ liegt. Die Eigenschafft nennt man #Abgeschlossenheit der Operation $\circ$ auf $B$. 

## Rechenregeln
Die folgenden Gesetzmäßigkeiten können für eine algebraische Struktur $(A,\circ)$ zusätzlich definiert werden

- (i) #Assoziativgesetz : Für alle $a,b,c \in A$ gilt $$
(a \circ b) \circ c = a \circ (b \circ c)
$$
- (ii) Existenz eines #neutralen_Elements : Es gibt ein $e \in A$ mit der Eigenschaft, dass für alle $a \in A$ gilt $$
e \circ a=a \circ e = a
$$
- (iii) Existenz #inverser_Elemente : Für alle $a \in A$ gibt es ein $a' \in A$ mit $$
a \circ a' = a' \circ a = e
$$
	wobei $e$ das neutrale Element aus (ii) bezeichnet
- (iv) #Kommutativgesetz : Für alle $a,b \in A$ gilt $$
a\circ b = b \circ a
$$
Bei Multiplikation schreibt man als das inverse Element von $a$ auch $a^{-1}$ oder $\frac{1}{a}$. Bei Addition ist das inverse Element von $a$, $-a$

Da diese Eigenschaften nur zusätzlich sind sieht man, dass das inverse Element bei Addition in den natürlichen Zahlen nicht existiert und bei Multiplikation ohne die Null auszuschließen nicht einmal in den Rationalen Zahlen.

In einer algebraischen Struktur $(A, \circ)$ gibt es höchstens ein neutrales Element, und in jeder assoziativen algebraischen Struktur gibt es zu jedem Element höchstens ein inverses Element.

Es wird daher im Folgenden nur mehr vom neutralen Element $e$ bzw. vom inversen Element $a^{-1}$ gesprochen werden, sofern diese existieren.

