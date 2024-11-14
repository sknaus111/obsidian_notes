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
#### Nochmal anschauen

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

$10101 ~~~~~ 10001
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

## Buch 1.19

