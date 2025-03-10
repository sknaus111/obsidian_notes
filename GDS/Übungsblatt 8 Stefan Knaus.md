0## Aufgabe 1: Formale Sprachen
### a) 
Berechnen Sie das Ergebnis der folgenden Ausdrücke.

- (i) $((\{a, ab\} ∪ \{ε\}) · (\{ε, bb, cc\} ∪ \{b\})) ∪ \{a, c\}$
  $(\{ a,ab \}\cup \{ \varepsilon \}) \implies \{ a,ab \}$ $(\{\varepsilon,bb,cc\} \cup \{ b \}) \implies \{ \varepsilon ,b,bb,cc\}$
  $(\{ a,ab \}\cdot  (\{ \varepsilon,b,bb,cc \})) \implies \{ a,ab,abb,acc,abbb, abcc \}$
  $\{ a,c,ab,abb,acc,abbb,abcc \}$
- (ii) $\{a, bc\}^{2} · \{\}$ 
  $\{ aa,abc,bca,bcbc \} \cdot \{  \} \implies \{  \}$
  $\{  \}$
- (iii) $\{a, bc\}^{2} ∪ \{\}^{*}$
  $\{ aa,abc,bca,bcbc \} \cup \{  \}$
  $\{ aa,abc,bca,bcbc \}$
- (iv) $\{a, bc\}^{2} · \{\}^{*}$
  $\{ \dots \}\cdot \{  \}$
  $\{  \}$
- (v) $(\{a\}^{*} · \{a\}^{+}) · \{a\}^{*}$
  $(\{ \varepsilon,a \}\cdot \{ a \}) \implies (\{ a,aa \})$
  $(\{ a,aa \}\cdot \{ \varepsilon,a \})$
  $\{ a,aa,aaa \}$


### b) 
Überlegen Sie für jede der folgenden Aussagen, welche Sprachen L sie erfüllen. Wenn die Aus-
sage von keiner oder allen Sprachen erfüllt wird, argumentieren Sie diesen Sachverhalt. Gilt eine
Aussage für manche Sprachen, aber nicht für andere, geben Sie je eine Beispielsprache an, d.h.,
geben Sie eine Sprache an, für die die Aussage gilt, und eine, für die die Aussage nicht gilt.

- (i) $L · \{\} = L ∪ \{ε\}$
  Gilt für keine Sprache, da $L\cdot \{  \}$ immer $\{  \}$ ist und eine Sprache vereinigt mit dem Leerwort mindestens das Leerwort enthält
- (ii) $L · \{ε\} = L ∪ \{\}$
  Gilt für alle Sprachen, da mit der Kombination des Leerworts nichts verändert wird und mit der Vereinigung der leeren Sprache nichts verändert wird.
- (iii) $\{ε\} · L^{*} = L^{+}$
  Gilt für: $\{ \varepsilon \}$
  Gilt nicht für: $\{ a \}$ $\{ \varepsilon,a \}\not=\{ a \}$
- (iv) $L ⊆ L^{2}$
  Gilt für: $\{ \varepsilon,a \}$, $\{ \varepsilon,a \}\subseteq \{ \varepsilon,a,aa \}$
  Gilt nicht für: $\{ a \}$, $\{ a \}\not\subseteq \{ aa \}$


## Aufgabe 2: Reguläre Sprachen und endliche Automaten 1
Sei $Σ$ das Alphabet $\{a, k, l, r\}$ und L die Menge aller Wörter über $Σ$, die entweder $karl$ oder $ara$ enthalten. Beispiele für solche Wörter sind $karl$ und $ara$ selber, aber auch die Wörter $kararl$ und $karla$ liegen in L.

### a) 
Geben Sie einen regulären Ausdruck in der Notation der Posix Extended Regular Expressions an,
der die Sprache L beschreibt.

$Sprache=Symbol^{*}\cdot\{ K,A \}\cdot Symbol^{*}$
$Karl=\{ k \}\cdot \{ a \}\cdot \{ r \}\cdot \{ l \}$
$Ara=\{ a \}\cdot \{ r \}\cdot \{ a \}$
$Symbol=\{ a,k,l,r \}$

