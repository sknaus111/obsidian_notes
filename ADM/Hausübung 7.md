## 327
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
1. $$
l(x)=0 \text{ und } l(b)=l(e)=l(c)=l(f)=l(d)=l(g)=l(y) = \infty, U= \{ x \} ,u=x
$$
2. $$
l(b) = min\{ \infty,0+4 \}=4, p(b)=x;l(e)=min\{ \infty,0+7 \}=7,p(e)=x
$$
3. $$
m=4, z=b, U = \{ x,b \}, u=b
$$
2. $$
l(e)=min\{ 7,4+2 \}=6, p(e)=b; l(c) = min\{ \infty,4+7 \}=11,p(c)=b
$$
3. $$
m=6, z=e, U = \{ x,b,e \}, u=e
$$
2. $$
l(c) = min\{ 4+7,4+2+5 \}=11, p(c)=b; l(f)=min\{ \infty, 4+2+3 \}=9, p(f)=c
$$
3. $$
m=9, z=f, U=\{ x,b,e,f \}, u=f
$$
2. $$
l(c) =min\{ 4+7, 4+3+2+1\}=10,p(c)=f; l(g)=min\{ \infty, 4+2+3+5\}=14, p(g)=f
$$
3. $$
m=11, z=c, U=\{ x,b,e,f,c \},u=c
$$
2. $$
l(d) = min\{ \infty,4+3+2+1+4\}=14,p(d)=c;l(g) = min\{ 4+2+3+5, 4+3+2+1+2\}=12, p(g)=c
$$
3. $$
m=12, z=g, U = \{ x,b,e,f,c,g \}, u=g
$$
2. $$
l(y)=min\{ \infty, 4+3+2+1+2+1\}=14, p(y)=g
$$
3. $$
m=14, z=y,U=\{ x,b,e,f,c,g,y \}, u=y
$$

$$
p(y)=g, p(g)=c,=p(c)=f,p(f)=e,p(e)=b,p(b)=x
$$

|     |  x  |    b     |    c     |    d     |    e     |    f     |    g     |    y     |
| :-: | :-: | :------: | :------: | :------: | :------: | :------: | :------: | :------: |
|  0  | *0* | $\infty$ | $\infty$ | $\infty$ | $\infty$ | $\infty$ | $\infty$ | $\infty$ |
|  1  |     |  *4/x*   | $\infty$ | $\infty$ |   7/x    | $\infty$ | $\infty$ | $\infty$ |
|  2  |     |          |   11/b   | $\infty$ |  *6/b*   | $\infty$ | $\infty$ | $\infty$ |
|  3  |     |          |   11/e   | $\infty$ |          |  *9/e*   | $\infty$ | $\infty$ |
|  4  |     |          |  *10/f*  | $\infty$ |          |          |   14/f   | $\infty$ |
|  5  |     |          |          |   14/c   |          |          |  *12/c*  | $\infty$ |
|  6  |     |          |          |   13/g   |          |          |          |  *13/g*  |
## 354) 
Untersuchen Sie, ob die Menge M mit der Operation ◦ ein Gruppoid, eine Halbgruppe,
ein Monoid bzw. eine Gruppe ist:
$$M = \mathbb{Q} \setminus \{1\}, a ◦ b = a + b − ab$$
### Abgeschlossenheit

$$
a+b-ab=1
$$
$$
a-ab=1-b
$$
$$
a(1-b)=1(1-b)
$$
$$
a=1
$$
Da dies vorhinein ausgeschlossen ist, ist die Gruppe Abgeschlossen
### Assoziativ

$$
(a \circ b) \circ c = a\circ(b \circ c)
$$
$$
(a \circ b) = (a+b-ab)
$$
$$
(b \circ c) = (b+c-bc)
$$
$$
(a+b-ab) + c - (a+b-ab)c = a+(b+c-bc)-a(b+c-bc)
$$
$$
a+b-ab+c-ca-cb+cab=a+b+c-bc-ab-ac+abc
$$
$$
-ab -ac -bc +abc = -bc -ab -ac +abc
$$

### Neutrales Element

$$
(a \circ e) = a
$$
$$
(a \circ e)=(a+e-ae)=a
$$
$$
a+0-a0=a
$$
### Inverse Elemente

$$
(a\circ a')=e=0
$$
$$
a+a'-aa'=0
$$
$$
a'(1-a)=-a
$$
$$
a'=\frac{a}{(1-a)}
$$
Handelt sich um eine Gruppe  
## 368
Beweisen Sie, dass in einer Gruppe $(G, ·)$ die folgenden Rechenregeln für alle $a, b, c ∈ G$
gelten:

- (a) $a · b = a · c ⇒ b = c$
- (b) $(a^{-1})^{-1} = a$
- (c) $(ab)^{-1} = b^{-1} · a^{-1}$
- (d) Die Gleichung $a · x = b$ ist in G immer eindeutig lösbar

### a
$$
a*b=a*c
$$
$$
b=e*b = (a*a')*b=a'*(a*b)=a'*(a*c)=(a'*a)*c=e*c=c
$$
### b

$$
(a')' = a
$$
$$
e = (a*a')
$$
$$
e = (a'*(a')')
$$
$$
a=a*e=a*(a'*(a')')=(a*a')*(a')'=e*(a')'=(a')'
$$
### c

$$
ab' = b' * a'
$$
$$
ab'=(a*b)'=e*(a*b)'=(b'*b)*(a*b)'=b'*e*b*(a*b)'='b*('a*a)*b*(a*b)'=
$$
$$
(b'*a')*((a*b)*(a*b)')=b'*a'*e=b'*a'
$$
### d

$$
a*x=b
$$
$$
x = x*e = x*(a*a') = (x*a)*a'=b*a'
$$

## 375) 
Sei $U$ die von $(2)(13)$ erzeugte Untergruppe der $S_{3}$. Man bestimme die Linksnebenklassen
von $U$. Ist $U$ Normalteiler von $S_{3}$?

## Präsenzaufgabe
Gruppe $S_{4}$ mit $e$ als neutrales Element. Finden $a,b,c \in S_{k}$, sodass $U=\{ e,a,b,c \}$ vierelementige Untergruppe von $S_{4}$ ist, sodass:
$(i) a^{2}=b^{2}=c^{2}=e$
$(ii)x \circ y=z$ für alle paare verschiedener
$x,y,z \in U\setminus\{ e \}$

$U=\{e, (1~2)(3~4),(1~3),(2~4),(1~4)(2~3) \}$
