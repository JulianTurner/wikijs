---
title: Netzwerksicherheit
published: 1
date: 2023-05-10T20:05:17.207Z
tags: 
editor: markdown
dateCreated: 2023-05-10T20:05:17.207Z
---

# Netzwerksicherheit

## Schutzziele der IT-Sicherheit

- Vertraulichkeit
- Integrität
  - Nicht-Vermehrbarkeit
  - Beherrschbarkeit
  - Verlässlichkeit
- Verfügbarkeit

Neue Schutzziele:

- Transparenz
  - Zurechenbarkeit
  - Authentizität
  - Revisionssicherheit
- Kontingenz
  - Glaubhafte Abstreitbarkeit

### Vertraulichkeit

- Pseudonymität
- Anonymität
- Verdecktheit
- Unbeobachtbarkeit
- Nicht-Verfolgbarkeit
- Unverkettbarkeit

Umsetzung:

- Zugriffskontrolle
- Verschlüsselung
  
> Verhindern, dass vertrauliche/geheime Information für unberechtigte Dritte zugänglich wird
{.is-info}

#### Pseudonymität

- Schutz vor direkter Identifizierung
- Ähnlich wie Anonymität, aber mit Möglichkeit der Wiedererkennung mit Hilfe einer Zuordnungsregel

Umsetzung:

Personenbezogene Daten werden soweit verändert, dass sie ohne Zuordnungsvorschrift nicht mehr einem Individuum zugeordnet werden können.

#### Anonymität

- Zuordnung von Daten zu einer Person ist nicht möglich

Umsetzung:

- Kappen der Zuordnung von Daten zu bestimmten Personen

#### Verdecktheit und Unbeobachtbarkeit

- es ist nicht erkennbar, wer Daten sendet oder Empfängt
- Existenz der Kommunikation ist nicht erkennbar

Umsetzung:

- Steganographie

#### Unverkettbarkeit und Nicht-Verfolgbarkeit

- Ereignisse können nicht in Verbindung gebracht werden
- Informationsinhalte können keiner Person zugeordnet werden

Umsetzung:

- verschiedene Pseudonyme bei verschiedenen Dienstleistern

### Transparenz

#### Authentizität

- eindeutige und nachweisbare Echtheit von Objekten und Subjekten

Umsetzung:

- Passwörter
- Token
- digitale Signaturen

### Integrität

- keine unerlaubte & unbemerkte Veränderung von Daten

Umsetzung:

- Hashfunktionen
- digitale Signaturen
- MACs

### Verfügbarkeit

- Gewährleistung der Verfügbarkeit von Daten und Diensten

Umsetzung:

- Erkennung von Angriffen
- Redundanz
- Backups
- Ressourcenzuweisung

## Kryptographie

- Vertraulichkeit -> Lesen für andere unmöglich machen
- Authentifizierung -> Identitätsbeweise von Sender gegenüber Empfänger
- Integrität -> Manipulationen erkennen
- Verbindlichkeit -> Nachweis von unverändertem Inhalt

> Verschlüsselungs- und Entschlüsselungsverfahren sollten öffentlich sein
{.is-info}

### Symmetrische Verschlüsselung

- gleicher Schlüssel für Verschlüsselung und Entschlüsselung
- Herausforderung: Schlüsselaustausch

### Asymmetrische Verschlüsselung

- löst Problem des Schlüsselaustauschs
- jeder Teilnehmer hat einen öffentlichen und einen privaten Schlüssel
- basiert auf mathematischen Problemen, die in eine Richtung schwer zu lösen sind (multiplizieren von Primzahlen)
- Asymmetrie zwischen Quadrieren und Wurzelziehen bildet die Basis für Public-Key-Verfahren
- Sender verwendet Public-Key um Nachricht zu verschlüsseln
- Empfänger verwendet Private-Key um Nachricht zu entschlüsseln
- 1000x langsamer als symmetrische Verschlüsselung
- Verfahren:
  - RSA
  - Diffie-Hellman

### WLAN Verschlüsselung

- WEP -> unsicher
- WPA -> unsicher
- WPA2 -> EOL
- WPA3 -> aktuell

Authentifizierung:

- PSK -> Pre-Shared Key
- RADIUS

### Hash / Einwegfunktionen

- Ermittlung einer irreversiblen Prüfsumme
- Verwendung:
  - digitale Signaturen
  - Passwörter
  - Prüfsummen
  - Integritätssicherung

> AES256 ist sicher da symmetrisch, und quantencomputersicher
{.is-info}

### Digitale Signaturen

- kryptographisches Verfahren zur Prüfung der Authentizität von Inhalten

Ziele:

- Integrität -> Prüfung der Unversehrtheit
- Authentifikation -> Identitätsnachweis auf Authentizität (Echtheit) geprüft

#### Prozessablauf

Sender:  

  1. Hashwert der Nachricht berechnen
  2. Hashwert mit privatem Schlüssel verschlüsseln -> Signatur
  3. Nachricht und Signatur übertragen  

