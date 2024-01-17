# Definition
$T_{M} \left( \overset{\rightarrow}{x} \right) =$ Anzahl der Schritte von $M$ mit Eingabe $\overset{\rightarrow}{x} \in \Sigma^{*}$.
# Worst-Case
$$S_{M}(n) = \underset{ x \in \Sigma^{*}, |\overset{\rightarrow}{x}| \leq n }{ \text{max} } S_{M}(\overset{\rightarrow}{x})$$
# Zeitbeschränkt
Eine Turing-Maschine heißt $t(n)$-zeitbeschränkt, wenn für alle $n \in \mathbb{N}$ gilt:
$$T_{M}(n) \leq t(n)$$