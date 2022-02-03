---
title: Klausurvorbereitung Neu
description: 
published: 1
date: 2022-02-03T18:17:51.781Z
tags: 
editor: markdown
dateCreated: 2022-02-03T15:11:53.417Z
---

# Prüfungsvorbereitung

## Microarchitecture

- 1. Ebene eines Computers (über Ebene 0 - digitale Logik)
- Besteht aus
    - 8 bis 32 Register
    - ALU (Arithmetic Logic Unit - Rechenwerk)
- Register sind mit ALU verbunden um einen Datenpfad (Data Path) zu bilden.
- Data Path Aufgaben:
    - Auswahl von 1 oder 2 Register mit denen die ALU arbeitet
    - Ergebnis ALU Operation in Register ablegen

## ISA

- 2. Ebene eines Computers (über Ebene 1 - Microarchitecture)
- Befehlssatzarchitektur-Ebene (ISA = Instruction Set Architecture)
- Beinhaltet Befehlssatz des Computers
- Handbuch für Befehlssatz wird vom Prozessor-Hersteller zur Verfügung gestellt


## System Design

## Logiken

## Schaltungsdesign

## Physikalische Implementierung

## Designvalidierung

## Von Neumann und Harvard Architektur
### Von Neumann Architektur
- Grundlage fast aller moderner Computer
- Besteht aus
	- Rechenwerk (ALU)
  	- führt Rechenoperationen und boolsche Verknüpfungen aus
  - Steuerwerk
  	- interpretiert Anweisungen eines Pgoramms
  - Bus-System
  	- Verknüpft die anderen Komponenten
  - Seicherwerk
  	- speichert Programme und Daten, welche für das Rechenwerk zugänglich sind
  - Eingabewerk/Ausgabewerk
  	- steuert Ein- und Ausgabe von Daten zu Anwender (Tastatur, Bildschirm) und anderen Systemen (Schnittstellen)
    
### Harvard Architektur
- Programm und Daten liegen in getrennten Speichern
- Heute geteilter Speicher im Bereich CPU Cache verbreitet


## Stack
- Kellerspeicher
- Lineare Datenstruktur
- Wächst von unten nach oben
- Enthält Rücksprungadressen und lokale Variablen
- automatisches Aufräumen von Variablen beim Verlassen eines Scopes

## Heap
- dynamischer Speicher (engl. Heap = dt. Haufen)
- Hierarchiche Datenstruktur
- enthält globale Variablen
- manuelle allocation und deallocation durch Programmier-Befehle

## CPU Kontrolleinheit
### Fest verdrahtet
- Fest verbaute logische Gatter dienen zum erzeugen der Kontrollsignale
- Schneller als microprogrammierte Signalerzeugung
- RISC Architektur basiert auf fest verdrahteter Kontrollsignalerzeugung

### Mikroprogrammierung
- Kontrollsignale -> Operation Mapping gespeichert als Kontrollwörter in speziellem, nicht via normalem Programmieren erreichbaren Speicherbereich
- Kontrollsignale werden programmatisch generiert
- Langsamer als fest verdrahtete Kontrollsignalvermittlung, wg. Aufrufzeit der Microinstruktionen vom dedizierten Speicher.


#### vertikaler Microcode
- Steuersignale repräsentiert mit decodiertem Binärformat
- Schneller als horizontaler Microcode
- Erlaubt hohen Grad an parallelisierung
- Benötigt keine zusätzliche Hardware
- Lange Kontrollwörter
- Jedes Bit in Kontrollfeld entspricht einer Kontrolllinie

#### Horizontaler Microcode
- Steuersignale repräsentiert mit encodiertem Binärformat
- Langsamer als vertikaler Microcode
- Niedriger Grad an parallelisierung (gerade soviel wie Decoder zulässt)
- Benötigt zusätzliche Decoder Hardware, welche enocodiertes Binärformat in decodierte Steuersignale übersetzt

## CISC
## RISC
## VLIW
## Parallelrechner
## SISD
## MIMD
## SIMD
## Benchmark
## Einheiten: MIPS, FLOPS
## Transistor und Röhre
## Hauptspeicher
## Dynamischer Speicher
## Block Device
## Char Device
## Festplatte
## SSD
## NAND und NOR Flash
## Drucker
## Was ist Information und Wissen
## Zeichen - Daten - Information – Wissen
## Umrechnen von Binär in Dezimal und umgekehrt ( evtl. Hexadezimal)
## Virtuelle Maschinen - Vor und Nachteile
## Hardwarevirtualisierung
## Bufferoverflow
## Activation Record
## Devicetreiber
## Soft- und Hardwareinterrupt
## System Call
## Deadlock
## Race Condition