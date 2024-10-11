Zahlen mit einem Nachkommaanteil werden im Dezimalsystem wie folgt mit Ziffern dargestellt. 
$$
\sum_{i=1}^{n}a_{-i}10^{-i}
$$
Beispielsweise würde diese Summenformel für Zahlen im Binärsystem so aussehen. 
$$
\sum_{i=1}^na_{-i}2^{-i}
$$
Beispielsweise will man den folgende Binärzahl $0.1101_{2}$ in das Dezimalsystem umwandeln. Als erste Variante könnte man wieder Stellenwerte verwenden.

## Stellenwerte
$0.1101_{2}=1*2^{-1}+1*2^{-2}+0*2^{-3}+1*2^{-4} = 0.8125_{10}$
## Hornerschema 

$~~~~~~~~~1 ~~~~~0 ~~~~~~~~~ 1 ~~~~~~~~~~~ 1$
$(((1/2+0)/2+1)/2 +1) / 2$
$~~~~~~~~~~~((0.5 / 2+1) / 2 + 1) / 2$
$~~~~~~~~~~~~~~~~~~~~~~~(1.25 / 2 + 1) / 2$
$~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~1.625 / 2 = (0.8125)_{10}$

Gegeben sei die Dezimalzahl u dargestellt als $(0.u_{-1}u_{-2}\dots u_{-m})_{10}$
Die Binärzahl U in der Darstellung $U = (0.U_{-1}U_{-2}\dots U_{-n})_{2}$

## Hornerschema 
$x_{-1} \gets u, i \gets 1$
Solange $x_{-i} \not = 0$ und $Nachkommastellen \leq n$
$U_{-i} = \lfloor x_{-i}*2  \rfloor$
$x_{-(i+1)} \gets x_{-i}*2-U_{-1}$
$i \gets i+1$

Mit einer konkreten Zahl kann dieses System wie folgt angewendet werden. 
Gegeben $(0.8125)_{10}$
Gesucht $(0.~~~~)_{2}$

$U_{-1} = \lfloor 0.8125 * 2 \rfloor = \lfloor 1.625 \rfloor = 1$
$U_{-2} = \lfloor 0.625*2 \rfloor = \lfloor 1.25 \rfloor = 1$
$U_{-3} = \lfloor 0.25*2 \rfloor =\lfloor 0.5 \rfloor=0$
$U_{-4} = \lfloor 0.5*2 \rfloor = \lfloor 1 \rfloor = 1$
$U_{5} = \lfloor 0*2 \rfloor = \lfloor 0 \rfloor$ Abbruch

Ergebnis $0.8125_{10} = 0.1101_{2}$

Gegeben $(0.815)_{10}$
Gesucht $(0.~~~~)_{2}$ bis zur 5ten Nachkommastelle

$U_{-1} = \lfloor 0.815*2 \rfloor = \lfloor 1.63 \rfloor = 1$
$U_{-2} = \lfloor 0.63*2 \rfloor = \lfloor 1.26 \rfloor = 1$
$U_{-3} = \lfloor 0.26*2 \rfloor = \lfloor 0.52 \rfloor = 0$
$U_{-4} = \lfloor 0.52*2 \rfloor = \lfloor 1.04 \rfloor = 1$
$U_{-5} = \lfloor 0.04*2 \rfloor = \lfloor 0.08 \rfloor = 0$
Abbruch da 5te Nachkommastelle erreicht wurde.

Ergebnis $(0.815)_{10}= (0.11010)_{2}$
