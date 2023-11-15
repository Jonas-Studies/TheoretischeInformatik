# Definition
Ein Nichtdeterministischer-Endlicher-Automat kurz NEA lässt sich als 5-Tupel definieren.
- Eine endliche Menge an Zuständen: $Q$
- Ein endliches Alphabet: $\Sigma$
- Eine Übergangsfunktion: $\delta: Q \times \Sigma \rightarrow P(Q)$
- Eine Menge an  Startzuständen: $E \subseteq Q$
- Eine Menge an Endzuständen: $F \subseteq Q$
## Transitionsfunktion
Die Transitionsfunktion $\hat{\delta}$ bildet eine beliebige Menge von Zuständen $Q' \subseteq Q$ für ein Wort $w$ auf deren endzustände ab.
Der einfachste Fall ist dabei für das leere Wort:
$$\hat{\delta}(Q', \epsilon) = Q'$$
Für alle anderen Wörter gilt:
$$\hat{\delta}(Q', w_{1}, ... , w_{n} = \underset{q \in Q'}{\bigcup} \hat{\delta}(\delta (q, w_{1}, w_{2}, ... w_{n}))$$
## Aktzeptierte Sprache eines NEA
$$L(M) = \{w \in \Sigma^{*} | \hat{\delta} (E, w) \cap F \neq \emptyset$$
# $\epsilon$-NEA
Sollen vom Automaten auch leere Übergänge ermöglicht werden, muss die Übergangsfunktion modifiziert werden. Dabei wird als Alphabet $\Sigma_{*} \equiv \Sigma \cup \{\epsilon\}$ verwendet. 
$$\delta: Q \times \Sigma_{*} \rightarrow P(Q)$$