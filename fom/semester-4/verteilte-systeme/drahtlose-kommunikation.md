---
title: Drahtlose Kommunikation
published: 1
date: 2023-04-18T20:26:30.207Z
tags: 
editor: markdown
dateCreated: 2023-04-18T20:26:30.207Z
---

# Drahtlose Kommunikation

## Kommunikationstechnologien

Relevante Technologien:

- Bluetooth
- WLAN
- Mobilfunk

> Reflektion und Interferenzen machen drahtlose Kommunikation schwierig.
{.is-info}

SNR (Signal-to-Noise-Ratio) ist ein Maß für die Qualität einer drahtlosen Verbindung.

BER (Bit-Error-Rate) ist ein Maß für die Anzahl der fehlerhaften Bits.

CDMA (Code-Division-Multiple-Access)

- Mehrere Nutzer können gleichzeitig auf einer Frequenz senden
- Jeder Nutzer hat einen eigenen "Chipping" Code
- Signal wird mit dem Chipping Code codiert

FDD (Frequency-Division-Duplex)

- Separate Empfangs- und Sendefrequenzblöcke
- Kann parallel Senden und Empfangen
- hohe Reichweite

TDD (Time-Division-Duplex)

- zeitlich gestaffeltes Senden und Empfangen
- MIMO/Beamforming einfacher zu implementieren

## Drahtlose und mobile Netze

### GSM und UMTS

Zellulare Netzarchitektur:

- MSC (Mobile Switching Center)
  - verbindet Zellen mit dem WAN
  - verbindet Verbindungsaufbau
  - verwaltet Mobilität
- Zellen
  - deckt physische Region ab
  - mobile Benutzer werden über Basisstation ans Netz angebunden

GSM (Global System for Mobile Communications):

- Teilt Spektrum in in Kanäle auf
- Teilt jeden Kanal in Zeitschlitze
- Jeder Benutzer bekommt 1-n Kanäle zugewiesen

UMTS (Universal Mobile Telecommunications System):

- Überlagerung einzelner Datenströme auf der gleichen Frequenz
- Scrambling Code zur Unterscheidung der Zellen (DOWNLINK)
- Jeder Benutzer bekommt pro Funkzelle einen Scrambling Code zugewiesen
- Benutzer kann nur senden wenn der Scrambling Code das zulässt

### Basisstationssteuerung

- Vermittlungsrechner mit Relaisfunktion
- Knotenpunkt von mehreren BTS (Base Transceiver Station)
- Zuweisung von Funkkanälen
- Routing zwischen BTS und MSC

![Basisstationssteuerung](/fom/semester-4/verteilte-systeme/bts.png)

Handoverarten:

- Intrazellenübergabe (stellt Verbindung wieder her)
- Interzellen- /Intra-BSC Übergabe (Verbindung wird auf andere Zelle übertragen)
- Inter-BSC-/Intra-MSC-Übergabe (Verbindung wird auf andere BSC übertragen)
- Inter-MSC-Übergabe (Verbindung wird auf andere MSC übertragen)

Mobile Originated Call (MOC):

1. MS sendet Verbindungsaufforderung
1. BSC leitet Verbindungsaufforderung an MSC weiter
1. MSC prüft ob Teilnehmer für den Dienst berechtigt ist
1. Prüfung ob ausreichend Ressourcen vorhanden sind
1. MSC baut Verbindung auf

### LTE & 5G

LTE (Long Term Evolution):

- Breitbandige Anbindung der BS an das Kernnetz
- Basisstation-Verbindung mit Glasfaser und/oder Richtfunk
- mehrere Mobilefunkstationen als Relaisstationen

5G:

- Oberbegriff für künftige Anforderungen
- beschreibt eine neue Generation
- nicht nur Mobilfunk, sondern auch Kommunikationsstandard
- Anwendungsfelder:
  - Enhanced mobile broadband (schnelleres Datennetz)
  - Massive machine-type communications (viele Verbindungen)
  - Ultra-reliable and low-latency communications (geringe Latenz, hohe Zuverlässigkeit)

### WLAN

- aktuell 802.11ax (WiFi 6)
- Diffusionsnetz (jeder kann Funkwellen empfangen)
- Medienzugriff über CSMA/CA
  - ermöglicht gemeinsamen Zugriff auf das Medium
  - Empfänger korrekter Daten wird bestätigt
  - bei Fehler wird die Übertragung wiederholt

- Ad-hoc-Modus
  - Verbindung zwischen 2 Geräten
  - keine Struktur
  - kein Access Point
  - Peer to Peer

- Infrastrukturmodus
  - Verbindung über Access Point
  - Access Point dient als Bridge zum drahtgebundenen Netz
  - kann bei zentraler Aufstellung Reichweite verdoppeln (steht in der Mitte)

- Verschlüsselung
  - WPA3 (aktuell)

### Bluetooth

- PAN (Personal Area Network) / WPAN (Wireless Personal Area Network)
- Reicheweite ca. 10m
- Übertragungsraten:
  - Synchrone Verbindung: 64 kbit/s
  - Asynchrone Verbindung: 721 kbit/s

### RFID

- Identifikation über Funk
- Erzeugt über Antenne ein elektromagnetisches Feld
- Kontaktloser Lesender Zugriff
- Aktive und passive Tags
- Probleme mit Datenschutz und Herstellerkosten

### LoRaWAN

- Long Range Wide Area Network
- energieeffizientes Senden über lange Strecken
- Sensoren können 10 Jahre mit einer Batterie betrieben werden

### UWB (Ultra Wide Band)

- kurze Reichweite (ca. 200m)
- hohe Refresh-Rate (200-1000x pro Sekunde)
- Echtzeit Tracking
- geringer Energieverbrauch
- schlüssellose Zugangssysteme, Assest Finding, Teilen von mobilen Daten

### direktes vs. indirektes Routing

direktes Routing:

- Teilnehmer wird ermittelt
- Paket wird direkt an den Teilnehmer gesendet

indirektes Routing:

- Status des Teilnehmers wird über Mittelsmann ermittelt
- Kommunikation über Mittelsmann

<!-- TODO: GSM -->
