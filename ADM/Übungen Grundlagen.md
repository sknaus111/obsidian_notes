## 1)
Man überprüfe die Gleichung

#Induktionsvoraussetzung 

$$1^2 + 2^2 + 3^2 + \dots + n^2 = \frac{n(n + 1)(2n + 1)}{6}
$$
für die ersten fünf natürlichen Zahlen und beweise sodann deren Gültigkeit für alle natürlichen
Zahlen durch vollständige Induktion.
#Induktionsanfang

$$
1^2=\frac{1(1+1)(2*1+1)}{6}
$$
$$
1=\frac{1(2)(3)}{6}
$$
$$1=\frac{6}{6}$$
$$1=1$$
$$
1^2+2^2=\frac{2(2+1)(2*2+1)}{6}
$$
$$
5=\frac{2(3)(5)}{6}
$$
$$
5=\frac{30}{6}
$$
$$
5=5
$$
$$
1^2+2^2+3^2=\frac{3(3+1)(2*3+1)}{6}
$$
$$
14=\frac{3(4)(7)}{6}
$$
$$
14=\frac{84}{6}
$$
$$
14=14
$$
$$
1^2+2^2+3^2+4^2=\frac{4(4+1)(2*4+1)}{6}
$$
$$
30=\frac{4(5)(9)}{6}
$$
$$
30=\frac{180}{6}
$$
$$
30=30
$$
$$
1^2+2^2+3^2+4^2+5^2=\frac{5(5+1)(2*5+1)}{6}
$$
$$
55=\frac{5(6)(11)}{6}
$$
$$
55=55
$$
#Induktionsbehauptung 
$$1^2 + 2^2 + 3^2 + \dots + n^2 + (n+1)^2= \frac{(n+1)((n+1) + 1)(2(n+1) + 1)}{6}$$
#Induktionsschritt 
$$
1^2+2^2+3^2+\dots+n^2+(n+1)^2=1^2+2^2+3^2+\dots+n^2 ~~~~+ (n+1)^2
$$
$$
=\frac{n(n+1)(2n+1)}{6}+(n+1)^2
$$
$$
=\frac{n(n+1)(2n+1)}{6}+\frac{6*(n+1)^2}{6}
$$
$$
=\frac{(n^2+n)(2n+1)}{6} + \frac{6(n^2+2n+1)}{6}
$$
$$
=\frac{2n^3+n^2+2n^2+n}{6}+\frac{6n^2+12n+6}{6}
$$
$$
=\frac{2n^3+3n^2+n+6n^2+12n+6}{6}
$$
$$
=\frac{2n^3+9n^2+13n+6}{6}
$$
$$
=\frac{(n^2+3n+2)(2n+3)}{6}
$$
$$
=\frac{(n+1)(n+2)(2(n+1)+1)}{6}
$$
$$
=\frac{(n+1)((n+1)+1)(2(n+1)+1)}{6}
$$
## 2)
Man zeige, dass $n^3 − n$ für alle $n ∈ \mathbb{N}$ stets durch $3$ teilbar ist, mittels

(a) eines direkten Beweises,
$$\frac{n^{3}-n}{3} \in \mathbb{N}$$
$$
\frac{n*(n^2-1)}{3}
$$
$$
\frac{n*(n^2-1^2)}{3}
$$
$$
\frac{n*(n+1)(n-1)}{3}
$$
Da drei aufeinander folgende Zahlen multipliziert werden ist eine von den Zahlen logischerweise durch drei teilbar. Daraus folgt das $n^3-n$ durch drei teilbar ist.

(b) eines Beweises durch vollständige Induktion.
#Induktionsanfang 
$$
\frac{0^3-0}{3}
$$
$$
\frac{0}{3} \in \mathbb{Z}
$$
#Induktionsbehauptung 
$$
\frac{(n+1)*((n+1)+1)*((n+1)-1)}{3} \in \mathbb{N}
$$
$$
\frac{(n+1)*(n+2)*(n)}{3} 
$$
Aus der #Induktionsvoraussetzung, dass drei aufeinander folgende Zahlen multipliziert durch drei teilbar sind folgt die Wahrheit der #Induktionsbehauptung 

