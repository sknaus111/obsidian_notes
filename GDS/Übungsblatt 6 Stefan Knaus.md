## Aufgabe 1: Aussagenlogik
Analysieren Sie die folgenden Sätze und identifizieren Sie ihre logische Struktur sowie die Elementaraussagen.

- (1) Wir haben den Baum umgeschnitten, weil er nicht mehr gesund war.

$$
\lnot x \implies y~~~~~x\dots \text{Baum gesund }~~~y\dots\text{Baum umschneiden}
$$

- (2) Fischers Fritz fischt frische Fische.

$$
x \implies y ~~~~~~x\dots\text{Fischer Fritz heißen}~~~~y\dots\text{frische Fische fischen}
$$

- (3) Obelix jagt entweder gerade Wildschweine oder er rauft mit Römern.

$$
x \nLeftrightarrow y ~~~~~x\dots\text{Obelix jagt Wildschweine}~~~y\dots\text{Obelix rauft mit Römern}
$$

- (4) Bring kein Eis oder Schokolade mit!

$$\lnot(x \lor y)~~~~~x\dots\text{Eis mitbringen}~~~y\dots\text{Schockolade mitbringen}$$

- (5) Mama und Papa können nur beide mitgehen, wenn es eine Familienermäßigung gibt, sonst muss einer von ihnen zu Hause bleiben.

$$
\lnot f \implies (m \nLeftrightarrow p) ~~~~~f\dots\text{gibt eine Familienermäßigung }~~~m\dots\text{Mama geht mit}~~~~p\dots\text{Papa geht mit}
$$

- (6) Wenn du Informatik studierst, musst du GDS machen, aber du musst es nicht lieben.


$$
(s \implies g) \land (\bot \implies l)~~~~~g\dots\text{GDS machen }~~~s\dots\text{Informatik studieren}~~~l\dots\text{GDS lieben}
$$
## Aufgabe 2: Aussagenlogik  
Sechs Kinder möchten im Prater mit dem Blumenrad fahren. Es sind sich alle einig, dass zumindest  
zwei Kinder mitfahren sollen. Petra und Silvio haben Höhenangst und fahren nicht mit. Die anderen vier Kinder diskutieren, wer fahren soll.  

Susanna: ”Wir können Emil und Hannah nicht gemeinsam gehen lassen.“  
Jun: ”Wenn Emil dabei ist, dann muss ich mitkommen!“  
Susanna: ”Jun oder ich müssen mit, aber nicht gleichzeitig!“  
Hannah: ”Nur wenn mich Jun oder Emil begleiten, fahre ich auch mit.“  

- a) Formalisieren Sie die beschriebene Situation inklusive aller Anhaltspunkte mittels aussagenlogischer Formeln. Geben Sie die Bedeutung der Aussagenvariablen an.  

$$
s \dots \text{Susanna fährt mit}~~~j\dots\text{Jun fährt mit}~~~h\dots\text{Hannah färhrt mit}~~~e\dots\text{Emil föhrt mit}
$$
$$
p\dots\text{Petra fährt mit}~~~si\dots\text{Silvio fährt mit}
$$
$$\lnot p \land \lnot si \land (e\nLeftrightarrow h)\land(e\implies j)\land(s \nLeftrightarrow j)\land(h \implies (j \lor e))$$

- b) Können sich die Kinder entscheiden, wer im Blumenrad mitfahren soll, sodass alle Anhaltspunkte berücksichtigt werden? Wer kommt in Frage? Ist die Antwort eindeutig? Begründen Sie Ihre Antwort mithilfe Ihrer aussagenlogischen Modellierung.

