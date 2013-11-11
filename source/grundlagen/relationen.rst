Fuzzy-Relationen (binär)
========================

Definition
----------

Sei Y ein Grundbereich der Form :math:`Y = X_1 \times X_2` also :math:`Y ) \{(x,y) \mid x \in X_1 \wedge y \in X_2 \}`. Eine unscharfe (fuzzy) binäre Realtion R über Y ist eine Fuzzy-Teilmenge von Y, also :math:`R \in F(Y)`.

Beispiel
--------

Eine Relation "ungefähr gleich", sei gegeben als :math:`X_1 = X_2 = \mathbb{N}, x \in X_1, y \in X_2`, so ist :math:`\mu_{ungefähr gleich}(x,y) = max \{ 0, 1 - a \mid x - y \mid\}` mit Parameter a > 0.

.. todo:: 1. Bild einfügen




Verallgemeinerung von Fuzzy-Relationen
=======================================

Definition
------------

Seien :math:`X_1, X_2 \subseteq \mathbb{R}` und :math:`A \in F(X_1)` und :math:`B \in F(X_2)` zwei Fuzzy-Mengen. Dann ist :math:`R \in F(X_1 \times X_2)` eine Fuzzy-Relation über A und B, wenn gilt:

.. math::
  \mu_B(x,y) &\le \mu_A(x) \text{ und } \\
  \forall (x,y) \in X_1 \times X_2:  \mu_B(x,y) &\le \mu_B(y)




Verknüpfungen (Verkettungen) von Fuzzy-Relationen
==================================================

Definition
----------

Seien :math:`K \in F(X_1 \times X_2), S \in F(X_2 \times X_3)`, so ist die Verkettung :math:`R \circ S` definiert durch

:math:`\mu_{R \circ S}(x,z) =_{def.} sup_{y \in X_2} min \{ \mu_R(x,y), \mu_S(y,z) \}`

Beispiel
--------

.. todo:: 2. Bild einfügen



Allgemeine Fuzzy-Relationen
===========================

Produkt: :math:`R \circ_{\cdot} S`
----------------------------------

.. math::
  \mu_{R \circ_{\cdot} S}(x,z) := sup_{y \in X_2} \{ \mu_R(x,y) \cdot \mu_S(y,z) \}

Average:  :math:`R \circ_{\cdot} S`
-----------------------------------

.. math::
  \mu_{R \circ_{av} S}(x,z) := sup_{y \in X_2} \{ \frac{1}{2} (\mu_R(x,y) + \mu_S(y,z)) \}




Projektionen
============

Definition
----------

Sei :math:`R \in F(X_1 \times X_2)` und seien zwei Projektionen :math:`pr_1(R), pr_2(R)` gegeben als:

.. math::
  &\forall x \in X_1: \mu_{pr_1(R)}(x) := sup_{y \in X_2} \{ \mu_R(x,y) \} \\
  &\forall y \in X_2: \mu_{pr_2(R)}(y) := sup_{x \in X_1} \{ \mu_R(x,y) \}

Die totale Projektion :math:`pr_{Total}(R)` ist dann definiert als:

.. math::
  \mu_{pr_{Total}} := sup_{x \in X_1} sup_{y \in X_2} \{ \mu (x,y) \}

.. todo:: Abbildung 3. Seite oben




Kartesisches Produkt
====================

Definition
----------

Seien :math:`A \in F(X_1), B \in F(X_2)`. Dann wird :math:`A \times B` definiert als:

.. math::
  \forall (x,y) \in X_1 \times X_2: \mu_{A \times B}(x,y) := min \{ \mu_A(x), \mu_B(y) \}

Beispiel
--------



.. todo:: Abbildung 3. Seite mitte




Äquivalenzrelation
==================

Definition
----------

Eine binäre Funktion :math:`R = R(X,X)` heißt Äquivalenzrelation (similarity relations), falls sie folgendes ist:

- reflexiv, wenn :math:`\mu_R(x,x) = 1` f.a. :math:`x \in X`
- syemtrisch, wenn :math:`\mu_R(x,y) = \mu_R(y,x)` f.a. :math:`x,y \in X`
- transitiv (sup min-transitiv), wenn :math:`sup_{z \in X} min \{ \mu_R(x,z), \mu_R(z,y) \}` f.a. :math:`x,y,z \in X`

Äquivalenzrelationen sind gut geeignet zur Modellierung von unscharfen Nachbarschaftsbeziehungen (Weil sie die Anforderung einer Abstandsnorm (Metrik) erfüllen).



Verallgemeinerung von :math:`\cup` und :math:`\cap` - Operatoren
=================================================================

T-Normen und T-Conormen (S-Normen)
----------------------------------

Gernerelle Voraussetzung: :math:`\mu_{A \cap B}` soll elementweise zu berechnen sein aus :math:`\mu_A` und :math:`\mu_B`.