## Eigenschaften der Binomialkoeffizienten
Die Binomialkoeffizienten erfüllen folgende Eigenschaften
- (i) $$\binom{n}{0}=\binom{n}{n}=1$$
- (ii) $$
\binom{n}{k}=\binom{n}{n-k}
$$
- (iii)$$
\binom{n+1}{k+1}=\binom{n}{k}+\binom{n}{k+1}
$$
### Beweis der Eigenschaften
Für die erste und zweite Eigenschaft folgt der Beweis unmittelbar aus der Definition.
Der Beweis der dritten Eigenschaft ist dieser
$$
\binom{n}{k}+\binom{n}{k+1}=\frac{n!}{k!(n-k)!}+\frac{n!}{(k+1)!(n-k-1)!}
$$
$$
=\frac{n!}{k!(n-k-1)!}* \left ( \frac{1}{n-k}+\frac{1}{k+1}\right )
$$
$$
=\frac{n!}{k!(n-k-1)!}*\frac{n+1}{(n-k)*(k+1)}
$$
$$
=\frac{(n+1)!}{(k+1)!(n-k)!}
$$$$
=\binom{n+1}{k+1}
$$
## Pascalschen Dreieck
Auch besteht ein enger Zusammenhang zwischen den Binomialkoeffizienten und dem Pascalschen Dreieck.

|         | $k=0$ | $k=1$ | $k=2$ | $k=3$ | $k=4$ | $k=5$ | $\dots$ |
| ------- | ----- | ----- | ----- | ----- | ----- | ----- | ------- |
| $n=0$   | $1$   |       |       |       |       |       |         |
| $n=1$   | $1$   | $1$   |       |       |       |       |         |
| $n=2$   | $1$   | $2$   | $1$   |       |       |       |         |
| $n=3$   | $1$   | $3$   | $3$   | $1$   |       |       |         |
| $n=4$   | $1$   | $4$   | $6$   | $4$   | $1$   |       |         |
| $n=5$   | $1$   | $5$   | $10$  | $10$  | $5$   | $1$   |         |
| $\dots$ |       |       |       |       |       |       |         |

Auch erfüllen die Binomialkoeffizienten andere Eigenschaften wie 
$$
\sum_{k=0}^{n}\binom{n}{k}=2^n
$$
## Binomischer Lehrsatz
$$
\sum_{k=0}^{n}\binom{n}{k}x^{n-k}y^{k}=(x+y)^{n}
$$
### Beweis des binomischen Lehrsatz
Dieser Satz kann nun mittels [[vollständige Induktion]] bewiesen werden. Der Induktionsanfang mit einem $n=0$ ist offensichtlich wahr. Man nehme an es sei für ein $n$ richtig so folgt mittels der [[#Eigenschaften der Binomialkoeffizienten]] folgendes
$$
(x+y)^{n+1}=(x+y)^{n}(x+y)
$$$$
=\sum_{k=0}^{n}\binom{n}{k}x^{n-k}y^{k}(x+y)
$$
$$
=\sum_{k=0}^{n}\binom{n}{k}x^{n-k+1}y^{k}+\sum_{k=0}^{n}\binom{n}{k}x^{n-k}y^{k+1}
$$
$$
=\sum_{k=0}^{n+1}\binom{n}{k}x^{n-k+1}y^{k}+\sum_{k=0}^{n+1}\binom{n}{k-1}x^{n-k+1}y^{k}
$$
$$
=\sum_{k=0}^{n+1}\left ( \binom{n}{k}+\binom{n}{k-1}\right)x^{n+1-k}y^{k}
$$
$$
=\sum_{k=0}^{n+1}\binom{n+1}{k}x^{n+1-k}y^{k}
$$
