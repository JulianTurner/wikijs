---
title: Fragen Handout
published: 1
date: 2023-12-02T10:23:39.207Z
tags: 
editor: markdown
dateCreated: 2023-12-02T10:23:39.207Z
---

# Fragen Handout

## Künstliche Intelligenz – allgemein

### 1

Erklären Sie beispielhaft die Bedeutung der u.a. Aspekte aus der folgenden Definition von KI:

Einsatz und die Analyse der Anwendung menschlicher Sinne (Lesen, Schreiben, Sehen, Fühlen, Hören, Sprechen):

- OCR, Chatbots, Bilderkennung, Sentimentanalyse, Spracherkennung, Sprachsynthese

Menschliches Verstehen, Lernen, Adaptieren und Schlussfolgern:

Mustererkennung, Konzeptualisierung, Anpassung, Vorhersage

### 2

Der wirtschaftliche und technologische Fortschritt China’s hat sich in den letzten Jahrzehnten rasant entwickelt.
Erläutern Sie China’s strategische Ausrichtung in den letzten Jahren.

- Made in China 2025 -> hochwertige Erzeugnisse aus China
- neue Seidenstraße -> See- und Landwege von China nach Europa
- Aufbau der Infrastruktur -> Einzelschicksale werden nicht beachtet

KI als Schlüsseltechnologie für weiteren Wohlstand und Innovationen spielt hierbei eine zentrale Rolle.
Erläutern Sie die vier Entwicklungswellen von China im Vergleich zu den USA.

- Internet-KI -> mehr Internetnutzer in China
- Business-KI -> mehr KI-Startups in China
- Perception-KI -> verzichten auf Schutz der Privatsphäre für komfortable Nutzung
- Autonome0KI -> USA hat Vorsprung durch Silicon Valley

### 3

Erklären Sie „Push“ und „Pull“ Strategien im Zusammenhang mit den technologischen Innovationen und der Marktentwicklung

- Push: Technologie wird entwickelt und auf den Markt gebracht
  - Digitalisierung
  - Leistungssteigerung im Preisleistungsverhältnis
  - Miniaturisierung
  - Standardisierung
  - Lokalisierung

- Pull: Marktbedarf wird ermittelt und Technologie wird entwickelt
  - Individualisierung
  - einfacher Zugriff
  - Senkung der Transaktionskosten
  - Multimediale Angebotsformen
  - Mobilität

### 4

Erläutern Sie die fünf Fähigkeiten für typisch menschliches Handeln (AI Spektrum): Wahrnehmen, Lernen, Denken, Handeln, Wissen.

- Wahrnehmen: Bilderkennung, Spracherkennung
- Lernen: Mustererkennung, Konzeptualisierung
- Denken: Anpassung, Vorhersage
- Handeln: OCR, Chatbots
- Wissen: Sentimentanalyse, Sprachsynthese

Geben Sie jeweils 2 Beispiele für KI-Technologien, die hier eingesetzt werden und deren Zuordnung zur symbolische bzw. subsymbolischen KI.

- autonomes Fahren: symbolisch, digitaler Assistent (Alexa): subsymbolisch
- Firewall: symbolisch, Textvorhersage: subsymbolisch
- Chatbot: symbolisch, Tradingbot: subsymbolisch
- Dokumentenanalyse: symbolisch, ChatGpt: subsymbolisch
- Review Aggregator: symbolisch, live übersetzen: subsymbolisch

### 5

Erklären Sie die wesentlichen Unterschiede zwischen symbolischer und subsymbolischer Künstlichen Intelligenz (KI) laut AI Spektrum.
Erläutern sie jeweils 2 der existierenden Technologien sowie Methoden.

- Symbolisch
  - regelbasiert (formale Logik)
  - Expertensysteme
- Subsymbolisch
  - neuronale Netze
  - genetische Algorithmen

## Machine Learning

### 6

