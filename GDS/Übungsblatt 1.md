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
$\lfloor 0.3359375 *16 \rfloor= \lfloor 3.359375+6*0.3359375 \rfloor$
$0.3359375*6$
$2.0156250$
$3.359375 +$
$5.375$
$\lfloor 5.375 \rfloor = 5$
$\lfloor 0.375 *16 \rfloor = \lfloor 3.75+6*0.375 \rfloor$
$0.375*6$
$2.25$
$3.75+$
$6$
$\lfloor 6 \rfloor = 6$

Nicht gerundet/gerundetes Ergebnis $EF.56_{16}$

Vorkommaanteil:

$53 ~mo d~ 16 = 5$
$3 ~mo d~16=3$

$53_{10}=35_{16}$

Nachkommaanteil:
$\lfloor 0.625*16 \rfloor = \lfloor 6.25 + 6*0.625 \rfloor$
$0.625*6$
$3.75$
$6.25+$
$10$
$\lfloor 10 \rfloor=10$

Nicht gerundet/gerundetes Ergebnis $35.A_{16}$

- c) Oktalsystem (Zahl zur Basis $b = 8$), $n = 1$

Vorkommaanteil:
$239 ~mo d~8=7$
$29 ~mo d~8=5$
$3 ~mo d~8 = 3$

$239_{10}=357_{8}$

Nachkommaanteil:
$\lfloor 0.3359375*8 \rfloor$
$0.3359375*8$
$2.6875$
$\lfloor 2.6875 \rfloor = 2$ 
$\lfloor 0.6875 *8\rfloor$
$5.5$
$\lfloor 5.5 \rfloor = 5$
$\lfloor 0.5*8 \rfloor$
$4.0$
$\lfloor 4.0 \rfloor = 4$

$0.3359375_{10}=254_{8}$

Nicht gerundetes Ergebnis $357.254_{8}$
Gerundetes Ergebnis $357.2_{8}$

Vorkommaanteil:

$53 ~mo d~8=5$
$6 ~mo d~8=6$

$53_{10}=65_{8}$

Nachkommaanteil
$\lfloor 0.625*8 \rfloor$
$5.0$
$\lfloor 5.0 \rfloor = 5$

Nicht gerundetes/Gerundetes Ergebnis $65.5_{8}$
## Aufgabe 2 [[Zahlenumwandlungen]]

Führen Sie die folgenden Umwandlungen ohne Umweg über das Dezimalsystem durch.

- a)  Wandeln Sie die Binärzahl $(1001 1111.1011 0101)_{2}$ in eine quarternäre Zahl (Zahl zur Basis $b = 4$) um.

Vorkommateil:
$1001 1111_{2} ~m od~100_{2}=11_{2} = 3_{4}$
$1001 11_{2} ~mo d~100_{2}=3_{4}$
$1001 ~mo d~100_{2}=1_{3}$
$10 ~mod~ 100_2=2_{4}$

$1001 1111_{2}=2133_{4}$

Nachkommateil:
$1011 0101_{2} ~mo d~100_{2}=1_{4}$
$1011 01_{2} ~mo d~100_{2}=1_{4}$
$1011_{2}~mo d~100_{2}=3_{4}$
$10_{2}~mo d~100_{2}=2_{4}$

$10110101_{2}=1132_{4}$

$1001 1111.1011 0101_{2} = 2133.1132_{4}$

- b) Wandeln Sie die Hexadezimalzahl $(27F5.B6)_{16}$ in eine binäre Zahl um.

Vorkommateil:
$5*16^0+15*16^1+7*16^2+2*16^3$
$0101 * 2^4$

- c) Wandeln Sie die ternäre Zahl $(22201001.110221)_{3}$ in eine Zahl zur Basis $b = 9$ um

Vorkommateil:
$22201001 ~mo d~9=$

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
$~~011010.110+$
$1000110.011$
- b) Subtraktion: $A – B$
$101011.101$
$011010.110-$
$_{1}~~~~~~~~~_{1}~_{1}$
$010000.111$

