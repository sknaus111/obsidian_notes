## Buch 2.1
Jemand wirft $2n-mal$ eine Münze. Wieviele verschiedene Spielverläufe gibt es, wenn gleich oft Kopf wie Adler auftreten soll. 

$$
\binom{2n+k-1}{n}
$$

## Buch 2.2
Wie viele Möglichkeiten gibt es, drei (voneinander unterscheidbare) Würfel so zu werfen, dass genau zwei dieselbe Augenzahl zeigen

$$
6 * 3 * 5
$$
## Buch 2.3

Man bestimme die Anzahl der möglichen Tottotipps $(1,2,X)$ die bei 12 Spielen und die Anzahl der möglichen richtigen Zehner 

$$
3^{12}
$$
$$
\binom{12}{10} * 2^{2}
$$
## Buch 2.4
Man berechne
### a
Wie viele "Wörter" der Länge 28 gibt es, bei denen genau 5-mal der Buchstabe $a$, 14-mal $b$, 5-mal $c$, 3-mal $c$ vorkommen und genau einmal $e$ vorkommt

$$
\frac{28!}{5!14!5!3!}
$$

### b

Wie viele Wörter der Länge $28$ aus denen Buchstaben $a,b$ gibt es, die genau 5-mal $a$ enthalten und zwischen je zwei $a$ mindestens 3-mal den Buchstaben $b$

$$
k=28-(4*4+1)=11
$$
$$
n=6
$$
$$
\binom{n+k-1}{k}=\binom{16}{11}
$$

## Buch 2.5
Wie viele Möglichkeiten gibt es, 23 verschieden große Kugeln so zu färben, dass 9 rot, 5 schwarz, 4 blau, 4 grün sind und eine weiß ist

$$
\frac{23!}{9!5!4!4!}
$$

## Buch 2.6
Wie viele Möglichkeiten gibt es, aus einem 32-bändigem Lexikon genau 7 Bücher auszuwählen, wobei zwischen zwei ausgewählten Bändern immer mindestens einer im Regal stehen bleiben sollen

$$
k=32-(6*2+1)=19
$$
$$
n=8
$$
$$
\binom{n+k-1}{k}=\binom{26}{19}
$$
## Buch 2.7
Man beantworte folgende Fragen für das "6 aus 45"-Lotto:
### a
Wie groß ist die Anzahl der möglichen richtigen Fünfer( d.h. die Anzahl derjenigen 6-elementigen Teilmengen von $\{ 1,2,\dots,45 \}$ die mit einer vorgegebenen 6-elementigen Teilmenge genau 5 Elemente gemeinsam haben)

