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

<!-- TODO! bis Seite 325 -->