---
title: Typ 2 Sprache, kontextfreie Sprache
description: 
published: 1
date: 2021-12-17T17:10:48.527Z
tags: formale sprache
editor: markdown
dateCreated: 2021-12-16T20:41:09.094Z
---

# Typ 2 Sprache, kontextfreie Sprache

## Produktionssystem Einschränkungen:

- rechte Seite ist nicht kürzer als linke Seite (wg. Typ 1 Grammatik)
- linke Seite nur eine Variable

## Formen
- Chomsky Normalform
  - Variable -> Variable Variable
  - Variable -> Terminalsymbol
- Greibach Normalform
  - Variable -> Terminalsymbol + (0 oder mehr) Variablen

## Wortproblem lösbar mit
- CYK-Algorithmus
- Push-Down-Automat

## Beispiel

- $L = \{u\overleftarrow{u}:u \in \{a,b\}^* \backslash \{\epsilon\}\}$, wobei $\overleftarrow{u}$ $u$ rückwärts gelesen bedeutet
- - $L = \{a^nb^n:n \in \mathbb{N}\}$

## Abschlusseigenschaften

Mit $L_1, L_2 \in \Sigma^*$

### Abgeschlossen gegenüber

| Eigenschaft      | Name |
| :----------- | :----------- |
| $L_1 \cup L_2$ | Vereinigung |
| $L_1L_2$ | Produkt|
| $L_1^*$ | Kleene Stern |

### Nicht abgeschlossen gegenüber

| Eigenschaft      | Name |
| :----------- | :----------- |
| $L_1 \cap L_2$ | Durchschnitt |
| $\overline{L_1} := \Sigma^* \backslash L_1$ | Komplement |