## Aufgabe 1: BDDs
Aus einer Wahrheitstabelle mit der Variablenreihenfolge $π = (x1, x2, x3, x4, x5)$ wurde folgender Bead mit Don’t-Cares ausgelesen:

$$10X0 ~01X1 ~1010 ~X1X1 ~000X ~0X00 ~11X1 ~1X11$$

Dieser Bead wurde mit dem in der Vorlesung vorgestellten Verfahren aus der Wahrheitstabelle von
unten nach oben ausgelesen.

### a) 
Erstellen Sie das minimale BDD mittels der gierigen Variante von Beads.

#### Ebene x1
$$
10X0~01X 1~1010~X1X1
$$
$$
000X~0X 00~11X 1~ 1X11
$$
Nicht zu einem Square vereinfachbar
#### Ebene x2
$$
10X0~01X1
$$
$$
1010~X1X1
$$
Zu einem Sqaure vereinfachbar $1010~01X1$
$$
000X~0X 00
$$
$$
11X 1~1X 11
$$
Nicht zu einem Square vereinfachbar


#### Ebene x3
$$
1010
$$
$$
01X1
$$
Nicht zu einem Square vereinfachbar
$$
000X
$$
$$
0X 00
$$
Zu einem Square vereinfachbar und direkt zu Null führend
$$
11X1
$$
$$
1X 11
$$
Zu einem Square vereinfachbar und direkt zur Eins führend

#### Ebene x4
$$
10
$$
$$
10
$$
Zu einem Square vereinfachbar
$$
01
$$
$$
X1
$$
Zu einem Square vereinfachbar

![[Unbenannt 1.png]]
### b) 

Erstellen Sie die ITE-Darstellung Ihres BDDs aus Unteraufgabe (a).

```python 
if x1 then:
	if x3 then:
		if x5 then:
			1
		else:
			0
	else:
		if x5 then:
			0
		else:
			1
else:
	if x2 then:
		0
	else:
		1
```


## Aufgabe 2: Substitution mit NAND Gattern
Gegeben ist folgende Schaltung:

![[Pasted image 20241122163938.png]]

Formen Sie die gegebene Schaltung so um, dass diese nur noch NAND Gatter mit 2 Eingängen enthält. Verwenden Sie dabei die logischen Konstanten 0 und 1 nicht. Überlegen Sie auch wie Sie durch Vereinfachungen NAND Gatter einsparen können.


Alle Und Gatter zu Nands mit einem Nand dahinter, alle Negationen zu einem Nand Gatter. Da Oder Gatter mit zwei nands zum negieren und einem nand zum verknüpfen.

![[Unbenannt 2.png]]

Diese Schaltung lässt sich aber noch vereinfachen
![[Unbenannt 3.png]]

## Aufgabe 3: Schaltnetz
Es soll eine 3-aus-4-Schaltung entworfen werden. Dabei wird der Ausgang f genau und nur dann logisch 1, wenn mindestens drei der vier Eingänge a, b , c und d logisch 1 sind.

## a) 
Befüllen Sie die zugehörige Wahrheitstafel:

| a   | b   | c   | d   | f(a, b, c, d) |
| --- | --- | --- | --- | ------------- |
| 0   | 0   | 0   | 0   | 0             |
| 0   | 0   | 0   | 1   | 0             |
| 0   | 0   | 1   | 0   | 0             |
| 0   | 0   | 1   | 1   | 0             |
| 0   | 1   | 0   | 0   | 0             |
| 0   | 1   | 0   | 1   | 0             |
| 0   | 1   | 1   | 0   | 0             |
| 0   | 1   | 1   | 1   | 1             |
| 1   | 0   | 0   | 0   | 0             |
| 1   | 0   | 0   | 1   | 0             |
| 1   | 0   | 1   | 0   | 0             |
| 1   | 0   | 1   | 1   | 1             |
| 1   | 1   | 0   | 0   | 0             |
| 1   | 1   | 0   | 1   | 1             |
| 1   | 1   | 1   | 0   | 1             |
| 1   | 1   | 1   | 1   | 1             |

b) Entwerfen Sie grafisch die 3-aus-4-Schaltung und beschriften Sie entsprechend alle Ein- und Ausgänge, wobei Ihnen nur folgende Bausteine zur Verfügung stehen: vier NAND-Gatter mit je drei Eingängen und ein NAND-Gatter mit vier Eingängen:

