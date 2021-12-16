---
title: Teilgraph, Teilbaum
description: Teilgraphen und Teilbäume
published: 1
date: 2021-12-16T20:54:24.647Z
tags: graphen
editor: markdown
dateCreated: 2021-12-16T20:42:05.356Z
---

# Teilgraph, Teilbaum

## Teilgraph eines (un)gerichteten Graphen
Ein Teilgraph eines (un)gerichteten Graphen ist ein (un)gerichteter Graph, dessen...
- <u>Knoten</u> eine <u>Teilmenge</u> der Knoten des original Graphen sind
- <u>Kanten</u> eine <u>Teilmenge</u> der Kanten des original Graphen sind
- <u>Zustandsübergänge</u> eine <u>Teilmenge</u> der Zustandsübergänge des original Graphen sind.
Dabei wird darauf geachtet, das die Start und Endpunkte in der neuen Knoten Teilmenge enthalten sind.

## Teilbaum
Ein Teilbaum ist ein Teilgraph eines [Baumes](/formaleBeschreibung/graphen/dag-tree#tree-baum).
Ein <u>vollständiger Teilbaum</u> hat keine Knoten die Startpunkte von Kanten sind, deren Zielknoten außerhalb des Teilbaums liegen.
Ein <u>unvollständiger Teilbaum</u> hat Knoten die Startpunkt von Kanten sind, deren Zielknoten außerhalb des Teilbaums liegen.

![teilbaum.png](/fom//teilbaum.png)