- c) Multiplikation: $A*D$
$~~~~~~~~~~~~~~~~-1010.1*101011.101$

$~~~~~~~~~~~~~~~~-10101$
$~~~~~~~~~~~~~~~~~~~00000$
$~~~~~~~~~~~~-10101$
$~~~~~~~~~~-10101$
$~~~~~~~~-10101$
$~~~~~~~~~~~00000$
$~~~~-10101$
$~~~~~~~00000$
$~~$$-10101$
$~~~~~~~~~~~~~~~~~~~~~~~~~$
$~~~~~0000000000001$

$~~~~~0000000000101$

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





4607.5221

7\*8^0+0+6*\*8^2+4\*8^3+5*8 ^ -1 + 2 * 8 ^ -2 + 2 * 8 ^ -3 + 1 * ^ -4
7+6 * 8 * 8+ 4 * 8 *8 * 8 +5 * 1/8 + 2 * 1/64 +

7+24+360+2048+5/8+1/32
393+2048
2451 + 0.625

011 110 110 000.101 010 110 101
3660.5265

10001010
01100100
00100100 

10000 / 110 = 0 1 0
1000
---110


103.131

0.131 * 2 = 0.262 0
0.262 *2  = 0.5 0

7 mod 4 =3
1 mod 4 

805.983

805 mod 2 = 1
402 mod 2 = 0
201 mod 2 = 1
100 mod 2 = 0
50 mod 2 = 0
25 mod 2 = 1
12 mod 2 = 0
6 mod 2 = 0
3 mod 2 = 1
1 mod 2 = 1

1100100101.

.983 * 2 = 1.966 = 1
0.966 * 2 =

11110.
11011

0+2+4+8+16=30

0.5+0.25+0.125*0+0.0625+0.03125
0.03125
0.0625
0.125
0.25
0.5
0.9685

EF4.0EF = 1110 1111 0100. 0000 1110 1111

1111000
1111110
11110110

 100100:1001=100
-1001
 00000
 -0000
  00000 

28+16

421 mod 8 = 5
52 mod 8 = 4
6 mod 8 = 6


.956 * 8 = 8.548 = 8
0.548 * 8 = 4.384 = 4
0.384 * 8 = 3.072 = 3


645.843

10100.
10011

0+0+4+0+16 = 20
0.5+0+0+0.0625 + 0.03125 = 0.593

4030.61010

100 000 011 000 , 110 001 000 001 000

1110100
1101111
11100011

 110010:1110=011
-0000
 11001
  -1110
   10110  
.....-1110
........1000

39 mod 8 = 4

332.882

332 mod 2 = 0
166 mod 2 = 0
83 mod 2 = 1
41 mod 2 = 1
20 mod 2 = 0
10 mod 2 = 0
5 mod 2 = 1
2 mod 2 = 0
1 mod 2 = 1

101001100.111

.882 *2 = 1.764=1
0.764 *2 = 1.528 = 1
0.528 * 2 = .

11010.11111

0+2+0+8+16 = 26

0.5+0.25+0.125+0.0625+0.03125
0.03125
0.06250
0.12500
0.25000
0.50000
0.96875

DA0.35C

110110100000,001101011100

10110001
01101001-
01001000

  1111000/1001=1101
-1001
..01100
 .-1001
 ...00110
 .-00000
   .......1100
   ......-1001
................0011

39+26=62

3*16+9=48

312.649

312 mod 8 = 0
39 mod 8 = 7
7 mod 8 4

740.514

.649 * 8 = 5.192 = 5
0.192 *8 = 1.536 = 1
0.536 * 8 = 4.288 4

5707.5512

((((5 * 8+7)*8+0)*8+7))
47*  * 8 = 376
376 * 8 = 2400+

4008

