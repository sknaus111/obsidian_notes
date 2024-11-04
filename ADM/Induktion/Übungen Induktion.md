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

# VOWI


## [[Hausübung 1#15)]]
## [[Hausübung 1#24)]] 