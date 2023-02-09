---
title: Klausurvorbereitung
description: 
published: 1
date: 2023-02-09T20:08:33.155Z
tags: 
editor: markdown
dateCreated: 2022-09-13T18:15:49.307Z
---

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

### Grundkomponenten der von Neumann Architektur

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

### Beschreiben Sie das Token Passing Verfahren

1. 1 Token wird in festgelegter Reihenfolge von Teilnehmer zu Teilnehmer weitergegeben
1. Teilnehmer, der das Token hat, darf senden
1. Nur an leeren Token darf Payload angehängt werden
1. Nur Empfänger darf Payload entfernen und leitet leeren Token weiter

Eigenschaften:

- keine Blockade möglich
- höhere Latenzzeiten
- jede Station muss Nachbarn kennen

### Funktionsweise von Kupfer-/Koaxialkabel

- Daten werden in Form von elektrischen Signalen übertragen

Eigenschaften:

- einfache Handhabung
- aufwändige Verlegung

### Funktionsweise von Funkstrecken

- Daten werden in Form von elektromagnetischen Wellen übertragen

Eigenschaften:

- einfache Verlegung
- Beeinflussung durch Umgebung
- Latenzzeiten

### Funktionsweise von Glasfaserkabel/Lichtwellenleiter

- Daten werden in Form von Lichtwellen übertragen

Eigenschaften:

- keine elektromagnetische oder witterungsbedingte Beeinflussung
- hohe Übertragungsgeschwindigkeit
- aufwändige Verlegung

### Unterschiede zwischen Twisted-Pair- und Koaxialkabel

Twisted-Pair-Kabel:

- 2 Adern, die sich gegenseitig umschlingen, um Störungen zu verringern
- kostengünstig im Vergleich zu Koaxialkabel

Koaxialkabel:

- 1 Innenleiter und 1 ummantelnder abschirmender Außenleiter
- Ausfall eines Kabels kann gesamtes Netzwerk lahmlegen
- hohe Übertragungsgeschwindigkeit

### Wie ist ein Glasfaserkabel aufgebaut?

- Kern und Mantel Brechen Lichtstrahlen unterschiedlich stark
- Lichtstrahlen werden durch den Kern geleitet und durch den Mantel gebrochen

### Aus welchen Teilen besteht ein Glasfaserkabel?

- Beschichtung
- Mantel
- Kern
- Mantel
- Beschichtung

### Was ist der Unterschied zwischen Online, netzinteraktiv und Offline USV?

Online USV (Klasse 1):

- Batterie wird vom Stromnetz geladen
- Verbraucher bezieht Strom permanent aus Batterie

z.B. Laptop, Handy

Netzinteraktive USV (Klasse 2):

- Batterie wird von Wechselrichter geladen
- Verbraucher bezieht Strom vom Wechselrichter
- Wechselrichter wandelt bei Stromausfall Gleichstrom aus Batterie in Wechselstrom für Verbraucher um
- Strom geht immer über Wechselrichter

Offline USV (Klasse 3):

- Batterie wird von Ladegerät geladen
- Verbraucher bezieht Strom direkt von Stromnetz
- bei Stromausfall wird Strom aus Batterie nach Umschaltzeit über Wechselrichter an Verbraucher weitergegeben

### Was bestimmt die Packungsdichte bei Rechenzentren?

Kühlung	der Komponenten

### Was ist SOC und NOC?

SOC (Service Operations Center):

- Überwachung und Wartung der internen IT-Services

NOC (Network Operations Center):

- Überwachung und Wartung der Netzwerke (Firewall, Router, Switches, etc.)

## Zuverlässigkeit

### Was ist Zuverlässigkeit?

Eigenschaft, dass ein System ununterbrochen zur Verfügung steht

### Was ist die Wartbarkeit?

Eigenschaft, wie leicht und schnell ein ausgefallenes System wiederhergestellt werden kann

### Was ist die Verfügbarkeit?

Wahrscheinlichkeit, dass ein System zur Verfügung steht

### Was ist Redundanz?

Zusätzliche technische Ressource als Reserve

### Was ist ein Metro Cluster?

Redundante Rechenzentren an verschiedenen Standorten

### Was ist der Flaschenhals beim Metro Cluster?

Die Spiegelung der Daten zwischen den Rechenzentren

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

### Wie funktioniert Virtualisierung?

Nachbildung eines Hard- oder Software-Objekts durch ein ähnliches Objekt vom selben Typ mit Hilfe eines Abstraktionslayers.

### Nennen Sie 3 Gründe für die Virtualisierung

