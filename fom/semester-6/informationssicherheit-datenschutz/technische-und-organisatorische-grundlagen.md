---
title: Technische und organisatorische Grundlagen

published: 1
date: 2024-03-26T20:05:02.207Z
tags: 
editor: markdown
dateCreated: 2024-03-26T20:05:02.207Z
---

# Technische und organisatorische Grundlagen

## Daten und Informationen

- Werte und Befunde über Dinge, Ereignisse und Zustände,
- durch Beobachtung und Messung ermittelt
- durch Formulierung technisch festgehalten

Datenarten:

- Persönliche Daten
  - beziehen sich auf natürliche Personen
- Technische Daten
  - beziehen sich auf eine Sache
  - kann auch personenbezogenbezug haben

- Anonymisierte Daten
  - frei zugänglich
  - nach Stand der Technik nicht mehr auf Personen zurückführbar

![Daten](./daten.png)
![datenschutz-semiotik](datenschutz-semiotik.png)

## Abgrenzung IT-Sicherheit/Datenschutz

- betrifft nicht nur das Firmennetzwerk
  - IOT
  - Homeoffice
  - Smartphones
  - Cloud
- Informationssicherheit bezieht sich auf alle Daten im Unternehmen, nicht nur IT/Datenträger

IT-Sicherheit:

- Teilbereich der Schnittmenge von Cybersicherheit und Informationssicherheit

Datensicherheit setzt voraus:

- Vertraulichkeit
- Integrität
- Verfügbarkeit

It-Sicherheit:

- dient dem Interesse der verarbeitenden Stelle
- Schützt vor Verlust der Vertraulichkeit, Integrität und Verfügbarkeit
- Realisiert durch technische und organisatorische Maßnahmen
- Automatisierte Datenverarbeitung

Datenschutz:

- Dient dem Interesse der betroffenen
- Schützt vor Technik, Intransparenz und ungerechtfertigter Verkettung von Daten mit Personenbezug
- Realisiert durch IT-Sicherheitsmaßnahmen
- Alle Verarbeitungsarten

### Schutzziele von ISM & DSM

- ISMS (Informationssicherheitsmanagementsystem)
  - Betriebsgeheimnisse
  - Technische Daten
  - ...
- DSMS (Datenschutzmanagementsystem)
  - Transparenz
  - Intervenierbarkeit
  - Nicht-Verkettbarkeit
  - ...

> Gemeinsame Ziele: Integrität, Vertraulichkeit, Verfügbarkeit von personenbezogenen Daten
{.is-info}

### IT-Sicherheitsbeauftragter / Datenschutzbeauftragter

- IT-Sicherheitsbeauftragter
  - stimmt Sicherheitsziele ab
  - erstellt Leitlinien
- Datenschutzbeauftragter
  - Berater zur realisierung des Datenschutzes & Datensicherheit

Aufgaben:

- Überwachungspflicht
- ordnungsgemäße Anwendung der Datenverarbeitungsprogramme
- Einbinden in die Unternehmensprozesse & Entscheidungen
- Beratung und Schulung

## Schutzziele der IT-Sicherheit

