*********
Variablen
*********

Atome
=====

Identifikatoren (Atome), die mit ? beginnen werden Variablen assoziiert. Variablen ( mit Ausnahme von gleichen Variablen) brauchen nicht (und können nicht)  vor dem ersten Benutzen definiert werden.
Die Wertezuweisung funnktioniert durch eine Bind-Funktion, z.B. bind ?x "The value"

Globale Variablen
=================

Konstruktionsvorschrift:
------------------------
(defglobal [?<global-name> = <value>])

Namen in globalen Variablen müssen mit * beginnen und enden (?*x*)

Fuzzy globale Variable
======================

Konstruktionsvorschrift für Objekte der Klasse Fuzzy-Variable
(FuzzyVariable string m double UODlower)

Fuzzy Sets
==========

Wertezuweisung (eine Mehtode der Klasse Fuzzy-Variable)
(?<global-name> addTerm string term, FuzzySet fset)

fset ist ein Obejkt der Klasse FuzzySet, als Objekt jann man beliebige Fuzzy-Mengen definieren oder eine der typischen Formen hier als Unterklasse definieren.

z.B. (?*tempFVar* addTerm "cold" (new TriangleFuzzySet 22,0 25,0 28,0))