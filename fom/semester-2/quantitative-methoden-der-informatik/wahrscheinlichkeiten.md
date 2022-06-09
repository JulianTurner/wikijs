---
title: Wahrscheinlichkeiten
description: 
published: 1
date: 2022-06-09T15:12:06.290Z
tags: 
editor: markdown
dateCreated: 2022-05-23T16:58:04.676Z
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

> $X \sim B(n, p)$ 
> Die Zufallsvariable $X$ folgt der Binominalverteilung mit den Parametern $n$ und $p$

&#8203;

### Poissonverteilung
Die Wahrscheinlichkeit für die Zufallsvariable X der Poisson-Verteilung wird durch folgende Formel berechnet:

$P(X=x)=\frac{\lambda^x}{x!} \cdot e^{-\lambda},\quad x \in\mathbb{N}_0$

Beispiel Befragung:  
$λ$ = ist der Erwartungswert an Gästen in einem Zeitraum  
$x$ = Anzahl der Gäste  
$P$ = Wahrscheinlichkeit für $x$ Gäste zu einem Zeitpunkt   
$X$ = Zufallsvariable  



$λ$ manchmal $µ$


Da der Binomialkoeffiziert bei größeren Werten nur unter erhöhtem Rechenaufwand – selbst für moderne Computersystem – zu berechnen ist, kann man die Poisson-Verteilung benutzen, um die Binomialverteilung anzunähern. Man benutzt die Poisson-Verteilung im allgemeinen zu Annäherung der Binomialverteilung, wenn $n$ groß ist und $p$ klein. Als Erwartungswert $µ$ der Poisson-Verteilung verwenden wir $µ = λ = n · p$.

>Wird vor allem dort eingesetzt, wo die Häufigkeit eines Ereignisses über eine gewisse Zeit betrachtet wird.

&#8203;

> $X \sim Po(\lambda)$ 
> Die Zufallsvariable $X$ folgt der Poissonverteilung mit dem Parameter $\lambda$

&#8203;

### Normalverteilung

Bietet sich immer an, wenn Werte innerhalb eines begrenzten Intervalls liegen und es kaum Ausreißer gibt. Bei großen Stichproben einer Binomialverteilung kann diese durch eine Normalverteilung approximiert werden.  

Beschrieben mit 2 Parametern:  
- $\mu$: Dichte hat ihr maximum bei $\mu = x$ (Hochpunkt / zentrale Lage / $E(X) = \mu$)  
- $\sigma$: Wendepunkte sind bei $x= \mu \pm \sigma$
- $\sigma^2$: Varianz

&#8203;

> Die Normalverteilung ist immer eine symmetrische Verteilung  
&#8203;  
> $X \sim N(\mu, \sigma^2)$  
> Die Zufallsvariable $X$ folgt der Normalverteilung mit den Parametern $\mu$ und $\sigma^2$  
&#8203;

