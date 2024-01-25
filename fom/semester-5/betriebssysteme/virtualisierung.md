---
title: Virtualisierung
published: 1
date: 2023-09-13T19:14:41.207Z
tags: 
editor: markdown
dateCreated: 2023-09-13T19:14:41.207Z
---

# Virtualisierung

- kritische Maschinenbefehle werden nachgebildet
- Effiziente Nutzung der Hardware
- Gastsysteme müssen modifiziert werden oder können nicht alle Funktionen nutzen
- in 64bit Befehlssatz sind alle sensitiven Befehle privilegiert
- Ressourcen werden vom [VMM](/fom/semester-3/it-infrastruktur/virtualisierung.md#hypervisor-vmm) verwaltet
- Unterschied zur [Emulation](/fom/semester-3/it-infrastruktur/virtualisierung.md#hardware-emulation):
  - Vollständige Nachbildung der Hardware
  - komplett unabhaengiges System
  - Gastsystem muss nicht modifiziert werden
  - Durch Binary Translation -> langsamer

Vorteile:

- weniger Hardware nötig
- bessere Auslastung der Hardware
- höhere Flexibilität
- bessere Wartbarkeit
- Verfügbarkeits- und Ausfallsicherheitskonzepte
-

Nachteile:

- Performanceverlust
- Virtualisierung spezieller Hardware schwierig/nicht möglich
- Host ist Single Point of Failure

[Vollständige Virtualisierung](/fom/semester-3/it-infrastruktur/virtualisierung.md#hardware-virtualisierung-full-virtualization):

- Maschinenbefehle müssen nicht emuliert werden
- Gastsystem muss nicht modifiziert werden
- unterschiedliche Kernel pro Gastsystem

Varianten:

- Typ 1: Hypervisor (Bare-Metal)
  - Hypervisor läuft direkt auf der Hardware
- Typ 2: Hypervisor mit Software
  - Hypervisor läuft als Anwendung auf einem Betriebssystem

[Paravirtualisierung](/fom/semester-3/it-infrastruktur/virtualisierung.md#paravirtualisierung):

- Gastsystem muss modifiziert werden (Gastsystem muss ohne Ring 0 laufen)
- Kernel des Gastsystems nutzt Kernelfunktionen des Hostsystems über Hypercalls
- CPU Befehle:
  - nicht privilegierte Befehle können direkt ausgeführt werden
  - privilegierte Befehle werden durch [VMM](/fom/semester-3/it-infrastruktur/virtualisierung.md#hypervisor-vmm) kontrolliert ausgeführt
  - kritische Befehle dürfen keine Einfluss auf das Hostsystem haben (z.B. Reset)

[Container-Virtualisierung](/fom/semester-3/it-infrastruktur/virtualisierung.md#betriebssystem-virtualisierung--containerisierung):

- Container teilen sich den Kernel des Hostsystems
- Prozesse laufen isoliert voneinander
- geringerer Overhead als bei vollständiger Virtualisierung
- Fokus auf Anwendung und nicht auf Betriebssystem (1 Dienst pro Container)
- Docker
  - Dockerfile für einzelne Container
  - docker-compose.yml für zusammenhängende Container
  - schichtweise Struktur
  - bei Änderungen nur die betroffene Schicht neu bauen
  - Kubernetes für Orchestrierung vieler Container

## Einsatzgebiete

- Server-Virtualisierung
  - mehrere Server auf einer Maschine
- Desktop-Virtualisierung
  - mehrere Desktops auf einer Fat-Client-Maschine
- Online-Virtualisierung
  - Terminal-Server mit Thin-Clients
- Anwendungs-Virtualisierung
  - Isolierte Anwendungen in Containern
