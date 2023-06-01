---
title: Klausurvorbereitung
published: 1
date: 2022-03-04T16:25:06.786Z
tags:
editor: markdown
dateCreated: 2022-03-04T12:23:19.207Z
---

# Klausurvorbereitung
<!-- 
Es wird ein Bild von WireShark Dump gegeben in dem man FTP Steuer- und Datenkanal identifizieren und erklären muss.
 -->
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

## Was ist die Aufgabe des Layers 7 (Application)?

- Bereitstellen von Diensten für Anwendungen
- Schnittstelle zwischen Benutzer und Computer, Client und Server

## Was macht das NTP?

- zentrale Zeitverwaltung im Netzwerk

## Wofür ist NTP wichtig?

- Kontrolle von zeitlicher Gültigkeit von Zertifikaten
- Synchronisation von Systemen

## Wie funktioniert die Namensauflösung (DNS) für die Domain de.wikipedia.org?

1. Client sucht in hosts Datei -> Falls nicht gefunden
1. Client fragt DNS Server -> Falls nicht gefunden
1. DNS Server fragt Root Server -> mit Anfrage nach de.wikipedia.org
1. Root Server antwortet mit IP Adresse des .org Nameservers
1. DNS Server fragt .org Nameserver -> mit Anfrage nach de.wikipedia.org
1. .org Nameserver antwortet mit IP Adresse des wikipedia.org Nameservers
1. DNS Server fragt wikipedia.org Nameserver -> mit Anfrage nach de.wikipedia.org
1. wikipedia.org Nameserver antwortet mit IP Adresse des de.wikipedia.org Nameservers
1. DNS antwortet mit IP Adresse von de.wikipedia.org

> DNS ist ein hierarchisches System, welches die Namensauflösung von Domains in IP Adressen delegativ und rekursiv ermöglicht
{.is-info}

## Was ist eine DNS Zone?

- Unterscheidung getrennt verwalteter Bereiche im DNS-Namespace
- ermöglicht präzise Steuerung der DNS-Komponenten, wie z.B. autoritative Nameserver
- Wird von einer Organisation / Administrator verwaltet wird
- Wird zur Delegation von Subdomains verwendet

## Was sind DNS Records?

- Eintrag in einem autoritativen DNS Server
- enthält Informationen über eine Domain -> IP Adresse, Mailserver, Nameserver, etc.

## Was ist DNSSEC?

- Erweiterung des DNS Protokolls
- ermöglicht Authentizität von DNS Daten
- verhindert DNS Spoofing

## Was ist Dynamic DNS?

- ermöglicht die automatische Aktualisierung von DNS Records zu einer dynamischen IP Adresse

## Ist IPv4 DNS mit IPv6 kompatibel?

- IPv4 und IPv6 sind nicht kompatibel
- IPv6 hat AAAA Records
- IPv4 hat A Records

## Was ist ein DNS Cache?

- Zwischenspeicher für DNS Anfragen

## Welche Arten von Records gibt es?

- A -> IPv4 Adresse
- AAAA -> IPv6 Adresse
- CNAME -> Alias für einen anderen Record
- MX -> Mailserver
- NS -> Nameserver
- PTR -> Reverse DNS
- TXT -> Text

## DNS Dump von Wireshark erklären

## Wie funktioniert FTP?

- FTP verwendet zwei Verbindungen -> Steuerkanal und Datenkanal

## Was ist der Unterschied zwischen FTPS und SFTP?

- FTPS ist FTP über SSL/TLS (Erweiterung von FTP)
- SFTP ist FTP über SSH (Erweiterung von SSH)

## Was ist der Unterschied zwischen aktiven und passiven FTP?

Aktives FTP:

- Steuerkanal vom Client
- Datenkanal vom Server
- kann durch Firewalls blockiert werden

Passives FTP:

- Steuerkanal vom Client
- Datenkanal vom Client
- alle Verbindungen werden vom Client aufgebaut

## Was ist SSH?

- verschlüsselter Konsolenzugriff
- Nachfolger von unverschlüsselten Telnet

## Wie funktioniert der SSL Handshake?

1. Client sendet Client Hello mit unterstützten Algorithmen
1. Server sendet Server Hello mit ausgewählten Algorithmen
1. Server sendet Zertifikat
1. Server sendet Hello Done
1. Server wartet auf Client Key Exchange
1. Client sendet Secret mit Server Public Key verschlüsselt
1. Client sendet Finished
1. Server antwortet Finished
1. Kommunikation wird mit symmetrischem Schlüssel verschlüsselt

## Wie funktioniert ein Zero Configuration Netzwerk?

- automatische Konfiguration von IP Adressen ohne DHCP
- auflösen von Hostnamen ohne DNS-Server
- finden von Diensten ohne Directory Server

z.B. Bonjour, AirDrop, AirPlay, AirPrint

## Was ist Freiraumdämpfung?

- mit zunehmender Entfernung nimmt die Signalstärke ab, dafür nimmt die Streuung zu

## Was ist Streuung?

- variable Reflexion des Signals an unebenen Objekten

## Was ist Überlagerung?

