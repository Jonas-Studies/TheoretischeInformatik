Ein DEA welcher als 5-Tupel definiert ist, kann einfach in eine reguläre Grammatik als 4-Tupel umgewandelt werden. Dabei gilt:
- $V$ der Grammatik entspricht $Q$ des Automaten.
- $\Sigma$ der Grammatik entspricht $\Sigma$ des Automaten.
- $S$ der Grammatik entspricht $q_{0}$ des Automaten.
- $P$ der Grammatik ergeben sich aus $\delta$ und $F$ des Automaten. Dabei gilt:
  - Für $r_{1} \in \Sigma$ sowie $q' \notin F$ des Automaten:
    $$\forall \delta(q, r_{1}) = q' \Rightarrow q \rightarrow r_{1}q'$$
	 - Für $r_{1} \in \Sigma$ sowie $q' \in F$ des Automaten:
  $$\forall \delta (q, r_{1} = q' \Rightarrow q \rightarrow r_{1} | r_{1}q')$$