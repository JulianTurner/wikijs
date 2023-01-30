---
title: Virtualisierung
description: 
published: 1
date: 2022-11-21T19:18:44.313Z
tags: 
editor: markdown
dateCreated: 2022-11-15T19:29:01.687Z
---

# Virtualisierung

- Reduktion der Anzahl physischer Computer
- Unterscheidung von logischen und physischen Computersystemen
- mehrere logische Systeme können auf einem physischen System laufen

Use Cases:

- VM unabhängig von Host Hardware
- Isolation von Anwendungen
- Ressourcenanpassung im laufenden Betrieb
- Verschieben, Isolation, Snapshots, Cloning

Aufbau:

- VM wird von Virtual Machine Monitor (VMM) erschaffen
- viele VMM sind im Hypervisor enthalten
- Gast -> OS der VM (Guest OS)
- Wirt -> OS des Hosts (Host OS)

> Virtualisierung beschreibt die Nachbildung eines Hard- Software Objekts vom selben Typ mit einem Abstraktionslayer

## Hypervisor (VMM)

- Prozess mit dem VM erstellt & ausgeführt werden
- Verwaltet & Verteilt Ressourcen an VMs

Typ 1:

- Bare Metal Hypervisor
- verbraucht weniger Ressourcen
- verfügt über alle Treiber der HW

Typ 2:

- setzt auf Betriebssystem auf
- nutzt Gästetreiber

Beispiele:

- VM Ware Workstation -> Desktop
- vSphere / ESX -> Rechenzentrum
- Hyper-V -> Windows

### Ringarchitektur

- Ringarchitektur mit 4 Ringen
- Ring 0 = Kernel Mode -> Ring 3 = User Mode
- größere Ringnummer = weniger Privilegien
- Privilegierte Befehle nur im Kernel Mode

![Ringarchitektur](/fom/semester-3/it-infrastruktur/virtualisierung_ringe.png)

> Wenn Gast-Betriebssystem wird es in Ring 1 gehoben und der VMM läuft im Ring 0

### Kritische Befehle

- Kritische Befehle müssen vom Hypervisor abgefangen werden
- Befehle werden mit Prescan überprüft
- Kritischer Befehl wird durch Software Breakpoint ersetzt

> durch Kritische Befehle kann Hypervisor Kontrolle über VM verlieren

### Verfügbarkeit

Migration auf anderen Host:

- geplant -> Hand-Over
- ungeplant -> Fail-Over

## Hardware Emulation

Funktionsweise:

- alle Hardwarekomponenten werden emuliert
- Emulator übersetzt Befehlssatz der emulierten Architektur in Befehle der ausführenden Architektur

Vorteile:

- Programme anderer Architekturen können ausgeführt werden z.B. alte Programme, mobile Emulator

Nachteile:

- Overhead durch Emulation

## Hardware Virtualisierung (Full-Virtualization)

Funktionsweise:

- mehrere VMs mit gleicher Architektur wie Host
- Gast-OS hat keine direkten Zugriff zur Hardware
- Hardware wird virtuell von Hypervisor an VMs übergeben
- Kommunikation zwischen VMs via Netzwerk

> Gast-OS weiß nicht dass es in einer VM läuft
{.is-info}

Vorteile:

- dynamische Zuweisung von Hardware-Ressourcen
- mehrere virtuelle Plattformen unabhängig voneinander ausführen
- einfache Migration von VMs auf andere Hosts

Nachteile:

- Risiko einer nicht autorisierten Steuerung von Gastsystemen über den Hypervisor
- Single Point of Failure ist die unterliegende Hardware / Hypervisor
- Seiteneffekte bei der Performance

## Paravirtualisierung

Funktionsweise:

- Weiterentwicklung der Full-Virtualization
- Gast-OS weiß dass es virtualisiert wird (angepasstes OS notwendig)
- Host stellt API bereit, welche von Gast-OS für Hardware-Ressourcen-Reservierung verwendet wird
- Gast ist an die Host Architektur gebunden

Vorteile:

- bessere Performance durch Reduktion des Overhead gegenüber der Vollvirtualisierung

Nachteile:

- Performance Gewinn ist nicht vorhersehbar / abhängig von verschiedenen Faktoren (z.B. Arbeitslast)

## Betriebssystem Virtualisierung / Containerisierung

Funktionsweise:

- Virtualisierungsebene läuft als Anwendungen innerhalb des OS
- VMs/Container teilen sich Kernel des Hosts
- Container enthält nur Anwendungen und Abhängigkeiten

Vorteile:

- granulare Kommunikation zwischen Containern via Ports / Datei
- schnelle Startzeit
- geringer Overhead

Nachteile:

- geringe Isolation
- Zugriff auf Kernel-OS
