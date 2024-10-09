#Induktion 
In der Verlaufsinduktion wird anstatt dem #Induktionsschritt die Information aus den vorigen $P(k)$ genutzt. Man nimmt an, dass $P(0)$, $P(1)$ bis $P(n)$ gültig sind und leitet daraus $P(n+1)$ ab.
#Induktionsbehauptung 
Diese Variante der vollständigen Induktion in logischer Schreibweise

$$
P(0) \land (\forall n \in \mathbb{N}:(\forall k\leq n:P(k)) \implies P(n+1)) \implies \forall n\in\mathbb{N}:P(n)
$$
## Beispiel
### Beispiel 1.3
Eine natürliche Zahl > 1 ist prim, wenn sie nicht als Produkt $n = r * s$ zweier natürlicher Zahlen r, s darstellbar ist, die beide kleiner als n sind.

Für alle $n > 1$ sei folgende Aussage zu überprüfen: n ist entweder selbst prim oder als Produkt endlich vieler Primzahlen darstellbar.

Der Induktionsanfang wurde auf die Zahl 2 verschoben. Somit wäre der Induktionsanfang bestätigt, da 2 offensichtlich eine Primzahl ist. 

Um die #Induktionsbehauptung zu beweisen nehme man an, dass P für alle natürlichen Zahlen kleiner gleich n wahr ist. Nun überprüft man ob n+1 prim ist. Ist dies der Fall so kann ohne weitere Argumentation die Aussage als wahr betrachtet werden. Sollte dies nicht der Fall sein so lässt sich n+1 als Produkt von zwei natürlichen Zahlen r und s darstellen. Unter der Annahme der #Induktionsvoraussetzung gilt die Eigenschaft P für r und für s. Folglich ist n+1 als Produkt endlich vieler Primzahlen darstellbar. Somit wurde gezeigt, dass jede natürliche Zahl > 1 eine Primfaktorzerlegung besitzt.