- Hardware ist oft nicht ausgelastet
- Anzahl der physischen Server kann reduziert werden
- Kosten für Hardware können gesenkt werden

### Was ist eine Virtuelle Maschine?

ein isoliertes Duplikat einer realen Maschine

### Was ist ein Hypervisor?

Ist ein Prozess mit dem virtuelle Maschinen erstellt und ausgeführt werden können

### Welche Arten von Hypervisors gibt es?

- Type 1 Hypervisor -> direkt auf Hardware
- Type 2 Hypervisor -> auf einem Betriebssystem

### Was ist die Besonderheit bei virtualisierten Betriebssystemen?

- VMM läuft in Ring 0
- Gast-Betriebssystem in Ring 1
- Reduzierung der Privilegien des Gast-Betriebssystems wird reduziert

### Was ist der Unterschied zwischen Hand-Overs und Failover?

Hand-Overs -> Geplante Übernahme
Failover -> Ungeplante Übernahme (Fehlerfall)

### Was ist Hardware Emulation?

- Hardware wird durch Software nachgebildet
- es können andere Architekturen simuliert werden
- Overhead durch Emulation
- keine dynamische Ressourcenzuweisung

siehe [Hardware-Emulation](/fom/semester-3/it-infrastruktur/virtualisierung.md#hardware-emulation)

### Was ist Hardware Virtualisierung / Full-Virtualisierung?

- mehrere VMs mit gleicher Architektur wie Host
- Gast-OS hat keine direkten Zugriff zur Hardware
- Hardware wird virtuell von Hypervisor an VMs übergeben
- Kommunikation zwischen VMs nur über Netzwerk möglich

siehe [Full Virtualisierung](/fom/semester-3/it-infrastruktur/virtualisierung.md#hardware-virtualisierung-full-virtualization)

### Was ist Paravirtualisierung?

- Weiterentwicklung der Full-Virtualization
- Gast-OS weiß dass es virtualisiert wird (angepasstes OS notwendig)
- Host stellt API bereit, welche von Gast-OS für Hardware-Ressourcen-Reservierung verwendet wird
- Gast ist an die Host Architektur gebunden

siehe [Paravirtualisierung](/fom/semester-3/it-infrastruktur/virtualisierung.md#paravirtualisierung)

### Was ist Container Virtualisierung?

- Virtualisierungsebene läuft als Anwendungen innerhalb des OS
- VMs/Container teilen sich Kernel des Hosts
- Container enthält nur Anwendungen und Abhängigkeiten
- granulare Kommunikation zwischen Containern via Ports / Datei

siehe [Container Virtualisierung](/fom/semester-3/it-infrastruktur/virtualisierung.md#container-virtualisierung)

### Nennen Sie Use-Cases für Virtualisierung

- VM unabhängig von Host Hardware
- Isolation von Anwendungen
- Ressourcenanpassung im laufenden Betrieb
- Verschieben, Isolation, Snapshots, Cloning

## It-Service-Management

### Was ist ein IT-Service?

Zweckmäßige Kombination von Informationstechnologie, Menschen und Prozessen

### Was sind die 5 Phasen des ITIL V3?

- Service Strategy -> Welche Strategie wird verfolgt? z.B. Kostenreduzierung, Effizienzsteigerung
- Service Design -> Ablauf des Prozesses wird definiert? z.B. Partnermanagement, Service Level Management
- Service Transition -> Veränderungen im Service? z.B. Change Management, Release Management
- Service Operation -> Betrieb des Services? z.B. Incident Management, Problem Management
- Continual Service Improvement -> Verbesserung des Services?

### Was ist der Unterschied zwischen Produktion und Dienstleistung?

Produktion:

- physische Güter
- lagerfähig, im Voraus produziert
- Eigentum wird übertragen

Dienstleistung:

- Dienstlesitungspotential muss vorhanden sein
- nicht lagerfähig
- mitwirken des Kunden notwendig

### Was ist ein SLA?

Service Level Agreement -> Vereinbarung zwischen IT-Service-Provider und IT-Service-Kunden bezüglich der der Rechte, Pflichten und Konditionen des IT-Services

### Welche Bestandteile hat ein SLA?

- Beschreibung des IT-Services
- Kontaktadressen der Verantwortlichen
- Glossar
- Service Level, z.B. Verfügbarkeit, Reaktionszeit, Wiederherstellungszeit

### Was ist ein Service Katalog?

- Beschreibung der IT-Services

### Was ist ein OLA?

Operational Level Agreement -> Interner Vertrag zwischen verschiedenen Abteilungen

### Was ist ein UC?

Underpinning Contract -> Vertrag mit externen Partnern
