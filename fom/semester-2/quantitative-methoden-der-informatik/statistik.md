---
title: Statistik
description: 
published: 1
date: 2022-06-10T18:57:56.968Z
tags: 
editor: markdown
dateCreated: 2022-05-10T19:15:11.210Z
---

# Statistik

## Statistik als Wissenschaft

### Mittelwerte
Mittelwerte bewahren uns davor den Überblick zu verlieren

### Statistik als Wissenschaft
Statistik ist die Wissenschaft vom Argumentieren mit empirischen Zahlen.

Ziele der Statistik:
- Auffinden von Strukturen in Datenstätzen
- Erleichterung der Kommunikatuion (visualisierung)
- treffen von fundierten Entscheidungen
- Vorhersagen
- Verbindung zwischen Theorie umd Empirie
- aufzeigen notwendiger Daten


### Big Data

Anhaltspunkte die zu beachten sind:
- volume (Datenvolumen)
- velocity (Geschwindigkeit)
- variety (Quellen, Datentypen)
- veracity (Wahrheit)
- value (Mehrwert der Daten)

> Daten müssen vor der Analyse strukturiert werden.

### Statistik und der Computer
- manche Techniken mit Stift und Papier
- Statistik ist eine High-End-Wissenschaft und benötigt Software um effektiv zu sein
- Computer macht berechnungen
- Menschen übernehmen die Argumentation
- Elementare Analyse mit Spreadsheet (Excel, usw.)

### Deskriptive und induktive Statistik

Ziele der deskriptiven Statistik sind Daten zu:
- beschreiben 
- zusammenfassen
- darstellen

Daten sollten reduziert werden

> Reduzierung der Datenmenge auf das wichtigste
{.is-info}


Ziele der induktiven Statistik sind:
- schließen von Daten auf allgemeine Prinzipien (Beobachtungen)
- schließen auf unbeobachtes (statische Inferenz)

> Aufstellen von allgemeingültigen Regeln und Prinzipen
{.is-info}


### Schlussfolgerungen

Es gibt 2 Arten von Schlussfolgerungen:
- deduktiv:
	- top-down-Logik
	- basierend auf einem Prinzip

> Beispiel: bekannte Krankheit heilen

- induktiv:
	- bottom-up-Logik
	- basierend auf beobachteten Daten

> Beispiel: Impfstoff für unbekannte Krankheit erforschen

## Population und Variablen

Daten sind das Ergebnis von Beobachtungen wie:
- Zählvorgänge
- Messvorgänge
- komplexe Vorgänge



### Population, Variablen und Werte
Population ist die gesamtheit von Objekten (Elemente, Einheiten).

> Zielpopulation ist die Polulation für die man sich interessiert

Variable ist ein interessantes Merkmal (oder Attribut) eines Objektes

> Bei jedem Objekt nimmt die Variable einen Wert an

Beispiel:
Population = Kaufverträge
Objekt = Kaufvertrag
Variable = Betrag des Vertrages

Beispiel:

    Liste<Kaufvertrag> Kaufverträge{
        Kaufvertrag (Betrag des Vertrages)
        Kaufvertrag (Betrag des Vertrages)
    }


### Skalierung von Variablen 

Es gibt qualitative und quantitative Variablen.

#### kategorial (nominalskaliert) / qualitativ 
Von dem Wert lässt sich nur bestimmen ob er gleich ist oder nicht (z.b. boolesche Werte)

> Beispiel: true/false

#### Rangvariable (ordinalskaliert) / qualitativ
Werte können angeordnet werden.

> Beispiel: 1, 2, 3, 4, 5

> bei qualitativen Variablen ist ein Vergleich nur mit == und != möglich

#### metrisch (quantitativ)
Ergebis von einem Mess- oder Zählvorgang.

> Beispiel: Anzahl an Objekten in einer Population

- intervallskalierte Variablen wie z.B. Temeratur in Grad Celsius 
- verhältnisskalierte Variablen wie z.B. Temeratur in Kelvin, Prozent, Punkteanzahl in einer Klausur

