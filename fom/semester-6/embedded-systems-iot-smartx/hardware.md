---
title: Hardware
published: 1
date: 2024-03-04T19:34:33.207Z
tags: 
editor: markdown
dateCreated: 2024-03-04T19:34:33.207Z
---

# Hardware

## Achritekturen

### John von Neumann Architektur

[siehe auch](/fom/semester-5/betriebssysteme/hardware-und-ein-ausgabe.md#von-neumann-architektur)

- bis heute verwendet
- binäre Datencodierung
- Programmierbarkeit
- Daten und Programm im selben Speicher
- Daten werden über berechnete Adressen angesprochen

Nachteile:

- Flaschenhals beim Speicherzugriff
- eingeschränkte Echtzeitfähigkeit
- Sicherheit reduziert

Aufgaben der CPU:

- Fetchen und Verarbeiten von Befehlen
- Befehlscodierung und Ausführung
- Verwalten der Ausführungszyklen
- Kontrolle von Zuständen und Flags
- Verwaltung von Interrupts & Exceptions

Steuerprozessor (CU - control unit):

- Adress- & Befehlsregister
- Steuer- & Statusregister
- Befehlszähler
- Befehlsdekodierung

Rechenprozessor (ALU - arithmetic logic unit):

- Datenregister
- Zustandsregister (Carry, Overflow, Zero, ...)
- Rechenoperationen
  - Arithmetik
  - Logik

Gleitkommaeinheit (FPU - floating point unit):

- Datenregister
- Numerik-Rechenwerke
- Ausnahmebehandlung

Zyklus:

1. Fetch -> Laden des Befehls
1. Decode -> Dekodieren des Befehls
1. Datenabruf
1. Execute -> Ausführen des Befehls
1. Writeback -> Schreiben des Ergebnisses

> Moderne Mikroprozessoren verwenden Pipelining & Superskalarität, um mehrere Befehle gleichzeitig auszuführen
{.is-info}

![Von Neumann Zyklus](/fom/semester-6/embedded-systems-iot-smartx/von-neumann-zyklus.png)

Befehle und Speicher aus gleichem Speicher via gleicher Bus

- häufig bei Mikrocontroller
- flexibler
- Beispiele:
  - ATmega Serie (Hersteller: Microchip)
  - PIC Serie (Hersteller: Microchip)
  - STM32 Serie (Hersteller: STMicroelectronics)

### Harvard Architektur

- Elektromechanisch (Relais)
- Daten und Befehle in getrennten Speichern
- getrennte Busse für Daten und Befehle
- Einsatz: Digital-Signal-Processing
- Schneller und nicht konkurrierender Zugriff

> Heutzutage meist als modifizierte Harvard Architektur (nur getrennte Caches,Befehlsspeicher für (statische) Daten, Laden von Befehlen aus jedem Speichersegment, Beschreiben des Befehlsspeichers)
{.is-info}

## Mikrocontroller

### Mikrocontroller vs. Mikroprozessor

- Mikrocontroller
  - CPU + Peripherie (Speicher, Timer, Kommunikationsschnittstellen) in einem Gehäuse
  - benötigt idealerweise nur eine Stromversorgung
  - dedizierte Aufgaben (z.B. Steuerung Waschmaschine)
  - Bauform
    - DIP (Dual Inline Packaging) -> rechteckig
    - SMP (Surface Mount Packaging) -> quadratisch
  - Clock (Taktgeber)
    - intern -> kompakt
    - extern -> stabiler und klareres Signal

- Mikroprozessor
  - reine Datenverarbeitung
  - benötigt externe Peripherie
  - höhere Rechenleistung (z.B. PC, Server)

### Peripherie

#### Timer / Counter

- regelmäßiges Auslösen von Interrupts z.B. bei Overflow, Wertevergleich
- Varianten
  - Up-/Down-Counter
  - Capture/Compare-Einheiten (CCU)
  - als Coprozessor zur Zähler- und Zeitgeber-Steuerung
- Komponenten
  - Zählregister
  - Vergleichsoperator
  - Output-Compare-Register
  - Kontrollregister -> Bestimmt Operationsmodus
  - Vorteiler (VT) -> Anzahl der Takte bis zum Inkrementieren des Zählregisters

Anwendungen:

- PWM (Pulse Width Modulation)
- Schrittmotorsteuerung
- Kommunikationsprotokolle

#### Watchdog

- Erkennung von Abstürzen oder Verklemmungen
- Programm setzt regelmäßig ein den Watchdog zurück
- Programmierbare Zeitspanne innerhalb der ein Reset ausgelöst werden muss
- Wichtig bei sicherheitskritischen Anwendungen
- Modi (Event bei nicht zurücksetzen)
  - Reset
  - ISR
  - Reset und ISR

#### PWM – Pulse-Width Modulation

- Verbunden mit Timer
- Verhältnis von An- und Ausschaltzeit -> Duty Cycle
- Leistung entspricht dem Integral
- hohes Störpotential
- Steuerung von Motoren, LEDs, etc.

![PWM](/fom/semester-6/embedded-systems-iot-smartx/pwm.png)

#### GPIO – General Purpose Input/Output

- Grundlegende digitale Schnittstelle
- entweder Eingang oder Ausgang
- Funktion wird durch Software bestimmt
- Synchrone und asynchrone Schnittstellen
  - Synchron -> eigene Taktquelle
  - Asynchron -> mit mehreren Leitungen

#### Interrupts

- ermöglichen schnelle Reaktion auf Ereignisse
- Signal bewirkt Unterbrechung des normalen Programmablaufs
- Ruft ISR (Interrupt Service Routine) auf

> Bei mehreren Interrupts ist eine Priorisierung notwendig
{.is-info}

#### DMA (Direct Memory Access)

- Transport von Daten zwischen Peripherie und Speicher ohne CPU
- nach Transfer wird ein Interrupt ausgelöst
- Wichtig für Echtzeitanwendungen

#### ADC – Analog/Digital Converter, DAC – Digital/Analog Converter

- grundlegende analoge Schnittstellen
- Auflösung und Wandlungszeit bestimmen Qualität des Wandlers
- mit abnehmender Wandlungszeit steigt Hardwareanforderung

#### Shannon‘s Theorem

C - achievable channel capacity  
B - bandwidth of the line  
S - average signal power  
N - average noise power  

$C = B * \log_2[1 + \frac{S}{N}][bp s]$

#### Shannon-Nyquist Theorem

- Fsampling – Abtastfrequenz
- Fin – Frequenz vom Eingangsignal

$F_{sampling} >= 2 * F_{in}$

## Peripherie
