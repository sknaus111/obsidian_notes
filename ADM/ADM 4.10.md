
   für alle element von nat Zahlen : Eigenschaft von n
   1) beweisen dass 0 eig p hat
   2) wenn eine nat zahl eig p besitzt, so besitzt auch n+1 eig p

manchen situationen funktioniert nicht perfekt 

für alle n aus nat Zahlen, welche größer als n0 sind gilt eig p

1) eig von p trifft auf n0 zu
2) für alle n lässt ich eig auf nachfolger übertragen

n0 element der nat Zahlen

Bsp:
P(n) = 2^n > n+2

P(0)= "2^2 >2" falsch Aussage

P(1) = "2^1 > 3" falsch Aussage

P(2) = "2^2 > 4" falsch Aussage

P(3) = "2^3 > 5" richtige Aussage Induktionsanfang

Vermutung: für alle n >= 3 gilt 2^n > n+2

für alle n>= 3 gilt 2^n>n+2 Induktionsvoraussetzung
folgt 2^n+1 > n+3 Induktionsbehauptung

Sei n element aus nat Zahl mit 2^n>n+2
2^n+1 =2 * 2^n > 2 * n + 4 =
2 * n + 4 umformbar zu: n+3+n+1
n+1 ist großer 0
n + 3 +n +1 > n + 3 

## Verlaufsinduktion

1) P(0)
2) für alle n für alle k <=n gilt P(k) daraus folgt P(n+1)

für alle n aus nat Zahlen gilt P(n)

P(0) und P(1) und ... und P(n)

Bsp:

P(n) = "n ist prim oder Produkt endlich vieler Primzahlen"

Def: nat Zahl n > 1 heißt prim wenn keine r und s existieren wo n = r*s wobei r>1 und s>1. Nicht als Produkt von zwei Zahlen dastellbar, welche größer als 1 und kleiner als n sind.

Beweis von für alle n aus nat Zahlen mit n>1 gilt P(n)

P(2) richtig
P(n+1) Induktions Behauptung
Induktionsvoraussetzung: für alle k zwischen 2 und n gilt P(k)

n+1 
1. Fall n+1 prim = P(n+1) wahr
2. Fall n+1 nicht prim => existiert r,s>1 n+1=r*s => r<n+1, s<n+1
P(r),P(s) wahr => folgt P(n+1) wahr

## Rechnen in N

Addition: n' = n+1
Definieren für alle n: n+0 = n, n+k' := (n+k)'
n * 0 := 0, n * k' := n * k + n

Satz: n,m,k seien N Dann gilt
1) Assoziativgesetz: (n+m)+k = n+(m+k)
2) Existiert neutrales Element: n+0: für alle n gilt n+0 = 0+n = n
3) Kommutativgesertz: n+m=m+n

analog für Multiplikation
4) Distributivgesetz: n * (m+k)=n * m+n * k

wenn n<=m:
m-n:
n+x=m hat Lösung in N

m/n:
n * x = m hat Lösung in N