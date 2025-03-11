## 5) 
Man finde alle Häufungspunkte der Folge $a_{n} = sin \frac{nπ}{2} + (−1)^{n(n+1)/2} ~~~~~(n ≥ 0)$.

$$
a_{0}=\sin0 + 1=1
$$
$$
a_{1}=\sin \frac{\pi}{2}+ -1 = 1 -1 = 0
$$
$$
a_{2}=\sin \pi + -1 = 0-1 = -1
$$
$$
a_{3}=\sin \frac{3\pi}{4} + 1 = -1 + 1 = 0
$$
$$
a_{4}=1\dots
$$
Behauptung: $\{ -1,0,1 \}$

$$
a_{4n+0}=\sin \frac{4n\pi}{2} + -1^{4n(4n+1)/2}=\sin (2\pi \cdot n) + -1^{2n(4n+1)} =0+ -1 ^{2(4n^{2}+n)} = 0 + 1 = 1
$$
$$
a_{4n+1} = \sin \frac{(4n+1)\pi}{2} + -1^{(4n+1)(4n+2)/2} = \sin \left( 2\pi n+\frac{\pi}{2} \right) + -1^{(16n^{2}+12n+2)/2} = 1 + -1^{8n^{2}+6n+1}
$$
$$
= 1+ -1^{(2n+1)(4n+1)} = 1 + -1 = 0
$$
$$
a_{4n+2} = \sin \frac{(4n+2)\pi}{2} + -1 ^{(4n+2)(4n+3)/2}= \sin(2\pi n+\pi) + -1^{(16n^{2}+20n+6)/2} = 0 + -1^{8n^{2}+10n+3} = 
$$
$$
= 0 + -1^{(2n+1)(4n+3)} = 0 -1 = -1
$$
$$
a_{4n+3} = \sin \frac{(4n+3)\pi}{2} + -1^{(4n+3)(4n+4)/2} =\sin \left( 2\pi n + \frac{3\pi}{2} \right) = -1 + -1^{(16n^{2}+28n+12)/2}= 
$$
$$
= -1 + -1^{8n^{2}+14n+6} = -1 + -1^{2\cdot(4n^{2}+7n+3)} = -1 + 1 = 0
$$

## 9) 
Man zeige, dass die Folge $(a_{n})_{n\in \mathbb{N}}$ konvergiert, indem man zu beliebigem $ε > 0$ ein
$N (ε)$ und ein geeignetes $a$ angebe, sodass $∀n > N (ε) : |a_{n} − a| < ε$.
$$
a_{n}= \frac{\sin n+\cos n}{\sqrt{ n }}, ~~~ n\geq 1
$$
$$
\frac{-2}{\sqrt{ n }}\leq \frac{\sin(n)+\cos(n)}{\sqrt{ n }}\leq \frac{2}{\sqrt{ n }}
$$
$$
\lim_{ n \to \infty } -\frac{2}{\sqrt{ n }}=0, \lim_{ n \to \infty } \frac{2}{\sqrt{ n }}=0 \implies \lim_{ n \to \infty } \frac{\sin n+\cos n}{\sqrt{ n }}=0
$$
$$
|a_{n}-0|<\varepsilon \iff | \frac{\sin n+\cos n}{\sqrt{ n }}| < \varepsilon
$$
$$
\frac{2}{\sqrt{ n }}<\varepsilon \iff \frac{4}{\varepsilon^{2}}<n
$$
$$
N(\varepsilon)=\left\lceil  \frac{4}{\varepsilon^{2}}  \right\rceil 
$$
$$
|a_{n}|<\varepsilon
$$

## 14)
Sei $(c_{n})_{n\in \mathbb{N}}$ eine beliebige reelle Folge. Man zeige, dass es zwei Nullfolgen $(a_{n})_{n\in \mathbb{N}},(b_{n})_{n\in \mathbb{N}}$ gibt, die $c_{n} = \frac{a_{n}}{b_{n}}$ für alle $n ∈ \mathbb{N}$ erfüllen.

$$
a_{n}=c_{n}\cdot b_{n}=c_{n} \cdot \frac{1}{n(|c_{n}|+1)}=\frac{c_{n}}{n(|c_{n}|+1)}
$$
$$
b_{n}=\frac{a_{n}}{c_{n}}=\frac{\frac{c_{n}}{n(|c_{n}+1|)}}{c_{n}}=\frac{c_{n}}{c_{n}n(|c_{n}|+1)}=\frac{1}{n(|c_{n}|+1)}
$$
$a_{n}$ und $b_{n}$ beides Nullfolgen

$$
c_{n}=\frac{a_{n}}{b_{n}}=\frac{\frac{c_{n}}{n\cdot(|c_{n}|+1)}}{\frac{1}{n\cdot(|c_{n}|+1)}} = \frac{c_{n}n(|c_{n}|+1)}{n(|c_{n}|+1)} = c_{n}
$$
Also lässt sich jedes beliebige $c_{n}$ als Division zweier Nullfolgen darstellen.
## 16) 
Seien $(a_{n})_{n\in \mathbb{N}}$ und $(b_{n})_{n\in \mathbb{N}}$ zwei konvergente Folgen mit $\lim_{ n \to \infty }a_{n}=a$ und $\lim_{ n \to \infty }b_{n}=b$. Man zeige, dass die Folge $(c_{n})_{n\in \mathbb{N}} = (3a_{n} − b_{n})_{n\in \mathbb{N}}$ auch konvergiert mit $\lim_{ n \to \infty }c_{n}=c=3a-b$, indem man zu beliebigem $ε > 0$ ein $N (ε)$ angebe.

Nehme an
$$
|c_{n}-c|=|3a_{n}-b_{n}-(3a-b)|<\varepsilon
$$
$$
|3a_{n}-b_{n}-(3a-b)|=|(3a_{n}-3a)-(b_{n}-b)|< |3a_{n}-3a| + |b_{n}-b| < \varepsilon
$$
Gibt $N_{1},N_{2}$ für $n>N_{1};n>N_{2}$

$$
3|a_{n}-a|+|b_{n}-b|<\varepsilon
$$
$$
|a_{n}-a| < \frac{\varepsilon}{6} \implies |3a_{n}-3a|< \frac{3\varepsilon}{6}=\frac{\varepsilon}{2}
$$

$$
|b_{n}-b|< \frac{\varepsilon}{2}
$$
$$
|(3a_{n}-3a)-(b_{n}-b)|\leq |3a_{n}-3a|+ |b_{n}-b|< \varepsilon
$$
für $n>max(N_{1},N_{2})$