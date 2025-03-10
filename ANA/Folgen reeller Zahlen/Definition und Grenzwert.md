## Begriff der Folge
Unter einer #reellen_Folge versteht man eine Anordnung von reellen Zahlen $a_{0},a_{1},a_{2},\dots$ Eine andere Schreibweise ist $(a_{n})_{n\geq 0}$. Folgen können auch als Funktionen $a:\mathbb{N}\rightarrow \mathbb{R}$ aufgefasst werden. In diesem Fall gilt $a(n)=a_{n}$. Die Zahlen $a_{n}$, aus denen die #Folge aufgebaut ist, nennt man die #Glieder der Folge, und $n$ heißt Index des #Folgenglieds $a_{n}$.

So kann eine Folge eine die Zahl $\pi$ approximieren. $a_{0}=3$, $a_{1}=3.1$,$a_{2}=3.14\dots$ Je größer das $n$ desto kleiner wird der Abstand $|a_{n}-\pi|$.

Der Index muss jedoch nicht zwangsweise mit 1 sondern kann auch mit einem beliebigen $k$ beginnen. Man betrachtet Folgen der Gestalt $(a_{n})_{n\geq 1}$ bzw. $(a_{n})_{n\geq k}$.

Natürlich kann man Folgen über beliebige Mengen betrachten doch bezieht sich die Theorie weiterhin auf Folgen über $\mathbb{R}$.

## Beispiele für Folgen

- a) $a_{n}=\frac{1}{n^{2}}\geq 1:1, \frac{1}{4}, \frac{1}{9}, \frac{1}{16}\dots$

- b) $a_{n}=2$ ergibt die Folge $2,2,2,2,2,\dots$

- c) Arithmetische Folgen der Form $a_{n}=a_{0}+dn$

- d) Geometrische Folgen der Form $a_{n}=a_{0}\cdot q^{n}$

- e) Rekursive Folgen beispielhaften Form $a_{0}=1,a_{1}=1,a_{n}=a_{n-1}+a_{n-2}$

Eine Aussage gilt für **fast alle** $n \in \mathbb{N}$, wenn sie für alle bis auf endlich viele Ausnahmen gilt. Weiters bezeichnen wir folgendes Intervall als $\varepsilon$-Umgebung von $a$.

$$
U_{\varepsilon}(a)=(a-\varepsilon,a+\varepsilon)=\{ x\in \mathbb{R}| | x-a|<\varepsilon \}
$$
Eine reelle Zahl $a$ heißt #Grenzwert (oder #Limes) der Folge $(a_{n})_{n\geq 0}$, falls in jeder $\varepsilon$-Umgebung von $a$ fast alle Folgenglieder $a_{n}$ liegen, d.h. falls
$$
\forall \varepsilon > 0 \exists N(\varepsilon)\in \mathbb{N}\forall n>N(\varepsilon):|a_{n}-a|<\varepsilon
$$
gilt. 
Eine Folge $(a_{n})_{n\geq 0}$ heißt #konvergent, falls sie einen Grenzwert $a$ besitzt. In diesem Falle konvergiert die Folge gegen $a$, und man schreibt
$$
\lim_{ n \to \infty } a_{n}=a \text{ oder } a_{n}\rightarrow a
$$
Besitzt die Folge $(a_{n})_{n\geq 0}$ keinen Grenzwert, so heißt sie #divergent. Eine Folge, die 0 als Grenzwert besitzt, nennt man auch #Nullfolge. 
Eine Folge $(a_{n})_{n\geq 0}$, deren Glieder beliebig groß werden, d.h. für die gilt
$$
\forall K>0\exists N(K)\in \mathbb{N}~\forall n>N(K):a_{n}>K
$$
heißt #uneigentlich_konvergent, und man schreibt $\lim_{ n \to \infty } = \infty$. Analog definiert man $\lim_{ n \to \infty }=-\infty$ und nennt solche Folgen ebenfalls uneigentlich konvergent. Der Wert $+\infty$ bzw. $-\infty$ wird dann als #uneigentlicher_Grenzwert bezeichnet.

