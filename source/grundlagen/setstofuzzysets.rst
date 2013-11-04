Übergang: Mengen --> Fuzzy Mengen
=================================

Eine Menge wird durch eine charakterisierende Eigenschaft oder durch eine charakteristische Funktion festgelegt. Für Fuzzy-Mengen wird diese Funktion zur sogenannten Zugehörigkeitsfunktion erweitert.

Klassische (Crisp) Menge
------------------------

**Bsp 1**: Grundlagenmenge :math:`\mathbb{N}`
Teilmenge

.. math::
  M = \{ x \mid x \in \mathbb{N} \wedge \text{x hat zweistellige Dezimaldarstellung ohne führende Null} \}

Also :math:`M = \{ 10,11,...,99 \}`

Charakteristische Funktion:

.. math::
  \mathcal{X}_m \mid \mathbb{N} \rightarrow \{ 0,1 \} \\
  \mathcal{X}_m(x) = \text{1 falls obrige dez. darstellung vorhanden, o sonst}

Fuzzy-Menge
-----------

**Grundlage**: Alle 4-jährigen Kinder mit Wohnort Kiel

**Teilmenge**: Alle großen 4-jährigen Kinder

**Frage**: Wie soll "groß" definiert werden?

**Idee**: Befragung von Kinderärzten und die Erweiterung der charakteristischen Funktion durch "Zugehörigkeitsfunktion".

**Graphisch**:
  .. image:: http://i.imgur.com/n4WBemF.jpg
    :width: 400
    :height: 300

**Bemerkung**: die definierende Eigenschaft einer Fuzzy-Menge wird allgemein linguistisch festgelegt. (z.B. "etwa 10",....)

**Modellierung**: linguistischer Begriff :math:`\rightarrow` Zugehörigkeitsfunktion

**Definition**:
Eine Fuzzy-Menge (unscharfe Menge) A über eine Definitionsmenge X ist eine Menge von geordneten Paaren mit

.. math::
  A = \{ (x, \mu_A(x) \mid x \in X, \mu_A(x) \in [0,1]\}

Dabei ist :math:`\mu_A(x)` eine Funktion :math:`\mu_A: X \rightarrow [0,1]`, die den Grad angibt zu dem ein Element :math:`x \in X` in der Menge A enthalten ist. :math:`\mu_A(x)` heißt Zugehörigkeitsfunktion von A. Die Gesamtheit aller Fuzzy-Mengen über X bezeichnen wir mit F(X).

**Interpretation**: Sei :math:`x \in X`. :math:`\mu_A(x) = 0` keine Zugehörigkeit, :math:`\mu_A(x) = 1` volle Zugehörigkeit. :math:`0 < \mu_A(x) < 1` fließender Übergang.

**Bemerkung**: Jede gewöhnliche (Crisp) Menge kann als spezielle Fuzzy-Menge aufgefasst werden.



Darstellung von Fuzzy-Mengen
----------------------------

**Bsp**: "Groß" als eiegenschaft einer bestimmten Menge von Individuen (mit Parametern a,b und a < b )

.. math::
  |x| =
    \left\{
      \begin{array}{lll}
        0  & \mbox{falls } x \le a \\
        \frac{x - a}{b - a} & \mbox{falls } a < x < b \\
        1 & \mbox{falls } x \ge b
      \end{array}
    \right.

Mögliche Interpretation der Zugehörigkeitsfunktion
--------------------------------------------------

- als Grad zu dem ein Element zu einer Menge gehört
- als Grad zu dem ein Element eine für diese Menge charakteristische Eigenschaft besitzt
- als Grad der Möglichkeit, dass ein Element in dieser Menge liegt
- als Möglichkeitsgrad zudem eine Aussage zutrifft

Träger der Fuzzy-Menge
----------------------

Der Träger einer Fuzzy-Menge A über X ist

.. math::
  supp_A :=_{df} \{x \in X \mid \mu_a(x) > 0 \}

Eine Vereinfachung für die Implementierung: ein abgeschlossenes statt zwar beschränktes aber offenes Interval.


Höhe
-----

Die Höhe eine unscharfen Menge A über X: :math:`hqt_A :=_{df} \mu_A(x)`

normalisierte Fuzzy-Menge
-------------------------

.. math::
  A_{normalisiert} \Leftrightarrow hgt(A) = 1



Konvexe Fuzzy-Menge
-------------------

Eine Fuzzy-Menge A über :math:`\mathscr{R}` heißt konvex, wenn

.. math::
  \forall a,b,c \in \mathscr{R}: a \le b \le c \Rightarrow \mu_A(b) \ge min(\mu_A(a), \mu_A(c))



unscharfe Zahl
--------------

Eine Fuzzy-Menge A über :math:`\mathscr{R}` heißt unscharfe Zahl, falls A konvex ist und es genau eine Zahl a gibt mit :math:`\mu_A(a) = 1`



:math:`\alpha`-Schnitt
----------------------

.. math::
  A^{\ge a} = \{ x \in X \mid \mu_A(x) \ge a \} \text{ mit } \alpha \in (0, 1]

Für :math:`\alpha = 0`, dann nehmen wir den Träger als Schnitt: :math:`A^{\ge 0} = supp(A)`