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

siehe [RAID](/fom/semester-1/hardware-grundlagen/Klausurvorbereitung2#RAID)

#### Telekommunikation

##### Vermittlung

Leitungsvermittlung:

- physicher Übertragunsweg zwischen Datenstationen
- Unabhängig von Daten
- langsamer Verbindungsaufbau
- schlechte Auslastung der Kapazität

Paketvermittlung:

- zerlegung der Daten in einzelne Pakete
- jedes Paket bekommt Adress- und Steuerungsinformationen
- Empfänger setzt Daten zusammen
- keine durchgängige direkte Verbindung zwischen Teilnehmern
- Kapazität kann besser genutzt werden

##### WAN

WAN steht für WIDE AREA NETWORK

Teilnehmeranschlussleitung:

- verbindet Teilnehmer / kleine Gewerbe mit Teilnehmervermittlungsstelle
- analoge Twisted-Pair-Kabel / digitale Glasfaserkabel

Verbindungsleitung:

- verbindet Teilnehmer-/ Fernvermittlungsstellen
- typisch Glasfaserkabel

Vermittlungsstellen:

- Teilnehmervermittlungsstelle => nimmt Anrufe entgegen, leiten Anrufe an Teilnehmer
- Fervermittlungsstelle => vermitteln Anrufe bis zur Teilnehmervermittlungsstelle

> Telefonnetz basiert auf Leitungsvermittlung
{.is-info}

##### Netzwerke

Entfernung | Ausdehnung | Name | Beispiel
-|-|-|-|
1m | Armlänge | PAN | Bluetooth, AdHoc WLAN
10m | Raum | LAN | Raum
100m | Gebäude | LAN | alle Räume im Gebäude
1km | Campus | LAN | zusammenhängende Gebäude
10km | Stadt | MAN | eine Stadt
1000km | Land | WAN | ein Land
10000km | Kontinent | WAN | ein Kontinent
100000km | Planet | WAN | ganzes Inernet

<!-- TODO: Grafik von Seite 59 einfügen -->

##### Schichtenmodell

Auflöung der Gesamtsituation in hierachisch strukturierte Ebenen, die als Schichten angeordnet werden

- unmittelbare Kommunikation findet nur mit direkt darüber / darunter liegenden Schicht statt
- gleiche Schichten kommunizieren über Protokolle

OSI

Nr | Ebene
-|-
7 | Anwendungsebene (Application Layer)
6 | Darstellungsebene (Presentation Layer)
5 | Sitzungsebene (Session Layer)
4 | Transportebene (Transportation Layer)
3 | Netzwerkebene (Network Layer)
2 | Leitungsebene (Data Link Layer)
1 | Physikalische Ebne (Physical Layer)

Vorteile:

- Unabhänig von Hard-/ Software
- Änderungen/ Anpassungen von Diensten sind einfach möglich

Prinzip:

- Daten (Payload) werden via Schnittstellen über Ebenen transportiert
- Protokollschichten fügen Daten weitere Transportinformationen (Header, Trailer) hinzu, welche für den Transport relevant sind
- Auf der Empfängerseite werden pro Schicht nur die relevanten Transportinformationen (Header, Trailer) ausgewertet und entfernt

<!-- ! TODO: Bild von Seite 66 einfügen -->

TCP/IP:

- logische Basis des Internets
- vier Schichten Familie
  - Anwendungsschicht (z.B. HTTP, POP, IMAP)
  - Transportschicht (z.B. TCP, UDP)
  - Internetschicht (z.B. IP, ICMP)
  - Verbindungsschicht (z.B. ARP, Kupferkabel)
- zusammenfassung herstellerneutralen Anwendungs- und Transportprotokollen

##### Netzwerk Hardware

#### Batterien

#### Notstromaggregate

#### Löschanlage

#### Kühlaggregate

#### Wärmerückgewinnung

#### Kühlwasservorrat

#### Gebäudesicherung

#### Kontrollzentrale
