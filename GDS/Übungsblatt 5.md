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

$$
(\lnot a \land b \land c \land d) \lor (a \land \lnot b \land c \land d) \lor(a \land b \land \lnot c \land d) \lor (a \land b \land c \land \lnot d) \lor (a \land b \land c \land d)
$$
$$
\lnot(\lnot(\lnot a \land b \land c \land d)\land \lnot(a \land \lnot b \land c \land d)\land \lnot(a \land b \land \lnot c \land d) \land \lnot(a \land b \land c \land \lnot d)\land \lnot(a \land b \land c \land d))
$$
$$
\lnot(\lnot(\lnot (a \land a) \land b \land c \land d)\land \lnot(a \land \lnot (b \land b) \land c \land d)\land \lnot(a \land b \land \lnot (c \land c)\land d) \land \lnot(a \land b \land c \land \lnot (d\land d))\land \lnot(a \land b \land c \land d))
$$

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
### b) 
Alle Hobbits haben haarige Füße, aber Frodo hat keine haarigen Füße. Frodo ist daher sicher kein
Hobbit.


Wahr
### c) 
Alle Clowns mit einem pinken Hut haben einen Luftballon, außerdem haben alle Clowns mit einem grünen Hut eine Masche. Deshalb hat kein Clown einen Luftballon und eine Masche.

Falsch
## Aufgabe 7: Syntax der Aussagenlogik
Betrachten Sie die formale Definition der Syntax von aussagenlogischen Formeln für Variablen $V = \{A, B, C, . . . , Z\}$ aus der Vorlesung. 

### a) 
Legen Sie diese Definition exakt aus und geben Sie für jeden der folgenden Ausdrücke an ob es
sich dabei um eine syntaktisch korrekte aussagenlogische Formel handelt. Begründen Sie Ihre
Antworten!

i ) $(A ⊤ X)$
ii ) $¬¬B$
iii ) $((B ∨ C) ⇔ A ⇔ D)$
iv ) $((A ∧ B) ⊕ C)$
v ) $(A ⇐ ¬⊥)$
vi ) $∃X (X ⇒ A)$
vii ) $¬((A ⇎ ¬B) ⇔ 0)$
viii ) $((A ⇒ ¬(B ∧ C)) ∨ ¬D)$
ix ) $(A ⇎ B(E, F))$
x ) $↑ (A ∨ B)$
### b) 
In der Praxis wird die Definition nicht so streng ausgelegt. Betrachten Sie die folgenden Beispiele
und erklären Sie wieso (a) diese genau genommen nicht der Definition von aussagenlogischen
Formeln entsprechen und (b) wieso das in der Praxis kein Problem ist.
i ) $A ⇎ B$
ii ) $(A ∨ ¬B ∨ C)$
iii ) $(A ∨ (D ⇔ E) ∨ C) ∧ D ∧ ¬E$

## Aufgabe 8: Interpretationen, Auswertung von Formeln, Logische Konsequenz
## a) 
Sei $ϕ$ die Formel $(A ∨ (B ⇒ C)) ⇎ (D ↑ E)$. Die Interpretationen $I, J$ und $K$ sind jeweils nur teil weise bekannt (d.h. sie weisen nicht jeder Variable in $ϕ$ einen Wahrheitswert zu). Lassen sich trotzdem $valI(ϕ), valJ(ϕ), valK(ϕ)$ eindeutig bestimmen? Wenn ja, was ist das Ergebnis? Wenn nein, vervollständigen Sie die Interpretation einmal so, dass die Formel zu wahr auswertet und einmal so, dass sie zu falsch auswertet.

-  Interpretation $I$ mit $I(C) = 1, I(E) = 0$
-  Interpretation $J$ mit $J(B) = 1, J(D) = 0$
-  Interpretation $K$ mit $K(C) = K(D) = K(E) = 1$

Hinweis: um das Beispiel zu lösen, müssen Sie sich zuerst mit dem Begriff der Interpretation von
aussagenlogischen Formeln auseinandersetzen. Versuchen Sie für sich selbst, in einem oder zwei
Sätzen zu erklären, was eine Interpretation ist.

### b) 
Sei $ϕ$ die Formel aus der letzten Teilaufgabe. Bestimmen Sie in jedem Punkt, ob die Konsequenz-
relation gilt $(|=)$ oder nicht gilt $(̸|=)$ und begründen Sie Ihr Ergebnis durch die Auswertung der
Wahrheitstabelle. Sie dürfen dabei irrelevante Fälle zusammenfassen.

• Gilt C, D, E |= ϕ ?
• Gilt ¬A, ¬B, C, D, E |= ϕ ?
• Gilt A ↓ B, A ⇎ B |= A ?
• Gilt A ⇐ B |= ¬B ?

Hinweis: hier setzen Sie sich mit dem Begriff der logischen Konsequenz auseinander. Wie oben
ist es hilfreich, sich zuerst zu überlegen, was es bedeutet, wenn eine Formel G die Konsequenz
der Formel F ist und wie die mathematische Schreibweisen $F1, F2 \vDash G$ bzw. $F \nvDash G$ oder $\vDash G$ zu
lesen sind. Es kann auch hilfreich sein, die Rollen von Konsequenzbeziehung $\vDash$ und Implikation
$⇒$ in der Aussage $\vDash F ⇒ G$ zu vergleichen. Was passiert, wenn man versucht, den einen Operator
durch den anderen zu ersetzen?
## Aufgabe 9: Unerfüllbare, widerlegbare, erfüllbare und gültige Formeln
Bestimmen Sie für die folgenden Formeln, ob diese unerfüllbar, widerlegbar, erfüllbar und / oder gültig sind. Geben Sie im Fall von erfüllbaren / widerlegbar Formeln eine entsprechende Wahrheitsbelegung an. Geben Sie bei gültigen / unerfüllbaren Formeln an, warum es kein Beispiel / Gegenbeispiel geben kann. Sie können dazu die aus der Vorlesung bekannten Äquivalenzumformungen verwenden, um die Formel zu vereinfachen und / oder die Wahrheitstabelle skizzieren.

- a) $(A ⇒ (B ⇒ C)) ⇔ ((A ∧ B) ⇒ C)$
- b) $(A ∨ (⊤ ⇒ C)) ⇎ (⊥ ↑ E)$
- c) $(A ⇎ B) ⇎ C$
- d) $(A ⇎ B) ⇎ (B ⇎ A)$
- e) $(A1 ∧ . . . ∧ An) ∧ (¬A1 ∨ . . . ∨ ¬An) mit n ≥ 1.$