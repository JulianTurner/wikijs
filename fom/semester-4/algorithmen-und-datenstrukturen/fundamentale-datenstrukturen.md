---
title: Fundamentale Datenstrukturen
published: 1
date: 2023-04-19T19:10:09.207Z
tags: 
editor: markdown
dateCreated: 2023-04-19T19:10:09.207Z
---

# Fundamentale Datenstrukturen

> Eine Datenstruktur ist ein Objekt welches Daten in einer bestimmen Art und Weise speichert und organisiert.

Grundlegende Datenstrukturen sind:

- Record (Datensatz) -> Feste Anzahl unterschiedlicher Datentypen
- Array -> Sequentielle Datenstruktur vieler gleichartiger Datentypen mit fester Positionierung (feste Größe)
- Vector -> Array mit dynamischer Größe

## Linked List

Sequentielle Datenstruktur zur Speicherung vieler gleichartiger Datentypen in der jedes Element auf seinen nächsten Nachbarn verweist

- Größe ist nicht fest
- Elemente können verschoben werden

Zeitkomplexität:

- Einfügen: O(1)
- Löschen: O(1)
- Zugriff: O(n)

Weitere Typen:

- Circular List
  - Letztes Element verweist auf erstes Element
- Doubly Linked List
  - Jedes Element verweist auf seinen Nachbarn und seinen Vorgänger
- Double Circular Linked List
  - Jedes Element verweist auf seinen Nachbarn und seinen Vorgänger und das letzte Element verweist auf das erste Element

## Stack

Sequentielle Datenstruktur zur Speicherung vieler gleichartige Datentypen, in welcher Elemente nach dem LIFO (Last In First Out)-Prinzip verwaltet werden.

- wird Hardwareseitig implementiert

Zeitkomplexität:

- Push: O(1)
- Pop: O(1)
- Top: O(1)

## Queue

Sequentielle Datenstruktur zur Speicherung vieler gleichartiger Datentypen, in welcher Elemente nach dem FIFO (First In First Out)-Prinzip verwaltet werden

- verhält sich wie eine Schlange

Zeitkomplexität:

- Push: O(1)
- Pop: O(1)
- Front: O(1)

## Priority Queue

Sequentielle Datenstruktur zur Speicherung vieler gleichartige Datentypen, die es erlaubt die Sortierfunktion der Elemente selbst zu wählen

- Elemente werden nach Priorität gepoppt

Zeitkomplexität:

- Push: O(log n)
- Pop: O(log n)
- Top: O(1)

## Tree

Zweidimensionale Datenstruktur zur Speicherung vieler gleichartiger Datentypen, in welcher Elemente (Knoten) über Kanten mit 0 bis 1 Vorgängern verbunden sind sowie 0 bis n Nachfolgern

- Wurzelknoten (Root) hat keine Vorgänger
- Blattknoten haben keine Nachfolger

![Tree](https://miro.medium.com/v2/resize:fit:1950/1*PWJiwTxRdQy8A_Y0hAv5Eg.png)

Zeitkomplexität:

- Einfügen: O(log n)
- Löschen: O(log n)
- Zugriff: O(log n)

Weitere Begriffe:

- Wald (Forrest)
  - Menge von nicht zusammenhängenden Bäumen
- Geordneter Baum (Ordered Tree)
  - Reihefolge der Kinder ist eindeutig festgelegt
- Ebene (Level)
  - Anzahl der Kanten von der Wurzel bis zum bestimmten Knoten
- Höhe (Height)
  - Maximale Ebene aller Knoten eines Baumes
- Länge (Length)
  - Summe aller Ebenen aller Knoten eines Baumes
  - interne Pfadlänge -> Nur Knoten  die keine Blätter sind
  - externe Pfadlänge -> Nur Blätter
- Mehrwege (Multiway) Baum mit Rang (order) m
  - Baum in welcher jeder Knoten m Kinder hat

## Binary Tree

Geordneter Mehrwege-Baum mit Rang 2, d.h. jeder Knoten hat exakt maximal zwei Kinder

- Full -> Jeder innere Knoten hat genau zwei Kinder
- Complete -> Jeder Ebene ist von links nach rechts befüllt, neue Ebenen werden erst befüllt wenn alle vorherigen Ebenen keine freien Plätze mehr haben
- Perfect -> Vollständiger Baum mit vollständigen Ebenen

### Theoreme

- Jedes Paar von Knoten ist mit genau einem Pfad verbunden
- Ein Baum mit n Knoten hat genau n-1 Kanten
- Ein Binärbaum mit n inneren Knoten hat genau n+1 äußere Knoten
- Die externe Pfadlänge eines vollen Binärbaumes mit n inneren Knoten ist genau 2n **größer** als die interne Pfadlänge
- Die Höhe h eines perfekten Binärbaums mit 𝑁 äußeren Knoten ist $log_2(n)$

### Traversal Verfahren

- Preorder (Tiefensuche)
  - Wurzel -> Links -> Rechts
  - Create / Copy tree
- Postorder
  - Links -> Rechts -> Wurzel
  - Delete tree
- Inorder
  - Links -> Wurzel -> Rechts
  - Binäre Suchbäume
- Levelorder (Breitensuche)
  - Ebene für Ebene
  - Graphen-Theorie

## Graphen

Datenstruktur zur Speicherung vieler gleichartige Datentypen, in welcher Elemente (Knoten) über Kanten mit 1 bis n anderen Elementen verbunden sind [siehe](/fom/semester-1/formale-beschreibungsverfahren/graphen/gerichtete-ungerichtete-graphen.md)

- Jeder Baum ist auch ein Graph

Repräsentation:

- Nachbarschaftsliste
  - Jeder Knoten hat eine Liste mit allen Nachbarn
  - Platzsparend
  - Einfaches Hinzufügen
  - Langsame Suche (O(n))
  - nur für ungerichtete Graphen
- Nachbarschaftsmatrix
  - Gibt durch binäre Werte in einer Matrix an ob zwei Knoten miteinander verbunden sind oder nicht
  - Anstatt binäre Werte kann auch ein Gewicht angegeben werden
  - Schnelle Suche (O(1))
  - Schnelles löschen einer Verbindung (O(1))
  - Speicherintensiv
  - komplexes Hinzufügen neue Knoten  
