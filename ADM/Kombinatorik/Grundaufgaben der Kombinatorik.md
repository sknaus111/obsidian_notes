Grundregeln für #Abzählverfahren

- #Summenregel $A \cap B = \emptyset \implies |A\cup B|=|A|+|B|$
- #Produktregel $|A\times B|=|A|*|B|$
- #Gleichheitsregel $\exists f:A\rightarrow B\text{ bijektiv }\implies |A|=|B|$
## Fakultät
Unter der Fakultät einer #natürlichen_Zahl $n\geq1$ (bzw. unter #n-Faktorielle ) versteht man das Produkt
$$
n!=1*2*3*\dots*(n-1)*n
$$
Für $0!$ gilt $0!=1$

## Binomialkoeffizient
Der #Binomialkoeffizient $\binom{n}{k}$ (in worten $n$ über $k$) wird für natürliche Zahlen $n,k$ mit $0\leq k \leq n$ durch
$$
\binom{n}{k}=\frac{n!}{k!*(n-k)!}
$$
definiert. Für $n\geq 0 ~\land~k<0$ oder $k>n$ setzt man $\binom{n}{k}=0$

## Anordnungsprobleme und Auswahlprobleme
In der Kombinatorik wird zwischen #Auswahlproblemen und #Anordnugnsproblemen unterschieden. Bei Anordnungsproblemen spielt die Reihenfolge der Elemente eine Rolle, bei Auswahlproblemen nicht.

Sei $A$ eine Menge $\{a_{1},a_{2},a_{3}\dots a_{n}\}$ mit $n$ Elementen.

### Anordnungen ohne Einschränkung
Die Menge $A^k$ der geordneten $k$-Tupel wird als die Menge der Anordnungen von Elementen von $A$ der Länge $k$ interpretiert. Die Reihenfolge ist hier wichtig. Aufgrund der Produktregel gilt
$$
|A^k| = |A|^k =n^k
$$
$A^k$ wird auch als #Variationen_mit_Wiederholung bezeichnet, eine geordnete Auswahl von $k$ Elementen aus $A$ mit zurücklegen. Unter dem Begriff zurücklegen versteht sich die mehrfache Verwendung der Elemente.

### Anordnung verschiedener Elemente
Die geordneten $k$-Tupel von $A$, wobei alle Elemente verschieden sind werden als #Variationen_ohne_Wiederholung bezeichnet. Hier ist die Auswahl ohne Zurücklegen also können Elemente nur einmal verwendet werden. Die abgeänderte Form der Produktregel hierfür sieht wie folgt aus.
$$
n*(n-1)*(n-2)*\dots*(n-k+1)=\frac{n!}{(n-k)!}
$$
### Permutation einer Menge
Eine #Permutation $\pi$ ist eine bijektive Funktion $\pi:A\rightarrow A$. Aufgrund der Bijektivität tritt jedes Element genau 1 auf. Daraus ergibt sich
$$
n!
$$
### Permutation einer Multimenge
Eine abgeänderte allgemeinere Version der Permutation einer Menge ist die #Permutation_einer_Multimenge. Hier gilt, dass jedes Element nicht immer genau einmal vorkommt, sondern, dass ein Element $a_{i}$ genau $k_{i}$ mal auftritt ($1\leq i \leq n$). So gibt es folgend verschiedene Möglichkeiten für so eine Anordnung.
$$
\frac{(k_{1}+k_{2}+\dots+k_{n})!}{k_{1}!*k_{2}!*\dots k_{n}!}
$$
Diese Formel leitet sich daraus her, dass $(k_{1}+k_{2}+\dots+k_{n})!$ die Anzahl aller möglichen Variationen ist, aber davon führen jedoch (aufgrund der Produktregel) $k_{1}!*k_{2}!*\dots*k_{n}!$ Anordnungen zum selben gesuchten Anordnung. 

### Auswahlen einer Teilmenge
Eine ungeordnete Auswahl von $k$ Elementen einer Menge $A$ ist nicht anderes als eine Teilmenge von $A$ der Größe $k$. Diese Auswahl wird auch als #Kombination_ohne_Wiederholung bezeichnet.
$$
\frac{n!}{k!*(n-k)!}
$$
Aus der Menge $A$ wird eine Teilmenge mit $k$ Elementen ohne Zurücklegen genommen.

### Auswahlen einer Teilmultimenge
