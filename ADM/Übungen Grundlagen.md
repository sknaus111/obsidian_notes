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
F_{n+2}=\frac{1}{\sqrt{ 5 }}  \bigg [ \bigg (     \frac{1+\sqrt{ 5 }}{2}     \bigg)^{n+1}-\bigg (    \frac{1-\sqrt{ 5 }}{2}   \bigg)^{n+1}\bigg ] + \frac{1}{\sqrt{ 5 }}  \bigg [ \bigg (     \frac{1+\sqrt{ 5 }}{2}     \bigg)^n-\bigg (    \frac{1-\sqrt{ 5 }}{2}   \bigg)^n\bigg ]
$$
$$
= \frac{1}{\sqrt{ 5 }} (a^{n+1}-b^{n+1})+\frac{1}{\sqrt{ 5 }} (a^{n}-b^{n})
$$
$$
=\frac{a*a^{n}}{\sqrt{ 5 }} - \frac{b*b^{n}}{\sqrt{ 5 }}+\frac{a^{n}}{\sqrt{ 5 }} -\frac{b^{n}}{\sqrt{ 5 }}
$$
$$
=(a^{n})\left( \frac{a}{\sqrt{ 5 }} +\frac{1}{\sqrt{ 5 }} \right) - (b^{n})\left( \frac{b}{\sqrt{ 5 }} + \frac{1}{\sqrt{ 5 }} \right)
$$
$$
=a^{n} \left( \frac{\frac{1+\sqrt{ 5 }}{2}}{\sqrt{ 5 } } + \frac{1}{\sqrt{ 5 }} \right) - b^{n}\left( \frac{\frac{1-\sqrt{ 5 }}{2}}{\sqrt{ 5 }} +\frac{1}{\sqrt{ 5 }} \right)
$$
$$
a^{n}\left( \frac{1+\sqrt{ 5 }}{2*\sqrt{ 5 }} +\frac{2}{2*\sqrt{ 5 }} \right) - b^{n} \left( \frac{1-\sqrt{ 5 }}{2*\sqrt{ 5 }} + \frac{2}{\sqrt{ 5 }} \right)
$$
$$
a^{n}\left( \frac{3+\sqrt{ 5 }}{2*\sqrt{ 5 }} \right) - b^{n}\left( \frac{3-\sqrt{ 5 }}{2*\sqrt{ 5 }} \right)
$$
$$
\frac{1}{\sqrt{ 5 }}\left( \frac{3*a^{n}+\sqrt{ 5 }*a^{n}}{2} \right) - \frac{1}{\sqrt{ 5 }} \left( \frac{3*b^{n}+\sqrt{ 5 }*b^{n})}{2}\right)
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
$$
= \frac{n+1}{6}*(2*(n^{2}+2n+1)+6n+6+4)
$$
$$
= \frac{n+1}{6 } *(2n^{2}+4n+2+6n+6+4)
$$
$$
= \frac{n+1}{6} * ( 2n^{2}+10n+12)
$$
$$
=\frac{1}{6} (2n^{3}+2n^{2}+10n^{2}+10n+12n+12)
$$
$$
=\frac{1}{6}(2n^{3}+12n^{2}+22n+12)
$$
#Induktionsschritt 
$$
\sum_{j=1}^{n+1} j (j+1)=\sum_{j=1}^{n} j (j+1) + (n+1)((n+1)+1)
$$
$$
= \frac{n}{6} ( 2n^{2}+6n+4) + (n+1)(n+2)
$$
$$
=\frac{1}{6}*(2n^{3}+6n^{2}+4n+6*(n+1)(n+2))
$$
$$
=\frac{1}{6} * (2n^{3}+6n^{2}+4n + 6n^{2}+12n+6n+12)
$$
$$
=\frac{1}{6}*(2n^{3}+12n^{2}+22n+12)
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

