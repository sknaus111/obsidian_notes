## Cauchykriterium
Eine Reihe $\sum_{n\geq 0}a_{n}$ ist genau dann konvergent, wenn für alle $\varepsilon>0$ ein $N(\varepsilon)$ existiert, so dass $|\sum_{k=n}^{m}a_{k}|<\varepsilon$ für alle $m\geq n>N(\varepsilon)$.

## Alternierende Reihen
Eine Reihe $\sum_{n\geq 0}a_{n}$ heißt #alternierend, wenn die Glieder $a_{n}$ abwechselnd positiv und negativ sind.

### Konvergenzkriterium von Leibniz
Eine alternierende Reihe $\sum_{n\geq 0} (-1)^{n}a_{n}$, für die $(a_{n})_{n\geq 0}$ eine monoton fallende Nullfolge ist, ist konvergent.

#### Beweis
Wir betrachten die Teilfolgen $(s_{2 n})_{n\geq 0}$ und $(s_{2n +1})_{n\geq 0}$ der Partialsummenfolge. Da $a_{n}$ monoton fällt, ist
$$
s_{2n+1}=(a_{0}-a_{1})+(a_{2}-a_{3})+\dots+(a_{2n}-a_{2n+1})
$$
eine monoton wachsende Folge, da $a_{2k}-a_{2k+1}\geq 0$. Aus demselben Grund ist
$$
s_{2n}=a_{0} - (a_{1}-a_{2}) - (a_{3}-a_{4})-\dots-(a_{2n-1}-a_{2n})
$$
monoton fallend. Weiters gilt $0\leq s_{2n+1}\leq s_{2n}\leq a_{0}$. Daraus folgt, dass $(s_{2n+1})_{n\geq 0}$ und $(s_{2n})_{n\geq 0}$ beschränkt und daher wegen dem Hauptsatz über monotone Folgen konvergent sind. Sei $a= \lim_{ n \to \infty }s_{2n+1}$ und $b=\lim_{ n \to \infty }s_{2n}$. Dann gilt auch $0\leq s_{2n}-s_{2n+1}=a_{2n+1}\rightarrow 0$, also ist $a=b=\lim_{ n \to \infty }s_{n}$.

#### Beispiel
Die alternierende Reihe $\sum_{n\geq 1} \frac{-1^{n}}{n}$ erfüllt die Voraussetzungen von dem Konvergenzkriterium von Leibniz, denn in diesem Fall ist $a_{n}=\frac{1}{n}$ offensichtlich eine monoton fallende Nullfolge. Daher ist die Reihe konvergent.

Dieses Beispiel illustriert den Fall, dass eine Reihe $\sum a_{n}$ konvergiert, die Reihe $\sum |a_{n}|$ der Beträge der Glieder aber divergiert. Denn $\sum |a_{n}|$ ist in diesem Fall nichts anderes als die harmonische Reihe. Dies führt zu folgendem Begriff.

## Absolute und bedingte Konvergenz
Eine Reihe $\sum_{n\geq 0}a_{n}$ heißt #absolut_konvergent, wenn $\sum_{n\geq 0}|a_{n}|$ konvergent ist. Eine konvergente Reihe, welche nicht absolut konvergent ist, nennt man #bedingt_konvergent.

Eine absolute konvergente Reihe ist auch konvergent.

### Beweis
Sei $\sum_{n}a_{n}$ absolut konvergent. Aus dem Cauchykriterium folgt, dass gegebenes $\varepsilon>0$ ein $N$ existiert, so dass für alle $m\geq n>N$ 
$$
|a_{n}|+|a_{n+1}|+\dots+|a_{m}|<\varepsilon
$$
Eine Anwendung der Dreiecksgleichung ergibt
$$
|a_{n}+a_{n+1}+\dots+a_{m}|\leq |a_{n}|+|a_{n+1}|+\dots+|a_{m}|< \varepsilon
$$
und daraus folgt nach nochmaliger Anwendung von dem Cauchykriterium die Konvergenz von $\sum_{n}a_{n}$.

