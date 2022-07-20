---
title: SQL
description: 
published: 1
date: 2022-01-13T19:25:58.309Z
tags: 
editor: markdown
dateCreated: 2021-12-16T19:44:54.647Z
---

# SQL
Die Abarbeitung erfolgt über einen Parser und Anfragenoptimierer

## Einfache Abfrage


```sql	
SELECT * 
FROM professoren;
```

## Einfache Abfrage ohne Duplikate


```sql	
SELECT DISTINCT rang 
FROM professoren;
```

## Einfache Abfrage sortiert

```sql	
SELECT * 
FROM professoren
ORDER BY rang;
```

## Abfrage über mehrere Tabellen mit alias

```sql	
SELECT *
FROM professoren p, assistenten a
WHERE a.boss = p.persnr;
```

## Mengenoperationen

```sql
(
	SELECT *
	FROM studenten
	WHERE semester = 2
)
UNION
(
	SELECT *
	FROM studenten
	WHERE semester = 8
);
```

## Aggregatfunktionen

```sql
SELECT AVG(note) 
FROM pruefen;
```

> weitere Aggregatfunktionen:  
> avg() , count() , max() , min() , sum()

> count(*) zählt alle Elemente auch NULL

> count(attribute) zählt nur die Elemente die nicht NULL sind

## Gruppierung

```sql
SELECT count(*), semester
FROM studenten
GROUP BY semester;
```

> Filterung nach Gruppierung muss HAVING verwenden

> Filterung vor Gruppierung darf sich nicht auf Gruppierung beziehen und verwendet WHERE

## Geschachtelte Anfrage

```sql
SELECT name
FROM studenten
WHERE semester = (
	SELECT MAX(sSub.semester)
	FROM studenten sSub
);
```

## Abfrage mit Platzhalter

```sql
SELECT name
FROM studenten
WHERE name like 'X%nokrates';
```
> % = beliebig viele Zeichen (inkl. kein Zeichen)  
> _ = genau ein Zeichen


## Left Join

Alle Tupel meiner Ausgangstabelle mit den verknpüft mit den Tupeln aus der rechten Tabelle wo ON Bedingung erfüllt ist
 
```sql
SELECT *
FROM studenten s
LEFT JOIN pruefen p ON s.matrnr = p.matrnr;
```

![](/fom/semester-2/datenbankmanagement/sql_joins.png)
![](https://external-preview.redd.it/yOLzCR0qSzul2WpjQorxINB0xpU3_N9twmFVsgbGJwQ.jpg?auto=webp&s=4feedc91302ba635b3028a21b98d047def5cdc2b)