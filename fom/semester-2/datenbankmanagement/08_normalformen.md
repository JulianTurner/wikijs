---
title: Normalformen
description: 
published: 1
date: 2022-01-13T19:25:58.309Z
tags: 
editor: markdown
dateCreated: 2021-12-16T19:44:54.647Z
---

# Normalformen

## Welche Anomalien gibt es?
- Updateanomalie
- Löschanomalie
- Einfügeanomalie

> nicht passende Informationen wurden zusammen gespeichert

## Kriterien für Zerlegung
- Verlustlosigkeit (kein Verlust von Informationen)
	- Ausprägungen des alten Schemata sind im neuen Schemata rekonstruierbar
- Abhängigkeitstreue (kein Verlust von Metainformationen)
	- Funktionale Abhängigkeiten sind im neuen Schemata übertragbar

## Normalform - 1NF
- Werte sind atomar

Keine Mengen als Werte erlaubt


## Normalform - 2NF
- alles von 1NF
- nicht Schlüsselattribut ist vom Schlüsselkandidat funktional abhängig
- Attribut kann selbst Relation sein

## Normalform - 3NF
- kein Nichtschlüsselattribut vom Schlüsselkandidat funktional abhängig

## Normalform - BCNF
- Schlüssel überlappen nicht


# Datenintegrität
## Bedingungen 
- Erhaltung der Datenkonsistenz mit DBMS
- Konsistenzerhaltung nach Systemfehler

> Semantische Integritätsbestimmungen => Aus Eigenschaften der modellierten Miniwelt

## Statische / Dynamische Integritätsbestimmungen
Statische => immer erfüllt  
Dynamische => bei Zustandsänderung der Datenbank erfüllt

## Implizierte Anforderungen
- Schlüssel müssen innerhalb einer Relation eindeutig sein  
- Kardinalitäten werden eingehalten
- Inklusion bei Generalisierung (Untertyp ist in Obertyp enthalten)