Empfänger:  

  4. Hashwert der Nachricht berechnen  
  5. Signatur mit öffentlichem Schlüssel entschlüsseln -> Hashwert  
  6. Hashwerte von Schritt 4 & 5 vergleichen

### Digitale Zertifikate

- gewährleisten Authentizität von öffentlichen Schlüsseln
- Zertifikate werden von vertrauenswürdigen Zertifizierungsstellen (CA) ausgestellt
- beglaubigen die Zusammengehörigkeit von öffentlichem Schlüssel und Identität (vergleichbar mit Notar)

#### Hybridverschlüsselung

> Kombination aus symmetrischer und asymmetrischer Verschlüsselung
{.is-info}

1. Generierung eines zufälligen symmetrischen Sitzungs-Schlüssels (Session-Key)
1. Verschlüsselung des Session-Keys mit dem öffentlichen Schlüssel des Empfängers
1. Übertragung des verschlüsselten Session-Keys
1. Empfänger entschlüsselt den Session-Key mit seinem privaten Schlüssel
1. Verschlüsselung aller Nachrichten mit dem Session-Key

Vorteile:

- schnelle symmetrische Verschlüsselung / Entschlüsselung
- sichere asymmetrische Schlüsselübertragung

Nachteile:

- Schlüsselaustausch notwendig
- anfällig gegen Man-in-the-Middle-Angriffe

