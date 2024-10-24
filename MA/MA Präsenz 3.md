## Aufgabe 1. 
Verwenden Sie die Definition $y = m − n :\iff n + y = m$ der Subtraktion um das
Symbol $−$ (minus) aus den folgenden Formeln zu entfernen und zu diesen äquivalente Formeln zu
bestimmen.
- a) $x − 0 = x$
	$x+0=x$
- b) $x − 1 \not= 2$
	$1+2\not=x$
- c) $y \not= 0 \implies x − y \not = x + y$
	$y\not=0 \implies x\not=x+y+x$
- d) $x \not= y \implies x − y\not= y − x$
	$x \not=y \implies x+x\not=y+y$
## Aufgabe 2. 
Welche der folgenden Funktionen sind für $x \in R$ wohldefiniert?
 $\forall y\in\mathbb{R}: \not\exists y_{1},y_{2}.y_{1}\not=y_{2}\land f(x)=y_{1}\land f(x)=y_{2}$
- $f_{1}(x) := max\{k \in \mathbb{Z} | k  \leq x\}$
	wohldefiniert, da die Funktion einfach abrundet.
- $f_{2}(x) := x − f_{1}(x)$
	wohldefiniert, da $f_{1}$ wohldefiniert ist, und der restliche Teil des Terms ebenfalls keine Möglichkeit für eine nicht Wohldefinition zulässt.
- $y = f_{3}(x) :\iff y^2 = x$
	nicht wohldefiniert, da ein Wert $x$ zwei verschiedene $y$ Werte ermöglicht $\pm$
- $f_{4}(x) := min\{k \in \mathbb{Z} | k \leq x\}$
	nicht wohldefiniert, da die Menge nach unten unbeschränkt ist, $min$ wäre $-\infty$
- $f_{5}(x) := max\{−x, x\}$
	wohldefiniert, da immer ein $max$ $\exists$
Geben Sie jeweils eine Begründung an.
## Aufgabe 3. 
Übersetzen Sie die folgenden Definitionen in die Prädikatenlogik, geben Sie jeweils
mindestens ein Beispiel und versuchen Sie möglichst viel über diese Begriffe herauszufinden indem
Sie sich natürliche Fragen zu ihnen stellen.

- a) Eine Quadratzahl ist eine natürliche Zahl die das Quadrat einer natürlichen Zahl ist.
	$x \in \mathbb{N}:\mathbb{Q^2}(x) \iff \exists n \in\mathbb{N}:n*n=x$
- b) Eine natürliche Zahl heißt Dreieckszahl falls sie als $\sum_{i=1}^{n}i$ geschrieben werden kann.
	$x \in \mathbb{N}:D(x) \iff \exists n \in \mathbb{N}:\sum_{i=1}^{n}i=x$
- c) Eine natürliche Zahl heißt quadratfrei falls sie nicht durch das Quadrat einer natürlichen Zahl $> 1$ geteilt wird.
	$x \in \mathbb{N}:\not\mathbb{Q^2}(x) \iff \forall n \in \mathbb{N} :\frac{x}{n^2}\not\in\mathbb{N} \land n>1$

Sie können zur Vereinfachung ihrer Übersetzungen in die Prädikatenlogik davon ausgehen dass sich alle Quantoren nur auf natürliche Zahlen beziehen.