---
title: Chomsky-Hierarchie
description: 
published: 1
date: 2021-12-18T08:20:47.255Z
tags: formale sprache
editor: markdown
dateCreated: 2021-12-16T20:40:30.908Z
---

- # Chomsky-Hierarchie

## Chomsky-Typ
- Eine Sprache kann mit unterschiedlichen Grammatiken und Typen spezifiziert werden
- Chomsky-Typ einer Sprache ist der **höchste** Typ einer Grammatik, welche diese Sprache produziert

## Chomsky-Hierarchie für Grammatiken
Für jeden Grammatik Typ gelten zusätzliche [Epsilon Regeln](/formaleBeschreibung/formaleSprachen/chomsky-hierarchie#%CE%B5varepsilon%CE%B5-regeln).

### Typ 0 Grammatik
- hat keine Regeleinschränkung für des Produktionssystems
  - Wörter können im Verlauf der Ableitung länger werden als das letztendlich produzierte Wort

### Typ 1 Grammatik: kontextsensitive Grammatik
- für jede Regel gilt: rechte Seite nicht kürzer linke Seite
- siehe auch [Typ 1 Sprache, kontextsensitive Sprache](/formaleBeschreibung/formaleSprachen/typ-1-sprache)

### Typ 2 Grammatik: kontextfreie Grammatik
- Regel von Typ 1 Grammatik (siehe oben)
- auf linker Seite ein nicht Terminal-Symbol
- auf rechter Seite beliebige Kombination von Terminal- und nicht Terminal-Symbolen
- siehe auch [Typ 2 Sprache, kontextfreie Sprache](/formaleBeschreibung/formaleSprachen/typ-2-sprache)

### Typ 3 Grammatik: reguläre Grammatik
- Regeln von Typ 2 Grammatik (siehe oben)
- rechte Seite entweder ein Terminal Symbol oder Terminal-Symbol + Nicht Terminal-Symbol
- siehe auch [Typ 3 Sprache, reguläre Sprache](/formaleBeschreibung/formaleSprachen/typ-3-sprache)

## $\varepsilon$-Regeln
Entgegen der Regel "rechte Seite nicht kürzer linke Seite" führt man für für alle Grammatiken neue Regeln ein, bei denen das Start-Symbol S auf $\varepsilon$ abgeleitet werden darf.

Für Regeln von Typ 2, 3 und 4 wird außerdem für jedes Terminal-Symbol je eine Ableitung auf $\varepsilon$ eingeführt.
Die Epsilon-Regeln können anschließend eliminiert werden, in dem Regel-Permutationen gebildet werden, bei denen auf der rechten Seite an verschiedenen Stellen die auf $\varepsilon$ ableitbaren Variablen entfernt werden (ausgenommen die Regel Startsymbol -> $\varepsilon$).

## Chomsky-Hierarchie für Sprachen

Eine formale [Sprache](/formaleBeschreibung/formaleSprachen/grammatik-sprache#sprache) $L$ ist vom Typ $i$, wenn es eine Grammatik vom Typ $i$ gibt welche die formale Sprache bildet.

Eine Sprache kann von einem höheren Typ sein als eine Grammatik die sie beschreibt, wenn es eine weitere Grammatik mit höherem Typen gibt, welche die gleiche Sprache bildet.

![chomsky-gramatik-sprachen-hierarchie.png](/fom/semester-1/chomsky-gramatik-sprachen-hierarchie.png)