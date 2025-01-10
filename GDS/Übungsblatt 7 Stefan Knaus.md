## Aufgabe 1: Unterschiedliche Arten von Automaten
Betrachten Sie die Definitionen der verschiedenen Automatentypen aus der Vorlesung.
### a) 
Kreuzen Sie in folgender Tabelle jene Automaten an, für die die jeweilige Aussage zutrifft. Überlegen Sie sich dazu jeweils eine Begründung, diese muss in der Übung erörtert werden können. 
![[Pasted image 20250110153229.png]]
### b) 
Betrachten Sie folgende grafische Darstellung von Automaten, analysieren Sie die Eigenschaften,
und überlegen Sie, um welche Arten von Automaten es sich jeweils handeln könnte. Geben Sie alle möglichen Arten von Automaten an und begründen Sie wieso Sie die anderen Arten ausschließen können.

![[Pasted image 20250110152040.png]]

#### 1
DEA: ja
NEA: ja
Transducer: nein, da gezeigter Automat keine Ausgabe hat
Mealy: nein, da gezeigter Automat keine Ausgabe hat
Moore: nein, da gezeigter Automat keine Ausgabe hat
D. Büchi: ja
N. Büchi: ja

#### 2
DEA: nein, da gezeigter Automat eine Ausgabe hat
NEA: nein, da gezeigter Automat eine Ausgabe hat
Transducer: nein, da gezeigter Automat keine Endzustände hat
Mealy: nein, da gezeigter Automat nicht deterministisch ist (mehrere Wege mit gleichem Input)
Moore: nein, da gezeigter Automat nicht deterministisch ist (mehrere Wege mit gleichem Input)
D. Büchi: nein, da gezeigter Automat eine Ausgabe hat
N. Büchi: nein, da gezeigter Automat eine Ausgabe hat

## Aufgabe 2: Unterschiedliche Arten von Automaten
Wir betrachten ein Kartenspiel mit zwei Personen A und B, bei dem mehrere Runden gespielt wer-
den. Beide starten mit 3 Punkten. In jeder Runde kann eine der beiden Personen gewinnen und dabei ihre Punkte um eins oder zwei reduzieren. Oder es gibt ein Unentschieden und die Punkte bleiben unverändert. Fallen die Punkte einer Person auf Null oder darunter, gewinnt sie das Spiel.

### a) 
Modellieren Sie die möglichen Spielabläufe als Automat. Es soll anhand der Zustände erkennbar
sein, wer bei einem Ablauf gewonnen hat. Sie müssen sich hier noch nicht für einen konkreten
Automatentyp entscheiden.

|      | AB-0 | $A-1$ | $A-2$ | $B-1$ | $B-2$ |
| ---- | ---- | ----- | ----- | ----- | ----- |
| sz   | sz   | A2    | A1    | B2    | B1    |
| A2   | A2   | A1    | Aez   | A2B2  | A2B1  |
| A1   | A1   | Aez   | Aez   | A1B2  | A1B1  |
| B2   | B2   | A2B2  | A1B2  | B1    | Bez   |
| B1   | B1   | A2B1  | A1B1  | Bez   | Ber   |
| A1B1 | A1B1 | Aez   | Aez   | Bez   | Bez   |
| A1B2 | A1B2 | Aez   | Aez   | A1B1  | Bez   |
| A2B1 | A2B1 | A1B1  | Aez   | Bez   | Bez   |
| A2B2 | A2B2 | A1B2  | Aez   | A2B1  | Bez   |
| Aez  |      |       |       |       |       |
| Bez  |      |       |       |       |       |
Startzustände: $\{ sz \}$
Endzustände: $\{ Aez,Bez \}$
### b) 
Vervollständigen Sie Ihren Automaten aus der vorigen Teilaufgabe zu einem DEA, sodass die
Abläufe des Spiels, bei denen Person A gewinnt, die Sprache des Automaten bilden.

