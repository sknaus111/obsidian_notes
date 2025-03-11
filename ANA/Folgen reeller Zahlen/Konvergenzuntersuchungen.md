## Sandwich Theorem
Seien $(a_{n})_{n\geq 0}$ und $(b_{n})_{n\geq 0}$ konvergente Folgen, deren Grenzwerte übereinstimmen, also $\lim_{ n \to \infty }a_{n}=\lim_{ n \to \infty }b_{n}=a$. Sei $(c_{n})_{n\geq 0}$ eine Folge mit $a_{n}\leq c_{n}\leq b_{n}$ für fast alle $n\in \mathbb{N}$. Dann folgt die Konvergenz von $(c_{n})_{n\geq 0}$, und es gilt $\lim_{ n \to \infty }c_{n}=a$.

### Beweis
Für $\varepsilon>0$ gilt $a_{n}\in U_{\varepsilon}(a)$, falls $n>N_{1}$, und $b_{n}\in U_{\varepsilon}(a)$, falls $n>N_{2}$. Daraus folgt $c_{n}\in U_{\varepsilon}(a)$, falls $n>max(N_{1},N_{2})$.

### Beispiel
Sei $\alpha>0$. Gilt für eine Folge $\frac{1}{n^{\alpha}}\leq a_{n}\leq n^{\alpha}$, dann folgt $\lim \sqrt[n]{ a_{n} }=1$. Zum Beweis benützen wir $\sqrt[n]{ n }\rightarrow 1$. Daraus folgt $\lim_{ n \to \infty } \frac{1}{\sqrt[n]{ n^{\alpha} }}=\lim_{ n \to \infty }\sqrt[n]{ n^{\alpha} }=1$.

## Teilfolgen
Seien $(a_{n})_{n\geq 0}$ eine Folge reeller Zahlen und $n_{0}<n_{1}<n_{2}<\dots$ natürliche Zahlen. Dann nennt man die Folge $(a_{n_{m}})_{m\in \mathbb{N}}=(a_{n_{0}},a_{n_{1}},a_{n_{2}},\dots)$ eine #Teilfolge von $(a_{n})_{n\geq 0}$.

### Beispiel
- (a) Die Folge der Quadratzahlen $(n^{2})_{n\geq 1}=(1,4,9,16,\dots)$ ist eine Teilfolge der Folge $(n)_{n\geq 1}=(1,2,3,4,5,6,7,8,9,10,\dots)$.
- (b) Sei $(a_{n})_{n\geq 0}=(1,-1,1,-1,1,-1,\dots)$. Diese Folge ist divergent. Nimmt man nur die geraden Indizes, so erhält man als Teilfolge die konstante Folge $(1,1,1,1,\dots)$, also eine konvergente Folge.


### Häufungspunkte und Teilfolgen
Sei $(a_{n})_{n\geq 0}$ eine Folge, die den Häufungspunkt $a$ besitzt. Dann gibt es eine gegen $a$ konvergierende Teilfolge. Falls umgekehrt $(a_{n})_{n\geq 0}$ eine konvergente Teilfolge mit Grenzwert $a$ enthält, so ist $a$ ein Häufungspunkt von $(a_{n})_{n\geq 0}$.

#### Beweis
Zu einem Häufungspunkt $a$ der Folge $(a_{n})_{n\geq 0}$ lässt sich auf folgende Weise eine konvergente Teilfolge konstruieren. Wir geben uns eine monoton fallende Nullfolge $(\varepsilon_{n})_{n\in \mathbb{N}}$ mit $\varepsilon_{n}>0$ (z.B. $\varepsilon_{0}=1,\varepsilon_{n}= \frac{1}{n}$ für $n\geq 1$) vor. Dann gibt es in $U_{\varepsilon_{0}}(a)$ unendlich viele Folgenglieder von $(a_{n})_{n\geq 0}$. Wir wählen eines aus, beispielsweise $a_{n_{0}}$. Danach wählen wir ein $a_{n_{1}}\in U_{\varepsilon_{1}}(a)$ mit $n_{1}>n_{0}$, usw. Dann ist $(a_{n_{k}})_{k\in \mathbb{N}}$ eine gegen $a$ konvergente Teilfolge von $(a_{n})_{n\geq 0}$. Denn bei Vorgabe eines $\varepsilon>0$ gibt es ein $k_{0}$, so dass $\varepsilon\geq \varepsilon_{k_{0}}\geq \varepsilon_{k_{0}+1}\geq\dots\geq 0$. Für alle $k\geq k_{0}$ gilt daher $|a_{n_{k}}-a|<\varepsilon$. 
Sei umgekehrt eine konvergente Teilfolge gegeben. Dann ist ihr Grenzwert $a$ ein Häufungspunkt von $(a_{n})_{n\geq 0}$, denn in jeder $\varepsilon$-Umgebung von $a$ liegen fast alle Glieder der Teilfolge, also insbesondere unendlich viele Folgenglieder von $(a_{n})_{n\geq 0}$