$.(karl|ara).$
### b) 
Geben Sie einen nichtdeterministischen Automaten an, der die Sprache L akzeptiert. Der Automat soll der Definition der Sprache direkt entsprechen, sodass die Korrektheit der Modellierung
unmittelbar einsichtig ist.

![[Pasted image 20250117164347.png]]

### c) 
Konstruieren Sie mit Hilfe des in der Vorlesung besprochenen Determinisierungsverfahrens zu
Ihrem nichtdeterministischen Automaten einen äquivalenten deterministischen.

| $\delta^{*}$ | a               | r   | k               | l   |
| ------------ | --------------- | --- | --------------- | --- |
| s            | $\{ s,a_{1} \}$ | s   | $\{ s,k_{1} \}$ | s   |
| k1           | k2              |     |                 |     |
| k2           |                 | k3  |                 |     |
| k3           |                 |     |                 | e   |
| a1           |                 | a2  |                 |     |
| a2           | a               |     |                 |     |
| e            | e               | e   | e               | e   |
SZ: s
EZ: e

| $\delta^{*}$          | a                     | r                     | k                 | l           |
| --------------------- | --------------------- | --------------------- | ----------------- | ----------- |
| $\{ s \}$             | $\{ s,a_{1} \}$       | $\{ s \}$             | $\{ s,k_{1} \}$   | $\{ s \}$   |
| $\{ s,a_{1} \}$       | $\{ s,a_{1} \}$       | $\{ s,a_{2} \}$       | $\{ s,k_{1} \}$   | $\{ s \}$   |
| $\{ s,k_{1} \}$       | $\{ s,a_{1},k_{2} \}$ | $\{ s \}$             | $\{ s,k_{1} \}$   | $\{ s \}$   |
| $\{ s,a_{2} \}$       | $\{ s,a_{1},e \}$     | $\{ s \}$             | $\{ s,k_{1} \}$   | $\{ s \}$   |
| $\{ s,a_{1},k_{2} \}$ | $\{ s,a_{1} \}$       | $\{ s,a_{2},k_{3} \}$ | $\{ s,k_{1} \}$   | $\{ s \}$   |
| $\{ s,a_{1},e \}$     | $\{ s,a_{1},e \}$     | $\{ s,a_{2},e \}$     | $\{ s,k_{1},e \}$ | $\{ s,e \}$ |
| $\{ s,a_{2},k_{3} \}$ | $\{ s,a_{1},e \}$     | $\{ s \}$             | $\{ s,k_{1} \}$   | $\{ s,e \}$ |
| $\{ s,a_{2},e \}$     | $\{ s,e \}$           | $\{ s,e \}$           | $\{ s,k_{1},e \}$ | $\{ s,e \}$ |
| $\{ s,k_{1},e \}$     | $\{ s,k_{2},e \}$     | $\{ s,e \}$           | $\{ s,k_{1},e \}$ | $\{ s,e \}$ |
| $\{ s,e \}$           | $\{ s,a_{1},e \}$     | $\{ s,e \}$           | $\{ s,k_{1},e \}$ | $\{ s,e \}$ |
| $\{ s,k_{2},e \}$     | $\{ s,e \}$           | $\{ s,k_{3},e \}$     | $\{ s,k_{1},e \}$ | $\{ s,e \}$ |

SZ: $\{ s \}$
EZ: $\{ s,a_{1},e \},\{ s,a_{2},e \},\{ s,k_{1},e \},\{ s,k_{2},e \},\{ s,e \}$

Vereinfacht zu


![[Pasted image 20250117171257.png]]

## Aufgabe 4: Reguläre Sprachen und Syntaxdiagramme
Die wesentlichen Eigenschaften eines Autoreifen sind seitlich in der folgenden Form vermerkt.
![[Pasted image 20250117183449.png]]

Die Spezifikation besteht aus den folgenden vier Teilen, die jeweils durch ein Leerzeichen (im Folgenden als ␣ notiert) getrennt sind.


1. Reifenbreite in mm (dreistellig), gefolgt von einem Schrägstrich und einer zweistelligen Zahl, die das Verhältnis von Reifenhöhe zu Reifenbreite in Prozent angibt;
2. Reifenbauart: R (Radial) oder D (Diagonalreifen); anschließend folgt der Buchstabe F, falls es sich um einen Notlaufreifen handelt.
3. Felgendurchmesser in Zoll: ein Wert zwischen 10 und 20
4. Tragfähigkeitsindex (eine zwei- oder dreistellige Zahl), gefolgt vom Geschwindigkeitsindex (ein oder zwei Großbuchstaben).


