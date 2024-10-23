## Aufgabe 1. 
Die folgenden Sätze sollen auf sinnvolle Weise in die Prädikatenlogik übersetzt wer-
den. Wählen Sie dazu zunächst eine geeignete Menge atomarer Prädikate und geben Sie dann die
Übersetzungen an.

$ist(x,y) \text{x ist Tier der Art y}$
$fürchtet(x,y) \text{x hat Angst vor y}$
$liebt(x,y) \text{x liebt y}$

- a) Katzen, Hunde und Bären sind Säugetiere.
$\forall x:(ist(x,Bär)\lor ist(x,Katze)\lor ist(x,Hund)\implies ist(x,Säugetiere))$
- b) Bruno ist ein Bär.
$\exists x:ist(Bruno,Bär)$
- c) Es gibt einen Bären der Angst vor Hunden hat.
$\exists x:ist(x,Bär)\implies fürchtet(x,Hund)$
- d) Bruno liebt Katzen die keine Angst vor Bären haben.
$\exists x: liebt(x,y) \land \forall y:\lnot fürchtet(y,Bär)$
- e) Bruno hat keine Angst vor Katzen und Hunden.
$\exists x \in Bären:\lnot fürchtet(x,Katze) \land \lnot fürchtet(x,Hund)$
## Aufgabe 2. 
Welche Variablen kommen in den folgenden Ausdrücken frei und welche gebunden vor?

- a) $\forall x (P(x) \implies Q(x,y))$
x kommt gebunden und y kommt frei vor 
- b) $x \leq y \land \forall z (x \leq z \implies y \leq z)$
x und y kommen frei vor, z kommt gebunden vor
- c) $\forall n \exists k \sum_{i=1}^{k}m*i=n$
n, k und i kommen gebunden vor, m kommt frei vor
- d) $\sum_{i=1}^{n}\sum_{j=1}^{i}j^2$
n, i und j kommen gebunden vor
- e) $\exists y (\exists x ~x^2 = y \land \exists z ~y * z = x)$
x, y und z kommen gebunden vor