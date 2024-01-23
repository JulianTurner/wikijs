---
title: Klausurvorbereitung
published: 1
date: 2023-09-13T19:04:20.207Z
tags: 
editor: markdown
dateCreated: 2023-09-13T19:04:20.207Z
---

# Klausurvorbereitung

Transferaufgaben:

- Scheduling
- Speicherverwaltung
Klausur Fragen Multiple-Choice
- Übungs-Aufgabe: Job Scheduling mit First Come First Serve und Shortest Job First

## [Schichtenmodell](/fom/semester-5/betriebssysteme/komponenten-und-konzepte.md#betriebssystemschichten) S. 18

## [Teile eines Betriebssystems](/fom/semester-5/betriebssysteme/komponenten-und-konzepte.md#teile-eines-betriebssystems) S. 19, 21

- Aufgaben und Merkmale eines Betriebssystems

## [Aufgaben eines Betriebssystems](/fom/semester-5/betriebssysteme/komponenten-und-konzepte.md) S. 22

- was macht ein Betriebssystem?

## [Klassen von Betriebssystemen](/fom/semester-5/betriebssysteme/komponenten-und-konzepte.md#betriebssystem) S. 27

## [Kernel-Einordnung](/fom/semester-5/betriebssysteme/komponenten-und-konzepte.md#kernel-einordnung-im-betriebssystem) S. 35

## [Sicherheits-Architektur](/fom/semester-5/betriebssysteme/komponenten-und-konzepte.md#sicherheits-architektur-moderner-cpus-ringe) S. 37

## [Architektur von Betriebssystemen](/fom/semester-5/betriebssysteme/komponenten-und-konzepte.md#architektur-von-betriebssystemen)

- Was ist ein Micro-Kernel
  ○ Dünner Kernel im privilegierten Modus
  ○  nicht => Treiber die im User-Mode laufen

- [Betriebsarten](/fom/semester-5/betriebssysteme/komponenten-und-konzepte.md#betriebsarten) S. 51

## [Mehrprogrammbetrieb](/fom/semester-5/betriebssysteme/komponenten-und-konzepte.md#mehrprogrammbetrieb) S. 62

## 68 - 71 Betriebssystem und Hardware

-Was ist ein BIOS? Was ist der Unterschied zwischen BIOS und UEFI. (Seite 68 - 71)
  ○ Starten des Betriebssystem
  ○ Muss auf Boot-Medium zugreifen (braucht dafür Geräte-Treiber)
  ○ BIOS nur bis 32 Bit Prozessor. UEFI für 64 Bit Anwendungen

## [von Neumann Architektur](/fom/semester-5/betriebssysteme/hardware-und-ein-ausgabe.md#von-neumann-architektur) S. 79

## [Prozessor-Aufbau](/fom/semester-5/betriebssysteme/hardware-und-ein-ausgabe.md#prozessor-aufbau) S. 83

## [Bus](/fom/semester-5/betriebssysteme/hardware-und-ein-ausgabe.md#bus) S. 89

## [Schichtung des I/O-Systems](/fom/semester-5/betriebssysteme/hardware-und-ein-ausgabe.md#schichtung-des-io-systems) S. 91

## [Polling](/fom/semester-5/betriebssysteme/hardware-und-ein-ausgabe.md#polling) S. 93

- Polling
- Busy Waiting

## [Interrupts](/fom/semester-5/betriebssysteme/hardware-und-ein-ausgabe.md#) S. 95, 99

## [Speicherbereiche eines Prozesses](/fom/semester-5/betriebssysteme/prozesse-und-threads.md#speicherbereiche-eines-prozesses) S. 125

## [Organisation von Prozessen](/fom/semester-5/betriebssysteme/prozesse-und-threads.md#organisation-von-prozessen) S. 128

## [Prozesszustände](/fom/semester-5/betriebssysteme/prozesse-und-threads.md#prozesszustände) S. 131,133

- Welche Zustände
- Bedingungen für Zustandsübergänge

## [Prozessverwaltung](/fom/semester-5/betriebssysteme/prozesse-und-threads.md#prozessverwaltung) S. 137

- Was ist ein Task-Wechsel?

## [Prozesse und Threads](/fom/semester-5/betriebssysteme/prozesse-und-threads.md) S. 141, 142, 146

- Was haben Threads gemeinsam das Prozesse nicht haben? Gemeinsamer Adressraum.
- Kernel/User Threads
- echt parallel vs quasi parallel

## [Interprozesskommunikation](/fom/semester-5/betriebssysteme/prozesse-und-threads.md#interprozesskommunikation) S. 154, 156, 157

- Möglichkeiten zur Interprozesskommunikation
- Race Conditions bei nicht gemeinsamen Hauptspeicher Zugriff?
  - Ja, bei HDD Zugriff.

- [Prozesssynchronisation](/fom/semester-5/betriebssysteme/prozesse-und-threads.md#prozesssynchronisation) 171

- Welche Mittel gibt es zum Synchronisieren. Atomare unteilbare Befehle

## [Deadlocks](/fom/semester-5/betriebssysteme/prozesse-und-threads#deadlocks) S. 175, 176, 179

- 4 Bedingungen für Deadlock (Coffman Bedingungen)?
- Deadlock Avoidance
- Nummerierung der Ressourcen

## [Prozesszustände](/fom/semester-5/betriebssysteme/prozesse-und-threads.md#prozesszustände) S. 184

## [Prozesskontext](/fom/semester-5/betriebssysteme/ablaufplanung-scheduling.md#prozesskontext) S. 188

## [Scheduling-Kriterien](/fom/semester-5/betriebssysteme/ablaufplanung-scheduling.md#scheduling-kriterien-aus-sicht-des-benutzers) S. 192

## [Scheduler für Harte Echtzeitsysteme](/fom/semester-5/betriebssysteme/ablaufplanung-scheduling.md#scheduler-für-harte-echtzeitsysteme) S. 212

- Welchen Scheduler für Harte Echtzeitsysteme: Earliest Deadline First (Seite 212)

## [Speicherhierarchie](/fom/semester-5/betriebssysteme/speicher-verwaltung.md#speicherhierarchie) S. 217, 218

- Speicherpyramide
- Probleme Speicherpyramide

## [Hauptspeicher](/fom/semester-5/betriebssysteme/speicher-verwaltung.md#hauptspeicher) S. 221

- Eigenschaften Hauptspeicher
  - Jedes Byte Adresse
  - Basis-Adresse
  
<!-- - Was ist der Unterschied zwischen Paging und Swapping?
- Unterschied Hart/Weiche Echtzeit

- Betriebsarten Betriebssystem
- Was ist Indexknoten & INode

- Unterschied zwischen Softlink & Hardlink

- Arten von Vitualisierung

- Was ist der unterschied zwischen Virtuelle-Betriebssysteme und Containern?
- Kann bei Pseudeo-Parallelität Race-Conditions auftreten? Ja, weil auch zwischen Instruktionen Single-Thread angehalten werden kann. -->
