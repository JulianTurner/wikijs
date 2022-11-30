---
title: Klausurvorbereitung
description: 
published: 1
date: 2022-07-20T17:05:20.330Z
tags: 
editor: markdown
dateCreated: 2022-03-04T12:22:55.269Z
---

# Klausurvorbereitung

//TODO warum Software Projekte fehlschlagen/scheitern

Was sind Anforderungen?
Welche Aktivitäten gehören zum Requirements Engineering?
Welche Nachteile entstehen bei fehlender Spezifikation?
Was sind Stakeholder?
Was ist ein Begriffslexikon?
Was ist ein Begriffsmodell?
Was sind funktionale Anforderungen?
Was sind nicht funktionale Anforderungen?

## [Aufwandschätzung](/fom/semester-3/software-engineering/aufwandschaetzng.md)

### Was ist der Schätztrichter?

- Zeigt wie die Unsicherheit im Laufe des Projekts abnimmt

### Nennen Sie Ansätze der Aufwandsschätzung

- Expertenschätzung
- Algorithmische Schätzung
- Top-Down
- Bottom-Up

### Was ist ein Delphi-Verfahren?

- Eine Moderator geführte Expertenschätzung
- Getrennte, anonyme Expertenschätzungen
- Diskussion der Ergebnisse
- Ergebnisse werden wiederholt abgefragt
- Ergebnis ist Median der Schätzungen

### Wie wird eine Analogie-Schätzung durchgeführt?

1. Zerlegen des Projekts in Komponenten
1. finden eines vergleichbaren Projekts
1. Aufwandsschätzung der Komponenten
1. Faktor  Personentage / Aufwandspunkte bestimmen bei vergleichbaren Projekts
1. Umrechnung der Aufwandspunkte des neuen Projekts in Personentage

### Auf welcher Idee basiert die Prozentsatzmethode?

Auf der Idee, dass die Aufwände der einzelnen Phasen in einem Projekt gleicher Größe in einem bestimmten Verhältnis zueinander stehen.

### Was ist die Grundlage der Aufwandsschätzung bei COCOMO?

Bei COCOMO liegt die Anzahl der Codezeilen zu Grunde.

### Welche Präzisionsstufen kennt COCOMO 81?

- Basic
- Intermediate
- Detailed

### Welche Bedeutung hat der Faktor M in den Berechnungsformeln von COCOMO 81?

Produkt der Kostenfaktoren, welche fördernde und hemmende Projektmerkmale repräsentieren.

### Was ist die Grundlage der Aufwandsschätzung bei der Function-Point-Methode?

Bei der Function-Point-Methode liegt die Anzahl der Funktionen zu Grunde.

### In welche Kategorien werden Anforderungen in der Function-Point-Methode eingeordnet?

Kategorie | Beispiel
---------|---------
Eingabe | Veranstaltung anlegen​
Abfrage | Veranstaltungen anzeigen​
Ausgabe | Veranstaltungsdetails anzeigen​
|
Datenbestände | Veranstaltungsdatenbank​
Referenzdaten | externes Teilnehmerverzeichnis​

### Was ist die Einflussbewertung in der Function-Point-Methode?

Beachtung von unternehmens- & Projektspezifischen Faktoren, welche die ungewichteten Aufwände beeinflussen.

z.B.:

- Schwierigkeit Algorithmen zu entwickeln
- Migrationen von Bestandsdaten​

### Was wird beim Planning Poker geschätzt?

- Aufwand in Aufwandspunkten

### Was sind Story Points?

Sind die Werte auf den Karten

### Wie ist der Ablauf beim Planning Poker?

[Ablauf beim Planning Poker](/fom/semester-3/software-engineering/aufwandschaetzng.md#planning-poker)

### Was ist der Unterschied zwischen Planning Poker und Magic Estimation?

Beim Planning Poker Schätzt jedes Teammitglied den Aufwand der gleichen Anforderung bis zur Einigung auf einen Wert oder weiterer Zerlegung.

Beim Magic Estimation werden die Anforderungen in Gruppe geschätzt und User Stories auf einer Zahlenreihe verschoben. Fall-Outs können mit andere Methode geschätzt werden.

## [Analyse und Entwurf](/fom/semester-3/software-engineering/analyse-entwurf.md)

### Wann ist die UML entstanden?

- 1990er

### Welche methodischen Wurzeln hat die UML?

- Definiert Wörter und Regeln für die Kombination der Wörter
- Syntax formal definiert
- Semantik nur informell definiert

### Was sind Strukturdiagramme?

- Beschreiben Beziehungen zwischen Programmteilen

### Was sind Verhaltensdiagramme?

- Beschreiben einzelne Aspekte eines Systems und deren Veränderungen zur Laufzeit

### Was sind Interaktionsdiagramme?

- Beschreiben eine Menge von Nachrichten welche interaktiv Ausgetauscht werden

### Welche Diagramme existieren in der UML?

- Use Case Diagramme
- Aktivitätsdiagramme
- Klassendiagramme
- Sequenzdiagramme
- Zustandsdiagramme

### In welcher Reihenfolge werden häufig Diagramme verwendet?

1. Use Case Diagramme (Analyse)
1. Aktivitätsdiagramme (Analyse)
1. Klassendiagramme (Analyse, Entwurf)
1. Sequenzdiagramme (Entwurf)
1. Zustandsdiagramme/Kommunikationsdiagramme (Entwurf)

### Was ist das Symbol für Akteure?

Strichmännchen*innen

### Was ist das Symbol für Use Cases?

Oval

### Wie unterscheiden sich «include» und «extend»?

- Benutzt-Beziehung (include)
  - Fragment welches auch in anderen Use Cases verwendet wird
  - Fragment kann nicht alleine als Use Case verwendet werden
  - Use Case ist nicht komplett ohne das Fragment

- Erweitert-Beziehung (extend)
  - Erweiterung mit einem eigenständigen Use Case
  - Use Case wäre auch komplett ohne das Fragment

### Was drückt die Assoziation in Use-Case-Diagrammen aus?

Beziehung zwischen Akteuren und Use Cases

### Modelliert man in Use-Case-Diagrammen Prozessketten?

Nein

### Modelliert man in Use-Case-Diagrammen Funktionshierarchien?

Nein

### Wofür Wird das Rauten-Symbol verwendet?

- Entscheidung (Verzweigung)
- Zusammenführung (Oder-Verknüpfung)

### Wie werden Bedingungen modelliert?

1. Pfeil von der Raute ausgehend
1. Bedingung in eckigen Klammern annotieren

### Was bedeuten Teilung und Synchronisation?

- Teilung
  - Teilung einer Aktivität in mehrere Aktivitäten
  - Aktivitäten werden parallel ausgeführt

- Synchronisation
  - Warten auf die Ausführung aller Aktivitäten
  
### Was ist der Unterschied zwischen Aktion und Aktivität?

Aktionen sind ein Bestandteil einer Aktivität

### Was ist ein Objektknoten?

Ein Trigger für eine Aktivität

### Wie Wird ein Objektknoten modelliert?

1. Rechteck auf der Grenze einer Aktivität
1. Pfeil zur initialen Aktion
1. Name des Objektknoten innerhalb des Rechtecks

### Was dokumentieren Pfeile in Aktivitätsdiagrammen?

Richtung des Kontrollflusses
