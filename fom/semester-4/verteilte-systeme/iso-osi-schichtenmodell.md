---
title: ISO/OSI Schichtenmodell
published: 1
date: 2023-03-27T20:23:57.207Z
tags: 
editor: markdown
dateCreated: 2023-03-27T20:23:57.207Z
---

# ISO/OSI Schichtenmodell

## Layer 5: Session

Ein Protokoll welches von Sessionlayer gebraucht macht: FTP

> Eröffnen, Aufrechterhalten, Synchronisieren und Verwalten der Kommunikation zwischen den Einheiten
{.is-info}

### Administration der Session

Festlegung des Dialogs:

- Simplex (unidirektional)
- Half-Duplex (beidseitig, aber nicht gleichzeitig)
- Full-Duplex (beidseitig, gleichzeitig)

1. Verbindungsaufbau:

- Log in
- Identifizierung

2. Datenübertragung:

- Datenübertragung
- Bestätigung (ACK, NACK)

3. Verbindungsaufbau:

- Normaler Abbau
- Abbruch

## Layer 6: Presentation

Protokolle welche in Schicht 6 verwendet werden: ASCII, JPEG, MPEG

> Umsetzen der Daten auf ein gegenseitig vereinbartes Format (Transfer Syntax), das von jeder Anwendung und dem Computer verstanden wird
{.is-info}

Translation:

- Bit Gruppierung
  - wie viele Bits für ein Zeichen
- Byte Order
  - in welcher Reihenfolge werden die Bits angeordnet
  - Little Endian
    - wenigstens signifikante Bytes zuerst
  - Big Endian
    - meistens signifikante Bytes zuerst
- Character Encoding
  - ASCII
  - Unicode
  - UTF-8

Aufgaben:

- Datendarstellung
- Codierung
- Konvertierung
- Kompression

Beispiel E-Mail:

- MIME = Multipurpose Internet Mail Extensions
- Anhänge werden mit MIME in Base64 kodiert
- S/MIME für digitale Signatur und Verschlüsselung

## Layer 7: Application

Protokolle welche in Schicht 7 verwendet werden: HTTP, SSH, FTP

Service Advertisements:

- Active - Ankündigung der Verfügbarkeit (Server pollen)
- Passive - Registrierung der angebotenen Dienste (Directory Service)

> Feste Koppelung zwischen Anwendung, Protokoll und Dienst ist nicht zwingend notwendig
{.is-info}
> Server bieten Dienste an, die von Clients genutzt werden können
{.is-info}

## OSI-Schichten und Adressen

|Layer|Funktion|Typ|Art
|-|-|-|-|
|7|Applikation|Netzwerk-Programm|Host-Name|Daten
|6|Präsentation|Interpretation|Host-Name|Daten
|5|Session|Verbindungskontrolle|Socket|Daten(ggf. Encoded)
|4|Transport|End-to-End Kommunikation|Port|Segmente
|3|Network|Routing|IP|Pakete
|2|Data Link|Verpackung der Daten/Fehlerkorrektur|MAC|Frames
|1|Physical|Physische Verbindung|MAC|Bits

## Internet

- Medium für Weltweite Datenkommunikation
- Schwerpunkt liegt auf Betriebs- und Ausfallsicherheit
- nicht zentral organisiert

### Protokolle

- Verbindungsorientiert
  - TCP:
    1. Verbindungsaufbau
    1. Nach dem Verbindungsaufbau erfolgt die Kommunikation
    1. Kontrolle der Verbindung durch ACKs
    1. Verbindung besteht zwischen zwei Endpunkten
- Verbindungslos
  - UDP:
    1. Daten werden einfach so gesendet
    1. Keine Empfangskontrolle
    1. Effektive Datenübertragung
- Sequencing
  - Reihefolge der Daten wird sichergestellt

Weitere Aspekte:

- Streaming Protokolle
- Paketbasierte Protokolle
- Fehlerkontrolle
- Flusskontrolle
- Übertragungsmethoden:
  - Half-Duplex
  - Full-Duplex

### Dienste im Internet

- NTP (Network Time Protocol)
  - wichtig für Services die aktuelle Zeit benötigen z.b TLS
- DNS (Domain Name System)
  - Wandelt Domainnamen in IP-Adressen um
  - Hierarchischer Aufbau zwingend notwendig
  - Grundsätzlicher Aufbau: Host . Domain-Name(n) . Top-Level-Domain .
  - Domain -> Bereich eigener Verantwortlichkeit
  - Zone -> Bereich der vom Nameserver verwaltet wird
  - Subdomain -> Teilbaum der Domain
  - Nameserver
    - Primary -> Verwaltet Daten der autoritativen Zone
    - Secondary -> Kopie der Daten der Primary
  - Dynamic DNS
    - Verwaltet dynamische IP-Adresse zu einem Hostnamen

<!-- S. 121 -->