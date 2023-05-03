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
