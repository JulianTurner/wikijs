---
title: Typ 1 Sprache, kontextsensitive Sprache
description: 
published: 1
date: 2021-12-17T17:12:45.250Z
tags: formale sprache
editor: markdown
dateCreated: 2021-12-16T20:41:03.313Z
---

# Typ 1 Sprache, kontextsensitive Sprache

## Produktionssystem Einschränkungen:

- rechte Seite ist nicht kürzer als linke Seite

## Formen
- Kontext-Form (einzelne Produktion)
  - (optional) Variable(n) +  Variable + (optional) Variable(n)
->  (optional) Variable + Variable(n) oder Terminalzeichen + (optional) Variablen(n)

- Kuroda Normalform
  - Variable -> Terminal
  - Variable -> Variable
  - Variable -> Variable Variable
  - Variable + Variable -> Variable + Variable
- Révész Normalform
  - Variable -> Terminal
  - Variable -> Variable
  - Variable -> Variable Variable
  - Variable A + Variable B -> Variable X + Variable B (B ist Kontext)
  - Variable A + Variable B -> Variable A + Variable X (A ist Kontext)
  
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