0.5512
((((2/8+1)/8+5)/8+5)/8)
1.25 / 8 
0.125+0.03125
0.15625 + 5 5.15625
5.15625/8

1 1000 1000 . 0110 1011 1111
1 8 8 . 6 B F

10100000
  1110010-
....0101110

.............1001 * 1110
..............0000
...........1001
.........1001
.......1001
...........1111110

9 mod 5 = 4
1

209.390

209 mod 8 = 1
26 mod 8 = 2
3 mod 8 = 3

321.307

0.39 * 8 = 3.12 = 3
0.12 * 8 = 0.96 = 0
0.96 * 8 = 7.68 = 7

11101.11001

1+0+4+8+16=29

0.5+0.25+0+0+0.03125

0.78125

676.076
 110 111 110. 000 111 110

 1101101
 1010011+
11000000

 1110001/1111=0111
-0000
 11100
 .-1111
 .011010
 ....-1111
 ...010111
 ......-1111
 ........1000
 
111100011
1+2+0+0+0+32+64+128
227

−371
+256+64+32+16+2+1
10101110011

10101110011
01010001100

1000110
0000011
1000011

111001
101111

e 52 = 110100

  111001
  101111+
1101000
  110100-
  100100

111001
110100-
000101

111010100

0+0+4+0+16+0+64+128

112

553
512+32+8+1

01000101001
10111010110

0010111100

1000000
-39 + e

1_000_000
64-39
25
11001

111010
110000

e = 58 = 111010

111010
111010-
000000

111010000
000101111

1+2+4+8+32 = 47

344
256+64+16+8
00101011000
11010100111
00000000001
11010101000

1010100 = e + 11100
1010100
0011100-
0111000

0111000

111000
100010
e = 48 110000

111000
110000-
001000
100010+
101010

111011111
000100000

355
256+64+32+2+1
10101100011

0010011111
1101100000

1001011  = -19 + e
0010011+
1011110

1000010
1000001
e = 54 110110
1000010
0110110-
0001100

101100011
1+2+0+0+0+32+64+256
355

238

128+64+32+8+4+2
00011101110
11100010001
00000000001+
11100010010

110111 = e -56
111000+
1101111

1000011
1001101
e = 1000000

1000011
1000000-
0000011
1001101+
1010000

C_e = 1010000 - 1000000
1010000
1000000-
0010000 = 

0 11101000101 0101

0.0625+0.25=0.3125

1 +0+4+0+0+0+64+0+256+512+1024=1840

1 10111 1 0001011 111

1.+0.0625+0.015625+0.0078125+0.00390625+0.001953125+0.0009765625
1.0927734375

10111-15

10111
01111-
01000=

1.0927734375 * 2^8
279,75

1 00000 0 000 000 101 0

0.5 0.25 0.125

0.0625 0.03125 0.015625

0.0078125 + 0.001953125 = -0.009765625

96.78

96 mod 2 = 0
48 mod 2 = 0
24 mod 2 = 0
12 mod 2 = 0
6 mod 2 = 0
3 mod 2 = 1
1 mod 2 = 1

1100000

.78 * 2 = 1.56 = 1
.56 * 2 = 1.12 = 1
0.12 * 2 = 0.24 = 0
0.24 * 2 = 0.48 = 0

0.48 * 2 = 0.96 = 0
0.96 * 2 = 1.92 = 1
0.92 * 2 = 1.84 = 1
0.84 * 2 = 1.68 = 1

0.68 * 2 = 1.36 = 1
0.36 * 2 = 0.72 = 0
0.72 * 2 = 1.44 = 1
0.44 * 2 = 0.88 = 0

0.88 * 2 = 1.76 = 1
0.76 * 2 = 1.52 = 1
0.52 * 2 = 1.04 = 1
0.04 * 2 = 0.08 = 0

0.16=0
0.32=0

11 0000  .  1100 0111 1010 1110 00
1.1 0000 1100 0111 1010 1110 00* 2^5


