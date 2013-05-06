Einleitung
=================

Datenmodellierung
=================

Datenbankdefinitionssprachen
============================

ER-Modell
=========

Datenbankmodell
---

- Sprache, in der Schemata beschrieben werden (z.B. UML, ER-Diagramm)
- legt fest:
    - statische Eigenschaften: Objekte, Beziehungen, Datentypen
    - dynamische Eigenschaften: Operationen, Beziehungen zwischen Operationen
    - Integritätsbedingungen für Objekte, Operationen und Beziehungen zwischen diesen
- Semantikfestlegung
    - Trägermengen für Datentypen: `μ`
    - `μ(integer) = ℤ`
    - `μ(string) = C* (C={a-zA-Z})`
    - `μ(set(z))=2^(μ(z))`
    - `μ(tuple(z_1,...,z_n))=μ(z_1)×...×μ(z_n)`
    - `σ` ist Funktion, die einer Variable den aktuellen Zustand zuordnet
    - ??? (S.10)

ER-Modell
---

- Modellierungskonzepte
    - `μ(E)` - Menge der möglichen Entities vom Typ E
    - `σ_i(E)` - Menge der aktuellen Entities vom Typ E in einem Zustand `σ_i`; Index weglassen wenn eindeutig
- Kardinalitäten
    - Standardkardinalität
      - ER-Notation: `a:b` (umgedrehte Notation als Teilnehmerkardinalität)
    - Teilnehmerkardinalität
      - ER-Notation: `[min, max]`
      - Text-Notation: `R(E1[a, b], E2[c, d])`, E1 besitzt min a und max b Beziehungen zu E2; E2 besitzt min c und max d Beziehungen zu E1
      - Erweiterungen: Spezialisierung, Partitionierung, Generalisierung, Aggregierung, Assoziation