## [[Hausübung 1#3)]]
## [[Hausübung 1#4)]]
## 5)
$$
\sum^n_{j=1} \frac{1}{j*(j+1)}=\frac{n}{n+1}
$$
#Induktionsanfang 
$$
\sum^1_{j=1} \frac{1}{1*(1+1)}=\frac{1}{1+1}
$$
$$
\frac{1}{2}=\frac{1}{2}
$$
#Induktionsbehauptung 
$$
\sum ^{n+1}_{j=1} \frac{1}{j(j+1)}=\frac{n+1}{(n+1)+1}
$$
#Induktionsschritt 
$$
\sum ^{n+1}_{j=1} \frac{1}{j(j+1)}=\sum^n_{j=1} \frac{1}{j*(j+1)} + \frac{1}{(n+1)((n+1)+1)}
$$
$$
= \frac{n}{n+1}+\frac{1}{(n+1)*(n+2)}
$$
$$
=\frac{n*(n+2)+1}{(n+1)(n+2)}
$$
$$
\frac{n^2+2n+1}{(n+1)(n+2)}
$$
$$
\frac{(n+1)^2}{(n+1)(n+2)}
$$
$$
\frac{(n+1)(n+1)}{(n+1)(n+2)}
$$
$$
\frac{(n+1)}{(n+2)}
$$
$$
\frac{(n+1)}{(n+1)+1}
$$
## 6)
$$
\sum^n_{j=0}j 2^j = 2^{n+1}(n-1)+2
$$
#Induktionsanfang 
$$
\sum ^{0}_{j=0}0 2^0=2^{0+1}*(0-1)+2
$$
$$
0=2*-1+2
$$
$$
0=-2+2
$$
$$
0=0
$$
#Induktionsbehauptung 
$$
\sum ^{n+1}_{j=0}j 2^j = 2^{(n+1)+1}((n+1)-1)+2
$$
#Induktionsschritt 
$$
\sum ^{n+1}_{j=0}j 2^j = \sum^n_{j=0}j 2^j + (n+1)*2^{n+1}
$$
$$
= 2^{n+1}(n-1)+2 +  (n+1)*2^{n+1}
$$
$$
=2^{n+1}(n-1)+2^{n+1}(n+1)+2
$$
$$
=2+2^{n+1}*((n-1)+(n+1))
$$
$$
=2+2^{n+1}*(2n)
$$
$$
=2+2^{n+1+1}*n
$$
$$
=2^{(n+1)+1}*(n+1-1)+2
$$
$$
=2^{(n+1)+1}*((n+1)-1)+2
$$
## 7)
$$
\sum ^{n}_{j=1}j 3 ^{j-1} = \frac{3^n(2n-1)+1}{4}
$$
#Induktionsanfang 
$$
\sum ^{1}_{j=1}1*3^{j-1}=\frac{3^1*(2*1-1)+1}{4}
$$
$$
3^{1-1}=\frac{3*1+1}{4}
$$
$$
3^0=\frac{4}{4}
$$
$$
1=1
$$
#Induktionsbehauptung 
$$
\sum ^{n+1}_{j=1}j 3^{j-1}=\frac{3^{n+1}(2(n+1)-1)+1}{4}
$$
#Induktionsschritt 
$$
\sum ^{n+1}_{j=1}j 3^{j-1}=\sum ^{n}_{j=1}j 3 ^{j-1} + (n+1)*3^{(n+1)-1}
$$
$$
\sum ^{n+1}_{j=1}j 3^{j-1}= \frac{3^n(2n-1)+1}{4}+ (n+1)*3^{(n+1)-1}
$$
$$
=\frac{3^n2n-3^n+1}{4}+(3^nn+3^n)
$$
$$
=\frac{3^n2n-3^n+1}{4}\frac{+(3^nn+3^n)*4}{4}
$$
$$
\frac{2*3^n n-3^n+1+4*3^nn+4*3^n}{4}
$$
$$
\frac{6*3^nn+3*3^n+1}{4}
$$
$$
\frac{2*3*3^nn+3*3^n+1}{4}
$$
$$
\frac{(3^n)*(2*3*n+3)+1}{4}
$$
$$
\frac{3*3^n*(2n+1)+1}{4}
$$
$$
\frac{3^{n+1}(2n+1)+1}{4}
$$
$$
\frac{3^{n+1}(2n+2-1)+1}{4}
$$
$$
\frac{3^{n+1}(2(n+1)-1)+1}{4}
$$
## 8)
$$
\sum ^{n}_{k=1}k 5^k=\frac{5}{16}(n5^{n+1}-(n+1)5^n+1)
$$
#Induktionsanfang 
$$
\sum ^{1}_{k=1}1*5^1=\frac{5}{16}(1*5^{1+1}-(1+1)5^1+1)
$$
$$
5=\frac{5}{16}*(25-10+1)
$$
$$
5=\frac{5}{16}*(16)
$$
$$
5=5
$$
#Induktionsbehauptung 
$$
\sum ^{n+1}_{k=1}k 5^k=\frac{5}{16}((n+1)5^{(n+1)+1}-((n+1)+1)5^{n+1}+1)
$$
$$
=\frac{5}{16}((n+1)5^{n+2}-(n +2)5^{n+1}+1)
$$
$$
= \frac{5}{16}(n 5^{n+2}+5^{n+2}-n 5^{n+1}-2*5^{n+1}+1)
$$
$$
=\frac{5}{16}(5^n(n*25+25-5n-10)+1)
$$
$$
= \frac{5}{16}(5^n(20n+15)+1)
$$
#Induktionsschritt
$$
\sum ^{n+1}_{k=1}k 5^k=\sum ^{n}_{k=1}k 5^k + (n+1)5^{n+1}
$$
$$
\sum ^{n+1}_{k=1}k 5^k=\frac{5}{16}(n5^{n+1}-(n+1)5^n+1) + (n+1)5^{n+1}
$$
$$
=\frac{5}{16}(n 5^{n+1}-(n+1)5^n+1+\frac{1}{5}16*5^{n+1}(n+1))
$$
$$
= \frac{5}{16}(n 5^{n+1}-(n+1)5^n+1+ 16*5^n(n+1))
$$
$$
= \frac{5}{16}(5^n(n 5-(n+1)+16*(n+1))+1)
$$
$$
=\frac{5}{16}(5^n(n5+15(n+1))+1)
$$
$$
=\frac{5}{16}(5^n(5n+15n+15)+1)
$$
$$
=\frac{5}{16}(5^n(20n+15)+1)
$$
## 9)
$$
\sum ^{n}_{l=1} \frac{l}{3^l}=\frac{3}{4}- \frac{2n+3}{4*3^n}
$$
#Induktionsanfang 
$$
\sum_{l=1}^1 \frac{l}{3^l}=\frac{3}{4}-\frac{2+3}{4*3}
$$
$$
\frac{1}{3}=\frac{3}{4}-\frac{5}{12}
$$
$$
\frac{1}{3}=\frac{9}{12}-\frac{5}{12}
$$
$$
\frac{1}{3}=\frac{4}{12}
$$
$$
\frac{1}{3}=\frac{1}{3}
$$
#Induktionsbehauptung 
$$
\sum ^{n+1}_{l=1} \frac{l}{3^l}=\frac{3}{4}- \frac{2(n+1)+3}{4*3^{n+1}}
$$
#Induktionsschritt 
$$
\sum ^{n+1}_{l=1} \frac{l}{3^l}=\sum ^{n}_{l=1} \frac{l}{3^l} + \frac{n+1}{3^{n+1}}
$$
$$
= \frac{3}{4}- \frac{2n+3}{4*3^n} + \frac{n+1}{3^{n+1}}
$$
$$
= \frac{3}{4}- \frac{3*(2n+3)}{4*3^n*3}+\frac{4(n+1)}{4*3^{n+1}}
$$
$$
=\frac{3}{4}+\frac{-3(2n+3)+4(n+1)}{4*3^{n+1}}
$$
$$
=\frac{3}{4}+ \frac{-6n-9+4n+4}{4*3^{n+1}}
$$
$$
=\frac{3}{4}+ \frac{-2n-5}{4*3^{n+1}}
$$ $$
= \frac{3}{4} - \frac{2n+5}{4*3^{n+1}}
$$
$$
= \frac{3}{4} - \frac{2(n+1)+3}{4*3^{n+1}}
$$
## 10)
Ist $a_{0} = 0$ und $a_{n+1} = a_{n} + (n + 1)$ für alle $n ∈ \mathbb{N}$, so gilt $a_{n} = \frac{n(n+1)}{2}$.
#Induktionsanfang 
$$
a_{0}=\frac{0(0+1)}{2}
$$
#Induktionsbehauptung 
$$
a_{n+1}=\frac{(n+1)(n+2)}{2}
$$
#Induktionsschritt 
$$
a_{n+1}=a_{n}+(n+1)
$$
$$
=\frac{n(n+1)}{2}+(n+1)
$$
$$
=\frac{n(n+1)+2(n+1)}{2}
$$
$$
= \frac{(n+1) * (n+2)}{2}
$$
## 11)
Ist $F_{0} = 0, F_{1} = 1$ und $F_{n+2} = F_{n+1} + F_{n}$ für alle $n ∈ \mathbb{N}$, so gilt
$$
F_{n}=\frac{1}{\sqrt{ 5 }}  \bigg [ \bigg (     \frac{1+\sqrt{ 5 }}{2}     \bigg)^n-\bigg (    \frac{1-\sqrt{ 5 }}{2}   \bigg)^n\bigg ]
$$
#Induktionsanfang 
$$
F_{2}=\frac{1}{\sqrt{ 5 }}  \bigg [ \bigg (     \frac{1+\sqrt{ 5 }}{2}     \bigg)^2-\bigg (    \frac{1-\sqrt{ 5 }}{2}   \bigg)^2\bigg ]
$$
$$
F_{2}=\frac{1}{\sqrt{ 5 }}  \bigg [ \bigg (     \frac{1+2*\sqrt{ 5 }+5}{4}     \bigg)-\bigg (    \frac{1+2*-\sqrt{ 5 }+5}{4}   \bigg)\bigg ]
$$
$$
F_{2}=\frac{1}{\sqrt{ 5 }}* \frac{4*\sqrt{ 5 }}{4}
$$
$$
F_{2}=\frac{1}{\sqrt{ 5 }}*\sqrt{ 5 }
$$
$$
F_{2}=1
$$
$$
F_{0}+F_{1}=1
$$
#Induktionsbehauptung 
$$
F_{n+2}=\frac{1}{\sqrt{ 5 }}  \bigg [ \bigg (     \frac{1+\sqrt{ 5 }}{2}     \bigg)^{n+2}-\bigg (    \frac{1-\sqrt{ 5 }}{2}   \bigg)^{n+2}\bigg ]
$$
#Induktionsschritt 
$$
F_{n+2}=F_{n+1}+F_{n}
$$
$$
=\frac{1}{\sqrt{ 5 }}  \bigg [ \bigg (     \frac{1+\sqrt{ 5 }}{2}     \bigg)^{n+1}-\bigg (    \frac{1-\sqrt{ 5 }}{2}   \bigg)^{n+1}\bigg ] + \frac{1}{\sqrt{ 5 }}  \bigg [ \bigg (     \frac{1+\sqrt{ 5 }}{2}     \bigg)^n-\bigg (    \frac{1-\sqrt{ 5 }}{2}   \bigg)^n\bigg ]
$$
$$
= \frac{1}{\sqrt{ 5 }} 
$$
### VOWI
## [[Hausübung 1#15)]]
## [[Hausübung 1#24)]] 
## Buch. 1.1
### a ([[#Hausübung 1 4)]])
### b
$$
\sum_{j=1}^{n} j(j+1)=\frac{n}{6} ( 2n^{2}+6n+4) \text{ für } (n\geq 1)
$$
#Induktionsanfang 
$$
1(1+1)=\frac{1}{6}(2*1^{2}+6*1+4)
$$
$$
2=\frac{12}{6}
$$
$$
2=2
$$
#Induktionsbehauptung 
$$
\sum_{j=1}^{n+1} j(j+1) =\frac{ (n+1)}{6} ( 2 *(n+1)^{2}+6(n+1)+4)
$$
#Induktionsschritt 
$$
\sum_{j=1}^{n+1} j (j+1)=\sum_{j=1}^{n} j (j+1) + (n+1)((n+1)+1)
$$
$$
= \frac{n}{6} ( 2n^{2}+6n+4) + (n+1)(n+2)
$$
$$
= \frac{2n^{3}+6n^{2}+4+(n+1)(6n+12)}{6}
$$
$$
\frac{(n+1)(2n^{2}+4)+(n+1)(6n+12)}{6}
$$
$$
=\frac{n+1}{6}(2n^{2}+4+6n+12)
$$
$$
=\frac{n+1}{6}(2n^{2}+6*(n+2)+4)
$$

