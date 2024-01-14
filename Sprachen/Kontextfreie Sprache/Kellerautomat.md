# Definition
Ein Kellerautomat ist eine Maschine zum erkennen von [[Kontextfreie Sprache|Kontextfreien Sprachen]]. Ein Nicht-Deterministischer Kellerautomat $M$ lässt sich als 6-Tupel definieren.

Dabei gilt $M = (Q, \Sigma, \Gamma, \delta, q_{0}, \#)$ mit:
- **$Q$ als Zustandsmenge.**
  Die Zustandsmenge ist dabei eine endliche Menge von Zuständen, welche die Maschine einnehmen kann.
- **$\Sigma$ als Bandalphabet.**
  Das Bandalphabet ist dabei eine endliche Menge von Zeichen, welche von der Maschine verarbeitet werden.
- **$\Gamma$ als Kelleralphabet.**
  Das Kelleralphabet ist dabei eine endliche Menge von Zeichen, welche die Maschine während einer Verarbeitung in den Kellerspeicher schreiben kann.
- **$\delta$ als Übergangsfunktion.**
  Die Übergangsfunktion beschreibt den Übergang der Maschine von einem Zustand in den nächsten. Dabei wird jeweils ein Zeichen vom Bandalphabet sowie das erste Zeichen vom Kellerspeicher gelesen. Zusätzlich werden beliebig viele Zeichen in den Kellerspeicher geschrieben.
  Sei $P_{f}(X)$ eine Funktion, welche die Menge aller endlichen Teilmengen der Menge $X$ angibt, Dann ist $\delta$ definiert als:
$$\delta: Q \times (\Sigma \cup \epsilon) \times \Gamma \longrightarrow P_{f}(Q \times \Gamma^{*})$$  
- **$q_{0} \in Q$ als Anfangszustand.**
  Der Anfangszustand ist ein Zustand der Zustandsmenge $Q$, in welchem sich die Maschine zu Beginn jeder Verarbeitung befindet.
- **$\# \in \Gamma$ als anfänglichem Kellersymbol.**
  Das Kellersymbol ist ein Zeichen des Kelleralphabets $\Gamma$, welches zu Beginn jeder Verarbeitung der Maschine im Kellerspeicher steht.
# Konfiguration
## Definition
Die Konfiguration eines PDA lässt sich als Drei-Tupel $(q, \Sigma^{*}, \Gamma^{*})$ darstellen. Diese stellt den aktuellen Zustand des PDA dar und besteht aus:
- Dem Zustand $q$ in welchem sich der PDA aktuell befindet, für welchen gilt: $q \in Q$
- Einer Zeichenkette $w'$ als der noch zu lesende Anteil der Eingabe. Für diese gilt: $w' \in \Sigma$
- Dem aktuellen Kellerinhalt $y$ für welchen gilt: $y \in \Gamma^{*}$

## Konfigurationsübergang
Der Konfigurationsübergang ist eine Funktion $\vdash$ welche von einer Konfiguration in die nächste übergeht.
$$|-: Q \times \Sigma^{*} \times \Gamma^{*} \rightarrow Q \times \Sigma^{*} \times \Gamma^{*}$$
# Erkannte Sprache
Die von einem Kellerautomaten erkannte Sprache ist wie folgt definiert:
Sei $\overset{*}{\vdash}$ die revlexiv-transitive Hülle von $\vdash.$ $\overset{*}{\vdash}$ ist somit eine Funktion welche von einer Konfiguration, durch mehrere Konfigurationen in eine gültige Konfiguration übergeht.
$$L(M) = \{w \in \Sigma^{*} | (q_{0}, w, \#) \overset{*}{\vdash} (q, \epsilon, \epsilon) \text{ für ein } q \in Q\}$$
# Determinismus
Per Definition sind Kellerautomaten Nicht-Deterministisch. Allerdings lassen sich auch deterministische Kellerautomaten (DPDA) konstruieren, für diese müsste die Konstruktion des PDAs um einen Endzustand $q_f$ erweitert werden. Mit solchen Automaten kann allerdings nicht jede kontextfreie Sprache erkannt werden. Stattdessen würden von diese eine Sprachklasse zwischen den kontextfreien Sprachen und den regulären Sprachen erkennen.