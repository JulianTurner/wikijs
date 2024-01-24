---
title: Persistenter Speicher, HDD, SSD, Dateisysteme
published: 1
date: 2023-09-13T19:14:29.207Z
tags: 
editor: markdown
dateCreated: 2023-09-13T19:14:29.207Z
---

# Persistenter Speicher, HDD, SSD, Dateisysteme

## Hierarchische Dateisysteme

- Dateien werden in Verzeichnissen organisiert
- Verzeichnisse können weitere Verzeichnisse enthalten (Baumstruktur)
- Verzeichnisse werden durch kanonische Dateinamen identifiziert

## Netzwerkdateisysteme

- übertragen Systemaufrufe über das Netzwerk
- für Anwendungen transparent

## Datei Attribute

- Meta-Informationen über Dateien
  - Dateilänge
  - Erstellungsdatum
  - Besitzer
  - Zugriffsrechte (ACL)
  - beliebige benutzerdefinierte Attribute

## Indizierung von Dateien

- Index-Block enthält Attribute und Zeiger auf Datenblöcke
- Indexknoten = Inode

## Journaling Filesystem mit Transaktionen

- Dateisysteme können durch Stromausfall oder Absturz in einen inkonsistenten Zustand geraten
- Journaling Filesysteme verwenden Transaktionen um Dateisysteme konsistent zu halten
- bei einem Stromausfall oder Absturz werden Transaktionen rückgängig gemacht
- bei Start des Betriebssystems muss nur das Journal geprüft werden

## Verzeichnisse als Dateien

- Verzeichnisse sind Dateien, die andere Dateien referenzieren
- enthält Hinweis auf Speicherort des Objekts das es beschreibt
- Standardeinträge:
  - `.` -> aktuelles Verzeichnis
  - `..` -> Elternverzeichnis
- Absoluter Pfad -> von Wurzelverzeichnis ausgehend
- Relativer Pfad -> von Arbeitsverzeichnis ausgehend

> Hauptfunktion: Pfad/Dateinamen auflösen zum Speicherort der Daten im Speicher
{.is-warning}

### Hardlink

- Verweis auf Inode
- nur Verweis auf Datei, nicht auf Verzeichnis
- nur auf gleicher Volume/Partition möglich

### Softlink

- Verweis auf Namen (anderes Verzeichnis oder Datei)
- Verknüpfung
- wird das Ziel gelöscht, zeigt der Softlink ins Leere
- kann zu kanonischen Name aufgelöst werden
