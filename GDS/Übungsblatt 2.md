## Aufgabe 1: Binäre Gleitpunkt-Arithmetik – Addition & Subtraktion  

Gegeben sind die Zahlen $A = (0.31525)_{8}$ und $B = (–0.02CE)_{16}$.  

Es gilt folgendes Gleitpunktformat:  
$F(2, 11, –14, 15, true)$ mit Formatbreite $16$ Bit und impliziter Darstellung des ersten Bits. Mit Ausnahme der kleineren Formatbreite ist dieses Gleitpunktformat analog zum IEEE 754 Single Precision-Format aufgebaut.

### a) 
Stellen Sie A und B in diesem Gleitpunktformat dar! Verwenden Sie Guard- und Round-Digit sowie  
das Sticky-Bit zur Vermeidung von numerischen Ungenauigkeiten. Runden Sie mittels round to  
nearest zusammen mit round to even.  

$0.31525$
$0.011~001~101~010~101$

$1.100~1101~0101~01 *2^{-2}$
$e=01111$
$0~~01101~~1001~1010~1010~1$
$0~~01101~~1001~1010~11$

$-0.02CE$
$-0.0000~0010~1100~1110$

$-1.01100111 * 2^{-7}$
$e=01111$

$1~~01000~~0110~0111~00$
### b)
Berechnen Sie anschließend $A + B$ sowie $A – B$ und stellen Sie das Ergebnis wieder als Gleitpunkt-  
zahl im angegebenen Format dar. Runden Sie die Ergebnisse wieder mittels round to nearest in  
Kombination mit round to even.

$1.0110~0111~00$
$-7-(-2)=-5$
$0.000010110~0111~00$


$1.1001~1010~1100~0~$
$0.0000~1011~0011~1-$
$1.1000~1111~1001~1$

$1.1000~1111~1001~1$
## Aufgabe 2: Binäre Gleitpunkt-Arithmetik – Multiplikation & Division  
Gegeben sind die folgenden im 16-Bit-Gleitpunktformat (vgl. Aufgabe 1) codierten Zahlen:  
$A = 0 11001 0100100001$  
$B = 1 00101 0110100000$  
$C = 1 10101 0100010000$  
Führen Sie mit den Zahlen folgende Berechnungen durch und codieren Sie das Ergebnis jeweils im 
angegebenen Gleitpunktformat! Verwenden Sie Guard- und Round-Digit sowie das Sticky-Bit zur Vermeidung von numerischen Ungenauigkeiten. Runden Sie mittels round to nearest zusammen mit round away from zero.

Hinweis: Beachten Sie das implizite erste Bit.  

### a)
$$
A * B
$$
### b) 
$$
\frac{A}{C}
$$

## Aufgabe 3: Binäre Gleitpunkt-Arithmetik – Sonderfälle  
Gegeben sind die folgenden im 16-Bit-Gleitpunktformat (vgl. Aufgabe 1) codierten Zahlen:  
$A = 0 00001 0000000000$  
$B = 0 00010 0000100101$  
$C = 1 11101 0001100001$  
$D = 0 00000 0010000000$  
Führen Sie mit den Zahlen folgende Berechnungen durch und codieren Sie das Ergebnis jeweils im 
angegebenen Gleitpunktformat! Verwenden Sie Guard- und Round-Digit sowie das Sticky-Bit zur Vermeidung von numerischen Ungenauigkeiten. Runden Sie mittels round to nearest zusammen mit round toward plus inﬁnity (= gerichtetes Aufrunden)!  

### a) 
$$
A*B
$$ 
### b)
$$
B+D
$$  
### c) 
$$
\frac{C}{D}
$$

## Aufgabe 4: Rundungsfunktionen  
Beantworten Sie folgende Fragen zum Thema Rundung. Verwenden Sie die Schreibweise und die Deﬁnitionen, die Sie aus der Vorlesung kennen.  

