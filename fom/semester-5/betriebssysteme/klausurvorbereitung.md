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
  - Speicher- und Prozessverwaltung
  - Dateiverwaltung
  - Geräteverwaltung
  - Interprozesskommunikation

## [Aufgaben eines Betriebssystems](/fom/semester-5/betriebssysteme/komponenten-und-konzepte.md) S. 22

- was macht ein Betriebssystem?
  - Verwaltung von Ressourcen wie Speicher, Prozessoren, Geräte
  - Steuerung von Hardware
  - Ausführung von Programmen

## [Klassen von Betriebssystemen](/fom/semester-5/betriebssysteme/komponenten-und-konzepte.md#betriebssystem) S. 27

- [Betriebsarten Betriebssystem](/fom/semester-5/betriebssysteme/komponenten-und-konzepte.md#betriebsarten)
  - Stapelbetrieb
  - Dialogbetrieb
  - Echtzeitbetrieb

## [Kernel-Einordnung](/fom/semester-5/betriebssysteme/komponenten-und-konzepte.md#kernel-einordnung-im-betriebssystem) S. 35

- Welche Kernel Modes gibt es?
  - User Mode
  - Kernel Mode

## [Sicherheits-Architektur](/fom/semester-5/betriebssysteme/komponenten-und-konzepte.md#sicherheits-architektur-moderner-cpus-ringe) S. 37

- Was ist ein Ring?
  - Ring 0: Kernel Mode
  - Ring 1: Treiber
  - Ring 2: Treiber
  - Ring 3: User Mode

> Ein Ring kann nur mit der nächsten Ring Ebene kommunizieren.
{.is-info}

## [Architektur von Betriebssystemen](/fom/semester-5/betriebssysteme/komponenten-und-konzepte.md#architektur-von-betriebssystemen)

- Was ist ein [Micro-Kernel](/fom/semester-5/betriebssysteme/komponenten-und-konzepte.md#mikrokernel)
  - Dünner Kernel im privilegierten Modus
  - Treiber laufen im User-Mode

- [Betriebsarten](/fom/semester-5/betriebssysteme/komponenten-und-konzepte.md#betriebsarten) S. 51

## [Mehrprogrammbetrieb](/fom/semester-5/betriebssysteme/komponenten-und-konzepte.md#mehrprogrammbetrieb) S. 62

## 68 - 71 Betriebssystem und Hardware

- Was ist ein BIOS?
  - Basic Input Output System
  - Lädt Betriebssystem von dem Boot-Medium

- Was ist der Unterschied zwischen BIOS und UEFI. (Seite 68 - 71)
  - BIOS nur bis 32 Bit Prozessor, UEFI für 64 Bit Anwendungen

## [von Neumann Architektur](/fom/semester-5/betriebssysteme/hardware-und-ein-ausgabe.md#von-neumann-architektur) S. 79

- Was ist die von Neumann Architektur?
  - Speicher und Prozessor sind in einem gemeinsamen Bus verbunden
  - Programm und Daten im gleichen Speicher
  - Flaschenhals: Bus

## [Prozessor-Aufbau](/fom/semester-5/betriebssysteme/hardware-und-ein-ausgabe.md#prozessor-aufbau) S. 83

- Wie ist ein Prozessor aufgebaut?
  - Steuerprozessor (CU)
    - Adress- & Befehlsregister
    - Steuer- & Statusregister
    - Befehlszähler
  - Rechenprozessor (ALU)
    - Datenregister
    - Zustandsregister (Carry, Overflow, Zero, ...)
  - Gleitkommaeinheit (FPU)
    - Datenregister
    - Numerik-Rechenwerke
    - Ausnahmebehandlung
  
## [Bus](/fom/semester-5/betriebssysteme/hardware-und-ein-ausgabe.md#bus) S. 89

- Was ist ein Bus?
  - gemeinsamer Datenweg für mehrere Funktionseinheiten
  - besteht aus Steuer-, Adress- & Datenleitungen
  - immer nur 1 Teilnehmer kann senden (wird zu Busmaster)
  - passive Komponenten (Slaves): z.B. Speicher, Peripherie

## [Schichtung des I/O-Systems](/fom/semester-5/betriebssysteme/hardware-und-ein-ausgabe.md#schichtung-des-io-systems) S. 91

## [Polling](/fom/semester-5/betriebssysteme/hardware-und-ein-ausgabe.md#polling) S. 93

- Was ist Polling?
  - zyklisches Abfragen des Gerätes
- Busy Waiting
  - kontinuierliches Abfragen des Gerätes

## [Interrupts](/fom/semester-5/betriebssysteme/hardware-und-ein-ausgabe.md#interrupts) S. 95, 99

- Was ist ein Interrupt?
  - Asynchrone Geräteabfrage
    1. CPU sendet Anfrage an Controller
    1. Controller bearbeitet Anfrage
    1. Controller sendet Interrupt Request (IRQ) an CPU
    1. CPU unterbricht aktuelle Ausführung
    1. CPU bearbeitet Interrupt

- Welche Arten von Interrupts gibt es?
  - Hardware-Interrupts
    - Geräte-Interrupts
  - Software-Interrupts
    - Exceptions

## [Speicherbereiche eines Prozesses](/fom/semester-5/betriebssysteme/prozesse-und-threads.md#speicherbereiche-eines-prozesses) S. 125

Welche Speicherbereiche gibt es?

- Code-Segment (ausführbarer Code):
  - Programmcode
- Daten-Segment (Heap):
  - alles was mit `new` angelegt wird
  - globale Variablen
  - kann dynamisch (zur Laufzeit) angefordert werden
- Stack-Segment (Stack):
  - lokale Laufzeitinformationen der aktuellen Methode
  - Rücksprungadresse
  - übergebene Parameter

## [Organisation von Prozessen](/fom/semester-5/betriebssysteme/prozesse-und-threads.md#organisation-von-prozessen) S. 128

- Was macht der Scheduler?
  - verwaltet Prozesse / entscheidet, welcher Prozess wann ausgeführt wird
- Was macht der Dispatcher?
  1. Kopiert Register-Inhalte des Prozesses aus Arbeitsspeicher in CPU-Register
  1. Wechselt in User-Mode und führt Prozess aus
  1. Nach Zeitablauf / Interrupt / Prozessende speichert Register-Inhalte von CPU in Arbeitsspeicher
  
## [Prozesszustände](/fom/semester-5/betriebssysteme/prozesse-und-threads.md#prozesszustände) S. 131,133

- Welche Zustände gibt es?
  - bereit
  - rechnend
  - blockiert
  - beendet

- Bedingungen für Zustandsübergänge
  - Ausführungsentscheidung vom Scheduler
  - Rechenzeit abgelaufen
  - I/O-Operation angefordert
  - I/O-Operation abgeschlossen
  - Prozess beendet

## [Prozessverwaltung](/fom/semester-5/betriebssysteme/prozesse-und-threads.md#prozessverwaltung) S. 137

- Was ist ein Task-Wechsel?
  - Wechsel zwischen Prozessen
  - Sicherung der aktuellen Register-Inhalte in den Haupt-Speicher
  - Laden der Register-Inhalte des nächsten Prozesses in die CPU

## [Prozesse und Threads](/fom/semester-5/betriebssysteme/prozesse-und-threads.md) S. 141, 142, 146

- Was haben Threads gemeinsam das Prozesse nicht haben?
  - Gemeinsamer Adressraum.
  - Kernel/User Threads

## [Interprozesskommunikation](/fom/semester-5/betriebssysteme/prozesse-und-threads.md#interprozesskommunikation) S. 154, 156, 157

- Möglichkeiten zur Interprozesskommunikation
  - Shared Memory
  - Pipes
  - Signale
  - Sockets
- Race Conditions bei nicht gemeinsamen Hauptspeicher Zugriff?
  - Ja, bei HDD Zugriff.

- Was ist eine Semaphore?
  - Ampel mit welche Zugriff auf gemeinsame Ressourcen regelt
  - Semaphore wird selbst geschlossen und von anderem Task geöffnet
- Was ist ein Mutex?
  - Semaphore mit Wert 0 oder 1
  - kann nur von dem Task geöffnet werden, der sie geschlossen hat

- [Prozesssynchronisation](/fom/semester-5/betriebssysteme/prozesse-und-threads.md#prozesssynchronisation) 171

- Welche Mittel gibt es zum Synchronisieren?
  - Atomare unteilbare Befehle

## [Deadlocks](/fom/semester-5/betriebssysteme/prozesse-und-threads#deadlocks) S. 175, 176, 179

- 4 Bedingungen für Deadlock (Coffman Bedingungen)?
  1. wechselseitiger Ausschluss (Resource kann nur von einem Prozess genutzt werden)
  1. Halten und Warten (Prozess hält Ressource und wartet auf weitere Ressourcen)
  1. Ununterbrechbarkeit (Ressource kann nicht entzogen werden)
  1. Zyklisches Warten (Prozesse warten in einer Kette aufeinander)
- Was kann zur Deadlock Avoidance getan werden?
  - Nummerierung der Ressourcenanforderung
- Kann bei Pseudo-Parallelität Race-Conditions auftreten?
  - Ja, weil auch zwischen Instruktionen Single-Thread angehalten werden kann.

## [Prozesszustände](/fom/semester-5/betriebssysteme/prozesse-und-threads.md#prozesszustände) S. 184

## [Prozesskontext](/fom/semester-5/betriebssysteme/ablaufplanung-scheduling.md#prozesskontext) S. 188

## [Scheduling-Kriterien](/fom/semester-5/betriebssysteme/ablaufplanung-scheduling.md#scheduling-kriterien-aus-sicht-des-benutzers) S. 192

## [Scheduler für Harte Echtzeitsysteme](/fom/semester-5/betriebssysteme/ablaufplanung-scheduling.md#scheduler-für-harte-echtzeitsysteme) S. 212

- Welchen Scheduler für Harte Echtzeitsysteme:
  - Earliest Deadline First (Seite 212)

- Unterschied Hart/Weiche Echtzeit:
  - Hart: Prozess muss zur bestimmten Zeitpunkt ausgeführt werden
  - Weich: Prozess muss innerhalb eines bestimmten Zeitraums ausgeführt werden

## [Speicherhierarchie](/fom/semester-5/betriebssysteme/speicher-verwaltung.md#speicherhierarchie) S. 217, 218

- Speicherpyramide
- Probleme Speicherpyramide
  - Kosten steigen mit der Geschwindigkeit, Zugriffszeit steigt mit Kapazität, Persistenter Speicher ist langsam

## [Hauptspeicher](/fom/semester-5/betriebssysteme/speicher-verwaltung.md#hauptspeicher) S. 221

- Eigenschaften Hauptspeicher
  - Jedes Byte Adresse
  - Basis-Adresse

- [Was ist der Unterschied zwischen Paging und Swapping?](/fom/semester-5/betriebssysteme/speicher-verwaltung.md#zu-wenig-schneller-speicher-ram)

- Swapping -> Vollständiger Prozess wird in den Speicher geladen
- Paging -> Prozess wird in Seiten aufgeteilt und teilweise in den Speicher geladen

## [Persistenter Speicher](/fom/semester-5/betriebssysteme/persistenter-speicher-hdd-ssd-dateisysteme.md)

- Was ist Indexknoten & INode
  - Grundlegende Datenstruktur zur Verwaltung von Dateisystemen

- Unterschied zwischen Softlink & Hardlink
  - Hardlink: Referenz auf INode (nur auf gleicher Partition möglich)
  - Softlink: Referenz auf Name (kann aufs leere zeigen)

## [Arten von Virtualisierung](/fom/semester-5/betriebssysteme/virtualisierung.md#einsatzgebiete)

- Arten von Virtualisierung
  - Vollvirtualisierung
  - Paravirtualisierung
- Was ist der unterschied zwischen Virtuelle-Betriebssysteme und Containern?
  - Virtuelle Betriebssysteme:
    - Fokus auf Betriebssystem
    - eigener Kernel
  - Container:
    - Fokus auf Anwendung
    - teilen sich Kernel mit dem Host
