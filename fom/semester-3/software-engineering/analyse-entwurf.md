---
title: Analyse & Entwurf 
description: 
published: 1
date: 2022-10-12T16:18:19.804Z
tags: 
editor: markdown
dateCreated: 2022-09-13T18:16:00.734Z
---

# Analyse & Entwurf

## Einführung UML

Unified Modeling Language wurde in den 1990er entwickelt

- Graphische Modellierungssprache
  - Definiert Wörter und Regeln für die Kombination der Wörter
  - Syntax formal definiert
  - Semantik nur informell definiert
- keine Entwicklungsmethode
- Basiert auf Metamodell
- Objektorientierter Ansatz

![Gliederung](https://upload.wikimedia.org/wikipedia/commons/d/da/UML-Diagrammhierarchie.svg)

Verbreitete Einsatzreihefolge UML Diagramme:

1. Use Case Diagramme (Analyse)
1. Aktivitätsdiagramme (Analyse)
1. Klassendiagramme (Analyse, Entwurf)
1. Sequenzdiagramme (Entwurf)
1. Zustandsdiagramme/Kommunikationsdiagramme (Entwurf)

## Vorstellung wichtiger Diagramme

### Strukturdiagramme

#### Klassendiagramme

- Klassen & Beziehungen unabhängig von der Programmiersprache abbilden
- Rahmen für Systemgrenze mit CD (Class Diagram) in der oberen linken Ecke
- Klassen werden in Bereiche aufgeteilt
  - Kopf: Name der Klasse
  - Attribute: Eigenschaften der von der Klasse beschriebenen Objekte (Name, Typ, Sichtbarkeit)
  - Methoden: Verhalten der Klasse (Name, Typ, Sichtbarkeit, Parameter)
- Eigenschaften der Sichtbarkeit
  - +: public
  - -: private
  - #: protected
  - ~: package
- Statische Attribute / Methoden werden unterstrichen
- Kommentare: Gestrichelte Linie mit Text

![Klassendiagramm](/fom/semester-3/software-engineering/Klassendiagramm.png)

#### Objektdiagramme

- Momentaufnahme eines Systems
- Rahmen für Systemgrenze mit OD (Object Diagram) in der oberen linken Ecke
- Jede Instanz hat einen Namen
- Beziehungen heißen Links

![Objektdiagramm](/fom/semester-3/software-engineering/Objektdiagramm.png)

### Verhaltensdiagramme

#### Anwendungsfalldiagramme

- Beschreibt Außensicht
- Spezifiziert Systemverhalten für jeden Anwendungsfall

Bestandteile:

- Use Case
  - Hauptfunktion (geforderte fachliche Funktionalität)
  - Basisfunktion (liefert Beitrag zur Funktionalität der Hauptfunktion)
- Akteur
- Generalisierungsbeziehung zwischen Use Cases / Akteuren
- Benutzt-Beziehung (include)
  - Fragment welches auch in anderen Use Cases verwendet wird
  - Fragment kann nicht alleine als Use Case verwendet werden
  - Use Case ist nicht komplett ohne das Fragment

- Erweitert-Beziehung (extend)
  - Erweiterung mit einem eigenständigen Use Case
  - Use Case wäre auch komplett ohne das Fragment

Beispiel:
![Anwendungsfalldiagramm](/fom/semester-3/software-engineering/Anwendugsfalldiagramm.png)

#### Zustandsdiagramme

#### Aktivitätsdiagramme

- Ausschnitt eine Programmablaufs
- Erweiterung von Flussdiagrammen
- Darstellung von parallelen Verhalten / Verantwortlichkeiten
- in komplexen Projekten zu jeden Use Case ein Aktivitätsdiagramm

![Aktivitätsdiagramm](/fom/semester-3/software-engineering/Aktivitaetsdiagramm.png)

#### Interaktionsdiagramme

##### Sequenzdiagramme

- Darstellung der zeitlichen Abfolge von Nachrichten
- Verwendung für Testfälle
- Aktive Form des [Objektdiagramms](#objektdiagramme)
- Zeit läuft von oben nach unten
- Beteiligte (Akteure, Objekte) kommunizieren über Nachrichten (Methodenaufrufe) => Horizontale Linien
- Gesamtheit der vertikalen Linie wird als Lebenslinie bezeichnet und mit X terminiert

![Sequenzdiagramm-Nachrichten](/fom/semester-3/software-engineering/squenzdiagramm_nachrichten.png)

![Sequenzdiagramm](/fom/semester-3/software-engineering/squenzdiagramm.png)

##### Kommunikationsdiagramme

- Stellt zusammenarbeit von Objekten dar
- keine Lebenslinien
- einfache Linien für Beziehungen
- Nachrichten werden mit Richtungsangaben versehen sowie in zeitlicher Reihenfolge durchnummeriert

![Kommunikationsdiagramm](/fom/semester-3/software-engineering/Kommunikationsdiagramm.png)

## Schritte der Systemanalyse

## Betrachtete Funktionen in Systemanalyse und Systementwurf

## Schritte im Systementwurf
