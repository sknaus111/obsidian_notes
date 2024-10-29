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
Eine Auswahl in der die Elemente von $A$ mehrmals vorkommen können. Diese Auswahl wird auch als #Kombination_mit_Wiederholung bezeichnet. 

#### Beispiel
Man nehme von der Menge $A$ eine Teilmenge bestehend aus $7$ Elementen
$$
A =\{a_{1},a_{2},a_{3},a_{4}\}, ~~~~~~~~~T=\{a_{1},a_{1},a_{1},a_{2},a_{2},a_{4},a_{4}\} 
$$
Wenn man nun alle Kugeln nicht gefüllt färben will gibt es keine Möglichkeit ihre ursprünglichen Werte zu unterscheiden. Aufgrund dessen setzen wir Trennkugeln $n-$ dazwischen.
$$
a_{1},a_{1},a_{1},\bullet ,a_{2},a_{2},\bullet,\bullet,a_{4},a_{4}
$$
Nun Ist es möglich aus rein gefüllten und nicht gefüllten die ursprünglichen Elemente zu rekonstruieren.
$$
\circ \circ \circ  \bullet  \circ \circ \bullet \bullet \circ \circ
$$
Aufgrund der Gleichheitsregel ist die Anzahl möglicher Auswahlmöglichkeiten von Elementen von $A$ die Anzahl der Permutationen von $k$ nicht gefüllten Kugeln und $n-1$ gefüllten Kugeln
$$
\frac{(k+n-1)!}{k!(n-1)!}=\binom{k+n-1}{k}
$$
## Aufteilungsprobleme

In den Aufteilungsproblemen geht es darum eine Menge in mehrere Teilmengen, auch #Partitionen , aufzuteilen.

Die Anzahl möglicher Partitionen einer Menge aus $n$ Elementen in $k$ Teile werden dargestellt durch die #Stirlingzahlen_2_Art .
$$
S_{n,k}=\frac{1}{k!}\sum_{j=0}^{k}(-1)^{k-j}\binom{k}{j}j^{n}, ~~~(0\leq k\leq n)
$$
Diese erfüllen auch folgende Rekursion
$$
S_{n+1,k}=S_{n,k-1}+k*S_{n,k}~~~~~~~~~~S_{n,n}=1, n>0 ~~~~~S_{n,0}=0, n\geq1
$$
Die Anzahl aller möglichen Partitionen einer einer Menge aus $n$ Elementen werden auch als #Bellzahlen bezeichnet.
$$
B_{n}=\sum ^{n}_{k=0}S_{n,k}
$$
Diese erfüllen folgende Rekursion
$$
B_{n+1}=\sum ^{n}_{k=0}\binom{n}{k}B_{k} ~~~~~~~~~~~~~~B_{1}=1
$$
### Zahlpartitionen
Auch ist es möglich natürliche Zahlen in ihre Summanden aufzuteilen. Zum Beispiel kann die Zahl $4$ wie folgt aufgeteilt werden
$$
1+1+1+1, 1+1+2, 2+2, 1+3, 4
$$
Somit ist $p(4)=5$, da es $5$ verschiedene Reihenfolgen unabhängige Möglichkeiten gibt $4$ als Summe von natürlichen Zahlen darzustellen.

Die #Partitionsfunktion $p(n)$ beschreibt alle möglichen Partitionen einer natürlichen Zahl
Ist nun ein $p(n,k)$ gegeben wo die Partitionen je aus $k$ Summanden bestehen, so ist folgende rekursive Definition gegeben.
$$
p(n,k) = p(n-k,k) + p(n-1,k-1) ~~~~~~~~~~~~~p(n,1)=p(n,n)=1
$$

## Schubfachprinzip
Ähnlich wie bei den Partitionen wird eine Menge aus $n$ Elementen in mehrere Teilmengen aufgeteilt. Beim Schubfachprinzip jedoch können die Teilmengen auch leer sein. Bildlich kann man sich eine Menge aus $n$ Elementen vorstellen die in $k$ Teilmengen (Schubladen) aufgeteilt wird. Beispielsweise kann man 13 Personen in Geburtsmonate aufteilen oder Zahlen in Restklassen. 

Ist $n>k$ so ist in einer Schublade mehr als $1$ Element enthalten.