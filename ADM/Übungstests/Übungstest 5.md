## (7 Punkte) 
Überprüfen Sie, ob Folgendes gilt und beweisen Sie ihre Aussage.

$$
\sum_{k=1}^{n}(4k-2)=2n^{2}
$$
#Induktionsvoraussetzung
$$
\sum_{k=1}^{n} (4k-2)=2n^{2}
$$
#Induktionsanfang
$$
4-2 = 2*1
$$
$$
2=2
$$
#Induktionsbehauptung
$$
\sum_{k=1}^{n+1} (4k-2) = 2(n+1)^{2}
$$
#Induktionsschritt
$$
 = 2n^{2} + (4(n+1)-2)
$$
$$
= 2n^{2} + 4n +4 -2
$$
$$
= 2n^{2} + 4n +2
$$
$$
= 2*(n^{2}+2n+1)
$$
$$
= 2(n+1)^{2}
$$
## 2. (2 Punkte) 
Überprüfen Sie, ob folgende Funktion bijektiv ist und geben sie gegebenenfalls eine Umkehrfunktion an.
$$
f : \mathbb{R} \setminus  \{1, 2\} → \mathbb{R} \setminus \{−2, 1\}
$$
$$
f (x) := \frac{x}{x-1}
$$
Injektiv
$$
f(x_{1}) = f(x_{2}) \implies x_{1} = x_{2}
$$
$$
\frac{x_{1}}{x_{1}-1} = \frac{x_{2}}{x_{2}-1}
$$
$$
x_{1}(x_{2}-1) = x_{2}(x_{1}-1)
$$
$$
x_{1}x_{2}-x_{1}=x_{2}x_{1}-x_{2}
$$
$$
-x_{1}=-x_{2}
$$
$$
x_{1}=x_{2}
$$
	Surjektiv
$$
\forall y \in R\setminus \{ -2,1 \}:f(x)=y
$$
$$
\frac{x}{x-1} = y
$$
$$
x = y(x-1)
$$
$$
x = xy -y
$$
$$
x - xy = -y
$$
$$
x(1-y) = -y
$$
$$
x = \frac{-y}{1-y}
$$
Umkehrfunktion
$$
f(x)^{-1} = -\frac{x}{1-x}
$$
## 4. (6 Punkte) 
Kreuzen Sie den richigen Wahrheitsgehalt der folgenden Aussagen an. Eine richtige Antwort führt zu zwei Punkten, eine falsche zu keinem Punkt. Ein Ankreuzen von ”42/keine Angabe” führt zu einem Punkt.

| Aussage                                          | gültig | nicht gültig | 42/keine Angabe |
| ------------------------------------------------ | ------ | ------------ | --------------- |
| $∃x ∈ \mathbb{Z} : ∀y ∈ \mathbb{Z} : x + y < 0$. |        | X            |                 |
| $A ∧ B → B ∧ A$                                  | X      |              |                 |
| $(¬A → B) → (A ∨ ¬B)$                            |        | X            |                 |
