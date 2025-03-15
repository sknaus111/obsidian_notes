
## Aufgabe 1. 
Gegeben ist folgende Instanz des Stable Matching Problems bei dem die Schüler innen $(A,B,C,D)$ den Gastfamilien $(W,X,Y,Z)$ zugeordnet werden sollen.

|     | 1.  | 2.  | 3.  | 4.  |
| --- | --- | --- | --- | --- |
| A   | W   | Y   | X   | Z   |
| B   | X   | W   | Y   | Z   |
| C   | W   | Y   | Z   | X   |
| D   | Y   | X   | W   | Z   |

|     | 1.  | 2.  | 3.  | 4.  |
| --- | --- | --- | --- | --- |
| W   | B   | C   | A   | D   |
| X   | D   | A   | B   | C   |
| Y   | A   | B   | C   | D   |
| Z   | A   | B   | D   | C   |

Finden Sie ein Stable Matching mithilfe des Gale-Shapley-Algorithmus aus den Vorlesungsfolien. Lässt der Algorithmus offen, welches Element als nächstes betrachtet werden soll, dann gehen Sie in alphabetischer Reihenfolge vor. Geben Sie alle Zwischenschritte an.

Alle Kinder und Familien als frei kennzeichnen.
Kind A auswählen und Familie W zuordnen.
Kind B auswählen und Familie X zuordnen.
Kind C auswählen, vergleichen welches Kind Familie W präferiert. W präferiert C also C zu Familie W zuordnen und A wieder frei machen.
Kind A auswählen und Familie Y zuordnen.
Kind D auswählen, vergleichen welches Kind Familie Y präferiert. Y präferiert A also bleibt Y und A bestehen.
Vergleichen welches Kind Familie X präferiert. Familie X präferiert D also D zu Familie X zuordnen und B wieder frei machen.
Kind B auswählen, vergleichen welches Kind Familie W präferiert. W präferiert B also B zu Familie W zuordnen und C wieder frei machen.
Kind C auswählen und vergleichen welches Kind Familie Y präferiert. Familie Y präferiert A also bleibt Y und A bestehen.
Kind C zu Familie Z zuordnen

A-Y
B-W
C-Z
D-X





## Aufgabe 4. 
Bestimmen Sie die Worst-Case und Best-Case Laufzeiten der unten angegebenen Algorithmen in Abhängigkeit von $n$ in $Θ$-Notation. Ein Array $A$ mit ausreichender Größe ist dabei als gegeben angenommen.

![[Pasted image 20250315185602.png]]

Worst-Case:
$(n+1)(n-1) = O(n²)$

Best-Case:
$\Omega()$


## Aufgabe 5. 
Bestimmen Sie die Laufzeiten der Algorithmen in Abhängigkeit von n in $Θ$-Notation. Bestimmen Sie außerdem die Werte der Variablen $a$ und $b$ nach der Ausführung der Algorithmen in Abhängigkeit von $n$ in $Θ$-Notation. Verwenden Sie hierfür möglichst einfache Terme.

Hinweis: Zum Lösen von Unteraufgabe (b) ist eine Fallunterscheidung notwendig.

![[Pasted image 20250315193441.png]]

Erklärung zu b
in der ersten schleife wird b immer um die wurzel von n multipliziert. Dies passiert so oft wie hoch der ceil von der wurzel von n ist bzw. floor +1. In der zweiten Schleife wird b mit 2 multipliziert und 2 werden addiert. Somit löst sich die Wurzel auf und es bleibt $(\lfloor \sqrt{ n } \rfloor +1)n+2$ übrig. Dies Schleife wird noch ein zweites mal durchlaufen um auf den Wert von $b$ zu kommen.
![[Pasted image 20250315204028.png]]
Die innere Schleife wiederholt zumindest den Vergleich der if Verzweigung in jedem Durchlauf n mal. Die Äußere Schleife wiederholt sich für jedes Element im Array bis alle unter dem Wert von floor(log(n)) sind. 