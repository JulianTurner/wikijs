---
title: Hadoop
description: 
published: 1
date: 2023-01-18T18:30:42.531Z
tags: 
editor: markdown
dateCreated: 2022-10-03T18:34:40.622Z
---

# Hadoop

- Open-Source-Softwareplattform bestehend aus verschieden Komponenten (Services)
- verteilte Speicherung mit digital attached Storage erweiterbar
- verteilte Verarbeitung sehr großer Datenmengen

Stellt eine Reihe von Anweisungen bereit, mit denen Daten auf vielen Servern organisiert und verarbeitet werden

![Hadoop](hadoop.png)

## Herausforderungen

### Bandbreite

Entscheidung ob es effizienter ist die Daten lokal zu verarbeiten oder über das Netzwerk zu verteilen

### Zuverlässigkeit der Skalierung

Redundanz ist Kernkomponente beim verteilten speichern von Daten mit Hadoop

### IOPS

IOPS = Input/Output Operations per Second
IOPS sollen pro GB verglichen werden (2TB = 2000 GB)

## Schema

Nutzt Vorteile von Schema on Write (strukturierte Daten) und Schema on Read (unstrukturierte Daten)

### Schema on Read (unstrukturierte Daten)

- Daten werden in beliebiger Form gespeichert (präskriptives Modellieren)
- Parser beinhaltet das Schema beim Lesen der Daten

### Schema on Write (strukturierte Daten)

- Daten werden in einem zuvor definierten Schema gespeichert (deklaratives Modellieren)

#### Hadoop Infrastruktur

![big-data-stack](big-data-stack.png)

## Ökosystem

- HDFS (Hadoop Distributed File System)
- YARN (Managed Ressourcen - "Welche Ressourcen sind verfügbar?"; Herzschlag des Clusters)
- Apache Ambari (Management-Interface)
- Zookeeper (Welcher Server ist Main? Down? Up?)
- MapReduce (Datenverarbeitung)
- Spark (in-memory Datenverarbeitung)

### Externe Datenbanken

- MySQL
- Cassandra
- MongoDB

### Query Engines

- Hue
- Drill (schreibt SQL Queries)
- Apache Phoenix

### Welche Elemente gehören zur Security MapReduce-Platform?

- Knox
- Sentry

## Hadoop Distributed File System (HDFS)

- skalierbares Dateisystem
- Speicherung von Daten auf mehreren Servern

## MapReduce

- Framework für verteilte Berechnungen
- JobTracker verteilt Aufgaben auf (mehrere) TaskTracker
- Anzahl TaskTracker abhängig von Cluster-Struktur

> Gibt nicht die roh Daten weiter sondern aggregiert wie viele Datensätze vorhanden sind (z.B. Array Länge)
{.is-info}

### Ablauf Job

1. Client startet Job
1. YARN entscheidet auf welcher Maschine der Job ausgeführt wird
1. Auf der Maschine wird Applikation Master gestartet (ist verantwortlich für alle MapReduce Aufgaben im Cluster und im Netzwerk)
1. Application Master fordert Ressourcen vom Node Manager an
1. Node Manager startet MapReduce Taskmanager auf Processing Nodes nahe dem Ablageort der Daten (Daten sind schwerfällig)

### Funktionsweise MapReduce

- Map: Daten werden in Key-Value Paare umgewandelt
- Key-Value Paare aggregieren zu Key-Tupel-Paaren
- Nutzt Array Kardinalität um zu zählen wie oft ein Key vorkommt
- Reducer aggregiert Ergebnisse von verschiedenen Map Task

### Was ist der Applikation Master?

Verantwortlich für alle MapReduce Aufgaben im Cluster und im Netzwerk

## Hadoop vs. Spark

Hadoop | Spark
---------|----------
schnell | 100x schneller als MapReduce
Speicherung auf Festplatte | Speicherung im Arbeitsspeicher
Stapelverarbeitung | Verarbeitung in Echtzeit
kostengünstig | höhere Kosten

Spark:

- Geschwindigkeit durch Daten im RAM
- Datenverlust bei Stromausfall / Reboot (USV unabdingbar)
- Arbeitsspeicher / Rechenleistung kann über verschiedene Nodes verteilt werden

Hadoop:

- Geschwindigkeit kommt von der Festplatte & Netzwerk
- Daten überleben Stromausfall / Reboot
- Festplatten / Rechenleistung kann über verschiedene Nodes verteilt werden

### RDD (Resilient Distributed Dataset)

Resilient: unverwüstlich
Distributed: verteilt
Dataset: Datensatz

- kann Dateifehler handeln über Parität & Redundanz
- sieht für den Nutzer als 1 Datenset aus
- Datenset = Key-Value Paare
- Parameter kann eine Lambda Funktion sein

### RDD Prozess

1. Daten liegen in langsamer Datenquelle vor (HDFS, JSON, CSV, ...)
1. initiale RDD wird aus Datenquelle erstellt
1. Umwandlung in neue RDD (Map, Filter, ... - Zwischenschritte sind kalt, werden nicht ausgeführt bis Ergebnis benötigt wird)
1. Abschließende Operation wird ausgeführt (z.B. count, collect)
1. Ergebnis: Ziel RDD (speichern, ausgeben, Basis für neue RDD Umwandlung)

> RDDs sind unveränderlich (immutable) und werden nur durch Transformationen verändert
{.is-info}

### SparkContext

- verantwortlich RDDs belastbar und verteilt zu machen
- Erzeugt RDDs
- Ökosystem rund um RDDs