Erklären Sie folgende Verfahren des Maschinellen Lernens bzgl. Lernverfahren
und Zielfunktion: unüberwacht (unsupervised), überwacht (supervised) und
verstärkend (reinforcement).

- unsupervised:
  - keine Zielvariable
  - Muster / Zusammenhang erkennen
  - Einsatz von Abstandsmaß
- supervised:
  - Zielvariable -> Klasse (Ja/Nein) oder numerischer Wert
  - Erlernen vom Zusammenhang zwischen Input und Zielvariable
  - Lernen anhand von Datensätzen
- reinforcement:
  - keine Zielvariable
  - Lernen durch Feedback
  - keine Beispieldaten sondern Simulationsumgebung
  - Strategie wird über viele Iterationen entwickelt

Geben Sie jeweils Anwendungsbeispiel an und erläutern Sie

- unsupervised -> Erkennen von Objekten wie Hund oder Katze auf einem Bild
- supervised -> Vorhersage von Hauspreisen anhand von Merkmalen wie Größe, Lage, Alter
- reinforcement -> Spielentwicklung wo ein Bot eine Strecke fahren muss, um so weiter er kommt, desto mehr Punkte bekommt er, stößt er an, wird die Strecke zurückgesetzt

### 7

### 8

Wodurch unterscheiden sich unüberwachte und überwachte Lernverfahren?
Erläutern Sie.

Erklären Sie die Unterschiede bzgl. Lernverfahren und
Zielvariablen jeweils anhand eines Beispiels.

### 9

### 10

### 11

### 12

## Data Mining/Big Data

### 13

### 14

### 15

## Künstliche Neuronale Netze (kNN)/ Deep Learning/ CNN

### 16

### 17

Erklären Sie den Unterschied zwischen klassischem Machine Learning und dem
Deep Learning Ansatz.

- Beim Deep Learning entfällt die Feature-Extraktion, da diese automatisch durchgeführt wird.

Erläutern Sie den Grund für den aktuellen Boom der
KI aufgrund des Deep Learning.

- Durch die Erhöhung der Rechenleistung und der Menge an Daten.

### 18

Berechnen Sie für dieses sehr einfache künstliche Neuronalen Netz (kNN) die
Gewichte nach der Vorwärtspropagierung

Annahme:  
$\eta = 0.001$
  
$y = 3$
  
$t = \sum x_i * w_i$

$t = 2,3$

$\Delta w_i = \eta * (y-t) * x_i$  

$\Delta w_1 = 0.0084$

$\Delta w_2 = -0,0056$

$\Delta w_3 = 0.0049$

$w_{i}^{neu} = w_{i}^{alt} + \Delta w_i$

$w_{1}^{neu} = 0.5084$

$w_{2}^{neu} = 0.1944$

$w_{3}^{neu} = -0.2951$

$t_{new} = 2.4799$

### 19

### 20

Erläutern Sie die Architektur von Convolutional Neural Networks (CNN).

- extrahiert und erkennt Merkmale mit Hilfe von Filtern
- Mehrschichtige Modelle mit Feature Learning und anschließender Klassifikation
  - Feature Learning
    - Convolutional + Relu
    - Pooling
  - Classification
    - Flatten (Vektorisierung)
    - Fully Connected
    - Softmax

Warum können diese als Deep Learning Verfahren bezeichnet werden?

- weil das Feature Learning automatisch durchgeführt wird
- Baut auf mehreren Schichten auf

Erklären Sie wie sich Machine Learning von Deep Learning Verfahren unterscheiden

- Beim Deep Learning entfällt die Feature-Extraktion, da diese automatisch durchgeführt wird.

### 21

Erläutern Sie die allgemeine Architektur einer RoBERTa (RoBERTa: A Robustly
Optimized BERT Pretraining Approach)

1. Input wird in Token zerlegt
2. Input Embedding (kontextunabhängig via lookup table)
3. Positional Encoding (hinzufügen von Position Embeddings)
4. Roberta Layer 4x
    1. Self-Attention: Berechnung der Attention Scores (normiert)
    2. Layer Normalization: Normalisierung der Attention Scores
    3. Feed Forward: Berechnung der Outputs
    4. Layer Normalization: Normalisierung der Outputs