| s   | j   | h   | e   | $e \nLeftrightarrow h$ | $e \implies j$ | $(s \nLeftrightarrow j)$ | $h \implies (j \lor e)$ | $(\dots)\land(\dots)\dots$ |
| --- | --- | --- | --- | ---------------------- | -------------- | ------------------------ | ----------------------- | -------------------------- |
| 0   | 0   | 0   | 0   | 0                      | 1              | 0                        | 1                       | 0                          |
| 0   | 0   | 0   | 1   | 1                      | 0              | 0                        | 1                       | 0                          |
| 0   | 0   | 1   | 0   | 1                      | 1              | 0                        | 1                       | 0                          |
| 0   | 0   | 1   | 1   | 0                      | 0              | 0                        | 1                       | 0                          |
| 0   | 1   | 0   | 0   | 0                      | 1              | 1                        | 1                       | 0                          |
| 0   | 1   | 0   | 1   | 1                      | 1              | 1                        | 1                       | 1                          |
| 0   | 1   | 1   | 0   | 1                      | 1              | 1                        | 1                       | 1                          |
| 0   | 1   | 1   | 1   | 0                      | 1              | 1                        | 1                       | 0                          |
| 1   | 0   | 0   | 0   | 0                      | 1              | 1                        | 1                       | 0                          |
| 1   | 0   | 0   | 1   | 1                      | 0              | 1                        | 1                       | 0                          |
| 1   | 0   | 1   | 0   | 1                      | 1              | 1                        | 0                       | 0                          |
| 1   | 0   | 1   | 1   | 0                      | 0              | 1                        | 1                       | 0                          |
| 1   | 1   | 0   | 0   | 0                      | 1              | 0                        | 1                       | 0                          |
| 1   | 1   | 0   | 1   | 1                      | 1              | 0                        | 1                       | 0                          |
| 1   | 1   | 1   | 0   | 1                      | 1              | 0                        | 1                       | 0                          |
| 1   | 1   | 1   | 1   | 0                      | 1              | 0                        | 1                       | 0                          |

Es ist nicht ganz eindeutig, wer fahren. Es können entweder Jun mit Emil oder Jun mit Hannah fahren.

## Aufgabe 3: Aussagenlogik  
###  a) 
Zeigen Sie, dass die Menge $\{f_{2.0}, f_{2.2}, f_{2.15}\}$ vollständig für die Klasse der aussagenlogischen Funktionen ist. Zur Erinnerung die Deﬁnition der drei Funktionen:  

| $e_{1}$ | $e_{2}$ | $f_{2.0}$ | $f_{2.2}$ | $f_{2.15}$ |
| ------- | ------- | --------- | --------- | ---------- |
| $0$     | $0$     | $0$       | $0$       | $1$        |
| $1$     | $0$     | $0$       | $0$       | $1$        |
| $0$     | $1$     | $0$       | $1$       | $1$        |
| $1$     | $1$     | $0$       | $0$       | $1$        |
$f_{2,0}\iff\bot$
$f_{2.15}\iff\top$
$f_{2.2}\iff$
checke nicht
same
### b) 
Sei F die Formel $((A ⇎ B) ⇒ C) ∧ (C ↑ A)$.  
- (1) Bestimmen Sie eine zu $F$ äquivalente Formel in konjunktiver Normalform. Verwenden Sie die semantische Methode (d.h. mit Hilfe einer Wahrheitstabelle).  

| A   | B   | C   | $A\nLeftrightarrow B$ | $(A \nLeftrightarrow B) \implies C$ | $\lnot(C \land A)$ | $((A \nLeftrightarrow B)\implies C) \land \lnot(C\land A)$ |
| --- | --- | --- | --------------------- | ----------------------------------- | ------------------ | ---------------------------------------------------------- |
| 0   | 0   | 0   | 0                     | 1                                   | 1                  | 1                                                          |
| 0   | 0   | 1   | 0                     | 1                                   | 1                  | 1                                                          |
| 0   | 1   | 0   | 1                     | 0                                   | 1                  | 0                                                          |
| 0   | 1   | 1   | 1                     | 1                                   | 1                  | 1                                                          |
| 1   | 0   | 0   | 1                     | 0                                   | 1                  | 0                                                          |
| 1   | 0   | 1   | 1                     | 1                                   | 0                  | 0                                                          |
| 1   | 1   | 0   | 0                     | 1                                   | 1                  | 1                                                          |
| 1   | 1   | 1   | 0                     | 1                                   | 0                  | 0                                                          |
$$
\lnot((\lnot A\land B\land \lnot C)\lor(A \land \lnot B \land \lnot C)\lor(A \land \lnot B \land C)\lor(A \land B \land C))
$$
$$
((A \lor \lnot B \lor C)\land(\lnot A \lor B \lor C)\land(\lnot A \lor B \lor \lnot C)\land(\lnot A \lor \lnot B \lor \lnot C))
$$

- (2) Bestimmen Sie eine zu $F$ äquivalente Formel in disjunktiver Normalform. Verwenden Sie die  algebraische Methode (d.h. mit Hilfe von algebraischen Umformungen).

$$
((A \nLeftrightarrow B)\implies C) \land \lnot(C\land A)
$$
$$
((( A \land \lnot B)\lor( \lnot A \land B))\implies C) \land \lnot( C \lor A)
$$
$$
(\lnot((A \land \lnot B) \lor(\lnot A \land B)) \lor C) \land \lnot(C \lor A)
$$
$$
(((\lnot A \lor B) \land (A \lor \lnot B))\lor C) \land \lnot(C \lor A)
$$





