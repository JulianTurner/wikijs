---
title: Typ 3 Sprache, reguläre Sprache
description: 
published: true
date: 2021-11-28T11:52:58.043Z
tags: formale sprache
editor: markdown
dateCreated: 2021-11-27T20:03:19.246Z
---

# Typ 3 Sprache, reguläre Sprache

## Produktionssystem Einschränkungen:

- rechte Seite ist nicht kürzer als linke Seite (wg. Typ 1 Grammatik)
- linke Seite nur eine Variable (wg. Typ 2 Grammatik)
- Regeln vom Typ
  - Variable -> Terminalsymbol
  - Variable -> Terminalsymbol Variable
  
## Wortproblem lösbar mit
- [NFA](/formaleBeschreibung/formaleSprachen/nfa) (Nondeterministic Finite Automaton)
- [DFA](/formaleBeschreibung/formaleSprachen/dfa) (Deterministic Finite Automaton)

NFA kann in DFA umgewandelt werden.
## Beispiel

- $L = \{a^n:n \in \mathbb{N}\}$

## Abschlusseigenschaften

Mit $L_1, L_2 \in \Sigma^*$

### Abgeschlossen gegenüber

| Eigenschaft      | Name |
| :----------- | :----------- |
| $L_1 \cup L_2$ | Vereinigung |
| $L_1 \cap L_2$ | Durchschnitt |
| $\overline{L_1} := \Sigma^* \backslash L_1$ | Komplement |
| $L_1L_2$ | Produkt|
| $L_1^*$ | Kleene Stern |