### Beispiel
Betrachten wir nochmals die Reihe $\sum_{n\geq 1} \frac{(-1)^{n}}{n}$. Wir haben bereits gesehen, dass es sich um eine konvergente Reihe handelt. Die aus den Beträgen ihrer Summanden gebildete Reihe ist aber die harmonische Reihe $\sum_{n\geq 1} \frac{1}{n}$, deren Divergenz wir bereits gezeigt haben. Diese Reihe ist daher ein Beispiel einer bedingt konvergenten Reihe.

Man kann zeigen, dass jede Umordnung einer absolut konvergenten Reihe gegen denselben Grenzwert konvergiert. Man spricht daher auch von unbedingt konvergenten Reihen. Für bedingt konvergente Reihen ist dies nicht der Fall. Es gilt nämlich der folgende Satz.

### Riemann'scher Umordnungssatz
Eine bedingt konvergente Reihe lässt sich so umordnen, dass sie gegen eine beliebige Zahl $\alpha\in \mathbb{R}\cup \{ -\infty,+\infty \}$ uneigentlich konvergiert.

### Majorantenkriterium
Seien $\sum_{n}a_{n}$ und $\sum_{n}b_{n}$ zwei Reihen mit $|a_{n}|\leq b_{n}$ für fast alle $n$. Falls $\sum_{n}b_{n}$ konvergent ist, so ist $\sum_{n}a_{n}$ absolut konvergent. In diesem Fall nennt man die Reihe $\sum_{n}b_{n}$ eine #Majorante von $\sum_{n}a_{n}$.
#### Beweis
Anwendung des Cauchykriteriums: Für alle $\varepsilon>0$ gibt es ein $N\in \mathbb{N}$, so dass
$$
\sum_{k=n}^{m}|a_{k}|\leq \sum_{k=n}^{m}b_{k}<\varepsilon
$$
für alle $m\geq n>N$. Daraus folgt die absolute Konvergenz von $\sum_{n}a_{n}$

Analog zum Konvergenzbeweis mittels Abschätzung nach oben durch konvergente Majoranten lässt sich auch ein Divergenzbeweis mittel Abschätzung nach unten durch divergente Minoranten durchführen. Man erhält

### Minorantenkriterium
Seien $\sum_{n}a_{n}$ und $\sum_{n}b_{n}$ zwei Reihen, so dass $0\leq a_{n}\leq b_{n}$ für fast alle $n$. Falls $\sum_{n}a_{n}$ divergent ist, so ist auch die Reihe $\sum_{n}b_{n}$ divergent.

#### Beispiel
Da $\frac{1}{n^{2}}$ eine monotone Nullfolge ist, folgt mit Hilfe des Leibnizkriteriums die Konvergenz von $\sum_{n\geq 1} \frac{-1^{n}}{n^{2}}$. Wir wollen nun zeigen, dass diese Reihe auch absolut konvergent ist. Dazu benutzen wir die Abschätzung $\frac{1}{n^{2}}\leq \frac{1}{n(n-1)}$ für $n\geq 2$. Wir wissen, dass
$$
\sum_{n\geq 2} \frac{1}{n(n-1)}=1
$$
Die Voraussetzungen des Majorantenkriteriums sind somit erfüllt, und daher konvergiert die Reihe $\sum_{n\geq 1} \frac{1}{n^{2}}$. Über den Grenzwert sagt das Majorantenkriterium nichts aus. Man kann aber zeigen, dass 
$$\sum_{n\geq 1} \frac{1}{n^{2}}=\frac{\pi^{2}}{6}$$
Es gilt weiters $\frac{1}{n^{\alpha}}\leq \frac{1}{n^{2}}$ für $\alpha\geq 2$. Infolge dessen ist die Reihe
$$
\sum_{n\geq 1} \frac{1}{n^{\alpha}}
$$
für alle $\alpha\geq 2$ konvergent. Man kann zeigen, dass dies sogar für alle $\alpha> 1$ gilt. Für $\alpha=1$ erhalten wir die harmonische Reihe, die bekanntlich divergent ist. 
#Hyperharmonische_Reihen sind konvergent für $\alpha>1$. Für $\alpha\leq 1$ sind sie divergent wie man durch Anwendung des Minorantenkriteriums leicht sieht.

