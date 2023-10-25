---
title: Modellbildung
published: 1
date: 2023-10-11T20:06:54.207Z
tags: 
editor: markdown
dateCreated: 2023-10-11T20:06:54.207Z
---

# Modellbildung

Prozess der Modellbildung:

1. Beschreibung des Systems (Systemfunktionen, Systemstruktur)
2. Modellbildung
3. mathematische Modellbeschreibung

Anforderungen an ein Modell:

- physikalische Transparenz
- Modellgültigkeit
- Effizienz

Eigenschaften eines Modells:

- Abbild / Repräsentation der Realität
- wesentliche Eigenschaften des Originals
- eingeschränkte Gültigkeit

## Symbolische Elemente eines Mechanischen Systems

```mermaid
graph TD

M[Mechanisches System]
T[Trägheit]
E[Elastizität]
R[Reibung]
K[Kraft/Moment]
STA[Starrer Körper]
ELA[Elastischer Körper]
F[Feder]
D[Dämpfer]
G[Gelenke]
S[Stellglieder]

M --> T
M --> E
M --> R
M --> K
T --> STA
T --> ELA
E --> ELA
E --> F
R --> D
K --> G
K --> S
```

## Einmassenschwinger (ein Freiheitsgrad)

![Einmassenschwinger](Einmassenschwinger.png)

> Speicher sind Feder und bewegte Masse
{.is-info}

## Generalisierte Variablen

- Systeme sind Aufnehmer für Leistung
- Leistung: $P$
- Effort: $e$
- Flow: $f$
- $P = e \cdot f$
![Leistungsvariablen](Leistungsvariablen.png)

- Elektrische Leistung: $P = U \cdot I$
  - Effort: $U$ (Spannung => Potentialdifferenz)
  - Flow: $I$ (Strom)
- Mechanische Leistung (Translation): $P = F \cdot v$
  - Effort: $F$ (Kraft)
  - Flow: $v$ (Geschwindigkeit)
- Mechanische Leistung (Rotation): $P = M \cdot \omega$
  - Effort: $M$ (Drehmoment)
  - Flow: $\omega$ (Winkelgeschwindigkeit)
- Hydraulische Leistung / Fluidik: $P = \Delta p \cdot \dot{V}$
  - Effort: $\Delta p$ (Druckdifferenz)
  - Flow: $\dot{V}$ (Volumenstrom)
- Thermische Leistung: $P = \Delta T \dot{S}$
  - Effort: $\Delta T$ (Temperaturdifferenz)
  - Flow: $\dot{S}$ (Entropiestrom)

## Zustands-Tetraeder

![Tetraeder](Tetraeder.png)

- $e$ = Effort
- $f$ = Flow
- $p$ = Impuls
- $q$ = Verschiebung
