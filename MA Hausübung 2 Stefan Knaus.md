## Aufgabe 1. 
Die folgenden Sätze sollen auf sinnvolle Weise in die Prädikatenlogik übersetzt wer-
den. Wählen Sie dazu zunächst eine geeignete Menge atomarer Prädikate und geben Sie dann die
Übersetzungen an.

- a) Katzen, Hunde und Bären sind Säugetiere.
$ist(Katzen,Säugetiere) \land ist(Hunde,Säugetiere) \land ist(Bären,Säugetiere)$
- b) Bruno ist ein Bär.
$ist(Bruno,Bär)$
- c) Es gibt einen Bären der Angst vor Hunden hat.
- d) Bruno liebt Katzen die keine Angst vor Bären haben.
- e) Bruno hat keine Angst vor Katzen und Hunden.
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