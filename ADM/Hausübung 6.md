![[Pasted image 20241113160509.png]]
## 280) 
Man bestimme alle Quadrupel $(a, b, c, d), a, b, c, d ∈ \{1, 2, . . . , 7\}$, sodass der von den Knoten
$a, b, c, d$ in $G_{1}$ aufgespannte Teilgraph zu $G_{2}$ ismorph ist.

garantiert:
$(5,1,2,7)$


falsch aufgrund zu vieler Kanten
$(4,1,7,2)$
$(6, 1, 2, 7)$
$(1,2,3,4)$

## 292) 
Gegeben sei der ungerichtete schlichte Graph $G = 〈V, E〉$ mit $V = \{a, b, c, d, e\}$ und $E =\{ab, ac, ae, bc, bd, ce\}$. Man veranschauliche $G$ graphisch, bestimme seine Adjazenzmatrix sowie alle Knotengrade und zeige, dass die Anzahl der Knoten, die einen ungeraden Knotengrad besitzen, gerade ist. Gilt diese Aussage in jedem ungerichteten Graphen?




```tikz 
\begin{document} \begin{tikzpicture}

% Knoten 
\node (a) at (0, 2) {a}; \node (b) at (-2, 0) {b}; \node (e) at (2, 0) {e}; \node (d) at (-2, -2) {d}; \node (c) at (2, -2) {c}; % Kanten 
\draw (a) -- (b); \draw (a) -- (c); \draw (a) -- (e); \draw (b) -- (c); \draw (b) -- (d); \draw (c) -- (e);

\end{tikzpicture} 
\end{document}
```

 $$\begin{array}{ccc} 0 & 1 & 1 & 0 & 1\\ 1 & 0 & 1 & 1 & 0 \\ 1 & 1 & 0 & 0 & 1 \\ 0 & 1 & 0 & 0 & 0 \\ 1 & 0 & 1 & 0 & 0 \\ \end{array}\
 $$
 $$
d(a) = 3, d(b)= 3, d(c)=3, d(d)=1, d(e)=2
$$

 Da es sich um einen ungerichteten schlichten Graphen handelt ist die Adjazentmatrix entlang der Diagonalen symmetrisch. Somit ist die Anzahl der Knotengrade die eine Hälfte der Matrix * 2. Somit ist die Anzahl der ungeraden Knotengrade gerade.
 
Ja dies gilt allgemein da jeder schlichter ungerichteter Graph entlang der Diagonalen symmetrisch ist.