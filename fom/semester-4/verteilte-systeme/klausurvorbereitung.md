---
title: Klausurvorbereitung
published: 1
date: 2022-03-04T16:25:06.786Z
tags:
editor: markdown
dateCreated: 2022-03-04T12:23:19.207Z
---

# Klausurvorbereitung

## Mit was wird in den Sichten im OSI Modell operiert?

Layer:

- 1: Bits
- 2: Frames
- 3: Pakete (mit IPSEC asymmetrisch verschlüsselt)
- 4: Segmente
- 5: Daten (Session)
- 6: Daten (Daten mit AES symmetrisch verschlüsselt, Codierung)
- 7: Daten (Cookies, HTML, CSS, JavaScript)

## Was ist peer to peer?

- Systeme welche direkt miteinander kommunizieren ohne einen Server zu benötigen.
- autonomes System
- keine garantierte Verfügbarkeit

## Was ist Software Defined Networking?

- Verlagern von Netzwerkfunktionen in Software
- Virtualisierung von Netzwerkfunktionen

## Was ist Edge Computing?

- Verlagern von Rechenleistung an den Rand des Netzwerks
- Verlagern von Rechenleistung an den Ort der Datenentstehung

## Vorteile von Edge Computing

- Reduzierung der Latenz
- Reduzierung der Netzwerklast

## Was ist ein verteiltes System?

- Ein verteiltes System ist ein System, welches aus mehreren, räumlich verteilten Komponenten besteht, die über ein Netzwerk miteinander kommunizieren und gemeinsam eine Aufgabe erfüllen.

## Transparenzarten

- Zugriff -> wie wird auf Ressourcen zugegriffen
- Ort -> wo befindet sich die Ressource
- Migration -> wie wird die Ressource verschoben
- Relocation -> verbirgt das Verschieben der Ressource
- Replikation -> wie wird die Ressource repliziert
- Nebenläufigkeit -> wie wird mit konkurrierenden Zugriffen umgegangen
- Fehler -> wie wird mit Fehlern umgegangen (Wiederherstellung)

## Wie funktioniert die Namensauflösung (DNS)?

1. DNS Client sendet Anfrage an lokalen DNS Server
1. Lokaler DNS Server sendet Anfrage an Root DNS Server
1. Root DNS Server sendet Anfrage an TLD DNS Server
1. TLD DNS Server sendet Anfrage an Authoritative DNS Server
1. Authoritative DNS Server sendet Antwort an TLD DNS Server
1. TLD DNS Server sendet Antwort an Root DNS Server
1. Root DNS Server sendet Antwort an lokalen DNS Server
1. Lokaler DNS Server sendet Antwort an DNS Client

> DNS ist ein hierarchisches System, welches die Namensauflösung   von Domains in IP Adressen delegativ und rekursiv ermöglicht
{.is-info}

## Was ist Middleware?

Ein zwischengelagerter Dienst

## Was ist die Aufgabe des Layers 5 (Session)?

- Eröffnen, Aufrechterhalten und Schließen von Kommunikationsverbindungen

## Welche Schritte gehören zur Administration einer Session?

- Festlegen der Kommunikationspartner (Half Duplex, Full Duplex)
- Verbindungsaufbau
- Datenübertragung
- Verbindungsabbau

## Was ist die Aufgabe des Layers 6 (Presentation)?

- Datendarstellung, Codierung, Kompression...

## Wie können Daten in einer E-Mail verschlüsselt werden?

- S/MIME
- PGP

<!-- 
Es wird ein Bild von WireShark Dump gegeben in dem man FTP Steuer- und Datenkanal identifizieren und erklären muss.
Welche Ports wurden verwendet? -->
e
