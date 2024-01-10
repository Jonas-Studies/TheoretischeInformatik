# Definition
Für eine kontextfreie Sprache $L$ gibt es eine Konstante $n$ so dass sich alle Wörter $z \in L$, $|z| \geq n$ zerlegen lassen in $z = uvwxy$, so dass folgende Aussagen zutreffen:
- $|vwx| \geq n$
- $|vx| \ge 1$
- $\forall i \ge 0: uv^{i}wx^{i}y \in L$
# Anwendung
Mithilfe des Pumping Lemmas kann ein Widerspruchsbeweis geführt werden, dass eine Sprache keine kontextfreie Sprache sein kann. Dabei müssen sich alle Wörter der Sprache wie in der Definition zerlegen lassen. Mit diesen wird dann versucht anhand der Struktur des Wortes sowie den drei Aussagen einen Widerspruch zu bilden.