### a) 
Nennen Sie die Eigenschaften, die eine Rundungsfunktion $□ : \mathbb{R} → \mathbb{Z}$ erfüllen muss.  
### b) 
Deﬁnieren Sie die Rundungsfunktion für ”round away from zero“ mithilfe von $x, x_{1}, x_{2}, \hat{x}$, wobei  
$x_{1} = max\{z ∈ \mathbb{Z} : z ≤ x\}, x_{2} = min\{z ∈ \mathbb{Z} : x < z\}$ und $\hat{x} = (x_{1} + x_{2})/2$. 
D.h. deﬁnieren Sie eine neue Rundungsfunktion, die positive Zahlen die nicht in $\mathbb{Z}$ sind zur nächst  
größeren Zahl aufrundet und negative Zahlen die nicht in $\mathbb{Z}$ sind auf die nächst kleinere Zahl  
abrundet.  



Hinweis: es werden nicht notwendigerweise alle hier deﬁnierten Variablen benötigt.

## Aufgabe 5: Gleitkommazahlen  
Sie haben folgendes Code-Fragment in Java gegeben:  
```java
float sum = 0.0 f ;  
int counter = 0;  

while ( counter < N ){  
	sum += 0.4 f ;  
	counter ++;  
}  
System . out . println ( sum );  
```

Auf einer Testmaschine ergeben sich für verschiedene Werte von $N$ folgende Zahlen als Ausgabe:  

0.8              ( bei N = 2 )  
2.4              ( bei N = 6 )  
2.8000002  ( bei N = 7 )  
4.0000005  ( bei N = 10)  
40.000008  ( bei N = 100)  
399.9962    ( bei N = 1000)  
3999.6116  ( bei N = 10000)  
39994.227  ( bei N = 100000)  
403833.38  ( bei N = 1000000)  
4351748.0  ( bei N = 10000000)  
8388608.0  ( bei N = 100000000)  
8388608.0  ( bei N = 1000000000)  
Beantworten Sie folgende Fragen:

## a) 
Warum haben nicht alle Berechnungen exakte Ergebnisse (auch bei kleineren Werten für N)?  
## b) 
Warum verändert sich das Ergebnis nicht mehr für sehr große Werte von N? Überlegen Sie was  
bei der Addition von zwei Gleitkommazahlen im Detail passiert.

### c) 
Auch wenn die Zuweisung $sum += 0.1f;$ lautet, sind die Ergebnisse z.B. für N = 100 nicht korrekt. 
Warum?  
### d) 
Wenn die Zuweisung $sum += 0.875f;$ (bzw. $sum = sum + 0.875f$) lautet, werden die Ergebnisse  
für z.B. N = 1 000 000 korrekt berechnet.  

– Warum ist das so?  
– Gilt das dann auch für N = 1 000 000 000? Begründen Sie ihre Antwort!

## Aufgabe 6: NRZ-Code  
Gegeben ist der nachfolgende Signalverlauf mit Pegel 1 (high) und Pegel 0 (low).  

![[Pasted image 20241126195619.png]]

### a) 
Interpretieren Sie den Signalverlauf als NRZ-L-Codierung und geben Sie die decodierte 0/1-Folge an (Länge 12 Bits).  
### b) 
Interpretieren Sie den Signalverlauf als NRZ-M-Codierung und geben Sie die decodierte 0/1-Folge an (Länge 12 Bits).  

### c) 
Zeichnen Sie zum nachfolgend gegebenen Signalverlauf in NRZ-S-Codierung darunter den entsprechenden Signalverlauf in NRZ-L-Codierung.  

![[Pasted image 20241126195731.png]]

## Aufgabe 7: EAN-13-Code  
### a) 
Decodieren Sie die nachfolgende EAN.  

![[Pasted image 20241126195755.png]]

### b) 
Codieren Sie die EAN 5 630136 879628. Berechnen Sie hierzu die Prüfziffer, vergleichen Sie diese  
mit der gegebenen Prüfziffer, und tragen Sie den resultierenden Code in das vorgedruckte Raster  
ein.  

![[Pasted image 20241126195824.png]]

Hinweis: Rand- und Trennzeichen sind grau hinterlegt.