00000101
01111111+
10000100

1 110011 1 1001

0.5+0+0+0.0625
0.5625

1+2+0+0+16+32=51

51+.5625

1 01011 1 11 0100 0100

1+0.5+0.25+0.0625+0.00390625

1.81640625

  01111
  01011-
-00100

2^-4*1.81640625

0 00000 0 01 1110 0111
0+0+0.25+0.125+0.0625+0.03125+0+0+0.00390625
3125 / 2 = 1562.5 = 0.01
15625/2= 7812.5 = 0.007
78125/2=390625 = 0.003

0.00390625
0.03125000
0.06250000
0.12500000
0.25000000
0.47265625

81.54

81 mod 2 = 1
40 mod 2 = 0
20 mod 2 = 0
10 mod 2 = 0
5 mod 2 = 1
2 mod 2 = 0
1 mod 2 = 1
1010001

17 Stellen

0.54 * 2 = 1.08 = 1
0.08 * 2 = 0.16 = 0
0.16 * 2 = 0.32 = 0
0.32 * 2 = 0.64 = 0

0.64 * 2 = 1.28 = 1
0.28 * 2 = 0.56 = 0
0.56 * 2 = 1.12 = 1
0.12 * 2 = 0.24 = 0

0.24 * 2 = 0.48 = 0
0.48 * 2 = 0.96 = 0
0.96 * 2 = 1.92 = 1
0.92 * 2 = 1.84 = 1

0.84 * 2 = 1.68 = 1
0.68 * 2 = 1.36 = 1
0.36 * 2 = 0.72 = 0
0.72 * 2 = 1.44 = 1

0.44 * 2 = 0.88 = 0

101 0001 . 1000 1010 0011 1101 0

1.01 0001 1000 1010 0011 1101 0 * 2^6


1 1 1010 1100 _ 1 _ 0110

0+0+4+8+0+32+0+64+128=236

0.25+0.125 = .375

010 00=8

0 01001 11 1101 1010

0.5+0.25+0.125+0.0625+0+0.015625+0.0078125+0+0.001953125
0.03125 0.00390625

0.5
0.25
0.125
0.0625
0.015625
0.0078125
0.001953125
0.962890625

1.962890625

01001 = 9 - 15 = -6

0.015625*1.962890625= 0,030670166015625

0 00000 - 0 - 11 0010 0001

0.5+0.25+0.03125+0,0009765625
0.5
0.25
0.03125
0.0009765625
0.7822265625

0.7822265625 * 2^-14
0,000047743320465087890625

53.73
53 mod 2 = 1
26 mod 2 = 0
13 mod 2 = 1
6 mod 2 = 0
3 mod 2 = 1
1 mod 2 = 1

110101

18 Nachkomma
0.73 * 2 = 1.46 = 1
0.46 * 2 = 0.92 = 0
0.92 * 2 = 1.84 = 1
0.84 * 2 = 1.68 = 1

0.68 * 2 = 1.36 = 1
0.36 * 2 = 0.72 = 0
0.72 * 2 = 1.44 = 1
0.44 * 2 = 0.88 = 0

0.88 * 2 = 1.76 = 1
0.76 * 2 = 1.52 = 1
0.52 * 2 = 1.04 = 1
0.04 * 2 = 0.08 = 0

0.08 * 2 = 0.16 = 0
0.16 * 2 = 0.32 = 0
0.32 * 2 = 0.64 = 0
0.64 * 2 = 1.28 = 1

0.28 * 2 = 0.56 = 0
0.56 * 2 = 1.12 = 1

1011 1010 1110 0001 01

11 0101 . 1011 1010 1110 0001 01
1.1 0101 1011 1010 1110 0001 01 * 2^5

01111111
00000101+
10000100

10101101110101110000101

0 1 1110 0011 1110

0.5
0.25
0.125
0.875

0011
+1+2

1110
+32+64+128

1
+256

