# Vorgehen
Ein als 5-Tupel definierter NEA $M = (Q, \Sigma, \delta, E, F)$ kann in einen als 5-Tupel definierten DEA $M' = (Q', \Sigma, \delta', q_{0}', F')$ umgewandelt werden. Für die Umwandlung gilt folgendes:
- Das Alphabet $\Sigma$ bleibt für beide Automaten das Selbe.
- $Q' \equiv P(Q)$
  Die Menge aller Zustände im DEA, ist die Potenzmenge aller Zustände im NEA. Wobei bei Elementen mit mehreren Zuständen, Kombi-Zustände gebildet werden.
- $\delta'(Z, a) \equiv \underset{q \in Z}{\bigcup} \delta(q, a)$ mit $Z \in Q' = P(Q)$
  Die Übergangsfunktion im DEA nimmt für einen Zustand $Z \in Q'$ und ein Symbol $a \in \Sigma$ einen weiteren Zustand aus $Q'$ an. Dabei ist dieser neue Zustand ein Kombi-Zustand für alle möglichen Ergebnisse der Übergangsfunktion $\delta$ für jedes Element des eingegebenen Zustandes $Z$ sowie dem Symbol $a$.
- $q_{0}' = E$
  Als neuer Startzustand $q_{0}'$ wird ein Kombi-Zustand aller Elemente der Menge $E$ gebildet.
- $F' = \{Z \in Q' | Z \cap F \neq \varnothing\}$
  Die Menge $F'$ der gültigen Endzustände beinhaltet alle (Kombi-)Zustände $Z \in Q'$ von denen ein Element in der Menge $E$ aller gültigen Endzustände des NEAs enthalten ist.
## Kombi-Zustand
Wenn ein Zustand selbst eine Menge aus mehreren Zuständen ist, wird dieser als Aneinandereihung aller dieser Zustände geschrieben.
### Beispiel
$$Q = \{q_{1}, q_{2}, \{q_{1}, q_{2}\}\} \Rightarrow Q = \{q_{1}, q_{2}, q_{1}q_{2} \}$$
# Ergebnis:
$$L(M) = L(M')$$