$$
(((\lnot A \land A) \lor ( \lnot A \land \lnot B) \lor (B \land A)\lor(B \land \lnot B))\lor C) \land \lnot (C \lor A)
$$
$$
((\lnot A \land \lnot B) \lor (A \land B) \lor C) \land \lnot (C \lor A)
$$
$$
(((\lnot A \land \lnot B) \land  (\lnot C \land \lnot A)) \lor ((A \land B) \land (\lnot C \land \lnot A)) \lor (C \land  (\lnot C \land \lnot A)))
$$
$$
((\lnot A \land \lnot B \land \lnot C) \lor ())
$$
$$
 
$$
## Aufgabe 4: SAT Solver, Konsequenzbeziehung  
In diesem Beispiel entwickeln wir eine Methode, mit einem SAT-Solver eine beliebige aussagenlogische Formel auf Gültigkeit zu prüfen, d.h. zu entscheiden, ob die Konsequenz $\vDash F$ gilt.  

### a) 
Informieren Sie sich$^{1}$ zu logischer Konsequenz und SAT-Solvern, sodass Sie folgende Fragen beantworten können:

- (1) Was bedeuten die folgenden Aussagen über die logische Konsequenz von $F$ bzw. $¬F$?  
	i. $\vDash F$  
	ii. $\nvDash F$  
	iii. $\vDash ¬F$  
	iv. $\nvDash ¬F$  

i. F ist gültig
ii. F ist widerlegbar
iii. F ist unerfüllbar
iv. F ist erfüllbar

- (2) Wann ist eine Formel $F$ gültig / erfüllbar / widerlegbar / unerfüllbar?

Gültig wenn immer Wahr, Unerfüllbar wenn immer falsch, erfüllbar mind. 1 Interpretation wahr, widerlegbar mind. 1 Interpretation falsch

- (3) Was ist der Input für einen SAT-Solver? Welches Problem lässt sich damit lösen – was ist der  Output?  
Input ist eine Formel in DIMACS Format
Erfüllbarkeit lässt sich lösen.
Output ist eine gültige Interpretation der Variablen für die die Formel bzw. deren Unerfüllbarkeit
### b) 
Bestimmen Sie mit einem SAT-Solver, ob die folgenden Formeln erfüllbar sind. Dabei kann es  
vorkommen, dass Sie eine Formel umformen müssen, die der SAT-Solver verarbeiten kann. Do-  
kumentieren Sie die Umformungsschritte und die Zuordnung der aussagenlogischen Variablen  
zu den Zahlen in der Input-Datei. Was bedeutet die Ausgabe des Solvers? Falls der SAT-Solver als  
Ergebnis SAT liefert, übersetzen Sie die Ausgabe zurück in eine erfüllende Interpretation.

Als SAT-Solver steht Ihnen dazu unter https://derivation.org/public/minisat eine Web-Version  
von Minisat zur Verfügung. Informationen zu DIMACS, dem Eingabe-Format von Minisat, ﬁnden  
Sie z.B. unter https://dwheeler.com/essays/minisat-user-guide.html bzw. bei den Folien zur  
Aussagenlogik.  

- (1) $(A ∨ B) ∧ A$ 

Ist bereits in KNF kein umforen nötig

Input
A ist 1 und B ist 2

p cnf 2 2
1 2 0
1 0

Output: 

1 -2

Beispielsweise wahr mit A und $\lnot B$

- (2) $¬((A ∨ B) ∧ A)$  

$$
\lnot(A \lor B) \lor \lnot A
$$
$$
(\lnot A \land \lnot B) \lor \lnot A
$$
$$
((\lnot A \lor \lnot A)\land \lnot B \lor \lnot A)
$$
$$
(\lnot B \lor \lnot A)
$$

Input
A ist 1 und B ist 2

p cnf 2 1
-1 -2 0

Output: 

-1 -2

Beispielsweise wahr mit $\lnot A$ und $\lnot B$

- (3) $(A ⇒ B) ⇒ ((A ⇒ ¬B) ⇒ ¬A)$

$$
(\lnot A \lor B) \implies ((\lnot A \lor \lnot B)\implies \lnot A)
$$
$$
\lnot(\lnot A \lor B) \lor (\lnot(\lnot A \lor \lnot B) \lor \lnot A)
$$
$$
(A \land \lnot B) \lor ((A \land B) \lor \lnot A)
$$
$$
(A \land \lnot B) \lor (B \lor \lnot A)
$$
$$
((A \lor B \lor \lnot A  ) \land (\lnot B  \lor B \lor \lnot A))
$$
$$
\top \land \top
$$
Formel ist gültig