$$
\binom{6}{5}*39
$$
### b
Wie groß ist die Anzahl der möglichen richtigen Fünfer mit Zusatzzahl (d.h die Anzahl derjenigen 6-elementigen Teilmengen von $\{ 1,2,\dots,45 \}$, die mit einer vorgegebenen 6-elementigen Teilmenge genau 5 Elemente gemeinsam haben und deren sechstes Element einen vorgegebenen Wert außerhalb der 6-elementigen Menge hat
$$
\binom{6}{5}
$$
### c
Wie viele verschiedene Tipps müssen beim Lotto "6 aus 45" abgegeben werden, um sicher einen Sechser zu erzielen? Wie viele verschiedene Tipps sind nötig, um mit Sichherheit mindestens einmal in den Gewinnrängen (d.h. Dreier oder besser) zu sein? Bei wie vielen möglichen Tipps stimmt mindestens eine Zahl, bei wie vielen sind alle Zahlen falsch

Sechs aus 45
$$
\binom{45}{6}
$$
drei oder besser
$$
\binom{6}{3}\binom{39}{3}+\binom{6}{4}\binom{39}{2}+\binom{6}{5}\binom{39}{1}+\binom{6}{6}\binom{39}0{}
$$
mindestens eine
$$
\binom{45}{6}-\binom{6}{0}\binom{39}{6}
$$
keine
$$
\binom{6}{0}\binom{39}{6}
$$

## Buch 2.8
Wie viele natürliche Zahlen $n<100 000$ enthalten in ihrer Dezimalentwicklung genau dreimal die Ziffer drei bzw. genau viermal die Ziffer zwei

5 positionen für zahlen
$$
\binom{5}{3}
$$
mal den übrigen beiden ziffern
$$
\binom{5}{3}*9*9
$$
$$
\binom{5}{4}
$$
mal der übrigen ziffer
$$
\binom{5}{4}*9
$$
## Buch 2.9
Man beweise die Formel

$$
\binom{2n}{n} = \sum_{k=0}^{n}\binom{n}{k}^{2}=\sum_{k=0}^{n}\binom{n}{k}\binom{n}{n-k}
$$
(Hinweis: man betrachte die Koeffizienten von $x^{n}$ in der Identität $(1+x)^{n}(1+x)^{n}=(1+x)^{2n}$)
$$
(1+x)^{n}(1+x)^{n}=(1+x)^{2n} \implies \sum_{k=0}^{n}\binom{n}{k}1^{n-k}x^{k}*\sum_{k=0}^{n}\binom{n}{k}1^{n-k}x^{k}
$$
$$
\implies \sum _{k=0}^{n}\sum_{k=0}^{n}\binom{n}{k}^{2}1^{2(n-k)}x^{k}
$$
Da n-k immer positiv kann der ausdruck weggelassen werden
$$
\sum_{k=0}^{n}\sum_{k=0}^{n}\binom{n}{k}^{2}x^{2k}
$$
$$
\sum_{k=0}^{n}\sum_{k=0}^{n}\binom{n}{k}^{2}1^{2k}=\sum_{k=0}^{n}\binom{n}{k}^{2} * \sum_{k=0}^{n}1^{2k}=\sum_{k=0}^{n}\binom{n}{k}^{2} * 1 = \sum_{k=0}^{n}\binom{n}{k}\binom{n}{n-k}$$

## Buch 2.10
Man beweise die Beziehung $\binom{n+1}{k+1} =\binom{n}{k+1}+\binom{n}{k}$ durch Interpretation von $\binom{n}{k}$ als Anzahl der k-elementigen Teilmenge einer n-elementigen Menge

$$
\frac{(n+1)!}{(k+1)!(n-k)!} = \frac{n!}{(k+1)!(n-k-1)!} + \frac{n!}{k!(n-k)!}
$$
$$
=  \frac{n!*n-k}{(k+1)!(n-k)!}+ \frac{n!*(k+1)}{(k+1)!(n-k)!}
$$
$$
=\frac{n!*(n-k)+n!*(k+1)}{(k+1)!(n-k)!}
$$
$$
=\frac{n*n! - n!*k + n! * k + n!}{(k+1)!(n-k)!}
$$
$$
=\frac{n*n!+n!}{(k+1)!(n-k)!}
$$
$$
= \frac{n! * (n+1)}{(k+1)!(n-k)!}
$$
$$
= \frac{(n+1)!}{(k+1)!(n-k)!}
$$
## Buch 2.11
Die folgenden Aufgaben sollen mit dem Inklusions-Exklusions-Prinzip bearbeitet werden.
### a
In einer Menge von $n$ Personen können $10$ Personen Deutsch, $7$ Englisch, $5$ Französisch, $6$ Deutsch und Englisch, $4$ Deutsch und Französisch, $3$ Englisch und Französisch, 3 alle drei Sprachen und niemand keine der drei Sprachen. Wie groß ist $n$

$$
|Personen|=|Deutsch|+|Englisch|+|Französisch| - |Deutsch+Englisch| - |Deutsch+Französisch| - |Englisch + Französisch| + |Deutsch+Englisch+Französisch|
$$
$$
10+7+5-6-4-3+3=22-13+3=12
$$

### b
Wie viele natürliche Zahlen $n$ mit $1 \leq n \leq 10^{6}$ gibt es, die weder Quadrat, noch dritte, vierte oder fünfte Potenz einer natürlichen Zahl sind. 

Seien $Z_{2},Z_{3},Z_{4},Z_{5}$ die Mengen an zahlen die eine $j$-te Potenz einer anderen natürlichen Zahl sind und $Z_{4}$ in $Z_{2}$ enthalten
$$
Z'_{2}\cap Z'_{3}\cap Z'_{5}=Z-Z_{2}-Z_{3}-Z_{5}+|Z_{2}\cap Z_{3}|+|Z_{2}\cap Z_{5}| + |Z_{3} \cap Z_{5}| - |Z_{2} \cap Z_{3} \cap Z_{5}|
$$

$$
Z_{2} = \sqrt{ 1000000 } = 1000, Z_{3} = \sqrt[3]{ 1000000 } = 100, Z_{5}=15
$$
$$
Z_{2}\cap Z_{3}=Z_{6}=10, Z_{2}\cap Z_{5}=Z_{10}=3, Z_{3}\cap Z_{5}=Z_{15}=2
$$
$$
Z_{2}\cap Z_{3} \cap Z_{5} = 1
$$
$$
1000000-1000-100-15+10+3+2-1=1000000-1101=998899
$$

### c
Wie viele natürliche Zahlen $n$ mit $1\leq n \leq 10^{3}$ gibt es, die durch 3 und 5, aber weder durch 9 noch durch 11 teilbar sind.

$$
N_{3}, N_{5}, N_{9}, N_{11}
$$

$$
|N_{3,5}|-|N_{3,5}\cap N_{9}|-|N_{3,5}\cap N_{11}|+|N_{3,5}\cap N_{9}\cap N_{11}|
$$
$$
N_{3,5}\frac{1000}{15}=66.
$$
$$
N_{9}=111, N_{11}=90
$$
$$
N_{3,5}\cap N_{9}=N_{45}=22
$$
$$
N_{3,5}\cap N_{11}=N_{161}=6
$$
$$
N_{3,5} \cap N_{11} \cap N_{9} = N_{495}=2
$$
$$
66-22-6+2=40
$$
### d
Wie viele natürliche Zahlen $n$ mit $1 \leq n \leq 10^{6}$ gibt es, die weder durch 2 teilbar noch Quadratzahlen, noch dritte, noch vierte Potenzen natürlicher Zahlen sind

$Z_{4}$ in $Z_{2}$ enthalten
$$
Z_{2} = 1000, Z_{3} = 100, Z_{|2} = 500000
$$
$$
Z_{2} \cap Z_{3} = Z_{6} = 10, Z_{2} \cap Z_{|2} = 500, Z_{3} \cap Z_{|2} = 50
$$
$$
Z_{6} \cap Z_{|2} = 5
$$
$$
1000000-1000-100-500000+10+500+50-5=-501105+560= 1105-560=545, 1000000-500545 = 499455
$$
### e
Man bestimme die Anzahl aller Anordnungen (Permutationen) der Buchstaben $a,b,c,d,e,f,g$ in denen weder der Block "$a,b,c,d$" noch der Block "$f,a$" vorkommt.

$$
7!-(4*3!)-(6*5!)+(3*2!)
$$
### f
Auf wie viele Arten können 8 Türme auf ein Schachbrett gestellt werden derart, dass sie einander nicht schlagen und die weiße Diagonale frei bleibt? (Ein Turm schlägt eine andere Figur, die horizontal oder vertikal auf gleicher Höhe steht, sofern keine weitere Figur dazwischen steht)


Schwarze Felder
$$
4*4*3*3*2*2 = 576
$$
#### Nochmal anschauen

