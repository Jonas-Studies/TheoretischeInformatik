# Definition
Eine kontextfreie Sprache ist eine Sprache welche durch eine Grammatik der [[Grammatik#Typ 2 Kontextfreie Grammatiken|Cromsky-Hierachie vom Typ 2]] abgebildet wird.

Kontextfreie Sprachen sind abgeschlossen unter:
- Vereinigung
- Produkt
- Stern

Kontextfreie Sprachen sind nicht abgeschloseen unter:
- Schnitt
- Komplement
# Chomsky-Normalform
Die möglichen Regeln einer Grammatik zum Bearbeiten einer Sprache $L$ werden auf zwei Fälle eingeschränkt.
- Ein Nicht-Terminalsymbol geht über in zwei Nicht-Terminalsymbole
- Ein Nicht-Terminalsymbol geht über in ein Terminalsymbol2
## Beispiel:
Die Sprache $L$ verwendet das Binäralphabet $\Sigma = \{0, 1\}$, die Nicht-Terminalsymbole $V = \{S, A, B\}$, dass Startsymbol $S = S \in V$ sowie folgende Produktionen:
$$S \rightarrow AB | 0 | 1$$
$$A \rightarrow 0$$
$$B \rightarrow 1$$
# Greibach-Normalform
Die möglichen Regeln einer Grammatik zum Bearbeiten einer Sprache werden auf einen Fall eingeschränkt. Hierbei wird immer aus einem Nicht-Terminalsymbol ein Terminalsymbol gefolgt von beliebig vielen Nicht-Terminalsymbolen.