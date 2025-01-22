## 568)
Bestimmen Sie die inverse Matrix $A^{-1}$

$$
A=\left(\begin{matrix}
-1 & -2 & 2 &| &1 & 0 & 0 \\ 
-1  & -3 & 2 & | & 0 & 1 & 0\\
 2 & 4 & 6 & | & 0 & 0 & 1
\end{matrix}\right)
$$
$$
(z_{2}=z_{2}-z_{1})\left(\begin{matrix}
-1 & -2 & 2 &| &1 & 0 & 0 \\ 
0  & -1 & 0 & | & -1 & 1 & 0\\
 2 & 4 & 6 & | & 0 & 0 & 1
\end{matrix}\right)
$$
$$
(z_{1}=z_{1}*-1)\left(\begin{matrix}
1 & 2 & -2 &| &-1 & 0 & 0 \\ 
0  & -1 & 0 & | & -1 & 1 & 0\\
 2 & 4 & 6 & | & 0 & 0 & 1
\end{matrix}\right)
$$
$$
(z_{1}=z_{1}*2)\left(\begin{matrix}
2 & 4 & -4 &| &-2 & 0 & 0 \\ 
0  & -1 & 0 & | & -1 & 1 & 0\\
 2 & 4 & 6 & | & 0 & 0 & 1
\end{matrix}\right)
$$
$$
(z_{3}=z_{3}-z_{1})\left(\begin{matrix}
2 & 4 & -4 &| &-2 & 0 & 0 \\ 
0  & -1 & 0 & | & -1 & 1 & 0\\
 0 & 0 & 10 & | & 2 & 0 & 1
\end{matrix}\right)
$$
$$
\left( z_{1}=\frac{z_{1}}{2} \right)\left(\begin{matrix}
1 & 2 & -2 &| &-1 & 0 & 0 \\ 
0  & -1 & 0 & | & -1 & 1 & 0\\
 0 & 0 & 10 & | & 2 & 0 & 1
\end{matrix}\right)
$$
$$
\left( z_{2}=z_{2}*-1 \right)\left(\begin{matrix}
1 & 2 & -2 &| &-1 & 0 & 0 \\ 
0  & 1 & 0 & | & 1 & -1 & 0\\
 0 & 0 & 10 & | & 2 & 0 & 1
\end{matrix}\right)
$$
$$
\left( z_{2}=z_{2}*2 \right)\left(\begin{matrix}
1 & 2 & -2 &| &-1 & 0 & 0 \\ 
0  & 2 & 0 & | & 2 & -2 & 0\\
 0 & 0 & 10 & | & 2 & 0 & 1
\end{matrix}\right)
$$
$$
\left( z_{1}=z_{1}-z_{2} \right)\left(\begin{matrix}
1 & 0 & -2 &| &-3 & 2 & 0 \\ 
0  & 2 & 0 & | & 2 & -2 & 0\\
 0 & 0 & 10 & | & 2 & 0 & 1
\end{matrix}\right)
$$
$$
\left( z_{2}= \frac{z_{2}}{2} \right)\left(\begin{matrix}
1 & 0 & -2 &| &-3 & 2 & 0 \\ 
0  & 1 & 0 & | & 1 & -1 & 0\\
 0 & 0 & 10 & | & 2 & 0 & 1
\end{matrix}\right)
$$
$$
\left( z_{3}= \frac{z_{3}}{10} \right)\left(\begin{matrix}
1 & 0 & -2 &| &-3 & 2 & 0 \\ 
0  & 1 & 0 & | & 1 & -1 & 0\\
 0 & 0 & 1 & | & \frac{2}{10} & 0 & \frac{1}{10}
\end{matrix}\right)
$$
$$
\left( z_{1}= z_{1}+2z_{3} \right)\left(\begin{matrix}
1 & 0 & 0 &| &-3+\frac{4}{10} & 2 & \frac{2}{10} \\ 
0  & 1 & 0 & | & 1 & -1 & 0\\
 0 & 0 & 1 & | & \frac{2}{10} & 0 & \frac{1}{10}
\end{matrix}\right)
$$


## 576)
Man berechne

