---
title: Reale Problemstellungen
published: 1
date: 2023-06-29T20:22:18.207Z
tags: 
editor: markdown
dateCreated: 2023-06-29T20:22:18.207Z
---

# Reale Problemstellungen

## Greedy-Algorithmus

- Greedy-Algorithmus: Algorithmus welcher immer die aktuell beste Lösung wählt (sucht nach lokalem Optimum)
- Vorgehen in Stufen

![Greedy-Algorithmus](/fom/semester-4/algorithmen-und-datenstrukturen/greedy-algorithmus.png)

### Dijkstra-Algorithmus

- Greedy-Algorithmus zur Bestimmung des kürzesten Weges in einem gewichteten Graphen
- Vorgehen:
  - Startknoten wird als aktueller Knoten gewählt
  - alle Nachbarknoten werden besucht und deren Distanz zum Startknoten wird berechnet
  - der Knoten mit der geringsten Distanz wird als aktueller Knoten gewählt
  - Schritte 2 und 3 werden wiederholt bis der Zielknoten erreicht wurde

> Der Dijkstra Algorithmus ist „greedy“, da er in jedem Schritt aus den möglichen Zielen das nächste wählt (=lokales Optimum).
{.is-info}

> Kann von Priority Queue unterstützt werden
{.is-info}

### Kruskal-Algorithmus

- Greedy-Algorithmus zur Bestimmung des minimalen Forrest in einem Graphen (wenn Graph zusammenhängend ist, dann ist das Ergebnis ein minimaler Spannbaum)
- Vorgehen:
  - alle Kanten werden nach Gewicht sortiert
  - die Kante mit dem geringsten Gewicht wird gewählt
  - die Kante wird in den Forrest aufgenommen, wenn sie keinen Kreis bildet
  - Schritte 2 und 3 werden wiederholt bis alle Knoten im Forrest sind

> Es wird immer die Kante mit dem geringsten Gewicht gewählt, die keinen Kreis bildet (=lokales Optimum), unabhängig davon, ob sie mit bisher erreichten Knoten verbunden ist
{.is-info}

### Huffman-Algorithmus

- Algorithmus zur Komprimierung von Daten
- Vorgehen:
  - alle Zeichen werden nach Häufigkeit sortiert
  - die zwei Zeichen mit der geringsten Häufigkeit werden zu einem Baum zusammengefasst
  - der Wert der Wurzel des Baums ist die Summe der Häufigkeiten der beiden zusammengefassten Knoten
  - Schritte 2 und 3 werden wiederholt bis alle Zeichen und Wurzeln zu einem Baum zusammengefasst wurden
  - der Baum wird durchlaufen und linke Kanten mit 0 und rechte Kanten mit 1 markiert
  - pro Zeichen wird das Codewort bestimmt, indem der Baum von oben nach unten durchlaufen wird -> Codewort = Zeichen der Pfade in auftretender Reihenfolge

Eigenschaften:

- Flexible Informationseinheiten: (Zeichen, Wörter, Sätze als kleinste Einheit verwendbar)
- Präfixfrei: kein Trennzeichen zwischen Codewörtern notwendig
- Optimal: minimale Ergebnislänge
- Verlustfrei: keine Information geht verloren

## Divide-and-Conquer-Algorithmus

- Algorithmus welcher ein Problem in kleinere Teilprobleme zerlegt
- Vorgehen:
  - Problem wird in kleinere Teilprobleme zerlegt
  - Teilprobleme werden gelöst
  - Lösungen werden zu einer Gesamtlösung zusammengefügt
- bsp. Merge-Sort und Quick-Sort

## Brute-Force-Algorithmus

- Algorithmus welcher den kompletten Lösungsraum durchprobiert
- bsp. Lineare Suche, Passwort Knacken

## Backtracking-Algorithmus

- Algorithmus welcher eine Tiefensuche im Lösungsraum durchführt, und bei einer Sackgasse zurückgeht
- Teile des Lösungsraums kann durch logische Schlussfolgerungen ausgeschlossen werden
- in der Regel rekursiv
- Zeitkomplexität: $O(m^h)$ m: Grad des Baumes, h: Höhe des Baumes
- bsp. Rat-in-a-Maze, Rucksack, Sudoku

## Approximations-Algorithmus

- Algorithmus welcher eine Lösung liefert, die nicht optimal ist, aber in akzeptabler Zeit berechnet werden kann

Approximations-Güte:

- Maximierungsproblem: $r_I =\frac{V*}{V(y)} c$
- Minimierungsproblem: $r_I =\frac{V(y)}{V*} c$
$I$ Eingabemenge
$V*$ Optimale Lösung
$V(y)$ Zielfunktion

> Eine optimale Lösung ist $r = 1$, eine approximierte Lösung ist $r > 1$
{.is-info}

### Traveling Salesman Heuristik

Nearest-Neighbor:

1. Beginne bei einem beliebigen Knoten
1. Wähle den nächsten Knoten, der noch nicht besucht wurde
1. Wiederhole Schritt 2 bis alle Knoten besucht wurden
1. Verbinde den letzten Knoten mit dem Startknoten

Nearest-Insertion:

1. Verbinde einige Knoten, für die sich eine schnelle exakte Route finden lässt
1. Füge einen neuen Knoten in die Kante ein, welche am nächsten an dem neuen Knoten ist
1. Wiederhole Schritt 2 bis alle Knoten besucht wurden

Minimum-Spanning-Tree:

1. Erstelle einen minimalen Spannbaum
1. Dupliziere alle Kanten => Multi-Graph
1. Mach Euler-Tour, bei Abzweigung immer die Kante mit dem geringsten Gewicht wählen
