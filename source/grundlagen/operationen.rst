Operationen auf Fuzzy-Mengen
=============================

Schnitt
-------

:math:`A \cap B` ist definiert als Fuzzy-Menge mit

.. math::
  \mu_{A \cap B}: X \rightarrow [0,1], \mu:{A \cap B} = min(\mu_A(X), \mu_B(X))



Vereinigung
------------

:math:`A \cup B` ist definiert als Fuzzy-Menge mit

.. math::
  \mu_{A \cup B}: X \rightarrow [0,1], \mu:{A \cup B} = max(\mu_A(X), \mu_B(X))



Komplement
----------

:math:`A \backslash B` ist definiert als Fuzzy-Menge mit

.. math::
  \mu_{\overline{A}}: X \rightarrow [0,1], \mu:{\overline{A}}(x) = 1 - \mu_A(X)


Eigenschaften dieser Operationen
=================================

Seien A,B,C Fuzzy-Mengen und schrieben wir statt :math:`max(\mu_A(x), \mu_B(x))x` kurz :math:`A \cup B`.
Es gelten für :math:`\cup` (und analog für :math:`\cap`):

- Kommmutativität :math:`A \cup B = A \cup B`
- Assoziativität :math:`(A \cup B) \cup C = A \cup (B \cup C)`
- Indempotenz: :math:`A \cup A = A`
- :math:`\forall A \in F(X): \emptyset \subseteq A \subseteq X` mit :math:`\mu_A = 0` und :math:`\mu_X = 1`
- :math:`A \subseteq B \cup B \subseteq A \Rightarrow A = B`
- :math:`A \cup \emptyset = A`
- :math:`A \cup X = X`
- :math:`A \cap \emptyset = \emptyset`
- :math:`A \cap X = A`
- Distributivität :math:`A \cup (B \cap C) = (A \cup B) \cap (A \cup C)`
- Komplettabbildung: :math:`\overline{\overline{A}} = A`

Es gilt **NICHT**:

- :math:`A \cup \overline{A} = X`
- :math:`A \cap \overline{A} = \emptyset`

Allgemeine Vereinigung und allgemeiner Schnitt
-----------------------------------------------

Seien undendlich viele Fuzzy-Mengen gegeben als: :math:`\{ A_i , i \in I \}` mit I als Indexmenge

.. math::
  &C = \bigcup_{i \in I} A_i, \mu_C (x) =_{def.} sup_{i \in I} \mu_{A_i}(x) \\
  &C = \bigcap_{i \in I} A_i, \mu_C (x) =_{def.} inf_{i \in I} \mu_{A_i}(x)
