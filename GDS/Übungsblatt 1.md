## Aufgabe 1 [[Zahlenumwandlungen]] 

Gegeben sind folgende Zahlen $A=(239.3359375)_{10}$ und $B = (53.625)_{10}$.

Wandeln Sie die Zahlen A und B direkt in die nachfolgend angegebenen Zahlensysteme um. Geben Sie zuerst das nicht gerundete Ergebnis und danach das gerundete Ergebnis auf n Nachkommastellen an. Runden Sie Ihr Ergebnis durch Abschneiden der späteren Nachkommastellen.

- a) Binärsystem (Zahl zur Basis $b = 2$), $n = 4$

Vorkommaanteil:
$239 ~mod~ 2 = 1$
$119 ~mod ~2 = 1$
$59 ~mo d~ 2 = 1$
$29 ~mo d~ 2=1$
$14 ~mo d~2=0$
$7 ~mo d~2=1$
$3 ~mo d~2=1$
$1 ~mo d~2=1$

$239_{10} = (11101111)_{2}$

Nachkommaanteil:

$\lfloor 0.3359375 * 2  \rfloor = \lfloor 0.671875 \rfloor = 0$
$\lfloor 0.671875 *2 \rfloor = \lfloor 1.343750 \rfloor = 1$
$\lfloor 0.34375 *2 \rfloor = \lfloor 0.68750 \rfloor = 0$
$\lfloor 0.6875*2 \rfloor = \lfloor 1.3750 \rfloor = 1$
$\lfloor 0.375*2 \rfloor = \lfloor 0.75 \rfloor = 0$
$\lfloor 0.75*2 \rfloor = \lfloor 1.5 \rfloor = 1$
$\lfloor 0.5*2 \rfloor = \lfloor 1 \rfloor = 1$
$\lfloor 0*2 \rfloor$ Abbruch

$0.3359375_{10}=0.0101011_{2}$

Nicht gerundetes Ergebnis $11101111.0101011_{2}$
Gerundetes Ergebnis $11101111.0101_{2}$

Vorkommaanteil:
$53 ~mo d~2=1$
$26 ~mo d~2=0$
$13 ~mo d~2=1$
$6 ~mo d~2=0$
$3 ~mo d~2=1$
$1 ~mo d~2 = 1$

$53_{10}=110101_{2}$

Nachkommaanteil:
$\lfloor 0.625*2 \rfloor = \lfloor 1.25 \rfloor = 1$
$\lfloor 0.25 * 2 \rfloor = \lfloor 0.5 \rfloor=0$
$\lfloor 0.5*2 \rfloor = \lfloor 1.0 \rfloor=1$
$\lfloor 0*2 \rfloor$Abbruch

$0.625_{10}=0.101$

Nicht gerundetes/gerundetes Ergebnis $110101.101_{2}$

- b) Hexadezimalsystem (Zahl zur Basis $b = 16$), $n = 2$

Vorkommaanteil:

$239 ~mod~ 16 = 15$
$14 ~mod~16=14$

$239_{10}=EF_{16}$

Nachkommaanteil:
$\lfloor 0.3359375 *16 \rfloor= $

- c) Oktalsystem (Zahl zur Basis $b = 8$), $n = 1$

## Aufgabe 2 [[Zahlenumwandlungen]]

Führen Sie die folgenden Umwandlungen ohne Umweg über das Dezimalsystem durch.

- a)  Wandeln Sie die Binärzahl $(1001 1111.1011 0101)_{2}$ in eine quarternäre Zahl (Zahl zur Basis $b = 4$) um.

- b) Wandeln Sie die Hexadezimalzahl $(27F5.B6)_{16}$ in eine binäre Zahl um.

- c) Wandeln Sie die ternäre Zahl $(22201001.110221)_{3}$ in eine Zahl zur Basis $b = 9$ um

## Aufgabe 3 [[Rechnen im Binärsystem]]
Es sind folgende Zahlen gegeben
$A = (101011.101)_{2}$
$B = (11010.11)_{2}$
$C = (10.01)_{2}$
$D = (–1010.1)_{2}$
$E = (1100100.001)_{2}$

Führen Sie mit diesen Zahlen die folgenden arithmetischen Operationen binär durch. 
Berechnen Sie die Ergebnisse exakt und geben Sie Ihren Rechenweg an.