| a   | b   | c   | d   | f(a, b, c, d) | $a \land b \land c$ | $a \land b \land d$ | $a \land c \land d$ | $b \land c \land d$ | $(\dots)\lor(\dots)\lor(\dots)\lor(\dots)$ |
| --- | --- | --- | --- | ------------- | ------------------- | ------------------- | ------------------- | ------------------- | ------------------------------------------ |
| 0   | 0   | 0   | 0   | 0             | 0                   | 0                   | 0                   | 0                   | 0                                          |
| 0   | 0   | 0   | 1   | 0             | 0                   | 0                   | 0                   | 0                   | 0                                          |
| 0   | 0   | 1   | 0   | 0             | 0                   | 0                   | 0                   | 0                   | 0                                          |
| 0   | 0   | 1   | 1   | 0             | 0                   | 0                   | 0                   | 0                   | 0                                          |
| 0   | 1   | 0   | 0   | 0             | 0                   | 0                   | 0                   | 0                   | 0                                          |
| 0   | 1   | 0   | 1   | 0             | 0                   | 0                   | 0                   | 0                   | 0                                          |
| 0   | 1   | 1   | 0   | 0             | 0                   | 0                   | 0                   | 0                   | 0                                          |
| 0   | 1   | 1   | 1   | 1             | 0                   | 0                   | 0                   | 1                   | 1                                          |
| 1   | 0   | 0   | 0   | 0             | 0                   | 0                   | 0                   | 0                   | 0                                          |
| 1   | 0   | 0   | 1   | 0             | 0                   | 0                   | 0                   | 0                   | 0                                          |
| 1   | 0   | 1   | 0   | 0             | 0                   | 0                   | 0                   | 0                   | 0                                          |
| 1   | 0   | 1   | 1   | 1             | 0                   | 0                   | 1                   | 0                   | 1                                          |
| 1   | 1   | 0   | 0   | 0             | 0                   | 0                   | 0                   | 0                   | 0                                          |
| 1   | 1   | 0   | 1   | 1             | 0                   | 1                   | 0                   | 0                   | 1                                          |
| 1   | 1   | 1   | 0   | 1             | 1                   | 0                   | 0                   | 0                   | 1                                          |
| 1   | 1   | 1   | 1   | 1             | 1                   | 1                   | 1                   | 1                   | 1                                          |

$$
(a \land b \land c) \lor (a \land b \land c) \lor ( a \land c \land d) \lor ( b \land c \land d)
$$
$$
\lnot\lnot((a \land b \land c) \lor (a \land b \land c) \lor ( a \land c \land d) \lor ( b \land c \land d))
$$
$$
\lnot(\lnot(a \land b \land c) \land \lnot(a \land b \land c) \land \lnot( a \land c \land d) \land \lnot( b \land c \land d))
$$
![[Unbenannt 5.png]]
## Aufgabe 4: Demultiplexer
Erstellen Sie ein Schaltbild für die in der Wahrheitstabelle gegebene Funktion mit Hilfe der unten gegebenen Bausteine (DEMUX ist ein Demultiplexer) und den Konstanten log 1 und log 0. Verwenden Sie jeden Baustein nur einmal und vergessen Sie nicht, alle Eingänge und Ausgänge Ihrer Lösung zu beschriften.
Hinweis: Beachten Sie dass beim DEMUX die Zahl $(e_{1}e_{0})_{}2$ den Index des ausgewählten Ausgangs angibt.

| x   | y   | f(x,y) |
| --- | --- | ------ |
| 0   | 0   | 0      |
| 0   | 1   | 1      |
| 1   | 0   | 0      |
| 1   | 1   | 1      |

![[Unbenannt 4.png]]
## Aufgabe 5: Induktive Definition
Sei $A = \{a, b, c, d, . . . , s\}$ eine Menge von Namen. Wir definieren Tripel $\mathbb{T}$ von Zeichenketten über $\mathbb{A}$. D.h. $\mathbb{T}$ ist die kleinste Menge, die folgende Bedingungen erfüllt:

- i) Wenn $α, β ∈ \mathbb{A}$, dann ist $[αα – α – β] ∈ \mathbb{T}$.
- ii) Wenn $α ∈ A$ und $[x – y – z] ∈ \mathbb{T}$, dann gilt auch $[xα – yα – zα] ∈ \mathbb{T}$
- iii) Wenn $[x – y – z] ∈ \mathbb{T}$ und $[v – w – w] ∈ \mathbb{T}$, dann gilt auch $[xv – yw – zw] ∈ \mathbb{T}$.

