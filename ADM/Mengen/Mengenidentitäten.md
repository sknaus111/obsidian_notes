Mengenidentitäten sind allgemein Gleichungen für Mengen. Um diese zu überprüfen kann ein allgemeines Verfahren angewendet werden. Man nehme die Identität
$$
A\cap(B\vartriangle C)=(A\cap B)\vartriangle(A\cap C)
$$
Mittels einer Wahrheitstabelle kann für jede Konstellation ob $x$ in $A,B$ oder $C$ ist ein genauer Wert gegeben werden.

| $A$        | $B$        | $C$        | $B\vartriangle C$ | $A\cap(B\vartriangle C)$ | $A\cap B$ | $A\cap C$ | $(A\cap B)\vartriangle (A\cap C)$ |
| ---------- | ---------- | ---------- | ----------------- | ------------------------ | --------- | --------- | --------------------------------- |
| $\in$      | $\in$      | $\in$      | $\not \in$        | $\not\in$                | $\in$     | $\in$     | $\not\in$                         |
| $\in$      | $\in$      | $\not \in$ | $\in$             | $\in$                    | $\in$     | $\not\in$ | $\in$                             |
| $\in$      | $\not \in$ | $\in$      | $\in$             | $\in$                    | $\not\in$ | $\in$     | $\in$                             |
| $\in$      | $\not \in$ | $\not \in$ | $\not\in$         | $\not\in$                | $\not\in$ | $\not\in$ | $\not\in$                         |
| $\not \in$ | $\in$      | $\in$      | $\not\in$         | $\not\in$                | $\not\in$ | $\not\in$ | $\not\in$                         |
| $\not \in$ | $\in$      | $\not \in$ | $\in$             | $\not\in$                | $\not\in$ | $\not\in$ | $\not\in$                         |
| $\not \in$ | $\not \in$ | $\in$      | $\in$             | $\not\in$                | $\not\in$ | $\not\in$ | $\not\in$                         |
| $\not \in$ | $\not \in$ | $\not \in$ | $\not\in$         | $\not\in$                | $\not\in$ | $\not\in$ | $\not\in$                         |
So kann man anhand der Tabelle erkennen, dass die beiden Ausdrücke gleich sind. 