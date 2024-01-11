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