|      | AB-0 | $A-1$ | $A-2$ | $B-1$ | $B-2$ |
| ---- | ---- | ----- | ----- | ----- | ----- |
| sz   | sz   | A2    | A1    | B2    | B1    |
| A2   | A2   | A1    | Aez   | A2B2  | A2B1  |
| A1   | A1   | Aez   | Aez   | A1B2  | A1B1  |
| B2   | B2   | A2B2  | A1B2  | B1    |       |
| B1   | B1   | A2B1  | A1B1  |       |       |
| A1B1 | A1B1 | Aez   | Aez   |       |       |
| A1B2 | A1B2 | Aez   | Aez   | A1B1  |       |
| A2B1 | A2B1 | A1B1  | Aez   |       |       |
| A2B2 | A2B2 | A1B2  | Aez   | A2B1  |       |
| Aez  |      |       |       |       |       |

Startzustände: $\{ sz \}$
Endzustände: $\{ Aez \}$
### c) 
Vervollständigen Sie Ihren Automaten aus der ersten Teilaufgabe zu einem geeigneten Automaten, sodass es nach jeder Runde eine Ausgabe gibt. Nach einer Runde in der Person A (bzw. Person B) das Spiel gewonnen hat, soll der Automat win A (bzw. win B) ausgeben.

|      | AB-0                    | $A-1$                   | $A-2$                   | $B-1$                    | $B-2$                   |
| ---- | ----------------------- | ----------------------- | ----------------------- | ------------------------ | ----------------------- |
| sz   | $\{ (Draw, sz) \}$      | $\{ (A ~Win,A 2) \}$    | $\{ (A ~Win,A 1) \}$    | $\{ (B ~Win,B 2) \}$     | $\{ (B ~Win,B 1) \}$    |
| A2   | $\{ (Draw, A 2) \}$     | $\{ (A ~Win,A 1) \}$    | $\{ (A~Win,Aez) \}$     | $\{ (B~Win, A 2 B 2) \}$ | $\{ (B~Win,A 2 B 1) \}$ |
| A1   | $\{ (Draw, A 1) \}$     | $\{ (A~Win,Aez) \}$     | $\{ (A~Win,Aez) \}$     | $\{ (B~Win,A 1 B 2) \}$  | $\{ (B~Win,A 1 B 1) \}$ |
| B2   | $\{ (Draw, B 2) \}$     | $\{ (A~win,A 2 B 2) \}$ | $\{ (A~Win,A 1 B 2) \}$ | $\{ (B ~Win,B 1) \}$     | $\{ (B~Win,Bez) \}$     |
| B1   | $\{ (Draw, B 1) \}$     | $\{ (A~Win,A 2 B 1) \}$ | $\{ (A~Win,A 1 B 1) \}$ | $\{ (B~Win,Bez) \}$      | $\{ (B~Win,Bez) \}$     |
| A1B1 | $\{ (Draw, A 1 B 1) \}$ | $\{ (A~Win,Aez) \}$     | $\{ (A~Win,Aez) \}$     | $\{ (B~Win,Bez) \}$      | $\{ (B~Win,Bez) \}$     |
| A1B2 | $\{ (Draw, A 1 B 2) \}$ | $\{ (A~Win,Aez) \}$     | $\{ (A~Win,Aez) \}$     | $\{ (B~Win,A 1 B 1) \}$  | $\{ (B~Win,Bez) \}$     |
| A2B1 | $\{ (Draw, A 2 B 1) \}$ | $\{ (A~Win,A 1 B 1) \}$ | $\{ (A~Win,Aez) \}$     | $\{ (B~Win,Bez) \}$      | $\{ (B~Win,Bez) \}$     |
| A2B2 | $\{ (Draw, A 2 B 2) \}$ | $\{ (A~Win,A 1 B 2) \}$ | $\{ (A~Win,Aez) \}$     | $\{ (B~Win,A 2 B 1) \}$  | $\{ (B~Win,Bez) \}$     |
| Aez  |                         |                         |                         |                          |                         |
| Bez  |                         |                         |                         |                          |                         |
Startzustände: $\{ sz \}$
Endzustände: $\{ Aez,Bez \}$
### d) 
Betrachten Sie den Fall, bei dem nach dem Ende eines Spiels sofort ein neues anfängt. Vervollständigen Sie Ihren Automaten aus der ersten Teilaufgabe, sodass er jene unendlichen Spielabläufe akzeptiert, bei denen B immer wieder einmal gewinnt, d.h., es gibt keine Spielrunde, ab der nur mehr A gewinnt.

