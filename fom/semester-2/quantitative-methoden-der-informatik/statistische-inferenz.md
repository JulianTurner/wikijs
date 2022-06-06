---
title: Statistische Inferenz
description: 
published: 1
date: 2022-05-02T17:37:44.824Z
tags: 
editor: markdown
dateCreated: 2022-03-08T19:21:23.407Z
---

# Statistische Inferenz
>Benutzt empirische Daten (Beobachtungen) um über *unbekannte Verteilungen* (oder unbekannte Parameter) zu lernen

> *unbekannte Verteilungen* charakterisiert gesamte Population

TODO: Link zu ### Beboachtungen und stochaistische Modelle in Warscheinlichkeiten

## Schätzung 
Methoden der statistischen Inferenz
- Punktschätzung von Parametern
- Intervallschätzung von Parametern
- Testen von Hypothesen über Parameter

### Punktschätzung 
unbekannte Parameter einer Verteilung wird mit einer einzigen Zahl ("Punkt") geschätzt

Vorteile:
- leicht verständlich
- leicht zu vermitteln

Nachteile:
- immer falsch
- zeigt nicht an wie genau die Schätzung ist

Besser Konfidenzintervall and Stelle Punktschätzer

### Intervallschätzung
unbekannte Parameter einer Verteilung wird mit einem Konfidenzintervall (Intervall von Zahlen) geschätzt

> Konfidenz = Vertrauen

Definition Konfidenzintervall:
- Verteilung $X$ hat einen unbekannten Parameter $\theta$
- Geplant ist eine Zufallsstichprobe von $n$ Einträgen von $X_1, ..., X_n$
- Intervall $[C1, C2] = [C1($X_1, ..., X_n$)]$   

$1-\alpha$ = Konfidenzniveau (Meist $1-\alpha = 0.95$)  
$\alpha$ = Irrtumswarscheinlichkeit (2,5% pro Seite)  
$\theta$ = unbekannter Parameter (ein Wert aus den möglichen Werten) 


![](https://datatab.de/assets/tutorial/Konfidenzintervall_95.png)

> Vor Stichprobe => Zufallsintervall  
> Nach Stichprobe => Intervall wurde beobachtet => Konfidenzintervall

> warscheinlichkeit, dass Zufallsintervall den wahren Wert $\theta$ enthält, soll groß

### Konfodenzintervall $p$

Standardisierung:
$P \left( -1,96 \leq \frac{\hat{p}-p}{\sqrt{(\frac{p(1-p)}{n})}} \leq 1,96 \right) = 0.95$  

Wenn $p$ unbekannt ist, verwenden wir $\hat{p}$  
$P \left(\hat{p} -1,96 \space \sqrt{\frac{\hat{p}(1-\hat{p})}{n}} \leq p \leq \hat{p} + 1,96 \space \sqrt{\frac{\hat{p}(1-\hat{p})}{n}} \right) = 0.95$ 

Intervall:

$\left[\hat{p} -1,96 \space \sqrt{\frac{\hat{p}(1-\hat{p})}{n}}, \space \hat{p} + 1,96 \space \sqrt{\frac{\hat{p}(1-\hat{p})}{n}} \right]$ 

> Formelsammlung S. 8

Anmerkungen:
- Jeder Wert im Konfidenzintervall => plausible Schätzung für unbekannten Parameter
- Präziseres 95% Konfidenzintervall => $n$ erhöhen (4 faches für doppelte Genauigkeit) 
- Höheres Konfidenzniveau (Bsp. 95% => 99,7%) =>  1.96 duruch 3 ersetzten (wg 3 $\sigma$) => Konfidenzintervall wird länger / ungenauer