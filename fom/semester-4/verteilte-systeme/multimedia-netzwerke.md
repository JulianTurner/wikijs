---
title: Multimedia-Netzwerke
published: 1
date: 2023-05-03T20:40:01.207Z
tags: 
editor: markdown
dateCreated: 2023-05-03T20:40:01.207Z
---

# Multimedia-Netzwerke

- Streaming von Audio und Video
- Live-Streaming
- Interaktive Multimedia-Anwendungen

## Jitter (Verzögerungsschwankungen)

- Schwankung der Verzögerung zwischen Sender und Empfänger
- tolerant gegenüber Paketverlusten

> Kompression wandelt Bandbreite in Rechenleistung um
{.is-info}

## Streaming: UDP oder TCP?

UDP:

- Server sendet ohne Rücksicht auf überlast
- Senderate = Rate des Encoders (konstant)

> Kleiner Puffer um Jitter auszugleichen
{.is-info}

TCP:

- Datenrate = maximale Senderate der TCP-Verbindung
- schwankt aufgrund von Überlastkontrolle
- verzögerte Auslieferung durch Übertragungswiederholungen
- größere Puffer nötig
- Weniger Probleme mit Firewalls

## RTSP (Real-Time Streaming Protocol)

- Kontrollkanal für Befehle
- Datenkanal zur eigentlichen Übertragung
- Benutzer steuert Datenverbindung mit Befehlen

## HLS (HTTP Live Streaming)

- HTTP-Streaming
- Video wird in Schnipsel zerlegt und fortlaufend Nummeriert
- UTF-8 Playlist mit Links zu den Schnipseln

## VoIP (Voice over IP)

- kein konstanter Datenstrom (Teilung in Pakete, Segmente)
- maximale Verzögerung: 400ms
- Übertragung mit UDP
- Aufrechterhaltung einer konstanten Abspielgeschwindigkeit
  - jedes Sample hat Zeitstempel t
  - wird zum Zeitpunkt t + q (Verzögerung) abgespielt
  - wenn Sample nicht rechtzeitig ankommt, wird es verworfen
  - große Verzögerung -> weniger Pakete werden verworfen
  - kleinere Verzögerung -> höhere Interaktivität

> Sprachübertragung über IP-Netzwerke mit niedriger Latenz
{.is-info}

## Best Effort: Internet und Multimedia

Tricks um die Qualität zu verbessern:

- UDP verwenden um Überlastkontrolle von TCP zu umgehen
- Puffern auf Clientseite
- Medienströme mit verschiedenen Datenraten bereitstellen

Kompensationen von Fehlern:

- Übertragungswiederholungen
- zu niedriger Qualität wechseln

## RTP (Real-Time Transport Protocol)

- Standard für die Übertragung von Audio und Video
- Header beinhaltet Sequenznummer, Zeitstempel und Identifikation des Payloads
- wird über UDP übertragen
- stellt kein QoS sicher

## RTCP (Real-Time Transport Control Protocol)

- leichtgewichtiger Sitzungsprotokoll
- jeder Teilnehmer sendet regelmäßig RTCP-Pakete an alle anderen Teilnehmer

## SIP (Session Initiation Protocol)

- Telefonie und Videokonferenzen werden über Internet geleitet
- Identifikation der Teilnehmer über E-Mail-Adresse
- Erreichen des Kommunikationspartners unabhängig vom IP-Endgerät
- Aushandeln der Codierung
  - Sender schlägt Codierung vor
  - Empfänger wählt aus
  - Einigung auf beidseitig akzeptierte Codierung
- Möglichkeit zur Ablehnung von Anrufen
- Mediendaten können über RTP übertragen werden

![sip](/fom/semester-4/verteilte-systeme/sip.png)
