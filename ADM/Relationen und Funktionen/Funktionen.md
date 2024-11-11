Generell ist eine Funktion zwischen zwei Mengen ein Spezialfall einer Relation.

Seien $A,B$ zwei nichtleere Mengen. Eine #Funktion oder **Abbildung** $f: A \rightarrow B$ von $A$ nach $B$ ist ein Tripel $(A,B,R_{f})$ , wobei $R_{f}\subseteq A\times B$ eine Relation ist mit der Eigenschaft, dass zu jedem $a\in A$ genau ein $b\in B$ mit $aR_{f}b$ existiert. Man schreibt dafür $b=f(a)$. Die Menge $R_{f} = \{(a,f(a)|a\in A)\} \subseteq A\times B$ bezeichnet man als #Graph der Funktion $f:A\rightarrow B$.

```tikz
\begin{document}
\begin{tikzpicture}

% Draw ovals 
\draw[thick] (0,0) ellipse (1.5cm and 2.5cm);
\node at (-1.5,2.5) {A};
\draw[thick] (5,0) ellipse (1.5cm and 2.5cm);
\node at (6.5,2.5) {B};

% Draw dots in oval A 
\filldraw (0, 1) circle (2pt); 
\filldraw (0, 0) circle (2pt); 
\filldraw (0, -1) circle (2pt); 

% Draw dots in oval B 
\filldraw (5, 1) circle (2pt); 
\filldraw (5, -1) circle (2pt);

% Draw arrows 
\draw[->] (0,1) -- (4.9,0.95); % From 2 in A to 2 in B 
\draw[->] (0,0) -- (4.9,-0.9); % From 3 in A to 4 in B 
\draw[->] (0,-1) -- (4.85,-1); % From 3 in A to 4 in B

\node at (2.3,1.3) {f};

\end{tikzpicture}
\end{document}
```

Man verwendet auch $f:A\rightarrow B, a\rightarrow f(a)$. Diese Notation zeigt dass eine Funktion auch eine Zuordnung ist. Einem $a\in A$ wird eindeutig ein $b=f(a)\in B$ zugeordnet.

## Injektive Funktion
Eine Funktion $f:A\rightarrow B$ heißt #injektiv oder #Injektion, wenn es zu jedem $b\in B$ **höchstens** ein $a\in A$ mit $b=f(a)\in B$ gibt. Verschiedene $a$ implizieren verschiedene Werte für der Funktion.

```tikz
\begin{document}
\begin{tikzpicture}

% Draw ovals 
\draw[thick] (0,0) ellipse (1.5cm and 2.5cm);
\node at (-1.5,2.5) {A};
\draw[thick] (5,0) ellipse (1.5cm and 2.5cm);
\node at (6.5,2.5) {B};

% Draw dots in oval A 
\filldraw (0, 1) circle (2pt); 
\filldraw (0, 0) circle (2pt); 
\filldraw (0, -1) circle (2pt); 

% Draw dots in oval B 
\filldraw (5, 1) circle (2pt); 
\filldraw (5, 0.3) circle (2pt);
\filldraw (5, -0.3) circle (2pt);
\filldraw (5, -1) circle (2pt);

% Draw arrows 
\draw[->] (0,1) -- (4.9,-0.95); % From 2 in A to 2 in B 
\draw[->] (0,0) -- (4.9,0.25); % From 3 in A to 4 in B 
\draw[->] (0,-1) -- (4.9,-0.35); % From 3 in A to 4 in B

\node at (2.3,1.3) {f};

\end{tikzpicture}
\end{document}
```
## Surjektive Funktion
Eine Funktion $f: A\rightarrow B$ heißt #surjektiv oder #Surjketion, wenn es jedem $b\in B$ **mindestens** ein $a\in A$ mit $b=f(a)\in B$ gibt.

```tikz
\begin{document}
\begin{tikzpicture}

% Draw ovals 
\draw[thick] (0,0) ellipse (1.5cm and 2.5cm);
\node at (-1.5,2.5) {A};
\draw[thick] (5,0) ellipse (1.5cm and 2.5cm);
\node at (6.5,2.5) {B};

% Draw dots in oval A 
\filldraw (0, 1) circle (2pt); 
\filldraw (0, 0) circle (2pt); 
\filldraw (0, -1) circle (2pt); 

% Draw dots in oval B 
\filldraw (5, 0.6) circle (2pt); 
\filldraw (5, -0.6) circle (2pt);

% Draw arrows 
\draw[->] (0,1) -- (4.9,-0.55); % From 2 in A to 2 in B 
\draw[->] (0,0) -- (4.9,0.55); % From 3 in A to 4 in B 
\draw[->] (0,-1) -- (4.9,-0.65); % From 3 in A to 4 in B

\node at (2.3,1.3) {f};

\end{tikzpicture}
\end{document}
```
## Bijektive Funktion
Eine Funktion $f: A\rightarrow B$ heißt #bijektiv oder #Bijektion, wenn es zu jedem $b\in B$ **genau ein** $a\in A$ mit $b=f(a)\in B$ gibt

