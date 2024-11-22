## Aufgabe 1: 
Sei $a_{1} = 2, a_{2} = 8$ und $a_{i} = 14a_{i-1} − 20a_{i-2}$, für alle $i ≥ 3$. Man zeige durch vollständige Induktion, dass $a_n$ durch $2^{n}$ teilbar ist, für alle $n ≥ 1$.

#Induktionsvoraussetzung
$$
a_{i} = 14a_{i-1} - 20a_{i-2}, ~~a_{1}=2,a_{2}=8
$$
#Induktionsanfang
$$
a_{3}=14*8-20*2
$$
$$
a_{3} = 112 - 40 = 72 
$$
$$
72 = 8 * p ~~~~p\in \mathbb{Z}
$$
$$
72 = 8 * 9
$$
#Induktionsbehauptung
$$
a_{n+1}=14a_{n}-20a_{n-1} = 2^{n+1} *p ~~~~~p\in \mathbb{Z}
$$

#Induktionsschritt
$$
a_{n+1} = 2*2^{n}*p ~~~~~~p\in \mathbb{Z}
$$
$$
14a_{n-1}-20a_{n-2} = 
$$
## Aufgabe 2: 
Bestimmen Sie alle Lösungen der folgenden Kongruenzen bzw. beweisen Sie die Unlösbarkeit
(in $\mathbb{Z}$)

### a) 
$$5x ≡ 10 \mod 15$$
$$
ggT(15,5)=5, 5| 10
$$
$$
x \equiv 2 \mod 3
$$
$$
x=2+3*p
$$
### b) 
$$10x ≡ 5 \mod 13$$
$$
ggT(10,13)=1
$$
$$
13 = 10 * 1 +3
$$
$$
10 = 3*3 +1
$$
$$
1= 10-3*3
$$
$$
1 = 10 - (13-10*1)*3
$$
$$
1 = 4*10-13*3
$$
$$
4*10x\equiv5*10 \mod 13
$$
$$
x \equiv 11 \mod 13
$$
$$
x = 11 + p * 13
$$
## Aufgabe 3:

### a) 
Seien A, B, C Mengen. Beweisen Sie, dass
$A ∩ (B \backslash C) = (A ∩ B) \backslash C$

| A   | B   | C   | $B\backslash C$ | $A\cap BC$ | $A \cap B$ | $A \cap B \backslash C$ |
| --- | --- | --- | --------------- | ---------- | ---------- | ----------------------- |
| 0   | 0   | 0   | 0               | 0          | 0          | 0                       |
| 0   | 0   | 1   | 0               | 0          | 0          | 0                       |
| 0   | 1   | 0   | 1               | 0          | 0          | 0                       |
| 0   | 1   | 1   | 0               | 0          | 0          | 0                       |
| 1   | 0   | 0   | 0               | 0          | 0          | 0                       |
| 1   | 0   | 1   | 0               | 0          | 0          | 0                       |
| 1   | 1   | 0   | 1               | 1          | 1          | 1                       |
| 1   | 1   | 1   | 0               | 0          | 1          | 0                       |
 ### b) 
Man zeige, dass es sich bei dem logischen Ausdruck
$((A ∨ B) ∧ (A → C) ∧ (B → C)) → C$
um eine Tautologie handelt.