|      | AB-0 | $A-1$ | $A-2$ | $B-1$ | $B-2$ |
| ---- | ---- | ----- | ----- | ----- | ----- |
| sz   | sz   | A2    | A1    | B2    | B1    |
| A2   | A2   | A1    | Aez   | A2B2  | A2B1  |
| A1   | A1   | Aez   | Aez   | A1B2  | A1B1  |
| B2   | B2   | A2B2  | A1B2  | B1    | Bez   |
| B1   | B1   | A2B1  | A1B1  | Bez   | Ber   |
| A1B1 | A1B1 | Aez   | Aez   | Bez   | Bez   |
| A1B2 | A1B2 | Aez   | Aez   | A1B1  | Bez   |
| A2B1 | A2B1 | A1B1  | Aez   | Bez   | Bez   |
| A2B2 | A2B2 | A1B2  | Aez   | A2B1  | Bez   |
| Aez  | sz   | A2    | A1    | B2    | B1    |
| Bez  | sz   | A2    | A1    | B2    | B1    |
Startzustände: $\{ sz \}$
Endzustände: $\{ Bez \}$

Hinweis: Überlegen Sie sich, ob hier die tabellarische oder die grafische Darstellung besser geeignet ist.


## Aufgabe 3: Modellieren mit Moore- und Mealy-Automaten
Wir betrachten eine Texteingabe, die Groß- und Kleinbuchstaben sowie die Zeichen -, ., ␣ enthalten
kann. Entwerfen Sie Automaten, die so eine Texteingabe verarbeiten und anzeigen, wenn eines der
beiden Wörter Moore-A, Mealy-A gefunden wird.

### a) 
Entwerfen Sie zunächst einen Moore-Automat, der jedes Vorkommen von Moore-A im Text mit
der Ausgabe :) anzeigt und jedes Vorkommen von Mealy-A mit der Ausgabe :( anzeigt.

![[Pasted image 20250110165252.png]]



### b) 
Entwerfen Sie jetzt einen Mealy-Automat, der jedes Vorkommen von Mealy-A mit der Ausgabe
:) anzeigt und jedes Vorkommen von Moore-A mit der Ausgabe :( anzeigt. Versuchen Sie hier im
Vergleich zu Ihrem Moore-Automaten Zustände einzusparen.


Stellen Sie beide Automaten grafisch dar und geben Sie auch die jeweiligen Tupel mit den Tabellen für $δ$ und $γ$ an! Illustrieren Sie die Funktionsweise Ihrer Automaten indem Sie eine geeignete Eingabe $w$ auswählen und für beide Automaten $δ∗(q_{0}, w)$ und $γ∗(q_{0}, w)$ berechnen.

## Aufgabe 4: Büchi-Automat
Betrachten Sie die Definitionen von deterministischen/nichtdeterministischen Büchi-Automaten aus
der Vorlesung.


### a) 
Geben Sie zu den folgenden nichtdeterministischen B¨uchi-Automaten an, welche Sprache L(A)
diese jeweils akzeptieren.
• A1
q1 q2 q3 q4
d,g,s
g d s
g
d,g,s
• A2
q1 q2 q3 q4
g d s
d,g,s
• A3
q1 q2
q3
q4
q5
q6
©
§
x,y
x,y
©
©x,y
©
§
b) Wandeln Sie den grafisch dargestellten, nichtdeterministische B¨uchi-Automaten An naiv mit dem
in der Vorlesung f¨ur NEA/DEA vorgestellten Verfahren der Potenzmengenkonstruktion in einen
deterministischen Automaten Ad um. Vergleichen Sie nun die von An und Ad akzeptierten Spra-
chen. Was k¨onnen Sie feststellen?
q1 q2
©, §
§
©


## Aufgabe 5: Syntax der Prädikatenlogik

### (a) 
 Betrachten Sie eine Signatur bestehend aus einem zweistelligen Funktionssymbol f/2, einem einstelligen Funktionssymbol g/1, zwei Konstantensymbolen o/0 und p/0, zwei zweistelligen Prädikatensymbolen P/2 und Q/2, einem einstelligen Prädikatensymbol R/1 sowie die Variablen $x, y, z.$