- Multi-Head Attention: Durchführung der Self Attention Operation (Verknüpfung von Input Embedding mit dem Kreuzprodukt)
  
Warum werden diese als Deep Learning Verfahren bezeichnet?

- Da das RoBERTa Konzept mehrmals verketten werden kann

### 22

### 23

## Entscheidungsbäume

### 24

Erläutern Sie den allgemeinen Aufbau von Entscheidungsbäumen.

- Ein Entscheidungsbaum ist ein Baum, dessen innere Knoten Merkmale (Attribute) repräsentieren
- Jede Kante steht für einen Attributwert
- An jedem Blattknoten ist ein Klassenwert angegeben

Um welchen Typ von Lernverfahren handelt es sich hier?

- Supervised Learning weil man gelabelte Daten benötigt, welche Zielvariable enthalten

Erklären Sie den Unterschied zwischen dem einfachen Lernalgorithmus und dem Greedy-Algorithmus.

- Einfacher Lernalgorithmus berechnet alle Bäume (inkl. Anzahl der Fehlklassifikationen) und wählt den Baum mit der geringsten Anzahl an Fehlklassifikationen aus
- Greedy-Algorithmus generiert den Baum schrittweise und wählt bei jedem Schritt die beste Entscheidung (höchste Informationsgewinn) aus

### 25

Erläutern Sie Vor- und Nachteile von Entscheidungsbäume.

Vorteile:

- gewonnenes Wissen ist als Blackbox verfügbar
- Anschauliche nachvollziehbare Entscheidungsregeln
- einfache Interpretation
- effiziente Auswertung des Modells

Nachteile:

- bei vielen Attributen unübersichtlich
- finden des optimalen Baumes ist exponentiell
- Heuristiken finden nur lokale Optima
- anfällig für Overfitting
- nicht immer eindeutig

Um die Prognosegüte von Entscheidungsbäumen zu verbessern, existieren die Verfahren Stacking, Bagging und Boosting. Erklären Sie anhand von Beispielen diese Verfahren

- Stacking
  - unterschiedliche Algorithmen auf den gleichen Datensätzen kombinieren (Häufigste Entscheidung gewinnt)
  - z.B. KNN, SVM, Entscheidungsbäume
- Bagging
  - gleicher Algorithmus auf unterschiedlichen Datensätzen (Häufigste Entscheidung gewinnt)
  - z.B. Random Forest
- Boosting
  - Training auf initialem Datenset, anschließend werden falsch klassifizierte Daten erneut trainiert (Gewichtung der Entscheidungen; schwer nachvollziehbar)

### 26

## Bias / Varianz Tradeoff / Overfitting

### 27

### 28

Der Bias-Varianz-Tradeoff ist ein zentrales Problem beim überwachten Lernen. Erklären Sie das zugrundeliegende Problem.

- Idealerweise möchte man ein Modell wählen, das sowohl die Regelmäßigkeiten in seinen Trainingsdaten genau erfasst, als auch gut auf neue Daten verallgemeinert. Leider ist es normalerweise unmöglich, beides gleichzeitig zu tun.

Erläutern Sie anhand einer Graphik die Methode der Bias-Varianz-Zerlegung

![Bias_and_variance_contributing](Bias_and_variance_contributing.png)

Bias-Error:

- Unterschied zwischen dem erwarteten Wert des Modells und dem wahren Wert
- übermäßige Vereinfachung der Annahmen -> Modell lernt die Muster nicht

Varianz-Error:

- Das Modell lernt die Muster der Trainingsdaten auswendig und kann nicht auf neue Daten verallgemeinern

Bias-Varianz-Tradeoff Methode: Finden des Sweet-Spots zwischen Bias und Varianz.

### 29

## NLP

### 30