- a) Addition: A + B
- b) Subtraktion: $A – B$
- c) Multiplikation: $A*D$
	Hinweis: Anzahl der Nachkommastellen des Produkts = Summe der Anz. d. NKSt der Faktoren
- d) Division: $\frac{E}{C}$
	Hinweis: Komma kann bei Divisor und Dividend um dieselbe Anzahl in dieselbe Richtung verschoben werden, ohne das Ergebnis zu beeinflussen


## Aufgabe 4: [[Zahlendarstellungen]]
Es sind folgende Zahlen gegeben:
$$A = (–90)_{10}
B = (DB)_{16}
C = (0)_{9}$$
Geben Sie die Zahlen A, B und C als 9 Bit lange Maschinenwörter in den nachfolgenden Zahlendarstellungen jeweils in binärer und in hexadezimaler Notation an. Falls es in einer Zahlendarstellung für dieselbe Zahl unterschiedliche Darstellungen gibt, geben Sie alle an.
Beispiel für Notationen:

binäre Notation: $(1 1110 0111)_2$
hexadezimale Notation: $(1E7)_{16}$

- a) Vorzeichen und Betrag
- b) Einerkomplementdarstellung
- c) Zweierkomplementdarstellung
- d) Exzessdarstellung ($Exzess = 28 – 1$)
## Aufgabe 5: Rechnen in unterschiedlichen [[Zahlendarstellungen]]
Folgende Maschinenwörter sind gegeben: $Z1 = (10100001)_{2}$ und $Z2 = (00001011)_{2}$.
Interpretieren Sie $Z1$ und $Z2$ als Binärzahlen, die beide jeweils in einer der nachfolgend angegebenen Darstellungen a) bis c) codiert sind. Führen Sie damit die Berechnung
$–(Z1 + Z2)$ (Addition von $Z1$ und $Z2$ und anschließende arithmetische Negation des Ergebnisses)
mit einer Maschinenwortlänge von 8 Bit binär durch und geben Sie Zwischenschritte an. Geben Sie
das Endergebnis der Berechnung auch als decodierte Dezimalzahl an.

- a) Darstellung durch Vorzeichen und Betrag
- b) Zweierkomplementdarstellung
- c) Exzessdarstellung mit Exzess $e = (01100100)_{2}$


Aufgabe 6: Genauigkeit von Zahlenumwandlungen
Wandeln Sie die Zahl (14.8198)10 in eine Bin¨arzahl mit 2 Nachkommastellen um – alle weiteren Nach-
kommastellen werden abgeschnitten (truncate, Rundung durch Abschneiden).
a) Berechnen Sie den absoluten und den relativen Rundungsfehler, der bei der Umrechnung ins
Bin¨arsystem entstanden ist.
b) Durch die Rundung werden alle reellen Zahlen aus einem Intervall [a, b[ ∈ R auf dieselbe Bin¨arzahl
abgebildet. Geben Sie die dezimalen Werte a, b f¨ur das Intervall an, in dem (14.8198)10 liegt.
Aufgabe 7: IEEE 754 Gleitpunktzahlen
Stellen Sie die nachfolgenden Zahlen A und B im Single Precision-Format (mit implizitem ersten Bit) des
IEEE 754 Gleitpunkt-Zahlensystems dar.
A = (–101.375)10 B = (0.6B)16
Aufgabe 8: Codierung von Gleitpunktzahlen
Gegeben ist ein Gleitpunkt-Zahlensystem F(2, 5, –14, 15, true), die Codierung erfolgt analog zum IEEE
754 Single Precision-Format.
Hinweis: Durch diese Vorgabe folgt unter anderem, dass obiges Format eine implizite Darstellung des
ersten Bits verwendet und somit eine Wortl¨ange von 10 Bit (1 Bit Vorzeichen, 5 Bit Exponent und 4 Bit
Mantisse) besitzt. Weiters ergibt sich (15)10 = (1111)2 f¨ur den Exzess des Exponenten.
In diesem Gleitpunkt-Zahlensystem sind die nachfolgenden Codew¨orter gegeben. Geben Sie zu jedem
Codewort die entsprechende Dezimalzahl oder die symbolische Bedeutung (z.B.: +∞, NaN, . . .) an.
a) 0 10001 0111
b) 1 00000 0000
c) 0 00000 1000
d) 0 11111 0000
e) 0 11111 1000