[siehe Verteile Systeme](/fom/semester-4/verteilte-systeme/netzwerksicherheit.md#schutzziele-der-it-sicherheit)

Prinzipien für die Gewährleistung der Integrität und Vertraulichkeit

- Need-to-know-Prinzip -> nur so viele Berechnungen wie nötig
- Separation-of-Duties-Prinzip -> Trennung von Aufgaben um Manipulation zu verhindern
- Rotation-of-Duties-Prinzip -> Wechselnde Aufgabenverteilung um Ausfall kompensieren zu können

## Kryptographie

[siehe Verteile Systeme](/fom/semester-4/verteilte-systeme/netzwerksicherheit.md#kryptographie)

Ziele:

- Verschlüsselung um Vertraulichkeit zu gewährleisten
- Integritätsmaßnahmen um Veränderungen zu erkennen

> Kommunikation unter Verwendung geheimer Zusatzinformationen
{.is-info}

### Symmetrische Verschlüsselung

[siehe Verteile Systeme (symmetrische-verschlüsselung)](/fom/semester-4/verteilte-systeme/netzwerksicherheit.md#symmetrische-verschlüsselung)

### Asymmetrische Verschlüsselung

[siehe Verteile Systeme (asymmetrische-verschlüsselung)](/fom/semester-4/verteilte-systeme/netzwerksicherheit.md#asymmetrische-verschlüsselung)

### Hash- und Einwegfunktionen

[siehe Verteile Systeme (hash--einwegfunktionen)](/fom/semester-4/verteilte-systeme/netzwerksicherheit.md#hash--einwegfunktionen)

### Digitale Signaturen

[siehe Verteile Systeme (digitale-signaturen)](/fom/semester-4/verteilte-systeme/netzwerksicherheit.md#digitale-signaturen)

### Digitale Zertifikate

[siehe Verteile Systeme (digitale-zertifikate)](/fom/semester-4/verteilte-systeme/netzwerksicherheit.md#digitale-zertifikate)

### Hybridverschlüsselung

[siehe Verteile Systeme (hybridverschlüsselung)](/fom/semester-4/verteilte-systeme/netzwerksicherheit.md#hybridverschlüsselung)

### Diffie-Hellman

[siehe Verteile Systeme (diffie-hellman)](/fom/semester-4/verteilte-systeme/netzwerksicherheit.md#diffie-hellman)

Nachteile:

- Schützt nicht vor Man-in-the-Middle-Angriffen

### Perfect Forward Secrecy (PFS)

[siehe Verteilte Systeme (perfect forward Secrecy)](/fom/semester-4/verteilte-systeme/netzwerksicherheit.md#perfect-forward-secrecy-pfs)

### MAC (Message Authentication Code)

[siehe Verteilte Systeme (Mac)](/fom/semester-4/verteilte-systeme/netzwerksicherheit.md#mac-message-authentication-code)

## Datenverarbeitung und Technischorganisatorische Maßnahmen(TOMs)

### Datenumgang/Datenzweck

- Erheben -> Messen, Zählen, Wiegen
- Verarbeiten -> Speichern, Übermitteln, Löschen
- Nutzen -> Auswerten, Analysieren, Verwenden

### Pflichten des Verantwortlichen Stelle (DSGVO)

Ablauf:

1. Zweck muss festgelegt sein
1. Ermächtigungsgrundlage muss vorhanden sein
1. Datenerhebung
1. Datenverarbeitung
1. Datennutzung
1. Datenlöschung

> Transparente Informationen für Betroffene
{.is-info}

### Technischorganisatorische Maßnahmen (TOMs)

#### Vertraulichkeit

- Zutrittskontrolle -> kein unbefugter Zutritt
  - Zutrittsüberwachung mit:
    - Chipkarten
    - Schlüssel
    - Sicherheitszonen

- Zugangskontrolle -> keine unbefugte Systemnutzung
  - Benutzer-Identifikation und Authentifizierung mit:
    - automatischer Sperrmechanismus
    - Mehrfaktor-Authentifizierung
    - FIDO2
    - Verschlüsselung

- Zugriffskontrolle -> keine unbefugte Datenverwendung
  - Berechtigungskonzepte
  - Protokollierung von Zugriffen
  - funktionsgebundene Zugriffsschlüssel

[siehe verteilte Systeme (Netzwerksicherheit -> Sichere Architektur)](/fom/semester-4/verteilte-systeme/netzwerksicherheit.md#sichere-architektur)

- Datenträgerkontrolle -> kein unbefugtes verarbeiten von Datenträgern
  - Verschlüsselung
  - Verschlossenes aufbewahren
  - Protokollierung

#### Integrität

- Weitergabe-, Übertragungs- und Transportkontrolle -> kein unbefugtes verarbeiten von  beim Transport
  - Berechtigungsnachweis (Need-to-know-Prinzip)
  - Gegenseitige Überwachung (Separation of Duties-, Rotation of Duties Prinzip)
  - Vpn, Signatur

- Eingabekontrolle -> Feststellung und Nachvollziehbarkeit von Eingaben in Datenverarbeitungssysteme
  - Protokollierung
  - Nachweis der Quelle (Authentizität)
  - Versionierung

- Auftragskontrolle -> Weisungsgemäße Auftragsverarbeitung durch Dritte / Abgrenzung der Kompetenzen zwischen Auftraggeber und Auftragnehmer
  - eindeutige Vertragsgestaltung
  - formalisiertes Auftragsmanagement
  - Datenschutz- und IT-Sicherheitsaudits

- Verfügbarkeitskontrolle -> Schutz gegen zufällige oder vorsätzliche Zerstörung/Verlust
  - Backup
  - Firewall
  - Brandfrüherkennung

- Trennungsgebot -> Getrennte Verarbeitung von Daten, die unterschiedlich Erhoben wurden
  - Trennen von Produktions- und Testumgebung
  - getrennte Ordnerstrukturen
  - Sandboxen

- Wiederherstellbarkeit -> Schnelle Wiederherstellung von Systemen nach einer Störung
  - Schutzbedarfsfeststellungen
  - Notfallplan
  - Schulung

> Auftragsverarbeitungsverträge als rechtliches Rahmenwerk
{.is-info}
