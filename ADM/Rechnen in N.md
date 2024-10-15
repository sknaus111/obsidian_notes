 Das Prinzip der #Induktion dient auch als Grundlage für die #rekursive Definition. Beispielsweise lässt sich eine Folge durch die Angabe des ersten Elementes und der rekursiven Beziehung definieren.
 $$
a_{n}=2^n,n\geq 0
$$
$$
a_{n+1} = 2a_{n},n\geq 0
$$
Auch #Exponenten
$$
x^0 := 1, x^{n+1}:=x^nx, n\geq 0
$$
oder die #Fibonacci-Zahlen
$$
F_{0}=0,F_{1}=1,F_{n+1}:=F_{n}+F_{n-1},n\geq 1
$$
können rekursiv definiert werden.

## Addition
Für die #Addition von natürlichen Zahlen dient das #Immerweiterzählen als Grundlage. Eine natürliche Zahl n addiert mit 1 ist durch den Nachfolger n' definiert. Eine Addition mit zwei durch den Nachfolger der Zahl 1.  So kann die Addition in rekursiver Schreibweise definiert werden.
$$
n+k' = (n+k)',n+0=0+n=n
$$
## Multiplikation
Für die #Multiplikation kann ebenfalls rekursiv definiert werden.
$$
k'*n=k*n+n
$$
## Eigenschaften
Für das Rechnen mit natürlichen Zahlen gelten folgende #Gesetze.
1. #Kommutativgesetz: $$
n+m = n+m, n*m = m*n
$$
2. #Assoziativgesetz $$
(n+m)+k = n+(m+k), (n*m)*k = n*(m*k)
$$
3. #Distributivgesetz $$
(n+m)*k = n*k+m*k
$$
4. Existenz eines #neutralen_Elements $$
n+0 = 0+n = n, n*1 = 1*n = n
$$
## Subtraktion
Ist n<= m, so bezeichnet man $k = m-n$ als die #Differenz. In anderen Worten ist k jene Zahl die mit n addiert m ergibt.
## Division
Gibt es zu zwei natürlichen Zahlen m und n, wobei n ungleich 0 ist, eine natürliche Zahl q, welche mit n multipliziert m ergibt, so ist q der #Quotient. Dieser wird als $q = m/n$ geschrieben.