## Satz von Bolzano-Weierstraß
Jede beschränkte Folge $(a_{n})_{n\geq 0}$ enthält einen Häufungspunkt

### Beweis
Diese Aussage ist äquivalent zur Existenz einer konvergenten Teilfolge. Aufgrund der Beschränktheit von $(a_{n})_{n\geq 0}$ und des Hauptsatzes über monotone Folgen genügt es, die Existenz einer monotonen Teilfolge nachzuweisen.
Wir definieren zunächst eine Menge $M$ gemäß $M=\{ k\in \mathbb{N}|\forall m>k:a_{m}<a_{k} \}$, d.h.  $k\in M$ ist gleichbedeutend damit, dass $a_{k}$ größer ist als sämtliche Folgenglieder mit größerem Index. Wir konstruieren nun eine monotone Folge, wobei wir unterscheiden müssen, ob $M$ unendlich ist oder nicht. Falls $M$ unendlich viele Elemente enthält, so ist $(a_{k})_{k\in M}$ bereits eine monoton fallende Teilfolge von $(a_{n})_{n\geq 0}$. Denn wenn $k_{1},k_{2}\in M$ mit $k_{1}<k_{2}$, dann ist $a_{k_{1}}$ laut Definition von $M$ größer als alle nachfolgenden Folgenglieder, also insbesondere größer als $a_{k_{2}}$.
Falls $M$ endlich ist, so bekommen wir mit der oben beschriebenen Vorgangsweise nur endlich viele Elemente und somit keine Teilfolge. In diesem Fall kann man aber eine monoton wachsende Teilfolge konstruieren. Da $M$ beschränkt ist, existiert ein $n_{1}\in \mathbb{N}$, mit $n_{1}>k$ für alle $k\in M$. Dann ist $a_{n_{1}}$ nicht größer als alle nachfolgenden Folgenglieder, weil sonst $n_{1}$ ja in $M$ enthalten wäre. Es gibt also ein mindestens ebenso großes Folgenglied $a_{n_{2}}$ mit $n_{2}>n_{1}$. Da auch $n_{2}\not\in M$, muss $a_{n_{3}}$ mit $n_{3}>n_{2}$ und $a_{n_{3}}\geq a_{n_{2}}$ existieren. Diesen Prozess setzen wir ad infinitum fort und erhalten auf diese Art eine monoton wachsende Teilfolge von $(a_{n})_{n\geq 0}$.

## Cauchyfolge
Eine reelle Folge heißt #Cauchyfolge, wenn für alle $\varepsilon>0$ ein $N(\varepsilon)$ existiert, so dass $|a_{n}-a_{m}|<\varepsilon$ für alle $n,m>N(\varepsilon)$.

### Cauchykriterium
Eine reelle Folge $(a_{n})_{n\geq 0}$ ist genau dann konvergent, wenn sie eine Cauchyfolge ist. 