Input
A ist 1 und B ist 2

p cnf 2 3
-1 1 2 0
-1 2 -2 0

Output
-1 -2
Beispielsweise wahr mit $\lnot A$ und $\lnot B$

- (4) $¬((A ⇒ B) ⇒ ((A ⇒ ¬B) ⇒ ¬A))$  

$$
\lnot((\lnot A \lor B) \implies ((\lnot A \lor \lnot B) \implies \lnot A))
$$
$$
\lnot(\lnot(\lnot A \lor B) \lor (\lnot(\lnot A \lor \lnot B) \lor \lnot A))
$$
$$
(\lnot A \lor B) \land \lnot(\lnot(\lnot A \lor \lnot B) \lor \lnot A)
$$
$$
(\lnot A \lor B) \land ((\lnot A \lor \lnot B) \land A)
$$
$$
(\lnot A \lor B) \land (\lnot B \land A)
$$
$$
(\lnot A \lor B) \land \lnot B \land A
$$
Input
A ist 1 und B ist 2

p cnf 2 3
-1 2 0
-2 0
1 0

Output: 

UNSAT

unerfüllbar
### c) 
In der vorigen Aufgabe haben wir jeweils eine Formel und danach ihre Negation auf ihre Erfüllbarkeit geprüft. In $(1)$ und $(2)$ war das $(A ∨ B) ∧ A$, in $(3)$ und $(4)$ war das $((A ⇒ B) ⇒ ((A ⇒ ¬B) ⇒ ¬A))$. Sie sollten bei den Formeln in $(1)$ und $(3)$ dieselbe Beurteilung bezüglich Erfüllbarkeit / Unerfüllbarkeit erhalten haben, bei den negierten Formeln in $(2)$ und $(4)$ aber eine unterschiedliche. Woran liegt das?  

Da 1 widerlegbar/erfüllbar ist ist deren Negation auch widerlegbar/erfüllbar
Da 3 gültig ist ist die Negation von 3 unerfüllbar


## Aufgabe 5: Mehrdeutigkeiten / Vagheit in der Modellierung mittels Aussagenlogik
In diesem Beispiel analysieren Sie den folgenden Text in Hinblick auf eine Modellierung durch eine 
aussagenlogische Formel. Die Beschreibung ist bewusst vage (bzw. sogar widersprüchlich) gehalten, sodass wir uns damit auseinandersetzen müssen, wie wir in diesem Fall vorgehen. 

- Sascha ist auf einem Teefestival und überlegt, welche Sorten sie einkaufen soll. Sie möchte zumindestens einen grünen und einen schwarzen Tee haben, mehr als drei sind aber dann schon arg teuer. Wenn sie Risheehat Tee nimmt, möchte sie auf keinen Fall einen Darjeeling haben. Es kommt entweder eine Wintermischung oder ein Brennesseltee in Frage, aber keinesfalls beide. Bei Alishan Oolong und Long Jing ist sie sich noch nicht sicher.

Formalisieren Sie den Text mittels einer Formel, die alle Einkaufskombinationen ausdrückt, die Saschas Bedingungen erfüllen.

### a) 
Markieren Sie unklare Stellen im Text (mindestens zwei) und beschreiben Sie, worin die Unklar-  
heit besteht.  

Die Unsicherheit bei Alishon Oolong und Long Jing kann nicht als logische Aussage übersetzt werden

Sie möchte keinen Darjeeling Tee wenn sie einen Risheehat Tee nimmt, aber Risheehat Tee kommt aus der Region Darjeeling

Was arg teuer in diesem Kontext als Konsequenz hat wird auch nicht beschrieben

Hinweise:  
- Manches Mal wird derselbe Begriff / Name für unterschiedliche Konzepte verwendet.  
- Manches Mal werden unterschiedliche Begriffe / Namen für dasselbe Konzept verwendet.  
- Wörter in der Möglichkeitsform (Konjunktiv) wie ”könnten“ etc. führen nicht zu eindeutigen Booleschen Aussagen, lassen sich aber vielleicht trotzdem auﬂösen.  
- Auf der nächsten Seite haben wir ein paar Hintergrundinformationen aus der Wikipedia zusammengestellt, die beim Finden der Unklarheiten helfen könnten.  
### b) 
Legen Sie aussagenlogische Variablen für die elementaren Aussagen im Text fest und geben Sie  
jeweils die Bedeutung an.  

