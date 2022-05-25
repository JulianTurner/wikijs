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


## Diskrete Warscheinlichkeitsverteilungen
### Diskrete Zufafallsvariablen und diskrete Verteilung
- diskrete Zufallsvariable nur isolierte Werte(z.B. 1,2,3,4)
- Verteilung nennt sich auch **Wahrscheinlichkeitsverteilung**

### Warscheinlichkeitsfunktion
mit dem Term für Wahrscheinlichkeit $p_i = P(X =i)$
kann man:
- Verteilung graphisch darstellen
- Maßzahl der Lage und Streuung berechnen

### Erwartungswert: ein Lageparamter
Der Erwartungswert ist eine Maßzahl zur Charakterisierung einer Wahrscheinlichkeits­verteilung.
Der Erwartungswert beschreibt die zentrale Lage einer Verteilung.
 
$E(X) = \displaystyle\sum_{i}x_i*P(X=x_i)$

Beispiel Würfel:

$i$ Anzahl der Werte (6 seitiger Würfel mit 6 Werten = 6)  
$P$ Wahrscheinlichkeit des Wurfes  
 (Fairer Würfel $\frac{1}{6}$ oder $\frac{Anzahl \space des \space Wertes}{Anzahl \space aller \space Werte}$)  
$X$ Zufallsvariable
&#8203;



Augenzahl $x_i$ &#8203;| 1 | 2 | 3 | 4 | 5 | 6
---------|----------|---------|---------|----------|---------|---------|
 $P(X=x_i)$  &#8203; | $\frac{1}{6}$ &#8203; | $\frac{1}{6}$ &#8203; | $\frac{1}{6}$ &#8203; | $\frac{1}{6}$ &#8203; | $\frac{1}{6}$ &#8203; | $\frac{1}{6}$ &#8203;
 
&#8203;



## Verteilungen

### Binomialverteilung
Ein binomialverteiltes Zufallsexperiment entsteht durch n-fache Wiederholung eines Bernoulli Experiments. **Man unterscheidet nur zwischen Erfolg und Nicht-Erfolg.**

Wenn ein binomverteiltes Experiment aus n Versuchen besteht, wobei jeder Versuch eine Wahrscheinlichkeit von p hat, dann ist die Wahrscheinlichkeit für k Erfolge:

$P(X=k) = \binom{n}{k}* p^k * (1-p)^{n-k}$  

Der Binominalkoeffizient $\binom{n}{k}$ berechnet für uns die Anzahl der Möglichkeiten, wie k Objekte in einer Gruppe aus n ohne Wiederholung angeordnet werden können.

Beispiel Befragung:
$n$ = Alle Befragten  
$p$ = Warscheinlichkeit (zwischen 0 und 1, 1 = 100%)  
$k$ = Anzahl der Erfolge

&#8203;

### Poissonverteilung
Die Wahrscheinlichkeit für die Zufallsvariable X der Poisson-Verteilung wird durch folgende Formel berechnet:

$P(X=x)=\frac{\lambda^x}{x!} \cdot e^{-\lambda},\quad x \in\mathbb{N}_0$

Beispiel Befragung:
$λ$ = ist der Erwartungswert an Gästen in einem Zeitraum  
$x$ = Anzahl der Gäste  
$P$ = Wahrscheinlichkeit für $x$ Gäste zu einem Zeitpunkt  



$λ$ manchmal $µ$


Da der Binomialkoeffiziert bei größeren Werten nur unter erhöhtem Rechenaufwand – selbst für moderne Computersystem – zu berechnen ist, kann man die Poisson-Verteilung benutzen, um die Binomialverteilung anzunähern. Man benutzt die Poisson-Verteilung im allgemeinen zu Annäherung der Binomialverteilung, wenn $n$ groß ist und $p$ klein. Als Erwartungswert $µ$ der Poisson-Verteilung verwenden wir $µ = λ = n · p$.

Wird vor allem dort eingesetzt, wo die Häufigkeit eines Ereignisses über eine gewisse Zeit betrachtet wird.