Hinweis: Vorsicht wir verwenden die Buchstaben $a, b, . . . , s$ als Elemente von $\mathbb{A}$ (vgl. Definition von $\mathbb{A}$) während wir die Buchstaben $v, w, x, y, z$ als Variablen verwenden.

### a) 
Schauen Sie sich die Regeln an, überlegen Sie welche verschiedenen Formen die Zeichenketten in
T haben können, und geben Sie mindestens drei solcher Zeichenketten an (versuchen Sie dabei,
möglichst viele mögliche Formen abzudecken).

### b) 
Betrachten Sie jeden der folgenden Ausdrücke:
• Entscheiden Sie ob der Ausdruck nach obiger Definition ein Term in $\mathbb{T}$ ist.
• Falls der Ausdruck nicht in T ist: Wie könnte man die Definition von $\mathbb{T}$ ändern damit auch
dieser Ausdruck von der Definition erfasst wird?
1) $[aa – b – b]$
2) $[ffg – fg – gg]$
3) $[aac – a – cc]$
4) $[ggc – ggc – agc]$
5) $[ffefe – fefe – fefe]$
6) $[mmnn – mn – nn]$
7) $[iija – ij – jj]$
8) $[ccdoop – cdop – edop]$

## Aufgabe 6: Inferenzen
Geben Sie für die folgenden Schlussfolgerungen die zugrundeliegende Inferenzregel an und stellen
Sie fest, ob die Regel gültig ist. Wenn ja, geben Sie unter Verwendung von Alltagsbegriffen eine weitere Schlussfolgerung an, die derselben Regel folgt.

Wenn nein, finden Sie eine neue Schlussfolgerung, die zeigt, warum die Regel nicht gültig ist. Wir suchen also eine Schlussfolgerung, die derselben Regel folgt und bei der die Prämissen wahr, die Schlussfolgerung aber falsch ist.

### a) 
Alle Kinder mögen Schokolade oder Zuckerwatte. Sara ist ein Kind, das keine Zuckerwatte mag.
Deshalb mag sie Schokolade.

Alle x mögen $z_{1}$ oder $z_{2}$          ... x Kinder , $z_{1}$ Schockolade, $z_{2}$ Zuckerwatte 
y  ist ein x                                ... y Sara
y mag keine $z_{2}$                               
- - - - - - 
y mag $z_{1}$

Gültige Inferenzregel

Alle Jugendlichen mögen Snus oder Zigaretten
Aleks ist ein Jugendlicher
Aleks mag keine Zigaretten
- - - - - - - 
Aleks mag Snus
### b) 
Alle Hobbits haben haarige Füße, aber Frodo hat keine haarigen Füße. Frodo ist daher sicher kein
Hobbit.

Alle x haben y                       ... x Hobbits, y haarige Füße
z hat keine y                         ... z Frodo
- - - - - - - 
z ist kein x

Gültige Inferenzegel

Alle Studenten haben Depressionen
Simon hat keine Depressionen
- - - - - - - 
Simon ist kein Student
### c) 
Alle Clowns mit einem pinken Hut haben einen Luftballon, außerdem haben alle Clowns mit einem grünen Hut eine Masche. Deshalb hat kein Clown einen Luftballon und eine Masche.


Alle x mit $y_{1}$ haben $z_{1}$                     ... x Clowns, $y_{1}$ pinkten Hut, $z_{1}$ Luftballon
Alle x mit $y_{2}$ haben $z_{2}$                     ... $y_{2}$ grünen Hut, $z_{2}$ Masche
- - - - - 
Kein x hat $z_{1}$ und $z_{2}$

Ungültige Inferenzregel

Alle Menschen mit linkem Arm haben ein linkes Auge
Alle Menschen mit rechtem Arm haben ein rechtes Auge
- - - - - - 
Kein Mensch hat ein linkes und rechtes Auge


## Aufgabe 7: Syntax der Aussagenlogik
Betrachten Sie die formale Definition der Syntax von aussagenlogischen Formeln für Variablen $V = \{A, B, C, . . . , Z\}$ aus der Vorlesung. 

### a) 
Legen Sie diese Definition exakt aus und geben Sie für jeden der folgenden Ausdrücke an ob es
sich dabei um eine syntaktisch korrekte aussagenlogische Formel handelt. Begründen Sie Ihre
Antworten!

