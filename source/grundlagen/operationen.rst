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
