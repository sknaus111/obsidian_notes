## Aufgabe 1
Stellen sie den Wahrheitswert der folgenden Aussagen, jeweils mit Begründung fest.
- a) $\forall x \in \mathbb{N} \exists y \in \mathbb{N} x\leq y$
Ja da man in den natürlichen Zahl ja immer weiterzählen kann, also 1 dazu addieren. jede natürliche Zahl hat einen Nachfolger
- b) $\exists x \in \mathbb{N} \forall y \in \mathbb{N} x\leq y$
Wahr für ein x von 1
- c) $\exists x \in \mathbb{Z} \forall y \in \mathbb{Z} x\leq y$
Nicht wahr, da man in den ganzen Zahlen auch immer in die andere Richtung weiterzählen kann, also immer eins abziehen. Somit hat x einen ganzen Nachfolger, welcher kleiner als x ist.
- d) $\forall x \in \mathbb{N} (x\leq 2 \implies x>2)$
Nicht wahr da eine Zahl nicht kleiner gleich 2 sein kann, in den natürlichen Zahlen trifft dies auf 1 und 2 zu. Diese drei Zahlen sind nicht größer als 2.
- e) $(\forall x \in \mathbb{N} x\geq 2)\implies (\forall x \in \mathbb{N} x>2)$
Ist richtig, da die linke Seite der Implikation falsch ist.
## Aufgabe 2
Verneinen sie die folgenden Aussagen
- $\forall x \exists y R(x,y)$
$\exists x\forall y \lnot R(x,y)$
- $\forall x(P(x) \implies Q(x))$ 
$\exists x( P(x) \land \lnot Q(x))$  
- $\exists x (P(x)\land Q(x))$
$\forall x (\lnot P(x)\lor \lnot Q(x))$
- $\forall x \exists y P(x,y) \implies \forall u\exists vR(u,v)$
$\forall x \exists y P(x,y) \land \exists u\forall v\lnot R(u,v)$

## Aufgabe 3
Wir wollen eine Situation in Wirtshaus beschreiben. Es seien die folgenden atomaren Prädikate gegeben. 

	sitzt(x,y) (die Person) x sitzt am Tisch y
	isst(x,y) x isst y
	trinkt(x,y) x trinkt y

Übersetzen Sie die folgenden Prädikate und Sätze in die Prädikatenlogik
- a)Karl isst ein Gulasch und trinkt Bier
$\exists x\in Personen : \exists g \in Essen: \exists b \in Trinken:~isst(Karl,Gulasch) \land trinkt(Karl,Bier)$
- b) $x_{1}$ sitzt am selben Tisch wie $x_{2}$
$\exists y: (sitzt(x_{1},y) \land sitzt(x_{2},y))$
- c) Am Tisch von Franz trinkt niemand Wein
$\exists y sitzt(Frank,y) \land \forall x:sitzt(x,y) \implies\lnot trinkt(x,Wein)$
- d) Manche trinken nur Bier aber essen nichts
$\exists x\forall y\vartheta trinkt(x,b) \land \lnot isst(x,y)$
$\exists x \exists \lnot b \forall y$
- e) Jeder der etwas isst trinkt etwas dazu
$\forall x: isst(x,e) \implies trinkt(x,g)$
