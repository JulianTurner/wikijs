---
title: Klausurvorbereitung
description: 
published: 1
date: 2022-02-08T12:23:35.428Z
tags: 
editor: markdown
dateCreated: 2021-12-16T19:53:55.468Z
---

# Klausurvorbereitung

# typische Datentypen
> Analag: Kontinurlischer Wertebereich
> Digital: Zifferndarstellung 

## Stellenwertsystem
Bei einem Stellenwertsystem ist die Position der Ziffer für die Wertigkeit entscheidend 
Zentrale Bedeutung hat die Basis. Im Dezimalsystem ist es die Basis 10.
Die Notwendigkeit eine 0 darstellen zu können. 
Die höchstwertige Stelle ist das **most significat digit** MSD
Die nierderwertigste Stelle ist das **least significat digit** LSD 

Beispiel:
$z_3 = 1, z_2 = 2, z_1, z_0 = 4, basis = 10$
$10^3 = 1000 \\ 10^2 = 100 \\ 10^1 = 10 \\ 10^0 = 1$
$w = 1*10^3+2*10^2+3*10^1+4*10^4$
$w = 1234$

- Durch die Bildung des Komplements kannman innerhalb  eines Restklassenrings (ohne Vorzeichen) negative Werte darstellen
- Die ALU kann nur Addieren
- Substraktionen können nur über die Addition des Komplements durchgeführt werden

### Gleitkommazahlen
besteht aus 3 Teilen:
- Basis
- Matisse
	- eine normalisiter gilt 1 <= m < b (hidden Bit lässt sich dann nutzen)
- Exponent 
	- Der Exponent speichert nach Normalisierung die genaue Stelle des Kommas und damit die Größenordnung der Zahl.


# grundlegende Rechnerarchitekturen beschreiben
es gibt 3 Bereiche:
#### ISA
ISA = Instruction Set Architecture
Befasst sich mit dem Entwurd von Intruktionssätzen, Adderesierungsarten, Registern, Datenformaten usw.
#### Microarchitektur
innere Struktur des Rechners
#### System Desing
alle Elemente außer Zentraleinheit
## von Neumann Architektur
- Trennung von Zentraleinheit und Speicher
- Speicher enthält Daten auf dem ein Programm operiert & das Programm selbst
- Flaschenhals da die Steuerung der Zentraleinheit & ALU auf den Speicher konkurierend zugreifen müsseen
<img src="https://upload.wikimedia.org/wikipedia/commons/8/84/Von_Neumann_architecture.svg" style="background: #FFF">

Mit zentralem Bus:
<img src="https://upload.wikimedia.org/wikipedia/commons/6/68/Computer_system_bus.svg" style="background: #FFF">

## Harvard Arichtektur
getrennter Speicher für Programm & Daten
<img src="https://upload.wikimedia.org/wikipedia/commons/3/3f/Harvard_architecture.svg" style="background: #FFF">

## Memory- Register Stackmachine
#### Registermaschine
Instruktionen arbeiten auf Operanden, die in Registern gehalten werden
#### Memory-Maschine
Operanden liegen direkt im Speicher
#### Stackmaschine
Instruktionen arbeiten auf eineM Stack

## Mikroprogrammmierung
### Festverdrahtete Logik
durch Gatterschaltungen
### Mikroprogrammierung 
Auslesen eines Speichers in dem ein Mikroprogramm abgelegt ist
#### vertikal
Mikrooperationen werden nacheinander abgearbeitet
#### horizontal
viele parallele Mikroschritte

## CISC
Complex Instruction Set Computer
- extrem komplexe Befehlssätze

Vorteile:
- kompakter Code
- elegant zu programmieren
Nachteile:
- komplexe Maschine
- langsame Programmausführung (Pipelining auf grund von verschiedenen Instruktionslängen nicht einfach möglich)
- komplexen Instruktionen werden oft nicht genutzt

## RISC
Reduced Instruction Set Computer
- wenige Instruktionen
- Operanden, die in Registern vorgehalten
- Load-Store-Architektur
- Steuerung meist fest verdrahtet
- Befehle haben im Idealfall alle die gleiche Länge, um Pipelining zu ermöglichen


## Skalar & Vektorrechner
Können nativ auf Vektoren als Operanden arbeiten
Vektorrechner sind meist Registerarchitekturen


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