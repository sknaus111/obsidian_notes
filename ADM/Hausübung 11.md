$$
f(x)+f(y)=f(x+y)
$$
## 527) 
Sei $f : \mathbb{R}^{2} → \mathbb{R}^{2}$ die lineare Abbildung mit $f\left(\begin{matrix} 0 \\ 1\end{matrix}\right)=f\left(\begin{matrix}3 \\ 2\end{matrix}\right) =\left(\begin{matrix}1 \\-1\end{matrix}\right)$. Bestimmen
Sie $ker(f )$ und $f (\mathbb{R}^{2})$ sowie $dim(ker(f ))$ und den Rang von $f$. Verifizieren Sie die Beziehung
$dim(ker(f )) + rg(f ) = dim \mathbb{R}^{2}$ und bestimmen Sie die Matrix von $f$ bezüglich der kanonischen
Basis.



$$
f\left(\begin{matrix}
0 & 3 | 1 & 1 \\
1 & 2 | -1 & -1
\end{matrix}\right)
$$
$$
f\left(\begin{matrix}
3  & 0|1 & 1 \\ 
2 & 1|-1 & -1
\end{matrix}\right)
$$
$s_{1}=s_{1}-2s_{2}$
$$
f\left(\begin{matrix}
3  & 0|-1 & 1 \\ 
0 & 1|1 & -1
\end{matrix}\right)
$$
$s_{1}=\frac{s_{1}}{3}$

$$
\left(\begin{matrix}
1  & 0|-\frac{1}{3} & 1 \\ 
0 & 1|\frac{1}{3} & -1
\end{matrix}\right)
$$

$$
F(x) = \left(\begin{matrix}
-\frac{1}{3} & 1 \\
\frac{1}{3} & -1
\end{matrix}\right)
\left(\begin{matrix}
x_{1} \\
x_{2}
\end{matrix}\right)
=\left(\begin{matrix}
-\frac{1}{3}x_{1} + x_{2} \\
\frac{1}{3}x_{1}-x_{2}
\end{matrix}\right)
=x'
$$
ker
$$
\left(\begin{matrix}
-\frac{1}{3} + 1 \\
\frac{1}{3}-1
\end{matrix}\right)\left(\begin{matrix}
3 \\
1
\end{matrix}\right)=
0
$$
dim ker
1

rang von f
1

dim ker f + rg f = dim R
$$
\left(\begin{matrix}
1 \\
0
\end{matrix}\right)
\left(\begin{matrix}
0 \\
1
\end{matrix}\right)
$$
$$
dim(r) = 2
$$
1+1=2






## 550)
Bestimmen Sie mit dem Gaußschen Eliminationsverfahren die Lösung des Gleichungssystems über dem Körper $K$:

### a)
$K = \mathbb{Q}$
$2x_{1} + 5x_{2} − 2x_{3} = 5$
$3x_{1} + x_{3} = 4$
$− x_{2} + 2x_{3} = 1$

$$
\left(\begin{matrix}
2 & 5 & -2| & 5 \\
3 & 0 & 1 | & 4 \\
0 & -1 & 2 | & 1
\end{matrix}\right)
$$

$z_{2}=2z_{2}-3z_{1}$

$$
\left(\begin{matrix}
2 & 5 & -2| & 5 \\
0 & -15 & 8 | & -7 \\
0 & -1 & 2 | & 1
\end{matrix}\right)
$$
$z_{3}=15z_{3}-z_{2}$
$$
\left(\begin{matrix}
2 & 5 & -2| & 5 \\
0 & -15 & 8 | & -7 \\
0 & 0 & 22 | & 22
\end{matrix}\right)
$$
$$
x_{3}=1
$$
$$
-15x_{2}+8=-7
$$
$$
-15x_{2}=-15
$$
$$
x_{2}=1
$$
$$
2x_{1}+5-2=5
$$
$$
x_{1}=1
$$

### b
wie a aber
$K=\mathbb{Z}_{11}$


$$
\left(\begin{matrix}
2 & 5 & 9| & 5 \\
3 & 0 & 1 | & 4 \\
0 & 10 & 2 | & 1
\end{matrix}\right)
$$
$z_{2}=2z_{2}-3z_{1}$

$$
\left(\begin{matrix}
2 & 5 & 9| & 5 \\
0 & 7 & 8 | & 4 \\
0 & 10 & 2 | & 1
\end{matrix}\right)
$$
$z_{3}=7z_{3}-10z_{2}$
$$
\left(\begin{matrix}
2 & 5 & 9| & 5 \\
0 & 7 & 8 | & 4 \\
0 & 0 & 0 | & 0
\end{matrix}\right)
$$
$$
z_{2}=8z_{2}
$$
$$
\left(\begin{matrix}
2 & 5 & 9| & 5 \\
0 & 1 & 9 | & 10 \\
0 & 0 & 0 | & 0
\end{matrix}\right)
$$
$z_{1}=6z_{1}$
$$
\left(\begin{matrix}
1 & 8 & 10| & 8 \\
0 & 1 & 9 | & 10 \\
0 & 0 & 0 | & 0
\end{matrix}\right)
$$
$$
x_{1}+8x_{2}+10x_{3}=8
$$
$$
x_{2}+9x_{3}=10
$$
$$
x_{2}=10-9t_{1}
$$
$$
x_{1}=8-10t_{1}-(10-9t_{1})
$$
$$
x_{1}=-2-t_{1}
$$
