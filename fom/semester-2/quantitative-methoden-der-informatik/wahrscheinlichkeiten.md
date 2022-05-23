---
title: Wahrscheinlichkeiten
description: 
published: 1
date: 2022-05-02T17:37:44.824Z
tags: 
editor: markdown
dateCreated: 2022-03-08T19:21:23.407Z
---

# Wahrscheinlichkeiten

## Daten und stochastische Modelle

### Zufall
- weitere Stichproben = andere Auswahl

Induktike Statistik:
- bemüht um Antworten
- bruht auf Warscheinlichkeiten

> z.B. Würfelwurf - Stochastisches Model erzeugt Ergebnisse beim Würfelwurf
  
> $p$ und $\^p$ sind nicht das selbe denn $\^p$ ist der Schätzwert


### Beboachtungen und stochaistische Modelle
Beobachtungen(, , , )  Stochastische Model(, , , )


Beobachtungen | Zusammenhang | Stochastische Model
---------|----------|---------
&#8203; | -- statistische Inferenz -> | &#8203;
Variablen | &#8203; | Zufallsvariablen
beobachtete Werte | &#8203; | Wahrscheinlichkeiten
relative Häufigkeit | &#8203; | ihre Realisationen
empirische Verteilung | &#8203; | Wahrscheinlichkeiten-Verteilung
&#8203; | <- Zufallsexperimente -- | &#8203;
&#8203; | <- Computersimulationen -- | &#8203;



### Warum brauchen wir stochastische Modelle?
Stochastisches Modell:
- charaktisiert Population
- lernen mit Zufallsstichprobe
- Schätung repräsentiert Wissen über Population


## Wahrscheinlichkeitsrechnung

### Kolmogorovs Axiome

siehe Formelsammlung (S. 3)

## Wie kann man die Warscheinlichkeit eines Ereignisses finden?
#### Laplace Experiment

$P(A)= \frac{\# \space günstige \space Ergebnisse \space für \space A}{\# \space mögliche \space Ergebnisse}$

&#8203;  

Beispiel Würfel:  
P = Probability   
A = gewünschtes Ereignis (Würfelaugen, z.b 4)  
günstige Ergebnisse = Anzahl der Seiten mit 4  
mögliche Ergebnisse = Anzahl der Seiten  

#### Urnenmodell
> Wird die Kugel zurückgelegt?
> Spielt die Reihnfolge / Züge eine Rolle?

Reihnfolge von mehrern Ereignissen:  
$P(B|A)$ = **Wahrscheinlichkeit, dass B nach A kommt**  
$P(B|A) = \frac{P(A \cap B)}{P(A)}$ 


&#8203;

Ziehen:
- ohne zurücklegen => A und B sind abhängig
- ohne zurücklegen mit **vielen Kugeln** => A und B sind nahezu unabhängig
- mit zurücklegen => A und B sind unabhängig

&#8203;

Kleine Popolation + ziehen ohne zurücklegen => reduziert Unsicherheit
Große Popolation + ziehen ohne zurücklegen => ähnlich wie ziehen mit zurücklegen


## Verteilungen

### Binomialverteilung
Ein binomialverteiltes Zufallsexperiment entsteht durch n-fache Wiederholung eines Bernoulli Experiments. **Man unterscheidet nur zwischen Erfolg und Nicht-Erfolg.**

