# Definition
Ein Kellerautomat (Pushdown Automaton kurz: PDA) lässt sich als 6-Tupel $(Q, \Sigma, \Gamma, \delta, q_{0}, \#)$ definieren.
- Eine endliche Zustandsmenge $Q$
- Ein endliches [[Bestandteile einer Sprache#Alphabet|Alphabet]] $\Sigma$ als Bandalphabet
- Ein endliches [[Bestandteile einer Sprache#Alphabet|Alphabet]] $\Gamma$ als Kelleralphabet
- Eine Übergangsfunktion $\delta$
  Sei $P_{f}(X)$ eine Funktion, welche die Menge aller endlichen Teilmengen der Menge $X$ angibt.
$$\delta: Q \times (\Sigma \cup \epsilon) \times \Gamma \longrightarrow P_{f}(Q \times \Gamma^{*})$$
- Ein Anfangszustand $q_{0}$ für welchen gilt $q_{0} \in Q$
- Ein ursprüngliches Kellersymbol $\#$ für welches gilt: $\# \in \Gamma$

Wörter wenden vom Kellerautomaten aktzeptiert wenn dieser das Wort komplett liest und danach der Kellerspeicher leer ist.
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