### Beweis
Sei $(a_{n})_{n\geq 0}$ konvergent und $\varepsilon>0$. Den Grenzwert von $(a_{n})_{n\geq 0}$ nennen wir $a$. Dann existiert $N(\varepsilon)$ derart, dass $|a_{n}-a|<\varepsilon$, falls $n> N(\varepsilon)$. Seien nun $n,m>N(\varepsilon)$. Dann gilt $|a_{n}-a_{m}|=|a_{n}-a-(a_{m}-a)|\leq |a_{n}-a|+|a_{m}-a|< \varepsilon + \varepsilon = 2\varepsilon$. Die Folge $(a_{n})_{n\geq 0}$ ist daher eine Cauchyfolge.
Umkehrung:
Gelte für ein $\varepsilon>0$, dass $|a_{n}-a_{m}|<\varepsilon$ für $n,m>N(\varepsilon)$. Dann ist $(a_{n})_{n\geq 0}$ beschränkt, denn für $m>N=N(\varepsilon)$ folgt aus $|a_{m}|-|a_{N+1}|\leq |a_{m}-a_{N+1}|<\varepsilon$, dass $|a_{m}|<|a_{N+1}|+\varepsilon$. Somit ist die Folge $(|a_{N+1}|,|a_{N+2}|,\dots)$ durch $a_{N+1}+\varepsilon$ nach oben beschränkt. Folglich ist $S=\max(|a_{0}|,|a_{1}|,\dots,a_{N},a_{N+1}+\varepsilon)$ eine obere Schranke von $(a_{n})_{n\in \mathbb{N}}$. Die Folge $(a_{n})_{n\geq 0}$ ist daher durch $S$ nach oben und durch $-S$ nach untern beschränkt. Nach dem Satz von Bolzano-Weierstraß existiert dann ein Häufungspunkt $a$ und infolge dessen eine Teilfolge $(a_{n_{k}})_{n\in \mathbb{N}}$ mit $a_{n_{k}}\rightarrow a$. Das bedeutet aber, dass für hinreichend große $k$, z.B. $k>K=K(\varepsilon),|a_{n_{k}}-a|<\varepsilon$ folgt. Sei nun $n>N$ und $k>\max(K,N)$, so dass also auch $n_{k}>N$ gilt. Dann folgt $|a_{n}-a|\leq |a_{n}-a_{n_{k}}|+|a_{n_{k}}-a|<2\varepsilon$ und daher $a_{n}\rightarrow a$.
### Beispiel
Gegeben ist die rekursiv definiert Folge $a_{n+1}= \frac{2+a_{n}}{1+a_{n}}$ mit $a_{0}=1$. Die ersten Glieder der Folge sind $1, \frac{3}{2}, \frac{7}{5}, \frac{17}{12}, \frac{41}{29},\dots$ Die dadurch aufkommende Vermutung $1\leq a_{n}\leq 2$ lässt sich leicht mit vollständiger Induktion beweisen. Sei nun $n>m$. Dann gilt
$$
|a_{n}-a_{m}|= \left| \frac{2+a_{n-1}}{1+a_{n-1}} - \frac{2+a_{m-1}}{1+a_{m-1}}\right| 
$$
$$
=\left| \frac{(2+a_{n-1})(1+a_{m-1})-(2+a_{m-1})(1+a_{n-1})}{(1+a_{n-1})(1+a_{m-1})}\right|
$$
$$
=\left| \frac{a_{m-1}-a_{n-1}}{(1+a_{n-1})(1+a_{m-1})}\right|
$$
Wegen $a_{n}\geq 1$ ist der Nenner des obigen Ausdrucks größer oder gleich 4. Daraus folgt $|a_{n}-a_{m}|\leq \frac{1}{4}|a_{n-1}-a_{m-1}|$. Iteriert man diese Vorgangsweise, so erhält man $|a_{n}-a_{m}|\leq \frac{1}{4^{m}}|a_{0}-a_{n-m}|\leq \frac{1}{4^{m-1}}$, wobei die letzte Ungleichung aus der Abschätzung $a_{n}\leq 2$ und der Dreiecksgleichung folgt. Die Folge $(a_{n})_{n\geq 0}$ ist daher eine Cauchyfolge und somit konvergent. Sei $a=\lim_{ n \to \infty }a_{n}$. Führt man in der definierenden Rekursion den Grenzübergang für $n\rightarrow \infty$ durch, so ergibt sich $a= \frac{2+a}{1+a}$. Lösen dieser Gleichung unter Berücksichtigung von $1\leq a_{n}\leq 2$ ergibt $a=\sqrt{ 2 }$.