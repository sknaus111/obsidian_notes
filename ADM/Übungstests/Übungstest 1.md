## 1.1 Aufgabe 1
Beweisen Sie mittels vollständiger Induktion für alle $n ≥ 1, n ∈ N:3^{n} ≥ n^{2} + n$
Führen Sie dazu alle Teile der Induktion durch und beschriften sie diese mit den bekannten Bezeichnungen.

#Induktionsvoraussetzung
$$
3^{n}\geq n^{2}+n
$$
#Induktionsanfang
$$
3^{1}\geq 1^{2}+1
$$
$$
3\geq2
$$
#Induktionsbehauptung
$$
3^{n+1}\geq (n+1)^{2} + (n+1)
$$
$$
\geq n^{2}+2n+1+n+1
$$
$$
\geq n^{2} + 3n+ 2
$$
#Induktionsschritt
$$
3^{n+1}=3*3^{n}\geq 3(n^{2}+n)
$$
$$
3n^{2}+3n\geq n^{2}+3n+2 \implies 2n^{2}\geq{2} \text{ für alle Fälle } n\geq1
$$
$$
3^{n+1} = 3 * 3^{n} \geq 3(n^{2}+n) \geq n^{2}+3n+2
$$


## 1.2 Aufgabe 2
Geben Sie alle Lösungen für die folgenden Kongruenzen an oder beweisen sie ihre Unlösbarkeit (in $\mathbb{Z}$):
$9x ≡ 2 \mod 24$
$$
ggT(9,24)=3
$$
keine lösung

$9x ≡ 2 \mod 25$
$$
ggT(9,25)=1
$$
$$
25 = 9 * 2 + 7
$$
$$
9 = 7 * 1 + 2
$$
$$
7 = 2 *3 +1
$$
$$
3 = 1 * 3 + 0
$$



$$
1 =7-2*3
$$
$$
1 = 7 - (9-7*1)*3
$$
$$
1 = 7*4 - 9 * 3
$$
$$
1 = (25-9*2)*4 - 9 * 3
$$
$$
1 = 25*4 - 9 *11
$$

$$
9x \equiv 2 \mod 25
$$
$$
9 * x *-11 \equiv 2 * -11 \mod 25
$$
$$
-99x \equiv -22 \mod 25
$$
$$
-99x + 25*4x \equiv -22 + 25 * 1
$$
$$
x \equiv 3 \mod 25
$$
$$
x= 3 + 25 * p ~~~ p \in \mathbb{Z}
$$
## 1.3 Aufgabe 3
Sie schauen in den Wetterbericht für die nächsten 14 Tage. Das Wetter kann entweder regnerisch oder sonnig sein. Wie viele verschiedene Möglichkeiten für Wetterberichte gibt es mit:

• ohne weitere Einschränkungen
• genau 3 Regentage
• genau 3 Regentage mit einem Sonnentag nach jedem Regentag

$$
2^{14}
$$
$$
\binom{14}{3}\binom{14}{11}
$$
$$
\binom{n+k-1}{k} = \binom{4+8-1}{8}=\binom{11}{8}
$$

## 2.1 Aufgabe 1
Beweisen Sie mittels vollständiger Induktion für alle $n ≥ 1, n ∈ N:4^{n} ≥ 3 · n^{2} + n$
Führen Sie dazu alle Teile der Induktion durch und beschriften sie diese mit den bekannten Bezeichnungen.

#Induktionsvoraussetzung
$$
4^{n}\geq3n^{2}+n
$$
#Induktionsanfang
$$
4^{1}\geq 3*1^{2}+1
$$
$$
4\geq 4
$$
#Induktionsbehauptung
$$
4^{n+1}\geq3(n+1)^{2}+(n+1)
$$
$$
\geq 3 * (n^{2}+2n+1) + n+ 1
$$
$$
\geq 3n^{2}+6n+3+n+1
$$
$$
\geq 3n^{2} +7n+4
$$
#Induktionsschritt
$$
4^{n+1} = 4*4^{n}\geq 4*(3n^{2}+n)
$$
$$
12n^{2}+4n\geq 3n^{2}+7n+4 \implies 9n^{2}\geq 3n +4 \text{ wahr für alle }n\geq1 
$$
$$
4^{n+1}=4*4^{n}\geq4(3n^{2}+n)\geq 3n+4
$$


## 2.2 Aufgabe 2
Geben Sie alle Lösungen für die folgenden Kongruenzen an oder beweisen sie ihre Unlösbarkeit (in $\mathbb{Z}$):

$15x ≡ 3 \mod 25$

$$
ggT(15,25) = 5
$$
keine Lösung

$15x ≡ 3 \mod 26$

$$
ggT(15,26)=1
$$
$$
26 = 15 * 1 + 11
$$
$$
15 = 11 * 1 +4
$$
$$
11 = 4 * 2 + 3
$$
$$
 4 = 3 * 1 + 1
$$
$$
1 = 1 + 0
$$




$$
1=4 - 3*1
$$
$$
1 = 4 - (11-4*2)*1
$$
$$
1= 3*4 - 11
$$
$$
1= 3 * (15-11*1) - 11
$$
$$
1 = 3 * 15 - 4 *11
$$
$$
1 = 3 * 15 - 4 * (26-15*1)
$$
$$
1 = 7 * 15 - 4 *26
$$

$$
15 x \equiv 3 \mod 26
$$
$$
15x * 7 \equiv 3 * 7 \mod 26
$$
$$
105x \equiv 21 \mod 26
$$
$$
x \equiv 21 \mod 26
$$
$$
x=21 + 26*p
$$


## 2.3 Aufgabe 3
Eine Münze wird 20 mal geworfen. Wie viele Verläufe kann es geben, wenn:

• ohne weitere Einschränkungen
• genau 4 mal Kopf
• genau 4 mal Kopf mit min. 2 mal Zahl nach jedem Kopf

$$
2^{20}
$$
$$
\binom{20}{4}\binom{20}{16}
$$
$$
n = 5, k = 20-(4*3)
$$
$$
\binom{5+8-1}{8}=\binom{12}{8}
$$
