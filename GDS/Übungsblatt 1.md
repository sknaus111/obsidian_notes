## Aufgabe 1 [[Zahlenumwandlungen]] 

Gegeben sind folgende Zahlen $A=(239.3359375)_{10}$ und $B = (53.625)_{10}$.

Wandeln Sie die Zahlen A und B direkt in die nachfolgend angegebenen Zahlensysteme um. Geben Sie zuerst das nicht gerundete Ergebnis und danach das gerundete Ergebnis auf n Nachkommastellen an. Runden Sie Ihr Ergebnis durch Abschneiden der späteren Nachkommastellen.

- a) Binärsystem (Zahl zur Basis $b = 2$), $n = 4$

Vorkommateil:
$239 \mod 2 = 1$
$119 \mod 2 = 1$
$59 \mod 2 = 1$
$29 \mod 2 = 1$
$14 \mod 2 = 0$
$7 \mod 2 = 1$
$3 \mod 2 = 1$
$1 \mod 2 = 1$

Nachkommateil:
$0.3359375 * 2 = 0.6718750 = 0$
$0.671875 * 2 = 1.343750 = 1$
$0.34375 * 2 = 0.68750 = 0$
$0.6\dots = 1$

$(1110~1111.0101)$

Vorkommateil:
$53 \mod 2 = 1$
$26 \mod 2 = 0$
$13 \mod 2 = 1$
$6 \mod 2 = 0$
$3 \mod 2 = 1$
$1 \mod 2 = 1$

Nachkommateil:
$0.625*2 =1.250 = 1$
$0.25 * 2 = 0.5 = 0$
$0.5 *2 = 1$

$(1101~01.1010)$

- b) Hexadezimalsystem (Zahl zur Basis b = 16), n = 2

$1110~1111.0101$
$EF.5$

$11~0101.1010$
$35.A$

- c) Oktalsystem (Zahl zur Basis $b = 8$), $n = 1$

$11~101~111.010~100$
$357.24$

$110~101.101$
$65.5$
## Aufgabe 2 [[Zahlenumwandlungen]]

Führen Sie die folgenden Umwandlungen ohne Umweg über das Dezimalsystem durch.

- a)  Wandeln Sie die Binärzahl $(1001 1111.1011 0101)_{2}$ in eine quarternäre Zahl (Zahl zur Basis $b = 4$) um.

$10~01~11~11.10~11~01~01$
$2133.2311$

- b) Wandeln Sie die Hexadezimalzahl $(27F5.B6)_{16}$ in eine binäre Zahl um.

$27F5.B6$
$0010~0111~1111~0101.1011~0110$

- c) Wandeln Sie die ternäre Zahl $(22201001.110221)_{3}$ in eine Zahl zur Basis $b = 9$ um

$22~20~10~01.11~02~21$
$8631.427$

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
$~~101011.101$
$~~~~11010.11$
$1000110.011$
- b) Subtraktion: A – B
$101011.101$
$~~11010.110$
$010000.111$

- c) Multiplikation: $A*D$

$101011.101 * 1010.1$
$101011101$
$~~~~101011101$
$~~~~~~000000000$
$~~~~~~~~101011101$
$1110010100001$
$-111001010.0001$


	Hinweis: Anzahl der Nachkommastellen des Produkts = Summe der Anz. d. NKSt der Faktoren
- d) Division: $\frac{E}{C}$

$1100100001 / 10010 = 101100.1$
$10010$
$00111$
$001110$
$0011100$
$0010010$
$0001010$
$00010100$
$00010010$
$00000010$
$000000100$
$0000001001$
$00000010010$

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

$-(0~0101~1010)_{2}$ $(0~1101~1011)_{2}$ $(000000000)_{2}$
$-(05A)_{16}$ $(0DB)_{16}$ $(000)_{16}$

- b) Einerkomplementdarstellung

$(1~1010~0101)_{2}$ $(0~1101~1011)_{2}$ $(1~1111~1111)_{2}$

- c) Zweierkomplementdarstellung

