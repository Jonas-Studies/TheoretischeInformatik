# Definition
Ein Deterministischer-Endlicher-Automat kurz DEA, lässt sich als 5-Tupel definieren $M = (Q, \Sigma, \delta, q_{0}, F)$. Für eine solche Definition gilt folgendes;
- $Q$
  Die endliche Menge an Zuständen, welche der Automat einnehmen kann.
- $\Sigma$
  Ein endliches Alphabet, welches vom Automaten verarbeitet wird.
- $\delta: Q \times \Sigma \rightarrow Q$
  Die Übergangsfunktion, welche zu jeweils einem gültigen Zustand, sowie einem Buchstaben des Alphabets, den nächsten Zustand zurückliefert.
- $q_{0} \in Q$
  Der Startzustand. Bei welchem der Automat beginnt.
- $F \subseteq Q$
  Eine Teilmenge von $Q$, welche die akzeptierten Endzustände enthält.