### GRR
## Buch 1.3
Man zeige, dass die Zahlen $\sqrt{ 3 }$, $\sqrt{ 5 }$ und $\sqrt[3]{ 2 }$ irrational sind

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
$$
m=k*2
$$
$$
(k*2)^{3}=n^{3}*2
$$
$$
k^{3}*8=n^{3}*2
$$
$$
(2*k^{3})*2=n^{3}
$$
Widerspruch da in der annahme m und n unkürbar sind

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

$$
\arctan \left( \frac{y_{1}}{x_{1}} \right) + \arctan\left( \frac{y_{2}}{x_{2}} \right) = 
$$
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
z_{1,2} = -1\pm i*\sqrt{ 3 }
$$
$$
z_{1} = -1 + \sqrt{ 3 }*i, z_{2} = -1 - \sqrt{ 3 }*i
$$
$$
z_{1}=[2,], z_{2}=[2,]
$$
$$
\cos = \frac{a}{r} = \frac{1}{2}
$$
$$
\sin = \frac{b}{r} = \frac{\sqrt{ 3 }}{2}
$$
### Nochmal anschauen
## Buch 1.8
Man finde alle sechsten Wurzeln von $z=8i$ bzw. alle fünften Wurzeln von $z=\sqrt{ 2 }-\sqrt{ 6 }i$ in $\mathbb{C}$ und stelle sie in der Gauß'schen Zahlenebene dar.

$$
r= 64, \varphi=\frac{\pi}{2}
$$
$$
w_{0} = \sqrt[6] 8 , \frac{\pi}{12}
$$
$$
w_{1}=\sqrt[6]{ 8 },\frac{\pi}{12} + \frac{2\pi}{6}
$$
$$
w_{2}=\sqrt[6]{ 8 }, \frac{\pi}{12} + \frac{4\pi}{6}
$$
$$
w_{3} = \sqrt[6]{ 8 }, \frac{\pi}{12} + \frac{6\pi}{6}
$$
$$
\vdots
$$
$$
w_{5}=\sqrt[6]{ 8 }, \frac{\pi}{12} + \frac{10\pi}{6}
$$
$$
r= 2 * \sqrt{ 2 }, \varphi=\arctan\left( -\frac{\sqrt{ 6 }}{\sqrt{ 2 }} \right) = \arctan(- \sqrt{ 3 })
$$
$$
\sqrt[5]{ 2*\sqrt[2]{ 2 } } = (2*2^{1/2})^{1/5} = 2^{1/5}*2^{1/10} = 2^{3/10}
$$
$$
w_{0} = \sqrt[10]{ 2^{3} }, \frac{\pi}{15} + \frac{2*\pi*0}{5}
$$
$$

$$
### Nochmal anschauen

## Buch 1.9
Man beantworte die nachstehenden Fragen

### a
Für welche komplexen Zahlen gilt $\overline{z}=\frac{1}{z}$

$$
\frac{1}{z}=\frac{\overline{z}}{z*\overline{z}}=\frac{\overline{z}}{|z|^{2}}
$$
Gilt für alle komplexen Zahlen mit einem Betrag von 1
### b
Man zeige  $|\frac{z_{1}+z_{2}}{2}|^{2}+|\frac{z_{1}-z_{2}}{2}|^{2}=\frac{1}{2}(|z_{1}|^{2}+|z_{2}|^{2})$