#### (1) 
Entscheiden Sie, ob die folgenden Zeichenketten syntaktisch korrekte prädikatenlogische Formeln darstellen und begründen Sie Ihre Aussage.

 -  (i) $∀x (P(g(f(x, x)), o) ⇒ ∃x R(x))$
richtig
- (ii) $∀x (⊤ ⇒ ∃y (f(x, y) ⇔ ¬R(y)))$
Funktion f wird mit Prädikat R verglichen
- (iii) $∃y ∀z ((Q(y, p) ⇎ R(f(g(z), z))) ⇒ Q(y, ¬z))$
richtig
- (iv) $(∃x ∃z Q(x, z) ∧ (¬P(x, f(p, g(x))) ⇎ (∃z R(z) ∨ ∀xP(x, y))))$
richtig
- (v) $∀x ∀y ((P(x, y) ∧ Q(y, x)) ⇒ (R(f(x, y)) ∨ x = y))$
= nicht definiert
- (vi) $(P(g(f(o, g(p))), o) ∧ ¬∀x ∀y (R(f(x, g(y))) ⇔ R(P(x, g(y)))))$
Prädikat P in Prädikat R nicht korrekt
#### (2) 
Überlegen Sie, welche Terme hier gebildet werden können. Welche Teile der Angabe sind
hierfür relevant? Geben Sie mindestens 5 verschiedene gültige Terme an und versuchen Sie
dabei alle Möglichkeiten Terme zu bilden zu verwenden.

$$
o
$$
$$
g(o)
$$
$$
f(o,p)
$$
$$
f(g(p),o)
$$
$$
f(g(o),g(p))
$$

#### (3) 
Wie viele syntaktisch korrekte Formeln können ohne Verwendung der Funktionssymbole f
und g gebildet werden, die keinen einzigen Operator (kein ¬, ∧, ↑, ∨, ↓, ⇔, ⇎, ⇒, ⇐) enthalten?
$$
R(o),R(p),R(x),R(y),R(z),P(o,p),P(o,x),P(o,y),P(o,z),\dots,Q\dots
$$
$$
5+4*5*2=25
$$
mit $\forall,\exists$
$+2*(12*3)+2*3*2*4=76+48=124+25=149$
### (b) 
Betrachten Sie folgende (syntaktisch korrekte) prädikatenlogische Formel. Identifizieren Sie die
Prädikatensymbole, Funktionssymbole (inkl. Konstanten) und Variablen. Ignorieren Sie dabei die
Konventionen aus der Vorlesung zur Schreibweise der entsprechenden Symbole. Kann ein Symbol nicht eindeutig einer dieser Gruppen zugeordnet werden, so geben Sie alle Möglichkeiten
an.

$$∃x ∀P (k(S, P) ∨ (U(y(P, z), x) ⇐ ∀a (f(x) ∧ k(a, g(P))))))$$
$$
V=x,P,a,S,z
$$
$$
P=k,U,f
$$
$$
F=S,y,z,g
$$

## Aufgabe 6: Quantoren
In dieser Aufgabe beschäftigen wir uns mit Interpretation in der Prädiaktenlogik, den dazugehörigen Funktionen $val_{I}$, und Quantoren.


### (a) 
Gegeben ist die prädikatenlogische Formel über der Variablen $x$, dem Konstantensymbol k, dem
einstelligen Funktionssymbol f/1, den einstelligen Prädikatensymbolen R und S sowie dem zwei-
stelligen Prädikatensymbol T.

$$(
∃x
(
R(x) ⇒ T(f(x), x)
)
∧ ∀x
(
S(x) ∨ ¬T(x, k)
))$$

Überprüfen Sie, ob die Interpretation I ein Modell dieser Formel ist. Seien Sie darauf vorbereitet,
die Auswertung der Formel Schritt für Schritt zu erklären/abzuleiten.

$$U = \{1, 2, 3\}$$
$$I(k) = 2$$
$$I(f) : I(f)(1) = 2, I(f)(2) = 1, I(f)(3) = 2$$
$$I(R) = \{1, 2, 3\} $$
$$I(S) = {1}$$ $$I(T) = \{(1, 2), (1, 3), (3, 1), (3, 3)\}$$
### (b) 
Betrachten Sie die beiden prädikatenlogischen Formeln

