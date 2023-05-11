---
title: Ereignisprozessketten
published: 1
date: 2023-05-11T20:20:25.207Z
tags: 
editor: markdown
dateCreated: 2023-05-11T20:20:25.207Z
---

# Ereignisprozessketten

## EPK

- beschreibt Arbeitsprozesse als Aufeinanderfolge von Ereignissen und Funktionen / Tätigkeiten
- Funktion ist fachliche Aufgabe / Tätigkeit an einem Objekt
  - Beschreibung mit Objekt und Verrichtung
- Ereignis beschreibt einen eintretenden Zustand

```mermaid
flowchart LR

id1{{Ereignis}}
id2(Funktion)
id3{{Ereignis}}

id1 -->|stößt an| id2 
id2-->|resultiert in| id3

```

Grundregeln:

- Prozess beginnen und enden mit Ereignissen
- Ereignisse lösen Funktionen aus
- Funktionen erzeugen Ereignisse

Verknüpfungsoperatoren:

- können aufteilen und zusammenführen
- UND
- ODER
- XOR (entweder oder)

> Splits können nur mit gleichem JOIN zusammengeführt werden
{.is-warning}

## Erweiterte EPK (eEPK)

Zusätzliche Sichten möglich:

- Datensicht
  - Fluss von Daten
- Organisationssicht
  - Beziehungen zwischen Ressourcen
- Funktionssicht
  - Beziehungen zwischen Vorgängen
- Leistungssicht
  - Zuordnung von Dienst-, Sach-, und finanziellen Leistungen

Zusätzliche Elemente:

Stelle: Beschreibt ein bestimmtes Aufgabenfeld einer
Person  
![Stelle](/fom/semester-4/geschaeftsprozessmodellierung/stelle.png)  
Rolle: Beschreibt eine bestimmte Aufgabe einer Person  
![Rolle](/fom/semester-4/geschaeftsprozessmodellierung/rolle.png)  
Organisationseinheit: Beschreibt eine Gruppe von Personen  
![Organisationseinheit](/fom/semester-4/geschaeftsprozessmodellierung/orga-einheit.png)  
Datencluster/Anwendungssystem: Funktionsspezifische Software  
![Datencluster](/fom/semester-4/geschaeftsprozessmodellierung/datensystem.png)  
Externe Personen: Personen, die nicht zur Organisation gehören, aber im Prozess eine Rolle spielen  
![Externe Personen](/fom/semester-4/geschaeftsprozessmodellierung/externe-person.png)  
Dokument: Informations- oder Planungsgrundlage  
![Dokument](/fom/semester-4/geschaeftsprozessmodellierung/dokument.png)  
Datenbank: Gespeicherte Informationen  
![Datenbank](/fom/semester-4/geschaeftsprozessmodellierung/datenbank.png)  