### c
$$
\sum_{j=1}^{n} \frac{1}{j(j+1)}=\frac{n}{n+1}
$$
#Induktionsanfang 
$$
\frac{1}{1(1+1)}=\frac{1}{1+1}
$$
#Induktionsbehauptung 
$$
\sum_{j=1}^{n+1} \frac{1}{j(j+1)} = \frac{n+1}{(n+1)+1}
$$
#Induktionsschritt 
$$
\sum_{j=1}^{n+1} \frac{1}{j(j+1)} = \sum_{j=1}^{n} \frac{1}{j(j+1)} + \frac{1}{(n+1)((n+1)+1)}
$$
$$
= \frac{n}{n+1}+\frac{1}{(n+1)(n+2)}
$$
$$
=\frac{n(n+2)+1}{(n+1)(n+2)}
$$
$$
=\frac{n^{2}+2n+1}{(n+1)(n+2)}
$$
$$
=\frac{(n+1)(n+1)}{(n+1)(n+2)}
$$
$$
=\frac{n+1}{(n+1)+1}
$$
### d
$$
\sum_{j=0}^{n}j2^{j}=2^{n+1}(n-1)+2 ~~~~~~(n\geq0)
$$
#Induktionsanfang 
$$
0 = 2(0-1)+2
$$
#Induktionsbehauptung 
$$
\sum_{j=0}^{n+1} j 2^{j} = 2^{(n+1)+1}((n+1)-1)+2
$$
#Induktionsschritt 
$$
\sum_{j=0}^{n+1} j 2^{j}= \sum_{j=0}^{n} j 2^{j} + (n+1)2^{n+1}
$$
$$
=2^{n+1}(n-1)+2 + (n+1)2^{n+1}
$$
$$
=2^{n+1}*n - 2^{n+1}*1 + 2^{n+1}*n +2^{n+1}*1 +2
$$
$$
=2^{n+1}*n+2^{n+1}*n + 2
$$
$$
= 2 (2^{n+1}n)+2
$$
$$
= 2^{n+2} n +2
$$
$$
= 2^{(n+1)+1}((n+1)-1)+2
$$
### e
$$
\sum_{j=1}^{n} j 3^{j-1}=\frac{3^{n}(2n-1)+1}{4}
$$
#Induktionsanfang 
$$
1=\frac{3(2-1)+1}{4}
$$
$$
1=\frac{4}{4}
$$
#Induktionsbehauptung 
$$
\sum_{j=1}^{n+1} j 3^{j-1} =\frac{ 3^{n+1}(2(n+1)-1)+1}{4}
$$
#Induktionsschritt 
$$
\sum_{j=1}^{n+1} j 3^{j-1} = \sum_{j=1}^{n} j3^{j-1} + (n+1)3^{(n+1)-1}
$$
$$
=\frac{3^{n}(2n-1)+1}{4}+ (n+1)3^{n}
$$
$$
=\frac{3^{n}(2n-1)+4(n+1)3^{n}}{4} + \frac{1}{4} 
$$
$$
=\frac{3^{n}2n-3^{n}+3^{n}4n+3^{n}4}{4} + \frac{1}{4}
$$
$$
=\frac{3^{n}6n+3^{n}3}{4} +\frac{1}{4}
$$
$$
= \frac{3^{n}(6n+3)}{4}\frac{1}{4}
$$
$$
= \frac{3^{n+1}(2n+1)}{4} + \frac{1}{4}
$$
$$
= \frac{3^{n+1}(2(n+1)-1)+1}{4}
$$
### f
$$
\sum_{j=1}^{n} \frac{j}{3^{j}} = \frac{3}{4} - \frac{2n+3}{4*3^{n}}
$$
#Induktionsanfang 
$$
\frac{1}{3}=\frac{3}{4}-\frac{2+3}{4*3}
$$
$$
\frac{1}{3}=\frac{9}{12} - \frac{5}{12}
$$
$$
\frac{1}{3} = \frac{4}{12}
$$
#Induktionsbehauptung 
$$
\sum_{j=1}^{n+1} \frac{j}{3^{j}} = \frac{3}{4} - \frac{2(n+1)+3}{4*3^{n+1}}
$$
#Induktionsschritt 
$$
\sum_{j=1}^{n+1} \frac{j}{3^{j}} = \sum_{j=1}^{n} \frac{j}{3^{j}} + \frac{n+1}{3^{n+1}}
$$
$$
= \frac{3}{4}-\frac{2n+3}{4*3^{n}} + \frac{n+1}{3^{n+1}}
$$
$$
= \frac{3}{4} - \frac{3*(2n+3)}{4*3^{n+1}}+ \frac{4(n+1)}{4*3^{n+1}}
$$
$$
=\frac{3}{4} - \frac{6n+9-4n-4}{4*3^{n+1}}
$$
$$
= \frac{3}{4} - \frac{2n+5}{4*3^{n+1}}
$$
$$
=\frac{3}{4} - \frac{2(n+1)+3}{4*3^{n+1}}
$$
## Buch 1.2
Man beweise mittels vollständiger Induktion: Ist $F_{0}=0, F_{1}=1$ und $F_{n+2}=F_{n+1}+F$ für alle $n\in\mathbb{N}$ so gilt
$$
F_{n}=\frac{1}{\sqrt{ 5 }} \left[\left( \frac{1+\sqrt{ 5 }}{2}\right)^{n} - \left( \frac{1-\sqrt{ 5 }}{2} \right)^{n}\right]
$$
## Buch 1.3
Man zeige, dass die Zahlen $\sqrt{ 3 }$, $\sqrt{ 5 }$ und $\sqrt[3]{ 2 }$
$m,n$ kleinste unkürzbare Darstellung
$$
\sqrt{ 3 } = \frac{m}{n} = x
$$
$$
x^{2} = \left( \frac{m}{n} \right)^{2} = 3
$$
$$
m^{2}=3*n^{2}
$$
$m$ durch drei teilbar
$$
(k*3)=m \implies (k*3)^2=3*n^2 \implies k^{2}*3=n^{2}
$$
$n$ durch drei teilbar, widerspruch zur definition
bei $\sqrt{ 5 }$ da exakt gleiche
$$\sqrt[3]{ 2 }= \frac{m}{n} = x$$
$$2=x^{3}=\left( \frac{m}{n} \right)^{3}$$
$$
m^{3}=n^{3}*2
$$
### Nochmal anschauen

