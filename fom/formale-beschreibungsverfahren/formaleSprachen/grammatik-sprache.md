---
title: Definition einer Grammatik und Sprache
description: 
published: true
date: 2021-11-27T18:38:54.791Z
tags: formale sprache
editor: markdown
dateCreated: 2021-11-27T18:38:04.342Z
---

# Definition einer Grammatik und Sprache
## Grammatik
Eine Grammatik $G = (V,\Sigma,P,S)$ besteht aus

- $V$ = endliche Menge von Variablen/nicht Terminalsymbolen
- $\Sigma$ = endliche Menge von Terminalsymbolen
- $P$ = Produktionssystem
  - enthält Regeln in der Form *linke Seite* -> *rechte Seite*
  - beide Seiten bestehen aus Zeichenketten aus dem Alphabet $V \cup \Sigma$
  - *linke Seite* ist nicht leer
- $S$ = eine Startvariable

## Sprache
- $L(G)$ = Sprache welche via Produktionssystem einer Grammatik $G$ gebildet wird