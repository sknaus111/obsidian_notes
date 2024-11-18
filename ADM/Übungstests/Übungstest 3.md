## 1. (7 Punkte) 
Überprüfen Sie, ob 

$$
\sum_{k=1}^{n}(4k - 1)=2n^{2}+n
$$

für alle $n ∈ N_{0}$ gilt und beweisen Sie Ihre Aussage.

#Induktionsvoraussetzung
$$
\sum = 2n^{2}+n
$$
#Induktionsanfang
$$
4*1-1 = 2*1^{2}+1
$$
$$
3 = 3
$$
#Induktionsbehauptung
$$
\sum_{k=1}^{n+1}(4k-1) = 2(n+1)^{2}+(n+1)
$$
$$
= 2n^{2}+4n+2+n+1
$$
$$
= 2n^{2}+ 5n+3
$$
#Induktionsschritt
$$
= 2n^{2}+n + (4(n+1)-1)
$$
$$
= 2n^{2}+n+(4n+3)
$$
$$
= 2n^{2} + 5n +3
$$

## 2. (2 Punkte) 
Seien $f : A → B, g : B → C$ und $h : C → D$ Funktionen. Mit $◦$ bezeichnen wir die Verknüpfung von Funktionen: $g ◦ f : A → C, x  → g(f (x))$. Zeigen Sie

$h ◦ (g ◦ f ) = (h ◦ g) ◦ f.$

Hinweis: Funktionen stimmen genau dann überein, wenn ihre Funktionswerte für alle Argumente
übereinstimmen.

$$
h \circ g(f(x)) = h(g(x)) \circ f
$$
$$
h(g(f(x))) = h(g(f(x)))
$$
## 3. (a) (3 Punkte) 
Sei $(G, ◦)$ eine Gruppe und $e$ das neutrale Element. Zeigen Sie, dass für alle $m, n ∈ N_{0}$ und $x ∈ G$ gilt:

$$(x^{m})^{n} = x^{mn}.$$
Dabei dürfen Sie ohne Beweis nutzen, dass

$$x^{m+n} = x^{m} ◦ x^{ n}$$
für alle $n, m ∈ \mathbb{N}_{0}$ und $x ∈ G$ gilt.
Zur Erinnerung: Für $x ∈ G$ und $n ∈ \mathbb{N}_{0}$ ist der Ausdruck $x^{n}$ rekursiv durch
$x_{0} := e$ und $x^{n+1} := x ◦ x^{n}$ für alle $n ∈ \mathbb{N}_{0}$ definiert.

(b) (2 Punkte) Überprüfen Sie, ob es sich bei $(\mathbb{Z}, ◦)$ um eine Gruppe handelt, wobei $◦$ folgen-
dermaßen operiert:

$$a ◦ b := 3a + 4b$$.
## 4. (6 Punkte) 
Kreuzen Sie in folgender Tabelle an, ob die angegebene Aussage gültig ist oder nicht. Eine richtiges Kreuz führt zu zwei Punkten, ein falsches zu keinem Punkt. Wenn Sie
”keine Angabe“ ankreuzen bekommen Sie einen Punkt.

| Aussage                                     | gültig | nicht gültig | keine Angabe |
| ------------------------------------------- | ------ | ------------ | ------------ |
| $∃x ∈ (0, 1) : ∀y ∈ (0, 1) : x ≥ y$         | x      |              |              |
| $(A ∧ B) ∨ C ⇒ (B ∨ C) ∧ A$                 |        | X            |              |
| Die leere Menge ist Element von jeder Menge |        | X            |              |
