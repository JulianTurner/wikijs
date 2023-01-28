---
title: Zuverlässigkeit, Redundanz
description: 
published: 1
date: 2023-01-28T10:14:20.487Z
tags: 
editor: markdown
dateCreated: 2023-01-25T19:02:44.455Z
---

# Zuverlässigkeit, Redundanz

## Zuverlässigkeit

MTBF beschreibt wie lange ein Objekt durchschnittlich zwischen zwei Ausfällen arbeitet.

- $MTBF = \frac{\Sigma(Betriebszeit)}{Anzahl \; Ausfälle}$ 
&nbsp;
- $MTBF_{seriell} = \frac{1}{\frac{1}{MTBF_a}+\frac{1}{MTBF_b}+ \frac{MTTR}{MTBF_a * MTBF_b}}$
&nbsp;
- $MTBF_{parallel} = \frac{MTBF_a * MTBF_b}{MTTR} + MTBF_a + MTBF_b$
&nbsp;
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

## Redundanz 

Verfügbarkeiten von Rechenzentren sind in vier Stufen aufgeteilt 

Tier I: 

- kleinere Unternehmen 
- einfach ausgelegte Strom- und Kühlsysteme
- keine redundanten Systeme 

Tier II: 

- mittelständische Unternehmen 
- einfach ausgelegte Strom- und Kühlsysteme 
- wenig Redundanz in Strom- und Kühlsystemen

Tier III: 

- große Unternehmen 
- Update und Wartung ohne Ausfall des Dienstes
- verfügen nicht über vollständige Redundanz 
- N + 1 Redundanz

Tier IV: 

- multi millionen Unternehmen 
- 2 unabändige Strom- und Kühlsysteme 
- vollständige Redundanz 2N + 1 

> Redundanz ist eine zusätzliche technische Ressource als Reserve
{.is-info}


