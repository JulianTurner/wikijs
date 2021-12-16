---
title: Pfad, Kreis, Schleife, Zyklus
description: Pfade, Kreise, Schleifen und Zyklen
published: true
date: 2021-11-27T17:52:47.323Z
tags: graphen
editor: markdown
dateCreated: 2021-11-26T14:45:09.071Z
---

# Pfad, Kreis, Schleife Zyklus

# Pfad
Ein Pfad ist eine Folge von Kanten.
Im Pfad-Verlauf muss der Endpunkt einer Kante der Startpunkt einer anderen Kante sein.
Bei gerichteten Graphen sind die Kanten-Richtungen zu beachten (T Tail -> H Head).

# Kreis
Ein Kreis ist ein geschlossener Pfad.
D. h. ein Knoten ist immer sowohl Start- als auch Endknoten.
Bei gerichteten Graphen lässt sich noch genauer sagen: ein Knoten ist immer Head und Tail.

# Schleife
Eine Schleife ist ein Kreis bei dem Start- und Endknoten der gleiche Knoten ist.
Eine Schleife hat immer nur eine Kante.

# Zyklus
Ein Zyklus ist ein Kreis ohne wiederholte Knoten/Kanten.
D. h. eine Schleife kann nie ein Zyklus sein.

## Beispiele:

### Ungerichteter Graph:

![pfad-zyklus-schleife-ungerichtet.png](/pfad-zyklus-schleife-ungerichtet.png)

### Gerichteter Graph

![pfad-zyklus-schleife-gerichtet.png](/pfad-zyklus-schleife-gerichtet.png)