$$
\left | \frac{a_{1}+a_{2}}{2} + i \frac{(b_{1}+b_{2})}{2} \right |^{2} + \left|\frac{a_{1}-a_{2}}{2} + i \frac{b_{1}-b_{2}}{2}\right|^{2} 
$$
$$
= \frac{a_{1}+a_{2}}{2}+\frac{b_{1}+b_{2}}{2} + \frac{a_{1}-a_{2}}{2} + \frac{b_{1}-b_{2}}{2}
$$
$$
= 
$$
#### Nochmal anschauen
### c
Man beschreibe die Menge jener komplexen Zahlen $z$ die $\mathrm{Re}\left( \frac{z-a}{b}  \right) > 0$ erfüllen 
#### Nochmal anschauen
### d
Welche Teilmenge der komplexen Zahlen wird durch die Ungleichung $|\frac{z+4}{z-4}| <3$ beschrieben
[[Hausübung 2#48)]]

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
3*p=(n-1)(n)(n+1) ~~~~~p \in \mathbb{Z}
$$
#Induktionsanfang 
$$
(1-1)(1)(1+1)=0 = 3*0 
$$
#Induktionsbehauptung 
$$
3*p=((n+1)-1)(n+1)((n+1)+1)
$$
#Induktionsschritt 
$$
=(n)(n+1)(n+2) ~~| ~3
$$

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

### Nochmal schauen
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
2 \equiv 3x-x^{2} \mod 5
$$
$$
2 \equiv x(3-x) \mod 5
$$
$$
x=0 \implies 2 \equiv 0  \mod 5
$$
$$
x = 1 \implies 2 \equiv 2 \mod 5
$$
$$
x = 2 \implies 2 \equiv 2 \mod 5
$$
$$
x = 3 \implies 2 \equiv 0 \mod 5
$$
$$
x = 4 \implies2 \equiv 1 \mod 5
$$
$$
x=1 +5*p, x=2+5*q
$$
### f
$$
x^{2}-3x+2\equiv0 \mod 6
$$
$$
2\equiv x(3-x) \mod 6
$$
$$
x = 0 \implies 2 \equiv 0 \mod 6
$$
$$
x=1 \implies 2 \equiv 2 \mod 6
$$
$$
x = 2 \implies 2 \equiv 2 \mod 6
$$
$$
x = 3 \implies 2 \equiv 0 \mod 6
$$
$$
x = 4 \implies 2 \equiv 2 \mod 6
$$
$$
x = 5 \implies 2 \equiv 2 \mod 6
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
## Buch 1.19
Entscheiden Sie mit Hilfe einer Wahrheitstafel, ob die folgenden Äquivalenzen richtig sind:

### a
$$
a \lor (b\lor c) \implies (a \lor b) \lor c
$$
### b
### c
### d
### e
### f

## Buch 1.20

### a
### l

## Buch 1.21
Sei $M$ eine nichtleere endliche Menge. Man zeige, dass $M$ gleich viele Teilmengen mit gerader Elementanzahl wie solche mit ungerade Elementanzahl besitzt, indem man ein Verfahren angebe, das aus den Teilmengen der einen Art umkehrbar eindeutig die der anderen Art erzeugt.

$$

$$

## Buch 1.22
Sei $A = \{ 1,2,\dots,8 \}$ und $R$ eine binäre Relation auf $A$, definiert durch
$$
a R b \iff a=b
 \text{ oder }ggT(a,b)=2$$
 Man gebe explizit die Relation $R$ sowie ihren Graphen $G(R)$ an

Die Relation beschreibt, ob die Zahlen gleich oder gerade sind.

Der Graph verbindet jede Zahl mit einer Schlinge zu sich selbst und die gerade Zahlen miteinander.
## Buch 1.23

Man untersuche nachstehend angeführte Relationen $R \subseteq M^{2}$ in Hinblick auf die Eigenschaften Reflexivität. Symmetrie, Transitivität und Antisymmetrie

### a
$M =$ Menge aller Einwohner von Wien, $aRb \iff a$ ist verheiratet mit $b$

nicht Reflexiv da man nicht mit sich selber verheiratet sein kann. Symmetrisch und daher nicht antisymmetrisch. Auch nicht transitiv.
### b
$M$ wie oben, $aRb \iff a$ ist nicht älter als $b$

Reflexiv, da gleich alt auch nicht älter bedeuten kann. Antisymmetrisch da es ein kleiner gleich vergleich ist. Transitiv ist ebenfalls wahr.
### c
$M$ wie oben, $aRb \iff a$ ist so groß wie $b$

Reflexiv, symmetrisch und antisymmetrisch, transitiv
### d
$M=\mathbb{R}, aRb \iff a-b \in \mathbb{Z}$

Reflexiv da 
$a-a=a-a=0$
Antiymmetrisch

$$
a-b=b-a
$$
$$
a+a=b+b
$$
$$
2(a)=2(b)
$$
$$
a=b
$$
Dadurch auch nicht symmetrisch
Transitiv
$$
a-b=z_{1}, b-c=z_{2}
$$
$$
a-c=
$$
#### Nochmal anschauen
### e
$M=\mathbb{R}^{n}, (x_{1},\dots,x_{n)}R(y_{1},\dots,y_{n}) \iff x_{i}\leq y_{i}(i=1,\dots,n)$

#### Nochmal anschauen

## Buch 1.24
Man zeige, dass durch $aRb \iff 3|a^{2}-b^{2}$ für alle $a,b \in \mathbb{Z}$ eine Äquivalenzrelation $R$ in der Menge $\mathbb{Z}$ erklärt wird, und bestimme die zugehörende Partition

Reflexivität
$$
3*q=a^{2}-a^{2}
$$
$$
3*q=0
$$

Symmetrie

$$
3*q = a^{2}-b^{2} \iff 3* p = -a^{2} + b^{2} ,~~~~~~~~(p=q*-1)
$$
Transitivität
$$
3 * q = a^{2}-b^{2}, 3*p = b^{2}-c^{2}
$$
$$
b^{2}=a^{2}-3*q
$$
$$
3*p=a^{2}-3*q-c^{2}
$$
$$
3*p+3*q=a^{2} - c^{2}
$$
$$
3(p+q)=a^{2}-c^{2}
$$
$$
3r=a^{2}-c^{2}
$$

$$
K(0) = \{ a\in \mathbb{Z}| ~ a \equiv 0 \mod 3 \}
$$
$$
K(1) = \{ a \in \mathbb{Z} | a \equiv1 \mod 3 \}
$$
$$
K(2) = \{ a \in \mathbb{Z} | a \equiv 2 \mod3 \}
$$

## Buch 1.25
Sei $f: A \rightarrow B$ eine Funktion. Man zeige, dass durch $x \equiv y \iff f(x) = f(y)$ eine Äquivalenzrelation $\equiv$ auf der Menge $A$ definiert wird

### Nochmal anschauen

## Buch 1.26
Untersuchen Sie, ob die Relation $ARB \iff A\vartriangle B = \emptyset$ auf der Potenzmenge einer Menge $M$ eine Äquivalenzrelation bildet ($\vartriangle$ bezeichnet die symmetrische Differenz)

Reflexivität
$$
A \vartriangle A = \emptyset
$$
Symmetrie
$$
A \vartriangle B = (A \backslash B ) \cup (A\backslash B) \iff (B\backslash A) \cup (A\backslash B) = B \vartriangle A 
$$
Transitivität
$$
A \vartriangle B \land B \vartriangle C \iff ((A \cap B)' \cap (A \cup B)) \cap ((B\cap C)'\cap(B\cup C))
$$
$$
\iff ((A' \cup B') \cap (A \cup B)) \cap ((B' \cup C') \cap (B \cup C))
$$
$$
\iff (A \cap (A'\cup B'))\cup(B \cap(A' \cup B')) \cap (B \cap(B' \cup C') \cup(C \cap (B' \cup C')) )
$$
$$
(B'\cup B)
$$

### Nochmal anschauen



$$
A \vartriangle B \land B \vartriangle C \iff ((A\backslash B) \cup (B\backslash A)) \land ((B\backslash C)\cup(C\backslash B))
$$
$$

$$
## Buch 1.27
Man vergleiche die Hassediagramme der beiden Halbordnungen $(P(\{ a,b,c \}),\subseteq)$ und $(T_{70},|)$, wobei $T_{70}=\{ n \in \mathbb{N} | ~n|70 \}$

### Später anschauen
## Buch 1.28
### Ich kann diese Funktionscheiße nicht mehr

## Buch 1.29
## Buch 1.30
## Buch 1.31
## Buch 1.32