## Buch 1.4
Nach der so genannten "abessinischen Bauernmethode" werden zwei Zahlen z.B. 21 und 17 wie folgt multipliziert.
$$
21 ~~~~~ 17
$$
kB alles weiter aufzuschreiben, ins buch schauen

Diese Methode funktioniert da dies der Binärentwicklung entspricht wenn man sich zumindest den ersten Faktor im Binärsystem anschaut.

$10101 ~~~~~ 10001$
$2^{0}(1*2^{4}+0*2^{3}+1*2^{2}+0*2^{1}+1*2^{0})+0(\dots)+0(\dots)+0(\dots)+2^{4}(1*2^{4}+0*2^{3}+1*2^{2}+0*2^{1}+1*2^{0})$
$$=357_{10}$$
## Buch 1.5

Man zeige, dass in $\mathbb{R}$ die Beziehung $\sqrt{ 5041 } -\sqrt{ 5040 }=71-12\sqrt{ 35 }=1/(71+12\sqrt{ 35 })$ gilt. Was ergibt sich bei der Rechnung in normalisierter Gleitkomma-Darstellung zur Basis 10 mit vierstelliger Mantisse. 

$$
\sqrt{ 5041 } -\sqrt{ 5040 } \implies 71 - \sqrt{ 144*35 } \implies17-12\sqrt{ 35 }
$$
$$
\implies (71-12*\sqrt{ 35 } )^2 = 5041 - 5040 = 1
$$
$$
\implies \frac{71-12\sqrt{ 35 }}{1} = \frac{1}{71+12\sqrt{ 35 }} 
$$

$7.0426 * 10^{-3}$

## Buch 1.6

Man zeige für komplexe Zahlen $z_{1}, z_{2}$ die Beziehung $arg(z_{1}z_{2})=(arg(z_{1})+arg(z_{2})) \mod 2\pi$
$$
\arctan\left( \frac{b_{2}}{a_{2}} \right) + \arctan\left( \frac{b_{1}}{a_{1}} \right) =  
$$
$$
z_{1}*z_{2}=(a_{1}a_{2}-b_{1}b_{2})+i(a_{1}b_{2}+a_{2}b_{1})
$$
$$
\arctan\left( \frac{a_{1}b_{2}+a_{2}b_{1}}{a_{1}a_{2}-b_{1}b_{2}} \right) = \arctan \left(  \frac{a_{1}b_{2}}{a_{1}a_{2}-b_{1}b_{2}} + \frac{a_{2}b_{1}}{a_{1}a_{2}-b_{1}b_{2}}\right)
$$

### Nochmal anschauen

## Buch 1.7

Man stelle alle Lösungen der quadratischen $z^{2}+2z+4=0$ sowohl in der Form $a+ib$, $a,b\in\mathbb{R}$, auch als Polarkoordinatenform $r(\cos \varphi+i\sin \varphi),r\geq 0,0 \leq \varphi<2\pi$, dar

$$
z_{1,2} = -\frac{p}{2} \pm \sqrt{ \frac{p^{2}}{4} -q }
$$
$$
z_{1,2}=-\frac{2}{2}\pm \sqrt{ \frac{4}{4}- 4}
$$
$$
z_{1,2} = -1\pm \sqrt{ -3 }
$$
$$
z_{1} = -1 + 3*i, z_{2} = -1 - 3*i
$$
$$
\arctan\left( \frac{-1}{3} \right)=\varphi_{1}, \arctan\left( -\frac{1}{-3} \right) = \varphi_{2}
$$
$$
1+\left( \frac{1}{3} \right)^{2} = \tan(\varphi_{1})
$$
$$
z_{1}=[10,], z_{2}=[10,]
$$

