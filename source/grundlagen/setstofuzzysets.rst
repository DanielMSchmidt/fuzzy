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

**Idee**: Befragung von Kinderärzten und die erweiterung der charakteristischen Funktion durch "Zugehörigkeitsfunktion".

**Graphisch**:
  .. image:: http://i.imgur.com/n4WBemF.jpg
    :width: 400
    :height: 300

**Bemerkung**: die definierende Eigenschaft einer Fuzzy-Menge wird allgemein linguistisch festgelegt. (z.B. "etwa 10",....)

**Modellierung**: linguistischer Begriff :math:`\rightarrow` Zugehörigkeitsfunktion