## 146) 
Seien $f : A → B$ und $g : B → C$ zwei Abbildungen, sodass $g ◦ f$ surjektiv und $g$ injektiv ist.
Man zeige, dass dann auch $f$ surjektiv ist.

Gegeben: Für $g\circ f$ Zu jedem $b\in B$ gibt es ein $a\in A$, für $g$ zu jedem $c\in C$ höchstens ein $b\in B$
$g(f(a))=g(b_{1})=b_{2}$
$g(b_{1})=g(b_{2})\implies b_{1}=b_{2}$

$g(f(a_{1}))=g(b_{1})=b_{2}=b_{1}=g(b_{2})=g(f(a_{2}))$

Beweisen: Für $f$ Zu jedem $b\in B$ gibt es ein $a\in A$, $f(a)=b$?

## 167) 
Wieviele Möglichkeiten gibt es, aus einem $50$-bändigen Lexikon genau $6$ Bücher auszuwählen,
wobei zwischen zwei ausgewählten Bänden immer mindestens drei im Regal stehen bleiben sollen?

Anders überlegt zieht man 5 mal Bücher mit den drei leeren Büchern danach + 1 Buch am Ende.
$5*4+1=29=k$

$n$ ist wie im Kugelbeispiel des Buches ein Trenner. Diese kommen 5 mal zwischen den Büchern und vor und nach ihnen vor
$5+2=7=n$

Auswahl einer Teilmultimenge
$$\binom{n-k-1}{k}=\binom{7+29-1}{29}=\binom{35}{29}$$

## 170) 
Man bestimme die Anzahl der möglichen Tototipps $(1, 2, x)$ bei $12$ Spielen und die Anzahl
der möglichen richtigen Zehner. (D. h. die Anzahl derjenigen Tipps, die mit einer vorgegebenen
Kolonne an genau $10$ der $12$ Stellen übereinstimmen.)

Wie im Buch Anzahl möglicher Tips: $3^{12}$



Anzahl von $12$ versch. Sachen $10$ richtig zu haben. Aus einem Sack mit unbegrenzten $(1,2,x)$ wird eines genommen wobei 10 von 12 Elementen korrekt sein müssen.
$$
\binom{12}{10}
$$
Da die 2 falschen Antworten $2$ verschiedene Möglichkeiten haben wird die Anzahl der möglichen Auswahlen mit $4$ multipliziert.
$$
\binom{12}{10}*4=264
$$
## 204) 
Man bestimme die Anzahl aller Anordnungen (Permutationen) der Buchstaben $a, b, c, d, e, f, g$ , in denen weder der Block ”$abcd$“ noch der Block ”$fa$“ vorkommt.

Sei $W$ die Menge an Permutationen von den Buchstaben $a,b,c,d,e,f,g$
So sei $W_{abcd}$ die Menge welche den Block $abcd$  enthält und $W_{fa}$ die menge welche den Block $fa$  enthält. Nun ist die Menge der gesuchten Wörter

$$
W_{abcd}' \cap W_{fa}'
$$

Daraus folgt
$$
|W_{abcd}' \cap W_{fa}'| = |W| - |W_{abcd}| - |W_{fa}| + |W_{abcd}\cap W_{fa}|
$$
$|W|$ ist $7!= 5040$, $|W_{abcd}|$ ist jede Position von dem Block multipliziert mit den Möglichkeiten der anderen Buchstaben also
$$
4 * 3!= 24
$$
$|W_{fa}|$ nach dem gleichen Prinzip
$$
6* 5! = 720
$$
$|W_{abcd}\cap W_{fa}|$ ist 
$$
3 * 2! = 6
$$
Somit
$$
5040-24-720+6=4302
$$