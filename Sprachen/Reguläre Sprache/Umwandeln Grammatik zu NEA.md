Eine als 4-Tupel definierte reguläre Grammatik $G = (V, \Sigma, P, S)$ kann wie folgt zu einem als 5-Tupel definierten NEA $M = (Q, \Sigma, \delta, E, F)$ umgewandelt werden.
- $Q = V$
  Die Nicht-Terminalsymbole der Grammatik werden zu den Zuständen des Automaten.
- $\Sigma$
  Die Terminalsymbole der Grammatik werden zum Alphabet des Automaten.
- Die Produktionen $P$ der Grammatik werden zur Übergangsfunktion des NEAs $\delta$. Dabei wird für Produktionen welche nur zu Terminalsymbolen führen ein weiterer Zustand eingefügt.
- $E = S$
  Das Startsymbol $S \in V$ wird zum Startzustand
- $F = l: P = l \longrightarrow r \land r = \epsilon$
  Alle produktionen $P = l \longrightarrow r$ für die gilt $r = \epsilon$ werden zu Endzuständen.