Ein Beispiel für eine gültige Reifenkennung: 205/55 ␣ R ␣16␣91V

Beschreiben Sie den Aufbau derartiger Reifenbeschriftungen mit den folgenden Methoden. Treffen
Sie sinnvolle Annahmen, wenn Ihnen Informationen fehlen.

### a) 
Geben Sie einen regulären Ausdruck in algebraischer Notation an. Nutzen Sie dabei die Möglichkeit Abkürzungen einzuführen um einen übersichtlichen und gut nachvollziehbaren Ausdruck zu erhalten.

$Reifen=B/VARAFATAG$
$A='␣'$
$B=DDD$
$V=DD$
$R=('R'+'D')(\varepsilon+'F')$
$F=((1)(D))(20)$
$T=DD(\varepsilon+D)$
$G=S(\varepsilon+S)$
$D=(0+\dots+9)$
$S=('A'+\dots+'Z')$

### b) 
Geben Sie einen regulären Ausdruck in der Notation der POSIX Extended Regular Expressions an,
der alle Zeilen beschreibt, die ausschließlich eine derartige Reifenbeschriftung enthalten.

$$
Rfn=[0-9][0- 9][0- 9]/[0- 9][0- 9]\text{␣}(R|D)F?\text{␣}((1[0- 9])|20)\text{␣}[0-][0- 9][0- 9]?\text{␣}[A-Z][A-Z]?
$$


### c) 
Geben Sie das Syntaxdiagramm an, das Ihrem regulären Ausdruck aus Teil a) entspricht.

![[Pasted image 20250117190751.png]]


## Aufgabe 5: Grammatik und Sprache
Die Papageien auf der Insel Jahatra haben eine Sprache entwickelt, die sich mit der Grammatik $G = ⟨V, T, P, A⟩$ beschreiben lässt, wobei


$$V = \{A, B, C\}$$
$$T = \{a, h, j, l, r, t\}$$
$$P = \{A → \text{"a" B "a"} ,$$
$$B → \text{"ha" B "al" | "ja" C "al} ,$$
$$C → \text{"ha" C "al" | "tr}\}.$$
Überprüfen Sie für die nachfolgenden Wörter, ob sie in der durch die Grammatik G spezifizierten Sprache L(G) liegen. Falls ja, geben Sie eine Ableitung an. Falls nein, argumentieren Sie, warum nicht.

### a) 
ahajahatralalala

$$
W=aBa
$$
$$
W=ahaBala
$$
$$
W=ahajaCalala
$$
$$
W=ahajahaCalalala
$$
$$
W=ahajahatralalala
$$
### b) 
ahajatrala

$$
W=aBa
$$
$$
W=ahaBala
$$
$$
W=ahajaCalala
$$
vordererteil entspricht der vorgabe und ist der einzige weg diesen zu generieren
hinterer teil aber anders, deswegen kein wort der sprache


Sind folgende Aussagen wahr oder falsch? Begründen Sie Ihre Antwort!
### c) 
Die Anzahl der a’s in jedem Wort der Sprache ist gerade.

Ja, da jedes mal wenn a's generiert werden, zwei Stück entstehen
### d) 
Jedes Wort enthält mindestens so viele al-Teile wie ja-Teile.

ja da jedes ja mit einem al generiert wird
### e) 
Jedes Wort enthält mindestens ein t.

ja da jedes wort nur mit tr enden kann

Überlegen Sie weiters:
### f) 
Wie lautet das kürzeste Wort der Sprache?

$W=aBa$
$W=ajaCala$
$W=ajatrala$
### g) 
Ist es möglich, die Sprache L(G) auch durch einen endlichen Automaten zu beschreiben? Falls ja,
geben Sie einen derartigen Automaten an. Falls nein, begründen Sie, warum das nicht geht.

nein da kontextfreie grammatiken mächtiger sind als automaten, und man sich in einem automaten nicht theoretisch unendlich a's merken kann, wie bei einer kontextfreien grammatik möglich