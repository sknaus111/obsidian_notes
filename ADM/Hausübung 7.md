# 327
Bestimmen Sie mit dem Algorithmus von Dijkstra einen kürzesten Weg zwischen den Knoten
$x$ und $y$ im folgenden Graphen:

```tikz
\begin{document} \begin{tikzpicture}

% Knoten 
\node (x) at (-4, 0) {x}; 
\node (b) at (-2, 1) {b}; 
\node (e) at (-2, -1) {e}; 
\node (c) at (0, 1) {c}; 
\node (f) at (0, -1) {f}; % Kanten 
\node (d) at (2, 1) {d};
\node (g) at (2, -1) {g};
\node (y) at (4,0) {y};

\draw (x) -- (b);
\node at (-3.2, 0.8) {4};
\draw (x) -- (e);
\node at (-3.2, -0.8) {7};
\draw (b) -- (c);
\node at (-1, 1.2) {7};
\draw (b) -- (e);
\node at (-1.8, 0) {2};
\draw (e) -- (c);
\node at (-0.8, -0.1) {5};
\draw (e) -- (f);
\node at (-1, -1.2) {3};
\draw (c) -- (d);
\node at (1, 1.2) {4};
\draw (c) -- (g);
\node at (0.2,0) {1};
\draw (c) -- (f);
\node at (1.2,0.2) {2};
\draw (f) -- (g);
\node at (1, -1.2) {5};
\draw (d) -- (y);
\node at (3.2, 0.8) {3};
\draw (d) -- (g);
\node at (2.2,0) {1};
\draw (g) -- (y);
\node at (3.2, -0.8) {1};

\end{tikzpicture} 
\end{document}
```
