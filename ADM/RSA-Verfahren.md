Das RSA-Verfahren ist ein **Verschlüsselungsverfahren**, welches folgenden Satz als Grundlage hat.

Seien $p,q$ zwei verschiedene Primzahlen, $v=$kgV$(p-1,q-1)$ und $m=pq$. Dann gilt für beliebige Zahlen $a,k$
$$
a^{kv+1}\equiv a\text{ mod }m
$$
Sind also $e,d \in \mathbb{Z}$ zwei Zahlen mit $ed \equiv 1 \text{ mod }v$, so gilt für alle $a \in \mathbb{Z}$
$$
(a^e)^d \equiv a \text{ mod }m
$$
## Beweis
Man beobachtet, dass $a^{kv+1} \equiv a \text{ mod }m$ genau dann gilt, wenn sowohl $a^{kv+1} \equiv a \text{ mod }p$ als auch $a^{kv+1} \equiv a \text{ mod }q$ gelten. Nun zeigt man die erste dieser beiden Eigenschaften. Die zweite folgt dazu analog, also mittels gleicher Überlegung.
Gilt $p \mid a$, ist die Wahrheit der Aussage offensichtlich, da $a^{kv+1}\equiv 0 \equiv a \text{ mod }p$. Gilt jedoch $p\nmid a$, so folgt aus dem [[Kongruenzen und Restklassen#Kleiner Satz von Fermat]], dass $a^{p-1}\equiv 1 \text{ mod }p$. Setzt man $v=s(p-1)$, so erhält man
$$
a^{kv+1}=a*a^{(k*s)*(p-1)}= a*(a^{p-1})^{k*s} \equiv a*1 \equiv a \text{ mod }p
$$
Möchte man nun mittels des RSA-Verfahren eine Nachricht verschlüsseln so multipliziert der Empfänger $A$ zwei über 100-stellige Primzahlen miteinander und veröffentlicht das Produkt der beiden Zahlen, sowie eine Zahl $e$ die zu $v=kgV(p-1,q-1)$ teilerfremd ist. Will nun der Sender $B$ dem Empfänger $A$ eine Nachricht senden, so unterteilt dieser seine Nachricht in Blöcke von $a_{1},a_{2},\dots$ bis zu maximal $a_{m-1}$. B verschlüsselt diese Blöcke nun durch
$$
b_{j}\equiv a_{j}^e \text{ mod }m ~~~~~~~~~~(j\geq1)
$$
Um die verschlüsselte Nachricht zu entschlüsseln kann $A$ folgende Rechnung anwenden.
$$
a_{j}\equiv b_{j}^d \text{ mod }m ~~~~~~~~~~(j\geq 1)
$$
Da für die manuelle Berechnung von $v=kgV(p-1,q-1)$ die Primfaktorzerlegung von $m=pq$ von Nöten ist und diese bei großen Primzahlen nicht effizient berechnet werden kann, stellt das RSA-Verfahren eine sichere Verschlüsselungsmethode dar.