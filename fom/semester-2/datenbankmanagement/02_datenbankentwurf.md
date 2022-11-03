---
title: Datenbankentwurf
description: 
published: 1
date: 2022-01-13T19:25:58.309Z
tags: 
editor: markdown
dateCreated: 2021-12-16T19:44:54.647Z
---

# Datenbankentwurf

## ER-Modell

![](https://image.jimcdn.com/app/cms/image/transf/dimension=576x10000:format=png/path/s834d64c225dfb243/image/i11975bc230269a82/version/1569885958/image.png)

### Was sind Entitäten?

Konzepte der zu modellierenden Welt

### Was sind Beziehungen?

Verknüpfung von Entitäten

### Was sind Attribute?

Eigenschaften einer Entität oder Beziehung

### Was sind Rollen?

Gerichtete Beschreibung einer Beziehung

### Was ist eine Schlüssel?

minimale Menge an Attributen die benötigt werden um ein Tupel eindeutig zu identifizieren

### Was sind funktionale Funktionalitäten?

Anzahl der Entitäten mit der eine Entität in Beziehung stehen kann
![](/fom/semester-2/datenbankmanagement/beziehungen.png)

### Wann ist eine Beziehung eine partielle Funktion?

- 1:1
- 1:N
- N:1

> Rechtseindeutig (injektiv)

### Was ist eine ternäre Beziehung?

Eine Beziehung zwischen 3 Entitäten

### Notation / Kardinalitäten für Beziehungen

- (min, max)
- 1:N

### Was ist eine schwache Entität?

- Existenz einer schwachen Entität hängt von einer übergeordneten Entität ab
- identifizierbar durch Schlüssel der übergeordneten Entität

Beispiel:  
Ohne Gebäude gibt es keinen Raum

### Was ist Generalisierung?

gemeinsame Eigenschaften werden zu einem Obertyp zusammengefasst

Beispiel:
Professor **ist ein** Angestellter  
Assistent **ist ein** Angestellter  

### Was is Aggregation?

Ist ein Teil von einer Entität

Beispiel:
Rahmen **ist Teil von** Fahrrad  
Rad **ist Teil von** Fahrrad  
