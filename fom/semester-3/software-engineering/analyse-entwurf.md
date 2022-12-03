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

- zeigt Zustände die ein Objekt einnehmen kann
- Ereignisse lösen Zustandswechsel aus
- Lebenszyklus kann über mehrere Anwendungsfälle hinweg abgebildet werden
- muss deterministisch sein

![zustandsdiagramm](/fom/semester-3/software-engineering/zustandsdiagramm.png)

Zustandskörper:  

ENTRY: Das Ereignis wird beim Eintritt in einen Zustand automatisch 1x ausgelöst => in allen hereinkommenden Übergängen  

DO: Das Ereignis wird immer wieder ausgelöst, wenn der Zustand nicht gewechselt wird.  

EXIT: Das Ereignis wird beim Verlassen eines Zustandes 1x ausgelöst => in allen abgehenden Übergängen.

z.B.:

![Tür Beispiel](https://www.ionos.de/digitalguide/fileadmin/DigitalGuide/Screenshots_2020/zustandsdiagramm-3.jpg)

Der Zustand einer Tür ist „geschlossen“.  

Um in diesen Zustand zu kommen, muss zunächst das Ereignis „Tür schließen“ (entry) erfolgen.  

Während des Zustands gilt „Tür ist (durchgehend) geschlossen“ (do).

Wird der Zustand verlassen, erfolgt das Ereignis „Tür öffnen“ (exit).

Unterzustände:

- Parallele Teilzustände
- ohne parallele Teilzustände müsste Kreuzprodukt der Zustände gebildet werden

![unterzustände](/fom/semester-3/software-engineering/unterzustand.png)

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

### Überprüfen der Anforderungen

- unvollständigen Beschreibungen des Kunden => Requirements-Spezifikation erstellen
- Anforderungen vereinzeln und hinterfragen
- Vorstellungen des Kunden analysieren und verstehen

> Nicht nur Probleme erkennen, sondern auch Gute Sachen beibehalten
{.is-info}

Requirements-Spezifikation:

- Funktionale Anforderungen
- Nicht-funktionale Anforderungen

> Nicht nur aus Nutzersicht, sondern auch aus Betreiber- und Entwicklersicht betrachten
{.is-info}

### Spezifizieren der Geschäftsprozesse

Geschäftsprozess:

- Aufgrabe die ein Unternehmen ausführt
- Analyse aller operationellen Geschäftsprozesse
- von Technik abstrahieren
- keine Festlegung auf eine Technologie

Anwendungsfall:

- Teilabschnitt eines Geschäftsprozesses, welcher mit einem zu erstellenden System automatisiert werden soll
- spezifiziert durch funktionale Anforderung

> Durch Analyse der Geschäftsprozesse können automatisierbare Anwendungsfälle identifiziert werden
{.is-info}

### Priorisieren der Anforderungen

- Priorisierung aller Anforderungen / Geschäftsprozesse
- Priorität bestimmt Umsetzungsreihenfolge
- schrittweise Umsetzung wird erleichtert

### Erstellen des Kontextdiagramms (Systemgrenzen festlegen)

#### Kontextdiagramm

- zeigt Datenflüsse zwischen System und Umgebung
- Hilfsmittel zur Festlegung der Systemgrenzen
- erster Überblick über zu erstellende Schnittstellenspezifikationen
- Text in [] verweist auf Anforderung

Umgebung:

- alle Systeme, die mit dem zu erstellenden System interagieren

### Anforderungen neu definieren (Pflichtenheft)

Überarbeitung der Anforderungen entsprechend der definierten Systemgrenzen

### Erstellen des Anwendungsfalldiagramms

![Anwendungsfalldiagramm](#anwendungsfalldiagramme)

### Kurzbeschreibung der Anwendungsfälle

- bildet Übergang von Blackbox-Sicht zu Whitebox-Sicht
- logischer Ablauf innerhalb des Systems => Erfüllung des Anwendungsfalls
- Kurzbeschreibungstext => Aktivitätsdiagramm / Klassendiagramm

### Finden von Klassen und Erstellen des Klassendiagramms der konzeptionellen Sicht

1. Finden von Klassen mit z.B. [CRC-Methode](#crc-methode)
1. Erstellen von [Klassendiagrammen](#klassendiagramme)

#### CRC-Methode

für jede Klasse eine Karteikarte erstellt:

![CRC-Karteikarte](/fom/semester-3/software-engineering/crc-methode.png)

### Langbeschreibung der Anwendungsfälle

- Einbindung der gefunden Klassen in die Anwendungsfälle

Ziel:
Strukturierte Langbeschreibung der Anwendungsfälle

### Erstellen der Kommunikationsdiagramme für jeden Anwendungsfall

[Kommunikationsdiagramme](#kommunikationsdiagramme)
