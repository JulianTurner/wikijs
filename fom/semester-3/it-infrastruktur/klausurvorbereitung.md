---
title: Klausurvorbereitung
description: 
published: 1
date: 2022-07-20T17:05:20.330Z
tags: 
editor: markdown
dateCreated: 2022-03-04T12:22:55.269Z
---
<!-- 

Foliensatz 2,3,4

	Schwerpunkte auf Skript 2 und 3
	
	Dienstleistungen sind nicht lagerfähig 
	
	Ausrichtig Itel
	Itel v3 
	5 Phasen ITIL V3 
	Was ist Servicamanagment
	Was ist ein ITService
	Was ist ein SLA
	Was ist ein Service Katalog
	
	
	- Unterschiedliche Epochen der Betreibsmodelle 5 Stück
	Zuverlässigkeit, Verfügbarkeit, Redudanz
	Etablierte Raid architekturen, 0,1, Mirroring, Striping, 5, 10 und 01
	Funktionsweise von kabeln twisted pair koaxial
Was ist unshielded -->

# Klausurvorbereitung

- Historische Rückblicke vernachlässigen

## Grundlagen

### Was sind Zeichen?

Zeichen sind Symbole, die eine Bedeutung haben

### Was sind Daten?

Werte die u.a. durch Messung oder Beobachtung ermittelt werden

### Was ist Wissen?

- Wissen entsteht aus der Verknüpfung von vielen Informationen, welche individuell in einen Kontext gesetzt werden
- bildet Grundlage für Entscheidungen
- ist mit Ziel und Zweck verbunden

explizites Wissen -> Wissen was unmittelbar vorliegt
implizites Wissen -> Wissen was nicht unmittelbar vorliegt (Bauchgefühl; kann nicht weiter gegeben werden)

### Grundkomponenten vin der von Neumann Architektur

- Prozessor
- Speicher
- Bussystem
- Eingabe- und Ausgabeeinheiten

### Wie funktioniert die von Neumann Architektur?

- Trennung von Zentraleinheit und Speicher
- Speicher enthält Daten auf dem ein Programm operiert & das Programm selbst
- Flaschenhals da die Steuerung der Zentraleinheit & ALU auf den Speicher konkurrierend zugreifen müssen

## Rechenzentrumsbetrieb

### Was sind Aufgaben eines Rechenzentrums?

- Netzbetrieb und Netzdienste
- Zentrale Server und Dienste
- Beratung und Unterstützung der Anwender
- Systemtechnik
- Systemverwaltung
- Operating

### 10 Komponenten von Rechenzentren

- Serverraum
- Telekommunikation
- Batterien
- Notstromaggregate
- Löschanlage
- Kühlaggregate
- Wärmerückgewinnung
- Kühlwasservorrat
- Kontrollzentrale

### Was ist ein Server?

- Physische Maschine
- eine Software (VM, Anwendung)

### Welche Server Organisationen gibt es?

- Shared Hosts -> Server werden für mehrere Kunden genutzt
- Dedicated Hosts -> Server werden für einen Kunden genutzt

> Appliances werden ganzheitlich von einem Hersteller bereitgestellt und betreut

### RAID

zusammenfassung mehrerer physikalischer Festplatten zu einem logischen Laufwerk

Mirroring:

- Spiegelung der Daten auf mindestens zwei Festplatten

Striping:

- Aufteilung zusammenhängender Daten auf mehrere Festplatten

#### RAID 0

- blockweises Striping
- keine Redundanz
- mindestens 2 Festplatten

#### RAID 1

- Mirroring
- Redundanz durch Spiegelung
- min. 2 Festplatten

#### RAID 5

- blockweises Striping mit Parity
- Redundanz durch Parity
- min. 3 Festplatten

#### RAID 0 + 1

- Mirroring und anschließendes blockweises Striping
- min. 4 Festplatten

#### RAID 1 + 0

- blockweises Striping und anschließendes Mirroring
- min. 4 Festplatten

### ISO/OSI Schichten

- Anwendungsebene
- Darstellungsebene
- Sitzungsebene
- Transportebene
- Netzwerkebene
- Leitungsebene
- Physikalische Ebene

### TCP/IP Familie

Fasst das 7 Schichten ISO/OSI Modell in 4 Schichten TCP/IP zusammen

- Anwendungsschicht
- Transportschicht
- Internetschicht
- Verbindungsschicht

### Topologien

- Bus: alle Teilnehmer sind mit einem Knoten verbunden
- Stern: alle Teilnehmer sind mit einem Knoten verbunden
- Ring: jeder Teilnehmer ist mit 2 Nachbarn verbunden
- Baum: Verbund von Sternen in dem zentrale Knoten der Sterne verbunden sind
- Mesh: alle Teilnehmer sind miteinander verbunden
- Diffusionsnetz: Daten werden an alle Teilnehmer verteilt -> Broadcast
- Teilstreckennetz: Daten werden über eine oder mehrere Teilstrecken übertragen

### Netzwerkkomponenten

Repeater: Verstärkt Signale
Bridge: Trennt Netzwerke physikalisch
Hub: unintelligentes Gerät, das Signale an alle Ports weiterleitet
Switch: intelligentes Gerät, das Signale an bestimmte Ports weiterleitet
Router: Kopplung von Netzwerken
WLAN Router: Multifunktionales Gerät, welches eine vielzahl von Funktionen bietet

S. 78 RZ

## Wie funktioniert Virtualisierung?

## Welche Modelle gibt es bei der Virtualisierung?

## Funktionsweise von Kabeln

## It-Service-Management

## Was ist ein Hypervisor?

### Was ist der Unterschied zwischen Produktion und Dienstleistung?
