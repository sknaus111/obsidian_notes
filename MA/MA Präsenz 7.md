## Aufgabe 1. 
Zeigen Sie die Gleichung
$$2(n^{2} − 1)(n + 2) = (n − 1)(2n + 4)(n + 1)$$ 
durch ...

- a) ... Ausrechnen beider Seiten.
- b) ... eine Gleichungskette.

### a
$$
2(n^{2}-1)(n+2)=(n-1)(2n+4)(n+1)
$$
$$
2(n^{3}+2n^{2}-n-2)=(2n^{2}+4n-2n-4)(n+1)
$$
$$
2n^{3}+4n^{2}-2n-4=2n^{3}+4n^{2}-2n^{2}-4n+2n^{2}+4n-2n-4
$$
$$
2n^{3}+4n^{2}-2n-4=2n^{2}+4n^{2}-2n-4
$$
### b
$$
2(n^{2}-1)(n+2)=(n^{2}-1)(2n+4)=(n-1)(2n+4)(n+1)
$$

## Aufgabe 2. 

Die Gleichung $4x −3 = 4x −4$ ist für $x ∈ \mathbb{R}$ unlösbar wie Subtraktion von $4x$ sofort zeigt.
Die folgende Gleichungsumformung scheint trotzdem die Lösung $x = − \frac{1}{2}$ zu bestimmen. Wieso tut sie das nicht? Was zeigt sie?

$$4x − 3 = 4x − 4$$
$$\iff x + 1 = x$$
$$\implies (x + 1)^{2} = x^{2}~~~~~~~|\cdot(x+1) \text{ und } \cdot x$$
$$ \iff x^{2} + 2x + 1 = x^{2}$$
$$\iff 2x = −1$$
$$\iff x = − \frac{1}{2}$$
Hinweis: Ergänzen Sie die Implikationspfeile (⇒, ⇐, oder ⇔) in dieser Umformung.

## Aufgabe 3. 
Wir haben Funktionen $f , g$ sowie ein Objekt $a$ mit

$$g (f (x), y ) = f (g (y , x))$$
$$g (a, x) = x$$
Zeigen Sie dass $g (f (a), f (f (a))) = f (f (f (a)))$. Kennzeichnen Sie bei jedem Schritt $x$ und $y$ .
$$
g(f(a),f(f(a))) = f(g(f(f(a)),a)) ~~~y=f(f(a)), x=a
$$
$$
f(g(f(f(a)),a)) = f(f(g(a,f(a)))) ~~y=a,x=f(a)
$$
$$
f(f(g(a,f(a)))) = f(f(f(a))) ~~~a=a, x=f(a)
$$
