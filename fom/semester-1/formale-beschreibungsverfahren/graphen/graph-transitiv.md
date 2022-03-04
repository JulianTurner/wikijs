---
title: Transitiv abgeschlossen, transitive Hülle, Clique
description: 
published: 1
date: 2022-03-04T12:48:02.370Z
tags: graphen
editor: markdown
dateCreated: 2021-12-16T20:41:40.348Z
---

# Transitiv abgeschlossen, transitive Hülle, Clique
## Graph transitiv abgeschlossen
Zwischen zwei Knoten die <u>über mehrere Kanten verbunden</u> sind, gibt es auch eine Kante welche die Knoten <u>direkt</u> verbindet.

Bei ungerichteten Graphen ist die Kanten-Richtung egal.
Bei gerichteten Graphen muss auf die Kanten-Richtung geachtet werden.

## Transitive Hülle
Eine transitive Hülle ist ein neuer Graph bestehend aus
- den gleichen Knoten wie die Knoten des original Graphen
- den Kanten
  - aus dem original Graph
  - weiteren Kanten, welche eingeführt werden um dem Graph die Eigenschaft *transitiv abgeschlossen* (siehe oben) zu geben

![transitive-huelle.png](/fom/semester-1/formale-beschreibungsverfahren/transitive-huelle.png)
(Hier: in Grün die übernommenen original Knoten, in Rot die übernommenen original Kanten, in Blau die neu eingeführte Kante für die transitive Abgeschlossenheit)

## Vollständiger ungerichteter Graph
In einem vollständigen ungerichteten Graph ist jeder Knoten mit jedem anderen Knoten via Kanten verbunden.

## Clique
Ist ein Teilgraph eines einfachen ungerichteten Graphen, der vollständig ist (siehe oben).

![clique.png](/fom/semester-1/formale-beschreibungsverfahren/clique.png)