```tikz
\begin{document}
\begin{tikzpicture}

% Draw ovals 
\draw[thick] (0,0) ellipse (1.5cm and 2.5cm);
\node at (-1.5,2.5) {A};
\draw[thick] (5,0) ellipse (1.5cm and 2.5cm);
\node at (6.5,2.5) {B};

% Draw dots in oval A 
\filldraw (0, 1) circle (2pt); 
\filldraw (0, 0) circle (2pt); 
\filldraw (0, -1) circle (2pt); 

% Draw dots in oval B 
\filldraw (5, 1) circle (2pt); 
\filldraw (5, 0) circle (2pt);
\filldraw (5, -1) circle (2pt);


% Draw arrows 
\draw[->] (0,1) -- (4.9,0.05); % From 2 in A to 2 in B 
\draw[->] (0,0) -- (4.9,0.95); % From 3 in A to 4 in B 
\draw[->] (0,-1) -- (4.9,-1); % From 3 in A to 4 in B

\node at (2.3,1.3) {f};

\end{tikzpicture}
\end{document}
```
Eine Funktion ist bijektiv, wenn sie surjektiv und injektiv ist.

## Funktionen gleicher Elemente
Haben zwei endliche Mengen $A,B$ gleich viele Elemente, $|A|=|B|$. Dann ist eine injektive/surjektive Funktion auch bijektiv und surjektiv/injektiv.

### Beweis
Sei $f: A\rightarrow B$ injektiv und $|A|=|B|=n$. Schreibt man $A=\{a_{1},a_{2},\dots a_{n}\}$ und setzt $b_{j}=f(a_{j})~~~1\leq j\leq n$ dann sind die Elemente $b_{1},b_{2},\dots,b_{n}$ eine Teilmenge $\{b_{1},b_{2},\dots b_{n}\}$ von $B$ aufgrund der Injektivität. Da diese Teilmenge $=B$  ist, folgt dass $f(A)=B$ gilt. Damit ist $f$ auch surjektiv.

## Zusammensetzungen von Funktionen
Sind $f:A\rightarrow B$ und $g:C\rightarrow D$ Funktionen, so wird die Zusammensetzung $g \circ  f:A\rightarrow C$ durch $(g\circ f)(a)=g(f(a))$ definiert. $g\circ f$ ist dann wieder eine Funktion

Sind $f:A\rightarrow C$ und $g:C\rightarrow D$ injektiv, so ist auch $g\circ f:A\rightarrow C$ injektiv/surjektiv/bijektiv.

### Beweis
Seien $g$ und $f$ injektiv. Daraus folgt, dass $f(a_{1})=f(a_{2})\implies a_{1}=a_{2}$ und $g(b_{1})=g(b_{2})\implies b_{1}=b_{2}$. Ist $(g\circ f)(a_{1})=g(f(a_{1}))=g(f(a_{2}))=(g\circ f)(a_{2})$, dann folgt aus der Injektivität der Funktion $g$ , dass $f(a_{1})=f(a_{2})$ und aus der Injektivität von $f$ folgt $a_{1}=a_{2}$ Somit ist auch $g\circ f$ injektiv.

Sind $f$ und $g$ surjektiv so gibt es ein $c\in C$ mit $b\in B$ in $g(b)=c$ und damit auch eine $a\in A$ mit $f(a)=b$. Insgesamt gilt $(g\circ f)(a)=g(f(a))=g(b)=c$

Sind $g$ und $f$ bijektiv, so folgt der Beweis aus den oberen beiden.

## Inverse Funktion
Eine Funktion $f^{-1}:B\rightarrow A$ heißt die zu der Funktion $f:A\rightarrow B$ #inverse_Funktion oder #Umkehrfunktion , wenn $f^{-1}\circ f=id_{a}$ und $f\circ f^{-1}=id_{b}$ gilt. Dabei bezeichnet $id_{a}$ die #identische_Funktion auf einer Menge $A$, d.h. $id_{a}=a$ für alle $a\in A$

Eine Funktion $f:A\rightarrow B$ besitzt genau dann eine inverse Funktion $f^{-1}:B\rightarrow A$, wenn $f$ bijektiv ist. Die inverse Funktion $f^{-1}$ ist dann auch bijektiv

### Beweis
Sei $g:B\rightarrow A$ die inverse Funktion von $f:A\rightarrow B$, $g=f^{-1}$. Aus der Beziehung $(f\circ g)(b)=f(g(b))=b$ folgt dass zu jedem $b\in B$ ein $a\in A$  $a=g(b)$ gibt mit der Eigenschaft $f(a)=b$. Folglich ist $f$ surjektiv. Sind $a_{1}a_{2}\in A$ mit $f(a_{1})=f(a_{2})$ so folgt $a_{1}=g(f(a_{1}))=g(f(a_{2}))=a_{2}$. Somit ist $f$ auch injektiv und daher auch bijektiv.
Da aus der Surjektivität folgt, dass es zu jedem $b\in B$ ein $a\in A$ mit $f(a)=b$ gibt. Aufgrund der Injektivität gibt es aber kein $a'\in A$ mit $f(a')=b$. Wir können daher eine Funktion $g:B\rightarrow A$ definieren, die jedem $b\in B$ genau ein $a\in A$ mit $f(a)=b$ zuordnet. Offensichtlich erfüllt die Funktion die Eigenschaft $g(f(a))=a$ und $f(g(b))=b$. Daher ist $g$ die inverse Funktion von $f$.