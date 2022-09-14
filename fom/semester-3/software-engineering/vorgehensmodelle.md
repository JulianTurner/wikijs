---
title: Vorgehensmodelle
description: 
published: 1
date: 2022-06-10T18:03:55.907Z
tags: 
editor: markdown
dateCreated: 2022-03-04T12:23:12.295Z
---

# Vorgehensmodelle

## Basismodelle
Vorgehensmodelle auf Projektebene
### Code & Fix
Loslegen ohne Entwurf

Vorteile:
- schnell
- einfache Tätigkeiten
- geringe Komplexität

Nachteile:
- Fehler werden nachträglich behoben
- häufige Überarbeitung notwendig
- Arbeiten können nicht verteilt werden
- schlechte Skalierbarkeit
- keine Dokumentation

### Sequentielles Modell
Definieren, Entwerfen, Entwickeln
Eine Phase nach der anderen
![](squentielles-modell.png)

Vorteile:
- einfach Verständlich
- geringer Projektaufwand
- wenig Kommunikationsaufwand

Nachteile:
- keine parallele Arbeit möglich
- Ergebnisse liegen später vor
- keine Schleife oder Iteration (keine Rückfragen)

### Wasserfallmodell
Jeder Aktivität wird eine Phase zugeordnet, die in einer bestimmten Reihenfolge abgearbeitet werden muss.
Möglichkeit von Rücksprung in die jeweils vorherige Phase

![](https://emergenz.hpfsc.de/html/modell.png)

Vorteile:
- einfach Verständlich
- geringer Projektaufwand
- wenig Kommunikationsaufwand
- Rücksprungmöglichkeit

Nachteile:
- kein Feedback
- keine parallele Arbeit möglich
- bei Änderungen startet das Modell neu

### V-Modell
- Integriert Maßnahmen zur Qualitätssicherung  
- Erweitert Wasserfallmodell  

![](v-modell.jpg)

Vorteile:
- Fehler werden früher als im Wasserfallmodell erkannt
- Abnahme durch den Auftraggeber vereinfacht
- arbeiten in verteilen Teams möglich

Nachteile:
- erneute Einarbeitung von Teams bei Änderungen / Rückfragen
- nicht iterativ
- nicht für komplexe Projekte geeignet

### Nebenläufiges Modell
Phasen werden so schnell wie möglich gestartet.
Erfordert viel Kommunikation und Koordination und ausreichend Ressourcen für Überarbeitungen innerhalb der Phasen. 

Vorteile:
- optimale Zeitnutzung
- parallele Arbeit möglich
- schnelle Ergebnisse
- allgemein anwendbar

Nachteile:
- unnötige Schleifen durch Überarbeitungen
- hoher Kommunikationsaufwand
- hoher Planungsaufwand
- doppelte Arbeiten

### Evolutionäres Modell
Anfangsentwurf wird iterativ weiterentwickelt. Konzentration liegt auf lauffähigen Zwischenversionen.

![](evolutionaeres-modell.png)

Vorteile:
- schnelle lauffähige Zwischenversionen
- geringes Projekt-Risiko - Auftraggeber hat keine Überraschungen
- Fehler werden frühzeitig erkannt


Nachteile:
- grundlegend Änderungen sind schwierig
- neue Anforderungen können unwirtschaftlich sein

### Komponentenmodell
Projekt wird in Komponenten aufgeteilt, die unabhängig voneinander entwickelt werden können.

Vorteile:
- frühe Produktlieferung
- Konzentration auf eigene Stärken

Nachteile:
- auffinden geeigneter Komponenten ist schwierig
- Anpassungen von fremden Komponenten sind schwierig
- abhängig von andere Lieferanten

### Prototypenmodell
Es wird ein horizontaler oder vertikaler Prototyp entwickelt, der die Anforderungen teilweise erfüllt.  
Der Nutzer bekommt einen frühzeitigen Einblick in die Funktionalität des Produktes.

![](prototypen-modell.png)

#### Vertikaler Prototyp
Bildet Funktionen über den ganzen Stack ab.  
zb. eine vollständige CRUD-Operation

#### Horizontaler Prototyp
Bildet eine Ebene des Stacks ab.  
zb. Wireframes für die UI




Vorteile:
- Reduzierung des Projektrisikos
- bessere Planbarkeit
- bessere Lösungsfindung

Nachteile:
- zusätzlicher Entwicklungsaufwand
- Dokumentation wird durch Prototypen ersetzt
- Grenzen und Einschränkungen schwer zu erkennen

#### Rapid Prototyping
Frühzeitige Entwicklung von Prototypen.   
Gewonnenes Wissen kann in den Entwicklungsprozess einfließen.

Der Prototyp:
- kein Teil Software
- Teil der Anforderungsanalyse
- darf nicht von schlechter Qualität sein
- ersetzt nicht die Spezifikation

> schnelles Zusammensetzten von Prototypen wird **Rapid Prototyping** genannt
{.is-info}
#### Vorgehensweise
![](vorgehensweise-protoyp.png)

### Inkrementelles Modell
Von einem Kern wird Stückweise die Software erweitert.  
Schalenförmiger Aufbau.
![](inkrementelles-modell.png)

Vorteile:
- vollstände Anforderungsdefinition von Anfang an
- schnelle Auslieferung von Teilprodukten
- geringes Risiko einer Fehlentwicklung
- kann in unterschiedlichen Teams entwickelt werden

Nachteile:
- Anforderungsdefinition kostet am Anfang viel Zeit
- schlechter Umgang mit Änderungen der Anforderungen

### Iteratives Modell
Entwicklung in mehreren geplanten Iterationen.
Jeder Iteration enthält die gleichen Teilschritte (z.B. Analyse, Design, Implementierung, Test).
Die Basis für die nächste Iteration ist das Ergebnis der vorherigen Iteration.

> größere Projekte können mehrere kleinere Projekte aufgeteilt.  
{.is-info}

### Spiralmodell
Ein iteratives Modell welches innerhalb einer Iteration ein Wasserfallmodell durchläuft. Wird gerne für große Projekte verwendet, um Risiken zu minimieren.
![](sprialmodell.png)

Vorteile:
- Flexibilität
- Risikobehandlung (minimiert Risiko der Planabweichung, nicht Risiko falscher Konzeption)
- hohes Kundenfeedback

Nachteile:
- hohe Kosten
- abhängig von der Risikoanalyse
- Komplexität
- schwierig zu planen
## Monumentale Modelle
Genaue Beschreibung wie Prozess und Qualitätsziele erreicht werden sollen 

## Agile Modelle
Gegenbewegung zu den monumentalen Modellen
