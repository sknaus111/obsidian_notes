## Aufgabe 1 (7 Punkte)
Beweisen Sie $\sum_{k=1}^{n} \frac{1}{2^{k}}=2-\frac{k+2}{2k}$ mittels vollständiger Induktion für alle $n ∈ N, n ≥ 1$

#Induktionsvoraussetzung
$$
\sum_{k=1}^{n} \frac{1}{2^{k}}=2- \frac{n+2}{2n}
$$

#Induktionsanfang
$$
\frac{1}{2} = 2- \frac{3}{2}
$$
$$
\frac{1}{2}=\frac{1}{2}
$$
#Induktionsbehauptung
$$
\sum_{k=1}^{n+1} \frac{1}{2^{k}}=2- \frac{(n+1)+2}{2(n+1)}
$$
#Induktionsschritt
$$
\sum ^{n+1} =  2- \frac{n+2}{2n} + \frac{1}{2^{n+1}}
$$
$$
= 2- (\frac{n+2}{2n} - \frac{1}{2*2^{n}})
$$
$$
= 2- \left( \frac{(n+2)2^{n}}{2*n*2^{n}} - \frac{n}{n*2*2^{n}}\right)
$$
$$
2- \left(\frac{2^{n}*n+2*2^{n}-n}{2*n*2^{n}}\right)
$$
$$
2- \left( \frac{2^{n}*n*(n+1)+2*2^{n}*(n+1)-n(n+1)}{2*n*2^{n}*(n+1)} \right)
$$
$$
2- \left(\frac{2^{n}*n*n+2^{n}*n+2*2^{n}*n+2*2^{n}-n*n-n}{2*n*2^{n}*(n+1)}\right)
$$
$$
2- \left(2^{n}*n^{2}+2^{n}n+2*2^{n}*n+2*2^{n}-n^{2}-n\right)
$$
$$
2 - (2^{n})(n)()
$$
$$
2 - (2^{n}*n^{2}-n^{2}+3*2^{n}n+2*2^{n}-n)
$$

## Aufgabe 2 (6 Punkte)
Es seien $z_{1} = 2 − 2i$ und $z_{2} = \left[ 4; \frac{3π}{2}  \right]$ komplexe Zahlen. Berechnen Sie Folgende Aufgaben und geben Sie das Ergebnis in kartesicher Form an.

- $z_{1} + z_{2}$

$$
a_{2} = 4*\cos \frac{3\pi}{2} 
$$
$$
b_{2} = 4* \sin \frac{3\pi}{2}
$$
$$
a_{2} = 4 * 0
$$
$$
b_{2} = 4 * -1
$$
$$
2+0  - i * (2+4)
$$
$$
z_{1}+z_{2}=2 - 6i
$$
- $\frac{z_{1}}{z_{2}}$

$$
\frac{z_{1}}{z_{2}} = \frac{z_{1}*z_{2}}{r_{2}} = 2*0- (-2*-4) + i (2*-4 + 0*-2)
$$
$$
 = -8 - i8 = 2 - i2
$$
- $z_{1}^{6}$

$$
z_{1}^2 * z_{1}^{2}*z_{1}^{2} = 2^{2} - 2i^{2} = 4 - (4*-1) = 8^{3} =512
$$
## Aufgabe 3 (7 Punkte)
Es sei $R ⊆ \mathbb{N} × \mathbb{N}$ eine Relation gegeben durch $aRb ⇔ "a$ und $b$ haben eine Ziffer gemeinsam” (z.B.: 12 und 23)

• Untersuchen Sie die Relation auf Reflexivität, Antisymmetrie und Transitivität

Reflexivität
$$
\forall a \in \mathbb{N}: aRa
$$
$$
\exists z \in \{ 0,1,\dots,9 \} \in a \implies z \exists \in a
$$
Antisymmetrie
$$
\forall a,b \in \mathbb{N} : aRb \land bRa \implies a=b
$$
$$
11R 21 \land 21R 11 \implies 11 = 21
$$
WIDERSPRUCH

Transitivität
$$
\forall a,b,c \in \mathbb{N}: aRb \land bRc \implies aRc
$$
$$
12 R 23 \land 23 R 34 \implies 12 R 34
$$
WIDERSPRUCH

• Ist die Relation eine Halbordnung

Nein da sie nicht antisymmetrisch und nicht transitiv ist.

