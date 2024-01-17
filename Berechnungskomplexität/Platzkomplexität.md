# Definition
$S_{M} \left( \overset{\rightarrow}{x} \right) =$ Anzahl verschiedener Zellen, die $M$ bei Eingabe $\overset{\rightarrow}{x} \in \Sigma^{*}$ besucht.
# Worst-Case
$$T_{M}(n) = \underset{ x \in \Sigma^{*}, |\overset{\rightarrow}{x}| \leq n }{ \text{max} } T_{M}(\overset{\rightarrow}{x})$$

# Platzbeschränkt
Eine Turing-Maschine heißt $s(n)$-platzbeschränkt, wenn für alle $n \in \mathbb{N}$ gilt:
$$S_{M}(n) \leq s(n)$$