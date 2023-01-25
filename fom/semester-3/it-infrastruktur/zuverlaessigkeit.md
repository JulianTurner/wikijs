---
title: Zuverlässigkeit, Redundanz
description: 
published: 1
date: 2022-11-21T19:18:44.313Z
tags: 
editor: markdown
dateCreated: 2022-11-15T19:29:01.687Z
---

# Zuverlässigkeit, Redundanz

## Zuverlässigkeit

MTBF beschreibt wie lange ein Objekt durchschnittlich zwischen zwei Ausfällen arbeitet.

- $MTBF = \frac{\Sigma(Betriebszeit)}{Anzahl \; Ausfälle}$
- $MTBF_{seriell} = \frac{1}{\frac{1}{MTBF_a}+\frac{1}{MTBF_b}+ \frac{MTTR}{MTBF_a * MTBF_b}}$

- $MTBF_{parallel} = \frac{MTBF_a * MTBF_b}{MTTR} + MTBF_a + MTBF_b$

> Zuverlässigkeit ist die Eigenschaft eines Systems, die angibt, dass eine System ununterbrochen und fehlerfrei arbeitet.
{.info}

## Wartbarkeit

MTTR beschreibt wie lange ein Objekt durchschnittlich repariert werden muss um wieder zu funktionieren.

- $MTTR = \frac {Ausfallzeit}{Anzahl \; Ausfälle}$

Wartbarkeit erhöht sich mit:

- Monitoring
- Hot-Swap
- Verfügbarkeit von Ersatzteilen
- Einfacher Zugang

## Verfügbarkeit

Verfügbarkeit ist die Wahrscheinlichkeit, dass ein Objekt verfügbar ist.

- $A = \frac{MTBF}{MTBF + MTTR}$
- $A = 1- W_{Ausfall} = 1- \frac{Ausfallzeit}{Gesamtzeit}$

### Verteilte Systeme

- $A_{gesamt} = A_a * A_b = \displaystyle \prod_{i=1}^{n}A_i$

> Auswirkungen hängen vom Kontext ab. Heimserver vs. AKWs
{.is-info}

### Verfügbarkeit von Systemen

Bei redundanten Systemen multiplizieren sich die Ausfallwahrscheinlichkeiten

- $A_{redundant} = 1- \displaystyle \prod_{j=1}^{m}(1-A_j)$