## Aufgabe 1: (7 Punkte)
Man beweise mittels vollständiger Induktion für alle $n ∈ \mathbb{N}$:
$$
\sum_{k=1}^{n}(3k-1)(3k+2)=3n^{3}+6n^{2}+n
$$
Dabei müssen alle Elemente eines Induktionsbeweises angeführt und die kennengelernten
Bezeichnungen angegeben werden.

#Induktionsvoraussetzung
$$
\sum_{k=1}^{n}(3k-1)(3k+2)=3n^{3}+6n^{2}+n
$$
#Induktionsanfang
$$
(3-1)(3+2) = 3+6+1
$$
$$
9 +6 -3 -2= 10
$$
$$
10 = 10
$$
#Induktionsbehauptung
$$
\sum_{k=1}^{n+1}(3k-1)(3k+2)=3(n+1)^{3}+6(n+1)^{2}+(n+1)
$$
$$
= 3((n^{2}+2n+1)(n+1))+6(n^{2}+2n+1)+n+1
$$
$$
3(n^{3}+n^{2}+2n^{2}+2n+n+1)+6n^{2}+12n+6+n+1
$$
$$
3n^{3}+3n^{2}+6n^{2}+6n+3n+3+6n^{2}+12n+6+n+1
$$
$$
3n^{3}+15n^{2}+22n+10
$$
#Induktionsschritt
$$
=3n^{3}+6n^{2}+n + (3(n+1)-1)(3(n+1)+2)
$$
$$
= 3n^{3}+6n^{2}+n + (3n+2)(3n+5)
$$
$$
= 3n^{3}+6n^{2}+n+9n^{2}+15n+6n+10
$$
$$
= 3n^{3}+15n^{2}+22n+10
$$

## Aufgabe 2: (7 Punkte)

### (a) (3 Punkte) 
Bestimmen Sie mit Hilfe des Euklidischen Algorithmus $d := ggT (522, 231)$.

$$
522 = 231 * 2 + 60
$$
$$
231 = 60 * 3 + 51
$$
$$
60 = 51 * 1 +9
$$
$$
51 = 9 * 5 + 6
$$
$$
9 = 6 * 1 + 3
$$
$$
6 = 3 * 2 + 0
$$
$$
ggT(522,231)=3
$$
### (b) (4 Punkte) 
Unter Benützung von Punkt (a) bestimmen Sie ganze Zahlen $x$ und $y$,
sodass $522x + 231y = 6$.

$$
3 = 9-6*1
$$
$$
3= 9 - (51-9*5)*1
$$
$$
3 = 6*9 - 51 * 1
$$
$$
3 = 6 * (60-51*1) - 51 * 1
$$
$$
3 = 6 * 60 - 51 * 7
$$
$$
3 = 6 * 60 - (231-60*3) * 7
$$
$$
3 = 27 * 60 - 231 *7
$$
$$
3 = 27 * (522-231*2) - 231 * 7
$$
$$
3 = 522 * 27 - 61 * 231 
$$
$$
6 = 522 * 54 - 122 * 231
$$
$$
x = 54, y = -122
$$
## Aufgabe 3: (6 Punkte)
Beweisen Sie die folgende Identität mittels einer Elementtafel oder geben Sie ein kon-
kretes Gegenbeispiel an:
$$
(A \backslash B) ∩ C = A \backslash (B ∩ C).
$$

| A   | B   | C   | $A\backslash B$ | $A\backslash B \cap C$ | $B\cap C$ | $A\backslash B\cap C$ |
| --- | --- | --- | --------------- | ---------------------- | --------- | --------------------- |
| 0   | 0   | 0   | 0               | 0                      | 0         | 0                     |
| 0   | 0   | 1   | 0               | 0                      | 0         | 0                     |
| 0   | 1   | 0   | 0               | 0                      | 0         | 0                     |
| 0   | 1   | 1   | 0               | 0                      | 1         | 0                     |
| 1   | 0   | 0   | 1               | 0                      | 0         | 1                     |
| 1   | 0   | 1   | 1               | 1                      | 0         | 1                     |
| 1   | 1   | 0   | 0               | 0                      | 0         | 1                     |
| 1   | 1   | 1   | 0               | 0                      | 1         | 0                     |
Stimmt nicht im Fall dass das Element in A B und nicht in C ist.