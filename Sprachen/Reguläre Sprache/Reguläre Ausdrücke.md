# Definition
Reguläre Ausdrücke sind Regeln welche zum erkennen von Zeichen und Zeichenketten verwendet werden können.
# Regeln
## Erkennen von Zeichen
- Erkennen einzelner Zeichen: ``r = a``
- Erkennen eines beliebigen kleinbuchstabens: ``r = a-z``
- Erkennen eines beliebigen Großbuchstabens: ``r = A-Z``
- Erkennen einer beliebigen Ziffer: ``r = 0-9``
## Verknüpfen von Ausdrücken
- Mehrfachanwendung von Ausdrücken
	- Beliebig oft: ``r = r*``
	- Mindestens einmal: ``r = r+``
	- Mindestens n maximal n mal: ``r = r{n, m}``
- Zusammenhängen von Ausdrücken: ``r = rr``
- Abgrenzen von Ausdrücken: ``r = r(rr)+``
- Oder Verknüpfung: ``r = r|r``