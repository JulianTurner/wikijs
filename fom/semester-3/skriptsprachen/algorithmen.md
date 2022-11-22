---
title: Algorithmen
description: 
published: 1
date: 2022-10-14T11:23:05.735Z
tags: 
editor: markdown
dateCreated: 2022-10-13T12:49:44.966Z
---

# Algorithmen

## Korrektheit

Algorithmen sind korrekt, wenn sie für alle Eingaben das richtige Ergebnis liefern.

Möglichkeiten Zuverlässigkeit zu erhöhen:

- Software Engineering
- Programmierung
- Validation
- Verifikation

Partielle Korrektheit + Terminierung = Totale Korrektheit

> Mit Testen kann man die Korrektheit eines Programms nicht vollständig beweisen
{.is-warning}

### Funktionale / Imperative Korrektheit

Funktional:

- meist einfach zu beweisen (z.B. vollständige Induktion)

Imperativ:

- kein funktionaler Zusammenhang zwischen Eingabe und Ausgabe
- Berechnungsschritte können Seiteneffekte haben
- schwerer zu beweisen (z.B. Hoare-Kalkül)

## Komplexität

### Laufzeitanalyse

Messen der Laufzeit:

- abhängig von Ausführungsumgebung (Hardware, Betriebssystem, Compiler)
- abhängig von Parameterwerten
- gängige Methode

Zählen der Elementaroperationen:

- Addition, Zuweisung, Vergleich, Zugriff auf Datenstruktur
- geht in Hochsprache nicht da Maschinencode abstrahiert wurde

### Betrachtete Eigenschaften

- Eingabegröße
- Laufzeit
- Speicherverbrauch

### Asymptotische Laufzeit

- bei kleinen Eingaben ist die Laufzeit uninteressant
- wie verhält sich die Laufzeit bei großen Eingaben?

asymptotischen Laufzeit => das Zeitverhalten des Algorithmus für eine potenziell unendlich große Eingabemenge

> Es interessiert also nicht der Zeitaufwand eines konkreten Programms auf einem bestimmten Computer, sondern viel mehr, wie der Zeitbedarf wächst, wenn mehr Daten zu verarbeiten sind, also z. B. ob sich der Aufwand für die doppelte Datenmenge verdoppelt oder quadriert (Skalierbarkeit)
{.is-info}

### Schranken

- Schwer genaue Verteilung zu finden
- Worst-Case Betrachtung am interessantesten => Obere Schranke

Laufzeit für beliebige Eingabe $<=$ Obere Schranke  