- (i) $∀x ∃y (R(x) ∨ T(x, y))$ 
- (ii) $∃y ∀x (R(x) ∨ T(x, y))$

über der selben Signatur wie in Aufgabe (a). Geben Sie eine Interpretation I über dem Wertebereich $U = \{1, 2, 3\}$ an welche ein Modell für (i), jedoch nicht für (ii) ist.
### (c) 
Gegeben sind die prädikatenlogischen Formeln über der Variablen x, den Konstantensymbolen
jon/0, rot/0 sowie den Prädikatensymbolen Stift/1, dabei/2 und schreibt/2.
#### (1) 
$$¬∃x
((Stift(x) ∧ dabei(jon, x)) ∧ ¬schreibt(x, rot)
)$$
#### (2) 
$$¬∃x
((Stift(x) ∧ dabei(jon, x)) ⇒ ¬schreibt(x, rot)
)$$
- (i) Überprüfen Sie für beide Formeln, ob die folgende Interpretation ein Modell der Formel ist.
$$U = {Arya, Jon, Kuli, Marker, Rot, Grün}$$
$$I(jon) = Arya$$
$$I(rot) = Rot$$
$$I(Stift) = {Kuli, Marker}$$
$$I(dabei) = {(Jon, Kuli), (Arya, Marker)}$$
$$I(schreibt) = {(Marker, Rot), (Kuli, Grün)}$$
- (ii) Geben Sie für jede Formel, für die die Interpretation kein Modell ist, eine Erweiterung der
Interpretation an, so dass die Erweiterung ein Modell der Formel darstellt.

## Aufgabe 7: Prädikatenlogik: Prädikaten- / Funktionssymbole finden
Gegeben sind zwei Beschreibungen von Situationen und jeweils ein dazu passender Wertebereich $U$.

- (i) Jessica und Paul sind Gäste eines Hotels und befinden sich jeweils in ihrem Zimmer. Beide Zimmer haben keinen Wasseranschluss, auch wenn es im Hotel Zimmer mit Wasseranschluss gibt. Jessicas Zimmer befindet sich im Haupthaus, Pauls Zimmer im Poolhaus. Beide bevorzugen jeweils das Gebäude, in dem ihre Zimmer liegen über das andere Gebäude. $U = \{Jessica, Paul, Room101, Room102, Room301, Room404, Haupthaus, Poolhaus\}$

- (ii) James ist auch in seinem Zimmer. Sein Zimmer hat einen Wasseranschluss und ist eine Suite im Haupthaus. James bevorzugt das Poolhaus über das Haupthaus, aber das Bergchateaux über die beiden anderen Gebäude. Er bestellt ein Omelette in sein Zimmer und Champagner in ein anderes Zimmer. Er bevorzugt Champagner über Omelette. $U = \{James, Room007, Room701, Room702, Haupthaus, Poolhaus, Bergchateaux, Omelette, Champagner\}$

Führen Sie folgende Schritte durch:

- a) Stellen Sie fest, welche Teile der Beschreibungen Sie mittels Prädikaten darstellen können. Geben Sie für die beiden Beschreibungen eine gemeinsame Menge an Prädikaten an, welche die identifizierten Teile beschreiben. Geben Sie jeweils passende Namen mit Aritäten an und legen Sie die Bedeutung des Prädikats bzw. der Funktion fest. Geben Sie gegebenenfalls auch die Bedeutung der Argumente an. Stellen Sie anschließend jede der beiden Beschreibungen so gut wie möglich als Modell für diese Prädikate über dem jeweiligen Wertebereich $U$ dar. Wählen Sie die nötige Interpretation I entsprechend der intuitiven Bedeutung der Elemente in $U$ (d.h. das Element Jessica soll z.B. nicht die Rolle eines Zimmers einnehmen).

$$
P=\{ Gast / 1, InZimmer / 2,Gebäude / 1,Wasseranschluss / 1,BestelltIn / 3,Bevorzugt / 3,InGebäude / 2 \}
$$

