Bevor weiter auf die Reelle Zahlen eingegangen werden sich die natürlichen Zahlen in Erinnerung gerufen. Diese kann man mittels einer [[Dezimalentwicklung]] angeben.

Doch lässt sich mittels der Dezimalentwicklung nicht jede rationale Zahl durch eine #endliche_Dezimalentwicklung darstellen. So können nur rationale Zahlen der Form $r=\frac{n}{10^m}, \{n,m\} \in \mathbb{N}$ dargestellt werden. Zahlen wie $\frac{1}{3}$ sind in dieser Form nicht darstellbar da $3*n = 10^m$ nicht möglich ist. Schließlich ist 10 nicht durch 3 teilbar.

Trotz dessen kann für die #Reelle_Zahlen durch eine endliche Dezimalentwicklung eine beliebig genaue #Approximation gefunden werden.

Man kommt auf den Fall $x = \sqrt{ 2 }$ zurück. Offensichtlich befindet sich ich zwischen den Zahlen $1$ und $2$. Betrachtet man alle Zahlen zwischen $1$ und $2$ mit einer Nachkommastelle 
$$
1.0,1.1,1.2,1.3,1.4,1.5,1.6,1.7,1.8,1.9,2.0
$$
Offensichtlich gilt dass $x$ zwischen $1.4$ und $1.5$ liegt, da $1.4^2=1.96 < 2$ und $1.5^2 = 2.25 > 2$ ist. Daraufhin betrachtet man alle Zahlen zwischen $1.4$ und $1.5$ mit zwei Nachkommastellen.
$$
1.40,1.41,1.42,1.43,1.44,1.45,1.46,1.47,1.48,1.49,1.50
$$
Es ist feststellbar, dass $1.41 < \sqrt{ 2 } <1.42$ gilt. So kann man mit jedem Schritt den genauen Dezimalwert von $\sqrt{ 2 }$ weiter approximieren. Nach $m$ Schritten gewinnt man die rationalen Zahlen $x'_{m}$ und $x''_{m}$ mit $m$ Nachkommastellen, so dass $x'_{m} \leq x \leq x''_{m}$ und $x''_{m} - x'_{m} = 10^{-m}$

Greift man auf das Beispiel mit $\sqrt{ 2 }$ zurück so unterscheidet sich die Annäherung mit 50 Nachkommastellen um weniger als $10^{-50}$. Für praktische Beispiele ist dies zwar ausreichend, doch lässt sich $\sqrt{ 2 }$ in endlich vielen Schritten nicht exakt darstellen.

Es liegt nahe $\sqrt{ 2 }$ in einer unendlichen [[Dezimalentwicklung]] zu identifizieren.

Die Menge aller positiven und negativen, endlichen und unendlichen Dezimalentwicklungen - wobei Zahlen mit (schließlicher) Periode $999\dots$ mit ihrer endlichen Dezimalentwicklung identifiziert werden - wird als die Menge $\mathbb{R}$ der #Reelle_Zahlen bezeichnet.

So füllen die reellen Zahlen die Lücken, welche die rationalen Zahlen auf der #Zahlengerade gelassen haben. Aus der #Dezimalentwicklung stellt sich eine auch eine natürliche Ordnung der Zahlen her.

Mit reellen Zahlen kann auch addiert und multipliziert werden. Man nehme zwei reelle Zahlen $x$ und $y$ , sowie die #Approximation der beiden Zahlen $x'_{m},x''_{m}$ und $y'_{m},y''_{m}$ mit $m$ Dezimalstellen nach dem Komma.
Selbstreden gilt für diese, dass $x'_{m}\leq x \leq x''_{m}$, $y'_{m}\leq y''_{m}$ und $x''_{m}-x'_{m}=y''_{m}-y'_{m}=10^{-m}$
Daraus kann man nun mit den Approximationen der beiden reellen Zahlen addieren und multiplizieren. 
Für Addition das Intervall $[x'_{m}+y'_{m},x''_{m}+y''_{m}]$ bildet eine Intervallschachtelung, welches eine reelle Zahl definiert welche mit $x+y$ identifiziert werden kann.
Für Multiplikation das Intervall $[x'_{m}*y'_{m},x''_{m}*y''_{m}]$ bildet eine Intervallschachtelung, welches eine reelle Zahl definiert welche mit $x*y$ identifiziert werden kann.
Für Subtraktion und Division übertragen sich alle Regeln der [[Ganze und rationale Zahlen]].

Eine weitere Darstellung für reelle Zahlen, ist sie in einen ganzen Vorkommaanteil, dem #Ganzteil und dem reellen Nachkommaanteil, dem #Bruchteil. 
Weiters besitzt jede reelle Zahl einen #Betrag $|x|$. Dieser beschreibt den Abstand zur $0$ auf der Zahlengerade und kann durch $|x| = max\{x,-x\}$ berechnet werden.
