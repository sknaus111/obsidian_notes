Eine #Menge ist eine Zusammenfassung von wohl unterschiedenen Objekten unserer Anschauung oder unseres Denken zu einem Ganzen. 

Beispiele für Mengen sind die ganzen Zahlen $\mathbb{Z}=\{\dots,-2,-1,0,1,2,\dots\}$.

Eine Menge $A$ enthält meist mehrere Objekte. Ein Objekt $x$ welches in einer Menge $A$ enthalten ist wird als $x \in A$ angeschrieben. Ist $x$ nicht in $A$ wird dies als $x \not \in A$ angeschrieben.

Die Menge mit keinem Element heißt #leere_Menge. 

Mengen können **unendlich** sein wie die Menge der ganzen Zahlen oder auch **endlich** mit einer gewissen Anzahl an Elementen. Für eine Menge $A = \{0,1,2,3\}$ ist die Anzahl ihrer Elemente $|A| = 4$

Eine Menge heißt #Teilmenge, wenn alle ihre Element in einer anderen Menge enthalten sind $A  \subseteq B$.
Zwei Mengen sind gleich, wenn alle ihre Elemente gleich sind $A=B$.  Dies trifft zu wenn A eine Teilmenge von B und B eine Teilmenge von A ist.
$$
A=B \iff A \subseteq B \land B\subseteq A
$$
## Beweis zur Gleichheit von Mengen
Definitionsgemäß sind die beiden Mengen $A$ und $B$ gleich wenn $x\in A$ und $x\in B$ gleichbedeutend sind. Anders könnte man dies so schreiben $\forall x:x\in A\iff x\in B$ und $x\in A \iff x \in B$ ist äquivalent zur Formel $(x\in A \implies x\in B)\land(x\in B\implies x\in A)$.
Die Begriffe $x\in A\implies x\in B$ und $x\in B \implies x\in A$ können mit jeweils $A\subseteq B$ und $B\subseteq A$ ausgetauscht werden. Somit ist $A=B$ gleichbedeutend wie $A \subseteq B \land B \subseteq A$

## Darstellung
Um Mengen darzustellen können mehrere Varianten gewählt werden. Bei einfachen endlichen Mengen kann eine Aufzählung ausreichend sein $A = \{1,2,3\}$. Bei unendlichen komplexeren Mengen ist eine beschreibende Darstellung meistens in Verwendung.
$$
A=\{x,P(x)\}
$$
Die Menge $A$ enthält alle $x$ auf die das Prädikat $P(x)$ zutrifft. Soll die Menge $A$ beispielsweise Teilmenge einer Menge $B$ sein, kann man dies wie folgt schreiben.
$$
A=\{x\in B,P(x)\}
$$
Oft ist es auch verallgemeinerte Mengen zu betrachteten in denen Elemente öfters vorkommen können wie $A=\{1,1,2,2,2,3,4,4\}$. Diese werden auch als #Multimengen bezeichnet. Die #Kardinaliät auch Größe einer Menge, ist bei endlichen Mengen einfach zu bestimmen. Schwieriger wird dies bei unendlichen Mengen.

## Kardinalität
Zwei Mengen sind gleich mächtig sind diese gleich groß. Es kann zu jedem Element einer Menge ein Element der anderen Menge zugeordnet werden. Unendliche Mengen sind jedoch immer gleich mächtig.
Um nun zwischen endlichen und unendlichen Mengen zu unterscheiden stellt man fest das für jede natürliche Zahl $n$ die Mengen $\{k\in\mathbb{N},k<n\}=\{0,1,2,\dots,n-1\}$ genau $n$ Elemente enthalten. Sie hat also die Mächtigkeit $n$. Gibt es eine Menge $A$, für die es eine Menge von einem $n$ gibt, welche gleich mächtig ist, ist $A$ eine endliche Menge. Jede Menge auf die dies nicht zutrifft ist unendlich.

Unendliche Mengen welche gleichmächtig zu $\mathbb{N}$ sind, werden als #abzählbare_Mengen bezeichnet. Diese können durchnummeriert werden. Abzählbar sind auch die ganzen Zahlen $\mathbb{Z}$ und rationalen Zahlen $\mathbb{Q}$. Nicht mehr abzählbar ist die Menge der reellen Zahlen $\mathbb{R}$, diese ist #überabzählbar.