Zwei Objekte $a,b$ einer Menge stehen miteinander in einer #Relation. Diese kann, aber muss nicht, Reihenfolgen relevant sein.
Um den **Relationsbegriff** zu fassen benötigt man den Begriff des #geordneten_Paars von Elementen und des #kartesischen_Produkts von Mengen

## Geordnetes Paar
Ein geordnetes Paar zweier Elemente $(a,b)$, welche nicht zwangsweise verschieden sein müssen, fasst diese mit relevanter Reihenfolge in ein neues Element zusammen.

## Kartesisches Produkt
Das kartesische Produkt zweier Mengen $A \times B$ ist die Menge aller geordneten Paare $(a,b), a\in A,b\in B$
$$
A\times B=\{(a,b)|a\in A\land b\in B\}
$$
Allgemein kann das Produkt endlich vieler Mengen wie folgt definiert werden.
$$
A_{1}\times A_{2}\times\dots\times A_{n}=\{(a_{1},a_{2},\dots,a_{n})|a_{1} \in A_{1}, a_{2} \in A_{2},\dots,a_{n}\in A_{n}\}
$$
Sind alle Mengen, welche multipliziert werden, gleich so kann auch $A^n$ geschrieben werden.

Kartesisch lässt sich das ganze ebenfalls darstellen.

```tikz
\begin{document}
\begin{tikzpicture}
% Draw the coordinate axes 
\draw[->] (-1,0) -- (5,0) node[right] {$x$}; % x-axis 
\draw[->] (0,-1) -- (0,3) node[above] {$y$}; % y-axis % Draw the circle with 

\foreach \x in  {1,2,3}
\draw[shift={(\x,0)},color=black] (0pt,3pt) -- (0pt,-3pt);
\foreach \x in {1,2,3}
\draw[shift={(\x,0)},color=black] (0pt,0pt) -- (0pt,-3pt) node[below] {$\x$};

\foreach \x in  {1,2}
\draw[shift={(0,\x)},color=black] (3pt,0pt) -- (-3pt,0pt);
\foreach \x in {2,4}
\draw[shift={(0,\x/2)},color=black] (0pt,0pt) -- (-3pt,0pt) node[left] {$\x$};


\foreach \x in {1,2,3}
\node at (\x,1)[circle,fill,inner sep=1pt]{};

\foreach \x in {1,2,3}
\node at (\x,2)[circle,fill,inner sep=1pt]{};

\draw[help lines] (-1,-1) grid (5,3);

\end{tikzpicture}
\end{document}
```
## Relation
Eine #Relation $R$ zwischen zwei Mengen $A$ und $B$ ist eine Teilmenge des kartesischen Produktes $A\times B$. Ist $A=B$ spricht man von einer #binären_Relation auf $A$.
Anstelle von $(a,b) \in R$ schreibt man $aRb$
Anstelle von $(a,b) \not \in R$ schreibt man $a\not Rb$

Auch können Relationen auf verschiedene Weisen graphisch ausgedrückt werden.

### Kartesische Darstellung

In der kartesischen Darstellung werden nur jene Punkte markiert, die der Relation $R\subseteq A\times B$ angehören.

```tikz
\begin{document}
\begin{tikzpicture}
% Draw the coordinate axes 
\draw[->] (-1,0) -- (5,0) node[right] {$x$}; % x-axis 
\draw[->] (0,-1) -- (0,3) node[above] {$y$}; % y-axis % Draw the circle with 

\foreach \x in  {1,2,3}
\draw[shift={(\x,0)},color=black] (0pt,3pt) -- (0pt,-3pt);
\foreach \x in {1,2,3}
\draw[shift={(\x,0)},color=black] (0pt,0pt) -- (0pt,-3pt) node[below] {$\x$};

\foreach \x in  {1,2}
\draw[shift={(0,\x)},color=black] (3pt,0pt) -- (-3pt,0pt);
\foreach \x in {2,4}
\draw[shift={(0,\x/2)},color=black] (0pt,0pt) -- (-3pt,0pt) node[left] {$\x$};


\foreach \x in {2}
\node at (\x,1)[circle,fill,inner sep=1pt]{};

\foreach \x in {2,3}
\node at (\x,2)[circle,fill,inner sep=1pt]{};

\draw[help lines] (-1,-1) grid (5,3);

\end{tikzpicture}
\end{document}
```

### Pfeildiagramm

Die Mengen werden durch Venndiagramme dargestellt und die Paare mit Pfeilen verbunden.

```tikz
\begin{document}
\begin{tikzpicture}

% Draw ovals 
\draw[thick] (0,0) ellipse (2cm and 4cm);
\node at (-2,4) {A};
\draw[thick] (5,0) ellipse (2cm and 4cm);
\node at (6.5,4) {B};

% Draw dots in oval A 
\filldraw (0, 1) circle (2pt) node[above right] {1}; 
\filldraw (0, 0) circle (2pt) node[below right] {2}; 
\filldraw (0, -1) circle (2pt) node[below right] {3}; 

% Draw dots in oval B 
\filldraw (5, 1) circle (2pt) node[above right] {2}; 
\filldraw (5, -1) circle (2pt) node[below right] {4};

% Draw arrows 
\draw[->] (0,0) -- (4.9,0.95); % From 2 in A to 2 in B 
\draw[->] (0,0) -- (4.9,-0.9); % From 3 in A to 4 in B 
\draw[->] (0,-1) -- (4.85,-1); % From 3 in A to 4 in B

\end{tikzpicture}
\end{document}
```

### Graph einer binären Relation
Da in einer binären Relation $A=B$,  $A\times A=A^{2}$ nur eine Menge dargestellt werden muss. Der Graph $G(R)$ besteht aus #Knoten, der Elemente und **gerichteten** #Kanten, ihrer Verbindungen.

```tikz
\begin{document}
\begin{tikzpicture}

% Draw ovals 
\draw[->,thick] (0,0) arc [start angle=340, end angle=685, radius=0.5];
\draw[->,thick] (5,0) arc [start angle=260, end angle=605, radius=0.5];
\draw[->,thick] (0,-5) arc [start angle=80, end angle=425, radius=0.5];


% Draw dots in oval A 
\filldraw (0, 0) circle (2pt) node[above right] {2}; 
\filldraw (5, 0) circle (2pt) node[below right] {3}; 
\filldraw (0, -5) circle (2pt) node[below right] {1}; 

% Draw arrows 
\draw[->] (0,0) -- (4.7,0); % From 2 in A to 2 in B 
\draw[->] (0,-5) -- (4.8,-0.1); % From 3 in A to 4 in B 
\draw[->] (0,-5) -- (0,-0.2); % From 3 in A to 4 in B

\end{tikzpicture}
\end{document}
```
In solchen Graphen können auch #Schlingen auftreten. Dies sind Kanten, welche wieder auf sich selbst zeigen $aRa$.