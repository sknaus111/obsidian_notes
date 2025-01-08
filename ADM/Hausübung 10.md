## 470
Untersuchen Sie, ob $W$ Teilraum des Vektorraums $\mathbb{R}^{3}$ über $\mathbb{R}$ ist, und beschreiben Sie
die Menge $W$ geometrisch.

$$W = \{(x, y, z) | x = −z\}$$
### Ungleich der leeren Menge
Vektoren beispiel
$$
\left(\begin{matrix}
1  \\
0 \\
-1
\end{matrix}\right)
$$
### Abgeschlossen bezüglich $W+W$
$$
\forall a,b\in W
$$
$$
\left(\begin{matrix}
a \\
0 \\
-a
\end{matrix}\right)+\left(\begin{matrix}
b \\
0 \\
-b
\end{matrix}\right)
=\left(\begin{matrix}
a+b \\
0 \\
-(a+b)
\end{matrix}\right)
$$
### Abgeschlossen bezüglich $\lambda \cdot W$
$$
\forall a\in W\forall \lambda\in \mathbb{R}
$$
$$
\left(\begin{matrix}
a \\
0 \\
-a
\end{matrix}\right) \cdot \lambda
= \left(\begin{matrix}
\lambda a \\
0 \\
-(\lambda a)
\end{matrix}\right)
$$
Bei $W$ handelt es sich um eine um 45° Grad liegende Ebene bezüglich der $y$-Achse 

## 494 
Untersuchen Sie, ob $B = \{(0, 7, 4), (−2, 4, −5), (6, 2, −1)\}$ eine Basis des $\mathbb{R}^{3}$ ist

### Lineare Unabhängigkeit
$$
\lambda_{1} \cdot \left(\begin{matrix}
0 \\
7 \\
4
\end{matrix}\right)+
\lambda_{2}\cdot \left(\begin{matrix}
-2 \\
4 \\
-5
\end{matrix}\right)+\lambda_{3}\cdot \left(\begin{matrix}
6 \\
2 \\
-1
\end{matrix}\right)
= \left(\begin{matrix}
0 \\
0 \\
0
\end{matrix}\right)
$$
$$
\lambda_{1}0+\lambda_{2}(-2)+\lambda_{3}6=0
$$
$$
\lambda_{1}7+\lambda_{2}4+\lambda_{3}2=0
$$
$$
\lambda_{1}4+\lambda_{2}(-5)+\lambda_{3}(-1)=0
$$

$$
\lambda_{1}0+\lambda_{2}(-2)+\lambda_{3}6=0\implies \lambda_{2}2=\lambda_{3}6 \implies \lambda_{2}=\lambda_{3}3
$$
$$
7\lambda_{1}+12\lambda_{3}+2\lambda_{3}=0 \implies 14\lambda_{3}=-7\lambda_{1} \implies 2\lambda_{3}=-1\lambda_{1}
$$
$$
4 \lambda_{1}+ (-5) \lambda_{2} + (-1)\lambda_{3}=0 \implies 4 \lambda_{1}+ (-15)\lambda_{3} + (-1 )\lambda_{3}=0\implies 4 \lambda_{1}+ 7 \frac{1}{2}\lambda_{1} + \frac{1}{2}\lambda_{1} = 12\lambda_{1}=0
$$
$$
\lambda_{1}=0, -0=2\lambda_{3} \implies \lambda_{3}=0, 0\cdot_{3}=\lambda_{2}\implies \lambda_{2}=0
$$

### lineare Hülle
Da $B$ drei Vektoren hat und $\mathbb{R}^{3}$ der dritten Dimension entspricht, spannt die lineare Hülle der Basis sich über den gesamten Vektorraum $\mathbb{R}^{3}$ auf.

## 497) 
Zeigen Sie, dass die Vektoren $x_{1}, x_{2}, x_{3}$ eines Vektorraumes genau dann linear unabhängig
sind, wenn $x_{1} − x_{2}, x_{2}, x_{2} − x_{3}$ linear unabhängig sind

$$
\lambda_{1}\vec{x_{1}}+\lambda_{2}\vec{x_{2}}+\lambda_{3}\vec{x_{3}}=\vec{0}
$$
$$
\mu_{1}\cdot(\vec{x_{1}}-\vec{x_{2}})+\mu_{2}\vec{x_{2}}+\mu_{3}\cdot(\vec{x_{2}}-\vec{x_{3}})=\vec{0}
$$
$$
\mu_{1}x_{1}-\mu_{1}x_{2}+\mu_{2}x_{2}+\mu_{3}x_{2}-\mu_{3}x_{3}=0
$$
$$
\mu_{1}x_{1}+x_{2}\cdot(-\mu_{1}+\mu_{2}+\mu_{3})-\mu_{3}x_{3}=0
$$
$$
\lambda_{1}=\mu_{1}, \lambda_{2}=-\mu_{1}+\mu_{2}+\mu_{3}, \lambda_{3}=-\mu_{3}
$$
$$
\mu_{1}=\lambda_{1}, \mu_{2}=\lambda_{1}+\lambda_{2}+\lambda_{3}, \mu_{3}=-\lambda_{3}
$$

Einfach umrechenbar, deswegen wenn das eine linear unabhängig ist, dann auch das andere.

## 558
Bestimmen Sie den Rang der folgenden reellen Matrizen

$$
\left(\begin{matrix}
1  & -2  & 3  & -4  & 5  \\
-2  & 3  &  -4  & 5  & -6 \\
3  & -4  & 5   & -6  &  7 \\
-4  & 5  & -6  & 7  & -8 
\end{matrix}\right)
$$
Ersetzen $a_{2}$ durch $a_{2}+2a_{1}$, $a_{3}$ durch $a_{3}-3a_{1}$, $a_{4}$ durch $a_{4}+4a_{1}$ und $a_{5}$ durch $a_{5}-5a_{1}$
$$
\left(\begin{matrix}
1  & 0  & 0  & 0  & 0  \\
-2  & -1  &  2  & -3  & 4 \\
3  & 2  & -4   & 6  &  -8 \\
-4  & -3  & 6  & -9  & 12 
\end{matrix}\right)
$$
Ersetzen $a_{3}'$ durch $a_{3}'+2a_{2}'$, $a_{4}'$ durch $a_{4}'-3a_{2}'$ und $a_{5}'$ durch $a_{5}'+4a_{2}'$
$$
\left(\begin{matrix}
1  & 0  & 0  & 0  & 0  \\
-2  & -1  &  0  & 0  & 0 \\
3  & 2  & 0   & 0  &  0 \\
-4  & -3  & 0  & 0  & 0
\end{matrix}\right)
$$
Zwei linear unabhängige Spalten also Rang 2

## Präsenzaufgabe
Seien $v_{1},v_{2},v_{3}, w \in V$
zu zeigen ist: $[\{ v_{1},v_{2},v_{3},w \}] = [\{ v_{1},v_{2},v_{3} \}] \iff$ $w$ kann als Linearkombination von $v_{1},v_{2},v_{3}$ dargestellt werden. 