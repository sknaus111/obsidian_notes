Um allgemein von einem beliebigen Zahlensystem in ein anderes umzurechnen kann entweder die Variante mit Stellenwerten verwendet werden oder das Hornerschema.

Gegeben $Z_{b}$ in Querdarstellung $(u_{m}\dots u_{2}u_{1}u_{0})_{b}$
Gesucht $U = (U_{n} \dots U_{2}U_{1}U_{0})_{B}$

## Stellenwerte
Umwandeln der Ziffern in $u_{i}$
Umwandeln von $b^i$
Berechnung von $u_{m}b^m+\dots+u_{1}b+u_{0}$

## Hornerschema
Setze $Z_{0} \gets Z, i \gets 0$
Solange $Z_{i} \not = 0$

$a_{i} \gets Z_{i} mod B$
$Z_{i+1} \gets \frac{Z_{i}-a_{i}}{B}$
$i\gets i+1$

Das gleiche auch mit dem Nachkommateil

Gegeben $Z_{b}$ in Querdarstellung $(0.u_{-1}u_{-2}\dots u_{-m})$
Gesucht $U = (0.U_{-1}U_{-2}\dots U_{-n})$

## Stellenwerte
Umwandeln der Ziffern in $u_{-i}$
Umwandeln der Stellenwerte in $b^{-i}$
Berechnung von $u_{-1}b^{-1}+u_{-2}b_{-2}+u_{-m}b_{-m}$

## Hornerschema
$x_{-1} \gets u, i \gets 1$
Solange $u_{-1} \not = 0$ und $Nachkommastellen \leq n$
$U_{-i} = \lfloor x_{-i}*B \rfloor$
$x_{-(i+1)}\gets x_{-i}*B-U_{-1}$
$i\gets i+1$


## Hexadezimalsystem

Das Hexadezimalsystem besteht aus den Ziffern $\{0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F\}$

Gegeben $(1C7)_{16}$
Gesucht $()_{10}$

## Stellenwerte

$(1 ~~~~~~~~~~~~~ C~~~~~~~~~~~~~~~ 7)_{16}$
$1*16^2+12*16^1+7*16^0 = (455)_{10}$

## Hornerschema

$(1 ~~~~~~~~~~~~~~ C ~~~~~~~~~~~~~~ 7)$
$(1*16 +12)*16 + 7$
$~~~~~~~~~~~~~~~~~~ 28*16+7 = (455)_{10}$

Gegeben $(29)_{10}$
Gesucht $()_{16}$

$U_{0} = 29 ~mod~ 16 = 13$
$U_{1} = 1 ~mod~16=1$

$(13)_{10} = (D)_{16}$
$(1)_{10}=(1)_{16}$

Ergebnis $(29) = (1D)_{16}$