001
002
032
064
128
256
483

0 110 01 00 1101 0011
11001
01111-
01010

01010
+2+8=10

11001 = 16+8+1=25-15=10


10110=16+4+2=22-15=7

0 10110 10 0111 0101

1+
0.5
0.0625
0.03125
0.015625
0.00390625
0.0009765625
0.6142578125

0.6142578125*2^7

0 10110 1001 110.101

+0+2+4
8+0+0+64
02
04
08
64
78

78

0.5
0.125
0.625

0 11111 0101000010
NaN

51.52

51 mod 2 = 1
25 mod 2 = 1
12 mod 2 = 0
6 mod 2 = 0
3 mod 2 = 1
1 mod 2 = 1

110011

18 Nachkommastellen
0.52 * 2 = 1.04 = 1
0.04 * 2 = 0.08 = 0
0.08 * 2 = 0.16 = 0
0.16 * 2 = 0.32 = 0

0.32 * 2 = 0.64 = 0
0.64 * 2 = 1.28 = 1
0.28 * 2 = 0.56 = 0
0.56 * 2 = 1.12 = 1

0.12 * 2 = 0.24 = 0
0.24 * 2 = 0.48 = 0
0.48 * 2 = 0.96 = 0
0.96 * 2 = 1.92 = 1

0.92 * 2 = 1.84 = 1
0.84 * 2 = 1.68 = 1
0.68 * 2 = 1.36 = 1
0.36 * 2 = 0.72 = 0

0.72 * 2 = 1.44 = 1
0.44 * 2 = 0.88 =0

1000 0101 0001 1110 10

11 0011 . 1000 0101 0001 1110 10
1.1 0011 1000 0101 0001 1110 10 * 2^5

10000100

0 1 0111 1010      0011

0.125
0.0625
0.1875

002 
008 
016 
032 
064 
256
........
378

001 00=4 -15 = -11

1 01100 11 0010 1100

01100=12-15=-3

0.0011 1001 0110 0

0.125 
0.0625 
0.03125 
0.00390625 
0,0009765625 
0,00048828125
0.22412109375



0 00000 1100 0011 11


0.5
0.25
0.0078125
0.00390625
0,001953125
0,0009765625
0.7646484375 * 2^-14

0,000046670432080078125

47.87

47 mod 2 = 1
23 mod 2 = 1
11 mod 2 = 1
5 mod 2 = 1
2 mod 2 = 0
1 mod 2 = 1

101111

18 nachkommastellen
0.87 * 2 = 1.74 = 1
0.74 * 2 = 1.48 = 1
0.48 * 2 = 0.96 = 0
0.96 * 2 = 1.92 = 1

0.92 * 2 = 1.84 = 1
0.84 * 2 = 1.68 = 1
0.68 * 2 = 1.36 = 1
0.36 * 2 = 0.72 = 0

0.72 * 2 = 1.44 = 1
0.44 * 2 = 0.88 = 0
0.88 * 2 = 1.76 = 1
0.76 * 2 = 1.52 = 1

0.52 * 2 = 1.04 = 1
0.04 * 2 = 0.08 = 0
0.08 * 2 = 0.16 = 0
0.16 * 2 = 0.32 = 0

0.32 * 2 = 0.64 = 0
0.64 * 2 = 1.28 = 1

1101 1110 1011 1000 01

101111 . 1101 1110 1011 1000 01
1.01111 . 1101 1110 1011 1000 01 * 2^5

01111110111101011100001

01101
01010-
00011

1.1111000101
1.0011011111

0.0011111000101
1.0011011111

0011111000
0011011111+
0111010111

1.0111010111 101

1011010111010111

0.010111101101

0101111011010
1000111010 +
1110110101

1100101110110101


11100110000 * 10010100100
=010.00010101101011000000

01010 + 10100 - 01111

01010 = -5
10100+ = 5
11110

11110
01111-

01111=0