gr ... grüner Tee
sch ... schwarzer Tee
ri ... risheehat Tee
da ... darjeeling Tee
wi ... Wintermischung
br ... brenneseltee
al ... Alishan
ol .. Oolong
lj ... Long Jing
### c) 
Finden Sie zwei unterschiedliche Formeln $G_{1}$ und $G_{2}$ die den Sachverhalt modellieren. Bei jeder  
der gefunden Unklarheiten aus a) sollen sich die beiden Formeln für verschiedene Möglichkeiten  
entscheiden. 

$F_{1}=(gr \land sch)$
$F_{2_{1}}=ri \implies \lnot da$
$F_{2_{2}}=\lnot(ri)$
$F_{3}=wi\nLeftrightarrow br$

$G_{1}=F_{1}\land F_{2_{1}}\land F_{3}$
$G_{2}=F_{1}\land F_{2_{2}}\land F_{3}$

Hinweis: Teilen Sie die Aufgabe in kleinere Aspekte$^{2}$ und modellieren Sie diese getrennt als Formeln $F_{1}, . . . , F_{n}$. Sie können dann $G_{1}$ und $G_{2}$ aus diesen zusammensetzen und gemeinsame Formeln wiederverwenden.  

$^{2}$ Seite 78 Aussagenlogik
### d) 
Vergleichen Sie $G_{1}$ und $G_{2}$ in Bezug auf ihre Interpretationen. Eine Unklarheit führt üblicherweise auch dazu, dass $G_{1}$ und $G_{2}$ nicht semantisch äquivalent sind. Finden Sie eine entsprechende  
Wahrheitsbelegung (Interpretationen) $I$, die nachweist, dass sich $G_{1}$ und $G_{2}$ semantisch unterscheiden, d.h., es muss $val_{I}(G_{1}) \not= val_{I}(G_{2})$ gelten.

| $gr$ | $sch$ | $ri$ | $da$ | $wi$ | $br$ | $gr \land sch$ | $ri \implies \lnot da$ | $\lnot ri$ | $wi\nLeftrightarrow br$ | $G_{1}$ | $G_{2}$ |
| ---- | ----- | ---- | ---- | ---- | ---- | -------------- | ---------------------- | ---------- | ----------------------- | ------- | ------- |
| 1    | 1     | 1    | 0    | 1    | 0    | 1              | 1                      | 0          | 1                       | 1       | 0       |
Unterschiedlich für $ri=1$ und $da=0$ aufgrund des widerspruchs in der angabe zu risheehat tee

Falls die Formeln äquivalent sind: was bedeutet das in Bezug auf die Unklarheit?  
Wären sie äquivalent hätte die unklarheit keine bedeutung bzw. wäre sie vlt gar keine unklarheit

Hinweis: Eine vollständige Wahrheitstabelle ist hier nicht notwendig, Sie werden aber einzelne Zeilen auswerten müssen (und können dann auch gleich eine Interpretation ablesen).  
### e) 
Es kann auch vorkommen, dass eine Ihrer Varianten eine unerfüllbare Formel ist. Was bedeutet  
das für die Modellierung?  

