# Definition
Eine Form eines Kellerautomaten ist die Turing-Maschine. Bei dieser wird für eine eindimensionale Eingabe von Zeichen überpüft, ob diese Teil der von der Maschine erkannten Sprache ist. Dabei liest die Maschine immer ein Zeichen der Eingabe und basierend auf dem Zustand in welchem sich die Maschine aktuell befindet, schreibt diese ein Zeichen an die Position des gelesenen Zeichens und wechselt entweder ein Zeichen nach Links, Rechts oder gar nicht. Die Eingabe gilt als akzeptiert wenn sich die Turing-Maschine am Ende der Verarbeitung in einem akzeptierten Endzustand befindet.
## Nicht-Deterministische Turing-Maschine
Eine Nicht-Deterministische Turing-Maschine $M$ wird als 7-Tupel definiert.

Dabei gilt $M = (Q, \Sigma, \Gamma, \delta, q_{0}, \#, F)$ mit:
- **$Q$ als Zustandsmenge.**
  Die Zustandsmenge ist dabei eine endliche Menge von Zuständen, welche die Maschine einnehmen kann.
- **$\Sigma$ als endliches Eingabealphabet.**
  Das Eingabealphabet ist dabei eine endliche Menge von Zeichen, welche von der Maschine verarbeitet werden.
- **$\Gamma \supset \Sigma$ als endliches Arbeitsalphabet.**
  Das Arbeitsalphabet besteht aus allen Zeichen welche während der Verarbeitung vom Band gelesen, oder auf das Band geschrieben werden können.
- **$\delta$ als Übergangsfunktion.**
  Die Übergangsfunktion
- **$q_{0} \in Q$ als Anfangszustand.**
  Der Anfangszustand ist ein Zustand der Zustandsmenge $Q$, in welchem sich die Maschine zu Beginn jeder Verarbeitung befindet.
- **$\square \in \Gamma$ als "Blanks" Symbol.**
  Fehlt
- **$F \subseteq Q$ als Menge von Endzuständen**
  Die Menge von Endzuständen ist eine Teilmenge der Zustandsmenge $Q$. Sie enthält alle Zustände, in welchen sich die Maschine am Ende einer Verarbeitung befinden muss um ein Wort zu akzeptieren.
## Determinitsiche Turing Maschine