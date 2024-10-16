## 3)

Man zeige durch [[vollständige Induktion ]]dass $7^n − 1$ für alle $n \in \mathbb{N}$ durch 6 teilbar ist.

Die #Induktionsvoraussetzung ist 

$$\frac{7^n-1 }{6}\in\mathbb{N}$$

Zuerst #Induktionsanfang beweisen.

$$\frac{7^0-1 }{6} \in\mathbb{N}$$

Danach Induktionsschritt
$$\frac{7^{n+1}-1}{6}\in\mathbb{N}$$
$$=\frac{7*7^n-1}{6}$$
$$= \frac{6*7^n+7^n-1}{6}$$
$$=7^n+\frac{7^n-1}{6} \in\mathbb{N}$$

Linker Term vom plus mit 6 multipliziert, also durch 6 wieder teilbar. Rechter Term in der Voraussetzung als durch 6 teilbar definiert.

## 4) 
$$\sum_{j=2}^{n}j(j-1)=\frac{(n-1)n(n+1)}{3}, (n\geq2)$$
Induktionsanfang

$$
\sum_{j=2}^{2}j(j-1) = \frac{(2-1)2(2+1)}{3}
$$
$$
2(2-1) = \frac{(2-1)2(2+1)}{3}
$$
$$
2=\frac{2*3}{3}
$$
$$
2=2
$$
Induktionsbehauptung

$$
\sum_{j=2}^{n+1}j(j-1) = \frac{((n+1)-1)(n+1)((n+1)+1)}{3}
$$
$$
\sum_{j=2}^{n+1}j(j-1) = \frac{n*(n+1)*(n+2)}{3}
$$
Induktionsschritt
$$
\sum_{j=2}^{n+1}j(j-1)=\sum_{j=2}^{n}j(j-1)+(n+1)((n+1)-1)
$$
$$
\sum_{j=2}^{n+1}j(j-1)=\frac{(n-1)n(n+1)}{3}+(n+1)((n+1)-1)
$$
$$
\sum_{j=2}^{n+1}j(j-1)=\frac{(n-1)n(n+1)}{3}+(n+1)n
$$
$$
\frac{(n-1)n(n+1)+3*(n+1)n}{3}
$$
$$
\frac{n*((n-1)(n+1)+3*(n+1))}{3}
$$
$$
\frac{(n+1)*n*((n-1)+3)}{3}
$$
$$
\frac{(n+1)*n*(n+2)}{3}
$$
## 15)
Man zeige mittels vollständiger Induktion, dass für die rekursiv definierte Folge $x_{0} = 1$ und $x_{k+1}= x_{k} + 18k + 15$ für $k \geq 0$ allgemein gilt: $x_{n} = (3n + 1)^2$ für alle n ≥ 0.

Induktionsanfang
$x_{0}=(3*0+1)^2, x_{0} =1$
$1 = (0+1)^2$
$1=1$

Induktionsbehauptung
$x_{n+1}=(3(n+1)+1)^2$
$(3n+3+1)$
$(3n+4)^2$

Induktionsschritt
$x_{n+1}=x_{n}+18n+15$
$(3n+4)^2 = x_{n}+18n+15$
 = (3n + 1)^2+18n+15$
$=15+18n+9n^2+6n+1$
$=16+24n+9n^2$
$=9n^2+24n+16$
$=3^2n^2+2*4*3*n+4^2$
$(3n+4)^2=(3n+4)^2$


## 24) 
Wo steckt der Fehler im Induktions-”Beweis“ der folgenden Behauptung:

Je zwei natürliche Zahlen a, b sind gleich groß.
Beweis: Vollständige Induktion nach dem $max\{a, b\}$.

a) $max\{a, b\} = 0$: Hier gilt $a = b = 0$.
b) Die Behauptung gelte für $max\{a, b\} = n$.

Sei nun $max\{a, b\} = n + 1$. Dann ist $max\{a − 1, b − 1\} = n$, und es folgt aus der  Induktionsvoraussetzung b), dass $a − 1 = b − 1$ ist, womit aber auch $a = b$ gilt

Max kann nicht eines Beweises verwendet werden.

Setzt man für a und b 0 ein würde die Gleichung $max\{a-1,b-1\}=-1$ ergeben. Dies liegt außerhalb der natürlichen Zahlen $\mathbb{N}$ und somit liegt kein gültiger Beweis vor.