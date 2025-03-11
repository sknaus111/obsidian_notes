## 1 Leserregister
Betrachten Sie die folgenden Relationen, wobei die Primärschlüssel unterstrichen sind:

```
leser(name, geburtsdatum, stadt)
buch(titel, autor, genre, erscheinungsjahr, bewertung)
gelesen(name → leser.name, titel → buch.titel, datum)
ausleihen(verleiher → leser.name, ausleiher → leser.name, titel → buch.titel,
datum)
```

### 1.1 Geben Sie für jede der folgenden Anfragen einen entsprechenden Ausdruck in relationaler Algebra an:
(a) Finden Sie die Namen aller Leser, die in der Stadt “Madrid” wohnen.
$$\pi_{name}(\sigma_{stadt=\text{"Madrid"}}(leser))$$

(b) Finden Sie die Titel aller Bücher, die seit dem “01.01.2000” erschienen sind.
$$\pi_{titel}(\sigma_{erscheinungsjahr\geq01.01.2000}(buch))$$

(c) Finden Sie die Namen aller Leser, die in der Stadt “Madrid” wohnen und zumindest ein
Buch gelesen haben
$$\pi_{name}(\sigma_{stadt=\text{"Madrid"}}(leser ⋉ gelesen))$$

(d) Finden Sie die Namen aller Leser, die in der Stadt “Madrid” wohnen und zumindest ein
Buch gelesen haben, dass seit dem “01.01.2000” erschienen ist.
$$\pi_{name}(\sigma_{stadt=\text{"Madrid"}}(leser ⋉ \sigma_{erscheinungsjahr\geq01.01.2000}(gelesen ⋈ buch)))$$
### 1.2 Geben Sie für jede der folgenden Anfragen einen entsprechenden Ausdruck in relationaler Algebra an:
(a) Finden Sie die Namen aller Leser, die dieses Jahr ein Buch ausgeliehen haben.
$$\pi_{name}(leser ⋉ \sigma_{datum\geq 01.01.2025} (ausleihen))$$
(b) Finden Sie die Namen und Städte aller Leser, die dieses Jahr ein Buch ausgeliehen haben
$$\pi_{name,stadt}(leser ⋉ \sigma_{datum\geq 01.01.2025} (ausleihen))$$
(c) Finden Sie die Titel der Bücher, die verliehen werden oder gelesen wurden.
$$\pi_{titel}(buch ⋉ (gelesen ⟗ ausleihen))$$
(d) Finden Sie die Autoren der Bücher, die verliehen werden oder gelesen wurden.
$$\pi_{autor}(buch ⋉ (gelesen ⟗ ausleihen))$$
### 1.3 Geben Sie für jede der folgenden Anfragen einen entsprechenden Ausdruck in relationaler Algebra an:
(a) Finden Sie die Namen aller Leser, die in der gleichen Stadt wohnen, wie eine Person von der sie ein Buch ausgeliehen haben.
$$
\pi_{name}(leser ⋉
$$
$$
(\sigma_{ausleiher.stadt=verleiher.stadt} (p_{ausleiher}(leser ⨝ ausleien) ⨝_{ausleiher.verleier=verleiher.name} p_{verleiher}(leser))) 
$$$$
)
$$

(b) Finden Sie die Namen aller Leser, die nicht das Buch “Elantris” gelesen haben. Bitte beachten Sie auch den Fall, dass eine Leser nicht in der Relation gelesen vorkommt.
$$\pi_{name}(leser)-\pi_{name}(\sigma_{titel=\text{"Elantris"}}(gelesen))$$

(c) Finden Sie die Namen von den Lesern, die ein Buch ausgeliehen haben, das sie schon gelesen
haben.
$$
\pi_{name}(leser ⋉ 
$$$$(\sigma_{ausgeliehen.titel=gelesen.titel}(p_{ausgeliehen}(ausleihen) ⨝_{augeliehen.ausleiher=gelesen.name}p_{gelesen}(gelesen)))
$$$$)
$$

### 1.4 Geben Sie für jede der folgenden Anfragen einen entsprechenden Ausdruck in relationaler Algebra an:
(a) Finden Sie die Anzahl an gelesenen Bücher pro Leser (einmal mit und einmal ohne den Personen, die keine Bücher gelesen haben).
$$
\gamma_{name;count(titel)}(gelesen)
$$
$$
\gamma_{name;count(titel)}(gelesen ⟗ leser) 
$$
(b) Finden Sie für jedes Genre die Bücher, die die beste Bewertung für dieses Genre haben.
$$
\pi_{titel}(\gamma_{genre;max(bewertung)}(buch) ⨝_{genre=auswahl.genre \land max(bewertung)=auswahl.bewertung}p_{auswahl}(buch) )
$$

(c) Finden Sie die Leser, die alle am besten bewerteten “fantasy” Bücher gelesen haben.
$$
\pi_{name}(gelesen ⋉ (\gamma_{genre;max(bewertung)} ⨝_{max(bewertung)=auswahl.bewrtung\land genre=\text{"Fantasy"}}p_{auswahl}(buch)))
$$

## 2 Relationale Division
Betrachten Sie die formale Definition der relationalen Division (alternativer Ausdruck in der
relationalen Algebra, der nur grundlegende Operationen verwendet und dasselbe Ergebnis liefert),
versuchen Sie zu verstehen, warum der alternative Ausdruck korrekt ist, und beschreiben Sie die
Schritte mit Ihren eigenen Worten.

$$π_{(R-S)}(R) − π_{(R-S)}((π_{(R-S)}(R) × S) − R)$$
In der Zieltabelle R werden alle Duplikate (gleiches erstes Attribut) entfernt. 
$$
\pi_{(R-S)}(R)
$$
Nun erstellt man eine Tabelle welche alle möglichen Kombinationen des ersten Attributs mit dem zweiten gibt
$$
\pi_{(R-S)}(R) \times S
$$
Die Kombinationen welche es in R bereits gibt wieder entfernen so, dass nur noch die nicht existierenden Kombinationen übrig bleiben.
$$
(\pi_{(R-S)}(R) \times S)-R
$$
Die nicht existierenden Tupel werden zu einer Liste der ersten Attribute vereinfacht. Diese zeigt nun welche der ersten Attribute nicht mit jedem Element des zweiten ein Tupel bilden.
$$
π_{(R-S)}((π_{(R-S)}(R) × S) − R)$$
Im letzten Schritt einfach die Tupel von der Liste alle Tupel abziehen, welche nicht eine Kombination mit jedem anderem zweiten Attribut haben.
$$π_{(R-S)}(R) − π_{(R-S)}((π_{(R-S)}(R) × S) − R)$$