Dass die Modellierung wahrscheinlich falsch ist und die Angabe neu interpretiert werden muss. Rein theoretisch kann es aber auch sein, dass die Angabe nicht erfüllbar ist.
### Zusatzinformationen zu Aufgabe 5  
Tee $[...]$ bezeichnet ein heißes Aufgussgetränk und Genussmittel, das aus den Blättern und Blattknospen, manchmal auch den Stängeln (Kukicha), der Teepﬂanze zubereitet wird. Tee enthält je nach aufgebrühtem Pﬂanzenteil rund 25–75 mg Coffein pro Tasse (250 ml). Im weiteren Sinne wird als ”Tee“ auch ein heißes Aufgussgetränk bezeichnet, das aus Blättern, Knospen, Blüten, Stängeln, Rinden oder auch Wurzeln anderer Pﬂanzen, insbesondere Kräutern oder Früchten, zubereitet wird.  
$[...]$  
Seit dem frühen 18. Jahrhundert wird das Wort Tee auch für den Aufguss aus getrockneten Bestandteilen anderer Pﬂanzen benutzt und bezeichnet nicht allein Schwarzen und Grünen Tee, sondern auch Kräuter- und Früchtetees. Eine ähnliche Situation herrscht in anderen germanischen Sprachen (zum Beispiel Englisch und Niederländisch). Auch im Türkischen ist çay ein Oberbegriff: siyah çay ’schwarzer Tee‘, bitki çayı ’Kräutertee‘ und meyve çayı ’Früchtetee‘. In vielen anderen Sprachen ist diese Zusammenfassung unterschiedlicher Getränke unter einem Begriff dagegen unbekannt. Im Spanischen ist té nur Schwarztee, alles andere heißt infusión. Ähnlich verhält es sich in Frankreich: thé ist schwarzer oder grüner Tee, Kräutertee dagegen wird tisane (oder infusion) genannt; ein Wort, das manchmal auch im Englischen benutzt wird. In der französischsprachigen Schweiz wiederum wird das Wort th´e wie im deutschen Sprachgebrauch auch für Kräuter- und Früchtetee verwendet. Abweichend vom allgemeinen Sprachgebrauch dürfen laut ISO-Norm 3720 nur Blätter und Aufguss der Teepﬂanze (Camellia sinensis) als ”Tee“ bezeichnet werden. Aufgüsse von Kräutern, Früchten oder Gewürzen gelten nach dieser Norm als ”teeähnliche Erzeugnisse“.
$[...]$  
Quelle: https://de.wikipedia.org/wiki/Tee  

Der Darjeeling $[...]$ ist eine Teesorte aus dem indischen Distrikt Darjeeling, dem Zentrum des bengalischen Teeanbaus in der Umgebung der Stadt Darjeeling.  
$[...]$  
Ganz allgemein bezeichnet die Marke Darjeeling jeden Tee, der aus der Region kommt. So wird eine breite Palette an Teearten in Darjeeling wie etwa Grüner Tee, Weißer Tee, Gelber Tee als auch Oolong produziert. Im Speziellen ist jedoch mit der Umschreibung ”Darjeeling-Tee“ meistens ein weitfermentierter Tee gemeint, der Eigenschaften von Oolong und Schwarztee in sich vereint und für gewöhnlich dem Schwarzen Tee zugeordnet wird.  
$[...]$  
Es gibt zahlreiche Teegärten in Darjeeling, die jeweils Tee mit unterschiedlichem Charakter und Aroma produzieren. Einige bekannte Teegärten sind Jogmaya, Arya, Chamong, Glenburn, Lingia, Castleton, Jungpana, Makaibari, Margaret’s Hope, Steinthal, Soom und Risheehat. Das Gebiet der Schluchten in Darjeeling wird in sieben Regionen aufgeteilt: West-Darjeeling, Ost-Darjeeling, Teesta, Mirik, Rungbong, Nord-Kurseong und Süd-Kurseong.  

Quelle: https://de.wikipedia.org/wiki/Darjeeling_(Tee)  

Long Jing, auch Longjing, ist ein gerösteter Grüntee aus der Umgebung des Dorfes Longjing nahe der Stadt Hangzhou in der ostchinesischen Provinz Zhejiang. Der Longjing der Region Xihu (Westsee) gehört zu den ”zehn bekanntesten Teesorten Chinas“  

Quelle: https://de.wikipedia.org/wiki/Long_Jing  

Oolong [...] ist eine traditionelle chinesische Teesorte. Die Oxidationsstufe liegt zwischen  
der von grünem und schwarzem Tee.  

Quelle: https://en.wikipedia.org/wiki/Oolong
## Aufgabe 6: Endliche Automaten  
Gegeben sei folgender Automat $A$:  

![[Pasted image 20241206134729.png]]
### a) 
Speziﬁzieren Sie $A$ als Tupel und geben sie $δ$ in tabellarischer Form an. Handelt es sich bei $A$ um  
einen deterministischen oder nichtdeterministischen Automaten?  

$$
A=\{ Q,\Sigma,\delta,q_{0},F \}
$$
$$
Q=\{ s_{1},s_{2},s_{3},s_{4} \}
$$
$$
\Sigma = \{ a,b \}
$$
$$
q_{0}=s_{1}
$$
$$
F=\{ s_{4} \}
$$
| $\delta$ | $a$     | $b$     |
| -------- | ------- | ------- |
| $s_{1}$  | $s_{1}$ | $s_{2}$ |
| $s_{2}$  | $s_{3}$ | $s_{2}$ |
| $s_{3}$  | $s_{1}$ | $s_{4}$ |
| $s_{4}$  | $s_{3}$ | $s_{2}$ |
Deterministischer Automat
### b) 
Berechnen Sie schrittweise $δ^{*}(s_{1}, baaabab)$. Zu welchem Zustand führt dieses Wort? Wird es von  
$A$ akzeptiert?  

