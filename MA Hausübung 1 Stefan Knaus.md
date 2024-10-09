## Aufgabe 1. 
Übersetzen Sie die folgenden Sätze in aussagenlogische Formeln. Geben Sie dabei die
atomaren Aussagen an die Sie verwenden.
Man definiere die Anwesenheit von Anna als Aussage A, die Anwesenheit von Bernhard als Aussage B und die Anwesenheit von Caro als Aussage C.

- a) Anna und Bernhard sind anwesend.
	$A~\land~B$  
- b) Wenn Caro anwesend ist, dann ist auch Bernhard anwesend.
	$C~\implies~B$
- c) Wenn weder Bernhard noch Caro anwesend sind, dann ist auch Anna nicht anwesend.
	$\neg(B~\lor~C)\implies \neg A$
- d) Caro ist nur anwesend wenn Bernhard oder Anna anwesend sind.
	$C \implies (B \lor A)$
- e) Wenn sowohl Anna als auch Caro anwesend sind, dann ist Bernhard nicht anwesend.
	$(A~\land~C)\implies \neg B$

## Aufgabe 2. Beweisen Sie die Rechenregel A ∧ (B ∨ C ) ⇔ (A ∧ B) ∨ (A ∧ C ).

| $A$ | $B$ | $C$ | $B\lor C$ | $A\land(B\lor C)$ | $A\land B$ | $A\land C$ | $(A\land B)\lor(A\land C)$ |
| --- | --- | --- | --------- | ----------------- | ---------- | ---------- | -------------------------- |
| 0   | 0   | 0   | 0         | 0                 | 0          | 0          | 0                          |
| 0   | 0   | 1   | 1         | 0                 | 0          | 0          | 0                          |
| 0   | 1   | 0   | 1         | 0                 | 0          | 0          | 0                          |
| 0   | 1   | 1   | 1         | 0                 | 0          | 0          | 0                          |
| 1   | 0   | 0   | 0         | 0                 | 0          | 0          | 0                          |
| 1   | 0   | 1   | 1         | 1                 | 0          | 1          | 1                          |
| 1   | 1   | 0   | 1         | 1                 | 1          | 0          | 1                          |
| 1   | 1   | 1   | 1         | 1                 | 1          | 1          | 1                          |

| $A\land(B\lor C)\iff(A\land B)\lor(A\land C)$ |
| --------------------------------------------- |
| 1                                             |
| 1                                             |
| 1                                             |
| 1                                             |
| 1                                             |
| 1                                             |
| 1                                             |
| 1                                             |

Die Aussage $A \land (B \lor C ) \iff (A \land B) \lor (A \land C)$ ist gültig.