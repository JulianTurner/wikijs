---
title: Graph Zusammenhänge
description: 
published: 1
date: 2022-03-04T12:46:58.787Z
tags: graphen
editor: markdown
dateCreated: 2021-12-16T20:41:45.376Z
---

# Graph Zusammenhänge
## Zusammenhang ungerichteter Graph
**Zusammenhängend**: wenn zwischen je zwei verschiedenen Knoten mindestens ein Pfad existiert.

![zusammenhang-ungerichtet.png](/fom/semester-1/formale-beschreibungsverfahren/zusammenhang-ungerichtet.png)

## Zusammenhang gerichteter Graph
<u>stark</u> **zusammenhängend**: falls es für zwei Knoten A und B die folgenden Bedingungen wahr sind: 
- Es gibt mind. einen Pfad A -> ... -> B
- Es gibt mind. einen Pfad B -> ... -> A

<u>schwach</u> **zusammenhängend**: wenn wir alle gerichtete Kanten als ungerichtete Kanten interpretieren und nach dieser Interpretation der Graph ungerichtet zusammenhängend ist (siehe oben).

![schwach-zusammenhang-gerichtet.png](/fom/semester-1/formale-beschreibungsverfahren/schwach-zusammenhang-gerichtet.png)