i ) $(A ⊤ X)$
Nein, da kein Verkettung zwischen den Formeln ist
ii ) $¬¬B$
Korrekte Syntax, da $\lnot B$ eine korrekte Formel ist und $\lnot \lnot B$ daher auch eine korrekte Formel ist
iii ) $((B ∨ C) ⇔ A ⇔ D)$
Nein, da für die Formeln vor der Äquivalenz zum D Klammern fehlen
iv ) $((A ∧ B) ⊕ C)$
Nein, da $⊕$ kein vordefiniertes binäre Operationssymbol ist
v ) $(A ⇐ ¬⊥)$
Richtige Syntax da keine Fehler gemacht wurden
vi ) $∃X (X ⇒ A)$
Nein, da Quantoren nicht zugelassen sind
vii ) $¬((A ⇎ ¬B) ⇔ 0)$
Nein, da der Wert 0 nicht zugelassen ists
viii ) $((A ⇒ ¬(B ∧ C)) ∨ ¬D)$
Richtige Syntax da alles passt
ix ) $(A ⇎ B(E, F))$
Nein, da die Formel B(E,F) in dieser Form Syntaktisch nicht zugelassen ist
x ) $↑ (A ∨ B)$
Nein da vor dem Nand Operator keine Formel ist
### b) 
In der Praxis wird die Definition nicht so streng ausgelegt. Betrachten Sie die folgenden Beispiele
und erklären Sie wieso (a) diese genau genommen nicht der Definition von aussagenlogischen
Formeln entsprechen und (b) wieso das in der Praxis kein Problem ist.
i ) $A ⇎ B$
Ansich falsch da Klammern fehlen doch ist offensichtlich welche beiden Formeln durch $⇎$ verbunden werden
ii ) $(A ∨ ¬B ∨ C)$
Ansich falsch da drei verschiedene Formeln in einer Klammer verknüpft werden, doch da es sich um zwei Oder Verknpüfungen handelt ist die Semantik in allen möglichen Interpretationen von Klammersetzungen gleich
iii ) $(A ∨ (D ⇔ E) ∨ C) ∧ D ∧ ¬E$
Ansich wieder falsch aufgrund von mangelnder Klammersetzung. Doch da es sich in den einzelnen Klammern immer um das gleiche binäre Operationssymbol handelt führen verschieden Klammersetzungen wie $((A \lor(D \iff E)) \lor C)$ oder $(A \lor ((D \iff E)\lor C))$ zum gleichen semantischen Ergebnis

## Aufgabe 8: Interpretationen, Auswertung von Formeln, Logische Konsequenz
## a) 
Sei $ϕ$ die Formel $(A ∨ (B ⇒ C)) ⇎ (D ↑ E)$. Die Interpretationen $I, J$ und $K$ sind jeweils nur teil weise bekannt (d.h. sie weisen nicht jeder Variable in $ϕ$ einen Wahrheitswert zu). Lassen sich trotzdem $valI(ϕ), valJ(ϕ), valK(ϕ)$ eindeutig bestimmen? Wenn ja, was ist das Ergebnis? Wenn nein, vervollständigen Sie die Interpretation einmal so, dass die Formel zu wahr auswertet und einmal so, dass sie zu falsch auswertet.

-  Interpretation $I$ mit $I(C) = 1, I(E) = 0$
$$
(A \lor (B \implies 1)) ⇎ \lnot(D \land 0)
$$
$$
(A \lor 1) ⇎ \lnot(0)
$$
$$
1 ⇎ 1
$$
Wertet als falsch aus


-  Interpretation $J$ mit $J(B) = 1, J(D) = 0$
$$
(A \lor (1 \implies C)) ⇎ \lnot(0 \land E)
$$
$$
(A \lor (0 \lor C)) ⇎  \lnot (0)
$$
$$
(A \lor C) ⇎ 1
$$

Nicht eindeutig
$$
J(A)=0,J(C)=0
$$
$$
0 ⇎ 1
$$
Wertet als richtig aus
$$
J(A)=1
$$
$$
1 ⇎ 1
$$
Wertet als falsch aus

-  Interpretation $K$ mit $K(C) = K(D) = K(E) = 1$

$$
(A \lor (B \implies 1)) ⇎ \lnot(1 \land 1)
$$
$$
(A \lor 1) ⇎ \lnot(1)
$$
$$
1 ⇎ 0
$$
Wertet als richtig aus