Lösung: [Digitale Zertifikate](#digitale-zertifikate)

#### Zertifikatstypen

- Domain Validated (DV) -> Domaininhaber
- Organization Validated (OV) -> CA prüft Domaininhaber und Organisation
- Extended Validation (EV) -> CA prüft Domaininhaber, Organisation und Identität des Antragstellers

Arten:

- Class 1 -> Überprüfung der E-Mail
- Class 2 -> Überprüfung anhand von Dokumenten
- Class 3 -> Überprüfung der Person IRL

#### PKI (Public Key Infrastructure)

- Infrastruktur zur Erstellung, Verwaltung und Verteilung von Zertifikaten
- besteht aus:
  - Zertifizierungsstelle (CA)
  - Registrierungsstelle (RA)
  - Zertifikatssperrliste (CRL)

#### IKE (Internet Key Exchange)

- Protokoll zur sicheren Schlüsselverteilung
- verwendet Diffie-Hellman-Schlüsselaustausch
- PSK (Pre-Shared Key) oder Zertifikate zur Authentifizierung

### Diffie-Hellman

- asymmetrisches Schlüsselaustauschverfahren
- ermöglicht sicheren Schlüsselaustausch über unsichere Kanäle
- basiert auf mathematischen Problemen, die in eine Richtung schwer zu lösen sind (multiplizieren von Primzahlen)

#### Funktionsweise

1. Alice und Bob einigen sich auf 2 öffentliche Zahlen (p & g)
1. Alice wählt eine zufällige private Zahl (a) und berechnet öffentliches (A) -> $A = g^a \mod p$
1. Bob wählt eine zufällige private Zahl (b) und berechnet öffentliches (B) -> $B = g^b \mod p$
1. Alice und Bob tauschen öffentliche Schlüssel A, B aus
1. Alice berechnet gemeinsamen Schlüssel (K) -> $K = B^a \mod p$
1. Bob berechnet gemeinsamen Schlüssel (K) -> $K = A^b \mod p$

#### Perfect Forward Secrecy (PFS)

- verhindert das Entschlüsseln von Daten, falls der private Schlüssel kompromittiert wurde
- nach dem benutzen des Schlüssels wird dieser verworfen und es wird ein neuer erzeugt

### MAC (Message Authentication Code)

1. Nachricht und Schlüssel werden mit Hashfunktion gehasht
1. Hashwert wird mit Schlüssel verschlüsselt
1. MAC wird an Nachricht angehängt
1. Empfänger berechnet mit symmetrischem Schlüssel und Nachricht die MAC
1. Vergleich der MACs (empfangen, berechnet)

> Sind beide MACs identisch, ist die Nachricht unverändert (erhöht die Integrität)
{.is-info}

### DANE (DNS-Based Authentication of Named Entities)

- DNSSEC
  - eigene PKI für DNS
  - Antwort vom DNS-Server kann verifiziert werden
- Schwachstellen:
  - Zertifikatsaussteller
  - DNS Cache Poisoning
- DANE
  - Automatische Überprüfung der TLS-Zertifikate über DNS

## Angriffsvektoren und Szenarien

- Schatten-IT
- Social Engineering
- Phishing
- Personen in stressiger Lage neigen zu Fehlern

Arten von Angriffen:

- indirekte externe Angriffe -> Phishing, PDF
- Interne Angriffe -> Social Engineering, Bestechung
- Physische Angriffe -> Diebstahl, Manipulation
- Brute-Force
- Passwort Spraying -> Account und Passwort Kombinationen werden bei anderen Diensten ausprobiert
- OAuth Phishing -> Angriff auf OAuth Token

### Reconnaissance

- Finden von Angriffszielen, Sicherheitslücken und Schwachstellen

Passiv:

- verwenden von Informationen, die öffentlich zugänglich sind

Aktiv:

- aktives Scannen von Systemen und Netzwerken

> Menschliche Schwachstellen sind oft die größte Schwachstelle
{.is-info}

## Netzwerke sichern

Aufgaben Cloud Provider:

- physikalische Sicherheit
- Sicherheit der Infrastruktur

Aufgaben Cloud Nutzer:

- Sicherheit der Betriebsumgebung
- Backups und Wartungen
- Zugangskontrolle
- Monitoring und Logging (SIEM -> Security Information and Event Management)

### Sichere Architektur

- Client grundsätzlich nicht vertrauen
- WAF (Web Application Firewall) verwenden -> Prüfung von Anfragen und Antworten des Webservers
- Datenbank Firewall verwenden -> Prüfung von Datenbankanfragen

Zugriffskontrollen:

- Regelbasierte Zugriffskontrolle (MAC) -> Zugriff auf Objekte wird durch Regeln festgelegt (z.B. MAC-Adressen Filter)
- Discretionary Access Control (DAC) -> Zugriff auf Objekte wird durch den Eigentümer festgelegt (z.B. Dateiberechtigungen werden vom Ersteller vergeben)
- Rollenbasierte Zugriffskontrolle (RBAC) -> Zugriff auf Objekte wird durch Rollen festgelegt (z.B. Admin, User, Gast)
- Chinese Wall -> Zugriff auf Objekte wird durch die Zugehörigkeit zu einer Gruppe festgelegt (z.B. Mitarbeiter dürfen nur auf Daten von Kunden zugreifen, die nicht in Konkurrenz zueinander stehen)

### VPN (Virtual Private Network)

Anforderungen:

- Privates Netzwerk über öffentliches Netzwerk
- Verschlüsselung der Daten
- Datenintegrität sicherstellen
- Feststellen der Authentizität der Kommunikationspartner

Implementierung:

- Intranet VPN -> Verbindung zwischen zwei Standorten
- Extranet VPN -> Verbindung zwischen zwei Unternehmen
- Access VPN -> Verbindung von einem Client in bekanntest Netzwerk

Protokolle:

Layer 2:

- PPTP (Point-to-Point Tunneling Protocol) -> unsicher
- L2TP (Layer 2 Tunneling Protocol) -> unsicher

Höhere Ebenen:

- IPSec (Internet Protocol Security) -> sicher
- OpenVPN -> sicher
- S/MIME (Secure/Multipurpose Internet Mail Extensions) -> sicher
- PGP (Pretty Good Privacy) -> sicher
- TLS (Transport Layer Security) -> sicher

### Firewall

- Lösung, Sicherheitskonzept
- Zusammenstellung von Komponenten welche den Datenverkehr zentral kontrollieren
- Prüfung von Datenpaketen auf Basis von Regeln
- Paketfilter -> Prüfung von IP-Adressen und Ports
- Protokollieren, Alarmieren, Blockieren
- Schutz vor DoS (Denial of Service) und DDoS (Distributed Denial of Service) Angriffen
- Intrusion Detection System (IDS) -> Erkennen von Angriffen
- IP-Masquerading -> Kombination von PAT (Port Address Translation) und NAT (Network Address Translation) -> Verbergen von internen IP-Adressen
- FW-Regeln:
  - Verbindung
  - Bedingung
  - Limit/Trigger
  - Aktion
- DMZ (Demilitarized Zone) -> Netzwerksegment zwischen internem und externem Netzwerk
- Stateful Inspection -> Prüfung von Paketen auf Basis von Anfragen und Antworten

Herausforderung:

- Dynamische Portvergabe überwachen -> White- und Blacklisting, Deep Packet Inspection

NGFW (Next Generation Firewall):

- Muss nicht nur Pakete filtern, sondern auch Anwendungen erkennen
- Muss User und Geräte erkennen

### VLAN (Virtual Local Area Network)

- logische Aufteilung eines physischen Netzwerks
- layer 2

Geswitchtes VLAN:

- Paket wird bis auf Layer 2 ausgepackt
- VLAN-Tag wird geprüft
- Paket wird in das richtige VLAN gepackt
- Paket wird an entsprechenden Port weitergeleitet

Static VLAN:

- statische Zuordnung von Ports zu VLANs

Dynamic VLAN:

- dynamische Zuordnung mit Software
- VLAN Management Policy Server (VMPS) ordnen Geräte zu VLANs zu
- Port / Authentifizierungsbasiert

Vorteile:

- Abschottung von Netzen
- Segmentierung von Netzen
- Abhören von Datenpaketen in anderen VLANs nicht möglich
- Erhöhte Performance durch Broadcast-Reduktion

Angriffsvektoren:

- Überfluten mit MAC
- Ungesicherte Ports
- Angreifer kann sich als Root Switch ausgeben