### Nochmal anschauen
## Buch 1.8
Man finde alle sechsten Wurzeln von $z=8i$ bzw. alle fünften Wurzeln von $z=\sqrt{ 2 }-\sqrt{ 6 }i$ in $\mathbb{C}$ und stelle sie in der Gauß'schen Zahlenebene dar.

$$
r= 64, \varphi=\pi
$$
$$
w_{0} = \sqrt[6] 8 , \frac{\pi}{6}
$$
$$
w_{1}=\sqrt[6]{ 8 },\frac{\pi}{6} + \frac{2\pi}{6}
$$
$$
w_{2}=\sqrt[6]{ 8 }, \frac{\pi}{6} + \frac{4\pi}{6}
$$
$$
w_{3} = \sqrt[6]{ 8 }, \frac{\pi}{6} + \frac{6\pi}{6}
$$
$$
\vdots
$$
$$
w_{5}=\sqrt[6]{ 8 }, \frac{\pi}{6} + \frac{10\pi}{6}
$$
$$
r= \sqrt[2]{ 8 }, \varphi=
$$
### Nochmal anschauen

## Buch 1.9
Man beantworte die nachstehenden Fragen:

### a
Für welche komplexen Zahlen gilt $\overline{z} = \frac{1}{z}$

### b
Man zeige $\left| \frac{z_{1}+z_{2}}{2}\right|^{2}+\left| \frac{z_{1}+z_{2}}{2}\right|^{2} = \frac{1}{2}(|z_{1}|^{2}+|z_{2}|^{2})$

### c
Man beschreibe die Menge jener komplexen Zahlen $z$ die $\mathrm{Re}\left( \frac{z-a}{b} \right) > 0$ erfüllen $(a,b \in \mathbb{C}, b\not=0)$

### d
Welche Teilmenge der komplexen Zahlenebene wird durch die Ungleichung $\left| \frac{z+4}{z-4}\right| <3$ beschrieben
### Nochmal anschauen

## Buch 1.10
Man bestimme die Richtigkeit der folgenden Behauptungen
### a
Für alle $n\in \mathbb{N}$ ist $n^{3} - n$ stets durch $3$ teilbar- mittels eines direkten Beweises

Der Ausdruck kann auch als $n*n*n-n$ geschrieben werden bzw. $n(n^{2}-1)$. Da $1$ auch $1^{2}$ ist kann man daraus eine binomische formel lösen. $n(n^{2}-1^{2}) = n(n+1)(n-1)$. Da hier drei nacheinander Folgende Zahlen multipliziert werden muss eine von den dreien durch drei teilbar sein. Somit ist der ganze Ausdruck durch drei teilbar 
### b
Ist die Summe $m+n$ zweier Zahlen $m,n\in\mathbb{Z}$ ungerade, dann ist genau einer der beiden Summanden ungerade - mittels eines indirekten Beweises

Wenn beide Summanden gerade sind, ist die Summe $m+n$ gerade. So können $m$ und $n$ dargestellt werden als $m=2*k, n=l*2$. $2*k+2*l=2(k*l)$. Somit ist die Summe der beiden Zahlen auch gerade
### c
Ist das Quadrat $n^{2}$ einer ganzen Zahl $n\in\mathbb{Z}$ gerade, dann ist auch $n$ gerade - mittels eines indirekten Beweises

Wenn $n$ nicht gerade ist, ist das Quadrat $n^{2}$ auch nicht gerade. $n$ kann dargestellt werden als ein $n=k*2+1$. Somit ist $n^{2} = n*n = (2k+1)*(2k+1)=4k^{2}+4k+1=2(2k^{2}+2k)+1$, was wieder eine ungerade Zahl ergibt.
### d
Die Aussage von a mittels eines Beweises durch vollständige Induktion
#Induktionsvoraussetzung 
$$
3*p=n^{3}-n
$$
#Induktionsanfang 
$$
0^{3}-0 = 3 * p = 3*0
$$
#Induktionsbehauptung 
$$
3*p=(n+1)^{3} - (n+1)
$$
#Induktionsschritt 
$$
3*p=3*q
$$
#### Nochmal anschauen

## Buch 1.11
Man zeige, dass für alle natürlichen Zahlen $n$ die beiden Teilbarkeitseigenschaften $2|(n^{2}+n)$ und $6|(n^{3}-n+12)$ gelten.

$$
2*p=n^{2}+n=n*n+n=(n)(n+1)
$$
Da entweder $n$ oder $n+1$ gerade sein müssen ist das Produkt der beiden Zahlen gerade und somit durch zwei teilbar.

$$
6*p=n^{3}-n+12=(n-1)(n)(n+1)+12
$$
Da zwölf insich schon durch sechs teilbar ist sieht man sich den linken Teil des Terms an. Da eine der drei Zahlen durch drei teilbar ist also ein vielfaches von drei und zumindest eine der drei Zahlen gerade also ein vielfaches von 2 ist das Produkt der drei Zahlen ein Vielfaches von $2*3=6$ und somit durch $6$ teilbar.

## Buch 1.12

Man bestimme den $ggT(7469,2464)$ sowie den $ggT(1109,4999)$ mit Hilfe des Euklidischen Algorithmus.

$$
7469 = 2464 * 3 + 77 , 2464*3=7392 , 7469-7392=69+8=77
$$
$$
2464 = 77 * 32 + 0, 30*77=2310 + 77 = 2387 + 77 = 
$$
$$
ggT()=77
$$
$$
4999 = 1109 * 4 + 578, 1104*4=4412, 4999-4412=500-1+88=587  
$$
$$
1109 = 578 * 1 + 531, 1109-578=22+400+109=531
$$
$$
578 = 531 * 1 + 47, 19+28=38+9=47
$$
$$
531=47* 11+14 , 11 * 47 = 470 + 47 = 517  
$$
$$
47 = 14 * 3 + 5
$$
$$
14 = 5 * 2 + 4
$$
$$
5 = 4 * 1 + 1
$$
$$
4 = 1 * 4 +0
$$
$$
ggT()=1
$$
## Buch 1.13

Man bestimme alle ganzen Zahlen $x,y$, welche die Gleichung $243x+198y=9$ erfüllen.

