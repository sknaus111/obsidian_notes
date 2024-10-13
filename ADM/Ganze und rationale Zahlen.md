Z,Q 
Da nicht alle Gleichungen in den natürlichen Zahlen lösbar sind fügt man die #Ganzen_Zahlen und die #Rationalen_Zahlen hinzu.

Man nehme $m,n \in \mathbb{N}$.
$$
n+x=m ,n>m
$$

Die Lösung der Gleichung ist nun die ganze Zahl $x$

$$
x = m-n
$$
Für eine Gleichung der Form 

$$
n*y=m
$$
ist die Lösung der Gleichung die rationale Zahl $y$
$$
y=\frac{m}{n}
$$

## Ganze Zahlen
Um #Multiplikation und #Addition für ganze Zahlen einzuführen muss zuerst angeschaut werden, wie diese konstruiert sind. Zusätzlich zu jeder natürlichen Zahlen $n$ wird ihr negatives Gegenstück $-n$ betrachtet. 

Im nächsten Schritt wird die Addition für die ganzen Zahlen definiert.

$(-m)+(-n)=-(m+n) \text{ für }n,m\geq 0$
$m+(-n)=(-n)+m=m-n \text{ für }0\leq n\leq m$ 
$m+(-n)=(-n)+m=-(n-m)$

Der Begriff negative Zahl wird wie folgt definiert.

$-(-n) = n \text{ für }n>0$

Mit dieser Festlegung wird auch die Subtraktion definiert.

$n-m=n+(-m)$

## Rationale Zahlen

Ähnlich wie die negative Zahl bei den ganzen Zahlen existiert der Kehrwert als Umkehrung von rationalen Zahlen $\mathbb{Q}$.

$$r^{-1}=\frac{1}{r} \text{ für }r=\frac{m}{n} \not = 0$$

So hat ist der Kehrwert folgender rationaler Zahl zu erkennen.

$$\left( \frac{m}{n} \right)^{-1}=\frac{1}{\frac{m}{n}}=\frac{n}{m}$$

Da rationale Zahlen aber auch die ganzen Zahlen umfassen wird ebenfalls die negative Zahl $-r$ einer rationalen Zahl $r=\frac{m}{n}$ definiert

$$-r = - \frac{m}{n}=\frac{-m}{n}$$

Schließlich wird auch die #Addition und #Multiplikation von zwei rationalen Zahlen $r = \frac{m}{n}$ und $s=\frac{k}{l}$
$$r+s=\frac{m}{n}+\frac{k}{l}=\frac{ml+nk}{nl}$$ und
$$r*s=\frac{m}{n} * \frac{k}{l}=\frac{m*k}{n*l}$$

Weiters wird auch die #Subtraktion und #Division für zwei rationale Zahlen definiert.

$$
r-s=r+(-s)
$$
und
$$
r:s=\frac{r}{s}=r*\frac{1}{s}, (s \not=0)
$$
So wie die natürlichen und ganzen Zahlen geordnet sind, so sind auch die rationalen Zahlen geordnet. Die Zahlengerade veranschaulicht wie rationale Zahlen geordnet sind.

```tikz 
\usepackage{amsmath}
\usetikzlibrary{arrows}
\begin{document}
\begin{tikzpicture}[scale=1]

\draw[latex-latex] (-8,0) -- (8,0) ;
\foreach \x in  {-8,-7,-6,-5,-4,-3,-2,-1,0,1,2,3,4,5,6,7,8}
\draw[shift={(\x,0)},color=black] (0pt,3pt) -- (0pt,-3pt);
\foreach \x in {-6,-5,-4,-3,-2,-1,0,1,2,3,4,5,6}
\draw[shift={(\x,0)},color=black] (0pt,0pt) -- (0pt,-3pt) node[below] 
{$\x$};
\end{tikzpicture}
\end{document}
```

```tikz 
\usepackage{amsmath}
\usetikzlibrary{arrows}
\begin{document}
\begin{tikzpicture}[scale=2]
\draw[latex-latex] (0.5,0) -- (4.5,0) ;
\foreach \x in  {0,1/2,1,3/2,2}
\draw[shift={(\x+2,0)},color=black] (0pt,3pt) -- (0pt,-3pt);
\foreach \x in {0,1/2,1,3/2,2}
\draw[shift={(\x+2,0)},color=black] (0pt,0pt) -- (0pt,-3pt) node[below] 
{$\x$};
\draw[->,thick] (2.4,1) -- (2,0.15); 
\draw[->,thick] (3.6,1) -- (4,0.15); 
\end{tikzpicture}
\end{document}
```

Für zwei rationale Zahlen $r=\frac{m}{n}, s=\frac{k}{l}$ wird definiert
$$
r=\frac{m}{n}<s=\frac{k}{l} \iff m*k<n*k
$$
Eine weitere Beobachtung ist die Existenz einer weiteren rationalen Zahlen zwischen zwei beliebigen rationalen Zahlen
$$
r< \frac{r+s}{2} < s
$$
So könnte man auf die Aussage schließen, dass die rationalen Zahlen auf der Zahlengerade lückenlos sind. Dies ist jedoch bei genauerer Betrachtung falsch.

Beispielsweise lässt sich folgende Gleichung im Rahmen der rationalen Zahlen nicht lösen.
$$
x^2=2
$$
Die Lösung dieser Gleichung wäre die irrationale Wurzel aus 2
$$
x=\sqrt{ 2 }
$$
Der Beweis dafür sieht wie folgt aus:
Man nimmt an es existiert eine Lösung für x in den rationalen Zahlen

$\Q:={\frac{m}{n}:m\in \Z, n \in \N \\{0} }$

$\Z={\dots,-2,-1,0,1,2,\dots}$ 

$r=\frac{m}{n}, s=\frac{k}{l},r<s pfeil ml<nk$
$r<s \implies r<\frac{(r+s)}{2}<s$

$\Q$ liegt dicht auf der Zahlengerade. Es existieren unendlich rationale Zahlen zwischen zwei beliebigen rationalen Zahlen.

Satz: $x^2=2$ ist unlösbar in $\Q$
Beweis: Ann $\E x = \frac{a}{b}\in\Q:x^2=2,~ggT(a,b)=1,~b\in\N\\{0},a\in\Z$
$x^2=\frac{a^2}{b^2}=2 \implies a^2 =2*b^2 \implies a^2 gerade \implies a gerade$
$\implies \Ec\in\Z: a=2c \implies a^2=2b^2 \pfeil 4c^2=2b^2 \pfeil 2c^2=b^2$
$\implies b~gerade \blitz$