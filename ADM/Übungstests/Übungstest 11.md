## Aufgabe 1: (8 Punkte)
Man beweise mittels vollständiger Induktion für alle $n ∈ \mathbb{N}$:
$$
\sum_{k=1}^{n}k(k+1)2^{k}=2^{n+1}(n^{2}-n+2)-4
$$
Dabei müssen alle Elemente eines Induktionsbeweises angeführt und die kennengelernten
Bezeichnungen angegeben werden.

#Induktionsvoraussetzung
$$
\sum_{k=1}^{n}k(k+1)2^{k}=2^{n+1}(n^{2}-n+2)-4
$$
#Induktionsanfang
$$
(1+1)2^{1}=2^{2}(1^{2}-1+2)-4
$$
$$
4 = 4(2)-4
$$
$$
4 = 4
$$
#Induktionsbehauptung
$$
\sum_{k=1}^{n+1}k(k+1)2^{k}=2^{n+2}((n+1)^{2}-(n+1)+2)-4
$$
$$
= 2^{n+2}(n^{2}+2n+1-n-1+2) -4
$$
$$
= 2^{n+2} ( n^{2}+n+2)
$$
#Induktionsschritt
$$
= 2^{n+1}(n^{2}-n+2)-4 + (n+1)(n+2)2^{n+1}
$$
$$
= 2^{n+1}(n^{2}-n+2)+2^{n+1}(n+1)(n+2)-4
$$
$$
= 2^{n+1}n^{2}-2^{n+1}n + 2^{n+1}2 + 2^{n+1}(n^{2}+3n+2) -4
$$
$$
= 2^{n+1}n^{2}-2^{n+1}n + 2^{n+1}2 + 2^{n+1}n^{2}+2^{n+1}3n+2^{n+1}2 -4
$$
$$
= 2^{n+1}n^{2}*2 + 2^{n+1}2n + 2*2^{n+1}2 -4
$$
$$
= 2^{n+2}n^{2}+2^{n+2}n+2*2^{n+2} -4
$$
$$
= 2^{n+2}(n^{2}+n+2)-4
$$

## Aufgabe 2: (6 Punkte)
Bestimmen Sie $(1 − i)^{10}$ und stellen Sie das Ergebnis in der Gauß’schen Zahlenebene dar.
$$
(1-i)^{2^{5}}
$$
$$
r = 2^{10/2} = 32, arg = \arctan -\frac{1}{1} =  \frac{7\pi}{4} *10 = \frac{70\pi}{4} \mod 2\pi = \frac{6\pi}{4}
$$
## Aufgabe 3: (6 Punkte)
Bestimmen Sie die Lösungen der folgenden Kongruenzen bzw. beweisen Sie die Unlösbarkeit in $\mathbb{Z}$:
### (a) (3 Punkte) 
$$4x ≡ 5 \mod 11.$$
$$
ggT(4,11)=1, 1|5
$$
$$
11 = 4 * 2 +3
$$
$$
4 = 3 * 1 +1
$$
$$
1 = 4 - 3*1
$$
$$
1 = 4 - (11-4*2)*1
$$
$$
1 = 4*3-11 * 1
$$
$$
4x*3 \equiv 5*3 \mod 11
$$
$$
x \equiv 4 \mod 11
$$
$$
x = 4 + p * 11
$$
### (b) (3 Punkte) 
$$4x ≡ 5 \mod 12.$$

$$
ggT(12,4)=4, 4 ~\not|5
$$