$$
243x + 198y = 9, \frac{243}{9}=9*20=180+9*5=225 + 234, 243 = 9*27, 198 = 9 * 20 + 2 * 9
$$
$$
27x + 22y = 1 
$$
$$
27 = 22 * 1 + 5
$$
$$
22 = 5 * 4 + 2
$$
$$
5 = 2 * 2 + 1
$$
$$
2 = 1 * 2 +0
$$
$$
1=5-2*2
$$
$$
1=5-2*(22-5*4)
$$
$$
1=5 - 2 * 22 + 5 * 4 * 2
$$
$$
1 = 9 * 5 - 2 * 22
$$
$$
1 = 9 * (27-22) - 2 * 22 
$$
$$
1 = 27 * 9 - 11 * 22
$$
$$
x=9, y=-11
$$
## Buch 1.14

Man zeige für alle natürliche Zahlen $a,b$ die Eigenschaft $ggT(a,b) * kgV(a,b)=a*b$

$$
ggT(a,b) = \prod_{p\in\mathbb{P}}p^{min\{ v_{p}(a),v_{p}(b) \}}, ~~~~~ kgV(a,b) = \prod_{p\in \mathbb{P}}p^{max\{ v_{p}(a),v_{p}(b) \}}
$$
Multipliziert man die beiden Primfaktor tritt entweder der Primfaktor von $a$ im ggT oder im kgV auf, gleiches für b, somit setzt sich die Multiplikation aus allen Primfaktoren zusammen und entspricht einer Multiplikation der beiden Zahlen.

## Buch 1.15

Man zeige, dass jede ganze Zahl der Form $n^{4}+4^{n}$ mit $n>1$ keine Primzahl ist. (Hinweis: Man unterscheide zwischen geradem $n$ und ungeradem $n$ Insbesondere betrachte man bei ungeradem $n$ die Zerlegung $(n^{2}+2^{n}+n2^{(n+1)/2})(n^{2}+2^{n}-n2^{(n+1)/2})$.)

ist n gerade so werden offensichtlich zwei gerade zahlen addiert

ist n ungerade so kann der Term $n^{4}+4n$ auch als Faktor von einer Zerlegung dargestellt werden. Somit muss man nur noch beweisen, dass keiner der beiden Einzelteile gleich 1 ist.
Bei $n^{2}+2^{n}+n 2^{(n+1)/2}$ ist dies offensichtlich da nur zahlen addiert werden. Bei $n^{2}+2^{n}-n2^{(n+1)/2}$ ist dies der Fall, da $n=2k+1$ ist die gleichung
$$
(2k+1)^{2}+2^{2k+1}-(2k+1)2^{(2k+2)/2}
$$
$$
4k^{2}+4k+1+2*2^{2k}-2*2^{k}*(2k+1)
$$
$$
4k^{2}+4k+1+2*2^{k}(2^{k}-2k-1)
$$
Da für ein k von 1 der Gesamte Ausdruck >1 ist, und für jedes größere k ein positiver klammerausdruck folgt, ist dies wieder eine addition aus nur positiven termen für k>1 und eine faktor ungleich 1.
## Buch 1.16


Lösen Sie die folgenden Kongruenzen bzw. beweisen Sie deren Unlösbarkeit

### a
$$
8x \equiv 4 \mod 16
$$
$$
2x \equiv 1 \mod 4
$$
Unlösbar da keine gerade Zahl durch 4 einen Rest von $1$ haben kann. $ggT(2,4)=2$

### b
$$
8x \equiv 4 \mod 15
$$
$$
2x \equiv 1 \mod 15
$$
$$
2x=1+q*15
$$
$$
2x = 1+15
$$
$$
x=8
$$
### c
$$
3x \equiv 9 \mod 11
$$
$$
x \equiv 3 \mod 11
$$
$$
x=3+11*p
$$
$$
x=3
$$
### d
$$
3x \equiv 9 \mod 12
$$
$$
x \equiv 3 \mod 4
$$
$$
x=3+4*p
$$
$$
x=3
$$
### e
$$
x^{2}-3x+2\equiv0 \mod 5
$$
$$
2 \equiv x(3-x) \mod 5
$$
$$
x = 1 *  5*p, x=2+5*q
$$
### f
$$
x^{2}-3x+2\equiv0 \mod 6
$$
## Buch 1.17
Im europäischen Artikelnummersystem EAN werden Zahlen mit 13 Dezimalziffern der Form $a_{1},a_{2},\dots,a_{12}p$ verwendet. Dabei wird die letzte der 13 Ziffern, das ist die Prüfziffer $p$, im EAN-Code so bestimmt, dass
$$
a_{1}+3a_{2}+a_{3}+3a_{4}+\dots+a_{11}+3a_{12}+p \equiv 0 \mod 10
$$
gilt. Man zeige, dass beim EAN-Code ein Fehler in einer einzelnen Ziffer stets erkannt wird, während eine Vertauschung von zwei benachbarten Ziffern genau dann nicht erkannt wird, wenn die beiden Ziffern gleich sind oder sich um 5 unterscheiden

Man nehme zwei EAN Codes an, welche sich an der Stelle $j$ unterscheiden
$$
s + n * x_{j} \equiv s + n * y_{j} \mod 10
$$
Da $ggT(n,10)=1$, wobei $n$ entweder $1$ oder $3$ ist, folgt
$$
x_{j}\equiv y_{j} \mod 10
$$
und da $x_{j}$ und $y_{j}$ per Definition Ziffern zwischen $\{ 0,1,\dots,9 \}$ sind folgt.
$$
x_{j} = y_{j}
$$
Eine Vertauschung zweier benachbarter Ziffern würde bedeuten.

$$
s + 3 * a + b \equiv s + a + 3*b \mod 10 \implies (3-1)(a-b) \equiv 0 \mod 10
$$
$$
2(a-b) \equiv 0 \mod 10
$$
$$
2a\equiv 2b \mod 10
$$$$
a \equiv b \mod 5 
$$
$$
a=b
$$
So ist eine Vertauschung erkannt, es sei denn der Unterschied zwischen den beiden Zahlen beträgt 5
## Buch 1.18
Sei $a$ die Aussage "Es gibt eine größte natürliche Zahl" und $b$ die Aussage "0 ist die größte natürliche Zahl". Man entscheide, ob die Aussagen $a\implies b$ bzw. $b\implies a$ wahr oder falsch sind.
$b\implies a$ ist wahr da eine falsche Aussage immer eine richtige Implikation ist. $a \implies b$ ist wahr da beide Aussagen falsch sind. 
## Buch 1.21

Sei M eine nichtleere endliche Menge. Man zeige, dass M gleich viele Teilmengen mit gerader Elementanzahl wie solche mit ungerader Elementanzahl besitzt, indem man ein Verfahren angebe, das aus den Teilmengen der einen Art umkehrbar eindeutig die der anderen Art erzeugt

Teilmengen mit $0\leq j\leq n$ Elementen
k-elementigen Teilmengen mit $\binom{n}{k}$ Permutationen
Insgesamt $2^{n}$ Teilmengen

