---
title: Rekursion
description: 
published: 1
date: 2022-01-13T19:25:58.309Z
tags: 
editor: markdown
dateCreated: 2021-12-16T19:44:54.647Z
---

# Rekursion

## Anmerkungen
- Iteration wird ausgeführt bis Fixpunkt erreicht ist (keine neuen Tupel)
- Anfrage muss monoton sein 
	- wenn neue Tupel hinzugefügt wurden, müssen mindestens die gleichen Tupel wie bei der ersten Iteration in der Ergebnismenge vorhanden sein
- SQL mit Rekursion ist Turing-vollständig
- Es kann nicht mehr garantiert werden, das SQL Anfragen terminieren

Beispiel:  Sucht alle Vorgänger zur Vorlesung 5052
```sql
WITH RECURSIVE TransitivVorl(Vorg, Nachf)
AS(
	SELECT vorgaenger, nachfolger
	FROM voraussetzen
	WHERE nachfolger = 5052
UNION
	SELECT DISTINCT v.vorgaenger, v.nachfolger
	FROM TransitivVorl t, voraussetzen v
	WHERE t.Vorg = v.nachfolger
)
SELECT * FROM TransitivVorl
```