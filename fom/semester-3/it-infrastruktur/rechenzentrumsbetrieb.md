---
title: Rechenzentrumsbetrieb
description: 
published: 1
date: 2022-11-21T19:18:44.313Z
tags: 
editor: markdown
dateCreated: 2022-11-15T19:29:01.687Z
---

# Rechenzentrumsbetrieb

## Rechenzentrum

Zu einem Rechenzentrum gehören:

- Gebäude mit IT-Infrastruktur
- Organisation (Firma)
- zentrales Rechenwerk (Rechner & für den Betrieb notwendige Komponenten)

> Standarisierung ist im BSI-IT Grundschutzkatalog (IT-Grundschutz) definiert.
{.is-info}

### Aufgaben eines Rechenzentrums

- Netzbetrieb & Netzdienste
- Serverbetrieb
  - Applikationen
  - Anwendungen
  - Datenbanken
- Beratung & Unterstützung der Anwender
- Systemtechnik
  - Wartung & Instandhaltung der Geräte
  - Installation & Konfiguration
  - Verkabelung
- Systemverwaltung
  - Administration Soft- & Hardware
  - Datensicherheit & Datenschutz
  - Monitoring
- Operation
  - 1st Level Support
  - Wechsel von Druckerpatronen

### Herausforderungen

- Platzproblematik => Packungsdichte
- Kühlproblematik => Wärmeabfuhr
- Sicherheitsproblematik => Zugangskontrolle
- Stromproblematik => Stromversorgung
- Ausfallsicherheit => Redundanz & Frühwarnsysteme
- Managementproblematik => Überblick über die IT-Infrastruktur

### Komponenten eines Rechenzentrums

- Serverraum
- Telekommunikation
- Batterien
- Notstromaggregate
- Löschanlage
- Kühlaggregate
- Wärmerückgewinnung
- Kühlwasservorrat
- Gebäudesicherung
- Kontrollzentrale

#### Serverraum

- Unterbringung der Server

Aufgaben:

- Recheneinheiten
- Applikationsserver
- Datenbankserver

Eigenschaften:

- besonders Abgeschirmt (z.B. Brandschutz)
- thermische Organisation (z.B. kalte, heiße Gänge, Doppelböden)
- standardisierte Komponenten (z.B. Racks)

> besitzen keinen ständigen besetzten Arbeitsplatz
{.is-info}

##### Airflow (Kalte und heiße Gänge)

Abluft wird zentral Abgeführt und gekühlt

![serverraum-airflow](https://www.researchgate.net/profile/Jetsadaporn-Priyadumkol/publication/270986657/figure/fig1/AS:647411743612928@1531366396569/A-raised-floor-air-conditioning-system-in-data-center.png)

> Eine Sauerstoffreduktion bremst die Ausbreitung von Feuer
{.is-info}

##### Racks

- Haltevorrichtung für Serverkomponenten:
  - USV
  - Raid-Array
  - Patchpanel
  - Server
  - Monitor
  - Power Strip
- Höhe wird in Höheneinheiten (HE) angegeben
- Breite wird in Teilungseinheiten (TE) angegeben
- Redundante Stromanbindung (verschiedene Stromkreise)
- Isoliertes Management Netzwerk

![rack](https://www.conceptdraw.com/samples/resource/images/solutions/network-diagram/network-diagram-Rack-Diagram.png)

##### Server

- Software (Dienst)
- Hardwarekomponente (dediziert)

Fokus:

- Dauerbetrieb - mission critical
- Hochverfügbarkeit - Redundanz
- Hochperformanz - Gerätschaften

###### Serverklassen

x86/x64 Commodity Server

- kostengünstig
- hohe Kompatibilität
- einfacher Austausch
- Probleme bei Skalierung

Proprietäre Server

- IBM Power, Oracle Exalogic
- lange Entwicklung
- viele Features
- hohe Verfügbarkeit
- hohe Skalierbarkeit
- hohe Taktfrequenz
- wenige Betriebssysteme

###### Organisation

Shared Hosts => mehrere Aufgaben auf einem Server
Dedicated Hosts => ein Aufgabe auf einem Server

- dedicated to Service => Server erfüllt nur eine Aufgabe
- dedicated to Customer => Server ist nur für einen Kunden

Dediziert => hohe Sicherheit, Performance, spezielle Software
Appliances => Server und Applikationen werden gemeinsam betrieben

###### Zuordnungsebenen

Anwendungsebene => Kunde erhält nur ein Web-Server (AS)
Betriebssystemzuordnung => Kunde erhält Betriebssystem (VM)
Hardwarezuordnung => Kunde erhält dedizierten Server (HW)

![server-zuordnung](https://avinetworks.com/wp-content/uploads/2020/04/virtual-server-diagram.png)

###### Speicher-Medien

siehe [Speichersysteme](/fom/semester-1/hardware-grundlagen/Klausurvorbereitung2#speichersysteme)

siehe [RAID](https://wiki.trner.de/fom/semester-1/hardware-grundlagen/Klausurvorbereitung2#RAID)

#### Telekommunikation

#### Batterien

#### Notstromaggregate

#### Löschanlage

#### Kühlaggregate

#### Wärmerückgewinnung

#### Kühlwasservorrat

#### Gebäudesicherung

#### Kontrollzentrale