Ein Verfahren wäre zu jede Teilmenge ihrer Differenz zur gesamten Menge zuzuweisen. So hätte in einer Menge $\{ 1,2,3 \}$ die Teilmenge $\{ 1,2 \}$ das Gegenstück $\{ 3 \}$ oder die Teilmenge $\{ 1,2,3 \}$ das Gegenstück $\emptyset$.

## Buch 1.22
Sei $A=\{ 1,2,\dots,8 \}$ und $R$ eine binäre Relation auf $A$ definiert durch
$$
aRb \iff a=b \text{ oder } ggT(a,b) = 2
$$
Man gebe explizit die Relation $R$ sowie ihren Graphen $G(R)$ an

$$
R = \{ (1,1),(2,2),(3,3),(4,4),(5,5),(6,6),(7,7),(8,8),(2,4),(2,6),(2,8),(4,2),(4,6),(6,2),(6,4),(6,8),(8,2),(8,6) \}
$$


## Buch 1.23
Man untersuche nachstehend angeführte Relationen $R \subseteq M^{2}$ in Hinblick auf die Eigenschaften Reflexivität, Symmetrie, Transitivität und Antisymmetrie

### a
$M =$ Menge aller Einwohner von Wien $a R b \iff a$ ist verheiratet mit $b$
Menschen sind nicht mit sich selbst verheiratet also nicht reflexiv
Relation ist Symmetrisch
Relation ist nicht Antisymmetrisch
Relation ist nicht transitiv

### b
$M$ wie oben, $aRb \iff a$ ist nicht älter als b
Relation ist reflexiv
Relation ist antisymmetrisch
Relation ist nicht symmetrisch
Relation ist transitiv

### c
$M$ wie oben, $aRb \iff a$ ist so groß wie $b$
Relation ist reflexiv
Relation ist Symmetrisch und Antisymmetrisch
Relation ist transitiv

### d
$M = \mathbb{R} ~~aRb \iff a-b \in \mathbb{Z}$
Relation ist reflexiv
Relation ist symmetrisch
Relation ist nicht antisymmetrisch
Relation ist transitiv

### e
$M = \mathbb{R}^{n}, (x_{1},x_{2},\dots,x_{n})R(y_{1},y_{2},\dots,y_{n}) \iff x_{i}\leq y_{1} (i=1,\dots,n)$
Relation ist Reflexiv
Relation ist nicht Symmetrisch
Relation ist Antisymmetrisch
Relation ist transitiv

## Buch 1.24
Man zeige, dass durch $aRb \iff 3|a^{2}-b^{2}$ für alle $a,b \in \mathbb{Z}$ eine Äquivalenzrelation $R$ in der Menge $\mathbb{Z}$ erklärt wird und bestimme die zugehörende Partition

Reflexivität
$$
\forall a \in \mathbb{Z}: aRa \iff
3|a^{2}-a^{2} = 3| 0 
$$
Symmetrie
$$
\forall a,b \in \mathbb{Z}: aRb \implies bRa
$$
$$
3| a^{2}-b^{2} \implies 3 | b^{2} - a^{2}
$$
$$
3*p=a^{2}-b^{2} \implies 3*q = b^{2}- a^{2} ~~~~p,q \in \mathbb{Z}
$$
$$
3*p= a^{2}-b^{2} \implies 3*q*(-1)=a^{2}-b^{2}
$$
$$
3*p = a^{2}-b^{2} \implies 3*q_{2} = a_{2} - b^{2} ~~~~~q_{2} \in \mathbb{Z}
$$

Transitivität
$$
aRb \land bRc \implies aRc
$$
$$
3 * p = a^{2}-b^{2} \land 3 * q = b^{2}-c^{2}
$$
$$
3*p+3*q=a^{2}-b^{2}+b^{2}-c^{2}
$$
$$
q=0, 3*p=a^{2}-c^{2}
$$

$$
K(a) = \{ b \in \mathbb{Z} | b^2-a^{2} \equiv 0 \mod 3 \} 
$$

## Buch 1.25
Sei $f: A \rightarrow B$ eine Funktion. Man zeige, dass durch $x\equiv y \iff f(x)=f(y)$ eine Äquivalenzrelation $\equiv$ auf der Menge $A$ definiert wird.

Reflexivität
$$
x \equiv x \iff f(x) = f(x)
$$
Symmetrie
$$
x \equiv y \implies y \equiv x : f(x) = f(y) \implies f(y) = f(x)
$$
Transitivität
$$
x \equiv y \land y \equiv z \implies x \equiv z : f(x)=f(y) \land f(y)=f(x) \implies f(x) = f(z)
$$
## Buch 1.26
Untersuchen Sie ob die Relation $ARB \iff A \vartriangle B = \emptyset$ Auf der Potenzmenge einer Menge $M$ eine Äquivalenzrelation bildet

Reflexivität
$$
A \vartriangle A = \emptyset \implies A = A
$$

Symmetrie
$$
A /B \cup  B/A = \emptyset : B/A \cup A/B = \emptyset
$$
$$
A/B \cup B/A = B/A \cup A/B = \emptyset
$$
$$
A = B
$$
Transitivität
$$
A \vartriangle B = \emptyset\land B \vartriangle C=\emptyset \implies A \vartriangle C = \emptyset
$$
Da die Mengen gleich sein müssen kann man schreiben
$$
A = B \land B = C \implies A = C
$$
## Buch 1.27
Man vergleiche die Hassediagramme der beiden Halbordnungen $(P(\{ a,b,c \}),\subseteq)$ und $(T_{70},|)$ wobei $T_{70} = \{ n\in \mathbb{N}:n|70 \}$

Die Hassediagramme schauen gleich aus wenn man sie aufzeichnet,