$$
Gast(x)\dots\text{x ist Gast im Hotel}
$$
$$
InZimmer(x,y)\dots\text{Gast x ist im Zimmer y}
$$
$$
Gebäude(x)\dots \text{x ist ein Gebäude}
$$
$$
Wasseranschluss(x)\dots \text{Zimmer x hat einen Wasseranschluss}
$$
$$
BestelltIn(x,y,z)\dots\text{Gast x bestellt Lebensmittel y in Zimmer z}
$$
$$
Bevorzugt(x,y,z)\dots\text{Gast x bevorzugt Objekt y über Objekt z}
$$
$$
InGebäude(x,y)\dots\text{Zimmer x ist im Gebäude y}
$$
$$
I(Gast)=\{ Jessica,Paul \}
$$
$$
I(InZimmer)=\{ (Jessica,Room101),(Paul,Room404) \}
$$
$$
I(Gebäude)=\{ Haupthaus,Poolhaus \}
$$
$$
I(Wasseranschluss)=\{ Room102,Room301 \}
$$
$$
I(Bevorzugt)=\{ (Jessica,Haupthaus,Poolhaus),(Paul,Poolhaus,Haupthaus) \}
$$
$$
I(InGebäude)=\{ (Room 101,Haupthaus),(Room 404, Poolhaus) \}
$$

$$
I(Gast)=James
$$
$$
I(InZimmer)=\{ (James,Room 007) \}
$$
$$
I(Gebäude)=\{ Haupthaus \}
$$
$$
I(Wasseranschluss)=\{ Room 007 \}
$$
$$
I(InGebäude) = \{( Room 007, Haupthaus) \}
$$
$$
I(Bevorzugt)=\{ (James,Poolhaus,Haupthaus),(James,Bergchateaux,Poolhaus),$$$$(James,Bergchateaux,Haupthaus),(James,Champagner,Omelette) \}
$$
$$
I(BestelltIn)=\{ (James,Omelette,Room 007),(James,Champagner, Room 702) \}
$$
- b) Überlegen Sie sich, welche der Prädikate auch durch Funktionen ausgedrückt hätten werden können. Identifizieren Sie mindestens ein solches Prädikat, ersetzen Sie es durch eine Funktion, und passen Sie die Modelle welche die beiden Beschreibungen abbilden entsprechend an. Finden Sie anschließend eine Möglichkeit die Beschreibungen so mittels Prädikaten und Funktionen darzustellen, dass Sie die Aussage Das Objekt, in dem sich der Raum befindet, in dem sich Jessica befindet, hat einen Wasseranschluss mittels einer Atomformel unter Verwendung eine passenden Konstante für Jessica darstellen können.


$$
zimmer(x)/1\dots \text{Gast x befindet sich im Zimmer ...}
$$
$$
gebäude(x)/1 \dots \text{Zimmer x befindet sich im Gebäude ....}
$$
$$
I(zimmer)=\{ (Jessica,Room 101),(Paul,Room 404),(James, Room007) \}
$$
$$
I(gebäude)=\{(Room 101,Haupthaus),(Room 404,Poolhaus), (Room 007,Haupthaus) \}
$$
$$
I(jessica)=Jessica
$$
$$
Wasseranschluss(zimmer(jessica))
$$
## Aufgabe 8: Modellieren mit PL

Gegeben seien folgende Prädikate und Funktionen:

Gewässer(x) . . . x ist ein Gewässer 
Badewanne(x) . . . x ist eine Badewanne
Fisch(x) . . . x ist ein Fisch 
Schwimmt(x, y) . . . x schwimmt in y
Boot(x) . . . x ist ein Boot 
Kanal(x,y) . . . es gibt einen Kanal von x nach y
Nass(x) . . . x ist nass 
mündet(x) . . . gibt zurück, worin x mündet

### (a) 
Übersetzen Sie die folgenden Formeln in deutsche Sätze.

- (i) $∀x((Fisch(x) ∧ Nass(x)) ⇒ ∃y Schwimmt(x, y))$

Alle nassen Fische schwimmen

- (ii) $∀x∀y ((Nass(y) ∧ Schwimmt(x, y)) ⇒ Nass(x))$

Alles, dass in etwas nassem schwimmt, ist nass

- (iii) $∀x∀y∀z((Schwimmt(x, y) ∧ Schwimmt(x, z) ∧ Boot(x)) ⇒ Kanal(y, z))$