$(1~1010~0110)_{2}$ $(0~1101~1011)_{2}$ $(0~0000~0000)$

- d) Exzessdarstellung ($Exzess = 2^{8} – 1$)

$e=11111111$

$011111111$
$001011010-$
$010100101$

$011011011$
$~~11111111+$
$111011010$

$011111111$
$000000000+$
$011111111$
## Aufgabe 5: Rechnen in unterschiedlichen [[Zahlendarstellungen]]
Folgende Maschinenwörter sind gegeben: $Z1 = (10100001)_{2}$ und $Z2 = (00001011)_{2}$.
Interpretieren Sie $Z1$ und $Z2$ als Binärzahlen, die beide jeweils in einer der nachfolgend angegebenen Darstellungen a) bis c) codiert sind. Führen Sie damit die Berechnung
$–(Z1 + Z2)$ (Addition von $Z1$ und $Z2$ und anschließende arithmetische Negation des Ergebnisses)
mit einer Maschinenwortlänge von 8 Bit binär durch und geben Sie Zwischenschritte an. Geben Sie
das Endergebnis der Berechnung auch als decodierte Dezimalzahl an.

- a) Darstellung durch Vorzeichen und Betrag

$~~0100001$
$00001011$-
$00010110$

$10010110$

$00010110$

2+4+16=22

- b) Zweierkomplementdarstellung

$10100001$
$00001011$
$10101100$

$10101100$
$00000001-$
$10101011$
$01010100 = 4+16+64=84$ 

- c) Exzessdarstellung mit Exzess $e = (01100100)_{2}$

$e=01100100$

$10100001$
$00001011+$
$10101100$
$01100100-$
$01001000$

$01100100$
$01001000-$
$00011100$

$00011100 = 4+8+16=28$
$01100100+$
$10000000$

## Aufgabe 6: Genauigkeit von Zahlenumwandlungen
Wandeln Sie die Zahl $(14.8198)_{10}$ in eine Binärzahl mit 2 Nachkommastellen um – alle weiteren Nachkommastellen werden abgeschnitten (truncate, Rundung durch Abschneiden).


# VIDEO

- a) Berechnen Sie den absoluten und den relativen Rundungsfehler, der bei der Umrechnung ins Binärsystem entstanden ist.

- b) Durch die Rundung werden alle reellen Zahlen aus einem Intervall $[a, b[ ∈ \mathbb{R}$ auf dieselbe Binärzahl abgebildet. Geben Sie die dezimalen Werte $a, b$ für das Intervall an, in dem $(14.8198)_{10}$ liegt.

## Aufgabe 7: IEEE 754 Gleitpunktzahlen
Stellen Sie die nachfolgenden Zahlen A und B im Single Precision-Format (mit implizitem ersten Bit) des IEEE 754 Gleitpunkt-Zahlensystems dar.
$$A = (–101.375)_{10}$$
# VIDEO

$$ B = (0.6B)_{16}$$
	
## Aufgabe 8: Codierung von Gleitpunktzahlen
Gegeben ist ein Gleitpunkt-Zahlensystem $F(2, 5, –14, 15, true)$, die Codierung erfolgt analog zum IEEE 754 Single Precision-Format.

Hinweis: Durch diese Vorgabe folgt unter anderem, dass obiges Format eine implizite Darstellung des ersten Bits verwendet und somit eine Wortlänge von 10 Bit (1 Bit Vorzeichen, 5 Bit Exponent und 4 Bit Mantisse) besitzt. Weiters ergibt sich $(15)_{10} = (1111)_{2}$ für den Exzess des Exponenten.

In diesem Gleitpunkt-Zahlensystem sind die nachfolgenden Codewörter gegeben. Geben Sie zu jedem Codewort die entsprechende Dezimalzahl oder die symbolische Bedeutung $(z.B.: +∞, NaN, . . .)$ an.

# VIDEO

- a) 0 10001 0111
- b) 1 00000 0000
- c) 0 00000 1000
- d) 0 11111 0000
- e) 0 11111 1000