> Bei quantitaive Variablen ist ein Vergleich mit >, <, >=, <=, == und != möglich
> Die meisten Variablen sind verhältnisskaliert 

Metrische Variablen nennt man...
- diskret, falls sie nur isolierte Werte annehmen können (Ganze Zahlen)
- stetig, falls sie beliebige Werte in einem Intervall annehmen können (Rationale Zahlen)

Die unterscheidung diskret/stetig ist wichtig für die Diagrammwahl.


kategorial / Rangvariable | metrisch diskret | metrisch stetig |
|-|---------|---------
Kreisdiagramm | Balkendiagramm | Stamm Blatt Diagramm 
Balkendiagramm | Säulendiagramm | Boxplot 
&#8203; | Kreisdiagramm | Histogramm

### Probleme bei der Definition von Variablen und Population
- Was ist eine geeignete Population?
- Wie kann eine Population definiert werden?
- Wie kann ein Objekt definiert werden?
- Unterscheidung Zielpopulation und Stichprobenpopulation

- Welche Variablen müssen definiert werden?
- Wie wird der Wert einer Variablen gemessen?


Grundanforderungen

Validität: 
     
	Eine Messung ist valide, wenn sie tatsächlich das misst, was sie messen soll und somit glaubwürdige Ergebnisse liefert.

Reliabilität: 

    Die Reliabilität bezieht sich darauf, ob deine Forschung bei wiederholter Durchführung zuverlässige Ergebnisse liefert.

Objektivität: 

    Eine Forschung ist objektiv, wenn keine ungewollten Einflüsse durch involvierte Personen entstehen.

### Validität & Reliabilität
- nicht leicht zu erfüllen
- interesse ist meistens bei Variablen mit <u>**nicht**</u> direkt messbarem Wert (latente Variablen)
- Forschung operationalisiert via manifeste Variablen (messbare Variablen) 

Beispiel für latente Variablen:
- Erwartungen eines Kunden
- Bonität eines Kunden
- Einstellung einer Person im Bezug auf die Umwelt

## Datensammlung

Grundstrategien:
- Beobachtung (Zählvorgänge, ...)
- Befragung (Fragebogen, Umfrage, ...)
- Experiment (AB-Test, Placebo-Test,...)

## Stichproben aus der Population
### Totalerhebung vs. Stichprobe
Totalerhebung(Zensus): Sammlung der Daten aus der gesamten Population
Teilerhebung(Stichprobe): Sammlung der Daten aus einer Teilpopulation

> Eine sorgfältige geplante Stichprobe kann besser sein als eine Totalerhebung.

### Was ist eine gute Stichprobe?

#### Zufallsstichprobe

Jede Stichprobe $n \in N$ ist eine reine Zufallsstichprobe, wenn jedes $n$ die gleich Chance hat, gezogen zu werden.

Vorteile:
- garantiert Repräsentativität
- erlaubt die Benutzung von induktiver Statistik

#### andere Stichprobe

