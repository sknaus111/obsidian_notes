Eine Folge $(a_{n})_{n\geq 0}$ heißt #monoton_fallend, wenn $a_{n+1}\leq a_{n}$ für alle $n\in \mathbb{N}$. Gilt $a_{n+1}<a_{n}$ spricht man von #strikt_monoton_fallend. Das gleiche Prinzip gilt auch für #monoton_wachsend $a_{n+1}\geq a_{n}$ und #strikt_monoton_wachsend $a_{n+1}>a_{n}$. 

Eine Folge $(a_{n})_{n\geq 0}$ heißt #nach_oben_beschränkt, wenn es eine reelle Zahl $S$ gibt, so dass $a_{n}<S$ für alle $n\in \mathbb{N}$. Jede solche Zahl $S$ heißt #obere_Schranke von $(a_{n})_{n\geq0}$. Die kleinste obere Schranke ist das #Supremum . Das Supremum $\sup a_{n}$ ist somit jene reelle Zahl $S_{0}$, welche die folgenden Bedingungen erfüllt. 

- (i) Es gilt $a_{n}\leq S_{0} \forall n\in \mathbb{N}$
- (ii) $\forall S\geq a_{n}\forall n\in \mathbb{N}:S_{0}\leq S$

Analog definiert man Beschränktheit nach unten und untere Schranken. Die größte untere Schranke wird das #Infimum genannt und $\inf a_{n}$ geschrieben. Falls die Folge nicht nach ober bzw. unten beschränkt ist, setzt man $\sup a_{n}=\infty$ bzw. $\inf a_{n}=-\infty$.

Sei $M\subseteq \mathbb{R}$. Da reelle Zahlen Dezimalentwicklungen besitzen, haben alle $x\in \mathbb{R}$ die Form $x_{0},x_{1}x_{2}\dots$ mit $x_{0}\in \mathbb{Z}$ und $x_{i} \in \{ 0,\dots ,9 \}$ für $i\geq 1$. Falls $M$ nach oben beschränkt und nicht leer ist, so lässt sich das Supremum auf folgende Weise finden. Zunächst bestimmt man die kleinste ganze Zahl, die eine obere Schranke von $M$ ist. Danach sucht man die kleinste Zahl der Form $x_{0},x_{1}$ also mit einer Nachkommastelle, wobei $x_{0}$ verschieden von der ganzen Zahl ist. Dieses Verfahren gibt eine monoton fallende Folge von oberen Schranken von $M$. Diese Folge konvergiert. Der Grenzwert dieser Folge ist das Supremum von $M$.

## Vollständigkeitssatz für die reellen Zahlen
Jede nach oben/unten beschränkte nicht leere Teilmenge von $\mathbb{R}$ besitzt ein Supremum/Infimum. Jede nach oben/unten beschränkte reelle Folge besitzt ein Supremum/Infimum. 

### Beispiel
Betrachte man die Folge $\left( \frac{1}{n^{2}} \right)_{n\geq 1}$. Da die Folge streng monoton fällt, ist das erste Folgenglied $a_{1}=1$ eine obere Schranke. Da $a_{n}\leq 1$ für alle $n\geq1$ gilt, ist 1 auch das Supremum der Folge.

Sei $S>0$. Dann gibt es ein $n\in \mathbb{N}$ derart, dass $a_{n}<S$, da $0$ der Grenzwert dieser Folge ist. Daher kann $S$ keine untere Schranke sein. Da alle Folgenglieder positiv sind, ist $0$ eine untere Schranke und das Infimum dieser Folge. Zu bemerken sei, dass $0$ kein Glied der Folge ist und das Supremum/Infimum kein Glied der Folge sein müssen. 

Sind das Supremum und Infimum in einer Menge enthalten nennt man sie auch #Maximum und #Minimum.

## Sätze zu Konvergenzuntersuchungen
Jede konvergente Folge ist beschränkt. 

### Beweis
Sei $(a_{n})_{n\geq 0}$ eine Folge mit $\lim_{ n \to \infty }a_{n}=a$ und $\varepsilon>0$. Dann liegen fast alle $a_{n}$ in $U_{\varepsilon}(a)$. Die Folgenglieder mit $a_{n}\not\in U_{\varepsilon}(a)$ seien $a_{n_{1}},a_{n_{2}},\dots,a_{n_{k}}$. Sei $\overline{\varepsilon}>max_{i=1,\dots,k}|a-a_{n_{i}}|$. Dann gilt insbesondere $\overline{\varepsilon}\geq \varepsilon$, und daher liegen alle Folgenglieder in $U_{\varepsilon}(a)$. Die Intervallgrenzen $a-\overline{\varepsilon}$ bzw. $a+\overline{\varepsilon}$ sind dann untere bzw. obere Schranken von $(a_{n})_{n\geq 0}$
### Hauptsatz über monotone Folgen
Eine monotone Folge ist genau dann konvergent, wenn sie beschränkt ist. 
#### Beweis
O.B.d.A sei $(a_{n})_{n\geq 0}$ eine monoton wachsende Folge. Aus der Konvergenz folgt nach dem vorigen Satz die Beschränktheit. Wir müssen daher nur noch zeigen, dass Beschränktheit hinreichend für die Konvergenz ist. Da $(a_{n})_{n\geq 0}$ ein Supremum besitzt sei $a=\sup a_{n}$ und $\varepsilon>0$. Da $a-\varepsilon$ keine obere Schranke von $(a_{n})_{n\geq 0}$ ist, existiert ein $N(\varepsilon)$ mit $a_{N(\varepsilon)}>a-\varepsilon$. Aufgrund der Monotonie muss $a_{n}>a-\varepsilon$ auch für alle $n>N(\varepsilon)$ gelten. Daher liegen fast alle $a_{n}$ in $U_{\varepsilon}(a)$. Da $\varepsilon$ beliebig gewählt werden kann, gilt $\lim_{ n \to \infty }a_{n}=a$
#### Beispiel
Man nehme die arithmetische Folge $a_{n}=a_{0}+dn$. Es ist zu sehen, dass $(a_{n})_{n\geq 0}$ nur für $d=0$ konvergent ist. In diesem Fall ist $(a_{n})_{n\geq0}$ eine konstante Folge und $\lim_{ n \to \infty }a_{n}=a_{0}$. Im Fall $d\not=0$ ist $(a_{n})_{n\geq 0}$ uneigentlich konvergent gegen $\pm \infty$, wobei das Vorzeichen mit jenem von $d$ übereinstimmt. 