1 01111 _ 10 _ 00010101101011000000

1 10000 _ 1 _ 0000 1010 11 010 

1100000000101011 

10001 = 17
01101- = 13 
00100 = 4

A = 1.1111001111
B = 0.00010011000110

0.00010011000110
1.1111001111+
10.0000011011011

1.0000 0011 01 101 1 (Exponent 01110)

1.0000 0011 10 (Exponent 01110)

0000001110

1 00110 1110011001
0 01000 0110101100

01000 = 8
00110 = 6
00010 = 2

0.011110011001

 01011 = 11
 00111 = 7

A: 1101001110
B: 0011010010
1.0011010010
0.00010011010010

00010011010010
1101001110
1110011011001

A: 0 00101 1111111010
B: 1 01001 1001010010

01001 = 9
00101 = 5
00100 = 4

0.00011111111010
00001111111

0.00011111111010
1.1001010010

00011111111010
1001010010
1011010001101
1011010010

0 01001 1011010010
0010011011010010

A: 1 01001 0000100011
B: 0 10001 0000000111

10000100011 * 10000000111
10000100011
222222222222
2222222222222
22222222222222
222222222222222
2222222222222222
22222222222222222
222222222222222222
2222222210000100011
22222222210000100011
222222222210000100011

100001000110000000000
000000001000010001100
000000000100001000110
000000000010000100011
100001010100011110101

100001010100011110101

01001 = 9
10001 = 17
11010 = 26
01111 = 15
01011 = 11

1.0000 1010 10 001 1110101
0000101010

++1+011+0000



++1+011+100

11+0+++1+++

11100111100

1100111111

++0+111+11

11+1+++0++

4+8=12

x^3+x
1010

x^3 * (x^3+x)
x^6+x^4 : x^3+x=x^3

1010000

0111010
x^1+x^3+x^4+x^5

x^5+x^4+x^3+0+x^1+0 : x^3 = x^2+x^1+1
0 + x^4 + x^3 +0 +x^1+0
0 + 0 +     x^3 + 0 + x^1 + 0
 0+ 0 + 0+ 0+ x^1

| q   | 0.37 | Antwort 1 Frage 1 |
| --- | ---- | ----------------- |
| u   | 0.23 |                   |
| r   | 0.18 | Antwort 2 Frage 1 |
| t   | 0.16 | Antwort 4 Frage 1 |
| s   | 0.06 | Antwort 3 Frage 1 |
|     |      |                   |

s + t = 0.22 = 0 1

(st) + r = 0.40

q+u = 0.6

(qu)+((st)r)=1

s = 010
t = 011
r = 00
u = 10
q = 11

0.3 * ld(0.3)+0.3 * ld(0.3)+0.3 * ld(0.3) + 0.1ld(0.1)

1,737 * 0.3 * 3 + 0.1 * 3,322

0.3 * 2 + 0.3 * 3 + 0.3 * 3 + 0.1 * 4 = 2.8

| x   | y   | z   | x xor z | y nand x | ynx implies xxz | z nand y | zny and z | x equiv znyaz |
| --- | --- | --- | ------- | -------- | --------------- | -------- | --------- | ------------- |
| 0   | 0   | 0   | 0       | 1        | 0               | 1        | 0         | 1             |
| 0   | 0   | 1   | 1       | 1        | 1               | 1        | 1         | 0             |
| 0   | 1   | 0   | 0       | 1        | 0               | 1        | 0         | 1             |
| 0   | 1   | 1   | 1       | 1        | 1               | 0        | 0         | 1             |
| 1   | 0   | 0   | 1       | 1        | 1               | 1        | 0         | 0             |
| 1   | 0   | 1   | 0       | 1        | 0               | 1        | 1         | 1             |
| 1   | 1   | 0   | 1       | 0        | 1               | 1        | 0         | 0             |
| 1   | 1   | 1   | 0       | 0        | 1               | 0        | 0         | 0             |
