# Definition
Eine Grammatik lässt sich als 4-Tupel $G = (V, \Sigma, P, S)$ definieren. Für diese Definition gilt:
- $V$
  Eine endliche Menge $V$ an Nicht-Terminal-Symbolen.
- $\Sigma: \Sigma \cap V = \emptyset$
  Ein von der Grammatik verwendetes Alphabet $\Sigma$ aus Terminal-Symbolen.
- $P: P \subseteq (V \cup \Sigma)^{+} \setminus \Sigma^{+} \times (V \cup \Sigma)^{*}$
  Eine endliche Menge an Produktionen oder Regeln $P$, welche die Konstruktion von Wörtern ermöglichen. Eine Regel folgert aus mindestens einem Nicht-Terminalsymbol und beliebig vielen Terminal-Symbolen, beliebig viele Nicht-Terminal- und Terminal-Symbole.
- $S \in V$
  Ein Startsymbol $S$, bei welchen die Grammatik beginnt.
# Chomsky-Hierachie (Typen)
## Definition
Einteilung der Menge aller Grammatiken in sich durch Einschränkungen unterscheidende Klassen.
## Typ 0: Phasenstrukturgrammatiken
Hier gibt es keine Einschränkungen für Anzuwendende Produkte.
## Typ 1: Kontextsensitive Grammatiken
Auf der linken Seite $l$ dürfen nicht mehr Symbole stehen als auf der rechten Seite $r$
$$|l| \leq |r|$$
Ausnahmefall für das leere Wort $\epsilon$. Wenn eine Sprache mit dem leeren Element gewünscht ist. Ist auch $l \rightarrow \epsilon$ zulässig.
## Typ 2: Kontextfreie Grammatiken
Auf der linken Seite $l$ darf nur ein Nicht-Terminal-Symbol $(V)$ stehen.
$$|l| = 1 \land l \in V$$
## Typ 3: Reguläre Grammatik:
Auf der rechten Seite $r$ darf nur ein Terminal-Symbol oder ein Terminal-Symbol gefolgt von einem Nicht-Terminal-Symbol stehen darf.
$$r \in \Sigma \cup \Sigma V$$
# Vereinfachungen (EBNF)
1. Wenn mehrere Produkte mit dem selben $l$ gebildet werden, müssen nicht alle Produkte einzeln aufgeschrieben werden. Stattdessen kann $l \rightarrow r_1 | r_2 | r_3$ geschrieben werden.
2. Symbole können durch eckige Klammern als optional gekennzeichet werden: $l \rightarrow a[b]c$
3. Symbole können durch geschweifte Klammern als beliebig oft wiederholend vorkommen: $l \rightarrow a{b}c$. Hieraus möglich ist: $abc, abbc, abbbc, ...$
# Ableitbarkeit
Sei ein Produkt $l \in (V \cup \Sigma)^{+} \backslash \Sigma^{+}$ und $r \in (V \cup \Sigma)^{*}$. Dann ist $r$ aus $l$:
- Direkt ableitbar, wenn es ein Produkt $(u, v) \in P$ und $\alpha, \beta \in (V \cup \Sigma)^{*}$ gibt, so dass:
  $$l = \alpha u \beta, r = \alpha v \beta$$Formal: $l \Rightarrow r$.
- Indirekt ableitbar, wenn es durch endlich viele Ableitungsschritte aus $l$ erzeugbar ist.
  Formal: $l \xRightarrow{*} r$ (reflexiv-transitive Hülle der Ableitungsrelation $\Rightarrow$)
#### Erzeugte Sprache $L(G)$
$$L(G) \equiv \{w \in \Sigma^{*} \mid S \xRightarrow{*} w\}$$
## Beispiel:
Nicht-Terminal-Symbole: $V = \{S, A, B, C\}$
Terminal-Symbole: $\Sigma = \{a, b, c\}$
Produkte (Regeln): $P = \{S \rightarrow A, A \rightarrow a | AB, B \rightarrow b | BC, C \rightarrow c\}$
Startsymbol: $A \in V$

Gewünschtes Wort: abc

Ableitbar durch:
$$ \begin{multline}
S \rightarrow A \newline
A \rightarrow AB \newline
AB \rightarrow ABC \newline
ABC \rightarrow abc
\end{multline} $$
Das Ganze lässt sich auch in einem Ableitungsbaum darstellen:
![[Grammatik_Ableitungsbaum_dark.png]]
## Eindeutigkeit
Eine Grammatik ist eindeutig wenn es für ein Wort $w$ immer nur einen Ableitungsbaum gibt. Sollte dies nicht zutreffen spricht man von einer mehrdeutigen Grammatik.