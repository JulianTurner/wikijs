---
title: Typ 1 Sprache, kontextsensitive Sprache
description: 
published: true
date: 2021-11-27T20:52:08.745Z
tags: formale sprache
editor: markdown
dateCreated: 2021-11-27T20:52:01.891Z
---

# Typ 1 Sprache, kontextsensitive Sprache

## Produktionssystem Einschränkungen:

- rechte Seite ist nicht kürzer als linke Seite

## Formen
- Kuroda Normalform
- Révész Normalform
  
## Wortproblem lösbar mit
- Linear beschränkte Turing-Maschiene

## Beispiel

- $L = \{a^nb^nc^n:n \in \mathbb{N}\}$
- $L = \{a^nb^nc^nd^n:n \in \mathbb{N}\}$

## Abschlusseigenschaften

Mit $L_1, L_2 \in \Sigma^*$

### Abgeschlossen gegenüber

| Eigenschaft      | Name |
| :----------- | :----------- |
| $L_1 \cup L_2$ | Vereinigung |
| $L_1 \cap L_2$ | Durchschnitt |
| $L_1L_2$ | Produkt|
| $L_1^*$ | Kleene Stern |
| $\overline{L_1} := \Sigma^* \backslash L_1$ | Komplement |