Hinweis: um das Beispiel zu lösen, müssen Sie sich zuerst mit dem Begriff der Interpretation von
aussagenlogischen Formeln auseinandersetzen. Versuchen Sie für sich selbst, in einem oder zwei
Sätzen zu erklären, was eine Interpretation ist.

### b) 
Sei $ϕ$ die Formel aus der letzten Teilaufgabe. Bestimmen Sie in jedem Punkt, ob die Konsequenz-
relation gilt $(\vDash)$ oder nicht gilt $(\nvDash)$ und begründen Sie Ihr Ergebnis durch die Auswertung der
Wahrheitstabelle. Sie dürfen dabei irrelevante Fälle zusammenfassen.

• Gilt C, D, E |= ϕ ?

| A   | B   | C   | D   | E   | $B \implies C$ | $A \lor (B\implies C)$ | $\lnot(D \land E)$ | ϕ   |
| --- | --- | --- | --- | --- | -------------- | ---------------------- | ------------------ | --- |
| 0   | 0   | 1   | 1   | 1   | 1              | 1                      | 0                  | 1   |
| 0   | 1   | 1   | 1   | 1   | 1              | 1                      | 0                  | 1   |
| 1   | 0   | 1   | 1   | 1   | 1              | 1                      | 0                  | 1   |
| 1   | 1   | 1   | 1   | 1   | 1              | 1                      | 0                  | 1   |

Konsequenz gültig

• Gilt ¬A, ¬B, C, D, E |= ϕ ?

| $A$ | $B$ | $C$ | D   | E   | $B \implies C$ | $A \lor (B\implies C)$ | $\lnot(D \land E)$ | ϕ   |
| --- | --- | --- | --- | --- | -------------- | ---------------------- | ------------------ | --- |
| 0   | 0   | 1   | 1   | 1   | 1              | 1                      | 0                  | 1   |
Konsequenz gültig
 
• Gilt A ↓ B, A ⇎ B |= A ?

| A   | B   | $\lnot(A \lor B)$ | $A ⇎ B$ | $\lnot(A\lor B) \land (A ⇎ B)$ |
| --- | --- | ----------------- | ------- | ------------------------------ |
| 0   | 0   | 1                 | 0       | 0                              |
| 0   | 1   | 0                 | 1       | 0                              |
| 1   | 0   | 0                 | 1       | 0                              |
| 1   | 1   | 0                 | 0       | 0                              |
Da Prämisse immer falsch ist, ist die Konsequenz wahr also gültig


• Gilt A ⇐ B |= ¬B ?

| A   | B   | $A \impliedby B$ | $\lnot B$ |
| --- | --- | ---------------- | --------- |
| 0   | 0   | 1                | 1         |
| 0   | 1   | 0                | 0         |
| 1   | 0   | 1                | 1         |
| 1   | 1   | 1                | 0         |
Konsequenz gilt im Falle $A=1,B=1$ nicht somit ungültig
 
Hinweis: hier setzen Sie sich mit dem Begriff der logischen Konsequenz auseinander. Wie oben
ist es hilfreich, sich zuerst zu überlegen, was es bedeutet, wenn eine Formel G die Konsequenz
der Formel F ist und wie die mathematische Schreibweisen $F1, F2 \vDash G$ bzw. $F \nvDash G$ oder $\vDash G$ zu
lesen sind. Es kann auch hilfreich sein, die Rollen von Konsequenzbeziehung $\vDash$ und Implikation
$⇒$ in der Aussage $\vDash F ⇒ G$ zu vergleichen. Was passiert, wenn man versucht, den einen Operator
durch den anderen zu ersetzen?
## Aufgabe 9: Unerfüllbare, widerlegbare, erfüllbare und gültige Formeln
Bestimmen Sie für die folgenden Formeln, ob diese unerfüllbar, widerlegbar, erfüllbar und / oder gültig sind. Geben Sie im Fall von erfüllbaren / widerlegbar Formeln eine entsprechende Wahrheitsbelegung an. Geben Sie bei gültigen / unerfüllbaren Formeln an, warum es kein Beispiel / Gegenbeispiel geben kann. Sie können dazu die aus der Vorlesung bekannten Äquivalenzumformungen verwenden, um die Formel zu vereinfachen und / oder die Wahrheitstabelle skizzieren.