## Buch 1.28
Für $k,n \in \{ 1,2,3,\dots,10 \}$
[[Hausübung 4#128)]]

## Buch 1.29
Man zeige: $(\mathbb{C},\leq)$ ist Halbordnung mit $z = a+ib \leq w=c+id$, falls $a<c$ oder $a=c$ und $b\leq d$. Weiters gebe man drei verschiedene komplexe Zahlen $z_{1},z_{2},z_{3} \in C \setminus \{ 0 \}$ an für die $z_{1}\leq z_{2}$ und $z_{3}\geq 0$ aber $z_{3}z_{1}\geq z_{3}z_{2}$ 

Reflexivität
$$
zRz: a\leq a \land b\leq b 
$$

Antisymmetrie
$$
(a\leq c \land b \leq d) \land (c \leq a \land d \leq b)
$$
$$
\implies a = c \land b = d
$$
Transitivität
$$
(a\leq c \land b \leq d) \land (c \leq e \land d \leq f) \implies (a \leq e) \land (b \leq f)
$$
$$
a\leq c \leq e \implies a\leq e, b \leq d \leq f \implies b\leq f
$$

$$
z_{1}*z_{3} = (a_{1}a_{3}-b_{1}b_{3} )+ i(a_{1}b_{3}+a_{3}b_{1})
$$
$$
z_{2}*z_{3} = (a_{2}a_{3}-b_{2}b_{3} )+ i(a_{2}b_{3}+a_{3}b_{2})
$$
$$
z_{1} = 1 + i 2, z_{2} = 2 + 10 i , z_{3} = 2 +i 1
$$
$$
a_{13}=1*2-2*1 = 0, a_{23} = 2*2-10 = -6
$$

## Buch 1.30
Untersuchen Sie, ob es sich bei folgenden Relationen $R \subseteq A \times B$ um Funktionen, injektive Funktionen, surjektive Funktionen, bzw. bijektive Funktionen handelt

### a
$R = \left\{  \left( x^{2}, \frac{1}{x^{2}} \right) | x \in \mathbb{R}^{+}  \right\}, A=B=\mathbb{R}$
$$
f(x^{2}) = \frac{1}{x^{2}}
$$
Da Der Menge $\mathbb{R}^{-}$ keine Werte zugeordnet werden handelt es sich hier nicht um eine Funktion
### b
$R$ wie oben jedoch $A=B=\mathbb{R}^{+}$

Jedes $x \in \mathbb{R}^{+}$ bildet auf einen anderen Wert in $\mathbb{R}^{+}$ einmal ab, somit handelt es sich hier um eine Funktion

$$
f(x^{2}) = \frac{1}{x^{2}}
$$
$$
f(x) = \sqrt{ \frac{1}{x^{2}} } = \frac{1}{x}
$$
injektiv
$$
f(x_{1})=f(x_{2})\implies x_{1}=x_{2}
$$
$$
\frac{1}{x_{1}}=\frac{1}{x_{2}}
$$
$$
x_{2}=x_{1} \implies x_{1}=x_{2}
$$


surjektivität
 $\frac{1}{x}$ ist in $R^{+}$ surjektiv, weil $∀b∈B∃a∈A:b=f⁡(a)$ gilt. (für jedes Element des Bildbereichs B lässt sich ein zugehöriges Element aus dem Definitionsbereich A finden)
### Beweisen?

bijektivität 
die die Funktion surjektiv und injektiv ist, ist sie auch bijektiv

### c
$R = \{ log_{2}x,x | x \in \mathbb{R}^{+} \}, A=B=\mathbb{R}$
[[Hausübung 4#139)]]
## Buch 1.31
Zu den nahestehenden Abbildungen $f$ bzw. $g$ auf der Menge $\{ 0,1,\dots,9 \}$ bestimme man jeweils den zugehörenden Graphen und untersuche die angegebene Zuordnung auf Injektivität, Surjektivität und Bijektivität

### a
$f(x)=x^{2} \mod 10$
$$
x = 0 \implies 0
$$
$$
x = 1 \implies 1
$$
$$
x = 2 \implies 4
$$
$$
x = 3 \implies 9
$$
$$
x = 4 \implies 6
$$
$$
x = 5 \implies 5
$$
$$
x = 6 \implies 6
$$
$$
x = 7 \implies 9
$$
$$
x = 8 \implies 4
$$
$$
x = 9 \implies 1
$$
Weder injektiv da 4,1 6 und 9 mehrfach vorkommen und nicht surjektiv da 2 3 6 und 8 garnicht vorkommen
### b
$g(x)=x^{3} \mod 10$

$$
x=0 \implies 0
$$
$$
x= 1 \implies 1
$$
$$
x = 2 \implies 8
$$
$$
x = 3 \implies7
$$
$$
x = 4 \implies 4
$$
$$
x = 5 \implies 5
$$
$$
x = 6 \implies 6
$$
$$
x = 7 \implies 3
$$
$$
x = 8 \implies  2
$$
$$
x = 9 \implies 9
$$
Die Funktion ist surjektiv, injektiv und daher auch bijektiv
## Buch 1.32
Man zeige, dass die Funktion bijektiv ist, und bestimme ihre Umkehrfunktion

### a
$f: \mathbb{R}\setminus \{ 7 \} \rightarrow \mathbb{R}\setminus \{ 2 \},x\rightarrow \frac{2x+1}{x-7}$

Injektivität
$$
f(x_{1})=f(x_{2}) \implies x_{1} = x_{2}
$$
$$
\frac{2x_{1}+1}{x_{1}-7}=
\frac{2x_{2}+1}{x_{2}-7}
$$
$$
(2x_{1}+1)(x_{2}-7)=(2x_{2}+1)(x_{1}-7)
$$
$$
2x_{1}x_{2}-14x_{1}+x_{2}-7=2x_{1}x_{2}-14x_{2}+x_{1}-7
$$
$$
x_{2}-14x_{1}=x_{1}-14x_{2}
$$
$$
15x_{1}=15x_{2}
$$
$$
x_{1}=x_{2}
$$
Surjektivität
$$
\forall y \in \mathbb{R} \setminus \{ 2 \} \exists x:f(x)=y
$$
$$
y=\frac{2x+1}{x-7}
$$
$$
y(x-7)=2x+1
$$
$$
xy-7y=2x+1
$$
$$
-1-7y=2x-xy
$$
$$
-1-7y=x(2-y)
$$
$$
\frac{-1-7y}{2-y}=x
$$
$$
f^{-1}=\frac{-1-7y}{2-y}
$$
### b
$f: \mathbb{R}\setminus\{ 2 \}\rightarrow \mathbb{R}\setminus\{ -1 \},x\rightarrow \frac{x+3}{2-x}$

Injektivität
$$
f(x_{1})=f(x_{2})\implies x_{1}=x_{2}
$$
$$
\frac{x_{1}+3}{2-x_{1}}=\frac{x_{2}+3}{2-x_{2}}
$$
$$
(x_{1}+3)(2-x_{2})=(x_{2}+3)(2-x_{1})
$$
$$
2x_{1}-x_{1}x_{2}+6-3x_{2}=2x_{2}-x_{1}x_{2}+6-3x_{1}
$$
$$
2x_{1}-3x_{2}=2x_{2}-3x_{1}
$$
$$
5x_{1}=5x_{2}
$$
$$
x_{1}=x_{2}
$$
Surjektivität
$$
\forall y \in \mathbb{R} \setminus \{ -1 \} \exists x: f(x) =y
$$
$$
y=\frac{x+3}{2-x}
$$
$$
y(2-x)=x+3
$$
$$
2y-yx=x+3
$$
$$
2y-3=x+xy
$$
$$
2y-3=x(1+y)
$$
$$
\frac{2y-3}{1+y}=x
$$
$$
f^{-1}=\frac{2y-3}{1+y}
$$