- verschiedene Signale stärken oder schwächen sich gegenseitig

## Was ist Abschattung?

- Abschirmung des Signals durch Hindernisse

## Was ist die Bit-Error-Rate?

- Anzahl der falsch empfangenen Bits im Verhältnis zur Gesamtzahl der empfangenen Bits

## Was ist der Signal-Rausch-Abstand?

- Abstand zwischen Signalen -> Hoher Abstand = Gute Trennbarkeit

## Was ist MSC, BSC?

- MSC -> Mobile Switching Center -> Vermittlungsstelle zwischen Mobilfunknetz und Festnetz, Zentrales Netzelement
- BSC -> Base Station Controller -> Zuständig für Steuerung der BTS z.B Handover
- BTS -> Base Transceiver Station -> Sendet und Empfängt Signale

## Wie funktioniert ein ausgehender Anruf im Mobilfunknetz (MOC)?

![MOC](/fom/semester-4/verteilte-systeme/moc.png)

1. MS sendet Verbindungsaufbauanforderung
1. BSC leitet Anforderung an MSC weiter
1. MSC prüft, ob Teilnehmer und Gerät berechtigt sind, die geforderten  Dienste in Anspruch zu nehmen (AUC, VLR, HLR)
1. Prüfung, ob genügend Ressourcen im GSM- und Festnetz verfügbar sind
1. MSC baut Verbindung zwischen MS (Mobile Station) und Festnetz auf

## Wofür braucht man 5g?

- geringere Latenz (IOT, Industrie 4.0)
- höhere Bandbreite (4k, 8k, VR, AR)

## Was ist der Nachteil von 5g?

- geringere Reichweite
- höherer Energieverbrauch

## Was ist MIMO?

- Multiple Input Multiple Output
- Mehrere Antennen senden und empfangen gleichzeitig

## Was zeichnet den Ad-Hoc Modus aus?

- Kein Access Point
- Direkte Kommunikation zwischen Geräten

## Was ist der Infrastruktur Modus?

- Datentransfer über Access Point
- Access Point dient als Brücke zum Netzwerk

## Welche WLAN Verschlüsselungen sind sicher?

WPA3
WPA2 mit AES

## Nenne weiterführende drahtlose Technologien

- LoRaWAN
- ZigBee
- Bluetooth
- NFC, RFID
- UWB

## Was ist der Unterschied zwischen NFC und RFID?

- RFID
  - One-Way Kommunikation (Read-Only)
  - RFID Tags können nicht (neu) beschrieben werden
- NFC
  - Zwei-Wege Kommunikation (Peer-to-Peer)
  - Senden und Empfangen von verschiedenen Daten

## Was ist der Unterschied zwischen indirektem und direktem Routing?

- Indirektes Routing
  - Adresse des Empfängers wird vom Foreign Agent and das Heimnetz des Empfängers gesendet
  - Sender sendet immer in Heimnetz des Empfängers
  - Heimnetz des Empfängers leitet an Empfänger weiter
  - Empfänger antwortet an eigenes Heimnetz
  - Heimnetz leitet an Sender weiter

- Direktes Routing (löst Dreiecksproblem)
  - Adresse des Empfängers wird vom Foreign Agent and das Heimnetz des Empfängers gesendet
  - Empfänger holt Adresse vom Heimnetz des Empfängers ab
  - Sender sendet Paket direkt an Empfänger
  - Empfänger sendet Paket direkt an Sender

## Was ist Jitter?

- variable Laufzeitverzögerung von Paketen im Netzwerk
- Empfang mit variabler Rate
- kann durch Pufferung ausgeglichen werden

## Was ist Streaming?

Client spielt Daten ab, während noch weitere Teile vom Server an den Client übertragen werden. z.B. Video Streaming

## Welche Streaming Arten gibt es?

- Best Effort Streaming
  - Keine Garantie für Verluste / Qualität / Verzögerung
  - verwenden Techniken auf der Anwendungsschicht um Verluste / Qualität / Verzögerung zu kompensieren
  - Puffern im Client
  - wechsel auf UDP
  - Kompression
  - Fehlerkorrektur
- RTP -> standardisiert Paketformat für Audio / Video Übertragung
- HLS ->

## Was ist RTP, RTSP und RTCP?

- RTP -> Real Time Protocol
  - Übertragung von Medieninhalten

- RTSP -> Real Time Streaming Protocol
  - Steuerung von Datenverbindung
  - z.B. Play, Pause, Stop

- RTCP -> Real Time Control Protocol
  - Übertragung von Steuernachrichten
  - Aushandlung und Einhaltung von Parametern der Dienstqualität
  
## Was ist der Unterschied zwischen SIP und VoIP?

- SIP -> Session Initiation Protocol
  - Aufbau und Abbau von Sitzungen
  - z.B. Telefonanruf
  - Verbindungsaufbau
  - Verbindungstrennung
  - Verbindungsaufrechterhaltung
  - Verbindungsumleitung

- VoIP -> Voice over IP
  - Übertragung von Sprache über IP Netzwerke
  - z.B. Telefonanruf
