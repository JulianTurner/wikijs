---
title: Firmware
published: 1
date: 2024-03-04T19:34:52.207Z
tags: 
editor: markdown
dateCreated: 2024-03-04T19:34:52.207Z
---

# Firmware

## Einfache Firmware

- Typische Struktur
  - Initialisierung
  - Endlosschleife
- zeitliche Verzahnung
- Scheduling muss berücksichtigt werden
- Struktur von Subroutinen muss reentrant (wiedereintrittsfähig) sein
- Lange Berechnungen in Abschnitte aufteilen

Automatenstruktur:

- lässt sich in Programmcode umsetzen
- enum erhöht die Lesbarkeit

![Automat_Firmware](Automat_Firmware.png)

### Reentranz – Wiedereintrittsfähigkeit

Problem:

- Globale Variablen -> Wert kann sich vor Verwendung ändern

Lösung:

- Lokale Variablen (Stack)
- keine gemeinsamen Daten -> keine Race Conditions

> Interrupt-Service-Routinen (ISR) sollten reentrant sein und keine Interrupts zu verlieren
{.is-info}

<!-- S. 141 -->
