---
title: Graph Zusammenhänge
description: 
published: true
date: 2021-11-27T17:41:16.630Z
tags: graphen
editor: markdown
dateCreated: 2021-11-26T15:57:18.592Z
---

# Graph Zusammenhänge
## Zusammenhang ungerichteter Graph
**Zusammenhängend**: wenn zwischen je zwei verschiedenen Knoten mindestens ein Pfad existiert.

![zusammenhang-ungerichtet.png](/zusammenhang-ungerichtet.png)

## Zusammenhang gerichteter Graph
<u>stark</u> **zusammenhängend**: falls es für zwei Knoten A und B die folgenden Bedingungen wahr sind: 
- Es gibt mind. einen Pfad A -> ... -> B
- Es gibt mind. einen Pfad B -> ... -> A

<u>schwach</u> **zusammenhängend**: wenn wir alle gerichtete Kanten als ungerichtete Kanten interpretieren und nach dieser Interpretation der Graph ungerichtet zusammenhängend ist (siehe oben).

![schwach-zusammenhang-gerichtet.png](/schwach-zusammenhang-gerichtet.png)