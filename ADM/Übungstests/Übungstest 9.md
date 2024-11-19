## 1. (7 Punkte) 
Für welche $n ∈ \mathbb{N}$ ist die Ungleichung $2n < 2^{n}$ erfüllt? Zeigen Sie die Ungleichung für diese $n ∈ \mathbb{N}$ mittels vollständiger Induktion. Geben Sie dabei alle Elemente eines Induktionsbeweises mit ihrer Bezeichnung an.

#Induktionsvoraussetzung
$$
2n<2^{n}
$$
#Induktionsanfang
$$
2<2^{1}
$$
$$
2*2< 2^{2}
$$
$$
4<4
$$
$$
2*3<2^{3}
$$
$$
6 < 8
$$
#Induktionsbehauptung
$$
2(n+1) < 2^{n+1}
$$

#Induktionsschritt
$$
2*(2n)<2*2^{n}
$$
$$
4n < 2^{n+1}
$$
$$
2n + 2*3 < 2^{n+1}
$$
$$
2(n+1)=2n+2<2n+2*3<2^{n+1}
$$
Wahr für alle $n\geq 3$
## 2. (a) (3 Punkte) 
Bestimmen Sie mit dem Euklidischen Algorithmus den ggT(122, 42).

$$
122 = 42 * 2 + 38
$$
$$
42 = 38 * 1 + 4
$$
$$
38 = 4*9 +2
$$
$$
4 = 2*2 +0
$$
$$
ggT(122,42)=2
$$
## (b) (4 Punkte) 
Bestimmen Sie unter Benützung von Punkt (a) ganze Zahlen $x, y ∈ \mathbb{Z}$ mit
$$122x + 42y = 2$$$$
2 = 38 -4*9
$$
$$
2 = 38 - 9*(42-38*1)
$$
$$
2 = 10 * 38 - 42 * 9
$$
$$
2 = 10 *(122-42*2 )-42*9
$$
$$
2 = 10 * 122 - 29 * 42
$$
$$
x=10, y=-29
$$
## 3. (6 Punkte) 
Überprüfen Sie mit Hilfe einer Wahrheitstafel die Gültigkeit der Äquivalenz
$$a ∧ (b ∧ ¬c) ⇐⇒ ¬((a ⇒ ¬b) ⇒ c).$$
Dabei seien a, b und c Aussagenvariablen. Geben Sie auch an, wie Sie die Gültigkeit aus
der Wahrheitstafel ablesen können.

| a   | b   | c   | $\lnot b$ | $\lnot c$ | $b \land \lnot c$ | $a \land (b \land \lnot c$ | $a \implies \lnot b$ | $(a \implies \lnot b) \implies c$ | $\lnot((a \implies \lnot b)\implies c)$ |
| --- | --- | --- | --------- | --------- | ----------------- | -------------------------- | -------------------- | --------------------------------- | --------------------------------------- |
| 0   | 0   | 0   | 1         | 1         | 0                 | 0                          | 1                    | 0                                 | 1                                       |
| 0   | 0   | 1   | 1         | 0         | 0                 | 0                          | 1                    | 1                                 | 0                                       |
| 0   | 1   | 0   | 0         | 1         | 1                 | 0                          | 1                    | 0                                 | 1                                       |
| 0   | 1   | 1   | 0         | 0         | 0                 | 0                          | 1                    | 1                                 | 0                                       |
| 1   | 0   | 0   | 1         | 1         | 0                 | 0                          | 1                    | 0                                 | 1                                       |
| 1   | 0   | 1   | 1         | 0         | 0                 | 0                          | 1                    | 1                                 | 0                                       |
| 1   | 1   | 0   | 0         | 1         | 1                 | 1                          | 0                    | 1                                 | 0                                       |
| 1   | 1   | 1   | 0         | 0         | 0                 | 0                          | 0                    | 1                                 | 0                                       |
Die Aussage ist nicht gültig

Beispiel
$a=0,b=0,c=0$