---
title: Speicher(-verwaltung)
published: 1
date: 2023-09-13T19:14:14.207Z
tags: 
editor: markdown
dateCreated: 2023-09-13T19:14:14.207Z
---

# Speicher(-verwaltung)

- damals Absolute Adressierung
- heute Relativer Adressierung mit Basisadresse
  - Code im Hauptspeicher ist verschiebbar
  - Trennung von logischen und physikalischen Adressen
  - Programme, Bibliotheken, Treiber, etc. werden an beliebige Basisadresse geladen
  - Hauptspeicher-Aufteilung zwischen Betriebssystem und Prozessen
    - Speicher vergeben und zurücknehmen
    - Speicherbereiche schützen (Zugriffsrechte)
    - Buchhaltung über Speicherbelegung (Frei/Belegt)

## Speicherhierarchie

- flüchtig (nicht persistent)
  - Register (KiB)
  - Cache (MiB)
  - RAM (GiB)
- nicht flüchtig (persistent)
  - HDD/SSD (TiB)
  - USB Sticks
  - CD/DVD
  - Band

> Kosten steigen mit der Geschwindigkeit, Zugriffszeit steigt mit Kapazität
{.is-info}

## Hauptspeicher

- jedes Byte hat eigene Adresse -> lesen & schreiben
- Adressraum beginnt bei 0
- CPU & E/A Geräte greifen auf Hauptspeicher zu

> CPU kann nur auf Hauptspeicher zugreifen, nicht auf Festplatte
{.is-info}

### Zu wenig schneller Speicher (RAM)

- RAM Speicher Verwaltung -> statische/dynamische Partition pro Prozess
  - je ein Bereich für Betriebssystem und Prozesse
  - Schutz des Betriebssystems durch Bereichsüberwachung
- Swapping ganzer Prozesse auf Festspeicher
- Virtueller Speicher(Paging) -> nur unwichtige Pages werden ausgelagert

<!-- S. 215 -->