$$
\delta^{*}(s_{1},baaabab)=\delta^{*}(\delta(s_{1},b),aaabab)
$$
$$
= \delta^{*}(\delta(s_{2},a),aabab)
$$
$$
=\delta^{*}(\delta(s_{3},a),abab)
$$
$$
=\delta^{*}(\delta(s_{1},a),bab)
$$
$$
=\delta^{*}(\delta(s_{1},b),ab)
$$
$$
=\delta^{*}(\delta(s_{2},a),b)
$$
$$
=\delta^{*}(s_{3},b)
$$
$$
=\delta^{*}(s_{4},\epsilon)
$$
$$
=s_{4}
$$
Wird akzeptiert

### c) 
Geben Sie alle akzeptierten Wörter mit einer Länge bis zu fünf Zeichen an.  

Überlegung: alle Wörter mit bis zu Länge 4 nach $s_{3}$

nur von $s_{2}$ möglich außer mit
babab

alle Wörter mit bis zu Länge 3 nach $s_{2}$

b
ab
bb
aab
abb
bbb

Alle Wörter mit bis zu fünf
bab
abab
bbab
aabab
abbab
bbbab
babab

### d) 
Welchem Muster folgen akzeptierte Wörter von $A$? Beschreiben Sie die Sprache $L_{A}$ in eigenen  
Worten.

Endet immer in der Folge bab, an den Stellen $s_{1}$ und $s_{2}$ können beliebig viele a bzw. b hinzugefügt werden.
## Aufgabe 7: Modellierung mit deterministischen Automaten  
Modellieren Sie die folgenden Problemstellungen als deterministische endliche Automaten (DEAs), indem Sie folgende Aufgaben erfüllen:

- Identiﬁzieren Sie die notwendigen Zustände. Finden Sie eine passende Darstellung, die einen Zustand eindeutig beschreibt. Wie viele Zustände gibt es insgesamt?  
- Welche Aktionen gibt es, die einen Zustand in einen anderen überführen? Geben Sie wieder eine passende Darstellung an.  
-  Geben Sie nun einen Automaten an, der alle möglichen Verläufe verarbeiten kann. Begründen Sie, warum der von Ihnen gefundene Automat deterministisch ist.  
-  Geben Sie die Sprache des Automaten an, um zu überprüfen, ob Ihre Modellierung passend ist.  

Problemstellung:  
### a) 
Wir betrachten Codewörter über dem Alphabet $\{0, 1\}$, die mit einem Parity-Bit für die Fehlererkennung ausgestattet wurden. Der Automat soll beliebig lange Codewörter überprüfen und sie akzeptieren, wenn kein Fehler erkannt wird. Codewörter müssen mindestens ein Zeichen enthalten (wir erlauben hier den Extremfall, bei dem nur das Parity-Bit übertragen wird). Entwerfen Sie jeweils einen Automaten für Even Parity und Odd Parity.  

Zwei Zustände, einen für das Codewort ist gerade gerade und einen für das Codewort ist gerade ungerade.

Jede 1 verändert den Zustand

Automat für Even Parity
![[Unbenannt 7.png]]

Automat für Odd Parity
![[Unbenannt 8.png]]

$L_{gerade}(A)=\{ w \in \{ 0,1 \}^{*} | \text{ gerade Anzahl an 1er} \}$

$L_{ungerade}(A)=\{ w \in \{ 0,1 \}^{*} | \text{ ungerade Anzahl an 1er} \}$
### b) 
Adaptieren Sie Ihren Automaten für Even Parity, sodass nur Codewörter der Länge 4 akzeptiert  
werden.

Notwendige Zustände sind Start, End und 6 Zwischenspeicherzustände plus impliziter Fehlerzustand.

8 Zustände

0 und 1 führen beide in andere Zustände über (0 ändert aktuelle Wortlänge) (1 ändert Wortlänge und ob Odd/Even)

![[Unbenannt 9.png]]

$L(A)=\{ w\in \{ 0,1 \}^{*} : |w^{*}| \leq 4 \land (2| |\{ 1 \} \in w^{*}|) \}$
## Aufgabe 8: Modellierung mit nichtdeterministischen Automaten  
Modellieren Sie den folgenden Sachverhalt mit einem NEA ohne $ϵ$-Übergänge. Wir bekommen als Eingabe eine Binärzahl, wobei die Zahl vom LSB Bit zum MSB eingeben wird (die Zahl $11011101$ entspricht also der Eingabe $10111011$), und interessieren uns für Eigenschaften der entsprechenden Darstellung als Hexadezimalzahl.