- a) $(A ⇒ (B ⇒ C)) ⇔ ((A ∧ B) ⇒ C)$

| A   | B   | C   | $(B ⇒ C)$ | $A⇒(B⇒ C)$ | $A \land B$ | $(A \land B) ⇒ C$ | $\iff$ |
| --- | --- | --- | --------- | ---------- | ----------- | ----------------- | ------ |
| 0   | 0   | 0   | 1         | 1          | 0           | 1                 | 1      |
| 0   | 0   | 1   | 1         | 1          | 0           | 1                 | 1      |
| 0   | 1   | 0   | 0         | 1          | 0           | 1                 | 1      |
| 0   | 1   | 1   | 1         | 1          | 0           | 1                 | 1      |
| 1   | 0   | 0   | 1         | 1          | 0           | 1                 | 1      |
| 1   | 0   | 1   | 1         | 1          | 0           | 1                 | 1      |
| 1   | 1   | 0   | 0         | 0          | 1           | 0                 | 1      |
| 1   | 1   | 1   | 1         | 1          | 1           | 1                 | 1      |

Gültig
Es kann kein Gegenbeispiel geben weil die oben skizzierte Wahrheitstabelle alle möglichen Belegungen an Wahrheitswerten abdeckt und diese beweist, dass die Formel gültig ist

- b) $(A ∨ (⊤ ⇒ C)) ⇎ (⊥ ↑ E)$
$$
( A \lor C) ⇎ ⊤
$$

| A   | C   | $A \lor C$ | $⊤$ | $( A \lor C) ⇎ ⊤$ |
| --- | --- | ---------- | --- | ----------------- |
| 0   | 0   | 0          | 1   | 1                 |
| 0   | 1   | 1          | 1   | 0                 |
| 1   | 0   | 1          | 1   | 0                 |
| 1   | 1   | 1          | 1   | 0                 |
erfüllbar mit $I(A)=0,I(C)=0$
widerlegbar mit allen anderen Interpretationen

- c) $(A ⇎ B) ⇎ C$

| A   | B   | C   | $(A⇎B)$ | $(A⇎B)⇎C$ |
| --- | --- | --- | ------- | --------- |
| 0   | 0   | 0   | 0       | 0         |
| 0   | 0   | 1   | 0       | 1         |
| 0   | 1   | 0   | 1       | 1         |
| 0   | 1   | 1   | 1       | 0         |
| 1   | 0   | 0   | 1       | 1         |
| 1   | 0   | 1   | 1       | 0         |
| 1   | 1   | 0   | 0       | 0         |
| 1   | 1   | 1   | 0       | 1         |
erfüllbar mit $I(A)=0,I(B)=0,I(C)=1$
widerlegbar mit $I(A)=0,I(B)=0,I(C)=0$

- d) $(A ⇎ B) ⇎ (B ⇎ A)$

| A   | B   | $A⇎B$ | $B⇎A$ | $(A⇎B)⇎(B⇎A)$ |
| --- | --- | ----- | ----- | ------------- |
| 0   | 0   | 0     | 0     | 0             |
| 0   | 1   | 1     | 1     | 0             |
| 1   | 0   | 1     | 1     | 0             |
| 1   | 1   | 0     | 0     | 0             |
unerfüllbar da $A⇎B$ und $B⇎A$ semantisch die exakt gleichen Formeln sind und somit keine Belegung entsteht in denen diese Formeln einen unterschiedlichen Wert haben

- e) $(A_{1} ∧ . . . ∧ An) ∧ (¬A_{1} ∨ . . . ∨ ¬An) \text{ mit } n ≥ 1.$

| A        |         | $A_{n}$ | $\lnot A$ |         | $\lnot A_{n}$ | $(A_{1}\dots A_{n})\land(\lnot A_{1} \lor \lnot)$ |
| -------- | ------- | ------- | --------- | ------- | ------------- | ------------------------------------------------- |
| 0        | $\dots$ | 0       | 1         | $\dots$ | 1             | 0                                                 |
| $\vdots$ |         |         | $\vdots$  |         |               | 0                                                 |
| $\vdots$ |         |         | $\vdots$  |         |               | 0                                                 |
| 1        |         | 1       | 0         |         | 0             | 0                                                 |
In der einzigen Belegung in der alle nicht negierten A zusammen mit und verknüpft 1 ergeben ist der Fall in denen mit oder verknüpften negierten A 0 ergeben.

unerfüllbar