### Wurzelkriterium
Falls es eine Zahl $q$ gibt, so dass
$$
\sqrt[n]{ |a_{n}| }\leq q < 1 \text{ für fast alle } n
$$
dann ist $\sum_{n}a_{n}$ absolut konvergent. Falls hingegen
$$
\sqrt[n]{ |a_{n}| } \geq 1 \text{ für unendlich viele }n
$$
so ist $\sum_{n}a_{n}$ divergent.

**Bemerkung**: Man beachte, dass die Konstante $q$ in der ersten Ungleichung wesentlich ist. Die Bedingung $\sqrt[n]{ a_{n} } \leq 1$ reicht nicht aus wie das folgende Beispiel zeigt

#### Beispiel
Für die divergente harmonische Reihe ist $\sqrt[n]{ |a_{n}| }= 1 / \sqrt[n]{ n }$ D.h., die Bedingung $\sqrt[n]{ a_{n} }\leq 1$ ist erfüllt. Ferner gilt $\sqrt[n]{ n }\rightarrow1$. Somit konvergiert auch $\sqrt[n]{ a_{n} }$ gegen $1$, also muss die Folge jede a priori vorgegebene Schranke $q<1$ überschreiten. Die erste Bedingung des Wurzelkriteriums ist somit verletzt.
Zu beachten ist aber, dass in diesem Fall auch die zweite Bedingung des Wurzelkriteriums nicht erfüllt ist. Mit Hilfe des Wurzelkriteriums kann also nicht für jede Reihe eine Entscheidung über Konvergenz bzw. Divergenz getroffen werden. 

#### Beweis
Aus $\sqrt[n]{ |a_{n}| }\leq q <1$ folgt, dass $|a_{n}|\leq q^{n}$ für fast alle $n$. Daher ist die geometrische Reihe $\sum_{n\geq 0}q^{n}$ eine konvergente Majorante, woraus die absolute Konvergenz von $\sum_{n}a_{n}$ folgt. Die Bedinung $\sqrt[n]{ |a_{n}| }\geq 1$ impliziert, dass $|a_{n}|\geq 1$ für unendlich viele $n$. Somit kann $(a_{n})_{n\geq 0}$ keine Nullfolge sein und daher $\sum_{n}a_{n}$ nicht konvergieren.

Eine leicht abgeschwächte, jedoch oft einfacher handhabbare Formulierung des Wurzelkriteriums ist die folgende.

### Limesform des Wurzelkriteriums
Aus $\lim\sup_{ n \to \infty }\sqrt[n]{ |a_{n}| }<1$ folgt die absolute Konvergenz der Reihe $\sum_{n}a_{n}$ und aus $\lim\sup_{ n \to \infty } \sqrt[n]{ |a_{n}| }>1$ deren Divergenz

Im Fall $\lim\sup_{ n \to \infty }\sqrt[n]{ |a_{n}| }=1$ ist wieder keine Aussage über das Konvergenzverhalten der Reihe möglich.

**Bemerkung**: Dass dieser Satz tatsächlich eine Abschwächung des Wurzelkriteriums ist, zeigt das triviale Beispiel $a_{n}=1$ für alle $n\in \mathbb{N}$. In diesem Fall ist das zweite Kriteriums des Wurzelkriteriums anwendbar, aber nicht die Limesform.

#### Beweis
Die Aussage $\sqrt[n]{ |a_{n}| }\leq q<1$ für fast alle $n$ ist äquivalent zu $\lim\sup_{ n \to \infty }\sqrt[n]{ |a_{n}| }<1$. Falls $\lim\sup_{ n \to \infty }\sqrt[n]{ |a_{n}| }>1$ so gilt sicherlich $\sqrt[n]{ a_{n} }\geq 1$ für unendlich viele $n$

### Quotienenkriterium
Es sei $a_{n}\not=0$ für alle $n\in \mathbb{N}$. Falls eine Zahl $q$ existiert, so dass
$$
\left| \frac{a_{n+1}}{a_{n}} \right|\leq q < 1 \text{ für fast alle }n
$$
so ist $\sum_{n}a_{n}$ absolut konvergent. Gilt hingegen
$$
\left| \frac{a_{n+1}}{a_{n}} \right|\geq 1 \text{ für fast alle }n
$$
so divergiert die Reihe $\sum_{n}a_{n}$

