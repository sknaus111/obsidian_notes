## Aufgabe 1. 
Geben Sie eine beschreibende Darstellung (verwenden Sie die Notation $\{x | P(x)\}$ oder
eine ihrer in der Vorlesung beschriebenen Abkürzungen) der Menge $\dots$

- a) ... der gemeinsamen Teiler von gegebenen $n_{1}, n_{2} ∈ \mathbb{Z}$

$$
A=\{ x\in \mathbb{Z}: x|n_{1} \land x|n_{2}\}
$$

- b) ... der Quadrate ungerader Zahlen

$$
B=\{ x^{2}\in \mathbb{Z}| \exists k \in \mathbb{Z}:2k+1=x\}
$$

- c) ... der natürlichen Zahlen, deren Quadratwurzel irrational ist

$$
C = \{ x\in \mathbb{N}| \sqrt{ x }\not\in \mathbb{Q} \}
$$

- d) ... der Teilmengen der ganzen Zahlen, die kein Quadrat enthalten an.

$$
D=\{ A\subseteq \mathbb{Z}|\forall x\in A:\sqrt{ x }\not\in \mathbb{Z} \}
$$

## Aufgabe 2. 
Sei $f : A → B$ und seien $A_{1}, A_{2} ⊆ A$. Beweisen oder widerlegen Sie:

- a) $f (A_{1} ∪ A_{2}) = f (A_{1}) ∪ f (A_{2})$

Zuerst überprüfen wir ob $f(A_{1} \cup A_{2}) \subseteq f(A_{1})\cup f(A_{2})$ gilt

$y\in f(A_{1}\cup A_{2})$ so dass $f(x)=y$
Also gilt für das $x \in A_{1} \cup A_{2}$
Somit kann man auch schreiben $f(x)\in f(A_{1})\cup f(A_{2})$
Somit stimmt nun die Aussage $f(A_{1}\cup A_{2})\subseteq f(A_{1})\cup f(A_{2})$


Die andere Seite ist $f(A_{1})\cup f(A_{2})\subseteq f(A_{1}\cup A_{2})$

$y\in f(A_{1})\cup f(A_{2})$ impliziert dass es ein $f(x)=y$ gibt für welches gilt
$x\in A_{1}\cup A_{2}$ daraus folgt $y\in f(A_{1}\cup A_{2})$
Somit stimmt nun die Aussage $f(A_{1})\cup f(A_{2})\subseteq f(A_{1}\cup A_{2})$

Da beide Mengen als Teilmenge ineinander enthalten sind, kann man sagen
$f(A_{1}\cup A_{2})=f(A_{1})\cup f(A_{2})$

- b) $f (A_{1} ∩ A_{2}) = f (A_{1}) ∩ f (A_{2})$

widerlegbar durch ein Gegenbeispiel

Sei die funktion $f:\mathbb{Z} \rightarrow \mathbb{Z}$ mit $f(x)=x^{2}$

Dann könnte man $A_{1}=\{ 2 \}$
und $A_{2}=\{ -2 \}$
einsetzten um folgendes zu bekommen

$$
f(\{ 2 \} \cap \{ -2 \}) = f(\emptyset)
$$
$$
f(\{ 2 \}) \cap f(\{ -2 \})
$$
$$\{ 4 \} \cap \{  4 \} = \{ 4 \}
$$
Da $\emptyset \not= \{ 4 \}$ ist wurde die Aussage widerlegt

- c) $f (A_{1}^{c}) = f (A_{1})^{c}$

Nehme man wieder die Funktion $f:\mathbb{Z}\rightarrow \mathbb{Z}$ mit $f(x)=x^{2}$
$$
f(\{ 2 \}^{c}) = f(\mathbb{R}\setminus \{ 2 \})=\mathbb{R}^{+}_{0}\setminus\{ 2 \}
$$
$$
f(\{ 2 \})^{c}=\{ 4 \}^{c}=\mathbb{R}^{+}_{0}\setminus\{ 4 \}
$$
Da $\mathbb{R}^{+}_{0}\setminus \{ 2 \}\not=\mathbb{R}^{+}_{0}\setminus\{ 4 \}$ ist, wurde die Aussage widerlegt