# Definition

Eine Form eines Kellerautomaten ist die Turing-Maschine. Bei dieser wird für eine eindimensionale Eingabe von Zeichen überpüft, ob diese Teil der von der Maschine erkannten Sprache ist. Dabei liest die Maschine immer ein Zeichen der Eingabe und basierend auf dem Zustand in welchem sich die Maschine aktuell befindet, schreibt diese ein Zeichen an die Position des gelesenen Zeichens und wechselt entweder ein Zeichen nach Links, Rechts oder gar nicht. Die Eingabe gilt als akzeptiert wenn sich die Turing-Maschine am Ende der Verarbeitung in einem akzeptierten Endzustand befindet.
## Nicht-Deterministische Turing-Maschine
Eine Nicht-Deterministische Turing-Maschine $M$ wird als 7-Tupel definiert.

Dabei gilt $M = (Q, \Sigma, \Gamma, \delta, q_{0}, \square, F)$ mit:
- **$Q$ als Zustandsmenge.**
  Die Zustandsmenge ist dabei eine endliche Menge von Zuständen, welche die Maschine einnehmen kann.
- **$\Sigma$ als endliches Eingabealphabet.**
  Das Eingabealphabet ist dabei eine endliche Menge von Zeichen, welche von der Maschine verarbeitet werden können.
- **$\Gamma \supset \Sigma$ als endliches Arbeitsalphabet.**
  Das Arbeitsalphabet besteht aus allen Zeichen welche während der Verarbeitung vom Band gelesen, oder auf das Band geschrieben werden können.
- **$\delta$ als Übergangsfunktion.**
  Die Übergangsfunktion beschreibt den Wechsel von einem Zustand in den nächsten, dabei wird immer das aktuelle Zeichen der Eingabe gelesen und mit einem beliebigen Zeichen des Arbeitsalphabets überschrieben. Nach lesen des Zeichens kann sich die Maschine in der Eingabe noch um ein Zeichen nach links oder rechts bewegen.
  $$\delta: Q \times \Gamma \rightarrow P(Q \times \Gamma \times \{ L, R, N \})$$
- **$q_{0} \in Q$ als Anfangszustand.**
  Der Anfangszustand ist ein Zustand der Zustandsmenge $Q$, in welchem sich die Maschine zu Beginn jeder Verarbeitung befindet.
- **$\square \in \Gamma - \Sigma$ als "Blanks" Symbol.**
  Das Blanks-Symbol ist ein Symbol welches zwar im Arbeitsalphabet, nicht aber im Eingabealphabet enthalten ist. Dieses Symbol befindet sich auf jedem Feld der Eingabe welches zu Beginn nicht beschrieben ist.
- **$F \subseteq Q$ als Menge von Endzuständen**
  Die Menge von Endzuständen ist eine Teilmenge der Zustandsmenge $Q$. Beim erreichen eines dieser Zustände beendet die Maschine die verarbeitung und das Wort gilt als aktzeptiert.
## Determinitsiche Turing Maschine
Eine Deterministische Turing-Maschine $M$ wird als 7-Tupel definiert $M = (Q, \Sigma, \Gamma, \delta, q_{0}, \square, F)$. Die  einzelnen Elemente sind dieselben wie für eine Nicht-Deterministische Turing-Maschine, mit Ausnahme der Übergangsfunktion.
Bei dieser geht die Maschine aus dem aktuellen Zustand, beim lesen eines Zeichens des Arbeitsalphabets in einen anderen Zustand über. Zusätzlich wird das Zeichen auf dem Band durch ein anderes, beliebiges Zeichen des Arbeitsalphabets ersetzt und die Maschine kann sich um ein Zeichen nach links oder rechts bewegen.
$$\delta: Q \times \Gamma \rightarrow Q \times \Gamma \times \{ L, R, N \}$$
## Konfiguration
Die Konfiguration einer Turing-Maschine lässt sich durch ein Wort $k$ darstellen. Dabei hat $k$ die Form $k = \alpha q \beta$ und besteht aus:
- $q \in Q$ als aktueller Zustand der Maschine
- $\alpha \in \Gamma^{*}$ als Zeichenkette links des aktuell selektierten Zeichens
- $\beta \in \Gamma^{*}$ als Zeichenkette ab dem aktuell selektierten Zeichen