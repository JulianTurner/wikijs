---
title: Einführung
description: 
published: 1
date: 2022-01-13T19:25:58.309Z
tags: 
editor: markdown
dateCreated: 2021-12-16T19:44:54.647Z
---

# Einführung


## Nachteile von direkten Dateisystem
- Redundanz und Inkonsistenz durch verschiedene Dateiformate
- Eingeschränkter Zugriff
- Datenisolation
- Integritätsverletzung
- schlechter Mehrbenutzerbetrieb 
- Sicherheitsprobleme (Zugriffskontrolle nur auf ganze Dateien)
- Dateiverwaltung (muss immer neu implementiert werden)

## Was bedeutet DBMS?
Datenbankmanagement System

## Abstraktionsebenen
![](/fom/semester-2/datenbankmanagement/datenebene.png)

### Physische Ebene
Werden die Daten auf einem physischen Medium gespeichert.
> Physische Datenunabhängigkeit => ändern der physischen Speicherstruktur ohne ändern der logischen Ebene
### Logische Ebene
Welche Daten werden gespeichert  
Welche Beziehung haben Daten zueinander
> Logische Datenunabhängigkeit: Anwendung sind bei geringfügigen Änderungen nicht betroffen 

### Sichten
Darstellung der Daten für Anwendungen

## Datenbankschema & Ausprägungen
Datenbankschema:
- Beschreibt Datenbankdesign auf logischer Ebene
- ändert sich selten

Ausprägungen:
- Momentaufnahme der Daten 
- ändert sich häufig

## Welche Teilsprachen gibt es?
- Datendefinitionssprache (DDL) z.B. CREATE, DROP, ALTER
- Datenmanipulationssprache (DML) z.B. INSERT, UPDATE, DELETE

> SQL dient beide Sprachen

## Anforderungen an das relationale Datenmodell
- einheitliche Verwaltung der Daten
- sichern, suchen, ändern
- Zugriff auf Datenbeschreibung
- Nutzersichten
- Zugriffskontrolle

moderne Relationale DBMS: 
- DDL, DML
- Einbettung in Programmiersprachen
- Mehrbenutzerbetrieb

Beispiele:
PostgreSQL, MySQL, SQLite, Oracle, Microsoft SQL Server

## Wie funktioniert DDL?
- DDL Compiler erstellt Metadaten
- Metadaten werden im Datenwörterbuch (Dictionary) gespeichert
	- Datenbankschema
	- Integritätsbedingungen z.b. Primärschlüssel
	- Zugriffsrechte

```sql	
CREATE TABLE person (
	id INTEGER PRIMARY KEY AUTOINCREMENT,
	name VARCHAR(255),
	age INTEGER
);
```

## Wie funktioniert DML?
- Zugriff und Manipulation der Daten

```sql
INSERT INTO person (name, age) VALUES ('Max', 30);
```	

> SQL ist deklarativ (wird beschrieben was man haben möchte)
## Was ist ein Objekt-relationales Datenmodell?
- Konzept aus der objektorientierten Datenmodellierung
> Modell ist "flach" und wird um zusätzliche Datentypen erweitert

## Was zeichnet XML aus?
- Semistrukturiert 
- war für Textauszeichnung gedacht - hält overhead klein

## Warum NoSQL?
- horizontale Skalierung
- kurz Laufzeit der Anfragen
- einfaches Schema mit großen Datenmengen
- geringe Anforderungen an die Konsistenz

## Was sind NoSql Kernsysteme?
- Key-Value-Store
- Document-Store
- Wide-Column-Store
- Graph-Store

