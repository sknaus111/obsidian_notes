## (1) 7 Punkte 
Beweisen Sie mittels vollständiger Induktion die Gültigkeit der folgenden Summenformel für alle natürlichen Zahlen $n ∈ \mathbb{N}$:

$$
\sum_{k=0}^{n} \frac{k}{4^{k}} = \frac{4}{9}- \frac{3n+4}{9*4^{n}}
$$
Dabei müssen alle Elemente eines Induktionsbeweises angeführt und die kennengelernten
Bezeichnungen angegeben werden.

#Induktionsvoraussetzung
$$
\sum_{k=0}^{n} \frac{k}{4^{k}} = \frac{4}{9}- \frac{3n+4}{9*4^{n}}
$$
#Induktionsanfang
$$
0 = \frac{4}{9} - \frac{4}{9}
$$
$$
0=0
$$
#Induktionsbehauptung
$$
\sum_{k=0}^{n+1} \frac{k}{4^{k}} = \frac{4}{9}- \frac{3(n+1)+4}{9*4^{(n+1)}}
$$
#Induktionsschritt
$$
= \frac{4}{9} - \frac{3n+4}{9*4^{n}} + \frac{n+1}{4^{n+1}}
$$
$$
= \frac{4}{9} - \left( \frac{4*(3n+4)}{9*4*4^{n}} - \frac{9(n+1)}{9*4*4^{n}} \right)
$$
$$
=\frac{4}{9} - \left( \frac{12n+16-9n-9}{9*4*4^{n}} \right)
$$
$$
=\frac{4}{9} - \left( \frac{3n+7}{9*4*4^{n}} \right)
$$
$$
= \frac{4}{9}-\frac{3(n+1)+4}{9*4^{n+1}}
$$

## (2) 6 Punkte 
Man ermittle alle komplexen Lösungen der quadratischen Gleichung
$$
iz^{2} − 2z − 2i = 0
$$
$$
z^{2}-\frac{2}{i}z-\frac{2i}{i}
$$
$$
z^{2}-\frac{1}{i}*2*z -2
$$
$$
z^{2}- \frac{-i}{i*-i}*2*z -2
$$
$$
z^{2}- \frac{-i}{1}*2*z -2
$$
$$
z^{2}+2iz-2
$$
$$
z_{1,2} = -\frac{2i}{2}\pm \sqrt{ \frac{2i^2}{4}-(-2) }
$$
$$
z_{1,2} = -i\pm \sqrt{ \frac{4*-1}{4}+2 }
$$
$$
z_{1,2} = -i\pm \sqrt{ 1 }
$$
$$
z_{1} = 1 - i, z_{2} = - 1 - i
$$
$$
r_{1} = \sqrt{ 2 } ,args_{1} = \arctan(-1) = -\frac{\pi}{4} + 2\pi = \frac{7\pi}{4}
$$

Argument liegt im 2. oder 3. quadranten also + pi
$$
z_{2} = \sqrt{ 2 }, args_{2} = \arctan\left( \frac{-1}{-1} \right)  +\pi= -\frac{-\pi}{4} + \pi = \frac{5\pi}{4}
$$
und gebe diese sowohl in kartesischer Form als auch in Polarform an.
## (3) 7 Punkte 
Überprüfen Sie mit Hilfe einer Elementtabelle die Gültigkeit der nachfolgend angegebenen Mengeninklusion (wobei ∆ die symmetrische Differenz von Mengen bezeichnet). Geben Sie dabei unbedingt an, wie Sie aus der Elementtabelle dies entscheiden können.

(A ∆ B) ∩ C ⊆ (A ∩ C) ∪ (B ∩ C).

| A   | B   | C   | $A\vartriangle B$ | $A \vartriangle B \cap C$ | $A \cap C$ | $B \cap C$ | $(A \cap C) \cup (B \cap C)$ |
| --- | --- | --- | ----------------- | ------------------------- | ---------- | ---------- | ---------------------------- |
| 0   | 0   | 0   | 0                 | 0                         | 0          | 0          | 0                            |
| 0   | 0   | 1   | 0                 | 0                         | 0          | 0          | 0                            |
| 0   | 1   | 0   | 1                 | 0                         | 0          | 0          | 0                            |
| 0   | 1   | 1   | 1                 | 1                         | 0          | 1          | 1                            |
| 1   | 0   | 0   | 1                 | 0                         | 0          | 0          | 0                            |
| 1   | 0   | 1   | 1                 | 1                         | 1          | 0          | 1                            |
| 1   | 1   | 0   | 0                 | 0                         | 0          | 0          | 0                            |
| 1   | 1   | 1   | 0                 | 0                         | 1          | 1          | 1                            |
Da jedes Element was in $A \vartriangle B \cap C$ auch in $A \cap C \cup B \cap C$ enthalten ist, entspricht dieser einer Teilmenge von zweiterem.