#### Standardnormalverteilung: $\mu = 0$ und $\sigma = 1$  
![](https://viles.uni-oldenburg.de/navtest/viles2/kapitel02_Theoretische~~lVerteilungen/modul02_Normalverteilung/ebene01_Konzepte~~lund~~lDefinitionen/STNV.png)
&#8203;


#### Standartisuerung
> Nur für die Standardnormalverteilung gibt es eine Tabelle (Formelsammlung s. 13)  
Wenn $X \sim N(\mu, \sigma^2) \neq N(0,1)$, dann können wir $X$ standardtisieren  
$Z = \frac{X-\mu}{\sigma} \sim N(0,1)$

#### Andere wichtige Eigenschaften
Stauchen (Strecken) / Verschieben einer Normalverteilung => Ergebnis erneut Normalverteilung

Diversität (z.B. Aktienportfolio-Optimierung)  
Wenn   
$X_1 \sim N(\mu_1, \sigma^2_1), X_2 \sim N(\mu_2, \sigma^2_2)$   
unabhänging sind dann gilt:  
$X_1 + X_2 \sim N(\mu_1 + \mu_2, \sigma^2_1 + \sigma^2_2)$   
Die Schwankungen einer Aktie wird von der Stabilität der zweiten aufgefangen.

#### Weitere wichitge Eigenschaften
Eine normalverteilte Zufallsvariable beobanchtet an $n$ verschiedenen unabhängigen Objekten.
Für jedes beobachtete Objekt hat die Zufallsvariable die gleiche Normalverteilung.
> $X_1, ..., X_n \sim N(\mu, \sigma^2)$   
> => Summe der Zufallsvariablen hat eine Normalverteilung $\displaystyle\sum_{i=1}^{n}X_i \sim N(n\mu, n\sigma^2)$   
> => arithmetisches Mittel ist ebenfals normalverteilt $\bar{X}=\frac{1}{n}\displaystyle\sum_{i=1}^{n}X_i \sim N(\mu,\frac{\sigma^2}{n})$  
&#8203;


## Stetige Wahrscheinlichkeitsverteilung
[Nützlicher Link](https://www.maths2mind.com/schluesselwoerter/verteilungsfunktion-stetiger-zufallsvariablen)

### Stetige Zufallsvariablen und stetige Verteilung
- stetige Zufallsvariable (X) kann jeden Wert annehmen
- Verteilung nennnt man **stetige Warscheinlihkeitsverteilung**

Beispiele:
- Tagesrendite beim DAX
- Reihnheitsgrad einer produzierten Chemie

### Berechnung von Warscheinlichkeiten
Warscheinlichkkeitsfunktion für stetige Zufallsvariablen ist **unbrauchtbar**.

> Man braucht die Dichte

### Dichte
Warscheinlichkeiten sind Flächen unter der Dichte  
Formel für die stetige Warscheinlichkeitsverteilung:  
$P(a \leq X \leq b) = \int_{a}^{b}f(x)dx$  
&#8203;

### Verteilungsfunktion
Gibt die Wahrscheinlichkeit an, dass eine Zufallsvariable X einen Wert der kleiner oder gleich x ist.
Entspricht Fläche unter der Dichtefunktion, bis zum Wert x (kumuliert).

$P(X \leq x) = \int_{- \infty}^{x}f(\zeta)d\zeta$  
&#8203;

### Erwartungswert (Lageparameter)
Der Erwartungswert $E(X)$ einer stetigen Zufallsvariable X gibt an, welchen Wert die Zufallsvariable X im Mittel bei einer unbegrenzten Wiederholung annimmt.  
$E(X) = \int_{-\infty}^{\infty}x*f(x)dx$  

### Varianz (Streuungsparameter)
Die Varianz ist die mittlere quadratische Abweichung der Zufallsvariablen von ihrem Erwartungswert und somit ein Streumaß  
$var(X) = \int_{-\infty}^{\infty}(x-E(X))^2*f(x)dx$  
&#8203;

# Mehr über Zufallsvariablen und ihre Verteilung

## Ziehen von Stichproben

Stichprobenziehung ist der Prozess der Auswahl von Objekten aus einer Population.

Ziel:
- Lernen über die Population
- mehr über die Verteilung einer Variable erfahren

Modell:
$X_1, ..., X_n$ iid, verteilt wie $X$   
iid => "independenly identically distributed" (unabhängig & gleichmäßig verteilt)

Wichtig ist:
- Stichprobenmittelwert $\bar{X} = \frac{1}{n}\displaystyle\sum_{i=1}^{n}X_i$  &#8203;

Kann zur Schätzung von $E(X)$ (Theoretischer Mittelwert) benutzt werden.

- Stichprobenvarianz $S^2 = \frac{1}{n}\displaystyle\sum_{i=1}^{n}(X_i-\bar{X})^2$ &#8203;
Kann zur Schätzung von $var(X)$ (Varianz) benutzt werden.

Intressant:
- Verteilungseigenschaften von $\bar{X}$ und $S^2$  
- Verhalten von von $\bar{X}$ und $S^2$ bei wachsendem Stichprobenumfang $n$
&#8203;
## Der Zentrale Grenzwert Satz (ZGWS)
### Binominalverteilung $B(n,p)$ bei großen $n$&#8203;
Ist $X \sim B(n,p)$ dann gilt approximativ für großes $n$:  &#8203;
$X \sim N(np, np(1-p))$
&#8203;

Beispiel:  
$B(100, 0.5)$ => 50 / 100  sagen JA  
$n = 100$  
$p = 0,5 (50\%)$  
$X \sim N(100*0.5, 100*0.5*(1-0,5))$  
$X \sim N(50, 25)$  
&#8203;

> Die Approxtimation ist gut falls für die Varianz $np(1-p)$ gilt:  
> $np(1-p) > 9$  
> (Datenverteilung muss breit genug sein) 

&#8203;

## Andere Verteilungen

### t-Verteilung

Vorraussetzungen:
- benutzt wenn Standardabweichung / Varianz unbekannt 
- Stichprobe muss zufällig entnommen sein
- Grundgesamtheit muss annähernd normalverteilt 

[Weitere Informationen zur t-Verteilung](https://welt-der-bwl.de/t-Verteilung)

