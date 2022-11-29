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

Verbesserung von Precision & Recall:

- Vorverarbeitung von Texten (z.B. Lowercase)
- Identifizierung von Synonymen (z.B. Sofa statt Couch)

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

- Anfang Turing-Test

Fähigkeiten für Turing-Test:

- natürlicher Sprachprozess (in menschlicher Sprache)
- Wissensrepräsentation (Wissen in Form von Kontext)
- Logische Schlussfolgerung (Antwort auf Basis des Wissens)
- Lernen (Mustererkennung, extrapolieren von Wissen)

- Unstrukturierte Texte sind eine kaum behandelte Quelle für Daten
- Vorstufen von Text-Processing sind Sprach-Analysen und optische Schriftzeichenerkennung

### Text Mining Grundlagen

#### Ziele des Text-Mining

Wissensentdeckung durch Text Analyse:

- Wovon handelt der Text?
- Was grenzt Text anderen Texten ab?
- Welche Elemente prägen einen Text?

Mustererkennung:

- Stil
- Wortgruppen
- Worthäufigkeiten
- Clusteranalyse

#### Anwendungen in Text-Mining

- Wort-Vektoren
- Chatbots
- Text-Predictive Analysen
- Text-Erstellung basierend auf gecrawlten Daten

#### Information Retrieval (IR)

Elemente:

- Dokumentenkorpus (Tweet, Artikel, Buch)
- Suchanfrage (Keyword, Wortgruppe)
  - Liste von Keywords
  - Wörter in bestimmter Reihefolge
  - boolesche Operatoren (AND, OR)
  - nicht-boolesche Operatoren (NEAR, SITE)
- Ergebnismenge (Teilmenge: relevante Dokumente)
- Repräsentation der Ergebnisse (sortierte Liste, mehrdimensionale Darstellung)

#### Klassifikation von Texten

Ziel: Texte in definierte Klassen unterteilen
=> Texte in Worte (Tokens) unterteilen => mit Operatoren nach Schlüsselwörtern & Wortkombinationen suchen

Unterscheidungen beachten: [Supervised](/fom/semester-3/big-data/text_mining#supervised-learning), [Unsupervised](/fom/semester-3/big-data/text_mining#unsupervised-learning) & [Hybrid](/fom/semester-3/big-data/text_mining#hybrid-semi-supervised-learning) Learning

Term Gewichtung:

- Konzentriertes Auftreten von Tokens in bestimmten Textgruppen
- Gleichmäßiges Auftreten von Tokens in allen Textgruppen

Clusteranalyse:

- Termgruppen und Häufigkeit von als Zahlenwerte ausdrücken und in Koordinate darstellen
- Signifikante Abgrenzung von Termgruppen erkennen

> Ergebnis: Texte als Zahlen ausdrücken und statistische Methoden nutzen
{.is-info}

#### Vorgehen: Text-Mining mit clustern von Termen

1. Texte in Wörter (Tokens) unterteilen
1. Häufigkeiten von gleichen Tokens pro Textgruppe zählen
1. Stopwords (Füllwörter z.B. wird, der, und) entfernen
1. Häufigkeit von Tokens aller Textgruppen summieren
1. Auswerten mit statistischen Methoden

Z.B.:
Text 1: Text Mining wird ein wichtiges Werkzeug sein.
Text 2: Text Mining nutzt die Methoden des Data Mining

Textgruppe | Text | Mining | <s>wird</s> | <s>ein</s> | wichtiges | Werkzeug | <s>sein</s> | nutzt | <s>die</s> | Methoden | <s>des</s> | Data
--- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | ---
Text 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 0 | 0 | 0 | 0
Text 2 | 1 | 2 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1
Summe | 2 | 3 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1

Alternative One-Hot-Encodierung:

- Schnelleres Rechnen
- Verlust von Häufigkeitsinformationen

#### Modelle

- eine Sprache besteht aus einer Menge von Zeichenfolgen
- eine Menge aus Regeln definiert eine Grammatik

- Sprachmodell z.B. Häufigkeit von Folgen von Zeichen
- n-Zeichenfolgen => n-Gramm-Modell
- n-Gramm-Modell = Markov-Kette mit Ordnung n-1 (Sliding Window)

Mit n-Gramm-Modell kann die Maschine natürliche Texte aufbauen

z.B.:
Hast du die E-Mail...:

- gelesen?
- geöffnet?
- gesehen?

<!-- Weiter bei Seite 556 / 530 -->

## Text Mining mit Deep Neural Networks

## Vektor-Repräsentanz von Worten, Word Embeddings
