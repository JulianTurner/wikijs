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
- mehere logische Systeme können auf einem physischen System laufen

Use Cases:

- VM unhabhäning von Host Harware
- Isolation von Anwendungen 
- Ressrourcenanpassung im laufenden Betrieb
- Snapshots, Backup, Restore

Aufbau:

- VM wird von Virtual Machine Monitor (VMM) erschaffen
- viele VMM sind im Hypervisor enthalten
- Gast -> OS der VM (Guest OS)
- Wirt -> OS des Hosts (Host OS) 

> Virtualisierung beschreibt die Nachbildung eines Hard- Software Obejekts vom selben Typ mit einem Abstraktionslayer

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

### Kritische Befehle

- Kritische Befehle müssen vom Hypervisor abgefangen werden
- Befehle werden mit Prescan überprüft
- Kritischer Befehl wird durch Software Breakpoint ersetzt 

> durch Kritische Befehle kann Hypervisor kontrolle über VM verlieren