$$
\left|\begin{matrix}
1 & 2 & 3 & 4 \\
2 & 3 & 4 & 5 \\
3 & 4 & 5 & 6 \\
4 & 5 & 6 & 7
\end{matrix}\right|
$$
$$
(z_{1}=z_{1}+z_{2})
\left|\begin{matrix}
3 & 5 & 7 & 9 \\
2 & 3 & 4 & 5 \\
3 & 4 & 5 & 6 \\
4 & 5 & 6 & 7
\end{matrix}\right|
$$
$$
z_{1}=z_{1}-z_{4}
\left|\begin{matrix}
-1 & 0 & 1 & 2 \\
2 & 3 & 4 & 5 \\
3 & 4 & 5 & 6 \\
4 & 5 & 6 & 7
\end{matrix}\right|
$$
$$
s_{3}=s_{3}+s_{1}
\left|\begin{matrix}
-1 & 0 & 0 & 2 \\
2 & 3 & 6 & 5 \\
3 & 4 & 8 & 6 \\
4 & 5 & 10 & 7
\end{matrix}\right|
$$
$$
s_{4}=s_{4}+2s_{1}
\left|\begin{matrix}
-1 & 0 & 0 & 0 \\
2 & 3 & 6 & 9 \\
3 & 4 & 8 & 12 \\
4 & 5 & 10 & 15
\end{matrix}\right|
$$
$$
s_{3}=s_{3}-2s_{2}
\left|\begin{matrix}
-1 & 0 & 0 & 0 \\
2 & 3 & 0 & 9 \\
3 & 4 & 0 & 12 \\
4 & 5 & 0 & 15
\end{matrix}\right|
$$
$$
s_{4}=s_{4}-3s_{2}
\left|\begin{matrix}
-1 & 0 & 0 & 0 \\
2 & 3 & 0 & 0 \\
3 & 4 & 0 & 0 \\
4 & 5 & 0 & 0
\end{matrix}\right|
$$
$$
-1\cdot 3 \cdot 0 \cdot 0 = 0
$$
## 593)
Man bestimme die Eigenwerte der Matrix A sowie zu jedem Eigenwert alle Eigenvektoren

$$
A=\left(\begin{matrix}
6 & 4 & 4 \\
-6 & -5 & -8 \\
3  & 4  & 7
\end{matrix}\right)
$$
$$
\left(\begin{matrix}
\lambda  & 0 & 0 \\
0 & \lambda & 0 \\
0 & 0 & \lambda
\end{matrix}\right)-
\left(\begin{matrix}
6 & 4 & 4 \\
-6 & -5 & -8 \\
3  & 4  & 7
\end{matrix}\right)=
\left(\begin{matrix}
\lambda-6 & -4 & -4 \\
6 & \lambda+5 & 8 \\
-3 & -4 & \lambda-7
\end{matrix}\right)
$$
$$
(\lambda-6)\cdot \left|\begin{matrix}
\lambda+5 & 8 \\
-4 & \lambda-7
\end{matrix}\right|
$$
$$
4 \cdot \left|\begin{matrix}
6 & 8 \\
-3 & \lambda-7)
\end{matrix}\right|
$$
$$
-4 \cdot \left|\begin{matrix}
6 & \lambda+5 \\
-3 & -4
\end{matrix}\right|
$$
$$
(\lambda-6)((\lambda+5)(\lambda-7)-8\cdot-4) = (\lambda-6)(\lambda^{2}-2\lambda-3)=\lambda^{3}-2\lambda^{2}-3\lambda-6\lambda^{2}+12\lambda+18
$$
$$
=\lambda^{3}-8\lambda^{2} +9\lambda+18
$$
$$
4\cdot(6\cdot (\lambda-7)+8\cdot3) = 4 \cdot(6\lambda-18)=24\lambda-72
$$
$$
-4 \cdot (6 \cdot -4 + 3 \cdot(\lambda+5))=-4\cdot(-24+3\lambda+15)=-4\cdot(-9+3\lambda)=36-12\lambda
$$
$$
=\lambda^{3}-8\lambda^{2}+21\lambda -18
$$

