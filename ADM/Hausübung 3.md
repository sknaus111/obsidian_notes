$a\equiv b \text{ mod } m\implies a \text{ mod }m =b \text{ mod }m$

$ac \equiv bc$

$m|b-a$

## 63)
Beweisen Sie die folgenden Behauptungen oder widerlegen Sie sie durch ein konkretes Gegenbeispiel.
- a) Falls $ac ≡ bc$ mod $m$, $c \not = 0$ und $c | m$, dann gilt auch $a ≡ b$ mod $\frac{m}{c}$  .
	$bc=ac +qm$
	$b=a+\frac{qm}{c}$
	$b=a+q\frac{m}{c}$
	$a\equiv b \text{ mod } \frac{m}{c}$

- b) Falls $a ≡ b$ mod $m$, dann gilt auch $a^2 ≡ b^2$ mod m.
	$m|b-a$
	$a=m*q+b$
	$a-b=mq$
	$(a-b)(a+b) = (a+b)mq$ 
	$a^2-b^2 = (a+b)mq$
	$a^2-b^2=amq+bmq$
	$a^2 = amq+bmq+b^2$
	$amq+bmq|b^2-a^2$
	$a,b,q \in \mathbb{Z} \implies$ kürzbar
	$2m|b^2-a^2$
	$m|b^2-a^2$
	$a^2\equiv b^2 \text{ mod }m$
	
- c) Falls $a^2 ≡ b^2$ mod $m$, dann gilt auch $a ≡ b$ mod $m$
	$4 \equiv 9 \text{ mod }5$ probiert $2 \equiv 3 \text{ mod }5$
	Gegenbeispiel. Behauptung funktioniert nicht. 

## 66) 
a) $3x ≡ 9 \text{ mod } 11$, b) $3x ≡ 9 \text{ mod } 12$
	Bestimmen Sie alle Lösungen der folgenden Kongruenzen bzw. beweisen Sie die Unlösbarkeit (in Z):

	$3x\equiv9 \text{ mod }11$
	$x\equiv 3 \text{ mod }11$
	$11|(3-x)$
	$x=11*q+3$

	$3x\equiv9 \text{ mod }12$
	$x\equiv 3 \text{ mod }4$
	$4|(3-x)$
	$x=4*q+3$
	
 Essenz ist ob $x$ kürzbar ist oder nicht
 
## 81) 
$(a ∧ ¬b) ∧ ¬c ⇐⇒ a ∧ ¬(b ∧ ¬c)$
Entscheiden Sie mit Hilfe einer Wahrheitstafel, ob die folgenden Äquivalenzen richtig sind.
$→$ und $↔$ bezeichnen Sub- bzw. Bijunktion.

| a   | b   | c   | $\lnot b$ | $\lnot c$ | $(a\land \lnot b)$ | $(a\land \lnot b)\land \lnot c$ | $(b\land\lnot c)$ | $\neg(b\land \neg c)$ | $a\land \neg(b\land \neg c)$ | $(a ∧ ¬b) ∧ ¬c ⇐⇒ a ∧ ¬(b ∧ ¬c$ |
| --- | --- | --- | --------- | --------- | ------------------ | ------------------------------- | ----------------- | --------------------- | ---------------------------- | ------------------------------- |
| 0   | 0   | 0   | 1         | 1         | 0                  | 0                               | 0                 | 1                     | 0                            | 1                               |
| 0   | 0   | 1   | 1         | 0         | 0                  | 0                               | 0                 | 1                     | 0                            | 1                               |
| 0   | 1   | 0   | 0         | 1         | 0                  | 0                               | 1                 | 0                     | 0                            | 1                               |
| 0   | 1   | 1   | 0         | 0         | 0                  | 0                               | 0                 | 1                     | 0                            | 1                               |
| 1   | 0   | 0   | 1         | 1         | 1                  | 1                               | 0                 | 1                     | 1                            | 1                               |
| 1   | 0   | 1   | 1         | 0         | 1                  | 0                               | 0                 | 1                     | 1                            | 0                               |
| 1   | 1   | 0   | 0         | 1         | 0                  | 0                               | 1                 | 0                     | 0                            | 1                               |
| 1   | 1   | 1   | 0         | 0         | 0                  | 0                               | 0                 | 1                     | 1                            | 0                               |
 
 Stimmt in zwei Fällen nicht.

## 100) 
$A △ (B ∩ C) = (A △ B) ∩ (A △ C)$
Beweisen Sie die folgenden Beziehungen mit Hilfe von Elementtafeln oder geben Sie ein
konkretes Gegenbeispiel an

| $A$        | $B$        | $C$        | $B\cap C$ | $A △ (B ∩ C)$ | $A\triangle B$ | $A\triangle C$ | $(A\triangle B)\cap(A\triangle C)$ | $A △ (B ∩ C) = (A △ B) ∩ (A △ C)$ |
| ---------- | ---------- | ---------- | --------- | ------------- | -------------- | -------------- | ---------------------------------- | --------------------------------- |
| $\in$      | $\in$      | $\in$      | $\in$     | $\not \in$    | $\not \in$     | $\not \in$     | $\not \in$                         | $\in$                             |
| $\in$      | $\in$      | $\not \in$ | $\not\in$ | $\in$         | $\not \in$     | $\in$          | $\not \in$                         | $\not \in$                        |
| $\in$      | $\not \in$ | $\in$      | $\not\in$ | $\in$         | $\in$          | $\not \in$     | $\not \in$                         | $\not \in$                        |
| $\in$      | $\not \in$ | $\not \in$ | $\not\in$ | $\in$         | $\in$          | $\in$          | $\in$                              | $\in$                             |
| $\not \in$ | $\in$      | $\in$      | $\in$     | $\in$         | $\in$          | $\in$          | $\in$                              | $\in$                             |
| $\not \in$ | $\in$      | $\not \in$ | $\not\in$ | $\not \in$    | $\in$          | $\not \in$     | $\not \in$                         | $\in$                             |
| $\not \in$ | $\not \in$ | $\in$      | $\not\in$ | $\not \in$    | $\not \in$     | $\in$          | $\not \in$                         | $\in$                             |
| $\not \in$ | $\not \in$ | $\not \in$ | $\not\in$ | $\not \in$    | $\not \in$     | $\not \in$     | $\not \in$                         | $\in$                             |


Stimmt in zwei Fällen nicht. 
Bsp. Im Fall $Element \in A$, $Element \in B$, $Element \not\in C$

## Präsenzaufgabe

10101 * 10001
01010 * 100010 -
00101 * 1000100
00010 * 10001000
00001 * 100010000


000010001
001000100
100010000
101100101

2^4 + +2^3 +2^2 +2^1 +2^0 * 10001

10001
10001 * 2^2 = 1000100
10001 * 2^4 = 100010000

