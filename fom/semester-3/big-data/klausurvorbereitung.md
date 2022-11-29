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

## Mehr, Unscharf, Korrelation

- mehr: detailliertere Datensammlung
- unscharf: Genauigkeit wird aufgegeben um mehr Datenpunkte auszuwerten
- Korrelation: Anstatt nach Korrelation (Zusammenhang) zu suchen wir nach Kausalität gesucht (Warum passiert etwas?)

## Fundamentals

> LOB (Line of Business) = Geschäftsbereich
.{is-info}

### Definition von Big Data?

Wirtschaftliche Gewinnung von Erkenntnissen aus qualitativen und unterschiedlich strukturierten Informationen, in ungekannten Umfang.

5 V's von Big Data?

- Datenmenge (Volume)
  - Anzahl von Datensätzen
- Datenvielfalt (Variety)
  - Fremd- & eigene Daten
- Geschwindigkeit (Velocity)
  - Generierung und Übertragung der erzeugten Daten
- Unsicherheit (Veracity)
  - Zusammenhänge, Bedeutungen, Muster
- Wert (Value)
  - Mehrwert aus größeren Datenmengen gewinnen

### Wachstum von Big Data?

mithilfe von:

- Mobilgeräten & Internet um Daten zu sammeln
- Geschäftsmodellen welche Daten sammeln (z.B. Google, Facebook)
- Sensoren (Veränderungen in der Umgebung)

### Unterschiede zwischen 2nd und 3rd Platform?

2nd Platform (Scale-Up):

- klassische Datenbanken
- Datawarehouse / in Memory
- Skalierbare Sicherung

3rd Platform (Scale-out):

- Analytik und Visualisierung
- NoSQL Datenbanken
- Hadoop

![](plattform-vergleich.png)

### Herausforderungen von Big Data?

50% der Unternehmen scheitern bei der Umsetzung von Big Data Projekten

- wird als Technologie betrachtet nicht als Unternehmenstransformation
- Ökosystem ist fragmentiert und entwickelt sich schnell weiter
- Technologien erfordern neue Rollen und Fähigkeiten

### Datenanalyse?

1. Vorbereiten (Abrufen, Bereinigen, Umwandeln)
1. Untersuchen (Exploration, Visualisierung)
1. Modell (Mining, Entdeckung)

### Bereiche und Rollen von Big Data?

- Business Facing => Business Analyst
- Applications => Application Developer, Data Scientist
- Infrastructure => Architecture, It Admin, Program Manager

### Reifegrade der Unternehmen?

![Reifegrad](reifegrad.png)

### Definition von Anwendungsfällen?

![](anwendugsfaelle.png)

### Big Data Architekturen?
<!-- TODO ! Abklären S. 138/139-->
### Nachteile der Strukturen?

![](1-data-warehouse.png)
![](2-hubedw.png)
![](3-aio.png)
![](4-newdw.png)

### Wann verwendet man Object Storage?

bei unstrukturierten Daten

### Wert von Object Storage?

- verteilter Zugriff auf Inhalte
- Unstrukturierte Datenworkloads
- Kapazität > 100 TBs

z.B. Patientenakte (Audio, Bilder, Text)

### Abgrenzung zwischen SQL und NoSQL?

MySql:

- Datenkonsistenz
- Verfügbarkeit

MongoDb:

- Verfügbarkeit
- Partitionierung

### Idee für Big Data Anwendungsfall?

- Dynamische Preisgestaltung
- Kundenbindung
- Kundenverhalten

### Wichtigsten Domänen für Data Science?

## Hadoop

[siehe Hadoop](./hadoop.md#hadoop)

## Maschine Learning

### Unterschied zwischen Maschine Learning und Deep Learning?

- Deep Learning ist ein Teilbereich von Maschine Learning

### Unterschied zwischen Random Forrest und Decision Tree?

Random Forrest:

- Art Schwarmintelligenz
- erzeugt hochwertige Modelle
- schnell zu trainieren
- langsam in der Vorhersage (im Vergleich zu anderen ML Algorithmen)
- schwer zu interpretieren

Decision Tree:

- einfach zu verstehen und zu implementieren
- nicht leistungsstark für komplexe Daten

### Unterschied zwischen Modellparameter und Hyperparameter?

Modellparameter:

- werden während des Trainings ermittelt
- beeinflussen die Vorhersage

Hyperparameter:

- werden vor dem Training festgelegt
- beeinflussen die Leistung des Modells (z.B. Anzahl der Schichten, Anzahl der Neuronen, Anzahl der Epochen)

## Text Mining

### Wann verwendet man Precision und Recall?

- [Precision](/fom/semester-3/big-data/text_mining.md#gütemaße): Misst den Anteil der tatsächlich relevanten Dokumente (True Positives) in den gefundenen Dokumenten
- [Recall](/fom/semester-3/big-data/text_mining.md#gütemaße): Bruchteil aller relevanten Dokumente, die gefunden wurden