- Zufallsstichprobe mit Schichtungsvariablen / stratified sampling
![](https://cdn.scribbr.com/wp-content/uploads/2020/09/stratified-sample-7-2048x863.png)

- Klumpen Stichprobe /  cluster sampling
![](https://cdn.scribbr.com/wp-content/uploads/2020/09/cluster-sample-step-1-1.png)
![](https://cdn.scribbr.com/wp-content/uploads/2020/09/cluster-sample-step-2-1.png)
![](https://cdn.scribbr.com/wp-content/uploads/2020/09/cluster-sample-step-3-1.png)

- Stichprobe "aufs Geratewohl(auf gut Glück)" / convenience smapling
es wird einfach der genommen der am einfachsten zu erreichen war

![](convenience_sample.png)

- Quotenten Stichprobe / quota sampling
es wird versucht eine Qute der Zielpopulation zu erreichen

![](quota_sample.png)

### Probleme bei der Stichprobe
- Telefonumfrage
- Antwortverweigerung
- preinliche Fragen
- Length Sampling Bias

> Was ist "Length Sampling Bias"?


> Beispiel im Supermarkt: Wenn man alle 10 Min einen Kandidaten an der Kasse befragt,
> ist die Chance einen mit vielen Produkten zu erwischen höher da er mehr Zeit an der Kasse verbringt.

### Repräsentativität
- Ziel: repräsentative Daten für Zielpopulation sammeln 
- Stichprobenfehler kontrollierbar
- nicht repräsentativ: Zusammenhang Auswahl-Chance & interessierte Variable

## Analyse von Daten

### Mögliche Fehler
- fehlerhafte Eingabe
- fehlende Werte
- Datum- & Zeitformat
- Inkonsistenzen

## Empirische Verteilung
$n$ beobachtungen einer Variable $X$:

$x_1, x_2, ..., x_n$

$k$ unterschiedliche Werte:

$a_1, a_2, ..., a_k$

**Absolute Häufigkeit**: Anzahl Beobachtungen von $a_j$ = $h(a_j)$
**Relative Häufigkeit**: $h(a_j) / n$ = $f(a_j)$
emprische Verteilung / Häufigkeitsverteilung = Liste Werte $a_j$ mit jeweiliger zugehöriger Häufigkeit 

## Diagramme
### Histogramm
Einteilung in $k$ Klassen

Jede Klasse: Untergrenze, Obergrenze & Breite
> Fläche der Klasse ist proprtional zur Zahl der Beobachtungen in der Klasse

> Unterschied zur Säule: Säule hat eine konstante Breite

***
### Boxplot
![boxplot.png](/fom/semester-2/quantitative-methoden-der-informatik/boxplot.png)
> Funktioniert immer bei stetigen Variablen

***
### Gestalt einer Verteilung

Die Gestalt betimmt die **Schiefe** & **Kurtosis (Wölbung)**
#### Schiefe
![](https://www.wiwiweb.de/assets/courses/media1/abb20-linksschiefe-verteilung-print.webp)
![](https://www.wiwiweb.de/assets/courses/media1/abb21-rechtsschiefe-verteilung-print.png)

#### Kurtosis
![kurtosis.png](/fom/semester-2/quantitative-methoden-der-informatik/kurtosis.png)

***
# Lage, Streuung und Gestalt einer Verteilung
## Askpekte der Verteilung einer metrischen Variable
- **Lage**: Wo liegen die Werte / Beobachtungen (Mitte der Werte)
- **Streuung**: Wie verstreut sind die Werte / Beobachtungen (um die Mitte)
![Abweichung](https://datatab.de/assets/tutorial/streuungsma%C3%9Fe.png)
***

## Charakterisierung der Lager einer Verteilung
**Modus / Modalwert**: häufigster Wert

> Bei metrisch stetigen Variablen ist die modale Klasse das Intervall mit der größten Häufigkeitsdichte
***
## Arithmetisches Mittel

Das arithmetische Mittel beschreibt die zentrale Lage einer Verteilung. 
Es handelt sich um einen sog. Mittelwert. Umgangssprachlich sagt man zum arithmetischen Mittel auch einfach <u>Durchschnitt</u>.


$\bar{x} = Summe \space  Bebobachtungen \space / \space Anzahl \space Beobachtungen$
&#8203;
***
## Median
Wert der in einer geordneten Daten in 2 Hälften teilt

> wird auch 50% Quantil genannt

## Arithmetisches Mittel & Median Vergleich
- beide messen die Lage einer Verteilung
arithmetisches Mittel:
- empfindlich gegen Ausreißer

Median:
- nicht empfindlich gegen Ausreißer

Skalierung:
- arithmetisches Mittel: metrische Variable
- Median: Rang- oder metrische Variable

> Faustegel: rechtsschiefe Verteilung: arithmetisches Mittel > Median

## Geometrisches Mittel

Im Gegensatz zum arithmetischen Mittel dient das geometrische Mittel zur **Messung des Durchschnitts einer prozentualen Veränderung**. Aus diesem Grund sagt man zum geometrischen Mittel auch <u>durchschnittliche Veränderungsrate</u>.

> $\bar{x}_{G} = \sqrt[Anzahl \space Werte]{Produkt \space Faktoren}$
{.is-info}

&#8203;


> Faktoren Bsp.:
> +50% => 1,5
> +20% => 1,2
> -50% => 0,5
> -20% => 0,8
{.is-info}


> typischer Anwendungsfall: Änderungsfaktoren
***
## Varianz
In der Statistik misst die Varianz die Abweichung vom Mittelwert. Zur Berechnung der Varianz, wird die Summe der quadrierten Abweichungen durch die Anzahl der Werte geteilt.

$Var = \sigma^2$

Die Varianz beschreibt also die quadrierte durchschnittliche Entfernung vom Mittelwert. Weil die Werte quadriert werden, hat das Ergebnis eine andere Einheit (eben die Einheit zum Quadrat) als die ursprünglichen Werte. Daher ist es schwer, die Ergebnisse in Bezug zu setzen.


$s^2 = \frac{1}{n} \displaystyle\sum_{i=1}^n \space (x_i - \bar{x})^2 = \frac{1}{n} \displaystyle\sum_{i=1}^n \space x_i^2 - \bar{x}^2$

> Varianz ist die Streuung um das arithmetische Mittel
***
## Standardabweichung


Die Standardabweichung gibt die Streubreite einer Variable rund um deren Mittelwert an. Damit ist die Standardabweichung die durchschnittliche Entfernung aller gemessenen Werte einer Variable vom Mittelwert der Verteilung.



![Abweichung](https://datatab.de/assets/tutorial/standardabweichung.png)

> $s = \sqrt{s^2}$
{.is-info}


> durchschnittliche Entfernung aller gemessenen Werte zum arithmetische Mittel
{.is-info}

## Unterschiede zwischen Standardabweichung und Varianz
Der Unterschied zwischen Varianz und Standardabweichung ist, dass die Standardabweichung die durchschnittliche Entfernung vom Mittelwert misst und die Varianz die quadrierte durchschnittliche Entfernung vom Mittelwert. Andersherum gesagt, die Varianz ist die quadrierte Standardabweichung und die Standardabweichung ist die Wurzel der Varianz.

Durch diese Quadrierung ergibt sich jedoch eine schwer zu interpretierende Kennzahl, da eben die Einheit nicht mit den Ausgangsdaten übereinstimmt. Aus diesem Grund ist es ratsam, zur Beschreibung einer Stichprobe stets die Standardabweichung heranzuziehen, da damit die Interpretation leichter von der Hand geht.
![UnterschiedeFormel](https://datatab.de/assets/tutorial/unterschied-Varianz-und-Standardabweichung.png)

[weitere Infos](https://datatab.de/tutorial/standardabweichung-varianz-spannweite)

***
## Sigma Regeln

1 Sigma Regel: Etwa 2/3
- $[\bar{x} - s, \bar{x} + s]$

2 Sigma Regel: Etwa 95%
- $[\bar{x} - 2s, \bar{x} + 2s]$

3 Sigma Regel: mehr als 99%
- $[\bar{x} - 3s, \bar{x} + 3s]$

![sigma-regeln.png](/fom/semester-2/quantitative-methoden-der-informatik/sigma-regeln.png)
&#8203;
***

### Normalverteilung
- Kurvenverlauf ist symmetrisch, Median und Mittelwert sind identisch
- 1 & 2 & 3 $\sigma$(Sigma) Regeln gelten
### Schiefe
$\gamma_1 = \frac{1}{n} \displaystyle\sum_{i}(\frac{x_i-\bar{x}}{s})^3$

$\gamma_1$ | Verteilung
---------|----------
 $= 0$ | symmetrisch 
 $> 0$ | rechtschief 
 $< 0$ | linkschief 

&#8203;

 ***
### Kurtosis

$\gamma_2 = \frac{1}{n} \displaystyle\sum_{i}(\frac{x_i-\bar{x}}{s})^4 - 3$

$\gamma_2$ | Verteilung
---------|----------
 $= 0$ | meso-kurtisch 
 $> 0$ | lepto-kurtisch  
 $< 0$ | platy-kurtisch  

&#8203;