Wenn Boote in einer und einer anderen Substanz schwimmen, dann gibt es einen Kanal zwischen den beiden Substanzen.
### (b) 
Schreiben Sie folgende deutsche Sätze (auch wenn sie faktisch falsch sein mögen) als prädikatenlogische Formeln unter Verwendung der obigen Prädikate, Funktionen und Konstanten:

- (i) Es gibt trockene (= nicht nasse) Badewannen.

$$
\exists x(Badewanne(x)\land \lnot Nass(x))
$$

- (ii) Alle Badewannen sind Gewässer.

$$
\forall x(Badewanne(x)\implies Gewässer(x))
$$

- (iii) Alles, was in einem Gewässer schwimmt, ist nass.

$$
\forall x\exists y((Schwimmt(x,y)\land Gewässer)\implies Nass(x))
$$

- (iv) Nur Fische und Boote schwimmen in Gewässern.

$$
\forall x\exists y((Schwimmt(x,y)\land Gewässer(y)) \implies (Fisch(x) \lor Boot(x)))
$$

- (v) Kein Gewässer mündet in eine Badewanne.

$$
\forall x\lnot(Gewässer(x)\land Badewanne(mündet(x)))
$$

## Aufgabe 9: Modellieren mit PL
Übersetzen Sie die folgenden deutschen Sätze in prädikatenlogische Formeln und geben Sie jeweils ein Modell über dem Wertebereich $U$ an. Geben Sie auch die Bedeutung der von Ihnen verwendeten Prädikate und Funktionen an. Hinweis: Sie können davon ausgehen, dass alle Objekte Menschen sind. Sie müssen das in Ihren Formeln also nicht gesondert überprüfen.

### a) 
Es gibt Hexen und Zauberer.
$U = \{Mim, Merlin, Ursula\}$

$$
P=Hexe/1,Zauberer/1
$$
$$
Hexe\dots \text{ist eine Hexe}, Zauberer \dots \text{ist ein Zauberer}
$$
$$
\exists x Hexe(x) \land \exists y Zauberer(y)
$$
$$I(Hexen)=\{ Mim,Ursula \}$$
$$I(Zauberer)=Merlin$$

### b)
Hexen und Zauberer sind Fantasiewesen.
$U = \{Bibi, Gandalf, Bigfoot, Sabrina\}$

$$
P=Fantasiewesen/1
$$
$$
Fantasiewesen\dots\text{ist ein Fantasiewesen}
$$
$$
\forall x((Hexe(x) \lor Zauberer(x)) \implies Fantasiewesen(x))
$$
$$
I(Hexen)=\{ Bifi,Sabrina \}
$$
$$
I(Zauberer)=\{ G an dalf,Bigfoot \}
$$
$$
I(Fantasiewesen)=\{Bibi, Gandalf, Bigfoot, Sabrina\}
$$

### c) 
Oberhexen sind jene Hexen, die Zauberer für sich arbeiten lassen.
$U = \{Harry, Ron, Hermine, Morgana\}$

$$
P=Oberhexen/1, ArbeitenLassen/2
$$
$$
Oberhexen\dots\text{ist eine Oberhexe}, ArbeitenLassen\dots \text{x lässt y für sich arbeiten}
$$
$$
\forall x((Hexe(x) \land \exists y(Zauberer(y)\land ArbeitenLassen(x,y)) ) \implies Oberhexe(x) )
$$
$$
I(Zauberer)=\{ Harry,Ron \}
$$
$$
I(Hexe)=\{ Hermine,Morgana \}
$$
$$
I(Oberhexe)=\{ Morgana \}
$$
$$
I(ArbeitenLassen)=\{ (Morgana,Ron) \}
$$
### d) 
Es gibt Zauberer die für jemanden arbeiten, obwohl niemand für sie arbeitet.
$U = \{Mim, Paige, Radagast, Ursula\}$

$$
\exists x \exists y(Zauberer(x)\land ArbeitenLassen(y,x)\land \forall z \lnot ArbeitenLassen(x,z))
$$
$$
I(Zauberer)=\{ Mim,Paige,Radagast,Ursula \}
$$
$$
I(ArbeitenLassen)=\{ (Mim,Paige) \}
$$