Erklären Sie was unter Natural Language Processing (NLP) verstanden wird.

- Verarbeitung und Analyse von natürlicher Sprache durch Computer
- Teilgebiet der KI, Informatik und Linguistik

Geben Sie ein Anwendungsbeispiel aus dem NLP an und erläutern Sie.

- Informationen & Erkenntnisse aus Dokumenten extrahieren

### 31

Erklären Sie das allgemeine Vorgehen bei Text-Mining Anwendungen, bei denen mit Hilfe einer Term-Document-Matrix ein Sentiment-Score ermitteln wird.

1. Kleinschreibung, Stoppworte, Punktation entfernen
1. Jedes Dokument in einzelne Wörter zerlegen
1. Wort mit der Positiv- und Negativliste vergleichen
1. Bei Match wird der Score entsprechend der Positiv- und Negativliste erhöht/reduziert

Führen Sie die einzelnen Schritte anhand des folgenden Beispiels durch und geben Sie an, welches der Aussagen die beste Bewertung erhält.

![NLP_Example](NLP_Example.png)

- "... lange ..." -> -0.2
- "Alles ..." -> 0.2
- "... abgelehnt ... zufrieden ... nachvollziehbar" -> -0.3 + 0.4 + 0.3 = 0.4
- "... schnell" -> 0.5
- "... alles ... allem zufrieden" -> 0.2 + 0.2 + 0.4 = 0.8

Der Satz "... alles ... allem zufrieden" erhält die beste Bewertung.

## Aussagenlogik

### 32

Wie ist die Syntax einer Aussagenlogik formal definiert?

- $A,B,C,...$ sind Aussagen
- $\top, \bot$ sind Aussagen
- Wenn $\phi, \psi$ bereits Aussagen sind, dann sind auch $\neg \phi, (\phi \land \psi), (\phi \lor \psi), (\phi \rightarrow \psi), (\phi \leftrightarrow \psi)$ Aussagen

Welche 5 Operatoren stehen bei der Aussagenlogik zur Verfügung? Geben Sie hier jeweils ein Beispiel an.

- $\neg$ Negation: nicht krank
- $\land$ Konjunktion: Ich bin krank und gehe zum Arzt
- $\lor$ Disjunktion: Ich gehe zum Arzt oder der Arzt kommt zu mir (oder beides)
- $\rightarrow$ Implikation: Wenn ich krank bin, gehe ich zum Arzt
- $\leftrightarrow$ Äquivalenz: Ich gehe zum Arzt, wenn ich krank bin und ich bin krank, wenn ich zum Arzt gehe

### 33

### 34

### 35

### 36

Erläutern Sie warum aussagenlogische Formeln in eine Konjunktive Normalform (KNF) überführt werden und wie diese definiert sind.

- um automaische Beweisverfahren einfach zu halten

1. besteht aus Konjunktionen von Klauseln
1. Klausel besteht aus Disjunktionen

Führen Sie folgende Klauselmenge in eine KNF und geben Sie bei jedem Schritt an welche Operation Sie eingesetzt haben

$(S \lor N) \land ((\neg S \land N ) \lor (P \land \neg S)) \land (\neg N \lor P)$

1.Distribution  
$(S \lor N) \land (\neg S \land (N \lor P)) \land (\neg N \lor P)$

2. Klammern entfernen

$(S \lor N) \land \neg S \land (N \lor P) \land (\neg N \lor P)$

3. Distribution

$(\neg S \land S) \lor (\neg S \land N) \land N \lor \neg S \land P \land \neg N \lor P$

4. Vereinfachung  
$ (\neg S \land N) \land N \lor \neg S \land P \land \neg N \lor P$

### 37

## Prädikatenlogik

### 38

### 39

### 40

### 41

### 42

### 43

## Fuzzy Logik/ Wissensbasierte Systeme /Expertensysteme

### 44

### 45

### 46

### 47

### 48

## Agenten

### 49

### 50

### 51

### 52

### 53

### 54

### 55
