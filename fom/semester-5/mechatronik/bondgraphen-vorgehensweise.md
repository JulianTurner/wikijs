---
title: Bondgraphen Vorgehensweise
published: 1
date: 2023-11-15T20:16:44.207Z
tags: 
editor: markdown
dateCreated: 2023-11-15T20:16:44.207Z
---

# Bondgraphen Vorgehensweise

## Mechanische Bondgraphen

1. Für jede unterschiedliche Geschwindigkeit (SE, I(m), SF) wird eine 1-Junction benötigt
1. Binde jede 1-Port Quelle an die 1-Junction an
1. Binde restliche 1-Port Elemente (R, C) an eine 0-Junction an
1. Binde 0-Junction and die entsprechende 1-Junction an
1. Allen Leistungsbonds (mit halb-Pfeil) eine Richtung geben
1. Alle 1-Junctions mit v=0 streichen
1. Vereinfache den Bondgraphen
1. Kausalitätsbits setzen (Feder (C) schiebt es weg, Dämpfer (R) egal, Masse (I) zieht es an)
1. ???
1. Profit

## Elektrische Bondgraphen

1. Für jedes unterschiedliches Potential (Spannung) wird eine 0-Junction benötigt
1. Binde 1-Port Elemente (R, C, I, SE, SF) an eine 1-Junction an und diese mit 0 Junctions verbinden
1. Allen Leistungsbonds (mit halb-Pfeil) eine Richtung geben
1. Falls 0 Potential bekannt -> alle 0 Junctions mit 0 Potential streichen
1. Falls 0 Potential unbekannt -> beliebiges Potential als 0 Potential festlegen
1. Vereinfache den Bondgraphen
1. Kausalitätsbits setzen (Kondensator (C) schiebt es weg, Spule (I) zieht es an)
1. ???
1. Profit