### a) 
Entwerfen Sie einen NEA, der nur Eingaben akzeptiert, deren Hexadezimaldarstellung die Ziffer $A$  
oder die Ziffer $D$ enthält.

$A=1010$
$D=1101$

![[Unbenannt 11.png]]
### b) 
Erweitern Sie Ihren NEA, sodass noch zusätzlich überprüft wird, ob die höchstwertige Ziffer der 
Hexadezimaldarstellung ein F ist.  

![[Unbenannt 12.png]]
### c) 
Geben Sie je ein Beispiel an für Wörter, die beide Automaten akzeptieren, die der erste Automat  
akzeptiert aber nicht der zweite, bzw. die keiner der beiden Automaten akzeptiert.

Beide akzeptieren

11110101

Erste akzeptiert, zweite nicht
00000101

Keiner akzeptiert
00000000

## Aufgabe 9: Determinisierung eines Automaten  
Sei $A$ der folgende nichtdeterministische endliche Automat. $ε$ bezeichnet das Leerwort.  
![[Pasted image 20241206133711.png]]
### a) 
Geben Sie für jedes Wort über dem Alphabet $\{a, b\}$ mit **höchstens drei Symbolen** an, ob es in der Sprache von $A$ liegt. Tragen Sie die Lösung in die Tabelle ein. 

| Wortlänge | Wörter in der Sprache | Wörter nicht in der Sprache |
| --------- | --------------------- | --------------------------- |
| $0$       | $\epsilon$            |                             |
| $1$       | $a$                   | $b$                         |
| $2$       | $aa,ba$               | $ab,bb$                     |
| $3$       | $aaa,aba,baa,bba$     | $aab,abb,bab,bbb$           |
  
## b) 
Konstruieren Sie einen deterministischen endlichen Automaten, der zu $A$ äquivalent ist. Verwenden Sie dafür das in der Vorlesung besprochene Verfahren. Geben Sie den Start- und die Endzustände an.

| $δ^{*}$ | $a$           | $b$         |
| ------- | ------------- | ----------- |
| $1$     | $\{ 1,2,3 \}$ | $\{ 2,3 \}$ |
| $2$     |               | $\{ 3 \}$   |
| $3$     | $\{ 1,2,3 \}$ | $\{ 2 \}$   |
 
| $\hat{δ}$     | a             | b           |
| ------------- | ------------- | ----------- |
| $\{ 1,2,3 \}$ | $\{ 1,2,3 \}$ | $\{ 2,3 \}$ |
| $\{ 2,3 \}$   | $\{ 1,2,3 \}$ | $\{ 2,3 \}$ |
|               |               |             |
|               |               |             |
|               |               |             |
|               |               |             |
Startzustand:  $\{ 1,2,3 \}$
Endzustände: $\{ 1,2,3 \}$

### c) 
Geben Sie Ihren DEA als Graph an.  

![[Unbenannt 13.png]]

### d) 
Überprüfen Sie Ihre Arbeit, indem Sie testen, ob das Wort $abbaabba$ sowohl vom NEA als auch  
von Ihrem DEA akzeptiert wird.

NEA
$\delta^{*}(1,abbaabba)=\delta^{*}(\delta(1,a),bbaabba)$
$=\delta^{*}(\delta(3,b),baabba)$
$=\delta^{*}(\delta(2,b),aabba)$
$=\delta^{*}(\delta(3,a),abba)$
$=\delta^{*}(\delta(1,a),bba)$
$=\delta^{*}(\delta(3,b),ba)$
$=\delta^{*}(\delta(2,b),a)$
$=\delta^{*}(\delta(3,a),\epsilon)$
$=\delta^{*}(1,\epsilon)$
$=1$
wird akzeptiert

DEA
$\delta^{*}(123,abbaabba)=\delta^{*}(\delta(123,a),bbaabba)$
$=\delta^{*}(\delta(123,b),baabba)$
$=\delta^{*}(\delta(23,b),aabba)$
$=\delta^{*}(\delta(23,a),abba)$
$=\delta^{*}(\delta(123,a),bba)$
$=\delta^{*}(\delta(123,b),ba)$
$=\delta^{*}(\delta(23,b),a)$
$=\delta^{*}(\delta(23,a),\epsilon)$
$=\delta^{*}(123,\epsilon)$
$=123$
wird akzeptiert