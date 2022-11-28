---
title: Text Mining
description: 
published: 1
date: 2022-07-20T17:05:20.330Z
tags: 
editor: markdown
dateCreated: 2022-03-04T12:22:55.269Z
---

# Text Mining

## Supervised Learning

Kernfähigkeiten Data Science sind analytische Fähigkeiten aus:

- Statistik
- maschinelles Lernen
- künstliche Intelligenz

### Unabhängige & Abhängige Variablen

- 1 oder mehrere unabhängige Variablen haben Einfluss auf eine abhängige Variable
- Mustererkennung => identifizieren von abhängigen Variablen

> Korrelation ist nicht Kausalität
{.is-info}

Ziele:

- Daten vorhersage: abhängige Variable durch Modell vorhersagen
- Güte der Vorhersage bestimmen

![variablen.png](/fom/semester-3/big-data/variablen.png)

Hypothesentest:

- **Überprüfen von** Wirkung einer unabhängigen Variable auf eine abhängige Variable
- beschreibt eine Stichprobe

Modell:

- **Erläutert die** Wirkung einer unabhängigen Variable auf eine abhängige Variable
- allgemeine Beschreibung des Effekts
- Übertragbarkeit auf neue Daten > Präzision

### Gütemaße

Precision: Anteil der korrekten Vorhersagen die richtig erkannt wurden

Recall: Anteil der korrekten Vorhersagen von allen korrekten Vorhersagen

### Hybrid: Semi-Supervised Learning

1. keine abhängige Variable im Datensatz
1. Generierung von einer abhängigen Variable basierend auf Stichprobe
1. Erzeugen von Modell auf Basis der Stichprobe mit abhängiger Variable
1. Modell auf gesamten Datensatz anwenden => Ergebnis
1. Stichprobe repräsentativ => Wird das Verhältnis der Ausprägungen der abhängigen Variablen in der Stichprobe dem des gesamten Datensatzes entsprechen

## Unsupervised Learning

- abhängige Variable nicht vorhanden
- keine Vorhersage von abhängiger Variable
- Gruppierung von ähnlichen Datensätzen mit Clusteranalyse
- Menge der Gruppen = Clusterzentren (k) variabel

- Größeres k => mehr Cluster => höhere Übertragbarkeit & Geringere Güte
- k-means Clustering => anfällig gegenüber Ausreißern => neue Cluster
- Jaccard-Koeffizient => Ähnlichkeit von Clusterzentren

![jaccard.png](/fom/semester-3/big-data/jaccard.png)

> hat viel mit Clustering zu tun
{.is-info}

## Natural Language Processing

## Text Mining Ansätze

## Text Mining mit Deep Neural Networks

## Vektor-Repräsentanz von Worten, Word Embeddings