Wenn in jeder $\varepsilon$-Umgebung von $a$ unendlich viele Folgenglieder liegen, so ist $a$ ein #Häufungspunkt (oder #Häufungswert) von $(a_{n})_{n\geq 0}$. Analog zum uneigentlichen Grenzwert werden #uneigentliche_Häufungspunkte definiert. Der größte Häufungspunkt (uneigentlich mit eingeschlossen) heißt #Limes_superior (man schreibt: $\lim\sup_{ n \to \infty } a_{n}$), der kleinste Häufungspunkt #Limes_inferior ($\lim\inf_{ n \to \infty }a_{n}$)

Eine Zahl $a$ ist somit Grenzwert einer Folge, wenn folgendes gilt: Gibt man einen Abstand $\varepsilon>0$ vor, so lässt sich ein Index $N$ derart finden, dass ab diesem $N$ alle Folgenglieder einen Abstand von $a$ haben, der kleiner als $\varepsilon$ ist. So ein $N$ muss es für jedes $\varepsilon$ geben, egal wie klein $\varepsilon$ gewählt war. Findet man eine $\varepsilon$-Umgebung von $a$, die unendlich viele Folgenglieder nicht enthält, so kann $a$ nicht Grenzwert der Folge sein.

Für einen Häufungspunkt $a$ ist hingegen nur verlangt, dass bei beliebig aber fest vorgegebenem Abstand $\varepsilon$ unendlich viele Folgenglieder diesen Abstand von $a$ unterschreiten. Die Anzahl der Folgenglieder mit größerem Abstand kann endlich, aber auch unendlich sein. Der Limes superior und der Limes inferior existieren im Gegensatz zum Grenzwert für jede Folge. 

Wie man leicht sieht, ist jeder Grenzwert einer Folge $(a_{n})_{n\geq0}$ auch ein Häufungspunkt dieser Folge. Die Umkehrung ist aber nicht richtig. Falls $a$ und $b$ zwei verschiedene Häufungspunkte von $(a_{n})_{n\geq 0}$ sind, so gilt für $\varepsilon< \frac{1}{2}|a-b|$, dass $U_{\varepsilon}(a)\cap U_{\varepsilon}(b)=\emptyset$. Daher können nicht fast alle $a_{n}$ sowohl in $U_{\varepsilon}(a)$ als auch in $U_{\varepsilon}(b)$ liegen. Aus dieser Überlegung folgt auch die Eindeutigkeit des Grenzwerts: Da in jeder Umgebung des Grenzwerts fast alle Folgenglieder liegen. kann eine konvergente Folge nur einen Häufungspunkt besitzen. Im Falle der Konvergenz gilt also $\lim_{ n \to \infty }a_{n}=\lim\sup_{ n \to \infty }a_{n}=\lim\inf_{ n \to \infty }a_{n}$

## Beispiele zu Grenzwerten
- a) Gegeben sei die Folge $\left( \frac{1}{n^{2}} \right)_{n\geq1}=\left( 1, \frac{1}{4}, \frac{1}{9}, \frac{1}{16}, \dots \right)$ und ein $\varepsilon>0$. Dann gilt $0<a_{n}<\varepsilon$ falls $n>N(\varepsilon)=\left\lfloor  \frac{1}{\sqrt{ \varepsilon }}  \right\rfloor$. Somit ist 0 Grenzwert dieser Folge
- b) Sei $a_{n}=(-1)^{n}$, also $(a_{n})=(1,-1,1,-1,1,-1,1,\dots)$. Diese Folge ist divergent. Es liegen jeweils unendlich viele Folgenglieder in jeder $\varepsilon$-Umgebung $U_{\varepsilon}(1)$ und $U_{\varepsilon}(-1)$. Also sind $-1$ und $1$ Häufungspunkte der Folge. Daher besitzt diese Folge keinen Grenzwert.
- c) Die Folge $a_{n}=(n^{2})_{n\in \mathbb{N}}=(0,1,4,9,16,\dots)$ ist uneigentlich konvergent gegen $+\infty$, da für jede beliebige vorgegebene Zahl $K>0$ eine Quadratzahl existiert, die größer als $K$ ist.