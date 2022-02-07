---
title: Klausurvorbereitung
description: 
published: 1
date: 2022-02-07T13:59:55.448Z
tags: 
editor: markdown
dateCreated: 2021-12-16T19:53:55.468Z
---

# Klausurvorbereitung

# typische Datentypen

# grundlegende Rechnerarchitekturen beschreiben
## CISC
## RISC
## VLIW/EPIC
## Skalar & Vektorrechner
## Memory- Register Stackmachone
## grundlegendes Memorymanagment
## Interrupthandling
## DMA

# historische Entwicklung der Rechentechnik
# Schaltungen
## Logikgatter 
# IO- Subsysteme 
## Eigenschaften 
## grundlegende Implemantation
## passende Systeme für Anwesdungsfälle 
# Assemblerprogramme
# Aufgaben eines Betrienbssystems

## Betriebssysteme
---
S. 364
Was ist ein Betriebssystem?
- Ein Betriebssystem ist die zentrale Vermittlerschicht zwischen Hardware und Software

Welche Aufgaben haben Betriebssysteme?
- Verwaltung von Systemressourcen(Speicher, Prozessor, IO-Geräte)
- Erzeugen von Prozessen
- Kommunikation zwischen Prozessen
- uvm.

## Begriffe
S. 365
Welche Programme bilden ein Betriebssystem?
- Ressourcenverwaltung
- Ein- und Ausgabegeräte steuern (Treiber)
- System-Api
- Programm steuern (scheduling)
- Kommunikation zwischen Programmen
- Schutzmechanismen um Programme und Benutzer abzugrenzen
- uvm.

Welche Ebenen gibt es in Rechnern?
- Maschienenebene (Hardware), Systemprogramme (Betriebssystem), Anwendungsprogramme (Anwendungsprogramme)
- Reale Maschine (Hardware), Abstrakte Maschine (Betriebssystem), Benutzermaschine (Anwendungsprogramme)

## Geschichte
S. 370
Welche Generationen von Betriebssystemen gibt es?
0. Generation: Digitalrechner
1. Generation: Kein Betriebssystem
2. Generation: Batchbetrieb
3. Generation: Dialogsysteme
4. Generation: Betriebssysteme mit grafischer Oberfläche

### Generation 0
Digitalrechner

- keinerlei Programmspeicher
- Verdrahtung muss geändert werden
- Verarbeitung vorbereiteter Lochkarten

### Generation 1
Kein Betriebssystem

- Verdrahtung muss **nicht mehr** geändert werden
- Programmierung geschah in Maschiensprache

### Generation 2
Batchbetrieb 

- Entstehtung von Bibliotheken
- verfügen über einfache Betriebssysteme (Ein- und Ausgabeoperationen & Jobsteuerung)
- Batchbetrieb: mehrere Programme quasi parallel ausführen


### Generation 3
Dialogsysteme

- direkte Interaktion der Benutzer mit dem Rechner
- Entwicklung von "Timesharingsystemen" 
- Entwicklung von Minicomputer als Alternative zu Großrechnern
	- 32bit Super Minicomputer

### Generation 4
aktuelle Betriebssysteme

- GUI
- Netzwerke (Ethernet)
- Nutzer bekommen dedizierte Rechner
- Einführung der von Neumann Architektur
- Verschiendene Betriensarten
#### Betriebsarten
CPU Betriebsarten:
- Usermode & Kernelmode
	- Anwendungsprogramme keinen direkten Zugriff auf Ein-/Ausgabegeräte 
	- Indirekter Zugriff auf Ein-/Ausgabegeräte mit Sytemcalls

Komplexere CPU Betriebsarten:
-  User-, System-, Kernel- und Executive-Mode (Ringe)
	- Aufteilung der privilegierten Bereiche

#### Zentraleinheit - Zugriff auf Ein-/Ausgabegeräte

Memory mapped IO
- speicherbasierte Ein- und Ausgabe

Spezielle IO-Instruktionen
- Steuer- und Datenregister von Ein-/Ausgabegeräten nur mit 
Hilfe besonderer IO-Instruktionen möglich

Nennen Sie Vor- und Nachteile von memory mapped IO.
Vorteile:
- direkter Zugriff mit Hochsprache auf IO-Geräte
Nachteile:
- je mehr IO-Geräte verwendet werden, desto mehr Speicher wird benötigt

Nennen Sie Vor- und Nachteile der Verwendung spezieller IO-Operationen für den 
Zugriff auf die Steuer- und Datenregister von Peripheriegerätesteuereinheiten.
Vorteile:
- Sicherer: Betriebssystem stellt IO-Instruktionen bereit und überwacht die Nutzung ggf. unterbinden
Nachteile:
- kompatibles Betriebssystem oder extra Treiber wird benötigt

#### Zentraleinheit – Datentransfer
Techniken zum Datentransfer:

- Programmgesteuerte Übertragung
	- mit Software (Direkte Kontrolle des Betriebssytems)

- DMA
	- mit Hardware (dedizierte Steuereinheit)
	- entlastet die CPU

Nennen Sie Vor- und Nachteile der DMA-Technik
Vorteile:
- entlastet die CPU
Nachteile:
- zusätzliche dedizierte Hardware



Nennen Sie Vor- und Nachteile des Pollings
Vorteile:
- kompletter hardwarezustand erfassbar
Nachteile:
- hohe datenlast

Was ist ein Interrupt?
eine kurzfristige Unterbrechung der normalen Programmausführung, um einen kritischen Vorgang abzuarbeiten

Nennen Sie Vor- und Nachteile der Interrupttechnik
Fragt Daten beim Vorliegen von Daten ab

Vorteile:
- effieznt
Nachteile:
- Konflikte

Nennen Sie Vor- und Nachteile der programmgesteuerten Datenübertragung zwischen Hauptspeicher und Ein-/Ausgabegeräten
Vorteil: 
- keine dedizierte Hardware
Nachteile:
- Belastung der CPU

#### Hauptspeicher

Interleaving
- Aufteilung des Speichers in Bänke, die jeweils getrennte Adressgruppen umfassen

Caching
- Unterstützung des Hauptspeichers mit schnelleren Zwischenspeichern mit kürzerer Zugriffszeit


#### Ein- und Ausgabegeräte – Magnetbänder

Typisch für Magnetbänder sind ihr rein sequentieller Zugriffscharakter sowie ihre in der Regel gute Austauschbarkeit zwischen unterschiedlichen Systemen.

#### Ein- und Ausgabegeräte – Magnetplatten
Speicherung von Daten auf Magnetplatten

#### Ein- und Ausgabegeräte – SSD

Solid State Disks, kurz SSD: Alternative zu Magnetplatten für die Langzeitspeicherung 

#### Ein- und Ausgabegeräte – RAID
RAID, kurz für Redundant Array of Inexpensive Disks bzw. heute 
Redundant Array of Independent Disks zusammengefasst.

### Betriebssystemgrundfunktionen
Typischen Aufgaben eines Betriebssystems:
- Speicherverwaltung
- Prozessverwaltung
- Prozesssynchronisation
- Prozesskommunikation Devicetreiber
- Dateisysteme
- Interaktion mit den Benutzern