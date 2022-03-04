---
title: Definition einer formalen Sprache
description: 
published: true
date: 2021-11-27T18:26:24.960Z
tags: formale sprache
editor: markdown
dateCreated: 2021-11-27T18:20:31.777Z
---

# Definition einer formalen Sprache
## Das Alphabet

Aus dem Alphabet $\Sigma$ können die folgenden Mengen gebildet werden:

- $\Sigma^+$ (sprich Sigma-Plus) = Menge aller <u>nicht leeren</u> Zeichenketten die aus dem Alphabet gebildet werden können
- $\Sigma^*$ (sprich Sigma-Stern) = $\Sigma^+$ + die leere Zeichenkette $\varepsilon$ (sprich Epsilon)
  - $w \in \Sigma^*$ heißen auch Wörter
  
## Konkatenation Operation auf $\Sigma^*$

Wenn $u, v \in \Sigma^*$ dann ist $uv \in \Sigma^*$  die Zeichenkette, die durch Konkatenation von $u$ und $v$ entsteht.

$u$ konkateniert mit $\varepsilon$ = $u$

$u$ und $v$ können selbst bereits Kombination von Buchstaben und Wörter des Alphabets sein.

## Formale Sprache über dem Alphabet $\Sigma$

- ist eine Teilmenge von $\Sigma^*$
  - bestimmt beispielsweise durch formale Regeln
- Elemente einer formalen Sprache heißen auch *Wörter* der Sprache
- Beispiele:
  - grammatisch korrekte Sätze der Deutschen Sprache
  - grammatisch korrekte Programme einer Programmiersprache