## Komponenten
Die 5 klassischen Komponenten eines Rechners bestehen aus
1. Rechenwerk (Arithmetic Logic Unit, #ALU)
2. Steuer- oder Leitwerk (Control Unit, #CU)
3. Hauptspeicher (Memory)
4. Eingabe (Input)
5. Ausgabe (Output)

dieses klassische Modell wurde von John von Neumann Mitte der 1940er konzipiert.


## Bits
Im Computer werden Daten mittels #Bits gespeichert. Diese sind
- binär
- typischerweise 0 und 1
- manchmal auch L (low) und H (high)
diese werden mit #Flipflops im Computer gespeichert.

## Bytes
Ein Byte fasst 8 Bits zusammen. Mittels diesen werden Größen für Speicher gemessen. Generell verwendet der Computer Bytes für jegliche Berechnung.

**SI-Präfixe**

| Kürzel | Name     | Potenz    | Wert                                |
| ------ | -------- | --------- | ----------------------------------- |
| kB     | Kilobyte | $10^3$    | $~~~~~~~~~~~~~~~~~~~~~$ 1 000 Bytes |
| MB     | Megabyte | $10^6$    | $~~~~~~~~~~~~~$ 1 000 000 Bytes     |
| GB     | Gigabyte | $10^9$    | $~~~~~~$ 1 000 000 000 Bytes        |
| TB     | Terabyte | $10^{12}$ | 1 000 000 000 000 Bytes             |

**Binärpräfixe**

| Kürzel | Name     | Potenz   | Wert                                |
| ------ | -------- | -------- | ----------------------------------- |
| KiB    | Kibibyte | $2^{10}$ | $~~~~~~~~~~~~~~~~~~~~~$ 1 024 Bytes |
| MiB    | Mebibyte | $2^{20}$ | $~~~~~~~~~~~~~$ 1 048 576 Bytes     |
| GiB    | Gibibyte | $2^{30}$ | $~~~~~~$ 1 073 741 824 Bytes        |
| TiB    | Tebibyte | $2^{40}$ | 1 099 511 627 776 Bytes             |
## Code 
Um eine Folge von 0 und 1 zu beispielsweise Buchstaben darzustellen, bedarf es eines Codes. 5 Bits sind bereits genügend um alle Kleinbuchstaben darzustellen, 6 Bits für alle Klein- und Großbuchstaben. 

Um eine Menge x an Kombinationen darzustellen benötigt man $\lceil \log_2{x} \rceil$ Bits.