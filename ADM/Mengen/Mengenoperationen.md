Die #Vereinigung $A \cup B$ enthält jene Elemente, die in mindestens einer von den Mengen enthalten sind
$$
A \cup B = \{x|x\in A\lor x\in B\}
$$
Der #Durchschnitt $A \cap B$ enthält jene Elemente, die in allen Mengen des Durschnitts enthalten sind.
$$
A \cap B=\{x|x\in A\land x\in B\}
$$

Sei $I$ eine Menge an mehreren Mengen $A_{i}$, wobei $i$ Objekte der Menge $I$ sind. Die Vereinigung aller einzelnen Elemente würde so aussehen.
$$
\bigcup_{i\in I}A_{i}=\{x| \exists i \in I :x\in A_{i}\}
$$
Der Durschnitt aller Elemente würde so aussehen.
$$
\bigcap_{i\in I}A_{i}=\{x|\forall i\in I:x \in A_{i}\}
$$
## Komplement
Sei die Menge $E$ ein **Universum**, welches alle im Kontext relevanten Elemente umfasst. So wäre für die Menge $A$ ihr Komplement $A'$
$$
A'=\{x\in E|x\not\in A\}
$$
## Rechenregeln
Seien $A,B,C$ und $A_{i}, i\in I$ Teilmengen einer Menge $E$ gelten folgende Rechenregeln.
- (i) $A \cup B=B\cup A~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~A\cap B=B\cap A$
- (ii) $A \cup (B \cup C)=(A\cup B)\cup C ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~A \cap (B\cap C)=(A\cap B)\cap C$
- (iii) $A \cap (B\cup C)=(A\cap B)\cup(A\cap C)~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~A\cup(B\cap C)=(A\cup B)\cap(A\cup C)$
- (iii)' $A \cap \bigcup_{i\in I}A_{i}=\bigcup_{i\in I}(A\cap A_{i})~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~A \cup\bigcap_{i\in I}A_{i}=\bigcap_{i\in I}(A\cup A_{i})$
- (iv) $A \cup \emptyset =A ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~A\cap E=A$
- (v) $A\cup A'=E~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~A\cap A'=\emptyset$
- (vi) $A\cup A=A~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~A\cap A=A$
- (vii) $A \cup E=E~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~A\cap \emptyset=\emptyset$
- (viii) $A\cup(A\cap B)=A~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~A\cap(A\cup B)=A$
- (ix) $(A\cup B)'=A'\cap B'~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~(A\cap B)'=A'\cup B'$
- (ix)' $(\bigcup_{i\in I}A_{i})'=\bigcap_{i\in I}A_{i}' ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~(\bigcap_{i\in I}A_{i})'=\bigcup_{i\in I}A_{i}'$

Erste Regel ist das #Kommutativgesetz , die zweite das #Assoziativgesetz , die dritte das #Distributivgesetz achte das #Verschmelzungsgesetz und neunte die #DeMorgansche_Regel 

Die #Mengendifferenz $A\setminus B$ enthält jene Elemente, die in $A$, aber nicht in $B$ enthalten sind.
$$
A\setminus B = \{x|x\in A \land x \not\in B\}
$$
Die **symmetrische Differenz** zweier Zahlen sind jene Menge von $A$ oder $B$ ausgeschlossen mit den Elementen in $A$ und $B$.
$$
A\vartriangle B=(A\setminus B)\cup(B\setminus A)
$$
Um Mengen zu veranschaulichen können #Vendiagramme nützlich sein.