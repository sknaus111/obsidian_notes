#Prädikate beschreiben Eigenschaften in der Aussagenlogik. Im Satz
$$
\text{Das Haus ist groß}
$$
Ist das Wort $\text{groß}$ ein Prädikat 
$$
P(x)=\text{x ist groß}
$$
Diesen Prädikaten kann durch das Einsetzen eines konkreten Wertes ein Wahrheitswert zugeordnet werden.

Auch gibt es Prädikate, welche mehrere Eingangvariablen beinhalten.
$$
\text{Peter ist größer als Klaus}
$$
Kann allgemein als folgendes Prädikat $Q(x_{1},x_{2},x_{3}\dots)$ ausgedrückt werden
$$
Q(x,y)=\text{x ist größer als y}
$$
Doch man kann nicht nur konkrete Variablen einsetzen. Auch allgemeine Ausdrücke wie
$$
\text{"Für alle" oder "Für ein"}
$$
Für die Aussage, dass das Prädikat für alle $x$ stimmt gibt es den #Allquantor
$$
\forall xP(x)
$$
Für die Aussage, dass das Prädikat für ein x stimmt gibt es den #Existenzquantor
$$
\exists xP(x)
$$
So ist es auch möglich Prädikate mit den Verbindungen der [[Aussagen]] zu verknüpfen um Formeln zu erstellen.
$$
\forall x_{1}((P_{1}(x_{1})\land p_{1})\implies(\exists x_{2}(P_{2}(x_{2})\land p_{2})\implies P_{3}(x_{1},x_{2})))
$$

## Äquivalenzen
So wie bei den [[Äquivalente Formeln]] der grundlegenden aussagen logischen Operatoren gibt es bei den Prädikaten Ebenfalls äquivalente Formeln.
- (x) $\forall x \forall y P(x,y) \iff \forall y \forall x P(x,y), ~~~~~\exists x \exists y P(x,y) \iff \exists y \exists xP(x,y)$
- (xi) $a\land \forall xP(x) \iff \forall x(a \land P(x))~~~~~a \lor \exists xP(x)\iff \exists x(a\lor P(x))$
- (xii) $a \land \exists P(x) \iff \exists x(a\land P(x))~~~~~a\lor \forall xP(x)\iff \forall x (a\lor P(x)$
- (xiii) $\lnot (\forall xP(x))\iff \exists x\lnot P(x)~~~~~~~~\lnot (\exists P(x))\iff \forall x \lnot P(x)$

Quantoren werden auch verwendet um über Elemente einer Menge Aussagen zu treffen. So ist 
$$
\forall x \in E : P(x)
$$
die Kurzschreibweise für.
$$
\forall x ((x\in E)\implies P(x))
$$
mit $\exists$ funktioniert dies Kurzschreibweise natürlich auch.