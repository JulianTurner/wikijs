---
title: Finite Automaton
description: Finite Automaton (FA)
published: true
date: 2021-11-28T11:51:28.054Z
tags: graphen, formale sprache
editor: markdown
dateCreated: 2021-11-28T11:29:07.750Z
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


Finite Automaton können mit [gerichteten Graphen](/formaleBeschreibung/graphen/gerichtete-ungerichtete-graphen#gerichtete-graphen) vom Typ [Multigraph](/formaleBeschreibung/graphen/graphenTypen#multigraph) dargestellt werden.

## Anwendung

- [DFA](/formaleBeschreibung/formaleSprachen/dfa)
- [NFA](/formaleBeschreibung/formaleSprachen/nfa)