#### Beweis
Im ersten Fall gilt für einen Index $N$ und alle $n\geq N$ die Ungleichung $|a_{n+1}|\leq q|a_{n}|$ und daher $|a_{n}|\leq q^{n-N} a_{N}$. Daher ist die geometrische Reihe $\sum_{n}|a_{N}|q^{n-N}$ eine konvergente Majorante. 
Im Fall $\left| \frac{a_{n+1}}{a_{n}} \right|\geq 1$ für fast alle $n$ ist $|a_{n}|$ eine ab einem gewissen Index $N$ monoton wachsende Folge positiver Zahlen und damit sicherlich keine Nullfolge.

Auch beim Quotientenkriterium kann der Fall eintreten, dass keine der beiden Bedingungen zutrifft und daher keine Aussage über das Konvergenzverhalten der Reihe gemacht werden kann. Die harmonische Reihe ist etwa ein Beispiel, wo das Quotientenkriterium versagt.

### Limesform des Quotientenkriteriums
Aus $\lim\sup_{ n \to \infty } \left| a_{n+1}/a_{n} \right|<1$ folgt die absolute Konvergenz der Reihe $\sum_{n}a_{n}$ und aus $\lim\inf_{ n \to \infty }\left| a_{n+1}/a_{n}\right|>1$ deren Divergenz.

#### Beispiel
Man untersuche die Exponentialreihe
$$
\sum_{n\geq 0} \frac{x^{n}}{n!}=1+x+\frac{x^{2}}{2!}+\frac{x^{3}}{3!}+\dots
$$
für festes $x\in \mathbb{R}$. Es gilt
$$
\left|\frac{a_{n+1}}{a_{n}}\right| = \left| \frac{\frac{x^{n+1}}{(n+1)!}}{\frac{x^{n}}{n!}} \right|=\frac{|x|}{n+1}\leq \frac{1}{2} < 1
$$
für hinreichend große $n$, da $\frac{|x|}{n+1}$ eine Nullfolge ist. Das Quotientenkriterium sagt uns nun, dass $\sum_{n\geq 0} \frac{x^{n}}{n!}$ für alle $x\in \mathbb{R}$ konvergiert.

Gegeben sei die Reihe $\sum_{n\geq 1} \frac{n!}{n^{n}}$. Wieder führt das Quotientenkriterium zum Ziel.
$$
\left| \frac{a_{n+1}}{a_{n}} \right| = \frac{(n+1)n^{n}}{(n+1)^{n+1}} = \left(1+ \frac{1}{n}\right)^{-n} \leq \frac{1}{2} < 1 \text{ für }n\geq 1
$$
und daher ist die Reihe konvergent.

Sei $a_{2n}= \frac{1}{4^{n}}$ und $a_{2n+1}=\frac{1}{4^{n-1}}$. Dann ist
$$
\frac{a_{n+1}}{a_{n}} = \Bigg \{ \begin{matrix}
4 \text{ falls }n \text{ gerade}\\
\frac{1}{16} \text{ falls }n \text{ ungerade}
\end{matrix}
$$
Daher gilt $\lim\sup_{ n \to \infty }a_{n+1}/a_{n}=4$ und $\lim\inf_{ n \to \infty }a_{n+1}/a_{n}=\frac{1}{16}$. Das Quotientenkriterium liefert daher keine Aussage. Der Versuch mit dem Wurzelkriterium erweist sich jedoch als zielführend, denn
$$
\sqrt[2n]{ \frac{1}{4^{n}} } = \frac{1}{2}, ~~~\sqrt[2n+1]{ \frac{1}{4^{n-1}} } = \sqrt[2n+1]{ \frac{2^{3}}{2^{2n+1}} } = \sqrt[2n+1]{ 8 } \cdot \frac{1}{2} \rightarrow \frac{1}{2} \text{ für }n\rightarrow \infty
$$
und daraus folgt die Konvergenz von $\sum_{n}a_{n}$. Allgemein lässt sich zeigen, dass das Wurzelkriterium leistungsfähiger ist als das Quotientenkriterium. Letzteres ist jedoch in vielen Fällen einfacher zu handhaben.
