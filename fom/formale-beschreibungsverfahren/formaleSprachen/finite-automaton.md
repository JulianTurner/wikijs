---
title: Finite Automaton
description: Finite Automaton (FA)
published: 1
date: 2021-12-17T17:17:24.528Z
tags: formale sprache, graphen
editor: markdown
dateCreated: 2021-12-16T20:40:43.349Z
---

# Finite Automaton

## Definition
Finite Automaton bestehen aus:

- einer endlichen Menge von Zuständen $Q$
- einem endlichen Alphabet $\Sigma$
- Zustandsübergangsfunktionen/ -relationen $\delta$
- <u>ein</u> Startzustand $q_0 \in Q$
  -  Im Graph wird der Startzustand mit einem <u>großen Punkt</u> markiert.
- <u>eine Menge von</u> Endzuständen $F \subseteq Q$ (Final States)
  - Im Graph wird jeder Endzustand mit einem <u>umkreisten Punkt</u> markiert.


Finite Automaton können mit [gerichteten Graphen](/fom/formale-beschreibungsverfahren/graphen/gerichtete-ungerichtete-graphen#gerichtete-graphen) vom Typ [Multigraph](/fom/formale-beschreibungsverfahren/graphen/graphenTypen#multigraph) dargestellt werden.

## Anwendung

- [DFA](/fom/formale-beschreibungsverfahren/formaleSprachen/dfa)
- [NFA](/fom/formale-beschreibungsverfahren/formaleSprachen/nfa)