Unter einer unendlichen #Reihe versteht man eine (formale) unendliche Summe $\sum_{n=0}^{\infty}a_{n}$. Dabei ist $(a_{n})_{n\geq 0}$ die Folge der Reihenglieder. Die Folge $(s_{n})_{n\geq 0}$ mit $$
s_{n}=\sum_{k=0}^{n}a_{k}
$$
heißt Folge der #Partialsummen der Reihe. Unter dem #Grenzwert (oder der #Summe) der Reihe versteht man den Grenzwert ihrer Partialsummenfolge. Ist die Folge $(s_{n})_{n\geq 0}$ konvergent bzw. divergent, so heißt auch die Reihe #konvergent bzw. #divergent.

## Konvergenz unendlicher Reihen
Falls die Reihe $\sum_{n\geq 0} a_{n}$ konvergiert, so ist die Folge der Reihenglieder eine Nullfolge d.h., $a_{n} \rightarrow 0$ 

### Beweis
Laut Voraussetzung gilt $\sum_{n\geq 0}a_{n} =\lim_{ n \to \infty }s_{n}=s\in \mathbb{R}$. Die Reihenglieder lassen sich aber mit Hilfe der Partialsummenfolge durch $a_{n}=s_{n}-s_{n-1}$ beschreiben. Übergang zum Grenzwert ergibt $\lim_{ n \to \infty }s_{n}-\lim_{ n \to \infty }s_{n-1}=s-s=0$ 

## Harmonische Reihe
Die #harmonische_Reihe ist definier durch
$$
\sum_{n\geq 1} \frac{1}{n} = 1 + \frac{1}{2} + \frac{1}{3} + \frac{1}{4} + \frac{1}{5} + \frac{1}{6} + \frac{1}{7} + \frac{1}{8} + \dots
$$
Es gilt offensichtlich $$
\sum_{n\geq 1} \frac{1}{n} \geq 1 + \frac{1}{2} + \left( \frac{1}{4}+\frac{1}{4}\right) + \left( \frac{1}{8}+\frac{1}{8}+\frac{1}{8}+\frac{1}{8}\right)+ \dots
$$
$$
\sum_{n\geq 1} \frac{1}{n}\geq 1 + \frac{1}{2} + \frac{1}{2} + \frac{1}{2} + \dots
$$
Die Partialsummenfolge $(s_{n})_{n\geq 0}$ ist also monoton wachsend, und nach den obigen Überlegungen gilt $s_{2^{n}}\geq 1+ \frac{n}{2} \rightarrow \infty$. Die harmonische Reihe ist somit divergent. Dies zeigt, dass die Umkehrung des vorigen Satzes nicht richtig ist. Aus $a_{n}\rightarrow0$ folgt im Allgemeinen nicht die Konvergenz der Reihe $\sum_{n\geq 0}a_{n}$.

## Geometrische Reihe
Unter einer #geometrischen_Reihe versteht man eine Reihe der Form 
$$
\sum_{n\geq 0}q^{n}=1+q+q^{2}+q^{3}+ \dots 
$$
Die Partialsummenfolge $(s_{n})_{n\geq 0}$ der geometrischen Reihe ist daher $s_{n}=1+q+q^{2}+q^{3}+\dots+q^{n}$. Folglich gilt
$$
s_{n}= 1+q + q^{2}+\dots+q^{n}
$$
$$
qs_{n}=q+q^{2}+\dots+q^{n}+q^{n+1}
$$
$$
\overline{(1-q)s_{n}= 1 ~~~~~~~~~~~~~~~~~~~~-q^{n+1}}
$$
und für $q\not= 1$ erhalten wir
$$
s_{n}= \frac{1-q^{n+1}}{1-q}
$$
Im Fall $|q|\geq1$ ist die geometrische Reihe divergent, da die Folge der Summanden, also $(q^{n})_{n\in \mathbb{N}}$ keine Nullfolge ist.

Gegeben ist die Reihe $\sum_{n\geq 1} \frac{1}{n(n+1)}$. Die Partialsummenfolge ist somit
$$
s_{n}=\sum_{k=1}^{n} \frac{1}{k(k+1)}=\sum_{k=1}^{n} \left(\frac{1}{k}- \frac{1}{k+1}\right)
$$
$$
= \left(1- \frac{1}{2}\right) + \left( \frac{1}{2} - \frac{1}{3}\right) + \left( \frac{1}{3 } - \frac{1}{4}\right) + \dots + \left( \frac{1}{n} - \frac{1}{n+1}\right)
$$
$$
= 1- \frac{1}{n+1}
$$
Nach der Definition der Summe einer Reihe gilt
$$
\sum_{n=1}^{\infty} \frac{1}{n(n+1)} = \lim_{ n \to \infty } s_{n}=\lim_{ n \to \infty } \left( 1 - \frac{1}{n+1}\right) = 1
$$
Summen, bei denen Auslöschungen auftreten, nennt man #Teleskopsummen.