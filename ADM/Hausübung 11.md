## 527) 
Sei $f : \mathbb{R}^{2} → \mathbb{R}^{2}$ die lineare Abbildung mit $f\left(\begin{matrix} 0 \\ 1\end{matrix}\right)=f\left(\begin{matrix}3 \\ 2\end{matrix}\right) =\left(\begin{matrix}1 \\-1\end{matrix}\right)$. Bestimmen
Sie $ker(f )$ und $f (\mathbb{R}^{2})$ sowie $dim(ker(f ))$ und den Rang von $f$. Verifizieren Sie die Beziehung
$dim(ker(f )) + rg(f ) = dim \mathbb{R}^{2}$ und bestimmen Sie die Matrix von $f$ bezüglich der kanonischen
Basis.

$$
ker(f) =
$$
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
Unlösbar
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
