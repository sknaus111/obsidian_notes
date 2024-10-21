#Natürliche_Zahlen beschreiben eine #Menge an Zahlen, wie man sie in der Volksschule das erste Mal kennengelernt hat 0, 1, 2, 3, …. Ebenfalls besitzt jede natürliche Zahl n einen Nachfolger $n' = n+1$.  
$$
0 \xrightarrow{} 1 \xrightarrow{} 2 \xrightarrow{} 3 \xrightarrow{} 4
$$
Streng genommen können die natürlichen Zahlen durch die #Peanoaxiome charakterisiert werden.

1. 0 (Null) ist eine natürliche Zahl
2. Jede natürliche Zahl n hat genau einen Nachfolger
3. 0 ist nicht Nachfolger einer natürlichen Zahl
4. Verschiedene natürliche Zahlen besitzen verschiedene Nachfolger
5. Jede Eigenschaft, welche 0 zukommt und sich von jeder natürlichen Zahl auf den Nachfolger überträgt, kommt bereits allen natürlichen Zahlen zu #Induktionsaxiom #Induktion 

#Axiom 

Aufgrund der #Peanoaxiome ist eine andere Struktur der natürlichen Zahlen nicht möglich.

```tikz 
\begin{document} \begin{tikzpicture}
\node at (-6,0) {};
\node at (-0.5,0.2) {0}; % 
\draw[->,thick] (-0.5,0) arc [start angle=210, end angle=510, radius=0.5];
\node[anchor=east] at (10.5,0.2) {unmöglich wegen 3.};
\end{tikzpicture} 
\end{document}
```

```tikz 
\begin{document} \begin{tikzpicture} 
\node at (0,0) {0}; 
\draw[->,thick] (0.5,0) -- (1.5,0); 
\node at (2,0) {1}; 
\draw[->,thick] (2.5,0) -- (3.5,0); 
\node at (4,0) {2}; 
\draw[->,thick] (4.5,0) -- (5.5,0); 
\node at (6,0) {...}; 
\draw[->,thick] (6.5,0) -- (7.5,0); 
\node at (8,0) {n};
\draw[->,thick] (8.5,0) -- (9.5,0.75); 
\node at (10,1) {n`}; 
\draw[->,thick] (8.5,0) -- (9.5,-0.75); 
\node at (10,-1) {n`}; 
\node[anchor=east] at (16.5,0.2) {unmöglich wegen 2.};
\end{tikzpicture} 
\end{document} 
```
```tikz 
\begin{document} \begin{tikzpicture} 
\node at (1,0) {0}; 
\draw[->,thick] (1.5,0) -- (2.15,0); 
\node at (2.75,0) {1}; 
\draw[->,thick] (3.25,0) -- (4,0); 
\node at (4.5,0) {...}; 
\draw[->,thick] (5,0) -- (5.75,0); 
\node at (6.25,0) {n}; 
\draw[->,thick] (6.75,0) -- (7.5,0); 
\node at (8,0) {n`};
\draw[->,thick] (8.5,-0.1) -- (9.5,-0.75); 
\node at (10,-1) {n``}; 
\draw[->,thick] (10.5,-1) -- (11.5,-1); 
\node at (12,-1) {n```}; 
\draw[->,thick] (12.5,-0.75) -- (13.5,-0.1); 
\node at (14,0) {n````}; 
\draw[->,thick] (13.5,0.1) -- (12.5,0.75);
\node at (11,1) {.....}; 
\draw[->,thick] (9.5,0.75) -- (8.5,0.1);
\node[anchor=east] at (17.5,0.2) {unmöglich wegen 4.};
\end{tikzpicture} 
\end{document} 
```
```tikz 
\begin{document} \begin{tikzpicture} 
\node at (0,0) {0}; 
\draw[->,thick] (0.5,0) -- (1.5,0); 
\node at (2,0) {1}; 
\draw[->,thick] (2.5,0) -- (3.5,0); 
\node at (4,0) {...}; 
\draw[->,thick] (4.5,0) -- (5.5,0); 
\node at (6,0) {n}; 
\draw[->,thick] (6.5,0) -- (7.5,-0.75); 
\node at (8,-1) {n`=m`};
\draw[->,thick] (7.5,-1.25) -- (6.5,-2); 
\node at (6,-2) {m}; 
\node at (15,-1) {unmöglich wegen 4.};
\end{tikzpicture} 
\end{document} 
```
```tikz 
\begin{document} \begin{tikzpicture} 
\node at (0,0) {0}; 
\draw[->,thick] (0.5,0) -- (1.5,0); 
\node at (2,0) {1}; 
\draw[->,thick] (2.5,0) -- (3.5,0); 
\node at (4,0) {...}; 
\node at (0,-1.5) {a}; 
\draw[->,thick] (0.5,-1.5) -- (1.5,-1.5); 
\node at (2,-1.5) {a`}; 
\draw[->,thick] (2.5,-1.5) -- (3.5,-1.5); 
\node at (4,-1.5) {...}; 
\node at (6, -0.75) {oder};
\node at (8,0) {0}; 
\draw[->,thick] (8.5,0) -- (9.5,0); 
\node at (10,0) {1}; 
\draw[->,thick] (10.5,0) -- (11.5,0); 
\node at (12,0) {...}; 
\node at (9.2,-1.5) {b};
\draw[->,thick] (9.4,-1.5) -- (10.6,-1.5);
\node at (10.8,-1.5) {b`};
\draw[->,thick] (10.6,-1.40) -- (10.2,-1.1);
\node at (10,-1) {b``};
\draw[->,thick] (9.8,-1.1) -- (9.4,-1.4);
\node at (15,-0.7) {unmöglich wegen 5.};
\end{tikzpicture} 
\end{document} 
```

Aus den natürlichen Zahlen ergibt sich eine natürliche #Ordnung bilden, in welcher folgende Fälle auftreten können. In der folgenden Tabelle seien m und n natürliche Zahl, m wird im Sachverhalt immer als erstes angegeben und das Verhältnis zu n wird beschrieben.

$$
\begin{array}{|c|c|} \hline m~kleiner~als~n & m<n  \\ \hline m~gleich~groß~wie~n & m=n \\ \hline m~größer~als~n & m>n \\ \hline m~größer~oder~gleich~groß~wie~n & m\geq n \\ \hline m~kleiner~oder~gleich~groß~wie~n & m\leq n\\ \hline \end{array}
$$


Das interessanteste #Axiom stellt sich herbei als das 5te da. Aus diesem lässt sich nämlich die [[vollständige Induktion]] ableiten.
